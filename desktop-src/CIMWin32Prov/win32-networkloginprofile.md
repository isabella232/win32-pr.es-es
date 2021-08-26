---
description: El perfil \_ NetworkLoginProfile de Win32&\# 8194; La clase WMI representa la información de inicio de sesión de red de un usuario específico en un sistema informático que ejecuta Windows.
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Win32_NetworkLoginProfile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4fb71b27093cb1011b9aebaadf0a6760124b64f9e13ae7b5ef46f5ffc478cce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972655"
---
# <a name="win32_networkloginprofile-class"></a>Clase NetworkLoginProfile de Win32 \_

La clase  [WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkLoginProfile de Win32** representa la información de inicio de sesión de red de un usuario específico en un equipo que ejecuta Windows. Esto incluye, entre otros, el estado de la contraseña, los privilegios de acceso, las cuotas de disco y las rutas de acceso del directorio de inicio de sesión.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a>Miembros

La **clase \_ NetworkLoginProfile de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ NetworkLoginProfile de Win32** tiene estas propiedades.

<dl> <dt>

**AccountExpires**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ acct expires")
</dt> </dl>

La cuenta expirará. Este valor se calcula a partir del número de segundos transcurridos desde 00:00:00, 1 de enero de 1970, y se establece en este formato: aaaammddhhmmss.mmmm sutc.

Ejemplo: 20521201000230.000000 000

</dd> <dt>

**AuthorizationFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Marcas de autenticación de usri3 de Estructuras de administración de redes win32API \| USER INFO \| [**\_ \_ 3"),**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ \_ [**BitValues**](../wmisdk/standard-qualifiers.md) ("Impresora", "Comunicación", "Servidor", "Cuentas")
</dt> </dl>

Conjunto de marcas que especifican los recursos que un usuario está autorizado a usar o modificar.

<dt>

1 (0x1)
</dt> <dd>

Impresora

</dd> <dt>

2 (0x2)
</dt> <dd>

Comunicación

</dd> <dt>

4 (0x4)
</dt> <dd>

Servidor

</dd> <dt>

8 (0x8)
</dt> <dd>

Cuentas

</dd> </dl>

</dd> <dt>

**BadPasswordCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Functions \| NetUserEnum")
</dt> </dl>

Número de veces que el usuario escribe una contraseña incorrecta al iniciar sesión en un equipo que ejecuta Windows.

Ejemplo: 0

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**CodePage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("página de códigos Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3") \_ \_
</dt> </dl>

Página de códigos para el idioma que elija el usuario. Una página de códigos es el juego de caracteres utilizado.

</dd> <dt>

**Comment**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ comment")
</dt> </dl>

Comentario o descripción de este perfil de inicio de sesión.

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Código de país usri3 de Estructuras de administración de redes win32API \| USER INFO \| [**\_ \_ 3")**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ \_
</dt> </dl>

Código de país o región para el idioma que elija el usuario.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**Marcas**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("marcas usri3 de User Info 3 de estructuras de administración de redes de Win32API"), \| \| [**\_ \_**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Script", "Account Disabled", "Home Dir Required", "Lockout", "Password Not Required", "Paswword Can't Change", "Encrypted Test Password Allowed", "Temp Duplicate Account", "Normal Account", "InterDomain Trust Account", "WorkStation Trust Account", "Cuenta de confianza del servidor", "No expirar contraseña", "Cuenta de inicio de sesión de MNS", "Smartcard Required", "Trusted for Delegation", "Not Delegated", "Use DES Key Only", "Don't Require Preauthorization", "Password Expired")
</dt> </dl>

Propiedades disponibles para este perfil de red.

Las propiedades que se pueden establecer incluyen:

<dt>

1 (0x1)
</dt> <dd>

Script

Se ha ejecutado un script de inicio de sesión. Este valor debe establecerse para LAN Manager 2.0.

</dd> <dt>

2 (0x2)
</dt> <dd>

Cuenta deshabilitada

La cuenta del usuario está deshabilitada.

</dd> <dt>

8 (0x8)
</dt> <dd>

Directorio principal requerido

Se requiere un directorio principal.

</dd> <dt>

16 (0x10)
</dt> <dd>

Bloqueo

La cuenta está bloqueada actualmente. Para [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), este valor se puede borrar para desbloquear una cuenta bloqueada previamente. Este valor no se puede usar para bloquear una cuenta desbloqueada previamente.

</dd> <dt>

32 (0x20)
</dt> <dd>

Contraseña no necesaria

No se requiere una contraseña.

</dd> <dt>

64 (0x40)
</dt> <dd>

No se puede cambiar la contraseña

El usuario no puede cambiar la contraseña.

</dd> <dt>

128 (0x80)
</dt> <dd>

Contraseña de prueba cifrada permitida

</dd> <dt>

256 (0x100)
</dt> <dd>

Cuenta duplicada temporal

Una cuenta para los usuarios cuya cuenta principal está en otro dominio. Esta cuenta proporciona acceso de usuario a este dominio, pero no a ningún dominio que confíe en este dominio. El Administrador de usuarios hace referencia a este tipo de cuenta como una cuenta de usuario local.

</dd> <dt>

512 (0x200)
</dt> <dd>

Cuenta normal

Tipo de cuenta predeterminado que representa un usuario típico.

</dd> <dt>

2048 (0x800)
</dt> <dd>

Cuenta de confianza entre dominios

Permiso a una cuenta de confianza para un dominio que confía en otros dominios.

</dd> <dt>

4096 (0x1000)
</dt> <dd>

Cuenta de confianza de estación de trabajo

Una cuenta de equipo para una Windows o servidor que sea miembro de este dominio.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Cuenta de confianza del servidor

Una cuenta de equipo para un controlador de dominio de copia de seguridad que sea miembro de este dominio.

</dd> <dt>

65536 (0x10000)
</dt> <dd>

No expirar contraseña

</dd> <dt>

131072 (0x20000)
</dt> <dd>

Cuenta de inicio de sesión de MNS

Tipo de cuenta de inicio de sesión del conjunto de nodos mayoritario (MNS) que representa un usuario de MNS.

</dd> <dt>

262144 (0x40000)
</dt> <dd>

Tarjeta inteligente requerida

</dd> <dt>

524288 (0x80000)
</dt> <dd>

Confianza para delegación

</dd> <dt>

1048576 (0x100000)
</dt> <dd>

No delegado

</dd> <dt>

2097152 (0x200000)
</dt> <dd>

Usar solo clave DES

</dd> <dt>

4194304 (0x400000)
</dt> <dd>

No requerir autenticación previa

</dd> <dt>

8388608 (0x800000)
</dt> <dd>

Contraseña expirada

Indica que la contraseña ha expirado.

</dd> </dl>

Las siguientes propiedades describen el tipo de cuenta. Solo se puede establecer un valor:

-   CUENTA \_ NORMAL DE \_ UF
-   CUENTA DUPLICADA \_ TEMPORAL \_ DE UF \_
-   CUENTA DE CONFIANZA \_ DE ESTACIÓN DE TRABAJO DE \_ \_ UF
-   CUENTA DE \_ CONFIANZA \_ DEL SERVIDOR \_ UF
-   UF \_ INTERDOMAIN \_ TRUST \_ ACCOUNT

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ full \_ name")
</dt> </dl>

Nombre completo del usuario que pertenece al perfil de inicio de sesión de red. Esta cadena puede estar vacía si el usuario decide no asociar un nombre completo a un nombre de usuario.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ home \_ dir")
</dt> </dl>

Ruta de acceso al directorio principal del usuario. Esta cadena puede estar vacía si el usuario decide no especificar un directorio principal.

Ejemplo: \\ "HOMEDIR"

</dd> <dt>

**HomeDirectoryDrive**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ home dir \_ \_ drive")
</dt> </dl>

Letra de unidad asignada al directorio principal del usuario con fines de inicio de sesión.

Ejemplo: "C:"

</dd> <dt>

**LastLogoff**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ last \_ logoff")
</dt> </dl>

El usuario ha cerrado sesión por última vez en el sistema. Este valor se calcula a partir del número de segundos transcurridos desde las 00:00:00 del 1 de enero de 1970. Un valor de " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " significa que se desconoce la última hora de cierre de sesión. El formato de este valor es aaaammddhhmmss.mmmmmm sutc. Para obtener información sobre cómo traducir esta propiedad a la hora local, vea [Tareas wmi: fechas y horas.](../wmisdk/wmi-tasks--dates-and-times.md)

Ejemplo: 19521201000230.000000 000

</dd> <dt>

**LastLogon**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ last \_ logon")
</dt> </dl>

El usuario inició sesión por última vez en el sistema. Este valor se calcula a partir del número de segundos transcurridos desde las 00:00:00 del 1 de enero de 1970. El formato de este valor es aaaammddhhmmss.mmmmmm sutc. Para obtener información sobre cómo traducir esta propiedad a la hora local, vea [Tareas wmi: fechas y horas.](../wmisdk/wmi-tasks--dates-and-times.md)

Ejemplo: 19521201000230.000000 000

</dd> <dt>

**LogonHours**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ logon \_ hours")
</dt> </dl>

Horas durante la semana en las que el usuario puede iniciar sesión. Cada bit representa una unidad de tiempo especificada por la **propiedad UnitsPerWeek.** Por ejemplo, si la unidad de tiempo es cada hora, el primer bit (bit 0, palabra 0) es domingo, de 0:00 a 0:59, el segundo bit (bit 1, palabra 0) es domingo, de 1:00 a 1:59, y así sucesivamente. Si este miembro se establece en **NULL,** no hay ninguna restricción de tiempo. La hora se establece en GMT y se debe ajustar para otras zonas horarias (por ejemplo, GMT menos 8 horas para PST).

</dd> <dt>

**LogonServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ logon \_ server")
</dt> </dl>

Nombre del servidor al que se envían las solicitudes de inicio de sesión. Los nombres de servidor deben ir precedidos de dos barras diagonales inversas ( \\ \\ ). Un nombre de servidor con un asterisco ( ) indica que cualquier servidor de inicio de sesión puede controlar la solicitud \\ \\ \* de inicio de sesión. Una cadena null indica que las solicitudes se envían al controlador de dominio.

Ejemplo: \\ \\ "MyServer"

</dd> <dt>

**MaximumStorage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ max \_ storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Cantidad máxima de espacio en disco disponible para el usuario. Si MaximumStorage está establecido en USER MAXSTORAGE UNLIMITED, el usuario puede usar todo \_ el espacio disponible en \_ disco.

Ejemplo: 10000000

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ name")
</dt> </dl>

Cuenta de usuario en un dominio o equipo determinado. El número de caracteres del nombre no puede superar el valor de UNLEN.

Ejemplo: "somedomain \\ johndoe"

</dd> <dt>

**NumberOfLogons**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ num \_ logons")
</dt> </dl>

Número de veces que el usuario intentó iniciar sesión en esta cuenta correctamente. Un valor de 0xFFFFFFFF indica que el valor es desconocido. Esta propiedad se mantiene por separado en cada controlador de dominio de copia de seguridad (BDC) del dominio. Para obtener un valor preciso, solo se debe usar el valor más grande de todos los BDC.

Ejemplo: 4

</dd> <dt>

**Parámetros**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parms")
</dt> </dl>

Espacio reservado para que lo usen las aplicaciones. Esta cadena puede ser null o puede tener cualquier número de caracteres antes del carácter nulo de terminación. Los productos de Microsoft usan este miembro para almacenar información de configuración de usuario. No modifique esta información, ya que este valor es específico de una aplicación.

</dd> <dt>

**PasswordAge**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ password \_ age")
</dt> </dl>

Tiempo durante el que una contraseña ha estado en vigor. Este valor se mide a partir del número de segundos transcurridos desde la última vez que se cambió la contraseña.

Ejemplo: 00001201000230.000000 000

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER \| [**\_ MODALS INFO \_ \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ max \_ passwd \_ age")
</dt> </dl>

Fecha y hora en que expira la contraseña. El valor se establece en este formato: aaaammddhhmmss.mmmmmm sutc

Ejemplo: 19521201000230.000000 000

</dd> <dt>

**PrimaryGroupId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ primary group \_ \_ id")
</dt> </dl>

Identificador relativo (RID) del grupo global principal para este usuario. El identificador comprueba el grupo principal al que pertenece el perfil del usuario.

</dd> <dt>

**Privilegios**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ priv")
</dt> </dl>

Nivel de privilegio asignado a la **propiedad de nombre usri3. \_**

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

**Invitado** (0)


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

**Usuario** (1)


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

**Administrador** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Perfil**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ profile")
</dt> </dl>

Ruta de acceso al perfil del usuario. Este valor puede ser una cadena nula, una ruta de acceso absoluta local o una ruta de acceso UNC. Un perfil de usuario contiene configuraciones que son personalizables para cada usuario, como los colores de escritorio.

Ejemplo: "C: \\ Windows"

</dd> <dt>

**ScriptPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ script \_ path")
</dt> </dl>

Ruta de acceso del directorio al script de inicio de sesión del usuario. Un script de inicio de sesión ejecuta automáticamente un conjunto de comandos cada vez que un usuario inicia sesión en un sistema.

Ejemplo: "C: \\ win \\ profiles \\ ThomasSteven"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador por el que se conoce el objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**UnitsPerWeek**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ units per \_ \_ week")
</dt> </dl>

Número de unidades de tiempo en las que se divide la semana. Se usa con la propiedad **LogonHours para** limitar el acceso del usuario al equipo.

Ejemplo: 168 (horas por semana)

</dd> <dt>

**UserComment**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ comment")
</dt> </dl>

Comentario o descripción definidos por el usuario para este perfil.

</dd> <dt>

**UserId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ user \_ id")
</dt> </dl>

RID del usuario. El identificador comprueba que el usuario existe y es único para este dominio.

</dd> <dt>

**UserType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags")
</dt> </dl>

Tipo de cuenta para la que el usuario tiene privilegios.

Los valores son:

-   "Cuenta normal"
-   "Cuenta duplicada"
-   "Cuenta de confianza de estación de trabajo"
-   "Cuenta de confianza del servidor"
-   "Cuenta de confianza de Interdomain"
-   "Desconocido"

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

**Cuenta normal** ("cuenta normal")


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

**Cuenta duplicada** ("Cuenta duplicada")


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

**Cuenta de confianza de estación de trabajo** ("cuenta de confianza de estación de trabajo")


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

**Cuenta de confianza del servidor** ("cuenta de confianza del servidor")


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

**Cuenta de confianza de Interdomain** ("Cuenta de confianza de Interdomain")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("Desconocido")


</dt> <dd></dd> </dl>

</dd> <dt>

**Estaciones**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estaciones de trabajo usri3 de Estructuras de administración de redes win32API \| USER INFO \| [**\_ \_ 3")**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_
</dt> </dl>

Nombres de las estaciones de trabajo desde las que el usuario puede iniciar sesión. Se pueden especificar hasta ocho estaciones de trabajo; los nombres deben estar separados por comas (,). Una cadena null indica que no hay restricciones. Para deshabilitar los inicios de sesión de todas las estaciones de trabajo en esta cuenta, establezca UF ACCOUNTDISABLE en la \_ **propiedad Flags** de esta clase.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ NetworkLoginProfile de Win32** se deriva de [**cim \_ setting**](cim-setting.md).

El proceso de llamada que usa esta clase debe tener el **SE \_ restore \_ NAME** en el equipo en el que reside el Registro. Para obtener más información, vea [Ejecutar operaciones con privilegios.](../wmisdk/executing-privileged-operations.md)

## <a name="examples"></a>Ejemplos

El [ejemplo de PowerShell Enumerar perfiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) de inicio de sesión de red devuelve información de inicio de sesión de red para todos los usuarios de un equipo.

El siguiente ejemplo de VBScript devuelve información de inicio de sesión de red.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
