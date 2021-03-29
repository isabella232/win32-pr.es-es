---
title: Mensaje de ICM_SET_STATUS_PROC (VFW. h)
description: El \_ mensaje del \_ procedimiento set \_ de estado de ICM proporciona una función de devolución de llamada de estado con el estado de una operación larga.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- Mensaje de ICM_SET_STATUS_PROC de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d7ad2745ab53c2e04a1588ddbf1b1e5d755202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493282"
---
# <a name="icm_set_status_proc-message"></a>\_Mensaje de procedimiento para establecer estado de ICM \_ \_

El mensaje del **\_ \_ \_ procedimiento set de estado de ICM** proporciona una función de devolución de llamada de estado con el estado de una operación larga.


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*
</dt> <dd>

Puntero a una estructura [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamaño, en bytes, de **ICSETSTATUSPROC**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La compatibilidad de este mensaje es opcional, pero se recomienda encarecidamente si la compresión o descompresión tarda más de aproximadamente una décima de segundo.

Una aplicación puede enviar este mensaje periódicamente a una función de devolución de llamada de estado durante las operaciones largas.

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

 

 





