---
title: Método INapEnforcementClientConnection SetEnforcerPrivateData (NapEnforcementClient.h)
description: Lo usa el aplicador para establecer datos privados.
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- Método NAP de SetEnforcerPrivateData
- Método NAP de SetEnforcerPrivateData, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebf42212d55f059286aa7b3d67f965b3b861755cc0291e57f339465291e5099
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368104"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a>Método INapEnforcementClientConnection::SetEnforcerPrivateData

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El aplicador usa el método **INapEnforcementClientConnection::SetEnforcerPrivateData** para establecer datos privados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*privateData* \[ En\]
</dt> <dd>

Puntero a un blob [**de datos opacos PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que solo el ejecutor puede interpretar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





