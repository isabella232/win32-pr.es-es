---
title: Método INapServerManagement RegisterSystemHealthValidator (NapServerManagement. h)
description: Registra un SHV.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- Método RegisterSystemHealthValidator NAP
- Método RegisterSystemHealthValidator NAP, interfaz INapServerManagement
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
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274559"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a>INapServerManagement:: RegisterSystemHealthValidator (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapServerManagement:: RegisterSystemHealthValidator** registra un SHV.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*validador* \[ de\]
</dt> <dd>

Puntero a una estructura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contiene la información de registro de SHV.

</dd> <dt>

*validatorClsid* \[ de\]
</dt> <dd>

Puntero al CLSID de la clase COM que implementa la interfaz [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                            | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                  | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**\_ \_ identificador conflictivo de NAP \_ E**</dt> </dl> | El ID. de SHV ya está registrado.<br/>                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





