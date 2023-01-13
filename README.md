# TensorflowCustomObjectDetection
 
![daisy_38](https://user-images.githubusercontent.com/80906568/212358417-d64b90f4-6941-476f-a67b-b1494ba62757.png)
![dandelion_50](https://user-images.githubusercontent.com/80906568/212358431-d2d21eda-78cf-4fe7-8ca6-40bc86fa49d8.png)
![rose_114](https://user-images.githubusercontent.com/80906568/212358451-16f67bee-a1cc-47d0-b1ff-1b6e372811d4.png)


![tulip_67](https://user-images.githubusercontent.com/80906568/212358582-9b8dd887-b6ab-49ae-bfd3-ae65ea51b270.png)
![magnolia](https://user-images.githubusercontent.com/80906568/212358585-206db59b-cee3-4dcd-a367-ab9bd4408009.png)
![water_lily_201](https://user-images.githubusercontent.com/80906568/212358639-f7f5dff4-d3aa-4b81-9b0e-f27f8b152610.png)

## Run
After the installation and labelling;

### Create tfrecord files
cd training_demo
python generate_tf_record.py -x images/train -l annotations/label_map.pbtxt -o annotations/train.record

python generate_tf_record.py -x images/test -l annotations/label_map.pbtxt -o annotations/test.record

### Train
python model_main.py --alsologtostderr --model_dir=training/ --pipeline_config_path=training/ssd_inception_v2_coco.config

### Save model as pb
python export_inference_graph.py --input_type image_tensor --pipeline_config_path training/ssd_inception_v2_coco.config --trained_checkpoint_prefix training/model.ckpt-13302 --output_directory trained-inference-graphs/output_inference_graph_v1.pb






## Resources
https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/install.html
