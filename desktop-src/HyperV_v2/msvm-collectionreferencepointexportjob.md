---
description: Esta clase representa un trabajo de operación de exportación de punto de referencia de colección.
ms.assetid: c752ff1d-163c-4aa9-b29e-76478a18a08c
title: Msvm_CollectionReferencePointExportJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob
- Msvm_CollectionReferencePointExportJob.Cancellable
- Msvm_CollectionReferencePointExportJob.ErrorSummaryDescription
- Msvm_CollectionReferencePointExportJob.CollectionId
- Msvm_CollectionReferencePointExportJob.ReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.BaseReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.VirtualMachineId
- Msvm_CollectionReferencePointExportJob.ExportDirectory
- Msvm_CollectionReferencePointExportJob.ExportedDisks
- Msvm_CollectionReferencePointExportJob.ExportedLogFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedConfigFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedRuntimeFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedGuestStateFilePaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3baf6405f160401b3a2fe8024861d92560484a513e1c55436f9e149e92daed7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681915"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a>Clase \_ CollectionReferencePointExportJob de Msvm

Esta clase representa un trabajo de operación de exportación de punto de referencia de colección.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  CollectionId;
  string  ReferencePointGroupId;
  string  BaseReferencePointGroupId;
  string  VirtualMachineId[];
  string  ExportDirectory;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePaths[];
  string  ExportedRuntimeFilePaths[];
  string  ExportedGuestStateFilePaths[];
};
```

## <a name="members"></a>Miembros

La **clase \_ CollectionReferencePointExportJob de Msvm** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ CollectionReferencePointExportJob de Msvm** tiene estos métodos.



| Método                                                                                  | Descripción                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**GetError**](msvm-collectionreferencepointexportjob-geterror.md)                     | Recupera un error.<br/>                     |
| [**GetErrorEx**](msvm-collectionreferencepointexportjob-geterrorex.md)                 | Recupera información de error adicional.<br/> |
| [**RequestStateChange**](msvm-collectionreferencepointexportjob-requeststatechange.md) | Solicita un cambio de estado.<br/>                |



 

### <a name="properties"></a>Propiedades

La **clase \_ CollectionReferencePointExportJob de Msvm** tiene estas propiedades.

<dl> <dt>

**BaseReferencePointGroupId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID del punto de referencia de colección que se usa como base en la operación exportoperation.

</dd> <dt>

**Cancelable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede cancelar el trabajo. El valor de esta propiedad no garantiza que una solicitud para cancelar el trabajo se realizará correctamente.

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID del grupo de máquinas virtuales para el que se hanexportado los archivos de registro.

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Cim \_ Job**](cim-job.md).**ErrorCode**")
</dt> </dl>

Contiene una descripción de resumen de errores.

</dd> <dt>

**ExportDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ubicación de exportación.

</dd> <dt>

**ExportedConfigFilePaths**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del archivo de configuración de la máquina virtual exportada.

</dd> <dt>

**ExportedDisks**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los ID de instancia de los discos virtuales para los que se exportaron los archivos de registro.

</dd> <dt>

**ExportedGuestStateFilePaths**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del archivo de estado de invitado de la máquina virtual exportada.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**ExportedLogFilePaths**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Rutas de acceso de los archivos de registro que se exportaron.

</dd> <dt>

**ExportedRuntimeFilePaths**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del archivo de estado en tiempo de ejecución de la máquina virtual exportada.

</dd> <dt>

**ReferencePointGroupId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID del punto de referencia de colección que se exporta.

</dd> <dt>

**VirtualMachineId**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID de las máquinas virtuales para las que se ha realizado la operación de exportación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1703 \[ solo para aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ConcreteJob**](cim-concretejob.md)
</dt> </dl>

 

