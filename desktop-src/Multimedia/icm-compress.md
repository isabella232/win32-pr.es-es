---
title: Mensaje de ICM_COMPRESS (VFW. h)
description: El \_ mensaje de compresión ICM notifica a un controlador de compresión de vídeo que debe comprimir un fotograma de datos en un búfer definido por la aplicación.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- Mensaje de ICM_COMPRESS de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651412"
---
# <a name="icm_compress-message"></a>\_Mensaje de compresión ICM

El **mensaje \_ de compresión ICM** notifica a un controlador de compresión de vídeo que debe comprimir un fotograma de datos en un búfer definido por la aplicación.


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icc"></span><span id="ICC"></span>*ICC*
</dt> <dd>

Puntero a una estructura [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) . Los siguientes miembros de esta estructura especifican los parámetros de compresión: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize** y **dwQuality**. El controlador también debe utilizar el miembro **biSizeImage** de la estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) asociada a **lpbiOutput** de **ICCOMPRESS** para devolver el tamaño del fotograma comprimido.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamaño, en bytes, de [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

