---
description: Las texturas de volumen son colecciones tridimensionales de píxeles (texturas) que se pueden usar para pintar una primitiva bidimensional, como un triángulo o una línea.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Recursos de textura de volumen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17e72448fd1fd4856cf81a344f5c176fdb6272546468126975edbff8b20218d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984365"
---
# <a name="volume-texture-resources-direct3d-9"></a>Recursos de textura de volumen (Direct3D 9)

Las texturas de volumen son colecciones tridimensionales de píxeles (texturas) que se pueden usar para pintar una primitiva bidimensional, como un triángulo o una línea. Las coordenadas de textura de tres elementos son necesarias para cada vértice de un primitivo que se va a texturar con un volumen. A medida que se dibuja la primitiva, cada píxel contenido se rellena con el valor de color de algún píxel dentro del volumen, de acuerdo con reglas análogas al caso de textura bidimensional. Los volúmenes no se representan directamente porque no hay primitivas tridimensionales que se puedan pintar con ellos.

Puede usar texturas de volumen para efectos especiales, como parches, explosións, y así sucesivamente.

Los volúmenes se organizan en segmentos y se pueden pensar en superficies 2D de ancho x alto apilados para crear un ancho x alto x volumen de profundidad. Cada segmento es una sola fila. Los volúmenes pueden tener niveles posteriores en los que las dimensiones de cada nivel se truncan a la mitad de las dimensiones del nivel anterior. En el diagrama siguiente se muestra el aspecto de una textura de volumen con varios niveles.

![diagrama de una textura de volumen con representaciones de cubo de 8x2x4, 4x1x2 y 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a>Crear una textura de volumen

En los ejemplos de código siguientes se muestran los pasos necesarios para usar una textura de volumen.

En primer lugar, especifique un tipo de vértice personalizado que tenga tres coordenadas de textura para cada vértice, como se muestra en este ejemplo de código.


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



Ahora, cree un búfer de vértices y llénlo con datos de los vértices.

El siguiente paso consiste en usar el método [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) para crear una textura de volumen, como se muestra en este ejemplo de código.


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



Antes de representar la primitiva, establezca la textura actual en la textura del volumen creada anteriormente. En el ejemplo de código siguiente se muestra todo el proceso de representación de una franja de triángulos.


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

 

 
