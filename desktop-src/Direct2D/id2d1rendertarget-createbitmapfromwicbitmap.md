---
title: Métodos ID2D1RenderTarget CreateBitmapFromWicBitmap
description: Crea un objeto ID2D1Bitmap copiando el mapa de bits de Microsoft Windows Imaging Component (WIC) especificado.
ms.assetid: 463fc2f9-8ec6-47e8-8d48-a9015616e656
keywords:
- Métodos de CreateBitmapFromWicBitmap direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 23ad055beab9f24c39f032a3e28456c231480c68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162850"
---
# <a name="id2d1rendertargetcreatebitmapfromwicbitmap-methods"></a>Métodos ID2D1RenderTarget::CreateBitmapFromWicBitmap

Crea un [**objeto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando el mapa de bits de Microsoft Windows Imaging Component (WIC) especificado.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                              | Descripción                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapFromWicBitmap(IWICBitmapSource \* ,ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_id2d1bitmap))                                                       | Crea un [**objeto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando el mapa de bits de Microsoft Windows Imaging Component (WIC) especificado.<br/>  |
| [**CreateBitmapFromWicBitmap(IWICBitmapSource \* ,D2D1 \_ BITMAP PROPERTIES \_&,ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1__id2d1bitmap1))  | Crea un [**objeto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando el mapa de bits de Microsoft Windows Imaging Component (WIC) especificado.<br/> |
| [**CreateBitmapFromWicBitmap(IWICBitmapSource \* ,D2D1 \_ BITMAP PROPERTIES \_ \* ,ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) | Crea un [**objeto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando el mapa de bits de Microsoft Windows Imaging Component (WIC) especificado.<br/> |



## <a name="remarks"></a>Observaciones

Para que Direct2D pueda cargar una imagen de WIC, debe convertirse a un formato de píxeles y un modo alfa admitidos. Para obtener una lista de los formatos de píxel admitidos y los modos alfa, vea [Formatos de píxeles admitidos y Modos alfa.](supported-pixel-formats-and-alpha-modes.md)

## <a name="examples"></a>Ejemplos

Para obtener ejemplos, [vea How to Load a Bitmap from a File](how-to-load-a-direct2d-bitmap-from-a-file.md) (Cómo cargar un mapa de bits desde un archivo) y How to Load a Bitmap from a Resource (Cómo cargar un mapa de bits desde un [recurso).](how-to-load-a-bitmap-from-a-resource.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[Cómo cargar un mapa de bits desde un archivo](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> <dt>

[Formatos de píxel admitidos y modos alfa](supported-pixel-formats-and-alpha-modes.md)
</dt> </dl>

 

