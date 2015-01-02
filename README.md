Image_label_Evaluation
======================
Tested under ubuntu 12.04 & matlab 2013b 
Running the code: 
        For simple testing prupose: 
                First run your algorithm over the 'test' set (Check in DemoAnalysis & PathDefine): 
                    imgset = 'test';
                    imgnames = textread([pathImgset,imgset,'.txt'],'%s'); 
                Run this analysis code: 
                    Modify the 'pathRes' in PathDefine to point at your predicted results.  Check our results for example.
                    Run DemoAnalysis to analysis the results. 
            In this test case, we have already computed error factor for each ground truth instance saved. We just load the groud truth and recompute the IOU. 
        
        Re-extract error factors: 
            We have precomputed segments (through UCM [5]), o2p appearance model [4], the detection results from HOG DPM [6] (both whole object & parts) available at:  
                to facility the computation. (You can also compute them yourself by using the original author's code.)
            Because it is very large, if you need you may download from this Link 
                
            You may use other feature (CNN) for measure appearance and shape of the objects. Check Sec: Change. 

Source of Data: 
	Data are from the following papers.  I used a beta version of data [1] & [2]. For Pascal 3D we use the one from [3].  
    We attach all the data to facility running of the code in zip file.  Simply unzip to the existing directory. 

Change: 
	For modeling appearance and shape, you may use any other strategies to model it other than o2p, simply write your functions for : getAppearanceErrFac  & getShapeErrFac

Any questions, you may contact : jerryking234@gmail.com


[1] X. Chen, R. Mottaghi, X. Liu, N.-G. Cho, S. Fidler, R. Urtasun, and A. Yuille. Detect what you can: Detecting and representing objects using holistic models and body parts. In CVPR, 2014.
[2] R. Mottaghi, X. Chen, X. Liu, S. Fidler, R. Urtasun, and A. Yuille. The role of context for object detection and semantic segmentation in the wild. In CVPR, 2014.
[3] Y. Xiang, R. Mottaghi, and S. Savarese. Beyond pascal: A benchmark for 3d object detection in the wild. In WACV, 2014.
[4] J. Carreira, R. Caseiro, J. Batista, and C. Sminchisescu. Semantic segmentation with second-order pooling. In ECCV (7), pages 430–443, 2012.
[5] P. Arbelaez, M. Maire, C. Fowlkes, and J. Malik. Contour detection and hierarchical image segmentation. In TPAMI, pages 898–916, 2011.
[6] P. F. Felzenszwalb, R. B. Girshick, and D. A. McAllester. Cascade object detection with deformable part models. In CVPR, pages 2241–2248, 2010.
