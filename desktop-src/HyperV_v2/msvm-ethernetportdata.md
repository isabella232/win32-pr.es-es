---
description: Clase abstracta que representa los datos de tiempo de ejecución de puerto recopilados por una extensión de conmutador Ethernet.
ms.assetid: bc41ad1d-e7ab-4d04-96a8-26eb68ea6601
title: Msvm_EthernetPortData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortData
- Msvm_EthernetPortData.InstanceID
- Msvm_EthernetPortData.Caption
- Msvm_EthernetPortData.Description
- Msvm_EthernetPortData.ElementName
- Msvm_EthernetPortData.SystemCreationClassName
- Msvm_EthernetPortData.SystemName
- Msvm_EthernetPortData.DeviceCreationClassName
- Msvm_EthernetPortData.DeviceID
- Msvm_EthernetPortData.CreationClassName
- Msvm_EthernetPortData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11f3f8841bb1101cb26efd142a31728eba21902cb0869432dfcf4676afaed96a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789995"
---
# <a name="msvm_ethernetportdata-class"></a>Clase Msvm \_ EthernetPortData

Clase abstracta que representa los datos de tiempo de ejecución de puerto recopilados por una extensión de conmutador Ethernet. Todas las clases de datos de puerto Ethernet deben derivarse de esta clase abstracta.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortData : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SystemCreationClassName;
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ EthernetPortData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ EthernetPortData** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de la subclase usada en la creación de esta instancia de datos de puerto.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**DeviceCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de clase de creación del sistema de ámbito. Esta propiedad siempre se establece en "Msvm \_ EthernetSwitchPort".

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Id. de dispositivo del puerto que tiene como ámbito esta instancia de datos de puerto.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

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

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Cadena que identifica de forma única esta instancia de datos de puerto dentro del ámbito del conmutador y el puerto.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de clase de creación del sistema de ámbito.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre del conmutador virtual que tiene como ámbito esta instancia de datos de puerto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

