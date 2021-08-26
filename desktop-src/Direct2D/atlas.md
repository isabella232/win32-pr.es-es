---
title: Efecto Atlas
description: Puede usar este efecto para generar una parte de una imagen, pero conservar la región fuera de la parte para usarla en operaciones posteriores.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b0d55e7751ef73d8f6bdff65a6ae5d5933695600a1003b9c4a010231628019
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929059"
---
# <a name="atlas-effect"></a>Efecto Atlas

Puede usar este efecto para generar una parte de una imagen, pero conservar la región fuera de la parte para usarla en operaciones posteriores.

El CLSID para este efecto es CLSID \_ D2D1Atlas.

El efecto atlas es útil si desea cargar una imagen grande que se conste de muchas imágenes más pequeñas, como varios fotogramas de un sprite.

Para crear la salida, haga lo siguiente:

1.  Recorta la entrada a la *propiedad InputRect* dada.
2.  Traduce el origen del resultado a (0,0).

> [!Note]  
> La *propiedad InputPaddingRect* solo debe ser mayor si y solo si los píxeles entre los dos rectángulos son de color negro transparente en la entrada. Esto puede dar lugar a que Direct2D ejecute el gráfico de forma más óptima.

 

Este es un ejemplo del efecto. Esta imagen es pequeña y sencilla con fines ilustrativos.

![imagen de entrada.](images/atlas.png)

La imagen anterior es la entrada al efecto. El código aquí crea un efecto atlas, establece la entrada, establece el rectángulo de entrada y, a continuación, dibuja la salida.


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



El código anterior selecciona un rectángulo que está alrededor del segundo triángulo. Se omite el relleno que lo rodea. Esta es la imagen resultante.

![imagen de salida.](images/atlas2.png)

> [!Note]  
> Se trata de una situación en la que puede optar por especificar *inputPaddingRect* porque el relleno es negro transparente. El rectángulo sería `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .

 

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                             | Descripción                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InputRect<br/> D2D1 \_ ATLAS \_ PROP \_ INPUT \_ RECT<br/>                 | Parte de la imagen pasada al siguiente efecto.<br/> El tipo es D2D1 \_ VECTOR \_ 4F.<br/> El valor predeterminado es (-FLT \_ MAX, -FLT \_ MAX, FLT \_ MAX, FLT \_ MAX). <br/> |
| InputPaddingRect<br/> D2D1 \_ ATLAS \_ PROP \_ INPUT \_ PADDING \_ RECT<br/> | Tamaño máximo muestreado para el rectángulo de salida.<br/> El tipo es D2D1 \_ VECTOR \_ 4F.<br/> El valor predeterminado es (-FLT \_ MAX, -FLT \_ MAX, FLT \_ MAX, FLT \_ MAX).<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

