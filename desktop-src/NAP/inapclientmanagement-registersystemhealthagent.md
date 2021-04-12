---
title: Método INapClientManagement RegisterSystemHealthAgent (NapManagement. h)
description: Registra un SHA con el sistema NAP.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- Método RegisterSystemHealthAgent NAP
- Método RegisterSystemHealthAgent NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método RegisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581c49a117a2b8aaa2c4dda2c6573e4a6327b688
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491710"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a>INapClientManagement:: RegisterSystemHealthAgent (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **RegisterSystemHealthAgent** registra un Sha con el sistema NAP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*agente* \[ de de\]
</dt> <dd>

Puntero a una estructura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contiene la información de registro para el Sha.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.



| Código devuelto                                                                                            | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Operación correcta.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**\_ \_ identificador conflictivo de NAP \_ E**</dt> </dl> | Un SHA que usa este identificador ya está registrado.<br/>         |



 

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

 

 





