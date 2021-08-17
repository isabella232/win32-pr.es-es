---
title: Efecto de transferencia de tabla
description: Use el efecto de transferencia de tabla para asignar las intensidades de color de una imagen mediante una función de transferencia creada a partir de la interpolación de una lista de valores que proporcione.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- efecto de transferencia de tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c533b55fd55c983b976633b766a6d8d273631d6111de9e2e36387f711f5f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665017"
---
# <a name="table-transfer-effect"></a>Efecto de transferencia de tabla

Use el efecto de transferencia de tabla para asignar las intensidades de color de una imagen mediante una función de transferencia creada a partir de la interpolación de una lista de valores que proporcione.

El CLSID para este efecto es CLSID \_ D2D1TableTransfer.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

La imagen aquí muestra la entrada y la salida del efecto de transferencia de tabla.



| Antes                                                         |
|----------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)     |
| Después                                                          |
| ![la imagen después de la transformación.](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



La función de transferencia se basa en una lista de entradas V=(V0,V1,V2,V3, V? ,V<sub>N</sub>) donde N es el número de elementos : 1.

La intensidad de píxeles de entrada se representa como C. La intensidad de píxeles de salida, C se puede calcular con la ecuación.

Para un valor C, elija un valor k, de forma que: k/N = C < (k+1)/N

La salida C se calcula mediante la siguiente ecuación: C' = V? + (C - k/N) \* N \* (V??? 1? - ¿V?)

Este efecto funciona en imágenes alfa rectas y premultiplicadas. El efecto genera mapas de bits alfa premultiplicados.

Este es el aspecto del gráfico de la función de transferencia de tabla si la propiedad table está establecida en `[0.0, 0.25, 1.0]` .

![gráfico de intensidad de píxeles para la función de transferencia de tabla.](images/table-transfer-graph.png)

## <a name="effect-properties"></a>Propiedades de efecto

> [!Note]  
> Los valores de todos los canales de las propiedades de transferencia de tabla no tienen unidad y tienen un mínimo de 0,0 y un máximo de 1,0.

 



| Enumeración de nombre para mostrar e índice                                           | Tipo y valor predeterminado                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> TABLA D2D1TRANSFER \_ \_ PROP RED \_ \_ TABLE<br/>         | Flotador\[\]<br/> {0.0f, 1.0f}<br/> | Lista de valores usados para definir la función de transferencia para el canal rojo.                                                                                                                                                                                                                                                                                                                                                                                  |
| RedDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ RED \_ DISABLE<br/>     | BOOL<br/> FALSE<br/>             | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal rojo. Si se establece en FALSE, se aplica la función RedTableTransfer al canal rojo.                                                                                                                                                                                                                                                                             |
| GreenTable<br/> TABLA D2D1TRANSFER \_ \_ PROP GREEN \_ \_ TABLE<br/>     | Flotador\[\]<br/> {0.0f, 1.0f}<br/> | Lista de valores usados para definir la función de transferencia para el canal verde.                                                                                                                                                                                                                                                                                                                                                                                |
| GreenDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ GREEN \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal verde. Si establece esta opción en FALSE, se aplica la función GreenTableTransfer al canal verde.                                                                                                                                                                                                                                                                       |
| BlueTable<br/> TABLA D2D1TRANSFER \_ \_ PROP BLUE \_ \_ TABLE<br/>       | Flotador\[\]<br/> {0.0f, 1.0f}<br/> | Lista de valores usados para definir la función de transferencia para el canal azul.                                                                                                                                                                                                                                                                                                                                                                                 |
| BlueDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ BLUE \_ DISABLE<br/>   | BOOL<br/> FALSE<br/>             | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal Azul. Si establece esta opción en FALSE, se aplica la función BlueTableTransfer al canal Azul.                                                                                                                                                                                                                                                                          |
| AlphaTable<br/> TABLA D2D1 \_ TABLE TRANSFER PROP ALPHA \_ \_ \_ \_ TABLE<br/>   | Flotador\[\]<br/> {0.0f, 1.0f}<br/> | Lista de valores usados para definir la función de transferencia para el canal Alfa.                                                                                                                                                                                                                                                                                                                                                                                |
| AlphaDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ ALPHA \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal Alfa. Si establece esta opción en FALSE, se aplica la función AlphaTableTransfer al canal Alfa.                                                                                                                                                                                                                                                                       |
| ClampOutput<br/> SALIDA DE LA FIJACIÓN \_ DE PROP DE TABLETRANSFER D2D1 \_ \_ \_<br/>   | BOOL<br/> FALSE<br/>             | Si el efecto fija los valores de color a entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto en el gráfico. El efecto fija los valores antes de multiplicar previamente el alfa .<br/> Si establece esta opción en TRUE, el efecto fijará los valores. Si establece esta opción en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no tienen una precisión lo suficientemente alta.<br/> |



 

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

 

