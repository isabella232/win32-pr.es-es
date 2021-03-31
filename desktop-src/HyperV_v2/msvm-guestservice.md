---
description: MSVM \_ GuestService es la clase base abstracta para los servicios del invitado a los que se puede tener acceso desde el host.
ms.assetid: F9E6FFE6-B8C5-4F06-BF22-A4BDB20F813A
title: Msvm_GuestService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService
- Msvm_GuestService.Caption
- Msvm_GuestService.CreationClassName
- Msvm_GuestService.Description
- Msvm_GuestService.InstallDate
- Msvm_GuestService.Name
- Msvm_GuestService.Started
- Msvm_GuestService.StartMode
- Msvm_GuestService.Status
- Msvm_GuestService.SystemCreationClassName
- Msvm_GuestService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99d1936a2678fc2d8357974f9c11a250a1d9bce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423699"
---
# <a name="msvm_guestservice-class"></a>MSVM \_ GuestService (clase)

**MSVM \_ GuestService** es la clase base abstracta para los servicios del invitado a los que se puede tener acceso desde el host. Esta clase deriva de la clase [**de \_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service) .

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, AMENDMENT]
class Msvm_GuestService : CIM_Service
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
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ GuestService** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MSVM \_ GuestService** tiene estos métodos.



| Método                                                             | Descripción                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**RequestStateChange**](requeststatechange-msvm-guestservice.md) | Solicita que el estado del servicio invitado cambie al valor especificado.<br/> |
| [**StartService**](startservice-msvm-guestservice.md)             | Pone el servicio invitado en un estado Iniciado. <br/>                                     |
| [**StopService**](stopservice-msvm-guestservice.md)               | Detiene el servicio invitado. <br/>                                                       |



 

### <a name="properties"></a>Propiedades

La clase **MSVM \_ GuestService** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción textual del objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

[**\_Servicio CIM**](cim-service.md)
</dt> <dt>

[**\_Servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

