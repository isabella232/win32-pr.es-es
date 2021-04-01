---
title: Efecto compuesto
description: Use el efecto compuesto para combinar dos o más imágenes. Este efecto tiene 13 modos compuestos distintos.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- efecto compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9872a66d031e8307f911ec7270af81397a80276
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996540"
---
# <a name="composite-effect"></a>Efecto compuesto

Use el efecto compuesto para combinar dos o más imágenes. Este efecto tiene 13 modos compuestos distintos. T

El efecto compuesto acepta 2 o más entradas. Cuando se especifican dos imágenes, el destino es la primera entrada (índice 0) y el origen es la segunda entrada (Índice 1). Si especifica más de 2 entradas, las imágenes se componen a partir de la primera entrada y la segunda, etc.

Este efecto implementa todos los modos mediante la unidad de fusión de la unidad de procesamiento de gráficos (GPU).

El CLSID para este efecto es CLSID \_ D2D1Composite.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Tipos de modo](#mode-types)
-   [Código de ejemplo](#sample-code)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En la imagen siguiente se muestran dos rectángulos redondeados del mismo tamaño que se superponen. El rectángulo azul es el origen y el rectángulo rojo es el destino. Las imágenes se han compuesto con el modo de origen sobre.

![imagen de ejemplo que muestra dos rectángulos redondeados del mismo tamaño que se superponen con el modo de origen sobre.](images/composite-over.png)

Este es otro ejemplo en el que se usa el modo predeterminado.



| Antes de la imagen 1                                                          |
|-------------------------------------------------------------------------|
| ![primera imagen de origen antes del efecto.](images/default-before.jpg) |
| Antes de la imagen 2                                                          |
| ![segunda imagen anterior al efecto.](images/3-composite(2of2).png)    |
| Después                                                                   |
| ![la imagen después de la transformación.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                     | Tipo y valor predeterminado                                                          | Descripción                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| Mode<br/> Modo de D2D1 \_ composite \_ props \_<br/> | \_Modo compuesto \_ D2D1<br/> \_Origen de \_ modo compuesto D2D1 \_ \_ sobre<br/> | Modo utilizado para el efecto. |



 

## <a name="mode-types"></a>Tipos de modo

En la tabla siguiente se muestran los modos de este efecto. Las ecuaciones que aparecen en la tabla usan estos elementos:

-   O = salida
-   S = origen
-   SA = alfa de origen
-   D = destino
-   DA = alfa de destino



| Enumeración                                  | Ecuación                          | Tamaño del mapa de bits de salida                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| \_Origen de \_ modo compuesto D2D1 \_ \_ sobre          | O = S + (1 SA) \* D             | Unión de mapas de bits de origen y de destino                                                                 |
| \_Destino de \_ modo compuesto D2D1 \_ \_ sobre     | O = (1 DA) \* S + D             | Unión de mapas de bits de origen y de destino                                                                 |
| \_ \_ Origen de modo compuesto D2D1 \_ \_ en            | O = DA \* S                       | Intersección de los mapas de bits de origen y de destino                                                          |
| \_ \_ Destino de modo compuesto D2D1 \_ \_ en       | O = SA \* D                       | Intersección de los mapas de bits de origen y de destino                                                          |
| \_Origen de \_ modo \_ compuesto \_ D2D1           | O = (1-DA) \* S                 | Región del mapa de bits de origen                                                                             |
| \_Destino de \_ modo \_ compuesto \_ de D2D1      | O = (1-SA) \* D                 | Región del mapa de bits de destino                                                                        |
| \_Origen de \_ modo \_ compuesto \_ D2D1 sobre          | O = DA \* S + (1-SA) \* D       | Región del mapa de bits de destino                                                                        |
| \_Destino de \_ modo \_ compuesto \_ D2D1 sobre     | O = (1-DA) \* S + SA \* D       | Región del mapa de bits de origen                                                                             |
| D2D1 \_ \_ modo compuesto \_ XOR                   | O = (1-DA) \* S + (1-SA) \* D | Unión de mapas de bits de origen y de destino                                                                 |
| D2D1 \_ \_ modo compuesto \_ más                  | O = S + D                         | Unión de mapas de bits de origen y de destino                                                                 |
| D2D1 \_ \_ copia de \_ origen del modo compuesto \_          | O = S                             | Región del mapa de bits de origen                                                                             |
| D2D1 \_ \_ copia de \_ origen enlazada en modo compuesto \_ \_ | O = S (solo cuando existe el origen)  | Unión de los mapas de bits de origen y de destino. El destino no se sobrescribe cuando el origen no existe. |
| Invertida de la \_ \_ máscara de modo compuesto \_ D2D1 \_          | O = (1 D) \* S + (1 SA) \* D  | Unión de los mapas de bits de origen y de destino. Los valores alfa no se modifican.                                 |



 

En la ilustración siguiente se muestra un ejemplo de cada uno de los modos con imágenes que tienen una opacidad de 1,0 o 0,5.

![una imagen de ejemplo de cada uno de los modos con opacidad establecida en 1,0 o 0,5.](images/composite-types.png)

## <a name="sample-code"></a>Código de ejemplo

Para obtener un ejemplo de este efecto, descargue el [ejemplo de modos de efecto compuesto de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Servidor mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Encabezado                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

