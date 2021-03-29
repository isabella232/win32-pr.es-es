---
title: Mensaje de ICM_COMPRESS_FRAMES_INFO (VFW. h)
description: El \_ mensaje de información de tramas compress de ICM \_ \_ notifica a un controlador de compresión que establezca los parámetros para la compresión pendiente.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- Mensaje de ICM_COMPRESS_FRAMES_INFO de Windows multimedia
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
ms.openlocfilehash: cbb6df0eab7706ebfc03a5e3069d4323be26ecdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492358"
---
# <a name="icm_compress_frames_info-message"></a>\_Mensaje de \_ información de marcos de compresión ICM \_

El mensaje de **\_ \_ \_ información de tramas compress de ICM** notifica a un controlador de compresión que establezca los parámetros para la compresión pendiente.


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icf"></span><span id="ICF"></span>*probar*
</dt> <dd>

Puntero a una estructura [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) . Los miembros **GetData** y **PutData** de esta estructura no se usan con este mensaje.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamaño, en bytes, de [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Un compresor puede usar este mensaje para determinar la cantidad de espacio que se va a asignar a cada fotograma durante la compresión.

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

 

 





