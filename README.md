# PSSR_docker

## Current usage
`docker run -v ${DIR_WITH_TIF}:/data/test/PSSR/stats -v ${DIR_MODELS}:/data/test/PSSR/models jawon/pssr:0.0.0 ${PWD} ${MODEL_FILE_NAME} ${SIZE}`

### Example
`docker run -v ${DIR_WITH_TIF}:/data/test/PSSR/stats -v ${DIR_MODELS}:/data/test/PSSR/models jawon/pssr:0.0.0 . PSSR_for_EM_1024.pkl 1024`

`singularity exec --cleanenv --nv pssr_0.0.0.sif /usr/local/bin/entrypoint.sh python /data/inference.py $WORKDIR $modelf $size`
