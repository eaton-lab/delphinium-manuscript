
# ran tetrad on delphinium min4 unlinked SNPs on pinky to get qrt scores
tetrad quartets DATA.snps.hdf5 -w . -n Delph --subsample -c 40 

# infer QMC supertrees under weights (0, 1, 2, 3) and infer consensus trees
tetrad consensus Delph.json -c 40 -w 0 >
tetrad consensus Delph.json -c 40 -w 1 >
tetrad consensus Delph.json -c 40 -w 2 >
tetrad consensus Delph.json -c 40 -w 3 > 

# infer quartet concordance statistics
tetrad concordance Delph.json -c 40 >
tetrad concordance Delph.json -c 40 > 
