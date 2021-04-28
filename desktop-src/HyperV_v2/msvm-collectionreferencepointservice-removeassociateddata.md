---
description: 'Método RemoveAssociatedData de la clase Msvm_CollectionReferencePointService : quita el registro de datos asociado al punto de referencia.'
ms.assetid: 42242b76-9123-41a7-b8b1-82d2e827ea53
title: Método RemoveAssociatedData de la Msvm_CollectionReferencePointService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66a5cf068545f31f9919a9da60a1b09b32f78e4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119233"
---
# <a name="removeassociateddata-method-of-the-msvm_collectionreferencepointservice-class"></a>Método RemoveAssociatedData de la clase CollectionReferencePointService de Msvm \_

Quita el registro de datos asociado al punto de referencia.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveAssociatedData(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedReferencePointCollection* \[ En\]
</dt> <dd>

Referencia a la colección de puntos de referencia del sistema virtual afectado.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación es de larga duración, opcionalmente se puede devolver un trabajo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, devuelve 0 (sin error) o 4096 (trabajo iniciado); de lo contrario, devuelva un error.

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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10 solo \[ aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Colección de \_ MsvmReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




