---
title: Win32_TSPublishedApplicationList (clase)
description: Representa la lista de programas que se encuentran en la lista Programas RemoteApp en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 3dbefe54-8c31-439f-a87a-5148214a07d5
ms.tgt_platform: multiple
keywords:
- Win32_TSPublishedApplicationList clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSPublishedApplicationList de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplicationList
- Win32_TSPublishedApplicationList.Caption
- Win32_TSPublishedApplicationList.Description
- Win32_TSPublishedApplicationList.InstallDate
- Win32_TSPublishedApplicationList.Name
- Win32_TSPublishedApplicationList.Status
- Win32_TSPublishedApplicationList.Disabled
- Win32_TSPublishedApplicationList.PolicySourceDisabled
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f87a87dc6f95bcdb33c7dbd1364ad6b3114ddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079239"
---
# <a name="win32_tspublishedapplicationlist-class"></a>\_Clase Win32 TSPublishedApplicationList

Representa la lista de programas que se encuentran en la lista Programas RemoteApp en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_TSPublishedApplicationList : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  Disabled;
  uint32   PolicySourceDisabled;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSPublishedApplicationList de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TSPublishedApplicationList de Win32** tiene estas propiedades.

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

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**Deshabilitada**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el servidor host de sesión de escritorio remoto restringe los programas que un usuario puede iniciar en la conexión inicial a los programas que se encuentran en la lista Programas RemoteApp.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Fecha en que se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**PolicySourceDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica dónde está configurada la propiedad **Disabled** . Entre los posibles valores se incluyen:

<dt>

0
</dt> <dd>

La configuración se configura en el servidor a través de Administrador de RemoteApp o del proveedor de WMI de RemoteApp.

</dd> <dt>

1
</dt> <dd>

La configuración se configura mediante la Directiva de grupo.

</dd> <dt>

2
</dt> <dd>

La configuración no está configurada. El valor predeterminado de **false** se utiliza para la propiedad **Disabled** .

</dd> </dl>

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Estado actual del objeto. Se pueden definir varios Estados operativos y no operativos. Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo). Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio". El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

<dt>



 ("Correcto")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconocido")


</dt> <dd></dd> <dt>



 ("Pred FAIL")


</dt> <dd></dd> <dt>



 ("Iniciando")


</dt> <dd></dd> <dt>



 ("Deteniéndose")


</dt> <dd></dd> <dt>



 ("Servicio")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo administradores para establecer las propiedades utilizando esta clase.

La propiedad **Disabled** no impide que los usuarios inicien de forma remota programas que no están en la lista después de conectarse al servidor host de sesión de escritorio remoto mediante un programa de RemoteApp.

La propiedad **Disabled** se establecerá en un valor de 2 solo si falta la siguiente entrada del registro:

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WindowsNT** \\ **CurrentVersion** \\ **TerminalServer** \\ **TSAppAllowList** \\ **fDisabledAllowList**

Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes. En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, que se puede establecer mediante la función com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) . En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6. En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. mof</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

