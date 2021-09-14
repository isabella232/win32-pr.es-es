---
title: ICM_SET_STATUS_PROC mensaje (Vfw.h)
description: El ICM SET STATUS PROC proporciona una función de devolución de llamada \_ de estado con el estado de una operación \_ \_ larga.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- ICM_SET_STATUS_PROC mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246255"
---
# <a name="icm_set_status_proc-message"></a>\_ICM Mensaje \_ SET STATUS \_ PROC

El **ICM SET STATUS \_ \_ \_ PROC** proporciona una función de devolución de llamada de estado con el estado de una operación larga.


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*
</dt> <dd>

Puntero a una [**estructura ICSETSTATUSPROC.**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamaño, en bytes, de **ICSETSTATUSPROC**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

La compatibilidad con este mensaje es opcional, pero se recomienda encarecidamente si la compresión o la descompresión tardan más de una décima parte aproximadamente de un segundo.

Una aplicación puede enviar este mensaje periódicamente a una función de devolución de llamada de estado durante operaciones largas.

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

 

 





