---
description: Las texturas también pueden proporcionar valores alfa.
ms.assetid: b9f53783-d4d8-4339-8cf3-5ad8305ff627
title: Textura alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694f8a72d3faede36c3e69ce1b6841b8f6450a3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666155"
---
# <a name="texture-alpha-direct3d-9"></a>Textura alfa (Direct3D 9)

Las texturas también pueden proporcionar valores alfa. En primer lugar, se debe crear la textura. En segundo lugar, los valores alfa se deben agregar a la textura. Para representar con la textura, establezca la textura en una fase de textura y seleccione la operación de fase de textura y los operandos adecuados. Cuando se llama a Draw, el primitivo se representará con transparencia. En este ejemplo se crea un recurso de textura y, a continuación, se carga el canal alfa.


```
LPDIRECT3DTEXTURE9 m_pTexture;

// Create an alpha texture
D3DXCreateTexture(m_d3dDevice, 128, 128, 0, D3DUSAGE_RENDERTARGET, 
    D3DFMT_A8R8G8B8, D3DPOOL_MANAGED, &m_pTexture);

// Initialize the alpha channel
int  yGrad, xGrad;
D3DLOCKED_RECT lockedRect;

if(SUCCEEDED(pTexture->LockRect(0, &lockedRect, NULL, D3DLOCK_DISCARD )))
{
    m_pRGBAData = new DWORD[128*128];
    if( m_pRGBAData != NULL )
    {
        for( DWORD y=0; y < m_dwHeight; y++ )
        {   
            DWORD dwOffset = y*m_dwWidth;
            yGrad = (int)(((float)y/(float)m_dwWidth) * 255.0f);
            
            for( DWORD x=0; x < m_dwWidth; x )
            {
                xGrad = (int)(((float)x/(float)m_dwWidth) * 255.0f);

                DWORD b = (DWORD)(xGrad + (255 - yGrad))/2 & 0xFF;
                DWORD g = (DWORD)((255 - xGrad) + yGrad)/2 & 0xFF;
                DWORD r = (DWORD)(xGrad + yGrad)/2 & 0xFF;
                DWORD a = (DWORD)(xGrad + yGrad)/2 & 0xFF;

                lockedRect.pBits[dwOffset+x] = ((a<<24L)+(r<<16L)+(g<<8L)+(b));
                x++;
            }
        }
    }
    pTexture->UnlockRect(&lockedRect);
}
```



El valor alfa se calcula en función de la posición de x/y relativa del píxel actual dentro del tamaño de la textura. A continuación, asigne la textura a una fase de textura y configure la fase de textura.


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

// Assign texture
m_pd3dDevice->SetTexture(0, m_pTexture);

// Texture stage states
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);  

m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE);

m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE);
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG2, D3DTA_DIFFUSE);

m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAOP, D3DTOP_MODULATE);

```



Esto da como resultado un primitivo con un degradado de transparencia. El degradado es transparente, donde x = 0 y opaco, donde x es su valor máximo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación alfa](alpha-blending.md)
</dt> </dl>

 

 



