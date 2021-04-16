---
title: Efecto de transferencia discreto
description: Use el efecto de transferencia discreta para asignar las intensidades de color de una imagen mediante una función de transferencia por pasos creada a partir de una lista de valores que proporcione.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- efecto de transferencia discreto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104562953"
---
# <a name="discrete-transfer-effect"></a>Efecto de transferencia discreto

Use el efecto de transferencia discreta para asignar las intensidades de color de una imagen mediante una función de transferencia por pasos creada a partir de una lista de valores que proporcione.

El CLSID para este efecto es CLSID \_ D2D1DiscreteTransfer.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

La imagen siguiente muestra la entrada y la salida del efecto de la transferencia discreta.



| Antes                                                            |
|-------------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)        |
| Después                                                             |
| ![la imagen después de la transformación.](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



La función de transferencia se basa en la lista de entradas: V = (V0, V1, V2, V3, V? , V<sub>n</sub>), donde N es el número de elementos-1.

La intensidad del píxel de entrada se representa como C. La intensidad de los píxeles de salida, C se calcula con la ecuación:

Para un valor C, elija un valor k, de modo que:

![fórmula para el proceso.](images/discrete-transfer1.png)

La salida C se puede calcular mediante la ecuación: C ' = V?

Este efecto funciona en imágenes alfa directas y premultiplicadas. El efecto genera mapas de bits alfa premultiplicados.

Este es el aspecto del gráfico de la función de transferencia discreta si las entradas son `[0.25, 0.5, 0.75, 1.0]` .

![gráfico de intensidad de píxeles para la función de transferencia discreta.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a>Propiedades del efecto

> [!Note]  
> Los valores de todos los canales de las propiedades de transferencia discreta son independientes y tienen un mínimo de 0,0 y un máximo de 1,0.

 



| Enumeración de índice y nombre para mostrar                                              | Tipo y valor predeterminado                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ roja, \_ tabla<br/>         | FLOT\[\]<br/> {0.0 f, 1.0 f}<br/> | Lista de valores que se usan para definir la función de transferencia para el canal rojo.                                                                                                                                                                                                                                                                                                                                                                                 |
| RedDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ rojo \_ deshabilitado<br/>     | BOOL<br/> false<br/>             | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal rojo. Si se establece en FALSE, el efecto aplica la función RedDiscreteTransfer al canal rojo.                                                                                                                                                                                                                                                                 |
| GreenTable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ verde \_ tabla<br/>     | FLOT\[\]<br/> {0.0 f, 1.0 f}<br/> | Lista de valores que definen la función de transferencia para el canal verde.                                                                                                                                                                                                                                                                                                                                                                                  |
| GreenDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ verde \_ deshabilitada<br/> | BOOL<br/> false<br/>             | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal verde. Si se establece en FALSE, el efecto aplica la función GreenDiscreteTransfer al canal verde.                                                                                                                                                                                                                                                           |
| BlueTable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ \_ tabla azul<br/>       | FLOT\[\]<br/> {0.0 f, 1.0 f}<br/> | Lista de valores que definen la función de transferencia para el canal azul.                                                                                                                                                                                                                                                                                                                                                                                   |
| BlueDisable<br/> Deshabilitar D2D1 de DISCRETETRANSFER de la \_ \_ prop \_ azul \_<br/>   | BOOL<br/> false<br/>             | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal azul. Si se establece en FALSE, el efecto aplica la función BlueDiscreteTransfer al canal azul.                                                                                                                                                                                                                                                              |
| AlphaTable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ \_ tabla alfa<br/>     | FLOT\[\]<br/> {0.0 f, 1.0 f}<br/> | Lista de valores que definen la función de transferencia para el canal alfa.                                                                                                                                                                                                                                                                                                                                                                                  |
| AlphaDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ alpha \_ deshabilitada<br/> | BOOL<br/> false<br/>             | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal alfa. Si se establece en FALSE, el efecto aplica la función AlphaDiscreteTransfer al canal alfa.                                                                                                                                                                                                                                                           |
| ClampOutput<br/> Salida de la abrazadera de D2D1 \_ DISCRETETRANSFER \_ \_ \_<br/>   | BOOL<br/> false<br/>             | Si el efecto fija los valores de color entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto del gráfico. El efecto fija los valores antes de que premultiplique el alfa.<br/> Si establece este valor en TRUE, el efecto fijará los valores. Si se establece en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no son de precisión lo suficientemente alta.<br/> |



 

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

 

