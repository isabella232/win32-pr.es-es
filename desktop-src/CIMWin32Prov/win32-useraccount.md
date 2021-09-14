---
description: La cuenta de usuario de Win32 \_&\# 32; La clase WMI contiene información sobre una cuenta de usuario en un sistema informático que ejecuta Windows.
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Win32_UserAccount clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount
- Win32_UserAccount.AccountType
- Win32_UserAccount.Caption
- Win32_UserAccount.Description
- Win32_UserAccount.Disabled
- Win32_UserAccount.Domain
- Win32_UserAccount.FullName
- Win32_UserAccount.InstallDate
- Win32_UserAccount.LocalAccount
- Win32_UserAccount.Lockout
- Win32_UserAccount.Name
- Win32_UserAccount.PasswordChangeable
- Win32_UserAccount.PasswordExpires
- Win32_UserAccount.PasswordRequired
- Win32_UserAccount.SID
- Win32_UserAccount.SIDType
- Win32_UserAccount.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5af83f7a52e9f3db9dbaa4a959bfe01ae740746
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892444"
---
# <a name="win32_useraccount-class"></a>Clase UserAccount de Win32 \_

La **clase WMI \_ UserAccount** [de](../wmisdk/retrieving-a-class.md) Win32 contiene información sobre una cuenta de usuario en un equipo que ejecuta Windows.

> [!Note]  
> Dado que el **nombre y** **el dominio** son propiedades clave, enumerar UserAccount de **Win32 \_** en una red grande puede afectar negativamente al rendimiento. Llamar **a GetObject** o consultar una instancia específica tiene menos impacto.

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserAccount : Win32_Account
{
  uint32   AccountType;
  string   Caption;
  string   Description;
  boolean  Disabled;
  string   Domain;
  string   FullName;
  datetime InstallDate;
  boolean  LocalAccount;
  boolean  Lockout;
  string   Name;
  boolean  PasswordChangeable;
  boolean  PasswordExpires;
  boolean  PasswordRequired;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a>Members

La **clase \_ UserAccount de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ UserAccount de Win32** tiene estos métodos.



| Método                                                     | Descripción                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [**Cambiar nombre**](rename-method-in-class-win32-useraccount.md) | Permite cambiar el nombre de la cuenta de usuario.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ UserAccount de Win32** tiene estas propiedades.

<dl> <dt>

**AccountType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("marcas usri2 de Estructuras de administración de redes win32API \| USER INFO \| [**\_ \_ 2")**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| \_
</dt> </dl>

Marcas que describen las características de una cuenta Windows usuario.

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Cuenta duplicada temporal** (256)


</dt> <dd>

**CUENTA DUPLICADA TEMPORAL DE UF \_ \_ \_**

Cuenta de usuario local para los usuarios que tienen una cuenta principal en otro dominio. Esta cuenta solo proporciona acceso de usuario a este dominio, no a ningún dominio que confíe en este dominio.

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Cuenta normal** (512)


</dt> <dd>

**CUENTA \_ NORMAL DE \_ UF**

Tipo de cuenta predeterminado que representa un usuario típico.

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Cuenta de confianza entre dominios** (2048)


</dt> <dd>

**CUENTA DE \_ CONFIANZA DE UF \_ \_ INTERDOMAIN**

Cuenta de un dominio del sistema que confía en otros dominios.

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Cuenta de confianza de estación** de trabajo (4096)


</dt> <dd>

**CUENTA DE CONFIANZA \_ DE LA ESTACIÓN DE TRABAJO DE \_ \_ UF**

Cuenta de equipo para un sistema informático que Windows que es miembro de este dominio.

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Cuenta de confianza del** servidor (8192)


</dt> <dd>

**CUENTA DE \_ CONFIANZA \_ DEL SERVIDOR \_ UF**

Cuenta de un controlador de dominio de copia de seguridad del sistema que sea miembro de este dominio.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Dominio y nombre de usuario de la cuenta.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descripción de la cuenta.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Deshabilitada**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| \_ \| UF \_ ACCOUNTDISABLE")
</dt> </dl>

Windows cuenta de usuario está deshabilitada.

</dd> <dt>

**Dominio**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Functions \| domainname")
</dt> </dl>

Nombre del dominio Windows al que pertenece una cuenta de usuario, por ejemplo: "NA-SALES".

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ full \_ name**")
</dt> </dl>

Nombre completo de un usuario local, por ejemplo: "Dan Apellido".

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Fecha de instalación")
</dt> </dl>

Fecha en que se instala el objeto. Esta propiedad no necesita un valor para indicar que el objeto está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**LocalAccount**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Corregido**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Si **es true**, la cuenta se define en el equipo local.

Esta propiedad se hereda de la [**cuenta de \_ Win32.**](win32-account.md)

</dd> <dt>

**Bloqueo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ LOCKOUT**")
</dt> </dl>

Si **es true**, la cuenta de usuario está bloqueada del Windows operativo.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](../wmisdk/standard-qualifiers.md) ("Nombre"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Nombre de estructuras de administración de red win32API") \| \|
</dt> </dl>

Nombre de la Windows usuario en el dominio que especifica la propiedad **Domain** de esta clase.

Ejemplo: "danwilson".

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**PasswordChangeable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ PASSWD \_ CANT \_ CHANGE**")
</dt> </dl>

Si **es true,** se puede cambiar la contraseña de esta cuenta de usuario.

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ DONT EXPIRE \_ \_ PASSWD**")
</dt> </dl>

Si **es true,** la contraseña de esta cuenta de usuario expira.

</dd> <dt>

**PasswordRequired**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ PASSWD \_ NOTREQD")**
</dt> </dl>

Si **es true,** se requiere una contraseña en una Windows de usuario. Si **es false,** esta cuenta no requiere una contraseña.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Security Identifiers (SIDs)")
</dt> </dl>

Identificador de seguridad (SID) de esta cuenta. Un SID es un valor de cadena de longitud variable que se usa para identificar a un administrador de confianza. Cada cuenta tiene un SID único que una autoridad, como un Windows, emite. El SID se almacena en la base de datos de seguridad. Cuando un usuario inicia sesión, el sistema recupera el SID de usuario de la base de datos, coloca el SID en el token de acceso de usuario y, a continuación, usa el SID en el token de acceso de usuario para identificar al usuario en todas las interacciones posteriores con la seguridad de Windows. Cada SID es un identificador único para un usuario o grupo, y un usuario o grupo diferente no puede tener el mismo SID.

Esta propiedad se hereda de la [**cuenta de \_ Win32.**](win32-account.md)

</dd> <dt>

**SIDType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Access Control Enumeration Types \| [**SID NAME \_ \_ USE**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")
</dt> </dl>

Valor enumerado que especifica el tipo de SID.

Esta propiedad se hereda de la [**cuenta de \_ Win32.**](win32-account.md)

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

**SidTypeUser** (1)


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

**SidTypeGroup** (2)


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

**SidTypeDomain** (3)


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

**SidTypeAlias** (4)


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

**SidTypeWellKnownGroup** (5)


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

**SidTypeDeletedAccount** (6)


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

**SidTypeInvalid** (7)


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

**SidTypeUnknown** (8)


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

**SidTypeComputer** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Estado actual de un objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail", que es un elemento como una unidad de disco duro habilitada para SMART que puede funcionar correctamente, pero predice un error en un futuro próximo. Los estados no de operación incluyen: "Error", "Starting", "Stopping" y "Service", que se pueden aplicar durante la resilización reflejada de un disco, volver a cargar una lista de permisos de usuario u otro trabajo administrativo.

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

La **clase \_ UserAccount de Win32** se deriva de [**la cuenta de Win32. \_**](win32-account.md)

> [!Note]  
> No se devuelve un error para un intento de escribir en una propiedad de solo lectura y el valor de la propiedad permanece sin cambios.

 

## <a name="examples"></a>Ejemplos

El ejemplo de código List [Local User Accounts Using WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript (Enumerar cuentas de usuario locales que usan WMI VBScript) de la Galería de TechNet usa **Win32 \_ UserAccount** para devolver información sobre las cuentas de usuario locales que se encuentran en un equipo.

[Traducir SID a cuenta de usuario y cuenta de usuario a SID](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) El ejemplo de código de PowerShell en la Galería de TechNet usa **\_ UserAccount de Win32** para traducir un SID a una cuenta de usuario o una cuenta de usuario a SID.

En el ejemplo de código de VBScript siguiente se muestra cómo obtener el nombre completo de un usuario en un equipo local. El nombre completo es el nombre de idioma humano, por ejemplo, una persona puede tener el nombre de usuario "kensandominio" y el nombre completo puede ser "Ken Sandominio", por lo que puede sustituir el nombre de dominio real y el nombre de usuario por "MyDomainName" y "MyUserName". Para una consulta eficaz, debe especificar las propiedades de dominio y nombre de usuario.

Si es administrador en un equipo remoto, puede asignar el nombre del equipo remoto para strComputer (en lugar de ".") y, a continuación, usar el siguiente tipo de script para obtener el nombre completo de una cuenta de usuario en un equipo local, desde un equipo remoto.


```VB
On Error Resume Next
strComputer = "."

Set objUserAccount = GetObject("winmgmts{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_UserAccount.Domain='MyDomainName',Name='MyUserName' ")

If Err = 0 Then
    WScript.Echo objUserAccount.FullName
Else
    WScript.Echo "No object found" & Err.Number
End If
```




```CSharp
using System.Management;

{
     ManagementScope mgmtScope = new ManagementScope("\\\\.\\Root\\CIMv2");
     ObjectQuery oQuery = new ObjectQuery("SELECT * FROM Win32_UserAccount Where Name=\"myUserName\"");
     ManagementObjectSearcher mgmtSearch = new ManagementObjectSearcher(mgmtScope, oQuery);
     ManagementObjectCollection objCollection = mgmtSearch.Get();
     foreach (ManagementObject mgmtObject in objCollection)
     {
          Console.WriteLine("Full Name : {0}", mgmtObject["FullName"]);
     }
}
```



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

[**Cuenta \_ win32**](win32-account.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
