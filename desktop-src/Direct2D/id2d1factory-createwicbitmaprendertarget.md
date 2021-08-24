---
title: Métodos ID2D1Factory CreateWicBitmapRenderTarget
description: Crea un destino de representación que se representa en un mapa de bits Windows Imaging Component (WIC) de Microsoft.
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Métodos De Direct2D de CreateWicBitmapRenderTarget
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 177f5459d8245292e2962e502882bb86643f3f8b777efd8a336fde5f8c671897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698185"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a>Métodos ID2D1Factory::CreateWicBitmapRenderTarget

Crea un destino de representación que se representa en un mapa de bits Windows Imaging Component (WIC) de Microsoft.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                            | Descripción                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**CreateWicBitmapRenderTarget(IWICBitmap \* ,D2D1 \_ RENDER TARGET PROPERTIES \_ \_ \* ,ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) | Crea un destino de representación que se representa en un mapa de bits Windows Imaging Component (WIC) de Microsoft.<br/> |
| [**CreateWicBitmapRenderTarget(IWICBitmap \* ,D2D1 \_ RENDER TARGET PROPERTIES \_ \_&,ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))  | Crea un destino de representación que se representa en un mapa de bits Windows Imaging Component (WIC) de Microsoft.<br/> |



## <a name="remarks"></a>Comentarios

La aplicación debe crear destinos de representación una vez y retenerlos durante la vida útil de la aplicación o hasta que se reciba el error [**D2DERR \_ RECREATE \_ TARGET.**](direct2d-error-codes.md) Cuando reciba este error, deberá volver a crear el destino de representación (y los recursos que creó).

**Nota**   Este método no se admite en Windows Phone y se producirá un error cuando se llame a en un dispositivo con código de error 0x8899000b ( No hay ningún dispositivo de representación de hardware disponible para esta operación ). Dado que Windows Phone Emulator la representación warp, este método producirá un error cuando se llame en el emulador con un código de error diferente, 0x88982f80 (wincodec \_ err \_ unsupportedpixelformat).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

