---
description: Describe las funciones del sistema de equipo de Msvm \_ asociado.
ms.assetid: 7e3b51ba-f85d-4b83-abc6-a094d412eca1
title: Msvm_VirtualSystemCapabilities clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCapabilities
- Msvm_VirtualSystemCapabilities.InstanceID
- Msvm_VirtualSystemCapabilities.Caption
- Msvm_VirtualSystemCapabilities.Description
- Msvm_VirtualSystemCapabilities.ElementName
- Msvm_VirtualSystemCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemCapabilities.MaxElementNameLen
- Msvm_VirtualSystemCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4b25f28c0ae75be9bc9b6cdb0ff752e99befb18131c758bd1ae461c909b1bf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789215"
---
# <a name="msvm_virtualsystemcapabilities-class"></a>Clase Msvm \_ VirtualSystemCapabilities

Describe las funciones del sistema de [**equipos de Msvm \_ asociado.**](msvm-computersystem.md)

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Capabilities";
  string  Description = "Defines Virtual System Capabilities";
  string  ElementName = "Hyper-V Virtual System Capabilities";
  boolean ElementNameEditSupported = True;
  unit16  MaxElementNameLen = 100;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a>Miembros

La **clase \_ VirtualSystemCapabilities de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ VirtualSystemCapabilities** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede modificar la propiedad **ElementName.** Esta propiedad se hereda de **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica las restricciones en **ElementName**, expresadas como una expresión regular. Esta propiedad se hereda de **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo de datos: **unit16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxValue** (256)
</dt> </dl>

Especifica la longitud máxima admitida de la **propiedad ElementName.** Esta propiedad se hereda de **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz unit16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los posibles estados que se pueden solicitar al usar el **método RequestStateChange** en el elemento lógico habilitado. Esta propiedad se hereda de **CIM \_ EnabledLogicalElementCapabilities.**



| Value                                                                         | Significado              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | habilitado<br/>   |
| <dl> <dt>3</dt> </dl>  | Deshabilita<br/>  |
| <dl> <dt>4</dt> </dl>  | Apagar<br/> |
| <dl> <dt>6</dt> </dl>  | Sin conexión<br/>   |
| <dl> <dt>7</dt> </dl>  | Prueba<br/>      |
| <dl> <dt>8</dt> </dl>  | Aplazar<br/>     |
| <dl> <dt>9</dt> </dl>  | Modo de inactividad<br/>   |
| <dl> <dt>10</dt> </dl> | Reboot<br/>    |
| <dl> <dt>11</dt> </dl> | Reset<br/>     |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

