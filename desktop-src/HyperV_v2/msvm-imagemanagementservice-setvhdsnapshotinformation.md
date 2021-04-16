---
description: Edita una entrada de instantánea de VHD dentro de un archivo de conjunto de VHD. Si el ID. de instantánea en cuestión ya existe, la entrada de instantánea existente se sobrescribirá con la nueva entrada. De lo contrario, la nueva entrada se agregará al archivo del conjunto de VHD.
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: Método SetVHDSnapshotInformation de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 54f5ac23cdf8f49532a05eee3fd23293715cd02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666609"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>Método SetVHDSnapshotInformation de la \_ clase ImageManagementService de MSVM

Edita una entrada de instantánea de VHD dentro de un archivo de conjunto de VHD. Si el ID. de instantánea en cuestión ya existe, la entrada de instantánea existente se sobrescribirá con la nueva entrada. De lo contrario, la nueva entrada se agregará al archivo del conjunto de VHD.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Información* \[ de de\]
</dt> <dd>

Información de instantánea de VHD que se va a cambiar o agregar en el archivo de VHD set. La cadena es una instancia incrustada de [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Referencia al trabajo (puede ser null si se ha completado la tarea).

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

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> <dt>

**No se encontró el archivo** (32779)
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

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




