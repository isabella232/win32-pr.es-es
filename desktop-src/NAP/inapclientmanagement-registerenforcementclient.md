---
title: Método INapClientManagement RegisterEnforcementClient (NapManagement. h)
description: Registra un cliente de cumplimiento con el sistema NAP.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- Método RegisterEnforcementClient NAP
- Método RegisterEnforcementClient NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método RegisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ed4b5fe5a97d60b764341f21f25628c3c3434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150624"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a>INapClientManagement:: RegisterEnforcementClient (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **RegisterEnforcementClient** registra un cliente de cumplimiento con el sistema NAP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*aplicación forzada* \[ de\]
</dt> <dd>

Puntero a una estructura de datos [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contiene la información de registro asociada al cliente de cumplimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.



| Código devuelto                                                                                            | Descripción                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Operación correcta.<br/>                                                  |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Límite de recursos del sistema, no se pudo realizar la operación.<br/>                |
| <dl> <dt>**\_ \_ identificador conflictivo de NAP \_ E**</dt> </dl> | Ya está registrado un agente de cumplimiento con el identificador especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





