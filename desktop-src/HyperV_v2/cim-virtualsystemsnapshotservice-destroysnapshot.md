---
description: Destruir una instantánea del sistema virtual existente. Este método puede destruir como efecto secundario otras instantáneas que dependen de la instantánea afectada.
ms.assetid: 69f60d0e-50ef-4a38-ad4b-88534b7fb3f8
title: Método DestroySnapshot de la CIM_VirtualSystemSnapshotService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 986ffe6a7a5bd6ac18d47bcbebe40ac038ea86cdc096173704d30515067fcccc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646374"
---
# <a name="destroysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>Método DestroySnapshot de la clase \_ CIM VirtualSystemSnapshotService

Destruir una instantánea del sistema virtual existente. Este método puede destruir como efecto secundario otras instantáneas que dependen de la instantánea afectada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedSnapshot* \[ En\]
</dt> <dd>

Una [**referencia CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) a la instantánea del sistema virtual afectada.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación es de larga duración, opcionalmente se puede devolver [**un \_ concretejob CIM**](cim-concretejob.md) que representa el trabajo.

> [!Note]  
> Este parámetro era de lectura y escritura en Windows 8.1.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ VirtualSystemSnapshotService**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




