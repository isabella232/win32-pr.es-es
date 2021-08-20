---
title: ICM_COMPRESS_FRAMES_INFO mensaje (Vfw.h)
description: El ICM \_ COMPRESS \_ FRAMES INFO notifica a un controlador de \_ compresión que establezca los parámetros de la compresión pendiente.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- ICM_COMPRESS_FRAMES_INFO mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2382a930b0ce12e212adf78ddaf3c7e1b3300e47597b4671d0eae223cb536f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140916"
---
# <a name="icm_compress_frames_info-message"></a>\_ICM Mensaje DE \_ INFORMACIÓN DE COMPRESS FRAMES \_

El **ICM COMPRESS FRAMES \_ \_ \_ INFO** notifica a un controlador de compresión que establezca los parámetros de la compresión pendiente.


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icf"></span><span id="ICF"></span>*Icf*
</dt> <dd>

Puntero a una [**estructura ICCOMPRESSFRAMES.**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) Los **miembros GetData** **y PutData** de esta estructura no se usan con este mensaje.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamaño, en bytes, de [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

Un resalte puede usar este mensaje para determinar la cantidad de espacio que se debe asignar para cada fotograma durante la compresión.

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

 

 





