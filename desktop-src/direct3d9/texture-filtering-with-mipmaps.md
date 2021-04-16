---
description: Un mipmap es una secuencia de texturas, cada una de las cuales es una representación de resolución progresivamente inferior de la misma imagen.
ms.assetid: b64abca9-0efb-4939-849d-e75a8d0dc10b
title: Filtrado de textura con mapas MIP (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc109ae6de93a26b5d5e5b90e948761e92ee92c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550430"
---
# <a name="texture-filtering-with-mipmaps-direct3d-9"></a>Filtrado de textura con mapas MIP (Direct3D 9)

Un mipmap es una secuencia de texturas, cada una de las cuales es una representación de resolución progresivamente inferior de la misma imagen. El alto y el ancho de cada imagen, o nivel, en el mipmap es una potencia de dos más pequeña que el nivel anterior. Los mapas MIP no tienen por qué ser cuadrados.

Se utiliza una imagen de mapa de bits de alta resolución para los objetos cercanos al usuario. Las imágenes de resolución inferior se usan cuando el objeto aparece más lejos. Mipmapping mejora la calidad de las texturas representadas a costa de usar más memoria.

Direct3D representa los mipmaps como una cadena de superficies asociadas. La textura de resolución más alta está en el encabezado de la cadena y tiene el siguiente nivel de mipmap como datos adjuntos. A su vez, ese nivel tiene datos adjuntos que son el nivel siguiente del mipmap, y así sucesivamente, hasta el nivel de resolución más bajo del mipmap.

En las ilustraciones siguientes se muestra un ejemplo de estos niveles. Las texturas de mapa de bits representan un inicio de sesión en un contenedor en un juego de primera persona 3D. Cuando se crea como un mipmap, la textura de resolución más alta es la primera en el conjunto. Cada una de las texturas posteriores en el conjunto de mipmap es más pequeña en el alto y el ancho con una potencia de 2. En este caso, el mipmap de resolución máxima es de 256 píxeles por 256 píxeles. A continuación, la textura es 128x128. La última textura de la cadena es 64 x 64.

Este signo tiene una distancia máxima a la que está visible. Si el usuario comienza lejos del signo, el juego muestra la textura más pequeña de la cadena de mipmap, que en este caso la textura 64 x 64.

![Ilustración de una textura 64 x 64 de un signo de peligro](images/mip1.jpg)

A medida que el usuario mueve el punto de vista más cerca del signo, se usan texturas progresivamente de resolución superior en la cadena de mipmap. La resolución de la siguiente ilustración es 128x128.

![Ilustración de una textura 128x128 de un signo de peligro](images/mip2.jpg)

La textura de resolución más alta se utiliza cuando el punto de vista del usuario se encuentra en la distancia mínima permitida del signo, como se muestra en la siguiente ilustración.

![Ilustración de una textura 256x256 de un signo de peligro](images/mip3.jpg)

Se trata de una forma más eficaz de simular la perspectiva de las texturas. En lugar de representar una sola textura en muchas resoluciones, es más rápido utilizar varias texturas en diferentes resoluciones.

Direct3D puede evaluar qué textura de un conjunto de mipmap es la resolución más cercana a la salida deseada y puede asignar píxeles en su espacio de textura. Si la resolución de la imagen final se encuentra entre las resoluciones de las texturas del conjunto de mipmap, Direct3D puede examinar textura en los mapas MIP y mezclar sus valores de color juntos.

Para usar los mapas MIP, la aplicación debe crear un conjunto de mapas MIP. Las aplicaciones aplican los mipmaps seleccionando el conjunto de mipmap como primera textura en el conjunto de texturas actuales. Para obtener más información, vea [Texture blending (Direct3D 9)](texture-blending.md).

A continuación, la aplicación debe establecer el método de filtrado que usa Direct3D para muestrear textura. El método más rápido de filtrado de mipmap es hacer que Direct3D Seleccione el textura más próximo. Use el \_ valor enumerado del punto D3DTEXF para seleccionarlo. Direct3D puede producir mejores resultados de filtrado si la aplicación usa el \_ valor enumerado lineal D3DTEXF. Esto selecciona el mipmap más cercano y, a continuación, calcula una media ponderada del textura alrededor de la ubicación en la textura a la que se asigna el píxel actual.

Las texturas de mipmap se usan en escenas 3D para reducir el tiempo necesario para representar una escena. También mejoran el realismo de la escena. Sin embargo, a menudo requieren grandes cantidades de memoria.

## <a name="creating-a-set-of-mipmaps"></a>Crear un conjunto de mapas MIP

En el ejemplo siguiente se muestra cómo la aplicación puede llamar al método [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) para crear una cadena de cinco niveles de mipmap: 256x256, 128x128, 64 x 64, 32x32 y 16x16.


```
// This code example assumes that m_d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface

IDirect3DTexture9 * pMipMap;
m_pD3DDevice->CreateTexture(256, 256, 5, 0, D3DFMT_R8G8B8, 
    D3DPOOL_MANAGED, &pMipMap);
```



Los dos primeros parámetros aceptados por [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) son el tamaño y el ancho de la textura de nivel superior. El tercer parámetro especifica el número de niveles de la textura. Si se establece en cero, Direct3D crea una cadena de superficies, cada una de las cuales tiene una potencia de dos más pequeña que la anterior, hasta el tamaño más pequeño posible de 1x1. El cuarto parámetro especifica el uso de este recurso; en este caso, se especifica 0 para indicar que no hay ningún uso específico para el recurso. El quinto parámetro especifica el formato de superficie de la textura. Use un valor del tipo enumerado [D3DFORMAT](d3dformat.md) para este parámetro. El sexto parámetro especifica un miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) que indica la clase de memoria en la que se va a colocar el recurso creado. A menos que use texturas dinámicas, se recomienda el uso de D3DPOOL \_ administrado. El último parámetro toma la dirección de un puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .

> [!Note]  
> Cada superficie de una cadena de mipmap tiene dimensiones que son una mitad de la superficie anterior de la cadena. Si el mipmap de nivel superior tiene dimensiones de 256x128, las dimensiones del mipmap de segundo nivel son 128x64, el tercer nivel es 64x32, y así sucesivamente, hasta 1x1. No se puede solicitar un número de niveles de mipmap en niveles que provoquen que el ancho o el alto de cualquier mipmap en la cadena sea menor que 1. En el caso simple de una superficie de mipmap de nivel superior de 4 TB, el valor máximo permitido para los niveles es tres. Las dimensiones de nivel superior son 4 TB, las dimensiones de segundo nivel son 2x1 y las dimensiones del tercer nivel son 1x1. Un valor mayor que 3 en niveles da como resultado un valor fraccionario en el alto del mipmap de segundo nivel y, por tanto, no se permite.

 

## <a name="selecting-and-displaying-a-mipmap"></a>Seleccionar y mostrar un mipmap

Llame al método [**IDirect3DDevice9:: SetTexture**](/windows/desktop/api) para establecer el conjunto de texturas de mipmap como la primera textura en la lista de texturas actuales. Para obtener más información, vea [Texture blending (Direct3D 9)](texture-blending.md).

Una vez que la aplicación selecciona el conjunto de texturas de mipmap, debe asignar valores del tipo enumerado [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) al estado de muestra de D3DSAMP \_ MIPFILTER. Después, Direct3D realiza automáticamente el filtrado de texturas MIP. En el ejemplo de código siguiente se muestra cómo habilitar el filtrado de texturas MIP.


```
m_pD3DDevice->SetTexture(0, pMipMap);
m_pD3DDevice->SetSamplerState(0, D3DSAMP_MIPFILTER, D3DTEXF_POINT);
```



La aplicación también puede atravesar manualmente una cadena de superficies MIP mediante el método [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) y especificando el nivel de mipmap que se va a recuperar. En el ejemplo siguiente se atraviesa una cadena de mipmap de la resolución más alta a la más baja.


```
IDirect3DSurface9 * pSurfaceLevel;
for (int iLevel = 0; iLevel < pMipMap->GetLevelCount(); iLevel++)
{
    pMipMap->GetSurfaceLevel(iLevel, &pSurfaceLevel);
    // Process this level
    pSurfaceLevel->Release();
}
```



Las aplicaciones deben atravesar manualmente una cadena de mipmap para cargar los datos de mapa de bits en cada superficie de la cadena. Esta suele ser la única razón para atravesar la cadena. Una aplicación puede recuperar el número de niveles de un mipmap llamando a [**IDirect3DBaseTexture9:: GetLevelCount**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getlevelcount).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de textura](texture-filtering.md)
</dt> </dl>

 

 
