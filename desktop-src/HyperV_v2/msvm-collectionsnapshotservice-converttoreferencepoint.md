---
description: Convertir una instantánea de colección existente en una colección de puntos de referencia. La colección de instantáneas se elimina como un efecto secundario. Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Método ConvertToReferencePoint de la clase Msvm_CollectionSnapshotService
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
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913702"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a>Método ConvertToReferencePoint de la \_ clase CollectionSnapshotService de MSVM

Convertir una instantánea de colección existente en una colección de puntos de referencia. La colección de instantáneas se elimina como un efecto secundario. Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.

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

*AffectedSnapshotCollection* \[ de\]
</dt> <dd>

Referencia a un [**\_ SnapshotCollection de MSVM**](msvm-snapshotcollection.md) que contiene la colección de instantáneas del sistema virtual afectada.

</dd> <dt>

*ResultingReferencePointCollection* \[ in, out\]
</dt> <dd>

Referencia a un [**\_ ReferencePointCollection de MSVM**](msvm-referencepointcollection.md) que contiene la colección de puntos de referencia del sistema virtual resultante

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.

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

**Tiempo de espera** (3)
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

**Método reservado** (de no.. 32767)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
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

[**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




