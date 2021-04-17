---
title: Métodos ID2D1Factory CreateWicBitmapRenderTarget
description: Crea un destino de representación que se representa en un mapa de bits de Microsoft Windows Imaging Component (WIC).
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Métodos de CreateWicBitmapRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4025028582c254e7a5724a575ef0d7f1c7d91570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660327"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a>ID2D1Factory:: CreateWicBitmapRenderTarget (métodos)

Crea un destino de representación que se representa en un mapa de bits de Microsoft Windows Imaging Component (WIC).

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                            | Descripción                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**CreateWicBitmapRenderTarget (IWICBitmap \* , D2D1 \_ representar \_ \_ propiedades \* de destino, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) | Crea un destino de representación que se representa en un mapa de bits de Microsoft Windows Imaging Component (WIC).<br/> |
| [**CreateWicBitmapRenderTarget (IWICBitmap \* , D2D1 \_ \_ \_ propiedades de destino de representación&, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))  | Crea un destino de representación que se representa en un mapa de bits de Microsoft Windows Imaging Component (WIC).<br/> |



## <a name="remarks"></a>Observaciones

La aplicación debe crear los destinos de representación una vez y mantenerlos en la vida de la aplicación o hasta que se reciba el error de [**\_ \_ destino de recreación de D2DERR**](direct2d-error-codes.md) . Cuando reciba este error, deberá volver a crear el destino de representación (y los recursos que haya creado).

**Nota:**   Este método no se admite en Windows Phone y se producirá un error cuando se lo llame en un dispositivo con el código de error 0x8899000b (no hay ningún dispositivo de representación de hardware disponible para esta operación). Dado que el emulador de Windows Phone admite la representación de ALABEo, este método producirá un error cuando se llame en el emulador con un código de error diferente, 0x88982f80 (wincodec \_ Err \_ unsupportedpixelformat).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

