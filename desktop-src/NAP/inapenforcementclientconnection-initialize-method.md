---
title: Método Initialize INapEnforcementClientConnection (NapEnforcementClient. h)
description: Inicializa la conexión de cliente.
ms.assetid: da72bfc3-9551-4fb0-b9a5-2931c14f618f
keywords:
- Inicializar el método NAP
- Inicializar método NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51f12025bbddb8a9e795a97f2ed443344327a17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489886"
---
# <a name="inapenforcementclientconnectioninitialize-method"></a>INapEnforcementClientConnection:: Initialize (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapEnforcementClientConnection:: Initialize** inicializa la conexión de cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ID.* \[ en\]
</dt> <dd>

Un puntero a un [**EnforementEntityId**](nap-datatypes.md) que identifica el cliente de cumplimiento que solicita la conexión. NapAgent establece este valor durante la creación de la conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





