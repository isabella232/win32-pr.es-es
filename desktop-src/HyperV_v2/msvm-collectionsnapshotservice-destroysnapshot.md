---
description: Destruye una instantánea existente de la colección del sistema virtual. Este método puede destruir como efecto secundario otras instantáneas que dependen de la instantánea afectada.
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Método DestroySnapshot de la Msvm_CollectionSnapshotService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bacdb760580057516b6663bf53f5cd02a83f76148fa782ab875ca7385c053cb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431505"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Método DestroySnapshot de la clase \_ CollectionSnapshotService de Msvm

Destruye una instantánea existente de la colección del sistema virtual. Este método puede destruir como efecto secundario otras instantáneas que dependen de la instantánea afectada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedSnapshotCollection* \[ En\]
</dt> <dd>

Referencia a una [**colección CIM \_ que**](cim-collection.md) describe la colección de instantáneas del sistema virtual afectada.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica. Si está presente, la referencia devuelta a una instancia de [**\_ CIM ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0 (completado) o 4096 (trabajo iniciado); de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Tiempo de** espera (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
</dt> <dt>

**Tipo no** válido (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
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

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




