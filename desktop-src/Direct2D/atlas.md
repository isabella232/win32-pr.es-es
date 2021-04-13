---
title: Efecto de Atlas
description: Puede usar este efecto para generar una parte de una imagen, pero conservar la región fuera de la parte para su uso en operaciones posteriores.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492125"
---
# <a name="atlas-effect"></a>Efecto de Atlas

Puede usar este efecto para generar una parte de una imagen, pero conservar la región fuera de la parte para su uso en operaciones posteriores.

El CLSID para este efecto es CLSID \_ D2D1Atlas.

El efecto de Atlas es útil si desea cargar una imagen grande formada por muchas imágenes más pequeñas, como varios marcos de un Sprite.

Para crear la salida del efecto:

1.  Recorta la entrada a la propiedad *InputRect* especificada.
2.  Traduce el origen del resultado a (0,0).

> [!Note]  
> La propiedad *InputPaddingRect* solo debe ser mayor si y solo si los píxeles entre los dos rectángulos son negros transparentes en la entrada. Esto puede dar lugar a que Direct2D ejecute el gráfico de forma más óptima.

 

Este es un ejemplo del efecto. Esta imagen es pequeña y sencilla con fines ilustrativos.

![imagen de entrada.](images/atlas.png)

La imagen anterior es la entrada al efecto. En el código siguiente se crea un efecto de Atlas, se establece la entrada, se establece el rectángulo de entrada y, a continuación, se dibuja la salida.


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



El código anterior selecciona un rectángulo que está alrededor del segundo triángulo. Se omite el relleno alrededor de él. Esta es la imagen resultante.

![imagen de salida.](images/atlas2.png)

> [!Note]  
> Se trata de una situación en la que puede optar por especificar un *InputPaddingRect* porque el relleno es negro transparente. El rectángulo sería `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .

 

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                             | Descripción                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InputRect<br/> D2D1 \_ \_ Rect de \_ entrada de Atlas \_ de la<br/>                 | Parte de la imagen que se pasa al siguiente efecto.<br/> El tipo es D2D1 \_ Vector \_ 4F.<br/> El valor predeterminado es (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ máx.). <br/> |
| InputPaddingRect<br/> \_Rect de \_ \_ relleno de \_ entrada \_ de D2D1 Atlas<br/> | Tamaño máximo muestreado para el rectángulo de salida.<br/> El tipo es D2D1 \_ Vector \_ 4F.<br/> El valor predeterminado es (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ máx.).<br/>   |



 

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

 

