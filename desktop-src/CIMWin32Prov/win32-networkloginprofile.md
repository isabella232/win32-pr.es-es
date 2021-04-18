---
description: Win32 \_ NetworkLoginProfile&\# 8194; La clase WMI representa la información de inicio de sesión de red de un usuario específico en un equipo con Windows.
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Win32_NetworkLoginProfile (clase)
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
ms.openlocfilehash: 3b138ce4bc92088896286f4a21a039b068e2206e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652341"
---
# <a name="win32_networkloginprofile-class"></a>\_Clase Win32 NetworkLoginProfile

La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkLoginProfile de Win32** representa la información de inicio de sesión de red de un usuario específico en un equipo con Windows. Esto incluye, entre otros, el estado de la contraseña, los privilegios de acceso, las cuotas de disco y las rutas de acceso del directorio de inicio de sesión.

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

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ acct \_ Expires")
</dt> </dl>

La cuenta expirará. Este valor se calcula a partir del número de segundos transcurridos desde 00:00:00, el 1 de enero de 1970 y se establece en este formato: aaaammddhhmmss. mmmmmm SUTC.

Ejemplo: 20521201000230,000000 000

</dd> <dt>

**AuthorizationFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ auth \_ flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")
</dt> </dl>

Conjunto de marcas que especifican los recursos que un usuario está autorizado a usar o modificar.

<dt>

1 (0x1)
</dt> <dd>

Impresora

</dd> <dt>

2 (0X2)
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

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Functions \| NetUserEnum")
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

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**CodePage**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ code \_ Page")
</dt> </dl>

Página de códigos para el idioma de elección del usuario. Una página de códigos es el juego de caracteres utilizado.

</dd> <dt>

**Comentario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ comment")
</dt> </dl>

Comentario o descripción para este perfil de inicio de sesión.

</dd> <dt>

**País**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Country \_ Code")
</dt> </dl>

Código de país o región para el idioma de elección del usuario.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**Marcas**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags"), [**Bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("script", "Account Disabled", "Home dir Required", "bloqueos", "Password Not Required", "Paswword not Change", "contraseña de prueba cifrada permitida", "cuenta temporal duplicada", "cuenta normal", "cuenta de confianza entre dominios", "cuenta de confianza de estación de trabajo", "cuenta de confianza de servidor", "no caducar contraseña", "cuenta de inicio de sesión de MNS", "tarjeta inteligente requerida", "de confianza para delegación", "no delegada", "usar solo la clave des", "no requerir autorización previa", "contraseña expirada")
</dt> </dl>

Propiedades disponibles para este perfil de red.

Entre las propiedades que se pueden establecer se incluyen:

<dt>

1 (0x1)
</dt> <dd>

Script

Se ejecutó un script de inicio de sesión. Este valor se debe establecer para el administrador de LAN 2,0.

</dd> <dt>

2 (0X2)
</dt> <dd>

Cuenta deshabilitada

La cuenta del usuario está deshabilitada.

</dd> <dt>

8 (0x8)
</dt> <dd>

Se requiere el directorio particular

Se requiere un directorio particular.

</dd> <dt>

16 (0x10)
</dt> <dd>

Bloqueo

La cuenta está bloqueada actualmente. En el caso de [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), este valor se puede borrar para desbloquear una cuenta bloqueada previamente. Este valor no se puede usar para bloquear una cuenta desbloqueada previamente.

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

Cuenta temporal duplicada

Una cuenta para usuarios cuya cuenta principal se encuentra en otro dominio. Esta cuenta proporciona acceso de usuario a este dominio, pero no a ningún dominio que confíe en este dominio. El administrador de usuarios hace referencia a este tipo de cuenta como cuenta de usuario local.

</dd> <dt>

512 (0x200)
</dt> <dd>

Cuenta normal

Tipo de cuenta predeterminado que representa a un usuario típico.

</dd> <dt>

2048 (0x800)
</dt> <dd>

Cuenta de confianza entre dominios

Permiso para una cuenta de confianza para un dominio que confía en otros dominios.

</dd> <dt>

4096 (0x1000)
</dt> <dd>

Cuenta de confianza de estación de trabajo

Una cuenta de equipo para una estación de trabajo de Windows o un servidor que sea miembro de este dominio.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Cuenta de confianza de servidor

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

Se requiere una tarjeta inteligente

</dd> <dt>

524288 (0x80000)
</dt> <dd>

De confianza para delegación

</dd> <dt>

1048576 (0x100000)
</dt> <dd>

No delegado

</dd> <dt>

2097152 (0x200000)
</dt> <dd>

Usar solo la clave DES

</dd> <dt>

4194304 (0x400000)
</dt> <dd>

No requerir autorización previa

</dd> <dt>

8388608 (0x800000)
</dt> <dd>

Contraseña expirada

Indica que la contraseña ha expirado.

</dd> </dl>

Las siguientes propiedades describen el tipo de cuenta. Solo se puede establecer un valor:

-   \_cuenta normal de fi \_
-   FI \_ - \_ cuenta duplicada temporal \_
-   cuenta de confianza de estación de trabajo de fi \_ \_ \_
-   \_cuenta de \_ confianza de servidor de up \_
-   cuenta de confianza entre \_ dominios \_ \_

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Full \_ Name")
</dt> </dl>

Nombre completo del usuario que pertenece al perfil de inicio de sesión de red. Esta cadena puede estar vacía si el usuario decide no asociar un nombre completo con un nombre de usuario.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir")
</dt> </dl>

Ruta de acceso al directorio particular del usuario. Esta cadena puede estar vacía si el usuario decide no especificar un directorio particular.

Ejemplo: " \\ HOMEDIR"

</dd> <dt>

**HomeDirectoryDrive**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir \_ Drive")
</dt> </dl>

Letra de unidad asignada al directorio principal del usuario para el inicio de sesión.

Ejemplo: "C:"

</dd> <dt>

**LastLogoff**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Logoff")
</dt> </dl>

El usuario cerró sesión por última vez en el sistema. Este valor se calcula a partir del número de segundos transcurridos desde el 00:00:00 de enero de 1970. Un valor de " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " significa que no se conoce la hora del último cierre de sesión. El formato de este valor es aaaammddhhmmss. mmmmmm SUTC. Para obtener información sobre cómo convertir esta propiedad en la hora local, vea [tareas de WMI: fechas y horas](../wmisdk/wmi-tasks--dates-and-times.md).

Ejemplo: 19521201000230,000000 000

</dd> <dt>

**LastLogon**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Logon")
</dt> </dl>

El usuario inició sesión por última vez en el sistema. Este valor se calcula a partir del número de segundos transcurridos desde el 00:00:00 de enero de 1970. El formato de este valor es aaaammddhhmmss. mmmmmm SUTC. Para obtener información sobre cómo convertir esta propiedad en la hora local, vea [tareas de WMI: fechas y horas](../wmisdk/wmi-tasks--dates-and-times.md).

Ejemplo: 19521201000230,000000 000

</dd> <dt>

**LogonHours**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ hours")
</dt> </dl>

Horas durante la semana en las que el usuario puede iniciar sesión. Cada bit representa una unidad de tiempo especificada por la propiedad **UnitsPerWeek** . Por ejemplo, si la unidad de tiempo es cada hora, el primer bit (bit 0, palabra 0) es domingo, de 0:00 a 0:59, el segundo bit (bit 1, palabra 0) es domingo, 1:00 a 1:59, etc. Si este miembro se establece en **null**, no hay ninguna restricción de tiempo. La hora se establece en GMT y debe ajustarse para otras zonas horarias (por ejemplo, GMT menos 8 horas para PST).

</dd> <dt>

**LogonServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ Server")
</dt> </dl>

Nombre del servidor al que se envían las solicitudes de inicio de sesión. Los nombres de servidor deben ir precedidos de dos barras diagonales inversas ( \\ \\ ). Un nombre de servidor con un asterisco ( \\ \\ \* ) indica que la solicitud de inicio de sesión se puede controlar mediante cualquier servidor de inicio de sesión. Una cadena nula indica que las solicitudes se envían al controlador de dominio.

Ejemplo: "mi \\ \\ Server"

</dd> <dt>

**MaximumStorage**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Max \_ Storage"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Cantidad máxima de espacio en disco disponible para el usuario. Si MaximumStorage se establece en USER \_ MAXSTORAGE \_ Unlimited, el usuario puede usar todo el espacio disponible en disco.

Ejemplo: 10 millones

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Name")
</dt> </dl>

Cuenta de usuario en un dominio o equipo determinado. El número de caracteres del nombre no puede superar el valor de UNLEN.

Ejemplo: \\ "algúndominio de los

</dd> <dt>

**NumberOfLogons**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ NUM \_ inicios de sesión")
</dt> </dl>

Número de veces que el usuario intentó iniciar sesión en esta cuenta. Un valor de 0xFFFFFFFF indica que el valor es desconocido. Esta propiedad se mantiene por separado en cada controlador de dominio de copia de seguridad (BDC) del dominio. Para obtener un valor preciso, solo se debe usar el valor más grande de todos los BDC.

Ejemplo: 4

</dd> <dt>

**Parámetros**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parms")
</dt> </dl>

Espacio reservado para que lo usen las aplicaciones. Esta cadena puede ser null o puede tener cualquier número de caracteres antes del carácter nulo de terminación. Los productos de Microsoft usan este miembro para almacenar información de configuración de usuario. No modifique esta información, ya que este valor es específico de una aplicación.

</dd> <dt>

**Contraseñas**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ password \_ Age")
</dt> </dl>

Cantidad de tiempo que una contraseña ha estado en vigor. Este valor se mide a partir del número de segundos transcurridos desde que se cambió la contraseña por última vez.

Ejemplo: 00001201000230,000000 000

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| Administración de red estructuras de usuario de la \| [**\_ \_ información \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ passwd \_ Age")
</dt> </dl>

Fecha y hora en que expira la contraseña. El valor se establece en este formato: aaaammddhhmmss. mmmmmm SUTC

Ejemplo: 19521201000230,000000 000

</dd> <dt>

**PrimaryGroupId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Primary \_ Group \_ ID")
</dt> </dl>

Identificador relativo (RID) del grupo global principal para este usuario. El identificador comprueba el grupo primario al que pertenece el perfil del usuario.

</dd> <dt>

**Privilegios**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ priv")
</dt> </dl>

Nivel de privilegio asignado a la **propiedad \_ nombre de usri3** .

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

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Profile")
</dt> </dl>

Ruta de acceso al perfil del usuario. Este valor puede ser una cadena nula, una ruta de acceso absoluta local o una ruta de acceso UNC. Un perfil de usuario contiene opciones de configuración que se pueden personalizar para cada usuario, como los colores del escritorio.

Ejemplo: "C: \\ Windows"

</dd> <dt>

**ScriptPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ script \_ path")
</dt> </dl>

Ruta de acceso al directorio del script de inicio de sesión del usuario. Un script de inicio de sesión ejecuta automáticamente un conjunto de comandos cada vez que un usuario inicia sesión en un sistema.

Ejemplo: "C: \\ Win \\ profiles \\ ThomasSteven"

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

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**UnitsPerWeek**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Units \_ per \_ Week")
</dt> </dl>

Número de unidades de tiempo en que se divide la semana. Se usa con la propiedad **LogonHours** para limitar el acceso del usuario al equipo.

Ejemplo: 168 (horas por semana)

</dd> <dt>

**UserComment**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ comment")
</dt> </dl>

Comentario o descripción definidos por el usuario para este perfil.

</dd> <dt>

**UserId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ User \_ ID")
</dt> </dl>

RID del usuario. El identificador comprueba que el usuario existe y es único para este dominio.

</dd> <dt>

**UserType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags")
</dt> </dl>

Tipo de cuenta en la que el usuario tiene privilegios.

Los valores son:

-   "Cuenta normal"
-   "Cuenta duplicada"
-   "Cuenta de confianza de estación de trabajo"
-   "Cuenta de confianza de servidor"
-   "Cuenta de confianza entre dominios"
-   Unknown

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

**Cuenta normal** ("cuenta normal")


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

**Cuenta duplicada** ("cuenta duplicada")


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

**Cuenta de confianza de estación de trabajo** ("cuenta de confianza de estación de trabajo")


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

**Cuenta de confianza del servidor** ("cuenta de confianza del servidor")


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

**Cuenta de confianza entre dominios** ("cuenta de confianza entre dominios")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("desconocido")


</dt> <dd></dd> </dl>

</dd> <dt>

**Estaciones**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Workstation")
</dt> </dl>

Nombres de las estaciones de trabajo desde las que el usuario puede iniciar sesión. Se pueden especificar hasta ocho estaciones de trabajo; los nombres deben estar separados por comas (,). Una cadena nula indica que no hay restricciones. Para deshabilitar los inicios de sesión de todas las estaciones de trabajo en esta cuenta, establezca el \_ ACCOUNTDISABLE de fi en la propiedad **Flags** de esta clase.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ NetworkLoginProfile de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).

El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro. Para obtener más información, vea [ejecutar operaciones con privilegios](../wmisdk/executing-privileged-operations.md).

## <a name="examples"></a>Ejemplos

El ejemplo de PowerShell [Mostrar perfiles de inicio de sesión de red](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) devuelve información de inicio de sesión de red para todos los usuarios de un equipo.

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
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
