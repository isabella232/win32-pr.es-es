---
title: Efecto compuesto
description: Use el efecto compuesto para combinar 2 o más imágenes. Este efecto tiene 13 modos compuestos diferentes.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- efecto compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8cf326e5d0bfb33b3dc927ba7366eb6d2b343a1a50db462de58fac8ef648bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826585"
---
# <a name="composite-effect"></a>Efecto compuesto

Use el efecto compuesto para combinar 2 o más imágenes. Este efecto tiene 13 modos compuestos diferentes. T

El efecto compuesto acepta 2 o más entradas. Cuando se especifican 2 imágenes, el destino es la primera entrada (índice 0) y el origen es la segunda entrada (índice 1). Si especifica más de 2 entradas, las imágenes se composiciónn a partir de la primera entrada y la segunda, etc.

Este efecto implementa todos los modos mediante la unidad de combinación de la unidad de procesamiento de gráficos (GPU).

El CLSID para este efecto es CLSID \_ D2D1Composite.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Tipos de modo](#mode-types)
-   [Código de ejemplo](#sample-code)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

La imagen aquí muestra dos rectángulos redondeados del mismo tamaño que se superponen. El rectángulo azul es el origen y el rectángulo rojo es el destino. Las imágenes se han compuesto con el modo Origen por encima.

![una imagen de ejemplo que muestra dos rectángulos redondeados del mismo tamaño que se superponen mediante el modo de origen sobre .](images/composite-over.png)

Este es otro ejemplo de uso del modo predeterminado.



| Antes de la imagen 1                                                          |
|-------------------------------------------------------------------------|
| ![la primera imagen de origen antes del efecto.](images/default-before.jpg) |
| Antes de la imagen 2                                                          |
| ![la segunda imagen antes del efecto.](images/3-composite(2of2).png)    |
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



## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                     | Tipo y valor predeterminado                                                          | Descripción                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| Mode<br/> MODO DE PROP COMPUESTO D2D1 \_ \_ \_<br/> | MODO COMPUESTO \_ D2D1 \_<br/> ORIGEN DEL MODO COMPUESTO D2D1 \_ \_ \_ \_ SOBRE<br/> | Modo utilizado para el efecto. |



 

## <a name="mode-types"></a>Tipos de modo

En la tabla siguiente se muestran los modos de este efecto. Las ecuaciones enumeradas en la tabla usan estos elementos:

-   O = Salida
-   S = Origen
-   SA = Alfa de origen
-   D = Destino
-   DA = Alfa de destino



| Enumeración                                  | Ecuación                          | Tamaño del mapa de bits de salida                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| ORIGEN DEL MODO COMPUESTO D2D1 \_ \_ \_ \_ SOBRE          | O = S + (1 SA) \* D             | Unión de mapas de bits de origen y destino                                                                 |
| DESTINO DEL MODO COMPUESTO D2D1 \_ \_ \_ \_ SOBRE     | O = (1 DA) \* S + D             | Unión de mapas de bits de origen y destino                                                                 |
| ORIGEN DEL MODO COMPUESTO D2D1 \_ \_ \_ \_ EN            | O = DA \* S                       | Intersección de mapas de bits de origen y destino                                                          |
| DESTINO DEL MODO COMPUESTO D2D1 \_ \_ \_ \_ EN       | O = SA \* D                       | Intersección de mapas de bits de origen y destino                                                          |
| SALIDA DE ORIGEN DEL MODO COMPUESTO D2D1 \_ \_ \_ \_           | O = (1 - DA) \* S                 | Región del mapa de bits de origen                                                                             |
| SALIDA DE DESTINO DEL MODO COMPUESTO D2D1 \_ \_ \_ \_      | O = (1 - SA) \* D                 | Región del mapa de bits de destino                                                                        |
| ORIGEN DEL MODO COMPUESTO D2D1 \_ \_ \_ \_ ATOP          | O = DA \* S + (1 - SA) \* D       | Región del mapa de bits de destino                                                                        |
| DESTINO DEL MODO COMPUESTO D2D1 \_ \_ \_ \_ ATOP     | O = (1 - DA) \* S + SA \* D       | Región del mapa de bits de origen                                                                             |
| D2D1 \_ COMPOSITE \_ MODE \_ XOR                   | O = (1 - DA) \* S + (1 - SA) \* D | Unión de mapas de bits de origen y destino                                                                 |
| D2D1 \_ COMPOSITE \_ MODE \_ PLUS                  | O = S + D                         | Unión de mapas de bits de origen y destino                                                                 |
| COPIA DE ORIGEN DEL MODO COMPUESTO D2D1 \_ \_ \_ \_          | O = S                             | Región del mapa de bits de origen                                                                             |
| COPIA DE ORIGEN LIMITADA DEL MODO COMPUESTO D2D1 \_ \_ \_ \_ \_ | O = S (solo donde existe el origen)  | Unión de mapas de bits de origen y destino. El destino no se sobrescribe cuando el origen no existe. |
| INVERTIR MÁSCARA \_ \_ DE MODO COMPUESTO \_ D2D1 \_          | O = (1 D) \* S + (1 SA) \* D  | Unión de mapas de bits de origen y destino. Los valores alfa no se modifican.                                 |



 

En la ilustración siguiente se muestra un ejemplo de cada uno de los modos con imágenes que tienen una opacidad de 1.0 o 0.5.

![una imagen de ejemplo de cada uno de los modos con opacidad establecida en 1.0 o 0.5.](images/composite-types.png)

## <a name="sample-code"></a>Código de ejemplo

Para obtener un ejemplo de este efecto, descargue el ejemplo de modos de efecto compuesto [de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

