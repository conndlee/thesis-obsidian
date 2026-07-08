rough sections

Lit review
	how can we do this lol
	lots of stuff not relevant anymore...
	
Background 
	OSB simulator
		digital twin
			velocity based damping
			deformable body
	Modelling kinematics (DH, FK/IK solver, Neural Network (ctr?))
		missing orientation control here.
	Optical flow/etc
Work 
	Soft-body implementation in sim
	Surgeon Study (evaluating fetal tools/preliminary feedback on control)
		note that orientation control etc
		design and improvement of fetal-maternal model
		improvement of simulators (virtual training, physical performance)
	Tool tracking 
		initially, seemed like position was incorrect using older methods of alignment (naive).
		next, we implement cross-correlation and dynamic time warping, for coarse and fine adjustment in time alignment (coming from different sensors) using velocity signal (speeds are frame invairant)
		next, solve double wabha's problem using kasbch solver (EM emitter frame mismatch with PSM frame + EM sensor frame mismatch with tool frame)
		actually reduces much of the forward kinematics error for POSITION
		(turns out MTMR/PSM1 encoders -> forward kinematics model is reliable for position. however, we still observe orientation mismatch by 30-50 degrees.)
		sections: Encoder only, camera, kalman filter/neural network
		predicting orientation 
	