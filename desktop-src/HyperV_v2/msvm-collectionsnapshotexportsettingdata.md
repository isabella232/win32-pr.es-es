---
description: Exportar los datos de configuración que se van a pasar al método ExportSnapshot de la \_ clase MSVM CollectionSnapshotService.
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Msvm_CollectionSnapshotExportSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3e146fe2e2af17223e792d86cff16bf1c4149dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666473"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a>MSVM \_ CollectionSnapshotExportSettingData (clase)

Exportar los datos de configuración que se van a pasar al método ExportSnapshot de la clase [**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md) .

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ CollectionSnapshotExportSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ CollectionSnapshotExportSettingData** tiene estas propiedades.

<dl> <dt>

**BackupIntent**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica la intención de usar los conjuntos de copia de seguridad exportados:

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)


</dt> <dd>

Todos los conjuntos de copia de seguridad completos y diferenciales exportados se conservarán tal como están.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)


</dt> <dd>

Los conjuntos de copia de seguridad completos y diferenciales exportados se combinarán para sintetizar los conjuntos de copia de seguridad completos.

</dd> </dl>

</dd> <dt>

**CopyVmStorage**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, el almacenamiento de la máquina virtual se copiará cuando se exporte la máquina virtual. En caso contrario, **false.**

</dd> <dt>

**DifferentialBackupBase**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Base para la exportación diferencial. Se trata de una ruta de acceso a una instancia de [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md) que representa el punto de referencia, o la ruta de acceso a una instancia de [**MSVM \_ SnapshotCollection**](msvm-snapshotcollection.md) que representa la instantánea que se va a usar como base para la exportación diferencial.

</dd> </dl>

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

[**SettingData de CIM \_**](cim-settingdata.md)
</dt> </dl>

 

 




