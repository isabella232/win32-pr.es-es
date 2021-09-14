---
description: La clase WMI PortResource de Win32 \_ representa un puerto de E/S en un sistema de equipo que ejecuta Windows.
ms.assetid: 820f4f49-571c-4044-aefc-69bac5d59e6f
ms.tgt_platform: multiple
title: Win32_PortResource clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortResource
- Win32_PortResource.Alias
- Win32_PortResource.Caption
- Win32_PortResource.CreationClassName
- Win32_PortResource.CSCreationClassName
- Win32_PortResource.CSName
- Win32_PortResource.Description
- Win32_PortResource.EndingAddress
- Win32_PortResource.InstallDate
- Win32_PortResource.Name
- Win32_PortResource.StartingAddress
- Win32_PortResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3c08424dd1aee555068c78a9308afe732634c61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255633"
---
# <a name="win32_portresource-class"></a>Clase PortResource de Win32 \_

La clase WMI **\_ PortResource** [de](../wmisdk/retrieving-a-class.md) Win32 representa un puerto de E/S en un sistema de equipo que ejecuta Windows.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PortResource : Win32_SystemMemoryResource
{
  boolean  Alias;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a>Members

La **clase \_ PortResource de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PortResource de Win32** tiene estas propiedades.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Administrador de configuración Structures IO \| \_ INFO")
</dt> </dl>

Si **es TRUE,** esta instancia representa uno de los intervalos con un alias. Si **es FALSE,** la instancia representa una dirección de puerto base. Una dirección de puerto base es una dirección de puerto predeterminada dedicada a un servicio o dispositivo específico. Una dirección de alias de puerto es aquella a la que responde un dispositivo como si fuera la dirección real de un puerto de E/S.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**clave CIM \_**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nombre de la primera clase concreta que aparece en la cadena de herencia usada en la creación de una instancia de . Cuando se usa con las demás propiedades clave de la clase , la propiedad permite identificar de forma única todas las instancias de esta clase y sus subclases.

Esta propiedad se hereda de [**\_ CIM MemoryMappedIO.**](cim-memorymappedio.md)

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre de clase de creación del sistema de equipo de ámbito.

Esta propiedad se hereda de [**\_ CIM MemoryMappedIO.**](cim-memorymappedio.md)

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nombre del sistema de equipo de ámbito.

Esta propiedad se hereda de [**\_ CIM MemoryMappedIO.**](cim-memorymappedio.md)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Memory Mapped I/O \| 001.2")
</dt> </dl>

Dirección final de E/S asignada a memoria.

Esta propiedad se hereda de [**\_ CIM MemoryMappedIO.**](cim-memorymappedio.md)

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Fecha de instalación")
</dt> </dl>

Fecha y hora en que se instaló el objeto. Esta propiedad no necesita un valor para indicar que el objeto está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasifica, la propiedad se puede invalidar para que sea una propiedad de clave.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("StartingAddress"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. E/S asignadas a memoria DMTF \| \| 001.1")
</dt> </dl>

Dirección inicial de E/S asignada a memoria. La propiedad del identificador de recursos de hardware debe establecerse en este valor para construir la clave de recurso de E/S asignada.

Esta propiedad se hereda de [**\_ CIM MemoryMappedIO.**](cim-memorymappedio.md)

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente pero predecir un error en un futuro próximo). Entre los estados no operativo se incluyen: "Error", "Starting", "Stopping" y "Service". El último, "Servicio", podría aplicarse durante la resilvering de reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "Correcto" ni está en uno de los demás estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Los valores son los siguientes:

<dt>

<span id="OK"></span><span id="ok"></span>

**Ok** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unknown** ("Unknown")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Detención")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("Servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Estresado** ("estresado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("Sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comm perdido** ("Comm perdido")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ PortResource de Win32** se deriva de [**\_ SystemMemoryResource de Win32.**](win32-systemmemoryresource.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
