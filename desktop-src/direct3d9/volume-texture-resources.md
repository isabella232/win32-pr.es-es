---
description: Las texturas de volumen son colecciones tridimensionales de píxeles (textura) que se pueden usar para pintar un primitivo bidimensional, como un triángulo o una línea.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Recursos de textura de volumen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c66ff97d04e3c7c6c0a032f9a230dfd511b38c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564695"
---
# <a name="volume-texture-resources-direct3d-9"></a>Recursos de textura de volumen (Direct3D 9)

Las texturas de volumen son colecciones tridimensionales de píxeles (textura) que se pueden usar para pintar un primitivo bidimensional, como un triángulo o una línea. Se requieren coordenadas de textura de tres elementos para cada vértice de una primitiva que se va a texturar con un volumen. A medida que se dibuja el primitivo, cada píxel contenido se rellena con el valor de color de algún píxel dentro del volumen, de acuerdo con las reglas análogas al caso de textura bidimensional. Los volúmenes no se representan directamente porque no hay primitivas tridimensionales que se puedan pintar con ellos.

Puede usar texturas de volumen para efectos especiales como la niebla de revisión, las explosiones, etc.

Los volúmenes se organizan en segmentos y se pueden considerar como superficies 2D de alto ancho x apiladas para crear un volumen x alto x de profundidad. Cada segmento es una sola fila. Los volúmenes pueden tener niveles posteriores en los que las dimensiones de cada nivel se truncan a la mitad de las dimensiones del nivel anterior. En el diagrama siguiente se muestra el aspecto de una textura de volumen con varios niveles.

![diagrama de una textura de volumen con representaciones de cubo 8x2x4, 4x1x2 y 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a>Crear una textura de volumen

En los ejemplos de código siguientes se muestran los pasos necesarios para usar una textura de volumen.

En primer lugar, especifique un tipo de vértice personalizado que tenga tres coordenadas de textura para cada vértice, tal como se muestra en este ejemplo de código.


```
struct VOLUMEVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu, tv, tw;
};

#define D3DFVF_VOLUMEVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|
                             D3DFVF_TEX1|D3DFVF_TEXCOORDSIZE3(0))
```



A continuación, rellene los vértices con datos.


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



Ahora, cree un búfer de vértices y rellénelo con los datos de los vértices.

El siguiente paso consiste en usar el método [**IDirect3DDevice9:: CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) para crear una textura de volumen, tal como se muestra en este ejemplo de código.


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



Antes de representar el primitivo, establezca la textura actual en la textura de volumen creada anteriormente. En el ejemplo de código siguiente se muestra todo el proceso de representación de una franja de triángulos.


```
if( SUCCEEDED( d3dDevice->BeginScene() ) )
{
    // Draw the quad, with the volume texture.
    d3dDevice->SetTexture( 0, pVolumeTexture );
    d3dDevice->SetFVF( D3DFVF_VOLUMEVERTEX );
    d3dDevice->SetStreamSource( 0, pVB, sizeof(VOLUMEVERTEX) );
    d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 2);

   // End the scene.
   d3dDevice->EndScene();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
