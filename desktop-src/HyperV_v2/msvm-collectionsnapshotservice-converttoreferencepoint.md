---
description: Convertir una instantánea de colección existente en una colección de puntos de referencia. La colección de instantáneas se elimina como efecto secundario. Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Método ConvertToReferencePoint de la Msvm_CollectionSnapshotService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97faedea1cdb852e26f6b94211586e5539075c0a225bf98f1a10cf45305d7296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148871"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a>Método ConvertToReferencePoint de la clase \_ CollectionSnapshotService de Msvm

Convertir una instantánea de colección existente en una colección de puntos de referencia. La colección de instantáneas se elimina como efecto secundario. Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedSnapshotCollection* \[ En\]
</dt> <dd>

Referencia a [**Msvm \_ SnapshotCollection que**](msvm-snapshotcollection.md) contiene la colección de instantáneas del sistema virtual afectada.

</dd> <dt>

*ResultingReferencePointCollection* \[ in, out\]
</dt> <dd>

Referencia a una [**colección \_ ReferencePointCollection de Msvm**](msvm-referencepointcollection.md) que contiene la colección de puntos de referencia del sistema virtual resultante

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación es de larga duración, opcionalmente se puede devolver un trabajo.

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

**Tipo no válido** (6)
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

[**Colección de \_ MsvmSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




