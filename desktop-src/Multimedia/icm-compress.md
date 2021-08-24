---
title: ICM_COMPRESS mensaje (Vfw.h)
description: El ICM COMPRESS notifica a un controlador de compresión de vídeo que comprima un marco de \_ datos en un búfer definido por la aplicación.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- ICM_COMPRESS mensaje Windows Multimedia
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
ms.openlocfilehash: f1230f429eb49596dd8a450b8a384e0a69856b69c51141834458c09fa41ca54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678475"
---
# <a name="icm_compress-message"></a>\_ICM Mensaje COMPRESS

El **ICM \_ compress notifica** a un controlador de compresión de vídeo que comprima un marco de datos en un búfer definido por la aplicación.


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icc"></span><span id="ICC"></span>*Icc*
</dt> <dd>

Puntero a una [**estructura ICCOMPRESS.**](/windows/desktop/api/Vfw/ns-vfw-iccompress) Los siguientes miembros de esta estructura especifican los parámetros de compresión: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags,** **dwFrameSize** y **dwQuality**. El controlador también debe usar el miembro **biSizeImage** de la estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) asociada a **lpbiOutput** de **ICCOMPRESS** para devolver el tamaño del marco comprimido.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamaño, en bytes, de [**ICCOMPRESS.**](/windows/desktop/api/Vfw/ns-vfw-iccompress)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

