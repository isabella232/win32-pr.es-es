---
title: Método INapServerManagement RegisterSystemHealthValidator (NapServerManagement.h)
description: Registra una SHV.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- Nap del método RegisterSystemHealthValidator
- Método NAP de RegisterSystemHealthValidator, interfaz INapServerManagement
- Interfaz INapServerManagement NAP, método RegisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb5dc93c5bb927ffb25df20f37e5b2c30560153efb006f3c91bf7e97efec360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012573"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a>Método INapServerManagement::RegisterSystemHealthValidator

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapServerManagement::RegisterSystemHealthValidator** registra una SHV.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*validador* \[ En\]
</dt> <dd>

Puntero a una [**estructura NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contiene la información de registro de SHV.

</dd> <dt>

*validatorClsid* \[ En\]
</dt> <dd>

Puntero al CLSID de la clase COM que implementa la [**interfaz INapSystemHealthValidator.**](inapsystemhealthvalidator.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                            | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                  | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | El límite de recursos del sistema no pudo realizar la operación.<br/> |
| <dl> <dt>**NAP \_ E \_ CONFLICTING \_ ID**</dt> </dl> | El identificador de SHV ya está registrado.<br/>                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





