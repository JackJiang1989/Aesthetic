---
title: Welcome to my blog
---


https://openfoamwiki.net/index.php/Write_OpenFOAM_meshes \
https://www.cfd-online.com/Forums/openfoam/95858-owner-neighbor.html \
https://openfoam.top/fvMesh/ \
https://openfoamwiki.net/index.php/Owner_and_neighbour_indices \



owner and neibour

> fvmesh frequently used methods
> ```
> //- Return cell volumes
> const DimensionedField<scalar, volMesh>& V() const;
> //- Return old-time cell volumes
> const DimensionedField<scalar, volMesh>& V0() const;
> //- Return old-old-time cell volumes
> const DimensionedField<scalar, volMesh>& V00() const;
> //- Return sub-cycle cell volumes
> tmp<DimensionedField<scalar, volMesh>> Vsc() const;
> //- Return sub-cycl old-time cell volumes
> tmp<DimensionedField<scalar, volMesh>> Vsc0() const;
> //- Return cell face area vectors
> const surfaceVectorField& Sf() const;
> //- Return cell face area magnitudes
> const surfaceScalarField& magSf() const;
> //- Return cell face motion fluxes
> const surfaceScalarField& phi() const;
> //- Return cell centres as volVectorField
> const volVectorField& C() const;
> //- Return face centres as surfaceVectorField
> const surfaceVectorField& Cf() const;
> ```
> 

>
    //- Internal face owner
    const labelUList& owner() const
    {
        return lduAddr().lowerAddr();
    }
    //- Internal face neighbour
    const labelUList& neighbour() const
    {
        return lduAddr().upperAddr();
    };

show how ower and neighbour looks like: \
<img src="https://github.com/JackJiang1989/Aesthetic/assets/16970448/efe0359d-5d8d-4d63-8e67-934f3b496652" alt="drawing" width="400"/>
<img src="https://github.com/JackJiang1989/Aesthetic/assets/16970448/3dbac2d5-1be8-4a1f-aceb-15d8c91ab2e0" alt="drawing" width="400"/>
<img src="https://github.com/JackJiang1989/Aesthetic/assets/16970448/306218cb-5b93-44b7-8364-ae94a68d296a" alt="drawing" width="400"/>




