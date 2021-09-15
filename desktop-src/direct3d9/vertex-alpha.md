---
description: Los datos alfa se pueden proporcionar en los datos de vértice. Para habilitar el alfa de vértices, establezca D3DRS \_ DIFFUSEMATERIALSOURCE en D3DMCS COLOR1 para que el tiempo de ejecución de Direct3D tome el valor difuso del color difuso en lugar del \_ material.
ms.assetid: 2b0d842d-ee7d-4633-846d-96697153adc7
title: Vértice alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f661c013e324a0bf209b4faca41d1974a41e81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580120"
---
# <a name="vertex-alpha-direct3d-9"></a>Vértice alfa (Direct3D 9)

Los datos alfa se pueden proporcionar en los datos de vértice. Para habilitar el alfa de vértices, establezca D3DRS \_ DIFFUSEMATERIALSOURCE en D3DMCS COLOR1 para que el tiempo de ejecución de Direct3D tome el valor difuso del color difuso en lugar del \_ material.


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE,  
                                D3DMCS_COLOR1 );
```



A continuación, proporcione valores alfa en el color difuso. La función AddAlphaToASphere agrega alfa a los vértices de una esfera. Este es un ejemplo de cómo proporcionar la información alfa a la función.


```
AddAlphaToASphere( m_pObstacleVertices, 12,  
                    D3DRGBA(light.dcvDiffuse.r, light.dcvDiffuse.g, 
                            light.dcvDiffuse.b, vAlpha ));
```



Este es el aspecto de la función.


```
 
void AddAlphaToASphere(D3DLVERTEX* pVertices, DWORD dwNumRings, D3DCOLOR lightcolor)
{
    WORD x, y;
    // rings around
    for( y=0; y < dwNumRings; y++ )
        for( x=0; x < (dwNumRings*2)+1; x++ )
            (pVertices++)->color = lightcolor;

    // top and bottom
    (pVertices++)->color = lightcolor;
    (pVertices++)->color = lightcolor;
}
```



AddAlphaToASphere simplemente modifica el miembro de color de cada vértice, que es de tipo D3DLVERTEX, para incluir la información alfa.

D3DLVERTEX tiene este aspecto.


```
 
// Lit vertex
typedef struct {
    D3DVALUE x, y, z;
    DWORD dwReserved;
    D3DCOLOR color, specular;
    D3DVALUE tu, tv;
} D3DLVERTEX, *LPD3DLVERTEX;
```



Dibujar la esfera,


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

//...

// Draw the lit sphere
m_pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, D3DFVF_LVERTEX,
                                    m_pObstacleVertices, m_dwNumObstacleVertices,
                                    m_pObstacleIndices,  m_dwNumObstacleIndices, 0 );
```



da como resultado una esfera transparente mediante vértice alfa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Alpha Blending](alpha-blending.md)
</dt> </dl>

 

 



