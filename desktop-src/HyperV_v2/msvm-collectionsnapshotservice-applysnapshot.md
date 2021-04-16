---
description: Aplica una colección de instantáneas a la colección de sistemas del equipo virtual.
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Método ApplySnapshot de la clase Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1fa5b664b39541b9d697dfbbfd0493f7a6f7cf96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686743"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Método ApplySnapshot de la \_ clase CollectionSnapshotService de MSVM

Aplica una colección de instantáneas a la colección de sistemas del equipo virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SnapshotCollection* \[ de\]
</dt> <dd>

Referencia a una [**\_ colección CIM**](cim-collection.md) que representa la colección de instantáneas que se va a aplicar.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica. Si está presente, la referencia devuelta a una instancia de [**CIM \_ ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve un 0; de lo contrario, devuelve un error.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




