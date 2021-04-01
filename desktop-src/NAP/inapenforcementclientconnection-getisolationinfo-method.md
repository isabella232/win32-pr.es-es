---
title: Método INapEnforcementClientConnection GetIsolationInfo (NapEnforcementClient. h)
description: Se usa para obtener la información de aislamiento del cliente.
ms.assetid: 33040554-dcbe-4563-b047-fc7e28bac55c
keywords:
- Método GetIsolationInfo NAP
- Método GetIsolationInfo NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método GetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890f7268801fda77a9794ed21c4d36e78a52dd5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997134"
---
# <a name="inapenforcementclientconnectiongetisolationinfo-method"></a>INapEnforcementClientConnection:: GetIsolationInfo (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapEnforcementClientConnection:: GetIsolationInfo** se usa para obtener la información de aislamiento del cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIsolationInfo(
  [out] IsolationInfo **isolationInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isolationInfo* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contiene el estado de Conectividad del cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

La NapAgent establece esta información después de procesar una [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) y el exigidor no debe establecerla.

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

 

 





