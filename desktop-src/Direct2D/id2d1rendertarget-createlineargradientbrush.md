---
title: Métodos ID2D1RenderTarget CreateLinearGradientBrush (D2d1. h)
description: Crea un objeto ID2D1LinearGradientBrush para dibujar áreas con un degradado lineal.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- Métodos de CreateLinearGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 428fcb44ddf50af7b3e78c28e359430bceee2f79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690162"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a>ID2D1RenderTarget:: CreateLinearGradientBrush (métodos)

Crea un objeto [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) para dibujar áreas con un degradado lineal.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                       | Descripción                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateLinearGradientBrush (D2D1 \_ \_ \_ propiedades de pincel de degradado lineal \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))                            | Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contiene los delimitadores de degradado especificados, no tiene ninguna transformación y tiene una opacidad base de 1,0. <br/> |
| [**CreateLinearGradientBrush (D2D1 \_ \_ propiedades de \_ pincel de degradado lineal \_&, \_ propiedades del pincel de D2D1 \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))   | Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contiene los delimitadores de degradado especificados y tiene la transformación y la opacidad base especificadas. <br/> |
| [**CreateLinearGradientBrush ( \_ \_ \_ propiedades del pincel de degradado lineal \_ de D2D1 \* , \_ propiedades del pincel de D2D1 \_ \* , ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) | Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contiene los delimitadores de degradado especificados y tiene la transformación y la opacidad base especificadas. <br/> |



## <a name="examples"></a>Ejemplos

Para ver un ejemplo en el que se muestra cómo crear una colección de delimitadores de degradado y cómo usarla para definir un degradado lineal, vea [Cómo crear un pincel de degradado lineal](how-to-create-a-linear-gradient-brush.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**CreateGradientStopCollection**](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[Cómo crear un pincel de degradado lineal](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Información general sobre los pinceles](direct2d-brushes-overview.md)
</dt> </dl>

�

�
