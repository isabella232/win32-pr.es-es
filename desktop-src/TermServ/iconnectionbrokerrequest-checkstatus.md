---
title: Método IConnectionBrokerRequest CheckStatus (Cbclient.h)
description: Se llama para determinar el estado de una solicitud asincrónica.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- Método CheckStatus Servicios de Escritorio remoto
- Método CheckStatus Servicios de Escritorio remoto , interfaz IConnectionBrokerRequest
- Interfaz IConnectionBrokerRequest Servicios de Escritorio remoto , método CheckStatus
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d2409c739e0d65315e512a4e9dd7027e4cc63f5b7ac36883ed766f215a7ec91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059183"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a>IConnectionBrokerRequest::CheckStatus (método)

Se llama para determinar el estado de una solicitud asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReqStatus* \[ out\]
</dt> <dd>

Dirección de una variable que recibe un valor de la enumeración [**CB \_ REQUEST \_ STATUS**](cb-request-status.md) que indica el estado de la solicitud.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Cbclient.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConnectionBrokerRequest**](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





