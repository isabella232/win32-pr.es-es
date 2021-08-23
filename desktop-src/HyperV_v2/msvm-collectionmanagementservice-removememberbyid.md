---
description: Quita el elemento administrado especificado como miembro de CIM \_ CollectionOfMSEs con el identificador especificado. Esto se realizará correctamente incluso si el objeto con ese identificador no está presente.
ms.assetid: 641535f0-ce71-4f57-a4e1-4775b3bb2374
title: Método RemoveMemberById de la Msvm_CollectionManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMemberById
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e371962198ea5a27228706a8b8ae7e65a30a9a8af4e5c3faa8276f7946cf4932
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682035"
---
# <a name="removememberbyid-method-of-the-msvm_collectionmanagementservice-class"></a>Método RemoveMemberById de la clase \_ CollectionManagementService de Msvm

Quita el elemento administrado especificado como miembro de [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) con el identificador especificado. Esto se realizará correctamente incluso si el objeto con ese identificador no está presente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveMemberById(
  [in]  CIM_ManagedElement REF Member,
  [in]  string                 CollectionId,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Miembro* \[ En\]
</dt> <dd>

Miembro que se va a quitar.

</dd> <dt>

*CollectionId* \[ En\]
</dt> <dd>

Identificador de colección de la colección de la que se quitará el miembro.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Referencia al trabajo (puede ser NULL si se completa la tarea).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se realiza correctamente o 4096 si se inició el trabajo; de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> <dt>

**Archivo no encontrado** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CollectionManagementService de Msvm \_**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




