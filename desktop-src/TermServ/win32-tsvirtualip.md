---
title: Win32_TSVirtualIP clase
description: Define la configuración de virtualización del protocolo de Internet (IP) para un Escritorio remoto host de sesión de escritorio remoto.
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualIP clase Servicios de Escritorio remoto
- Win32_TSVirtualIP clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28830e44fd54e9246cb0affc5fdde1427673d92e843adfd3e1e19cd221af370e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769055"
---
# <a name="win32_tsvirtualip-class"></a>Clase \_ TSVirtualIP de Win32

Define la configuración de virtualización del protocolo de Internet (IP) para un Escritorio remoto host de sesión de escritorio remoto.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSVirtualIP de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ TSVirtualIP de Win32** tiene estos métodos.



| Método                                                                                                   | Descripción                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddProgram**](addprogram-win32-tsvirtualip.md)                                                       | Agrega un programa a la lista de programas que usan la virtualización IP.<br/>                                                                                                |
| [**RemoveProgram**](removeprogram-win32-tsvirtualip.md)                                                 | Quita un programa de la lista de programas que usan la virtualización ip.<br/>                                                                                           |
| [**SeleccioneNetworkAdapter.**](selectnetworkadapter-win32-tsvirtualip.md)                                   | Establece la dirección MAC del adaptador de red que se usará para la virtualización de IP.<br/>                                                                                         |
| [**SetProgramList**](setprogramlist-win32-tsvirtualip.md)                                               | Sobrescribe la lista de programas que usan la virtualización de IP.<br/>                                                                                                       |
| [**SetVirtualIPActive**](setvirtualipactive-win32-tsvirtualip.md)                                       | Establece el **valor de la propiedad VirtualIPActive.**<br/>                                                                                                                      |
| [**SetVirtualIPMode**](setvirtualipmode-win32-tsvirtualip.md)                                           | Establece el **valor de la propiedad VirtualIPMode.**<br/>                                                                                                                        |
| [**SetVirtualizeLoopbackAddressesEnabled**](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | Establece el **valor de la propiedad VirtualizeLoopbackAddressesEnabled.**<br/> **Windows Server 2008 R2:** Este método no está disponible antes de Windows Server 2012.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSVirtualIP de Win32** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Descripción breve (cadena de una línea) del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Fecha en que se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NetworkAdapterDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del adaptador de red.

</dd> <dt>

**NetworkAdapterDescriptionList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de descripciones de los adaptadores de red físicos disponibles.

</dd> <dt>

**NetworkAdapterMacAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección MAC del adaptador de red.

</dd> <dt>

**NetworkAdapterMacList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de direcciones MAC de los adaptadores de red físicos disponibles.

</dd> <dt>

**PolicySourceNetworkAdapter**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el adaptador de red está configurado por el servidor o por la directiva de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceProgramList**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **ProgramList** está configurada por el servidor o por la directiva de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceVirtualIPActive**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servidor o la directiva de grupo configuran la propiedad **VirtualIPActive.**

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceVirtualIPMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servidor o la directiva de grupo configuran la propiedad **VirtualIPMode.**

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**ProgramList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica los programas que están configurados para usar la virtualización ip. Puede ser un nombre de programa o la ruta de acceso completa.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente pero predecir un error en un futuro próximo). Los estados no operativo incluyen: "Error", "Starting", "Stopping" y "Service". El último, "Servicio", podría aplicarse durante la resilvering de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "correcto" ni está en uno de los demás estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>



 ("Ok")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconocido")


</dt> <dd></dd> <dt>



 ("Error previo")


</dt> <dd></dd> <dt>



 ("Starting")


</dt> <dd></dd> <dt>



 ("Deteniendo")


</dt> <dd></dd> <dt>



 ("Servicio")


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualIPActive**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Especifica si la virtualización IP está activa en el servidor. Puede ser uno de los siguientes valores.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

La virtualización de IP no está activa.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

La virtualización de IP está activa.

</dd> </dl>

</dd> <dt>

**VirtualIPMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica qué modo de virtualización IP se usa en el servidor. Puede ser uno de los siguientes valores.

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Por sesión** (0)


</dt> <dd>

El modo de virtualización ip es por sesión.

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Por programa** (1)


</dt> <dd>

El modo de virtualización ip es por usuario.

</dd> </dl>

</dd> <dt>

**VirtualizeLoopbackAddressesEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si la virtualización de direcciones de bucleback está habilitada.

**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

no habilitado.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

habilitado

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



 

