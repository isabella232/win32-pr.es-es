---
title: Métodos ID2D1RenderTarget CreateRadialGradientBrush (D2d1.h)
description: Crea un objeto ID2D1RadialGradientBrush que se puede usar para pintar áreas con un degradado radial.
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- Métodos CreateRadialGradientBrush de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 680cc981943e45eb32834e48151f391f6249cc1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162830"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a>Métodos ID2D1RenderTarget::CreateRadialGradientBrush

Crea un [**objeto ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que se puede usar para pintar áreas con un degradado radial.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                       | Descripción                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH PROPERTIES \_ \_ \_&,ID2D1GradientStopCollection \* ,ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))                            | Crea un [**objeto ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contiene los delimitadores de degradado especificados, no tiene ninguna transformación y tiene una opacidad base de 1,0. <br/> |
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH PROPERTIES \_ \_ \_&,D2D1 \_ BRUSH PROPERTIES \_&,ID2D1GradientStopCollection \* ,ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))   | Crea un [**objeto ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contiene los delimitadores de degradado especificados y tiene la transformación y opacidad base especificadas. <br/> |
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH PROPERTIES \_ \_ \_ \* ,D2D1 \_ BRUSH PROPERTIES \_ \* ,ID2D1GradientStopCollection \* ,ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) | Crea un [**objeto ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contiene los delimitadores de degradado especificados y tiene la transformación y opacidad base especificadas. <br/> |



## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, [vea How to Create a Radial Gradient Brush](how-to-create-a-radial-gradient-brush.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Cómo crear un pincel de degradado radial](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Información general sobre los pinceles](direct2d-brushes-overview.md)
</dt> </dl>

�

�
