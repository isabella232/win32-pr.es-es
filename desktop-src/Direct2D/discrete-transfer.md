---
title: Efecto de transferencia discreta
description: Use el efecto de transferencia discreta para asignar las intensidades de color de una imagen mediante una función de transferencia paso a paso creada a partir de una lista de valores que proporcione.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- efecto de transferencia discreto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163330"
---
# <a name="discrete-transfer-effect"></a>Efecto de transferencia discreta

Use el efecto de transferencia discreta para asignar las intensidades de color de una imagen mediante una función de transferencia paso a paso creada a partir de una lista de valores que proporcione.

El CLSID para este efecto es CLSID \_ D2D1DiscreteTransfer.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

La imagen aquí muestra la entrada y la salida del efecto de transferencia discreta.



| Antes                                                            |
|-------------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)        |
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



La función de transferencia se basa en la lista de entradas: V=(V0,V1,V2,V3,V? ,V<sub>N</sub>) donde N es el número de elementos : 1.

La intensidad de píxeles de entrada se representa como C. La intensidad de píxeles de salida, C se calcula con la ecuación:

Para un valor C, elija un valor k, de forma que:

![fórmula para el proceso.](images/discrete-transfer1.png)

La salida C se puede calcular mediante la ecuación: C' = V?

Este efecto funciona en imágenes alfa rectas y premultiplicadas. El efecto genera mapas de bits alfa premultiplicados.

Este es el aspecto del gráfico de la función de transferencia discreta si las entradas son `[0.25, 0.5, 0.75, 1.0]` .

![gráfico de intensidad de píxeles para la función de transferencia discreta.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a>Propiedades de efecto

> [!Note]  
> Los valores de todos los canales de las propiedades de transferencia discretas no tienen unidad y tienen un mínimo de 0,0 y un máximo de 1,0.

 



| Enumeración de nombre para mostrar e índice                                              | Tipo y valor predeterminado                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ RED \_ TABLE<br/>         | FLOTADOR\[\]<br/> {0.0f, 1.0f}<br/> | Lista de valores usados para definir la función de transferencia para el canal rojo.                                                                                                                                                                                                                                                                                                                                                                                 |
| RedDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ RED \_ DISABLE<br/>     | BOOL<br/> false<br/>             | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal rojo. Si establece esta opción en FALSE, el efecto aplica la función RedDiscreteTransfer al canal rojo.                                                                                                                                                                                                                                                                 |
| GreenTable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ GREEN \_ TABLE<br/>     | FLOTADOR\[\]<br/> {0.0f, 1.0f}<br/> | Lista de valores que definen la función de transferencia para el canal verde.                                                                                                                                                                                                                                                                                                                                                                                  |
| GreenDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ GREEN \_ DISABLE<br/> | BOOL<br/> false<br/>             | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal verde. Si establece esta opción en FALSE, el efecto aplica la función GreenDiscreteTransfer al canal verde.                                                                                                                                                                                                                                                           |
| BlueTable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ BLUE \_ TABLE<br/>       | FLOTADOR\[\]<br/> {0.0f, 1.0f}<br/> | Lista de valores que definen la función de transferencia para el canal azul.                                                                                                                                                                                                                                                                                                                                                                                   |
| BlueDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ BLUE \_ DISABLE<br/>   | BOOL<br/> false<br/>             | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal Azul. Si establece esta opción en FALSE, el efecto aplica la función BlueDiscreteTransfer al canal Azul.                                                                                                                                                                                                                                                              |
| AlphaTable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ ALPHA \_ TABLE<br/>     | FLOTADOR\[\]<br/> {0.0f, 1.0f}<br/> | Lista de valores que definen la función de transferencia para el canal Alfa.                                                                                                                                                                                                                                                                                                                                                                                  |
| AlphaDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ ALPHA \_ DISABLE<br/> | BOOL<br/> false<br/>             | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal Alfa. Si establece esta opción en FALSE, el efecto aplica la función AlphaDiscreteTransfer al canal Alfa.                                                                                                                                                                                                                                                           |
| ClampOutput<br/> SALIDA DE LA FIJACIÓN \_ DE \_ PROP \_ DISCRETETRANSFER D2D1 \_<br/>   | BOOL<br/> false<br/>             | Si el efecto fija los valores de color a entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto en el gráfico. El efecto fija los valores antes de multiplicar previamente el valor alfa.<br/> Si establece esta opción en TRUE, el efecto fijará los valores. Si establece esta opción en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no tienen una precisión lo suficientemente alta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio \| Windows store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio \| Windows store\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

