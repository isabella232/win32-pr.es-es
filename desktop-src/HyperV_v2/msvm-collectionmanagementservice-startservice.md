---
description: detiene el servicio.
ms.assetid: 0f9a015d-b895-496a-a4c6-2737c0742746
title: Método StartService de la clase Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f76fa9e5069c2a9e19b83a8ab83136879c6657e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688721"
---
# <a name="startservice-method-of-the-msvm_collectionmanagementservice-class"></a>Método StartService de la \_ clase MSVM CollectionManagementService

detiene el servicio.

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se realiza correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




