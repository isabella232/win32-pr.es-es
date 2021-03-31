---
title: Efecto de transferencia de tabla
description: Utilice el efecto transferencia de tabla para asignar las intensidades de color de una imagen mediante una función de transferencia creada a partir de la interpolación de una lista de valores que proporcione.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- efecto de transferencia de tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d590e7f232ac3d4cecd434786353dfc5b8ea80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490643"
---
# <a name="table-transfer-effect"></a>Efecto de transferencia de tabla

Utilice el efecto transferencia de tabla para asignar las intensidades de color de una imagen mediante una función de transferencia creada a partir de la interpolación de una lista de valores que proporcione.

El CLSID para este efecto es CLSID \_ D2D1TableTransfer.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

La imagen siguiente muestra la entrada y la salida del efecto de transferencia de tabla.



| Antes                                                         |
|----------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)     |
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



La función de transferencia se basa en una lista de entradas V = (V0, V1, V2, V3, V? , V<sub>n</sub>), donde N es el número de elementos-1.

La intensidad del píxel de entrada se representa como C. La intensidad de los píxeles de salida, C se puede calcular con la ecuación.

Para un valor C, elija un valor k, de modo que: k/N = C < (k + 1)/N

La salida C se calcula con la siguiente ecuación: C ' = V? + (C-k/N) \* N \* (V??? dimensional? -V?)

Este efecto funciona en imágenes alfa directas y premultiplicadas. El efecto genera mapas de bits alfa premultiplicados.

Este es el aspecto del gráfico de la función de transferencia de tabla si la propiedad de tabla está establecida en `[0.0, 0.25, 1.0]` .

![gráfico de intensidad de píxeles para la función de transferencia de tabla.](images/table-transfer-graph.png)

## <a name="effect-properties"></a>Propiedades del efecto

> [!Note]  
> Los valores de todos los canales de las propiedades de transferencia de tabla son no reunitarios y tienen un mínimo de 0,0 y un máximo de 1,0.

 



| Enumeración de índice y nombre para mostrar                                           | Tipo y valor predeterminado                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ roja, \_ tabla<br/>         | FLOT\[\]<br/> {0.0 f, 1.0 f}<br/> | Lista de valores que se usan para definir la función de transferencia para el canal rojo.                                                                                                                                                                                                                                                                                                                                                                                  |
| RedDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ rojo \_ deshabilitado<br/>     | BOOL<br/> false<br/>             | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal rojo. Si se establece en FALSE, se aplica la función RedTableTransfer al canal rojo.                                                                                                                                                                                                                                                                             |
| GreenTable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ verde \_ tabla<br/>     | FLOT\[\]<br/> {0.0 f, 1.0 f}<br/> | Lista de valores que se usan para definir la función de transferencia para el canal verde.                                                                                                                                                                                                                                                                                                                                                                                |
| GreenDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ verde \_ deshabilitada<br/> | BOOL<br/> false<br/>             | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal verde. Si se establece en FALSE, se aplica la función GreenTableTransfer al canal verde.                                                                                                                                                                                                                                                                       |
| BlueTable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ \_ tabla azul<br/>       | FLOT\[\]<br/> {0.0 f, 1.0 f}<br/> | Lista de valores que se usan para definir la función de transferencia del canal azul.                                                                                                                                                                                                                                                                                                                                                                                 |
| BlueDisable<br/> Deshabilitar D2D1 de TABLETRANSFER de la \_ \_ prop \_ azul \_<br/>   | BOOL<br/> false<br/>             | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal azul. Si se establece en FALSE, se aplica la función BlueTableTransfer al canal azul.                                                                                                                                                                                                                                                                          |
| AlphaTable<br/> D2D1 \_ TABLE \_ Transfer \_ tabla \_ alfa \_<br/>   | FLOT\[\]<br/> {0.0 f, 1.0 f}<br/> | Lista de valores utilizados para definir la función de transferencia para el canal alfa.                                                                                                                                                                                                                                                                                                                                                                                |
| AlphaDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ alpha \_ deshabilitada<br/> | BOOL<br/> false<br/>             | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal alfa. Si se establece en FALSE, se aplica la función AlphaTableTransfer al canal alfa.                                                                                                                                                                                                                                                                       |
| ClampOutput<br/> Salida de la abrazadera de D2D1 \_ TABLETRANSFER \_ \_ \_<br/>   | BOOL<br/> false<br/>             | Si el efecto fija los valores de color entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto del gráfico. El efecto fija los valores antes de que premultiplique el alfa.<br/> Si establece este valor en TRUE, el efecto fijará los valores. Si se establece en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no son de precisión lo suficientemente alta.<br/> |



 

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

 

