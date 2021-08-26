---
title: CB_REQUEST_STATUS enumeración (Cbclient.h)
description: Especifica el estado de una solicitud asincrónica.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- CB_REQUEST_STATUS enumeración Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6647f10ab91fd5cb1919d49c4c00d22b8b1722de9b20d9b83fdee8fcceaef95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871975"
---
# <a name="cb_request_status-enumeration"></a>Enumeración \_ CB REQUEST \_ STATUS

Especifica el estado de una solicitud asincrónica. Esta enumeración se usa con el [**método IConnectionBrokerRequest::CheckStatus.**](iconnectionbrokerrequest-checkstatus.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**ESTADO DE \_ CB \_ NO VÁLIDO**
</dt> <dd>

El objeto de solicitud no se inicializa.

</dd> <dt>

<span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**SOLICITUD \_ DE INICIO DE ESTADO \_ DE CB \_**
</dt> <dd>

No se usa.

</dd> <dt>

<span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**SOLICITUD \_ DE ESTADO DE CB \_ \_ COMPLETADA**
</dt> <dd>

La solicitud se ha completado.

</dd> <dt>

<span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**ERROR \_ EN LA SOLICITUD DE ESTADO \_ DE CB \_**
</dt> <dd>

Error en la solicitud.

</dd> <dt>

<span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**SOLICITUD \_ DE ESTADO CB \_ \_ ANULADA**
</dt> <dd>

Se anuló la solicitud.

</dd> <dt>

<span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**DESTINO \_ DE BÚSQUEDA DE ESTADO \_ \_ DE CB**
</dt> <dd>

No se usa.

</dd> <dt>

<span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**DESTINO DE \_ CARGA DE ESTADO DE \_ \_ CB**
</dt> <dd>

No se usa.

</dd> <dt>

<span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**ESTADO DE \_ CB QUE LLEVA LA SESIÓN EN \_ \_ \_ LÍNEA**
</dt> <dd>

No se usa.

</dd> <dt>

<span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**REDIRECCIONAMIENTO \_ DEL ESTADO CB AL \_ \_ \_ DESTINO**
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





