---
description: Exporte los datos de configuración que se pasarán al método ExportSnapshot de la \_ clase CollectionSnapshotService de Msvm.
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Msvm_CollectionSnapshotExportSettingData clase
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
ms.openlocfilehash: bd148b7ea73bf7c2eaff7f648c7084c37a8669779515749611c675e7f5564d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130635"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a>Clase Msvm \_ CollectionSnapshotExportSettingData

Exporte los datos de configuración que se pasarán al método ExportSnapshot de la [**\_ clase CollectionSnapshotService de Msvm.**](msvm-collectionsnapshotservice.md)

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

La **clase \_ CollectionSnapshotExportSettingData de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ CollectionSnapshotExportSettingData** tiene estas propiedades.

<dl> <dt>

**BackupIntent**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica la intención de cómo se usarían los conjuntos de copia de seguridad exportados:

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)


</dt> <dd>

Todos los conjuntos de copia de seguridad completos y diferenciales exportados se conservarían tal y como están.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)


</dt> <dd>

Los conjuntos de copia de seguridad completos y diferenciales exportados se combinarían para sintetizar conjuntos de copia de seguridad completos.

</dd> </dl>

</dd> <dt>

**CopyVmStorage**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es true,** el almacenamiento de la máquina virtual se copiará cuando se exporte la máquina virtual. De lo contrario, **false.**

</dd> <dt>

**DifferentialBackupBase**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Base para la exportación diferencial. Se trata de una ruta de acceso a una instancia [**\_ de Msvm ReferencePointCollection**](msvm-referencepointcollection.md) que representa el punto de referencia, o bien una ruta de acceso a una instancia de [**\_ SnapshotCollection de Msvm**](msvm-snapshotcollection.md) que representa la instantánea que se va a usar como base para la exportación diferencial.

</dd> </dl>

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




