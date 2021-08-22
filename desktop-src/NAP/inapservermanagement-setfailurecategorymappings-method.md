---
title: Método INapServerManagement SetFailureCategoryMappings (NapServerManagement.h)
description: Se usa para establecer las asignaciones de categorías de error de SHV.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- Método NAP de SetFailureCategoryMappings
- Método NAP de SetFailureCategoryMappings, interfaz INapServerManagement
- Interfaz INapServerManagement NAP, método SetFailureCategoryMappings
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
ms.openlocfilehash: c22bc51edf887d26bf34f59932248c62bfca86199771a2b971a10e9c1b323eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939619"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a>Método INapServerManagement::SetFailureCategoryMappings

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapServerManagement::SetFailureCategoryMappings** se usa para establecer las asignaciones de categoría de error de SHV.

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

Estructura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) que contiene los datos de asignación de categorías de error.

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
| Header<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





