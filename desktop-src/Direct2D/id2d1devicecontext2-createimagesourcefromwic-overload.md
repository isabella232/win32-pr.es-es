---
title: Métodos ID2D1DeviceContext2 CreateImageSourceFromWic (D2d1 \_ 3.h)
description: Crea un objeto de origen de imagen a partir de un origen de mapa de bits de WIC, mientras se rellenará toda la memoria de píxeles dentro del origen de la imagen. La imagen se carga y almacena mientras se usa una cantidad mínima de memoria.
ms.assetid: af02630d-a9ca-f5b4-6f2a-31a73ef603e5
keywords:
- Métodos CreateImageSourceFromWic de Direct2D
topic_type:
- apiref
api_location:
- d2d1_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 91ca60f19a798d2c215d6810adafc08d83e96bf1923bd006f394910879cae14e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749635"
---
# <a name="id2d1devicecontext2createimagesourcefromwic-methods"></a>Métodos ID2D1DeviceContext2::CreateImageSourceFromWic

Crea un objeto de origen de imagen a partir de un origen de mapa de bits de WIC, mientras se rellenará toda la memoria de píxeles dentro del origen de la imagen. La imagen se carga y almacena mientras se usa una cantidad mínima de memoria.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                       | Descripción                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateImageSourceFromWic (IWICBitmapSource \* , D2D1 \_ IMAGE SOURCE LOADING \_ \_ \_ OPTIONS, ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))                   | Versión del método que permite especificar el origen de mapa de bits de WIC, el objeto de origen de la imagen de salida y las opciones de carga con el modo alfa predeterminado.<br/>   |
| [**CreateImageSourceFromWic (IWICBitmapSource, \* D2D1 \_ IMAGE SOURCE LOADING \_ \_ \_ OPTIONS, D2D1 \_ ALPHA \_ MODE, ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic)) | Versión del método que permite especificar el origen de mapa de bits de WIC, el objeto de origen de la imagen de salida, las opciones de carga y el modo alfa.<br/>           |
| [**CreateImageSourceFromWic (IWICBitmapSource \* , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))                                                          | Versión del método que permite especificar el origen de mapa de bits de WIC y el objeto de origen de la imagen de salida con opitons de carga y modo alfa predeterminados.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D2d1 \_ 3.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1DeviceContext2**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2)
</dt> </dl>

�

�
