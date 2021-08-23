---
title: Método INapEnforcementClientConnection GetFlags (NapEnforcementClient.h)
description: Se usa para diferenciar las respuestas por primera vez de las respuestas debido a soHRequests almacenados en caché por los aplicadores. | Método INapEnforcementClientConnection GetFlags (NapEnforcementClient.h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- Nap del método GetFlags
- Método GetFlags NAP , interfaz INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , Método GetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aea1815a8892f5d072f72d32d433070038b35cd663f10dfba08422a81153660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781055"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a>INapEnforcementClientConnection::GetFlags (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapEnforcementClientConnection::GetFlags** se usa para diferenciar las respuestas por primera vez de las respuestas debido a SoHRequests almacenadas en caché por los aplicadores.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flags* \[ out\]
</dt> <dd>

Puntero a una marca que determina si [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) se debe a una **soHRequest almacenada en caché.** Si *flags* tiene un valor [**de freshSoHRequest**](nap-type-constants.md), es una nueva solicitud; de lo contrario, es una solicitud almacenada en caché.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





