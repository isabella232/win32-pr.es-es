---
title: Método INapServerManagement SetFailureCategoryMappings (NapServerManagement.h)
description: Se usa para establecer las asignaciones de categoría de error de SHV.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- Método NAP de SetFailureCategoryMappings
- Método NAP de SetFailureCategoryMappings, interfaz INapServerManagement
- INapServerManagement interface NAP , SetFailureCategoryMappings method
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a220d6603ef5bbb49377ac0e212d5d98afa4bdd0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473770"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a>Método INapServerManagement::SetFailureCategoryMappings

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapServerManagement::SetFailureCategoryMappings** se usa para establecer las asignaciones de categorías de error de SHV.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*id* \[ en\]
</dt> <dd>

[**SystemHealthEntityId que**](nap-type-constants.md) contiene el identificador único de la SHV.

</dd> <dt>

*asignación* \[ En\]
</dt> <dd>

Estructura [**FailureCategoryMapping que**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) contiene los datos de asignación de categoría de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





