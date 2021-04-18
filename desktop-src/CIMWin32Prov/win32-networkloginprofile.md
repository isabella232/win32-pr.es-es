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
# <a name="win32_networkloginprofile-class"></a><span data-ttu-id="0f194-103">\_Clase Win32 NetworkLoginProfile</span><span class="sxs-lookup"><span data-stu-id="0f194-103">Win32\_NetworkLoginProfile class</span></span>

<span data-ttu-id="0f194-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkLoginProfile de Win32** representa la información de inicio de sesión de red de un usuario específico en un equipo con Windows.</span><span class="sxs-lookup"><span data-stu-id="0f194-104">The **Win32\_NetworkLoginProfile** [WMI class](../wmisdk/retrieving-a-class.md) represents the network login information of a specific user on a computer system running Windows.</span></span> <span data-ttu-id="0f194-105">Esto incluye, entre otros, el estado de la contraseña, los privilegios de acceso, las cuotas de disco y las rutas de acceso del directorio de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0f194-105">This includes, but is not limited to password status, access privileges, disk quotas, and logon directory paths.</span></span>

<span data-ttu-id="0f194-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0f194-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f194-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f194-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="0f194-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f194-108">Members</span></span>

<span data-ttu-id="0f194-109">La **clase \_ NetworkLoginProfile de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0f194-109">The **Win32\_NetworkLoginProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="0f194-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0f194-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f194-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0f194-111">Properties</span></span>

<span data-ttu-id="0f194-112">La **clase \_ NetworkLoginProfile de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0f194-112">The **Win32\_NetworkLoginProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f194-113">**AccountExpires**</span><span class="sxs-lookup"><span data-stu-id="0f194-113">**AccountExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-114">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f194-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-116">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ acct \_ Expires")</span><span class="sxs-lookup"><span data-stu-id="0f194-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_acct\_expires")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-117">La cuenta expirará.</span><span class="sxs-lookup"><span data-stu-id="0f194-117">Account will expire.</span></span> <span data-ttu-id="0f194-118">Este valor se calcula a partir del número de segundos transcurridos desde 00:00:00, el 1 de enero de 1970 y se establece en este formato: aaaammddhhmmss. mmmmmm SUTC.</span><span class="sxs-lookup"><span data-stu-id="0f194-118">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970, and is set in this format: yyyymmddhhmmss.mmmmmm sutc.</span></span>

<span data-ttu-id="0f194-119">Ejemplo: 20521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="0f194-119">Example: 20521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="0f194-120">**AuthorizationFlags**</span><span class="sxs-lookup"><span data-stu-id="0f194-120">**AuthorizationFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-121">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f194-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-123">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ auth \_ flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")</span><span class="sxs-lookup"><span data-stu-id="0f194-123">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_auth\_flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-124">Conjunto de marcas que especifican los recursos que un usuario está autorizado a usar o modificar.</span><span class="sxs-lookup"><span data-stu-id="0f194-124">Set of flags that specify the resources a user is authorized to use or modify.</span></span>

<dt>

<span data-ttu-id="0f194-125">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f194-125">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-126">Impresora</span><span class="sxs-lookup"><span data-stu-id="0f194-126">Printer</span></span>

</dd> <dt>

<span data-ttu-id="0f194-127">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="0f194-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-128">Comunicación</span><span class="sxs-lookup"><span data-stu-id="0f194-128">Communication</span></span>

</dd> <dt>

<span data-ttu-id="0f194-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="0f194-129">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-130">Servidor</span><span class="sxs-lookup"><span data-stu-id="0f194-130">Server</span></span>

</dd> <dt>

<span data-ttu-id="0f194-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="0f194-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-132">Cuentas</span><span class="sxs-lookup"><span data-stu-id="0f194-132">Accounts</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0f194-133">**BadPasswordCount**</span><span class="sxs-lookup"><span data-stu-id="0f194-133">**BadPasswordCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f194-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-136">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Functions \| NetUserEnum")</span><span class="sxs-lookup"><span data-stu-id="0f194-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|NetUserEnum")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-137">Número de veces que el usuario escribe una contraseña incorrecta al iniciar sesión en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="0f194-137">Number of times the user enters a bad password when logging on to a computer system running Windows.</span></span>

<span data-ttu-id="0f194-138">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="0f194-138">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="0f194-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0f194-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-142">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0f194-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0f194-143">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="0f194-143">Short textual description of the current object.</span></span>

<span data-ttu-id="0f194-144">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0f194-144">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f194-145">**CodePage**</span><span class="sxs-lookup"><span data-stu-id="0f194-145">**CodePage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f194-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-148">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ code \_ Page")</span><span class="sxs-lookup"><span data-stu-id="0f194-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_code\_page")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-149">Página de códigos para el idioma de elección del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f194-149">Code page for the user's language of choice.</span></span> <span data-ttu-id="0f194-150">Una página de códigos es el juego de caracteres utilizado.</span><span class="sxs-lookup"><span data-stu-id="0f194-150">A code page is the character set used.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-151">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="0f194-151">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-154">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ comment")</span><span class="sxs-lookup"><span data-stu-id="0f194-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-155">Comentario o descripción para este perfil de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0f194-155">Comment or description for this logon profile.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-156">**País**</span><span class="sxs-lookup"><span data-stu-id="0f194-156">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f194-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-159">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Country \_ Code")</span><span class="sxs-lookup"><span data-stu-id="0f194-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_country\_code")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-160">Código de país o región para el idioma de elección del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f194-160">Country/region code for the user's language of choice.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f194-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f194-164">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="0f194-164">Textual description of the current object.</span></span>

<span data-ttu-id="0f194-165">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0f194-165">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f194-166">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="0f194-166">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-167">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f194-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-169">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags"), [**Bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("script", "Account Disabled", "Home dir Required", "bloqueos", "Password Not Required", "Paswword not Change", "contraseña de prueba cifrada permitida", "cuenta temporal duplicada", "cuenta normal", "cuenta de confianza entre dominios", "cuenta de confianza de estación de trabajo", "cuenta de confianza de servidor", "no caducar contraseña", "cuenta de inicio de sesión de MNS", "tarjeta inteligente requerida", "de confianza para delegación", "no delegada", "usar solo la clave des", "no requerir autorización previa", "contraseña expirada")</span><span class="sxs-lookup"><span data-stu-id="0f194-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags"), [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Script", "Account Disabled", "Home Dir Required", "Lockout", "Password Not Required", "Paswword Can't Change", "Encrypted Test Password Allowed", "Temp Duplicate Account", "Normal Account", "InterDomain Trust Account", "WorkStation Trust Account", "Server Trust Account", "Don't Expire Password", "MNS Logon Account", "Smartcard Required", "Trusted For Delegation", "Not Delegated", "Use DES Key Only", "Don't Require Preauthorization", "Password Expired")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-170">Propiedades disponibles para este perfil de red.</span><span class="sxs-lookup"><span data-stu-id="0f194-170">The properties available to this network profile.</span></span>

<span data-ttu-id="0f194-171">Entre las propiedades que se pueden establecer se incluyen:</span><span class="sxs-lookup"><span data-stu-id="0f194-171">Properties that can be set include:</span></span>

<dt>

<span data-ttu-id="0f194-172">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f194-172">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-173">Script</span><span class="sxs-lookup"><span data-stu-id="0f194-173">Script</span></span>

<span data-ttu-id="0f194-174">Se ejecutó un script de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0f194-174">A logon script executed.</span></span> <span data-ttu-id="0f194-175">Este valor se debe establecer para el administrador de LAN 2,0.</span><span class="sxs-lookup"><span data-stu-id="0f194-175">This value must be set for LAN Manager 2.0.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-176">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="0f194-176">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-177">Cuenta deshabilitada</span><span class="sxs-lookup"><span data-stu-id="0f194-177">Account Disabled</span></span>

<span data-ttu-id="0f194-178">La cuenta del usuario está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="0f194-178">The user's account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-179">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="0f194-179">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-180">Se requiere el directorio particular</span><span class="sxs-lookup"><span data-stu-id="0f194-180">Home Directory Required</span></span>

<span data-ttu-id="0f194-181">Se requiere un directorio particular.</span><span class="sxs-lookup"><span data-stu-id="0f194-181">A home directory is required.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-182">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="0f194-182">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-183">Bloqueo</span><span class="sxs-lookup"><span data-stu-id="0f194-183">Lockout</span></span>

<span data-ttu-id="0f194-184">La cuenta está bloqueada actualmente. En el caso de [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), este valor se puede borrar para desbloquear una cuenta bloqueada previamente.</span><span class="sxs-lookup"><span data-stu-id="0f194-184">The account is currently locked out. For [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), this value can be cleared to unlock a previously locked account.</span></span> <span data-ttu-id="0f194-185">Este valor no se puede usar para bloquear una cuenta desbloqueada previamente.</span><span class="sxs-lookup"><span data-stu-id="0f194-185">This value cannot be used to lock a previously unlocked account.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-186">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="0f194-186">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-187">Contraseña no necesaria</span><span class="sxs-lookup"><span data-stu-id="0f194-187">Password Not Required</span></span>

<span data-ttu-id="0f194-188">No se requiere una contraseña.</span><span class="sxs-lookup"><span data-stu-id="0f194-188">No password is required.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-189">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="0f194-189">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-190">No se puede cambiar la contraseña</span><span class="sxs-lookup"><span data-stu-id="0f194-190">Password Cannot Change</span></span>

<span data-ttu-id="0f194-191">El usuario no puede cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="0f194-191">The user cannot change the password.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-192">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="0f194-192">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-193">Contraseña de prueba cifrada permitida</span><span class="sxs-lookup"><span data-stu-id="0f194-193">Encrypted Test Password Allowed</span></span>

</dd> <dt>

<span data-ttu-id="0f194-194">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="0f194-194">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-195">Cuenta temporal duplicada</span><span class="sxs-lookup"><span data-stu-id="0f194-195">Temp Duplicate Account</span></span>

<span data-ttu-id="0f194-196">Una cuenta para usuarios cuya cuenta principal se encuentra en otro dominio.</span><span class="sxs-lookup"><span data-stu-id="0f194-196">An account for users whose primary account is in another domain.</span></span> <span data-ttu-id="0f194-197">Esta cuenta proporciona acceso de usuario a este dominio, pero no a ningún dominio que confíe en este dominio.</span><span class="sxs-lookup"><span data-stu-id="0f194-197">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="0f194-198">El administrador de usuarios hace referencia a este tipo de cuenta como cuenta de usuario local.</span><span class="sxs-lookup"><span data-stu-id="0f194-198">The User Manager refers to this account type as a local user account.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-199">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="0f194-199">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-200">Cuenta normal</span><span class="sxs-lookup"><span data-stu-id="0f194-200">Normal Account</span></span>

<span data-ttu-id="0f194-201">Tipo de cuenta predeterminado que representa a un usuario típico.</span><span class="sxs-lookup"><span data-stu-id="0f194-201">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-202">2048 (0x800)</span><span class="sxs-lookup"><span data-stu-id="0f194-202">2048 (0x800)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-203">Cuenta de confianza entre dominios</span><span class="sxs-lookup"><span data-stu-id="0f194-203">Interdomain Trust Account</span></span>

<span data-ttu-id="0f194-204">Permiso para una cuenta de confianza para un dominio que confía en otros dominios.</span><span class="sxs-lookup"><span data-stu-id="0f194-204">A permit to a trust account for a domain that trusts other domains.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-205">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="0f194-205">4096 (0x1000)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-206">Cuenta de confianza de estación de trabajo</span><span class="sxs-lookup"><span data-stu-id="0f194-206">Workstation Trust Account</span></span>

<span data-ttu-id="0f194-207">Una cuenta de equipo para una estación de trabajo de Windows o un servidor que sea miembro de este dominio.</span><span class="sxs-lookup"><span data-stu-id="0f194-207">A computer account for a Windows workstation or server that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-208">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="0f194-208">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-209">Cuenta de confianza de servidor</span><span class="sxs-lookup"><span data-stu-id="0f194-209">Server Trust Account</span></span>

<span data-ttu-id="0f194-210">Una cuenta de equipo para un controlador de dominio de copia de seguridad que sea miembro de este dominio.</span><span class="sxs-lookup"><span data-stu-id="0f194-210">A computer account for a backup domain controller that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-211">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="0f194-211">65536 (0x10000)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-212">No expirar contraseña</span><span class="sxs-lookup"><span data-stu-id="0f194-212">Do Not Expire Password</span></span>

</dd> <dt>

<span data-ttu-id="0f194-213">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="0f194-213">131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-214">Cuenta de inicio de sesión de MNS</span><span class="sxs-lookup"><span data-stu-id="0f194-214">MNS Logon Account</span></span>

<span data-ttu-id="0f194-215">Tipo de cuenta de inicio de sesión del conjunto de nodos mayoritario (MNS) que representa un usuario de MNS.</span><span class="sxs-lookup"><span data-stu-id="0f194-215">Majority Node Set (MNS) logon account type that represents an MNS user.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-216">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="0f194-216">262144 (0x40000)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-217">Se requiere una tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="0f194-217">Smartcard Required</span></span>

</dd> <dt>

<span data-ttu-id="0f194-218">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="0f194-218">524288 (0x80000)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-219">De confianza para delegación</span><span class="sxs-lookup"><span data-stu-id="0f194-219">Trusted for Delegation</span></span>

</dd> <dt>

<span data-ttu-id="0f194-220">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="0f194-220">1048576 (0x100000)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-221">No delegado</span><span class="sxs-lookup"><span data-stu-id="0f194-221">Not Delegated</span></span>

</dd> <dt>

<span data-ttu-id="0f194-222">2097152 (0x200000)</span><span class="sxs-lookup"><span data-stu-id="0f194-222">2097152 (0x200000)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-223">Usar solo la clave DES</span><span class="sxs-lookup"><span data-stu-id="0f194-223">Use DES Key Only</span></span>

</dd> <dt>

<span data-ttu-id="0f194-224">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="0f194-224">4194304 (0x400000)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-225">No requerir autorización previa</span><span class="sxs-lookup"><span data-stu-id="0f194-225">Do Not Require Preauthorization</span></span>

</dd> <dt>

<span data-ttu-id="0f194-226">8388608 (0x800000)</span><span class="sxs-lookup"><span data-stu-id="0f194-226">8388608 (0x800000)</span></span>
</dt> <dd>

<span data-ttu-id="0f194-227">Contraseña expirada</span><span class="sxs-lookup"><span data-stu-id="0f194-227">Password Expired</span></span>

<span data-ttu-id="0f194-228">Indica que la contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="0f194-228">Indicates that the password has expired.</span></span>

</dd> </dl>

<span data-ttu-id="0f194-229">Las siguientes propiedades describen el tipo de cuenta.</span><span class="sxs-lookup"><span data-stu-id="0f194-229">The following properties describe the account type.</span></span> <span data-ttu-id="0f194-230">Solo se puede establecer un valor:</span><span class="sxs-lookup"><span data-stu-id="0f194-230">Only one value can be set:</span></span>

-   <span data-ttu-id="0f194-231">\_cuenta normal de fi \_</span><span class="sxs-lookup"><span data-stu-id="0f194-231">UF\_NORMAL\_ACCOUNT</span></span>
-   <span data-ttu-id="0f194-232">FI \_ - \_ cuenta duplicada temporal \_</span><span class="sxs-lookup"><span data-stu-id="0f194-232">UF\_TEMP\_DUPLICATE\_ACCOUNT</span></span>
-   <span data-ttu-id="0f194-233">cuenta de confianza de estación de trabajo de fi \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="0f194-233">UF\_WORKSTATION\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="0f194-234">\_cuenta de \_ confianza de servidor de up \_</span><span class="sxs-lookup"><span data-stu-id="0f194-234">UF\_SERVER\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="0f194-235">cuenta de confianza entre \_ dominios \_ \_</span><span class="sxs-lookup"><span data-stu-id="0f194-235">UF\_INTERDOMAIN\_TRUST\_ACCOUNT</span></span>

</dd> <dt>

<span data-ttu-id="0f194-236">**FullName**</span><span class="sxs-lookup"><span data-stu-id="0f194-236">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-239">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Full \_ Name")</span><span class="sxs-lookup"><span data-stu-id="0f194-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_full\_name")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-240">Nombre completo del usuario que pertenece al perfil de inicio de sesión de red.</span><span class="sxs-lookup"><span data-stu-id="0f194-240">Full name of the user belonging to the network login profile.</span></span> <span data-ttu-id="0f194-241">Esta cadena puede estar vacía si el usuario decide no asociar un nombre completo con un nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="0f194-241">This string can be empty if the user chooses not to associate a full name with a user name.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-242">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="0f194-242">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-245">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir")</span><span class="sxs-lookup"><span data-stu-id="0f194-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-246">Ruta de acceso al directorio particular del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f194-246">Path to the home directory of the user.</span></span> <span data-ttu-id="0f194-247">Esta cadena puede estar vacía si el usuario decide no especificar un directorio particular.</span><span class="sxs-lookup"><span data-stu-id="0f194-247">This string may be empty if the user chooses not to specify a home directory.</span></span>

<span data-ttu-id="0f194-248">Ejemplo: " \\ HOMEDIR"</span><span class="sxs-lookup"><span data-stu-id="0f194-248">Example:"\\HOMEDIR"</span></span>

</dd> <dt>

<span data-ttu-id="0f194-249">**HomeDirectoryDrive**</span><span class="sxs-lookup"><span data-stu-id="0f194-249">**HomeDirectoryDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-250">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-252">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir \_ Drive")</span><span class="sxs-lookup"><span data-stu-id="0f194-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir\_drive")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-253">Letra de unidad asignada al directorio principal del usuario para el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0f194-253">Drive letter assigned to the user's home directory for log on purposes.</span></span>

<span data-ttu-id="0f194-254">Ejemplo: "C:"</span><span class="sxs-lookup"><span data-stu-id="0f194-254">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="0f194-255">**LastLogoff**</span><span class="sxs-lookup"><span data-stu-id="0f194-255">**LastLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-256">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f194-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-258">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Logoff")</span><span class="sxs-lookup"><span data-stu-id="0f194-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logoff")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-259">El usuario cerró sesión por última vez en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0f194-259">User last logged off the system.</span></span> <span data-ttu-id="0f194-260">Este valor se calcula a partir del número de segundos transcurridos desde el 00:00:00 de enero de 1970.</span><span class="sxs-lookup"><span data-stu-id="0f194-260">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="0f194-261">Un valor de " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " significa que no se conoce la hora del último cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="0f194-261">A value of " \*\*\*\*\*\*\*\*\*\*\*\*\*\*.\*\*\*\*\*\*+\*\*\* " means that the last logoff time is unknown.</span></span> <span data-ttu-id="0f194-262">El formato de este valor es aaaammddhhmmss. mmmmmm SUTC.</span><span class="sxs-lookup"><span data-stu-id="0f194-262">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="0f194-263">Para obtener información sobre cómo convertir esta propiedad en la hora local, vea [tareas de WMI: fechas y horas](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="0f194-263">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="0f194-264">Ejemplo: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="0f194-264">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="0f194-265">**LastLogon**</span><span class="sxs-lookup"><span data-stu-id="0f194-265">**LastLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-266">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f194-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-268">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Logon")</span><span class="sxs-lookup"><span data-stu-id="0f194-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logon")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-269">El usuario inició sesión por última vez en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0f194-269">User last logged on to the system.</span></span> <span data-ttu-id="0f194-270">Este valor se calcula a partir del número de segundos transcurridos desde el 00:00:00 de enero de 1970.</span><span class="sxs-lookup"><span data-stu-id="0f194-270">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="0f194-271">El formato de este valor es aaaammddhhmmss. mmmmmm SUTC.</span><span class="sxs-lookup"><span data-stu-id="0f194-271">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="0f194-272">Para obtener información sobre cómo convertir esta propiedad en la hora local, vea [tareas de WMI: fechas y horas](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="0f194-272">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="0f194-273">Ejemplo: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="0f194-273">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="0f194-274">**LogonHours**</span><span class="sxs-lookup"><span data-stu-id="0f194-274">**LogonHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-275">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-277">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ hours")</span><span class="sxs-lookup"><span data-stu-id="0f194-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_hours")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-278">Horas durante la semana en las que el usuario puede iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="0f194-278">Times during the week when the user can log on.</span></span> <span data-ttu-id="0f194-279">Cada bit representa una unidad de tiempo especificada por la propiedad **UnitsPerWeek** .</span><span class="sxs-lookup"><span data-stu-id="0f194-279">Each bit represents a unit of time specified by the **UnitsPerWeek** property.</span></span> <span data-ttu-id="0f194-280">Por ejemplo, si la unidad de tiempo es cada hora, el primer bit (bit 0, palabra 0) es domingo, de 0:00 a 0:59, el segundo bit (bit 1, palabra 0) es domingo, 1:00 a 1:59, etc.</span><span class="sxs-lookup"><span data-stu-id="0f194-280">For instance, if the unit of time is hourly, the first bit (bit 0, word 0) is Sunday, 0:00 to 0:59, the second bit (bit 1, word 0) is Sunday, 1:00 to 1:59, and so on.</span></span> <span data-ttu-id="0f194-281">Si este miembro se establece en **null**, no hay ninguna restricción de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0f194-281">If this member is set to **NULL**, then there is no time restriction.</span></span> <span data-ttu-id="0f194-282">La hora se establece en GMT y debe ajustarse para otras zonas horarias (por ejemplo, GMT menos 8 horas para PST).</span><span class="sxs-lookup"><span data-stu-id="0f194-282">The time is set to GMT and must be adjusted for other time zones (for example, GMT minus 8 hours for PST).</span></span>

</dd> <dt>

<span data-ttu-id="0f194-283">**LogonServer**</span><span class="sxs-lookup"><span data-stu-id="0f194-283">**LogonServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-284">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-286">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ Server")</span><span class="sxs-lookup"><span data-stu-id="0f194-286">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_server")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-287">Nombre del servidor al que se envían las solicitudes de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0f194-287">Name of the server to which logon requests are sent.</span></span> <span data-ttu-id="0f194-288">Los nombres de servidor deben ir precedidos de dos barras diagonales inversas ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="0f194-288">Server names should be preceded by two backslashes (\\\\).</span></span> <span data-ttu-id="0f194-289">Un nombre de servidor con un asterisco ( \\ \\ \* ) indica que la solicitud de inicio de sesión se puede controlar mediante cualquier servidor de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0f194-289">A server name with an asterisk (\\\\\*) indicates that the logon request can be handled by any logon server.</span></span> <span data-ttu-id="0f194-290">Una cadena nula indica que las solicitudes se envían al controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="0f194-290">A null string indicates that requests are sent to the domain controller.</span></span>

<span data-ttu-id="0f194-291">Ejemplo: "mi \\ \\ Server"</span><span class="sxs-lookup"><span data-stu-id="0f194-291">Example: "\\\\MyServer"</span></span>

</dd> <dt>

<span data-ttu-id="0f194-292">**MaximumStorage**</span><span class="sxs-lookup"><span data-stu-id="0f194-292">**MaximumStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-293">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0f194-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-295">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Max \_ Storage"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="0f194-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_max\_storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-296">Cantidad máxima de espacio en disco disponible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="0f194-296">Maximum amount of disk space available to the user.</span></span> <span data-ttu-id="0f194-297">Si MaximumStorage se establece en USER \_ MAXSTORAGE \_ Unlimited, el usuario puede usar todo el espacio disponible en disco.</span><span class="sxs-lookup"><span data-stu-id="0f194-297">If MaximumStorage is set to USER\_MAXSTORAGE\_UNLIMITED, the user is allowed to use all of the available disk space.</span></span>

<span data-ttu-id="0f194-298">Ejemplo: 10 millones</span><span class="sxs-lookup"><span data-stu-id="0f194-298">Example: 10000000</span></span>

<span data-ttu-id="0f194-299">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f194-299">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0f194-300">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0f194-300">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-303">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Name")</span><span class="sxs-lookup"><span data-stu-id="0f194-303">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_name")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-304">Cuenta de usuario en un dominio o equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="0f194-304">User account on a particular domain or computer.</span></span> <span data-ttu-id="0f194-305">El número de caracteres del nombre no puede superar el valor de UNLEN.</span><span class="sxs-lookup"><span data-stu-id="0f194-305">The number of characters in the name cannot exceed the value of UNLEN.</span></span>

<span data-ttu-id="0f194-306">Ejemplo: \\ "algúndominio de los</span><span class="sxs-lookup"><span data-stu-id="0f194-306">Example: "somedomain\\johndoe"</span></span>

</dd> <dt>

<span data-ttu-id="0f194-307">**NumberOfLogons**</span><span class="sxs-lookup"><span data-stu-id="0f194-307">**NumberOfLogons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-308">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f194-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-310">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ NUM \_ inicios de sesión")</span><span class="sxs-lookup"><span data-stu-id="0f194-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_num\_logons")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-311">Número de veces que el usuario intentó iniciar sesión en esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="0f194-311">Number of successful times the user tried to log on to this account.</span></span> <span data-ttu-id="0f194-312">Un valor de 0xFFFFFFFF indica que el valor es desconocido.</span><span class="sxs-lookup"><span data-stu-id="0f194-312">A value of 0xFFFFFFFF indicates that the value is unknown.</span></span> <span data-ttu-id="0f194-313">Esta propiedad se mantiene por separado en cada controlador de dominio de copia de seguridad (BDC) del dominio.</span><span class="sxs-lookup"><span data-stu-id="0f194-313">This property is maintained separately on each backup domain controller (BDC) in the domain.</span></span> <span data-ttu-id="0f194-314">Para obtener un valor preciso, solo se debe usar el valor más grande de todos los BDC.</span><span class="sxs-lookup"><span data-stu-id="0f194-314">To get an accurate value, only the largest value from all BDCs should be used.</span></span>

<span data-ttu-id="0f194-315">Ejemplo: 4</span><span class="sxs-lookup"><span data-stu-id="0f194-315">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="0f194-316">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="0f194-316">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-319">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parms")</span><span class="sxs-lookup"><span data-stu-id="0f194-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_parms")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-320">Espacio reservado para que lo usen las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0f194-320">Space set aside for use by applications.</span></span> <span data-ttu-id="0f194-321">Esta cadena puede ser null o puede tener cualquier número de caracteres antes del carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="0f194-321">This string can be null, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="0f194-322">Los productos de Microsoft usan este miembro para almacenar información de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="0f194-322">Microsoft products use this member to store user configuration information.</span></span> <span data-ttu-id="0f194-323">No modifique esta información, ya que este valor es específico de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="0f194-323">Do not modify this information, because this value is specific to an application.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-324">**Contraseñas**</span><span class="sxs-lookup"><span data-stu-id="0f194-324">**PasswordAge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-325">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f194-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-327">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ password \_ Age")</span><span class="sxs-lookup"><span data-stu-id="0f194-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_password\_age")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-328">Cantidad de tiempo que una contraseña ha estado en vigor.</span><span class="sxs-lookup"><span data-stu-id="0f194-328">Length of time a password has been in effect.</span></span> <span data-ttu-id="0f194-329">Este valor se mide a partir del número de segundos transcurridos desde que se cambió la contraseña por última vez.</span><span class="sxs-lookup"><span data-stu-id="0f194-329">This value is measured from the number of seconds elapsed since the password was last changed.</span></span>

<span data-ttu-id="0f194-330">Ejemplo: 00001201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="0f194-330">Example: 00001201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="0f194-331">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="0f194-331">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-332">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f194-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-334">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| Administración de red estructuras de usuario de la \| [**\_ \_ información \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ passwd \_ Age")</span><span class="sxs-lookup"><span data-stu-id="0f194-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_MODALS\_INFO\_0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0)\|usrmod0\_max\_passwd\_age")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-335">Fecha y hora en que expira la contraseña.</span><span class="sxs-lookup"><span data-stu-id="0f194-335">Date and time the password expires.</span></span> <span data-ttu-id="0f194-336">El valor se establece en este formato: aaaammddhhmmss. mmmmmm SUTC</span><span class="sxs-lookup"><span data-stu-id="0f194-336">The value is set in this format: yyyymmddhhmmss.mmmmmm sutc</span></span>

<span data-ttu-id="0f194-337">Ejemplo: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="0f194-337">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="0f194-338">**PrimaryGroupId**</span><span class="sxs-lookup"><span data-stu-id="0f194-338">**PrimaryGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-339">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f194-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-341">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Primary \_ Group \_ ID")</span><span class="sxs-lookup"><span data-stu-id="0f194-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_primary\_group\_id")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-342">Identificador relativo (RID) del grupo global principal para este usuario.</span><span class="sxs-lookup"><span data-stu-id="0f194-342">Relative identifier (RID) of the Primary Global Group for this user.</span></span> <span data-ttu-id="0f194-343">El identificador comprueba el grupo primario al que pertenece el perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f194-343">The identifier verifies the primary group to which the user's profile belongs.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-344">**Privilegios**</span><span class="sxs-lookup"><span data-stu-id="0f194-344">**Privileges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-345">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f194-345">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-347">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ priv")</span><span class="sxs-lookup"><span data-stu-id="0f194-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_priv")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-348">Nivel de privilegio asignado a la **propiedad \_ nombre de usri3** .</span><span class="sxs-lookup"><span data-stu-id="0f194-348">Level of privilege assigned to the **usri3\_name** property.</span></span>

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

<span data-ttu-id="0f194-349">**Invitado** (0)</span><span class="sxs-lookup"><span data-stu-id="0f194-349">**Guest** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

<span data-ttu-id="0f194-350">**Usuario** (1)</span><span class="sxs-lookup"><span data-stu-id="0f194-350">**User** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

<span data-ttu-id="0f194-351">**Administrador** (2)</span><span class="sxs-lookup"><span data-stu-id="0f194-351">**Administrator** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f194-352">**Perfil**</span><span class="sxs-lookup"><span data-stu-id="0f194-352">**Profile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-355">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Profile")</span><span class="sxs-lookup"><span data-stu-id="0f194-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_profile")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-356">Ruta de acceso al perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f194-356">Path to the user's profile.</span></span> <span data-ttu-id="0f194-357">Este valor puede ser una cadena nula, una ruta de acceso absoluta local o una ruta de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="0f194-357">This value can be a null string, a local absolute path, or a UNC path.</span></span> <span data-ttu-id="0f194-358">Un perfil de usuario contiene opciones de configuración que se pueden personalizar para cada usuario, como los colores del escritorio.</span><span class="sxs-lookup"><span data-stu-id="0f194-358">A user profile contains settings that are customizable for each user such as the desktop colors.</span></span>

<span data-ttu-id="0f194-359">Ejemplo: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="0f194-359">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="0f194-360">**ScriptPath**</span><span class="sxs-lookup"><span data-stu-id="0f194-360">**ScriptPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-363">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ script \_ path")</span><span class="sxs-lookup"><span data-stu-id="0f194-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_script\_path")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-364">Ruta de acceso al directorio del script de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f194-364">Directory path to the user's logon script.</span></span> <span data-ttu-id="0f194-365">Un script de inicio de sesión ejecuta automáticamente un conjunto de comandos cada vez que un usuario inicia sesión en un sistema.</span><span class="sxs-lookup"><span data-stu-id="0f194-365">A logon script automatically executes a set of commands each time a user logs on to a system.</span></span>

<span data-ttu-id="0f194-366">Ejemplo: "C: \\ Win \\ profiles \\ ThomasSteven"</span><span class="sxs-lookup"><span data-stu-id="0f194-366">Example: "C:\\win\\profiles\\ThomasSteven"</span></span>

</dd> <dt>

<span data-ttu-id="0f194-367">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="0f194-367">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-368">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-370">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0f194-370">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0f194-371">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="0f194-371">Identifier by which the current object is known.</span></span>

<span data-ttu-id="0f194-372">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0f194-372">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f194-373">**UnitsPerWeek**</span><span class="sxs-lookup"><span data-stu-id="0f194-373">**UnitsPerWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-374">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f194-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-376">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Units \_ per \_ Week")</span><span class="sxs-lookup"><span data-stu-id="0f194-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_units\_per\_week")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-377">Número de unidades de tiempo en que se divide la semana.</span><span class="sxs-lookup"><span data-stu-id="0f194-377">Number of time units the week is divided into.</span></span> <span data-ttu-id="0f194-378">Se usa con la propiedad **LogonHours** para limitar el acceso del usuario al equipo.</span><span class="sxs-lookup"><span data-stu-id="0f194-378">It is used with the **LogonHours** property to limit user access to the computer.</span></span>

<span data-ttu-id="0f194-379">Ejemplo: 168 (horas por semana)</span><span class="sxs-lookup"><span data-stu-id="0f194-379">Example: 168 (hours per week)</span></span>

</dd> <dt>

<span data-ttu-id="0f194-380">**UserComment**</span><span class="sxs-lookup"><span data-stu-id="0f194-380">**UserComment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-381">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-383">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ comment")</span><span class="sxs-lookup"><span data-stu-id="0f194-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_usr\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-384">Comentario o descripción definidos por el usuario para este perfil.</span><span class="sxs-lookup"><span data-stu-id="0f194-384">User-defined comment or description for this profile.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-385">**UserId**</span><span class="sxs-lookup"><span data-stu-id="0f194-385">**UserId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-386">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f194-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-388">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ User \_ ID")</span><span class="sxs-lookup"><span data-stu-id="0f194-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_user\_id")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-389">RID del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f194-389">RID of the user.</span></span> <span data-ttu-id="0f194-390">El identificador comprueba que el usuario existe y es único para este dominio.</span><span class="sxs-lookup"><span data-stu-id="0f194-390">The identifier verifies that the user exists and is unique to this domain.</span></span>

</dd> <dt>

<span data-ttu-id="0f194-391">**UserType**</span><span class="sxs-lookup"><span data-stu-id="0f194-391">**UserType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-392">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-394">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags")</span><span class="sxs-lookup"><span data-stu-id="0f194-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-395">Tipo de cuenta en la que el usuario tiene privilegios.</span><span class="sxs-lookup"><span data-stu-id="0f194-395">Type of account to which the user has privileges.</span></span>

<span data-ttu-id="0f194-396">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="0f194-396">The values are:</span></span>

-   <span data-ttu-id="0f194-397">"Cuenta normal"</span><span class="sxs-lookup"><span data-stu-id="0f194-397">"Normal Account"</span></span>
-   <span data-ttu-id="0f194-398">"Cuenta duplicada"</span><span class="sxs-lookup"><span data-stu-id="0f194-398">"Duplicate Account"</span></span>
-   <span data-ttu-id="0f194-399">"Cuenta de confianza de estación de trabajo"</span><span class="sxs-lookup"><span data-stu-id="0f194-399">"Workstation Trust Account"</span></span>
-   <span data-ttu-id="0f194-400">"Cuenta de confianza de servidor"</span><span class="sxs-lookup"><span data-stu-id="0f194-400">"Server Trust Account"</span></span>
-   <span data-ttu-id="0f194-401">"Cuenta de confianza entre dominios"</span><span class="sxs-lookup"><span data-stu-id="0f194-401">"Interdomain Trust Account"</span></span>
-   <span data-ttu-id="0f194-402">Unknown</span><span class="sxs-lookup"><span data-stu-id="0f194-402">"Unknown"</span></span>

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="0f194-403">**Cuenta normal** ("cuenta normal")</span><span class="sxs-lookup"><span data-stu-id="0f194-403">**Normal Account** ("Normal Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="0f194-404">**Cuenta duplicada** ("cuenta duplicada")</span><span class="sxs-lookup"><span data-stu-id="0f194-404">**Duplicate Account** ("Duplicate Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="0f194-405">**Cuenta de confianza de estación de trabajo** ("cuenta de confianza de estación de trabajo")</span><span class="sxs-lookup"><span data-stu-id="0f194-405">**Workstation Trust Account** ("Workstation Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="0f194-406">**Cuenta de confianza del servidor** ("cuenta de confianza del servidor")</span><span class="sxs-lookup"><span data-stu-id="0f194-406">**Server Trust Account** ("Server Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="0f194-407">**Cuenta de confianza entre dominios** ("cuenta de confianza entre dominios")</span><span class="sxs-lookup"><span data-stu-id="0f194-407">**Interdomain Trust Account** ("Interdomain Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f194-408">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="0f194-408">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f194-409">**Estaciones**</span><span class="sxs-lookup"><span data-stu-id="0f194-409">**Workstations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f194-410">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f194-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f194-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f194-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f194-412">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Workstation")</span><span class="sxs-lookup"><span data-stu-id="0f194-412">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_workstations")</span></span>
</dt> </dl>

<span data-ttu-id="0f194-413">Nombres de las estaciones de trabajo desde las que el usuario puede iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="0f194-413">Names of workstations from which the user can log on.</span></span> <span data-ttu-id="0f194-414">Se pueden especificar hasta ocho estaciones de trabajo; los nombres deben estar separados por comas (,).</span><span class="sxs-lookup"><span data-stu-id="0f194-414">Up to eight workstations can be specified; the names must be separated by commas (,).</span></span> <span data-ttu-id="0f194-415">Una cadena nula indica que no hay restricciones.</span><span class="sxs-lookup"><span data-stu-id="0f194-415">A null string indicates no restrictions.</span></span> <span data-ttu-id="0f194-416">Para deshabilitar los inicios de sesión de todas las estaciones de trabajo en esta cuenta, establezca el \_ ACCOUNTDISABLE de fi en la propiedad **Flags** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="0f194-416">To disable logons from all workstations to this account, set the UF\_ACCOUNTDISABLE in the **Flags** property of this class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f194-417">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f194-417">Remarks</span></span>

<span data-ttu-id="0f194-418">La **clase \_ NetworkLoginProfile de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0f194-418">The **Win32\_NetworkLoginProfile** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="0f194-419">El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro.</span><span class="sxs-lookup"><span data-stu-id="0f194-419">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="0f194-420">Para obtener más información, vea [ejecutar operaciones con privilegios](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="0f194-420">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0f194-421">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0f194-421">Examples</span></span>

<span data-ttu-id="0f194-422">El ejemplo de PowerShell [Mostrar perfiles de inicio de sesión de red](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) devuelve información de inicio de sesión de red para todos los usuarios de un equipo.</span><span class="sxs-lookup"><span data-stu-id="0f194-422">The [List Network Login Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) PowerShell sample returns network login information for all the users of a computer.</span></span>

<span data-ttu-id="0f194-423">El siguiente ejemplo de VBScript devuelve información de inicio de sesión de red.</span><span class="sxs-lookup"><span data-stu-id="0f194-423">The following VBScript sample returns network login information.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0f194-424">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f194-424">Requirements</span></span>



| <span data-ttu-id="0f194-425">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f194-425">Requirement</span></span> | <span data-ttu-id="0f194-426">Value</span><span class="sxs-lookup"><span data-stu-id="0f194-426">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f194-427">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f194-427">Minimum supported client</span></span><br/> | <span data-ttu-id="0f194-428">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f194-428">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f194-429">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f194-429">Minimum supported server</span></span><br/> | <span data-ttu-id="0f194-430">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f194-430">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f194-431">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0f194-431">Namespace</span></span><br/>                | <span data-ttu-id="0f194-432">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0f194-432">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f194-433">MOF</span><span class="sxs-lookup"><span data-stu-id="0f194-433">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f194-434"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f194-434"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f194-435">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0f194-435">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f194-436"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f194-436"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f194-437">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f194-437">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f194-438">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="0f194-438">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="0f194-439">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0f194-439">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
