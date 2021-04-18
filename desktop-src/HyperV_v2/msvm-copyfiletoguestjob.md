---
description: Representa un trabajo de operación del servicio de archivos invitados.
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Msvm_CopyFileToGuestJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57e27b4ba610eea4559f3b045b2d823661cf4cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667823"
---
# <a name="msvm_copyfiletoguestjob-class"></a>MSVM \_ CopyFileToGuestJob (clase)

Representa un trabajo de operación del servicio de archivos invitados. Esta clase deriva de [**MSVM \_ GuestFileService**](msvm-guestfileservice.md).

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ CopyFileToGuestJob** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MSVM \_ CopyFileToGuestJob** tiene estos métodos.



| Método                                                                   | Descripción                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**CopyFilesToGuest**](copyfilestoguest-msvm-guestfileservice.md)       | Copia archivos del host de Hyper-V a la máquina virtual.<br/> |
| [**GetError**](geterror-msvm-copyfiletoguestjob.md)                     | Recupera el objeto de error del trabajo.<br/>                    |
| [**GetErrorEx**](geterrorex-msvm-copyfiletoguestjob.md)                 | Recupera los objetos de error del trabajo.<br/>                   |
| [**RequestStateChange**](requeststatechange-msvm-copyfiletoguestjob.md) | Cambia el estado del trabajo.<br/>                              |
| **StartService**                                                         | No se admite este método.<br/>                              |
| **StopService**                                                          | No se admite este método.<br/>                              |



 

### <a name="properties"></a>Propiedades

La clase **MSVM \_ CopyFileToGuestJob** tiene estas propiedades.

<dl> <dt>

**Cancelable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede cancelar el trabajo. El valor de esta propiedad no garantiza que una solicitud para cancelar el trabajo se realizará correctamente. Si **es true**, el trabajo se puede cancelar; en caso contrario, **false**.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción textual del objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CopyFileToGuestSettingData**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Establecer los datos que se usan para copiar un archivo.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase o subclase utilizada en la creación de una instancia de. Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabajo de CIM**](cim-job.md).**ErrorCode**")
</dt> </dl>

Descripción breve del error, si está presente. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se instaló el objeto. Esta propiedad no necesita un valor para indicar que el objeto está instalado. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único para el servicio que también proporciona una indicación de la funcionalidad que se administra. Para obtener más información sobre la funcionalidad, vea la propiedad **Description** del objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Iniciado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, el servicio se ha iniciado.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servicio se inicia automáticamente (por ejemplo, por un sistema operativo) o solo se inicia después de la solicitud.

Los valores son los siguientes:

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

**Automático**
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

**Manualmente**
</dt> </dl>

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

Los valores son los siguientes:

<dl><span id="OK"></span><span id="ok"></span><dt>

**ACEPTAR**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**Error**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**Degradado**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**Unknown**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Pred FAIL"**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**Comenzar**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**Bloqueo**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**Servicio**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**Calca**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"Recover"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Sin contacto"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Pérdida de comunicación"**
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase de creación del sistema de ámbito.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del sistema que hospeda el servicio.

</dd> <dt>

**VirtualSystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID del sistema virtual afectado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_CONCRETEJOB CIM**](cim-concretejob.md)
</dt> <dt>

[**MSVM \_ GuestFileService**](msvm-guestfileservice.md)
</dt> <dt>

[**MSVM \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

