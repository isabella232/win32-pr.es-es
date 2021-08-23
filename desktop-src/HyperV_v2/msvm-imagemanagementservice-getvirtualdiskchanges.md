---
description: Recupera una lista de cambios en la región especificada de un disco virtual desde el identificador de Change Tracking resistente proporcionado o el identificador de instantánea vhdset.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Método GetVirtualDiskChanges de la Msvm_ImageManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8b96c5b4d2bbdff78b6f9f2bc9a1e7547742a553564e0f81547b8d998f86f14f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522565"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a>Método GetVirtualDiskChanges de la clase \_ ImageManagementService de Msvm

Recupera una lista de cambios en la región especificada de un disco virtual desde el identificador de Change Tracking resistente proporcionado o el identificador de instantánea vhdset.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ruta de acceso* \[ En\]
</dt> <dd>

Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual.

</dd> <dt>

*LimitId* \[ En\]
</dt> <dd>

Un identificador de Change Tracking resistente o id. de instantánea de conjunto de VHD que indica la línea base para los cambios en el disco virtual.

</dd> <dt>

*TargetSnapshotId* \[ En\]
</dt> <dd>

Identificador de instantánea VHDSet que indica la instantánea que se comparará con la línea de base cuando se desenlazen los cambios en el disco duro virtual. Este parámetro solo es válido para los archivos de conjunto de VHD.

</dd> <dt>

*ByteOffset* \[ En\]
</dt> <dd>

Desplazamiento de bytes de la región del disco virtual para el que se consultan los cambios.

</dd> <dt>

*ByteLength* \[ En\]
</dt> <dd>

Longitud de bytes de la región del disco virtual para la que se consultan los cambios. Debe ser menor que el tamaño del disco virtual.

</dd> <dt>

*ProcessedByteLength* \[ out\]
</dt> <dd>

Longitud total de bytes que se procesó. Puede ser igual a ByteLength o menor.

</dd> <dt>

*ChangedByteOffsets* \[ out\]
</dt> <dd>

Lista de desplazamientos de bytes en el disco virtual que indica el principio de cada intervalo modificado.

</dd> <dt>

*ChangedByteLengths* \[ out\]
</dt> <dd>

Lista de longitudes de bytes de los intervalos modificados en el disco virtual.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Referencia al trabajo (puede ser NULL si se completa la tarea).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes valores:

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

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




