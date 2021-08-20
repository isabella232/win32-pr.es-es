---
title: Método INapEnforcementClientConnection SetFlags (NapEnforcementClient.h)
description: Se usa para diferenciar las respuestas por primera vez de las respuestas debido a las solicitudes SoHRequest almacenadas en caché por los aplicadores. | Método INapEnforcementClientConnection SetFlags (NapEnforcementClient.h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- Método NAP de SetFlags
- Método NAP de SetFlags, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306ab4312138136dc00aec701d322ed82e95a731c8c4f418fb2cfaddd921ed50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133997"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a>INapEnforcementClientConnection::SetFlags (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapEnforcementClientConnection::SetFlags** se usa para diferenciar las respuestas por primera vez de las respuestas debido a soHRequests almacenados en caché por los aplicadores.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flags* \[ En\]
</dt> <dd>

Marcas que determinan si [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) se debe a una **soHRequest almacenada en caché.** Si *flags* tiene un valor [**de freshSoHRequest,**](nap-type-constants.md)es una nueva solicitud; De lo contrario, es una solicitud almacenada en caché.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

NapAgent establece este valor.

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

 

 





