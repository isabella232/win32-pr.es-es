---
title: ICM_COMPRESS mensaje (Vfw.h)
description: El ICM COMPRESS notifica a un controlador de compresión \_ de vídeo que comprime un marco de datos en un búfer definido por la aplicación.
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
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370418"
---
# <a name="icm_compress-message"></a>\_ICM Mensaje COMPRESS

El **ICM \_ COMPRESS** notifica a un controlador de compresión de vídeo que comprime un marco de datos en un búfer definido por la aplicación.


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

Tamaño, en bytes, de [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

