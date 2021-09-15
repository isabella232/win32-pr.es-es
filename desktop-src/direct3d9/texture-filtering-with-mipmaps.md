---
description: Un mapa mip es una secuencia de texturas, cada una de las cuales es una representación de resolución progresivamente inferior de la misma imagen.
ms.assetid: b64abca9-0efb-4939-849d-e75a8d0dc10b
title: Filtrado de texturas con mapas Mip (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc109ae6de93a26b5d5e5b90e948761e92ee92c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465653"
---
# <a name="texture-filtering-with-mipmaps-direct3d-9"></a>Filtrado de texturas con mapas Mip (Direct3D 9)

Un mapa mip es una secuencia de texturas, cada una de las cuales es una representación de resolución progresivamente inferior de la misma imagen. El alto y ancho de cada imagen, o nivel, en el mapa mip es una potencia de dos menores que el nivel anterior. Los mapas Mip no tienen que ser cuadrados.

Se usa una imagen mipmap de alta resolución para los objetos que están cerca del usuario. Las imágenes de menor resolución se usan cuando el objeto aparece más lejos. Mipmapping mejora la calidad de las texturas representados a costa de usar más memoria.

Direct3D representa mapas MIP como una cadena de superficies adjuntas. La textura de resolución más alta está en la parte superior de la cadena y tiene el siguiente nivel de mipmap como datos adjuntos. A su vez, ese nivel tiene un dato adjunto que es el siguiente nivel del mapa mip, y así sucesivamente, hasta el nivel de resolución más bajo del mapa mip.

En las ilustraciones siguientes se muestra un ejemplo de estos niveles. Las texturas de mapa de bits representan un signo en un contenedor en un juego en 3D en primera persona. Cuando se crea como un mapa mip, la textura de resolución más alta es la primera del conjunto. Cada textura correcta del conjunto de mapas mipmap es más pequeña en alto y ancho por una potencia de 2. En este caso, el mapa mip de resolución máxima es de 256 píxeles por 256 píxeles. A continuación, la textura es 128 x 128. La última textura de la cadena es 64 x 64.

Este signo tiene una distancia máxima desde la que está visible. Si el usuario comienza lejos del signo, el juego muestra la textura más pequeña de la cadena mipmap, que en este caso es la textura 64x64.

![ilustración de una textura de 64 x 64 de un signo de peligro](images/mip1.jpg)

A medida que el usuario mueve el punto de vista más cerca del signo, se usan texturas de mayor resolución progresivamente en la cadena mipmap. La resolución de la ilustración siguiente es 128 x 128.

![ilustración de una textura de 128 x 128 de un signo de peligro](images/mip2.jpg)

La textura de resolución más alta se usa cuando el punto de vista del usuario está a la distancia mínima posible del signo, como se muestra en la ilustración siguiente.

![ilustración de una textura de 256 x 256 de un signo de peligro](images/mip3.jpg)

Se trata de una manera más eficaz de simular la perspectiva de las texturas. En lugar de representar una sola textura a muchas resoluciones, es más rápido usar varias texturas con distintas resoluciones.

Direct3D puede evaluar qué textura de un conjunto de mapas mip es la resolución más cercana a la salida deseada y puede asignar píxeles a su espacio de textura. Si la resolución de la imagen final se encuentra entre las resoluciones de las texturas del conjunto de mapas mip, Direct3D puede examinar los elementos de textura en ambos mapas mipmap y combinar sus valores de color.

Para usar mapas mip, la aplicación debe compilar un conjunto de mapas mip. Las aplicaciones aplican mapas mip seleccionando el conjunto de mapas mip como la primera textura del conjunto de texturas actuales. Para obtener más información, vea [Mezcla de textura (Direct3D 9).](texture-blending.md)

A continuación, la aplicación debe establecer el método de filtrado que usa Direct3D en los elementos de textura de ejemplo. El método más rápido de filtrado de mapas mip es hacer que Direct3D seleccione el elemento de textura más cercano. Use el valor enumerado D3DTEXF \_ POINT para seleccionarlo. Direct3D puede producir mejores resultados de filtrado si la aplicación usa el valor enumerado linear \_ D3DTEXF. Esto selecciona el mapa mip más cercano y, a continuación, calcula un promedio ponderado de los elementos de textura que rodean la ubicación en la textura a la que se asigna el píxel actual.

Las texturas mipmap se usan en escenas 3D para reducir el tiempo necesario para representar una escena. También mejoran el realismo de la escena. Sin embargo, a menudo requieren grandes cantidades de memoria.

## <a name="creating-a-set-of-mipmaps"></a>Creación de un conjunto de mapas Mip

En el ejemplo siguiente se muestra cómo la aplicación puede llamar al método [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) para compilar una cadena de cinco niveles de mapa mip: 256x256, 128x128, 64x64, 32x32 y 16x16.


```
// This code example assumes that m_d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface

IDirect3DTexture9 * pMipMap;
m_pD3DDevice->CreateTexture(256, 256, 5, 0, D3DFMT_R8G8B8, 
    D3DPOOL_MANAGED, &pMipMap);
```



Los dos primeros parámetros aceptados por [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) son el tamaño y el ancho de la textura de nivel superior. El tercer parámetro especifica el número de niveles de la textura. Si establece esta opción en cero, Direct3D crea una cadena de superficies, cada una de ellas una potencia de dos más pequeñas que la anterior, hasta el menor tamaño posible de 1x1. El cuarto parámetro especifica el uso de este recurso; En este caso, se especifica 0 para indicar que no hay ningún uso específico para el recurso. El quinto parámetro especifica el formato de superficie para la textura. Use un valor del tipo [enumerado D3DFORMAT](d3dformat.md) para este parámetro. El sexto parámetro especifica un miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) que indica la clase de memoria en la que se va a colocar el recurso creado. A menos que use texturas dinámicas, se recomienda D3DPOOL \_ MANAGED. El parámetro final toma la dirección de un puntero a una [**interfaz IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)

> [!Note]  
> Cada superficie de una cadena de mapa mip tiene dimensiones que son la mitad de la superficie anterior de la cadena. Si el mapa mip de nivel superior tiene dimensiones de 256 x 128, las dimensiones del mapa mip de segundo nivel son 128 x 64, el tercer nivel son 64 x 32, y así sucesivamente, hasta 1x1. No se puede solicitar un número de niveles de mapa mip en Niveles que harían que el ancho o el alto de cualquier mapa mip de la cadena sea menor que 1. En el caso simple de una superficie mipmap de nivel superior de 4x2, el valor máximo permitido para Levels es tres. Las dimensiones de nivel superior son 4x2, las dimensiones de segundo nivel son 2x1 y las dimensiones del tercer nivel son 1x1. Un valor mayor que 3 en Niveles da como resultado un valor fraccionado en el alto del mapa MIP de segundo nivel y, por lo tanto, no se puede.

 

## <a name="selecting-and-displaying-a-mipmap"></a>Selección y visualización de un mapa Mip

Llame al [**método IDirect3DDevice9::SetTexture**](/windows/desktop/api) para establecer el conjunto de texturas mipmap como la primera textura de la lista de texturas actuales. Para obtener más información, vea [Mezcla de textura (Direct3D 9).](texture-blending.md)

Una vez que la aplicación selecciona el conjunto de texturas mipmap, debe asignar valores del tipo enumerado [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) al estado del muestreador MIPFILTER de D3DSAMP. \_ A continuación, Direct3D realiza automáticamente el filtrado de textura de mapa mipmap. La habilitación del filtrado de texturas mipmap se muestra en el ejemplo de código siguiente.


```
m_pD3DDevice->SetTexture(0, pMipMap);
m_pD3DDevice->SetSamplerState(0, D3DSAMP_MIPFILTER, D3DTEXF_POINT);
```



La aplicación también puede atravesar manualmente una cadena de superficies de mapa mip mediante el método [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) y especificando el nivel de mapa mipmap que se va a recuperar. En el ejemplo siguiente se recorre una cadena de asignación mip de las resoluciones más altas a las más bajas.


```
IDirect3DSurface9 * pSurfaceLevel;
for (int iLevel = 0; iLevel < pMipMap->GetLevelCount(); iLevel++)
{
    pMipMap->GetSurfaceLevel(iLevel, &pSurfaceLevel);
    // Process this level
    pSurfaceLevel->Release();
}
```



Las aplicaciones deben atravesar manualmente una cadena de mapas mipmap para cargar datos de mapa de bits en cada superficie de la cadena. Este suele ser el único motivo para recorrer la cadena. Una aplicación puede recuperar el número de niveles de un mapa mipmap llamando a [**IDirect3DBaseTexture9::GetLevelCount**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getlevelcount).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de texturas](texture-filtering.md)
</dt> </dl>

 

 
