---
title: Método IConnectionBrokerRequest CheckStatus (Cbclient. h)
description: Se llama para determinar el estado de una solicitud asincrónica.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- Método CheckStatus Servicios de Escritorio remoto
- Método CheckStatus Servicios de Escritorio remoto, interfaz IConnectionBrokerRequest
- Interfaz IConnectionBrokerRequest Servicios de Escritorio remoto, método CheckStatus
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
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422573"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a>IConnectionBrokerRequest:: CheckStatus (método)

Se llama para determinar el estado de una solicitud asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReqStatus* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe un valor de la enumeración del [**\_ \_ Estado de la solicitud CB**](cb-request-status.md) que indica el estado de la solicitud.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConnectionBrokerRequest**](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





