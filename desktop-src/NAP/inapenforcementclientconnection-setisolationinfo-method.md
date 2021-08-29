---
title: Método INapEnforcementClientConnection SetIsolationInfo (NapEnforcementClient.h)
description: NapAgent lo usa para establecer la información de aislamiento del cliente.
ms.assetid: e92d8762-4ae9-40e5-a18e-7da757aa6f9e
keywords:
- Método NAP de SetIsolationInfo
- Método NAP de SetIsolationInfo , interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042f0d7f6f6b36172b33cd681f2c605ff0f83b0eec987a71ee2643bf510f02ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133987"
---
# <a name="inapenforcementclientconnectionsetisolationinfo-method"></a>Método INapEnforcementClientConnection::SetIsolationInfo

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

NapAgent usa el método **INapEnforcementClientConnection::SetIsolationInfo** para establecer la información de aislamiento del cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetIsolationInfo(
  [in] const IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isolationInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contiene el estado de conectividad del cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

NapAgent establece esta información después de procesar un SoHResponse y el aplicador no debe establecer esta información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





