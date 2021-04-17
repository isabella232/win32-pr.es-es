---
description: Win32 \_ SystemAccount&\# 8194; La clase WMI representa una cuenta del sistema.
ms.assetid: 0f745d93-cbac-428e-bf27-56f6e97d529f
ms.tgt_platform: multiple
title: Win32_SystemAccount (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemAccount
- Win32_SystemAccount.Caption
- Win32_SystemAccount.Description
- Win32_SystemAccount.InstallDate
- Win32_SystemAccount.Status
- Win32_SystemAccount.LocalAccount
- Win32_SystemAccount.SID
- Win32_SystemAccount.SIDType
- Win32_SystemAccount.Domain
- Win32_SystemAccount.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ef246a0ee372c5755aeb30980095e7f2f6ca1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659693"
---
# <a name="win32_systemaccount-class"></a><span data-ttu-id="7fe86-103">\_Clase Win32 SystemAccount</span><span class="sxs-lookup"><span data-stu-id="7fe86-103">Win32\_SystemAccount class</span></span>

<span data-ttu-id="7fe86-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemAccount de Win32** representa una cuenta del sistema.</span><span class="sxs-lookup"><span data-stu-id="7fe86-104">The **Win32\_SystemAccount** [WMI class](../wmisdk/retrieving-a-class.md) represents a system account.</span></span> <span data-ttu-id="7fe86-105">El sistema operativo y los servicios utilizan la cuenta del sistema.</span><span class="sxs-lookup"><span data-stu-id="7fe86-105">The system account is used by the operating system and services.</span></span> <span data-ttu-id="7fe86-106">Hay muchos servicios y procesos dentro de Windows que necesitan la capacidad de iniciar sesión internamente, por ejemplo, durante una instalación de Windows.</span><span class="sxs-lookup"><span data-stu-id="7fe86-106">There are many services and processes within Windows that need the capability to logon internally, for example, during a Windows installation.</span></span> <span data-ttu-id="7fe86-107">La cuenta del sistema se diseñó para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="7fe86-107">The system account was designed for that purpose.</span></span>

<span data-ttu-id="7fe86-108">La cuenta del sistema es una cuenta interna que no se muestra en el administrador de usuarios, no se puede Agregar a ningún grupo y no puede tener derechos de usuario asignados.</span><span class="sxs-lookup"><span data-stu-id="7fe86-108">The system account is an internal account that does not show up in User Manager, cannot be added to any groups, and cannot have user rights assigned to it.</span></span> <span data-ttu-id="7fe86-109">Sin embargo, la cuenta del sistema se muestra en un volumen del sistema de archivos NTFS en el administrador de archivos, que se encuentra en la sección permisos del menú seguridad.</span><span class="sxs-lookup"><span data-stu-id="7fe86-109">However, the system account does show up on an NTFS file system volume in file manager, which is located in the Permissions section of the Security menu.</span></span> <span data-ttu-id="7fe86-110">De forma predeterminada, se concede a la cuenta del sistema control total sobre todos los archivos de un volumen del sistema de archivos NTFS, lo que significa que la cuenta del sistema tiene los mismos privilegios funcionales que la cuenta de administrador.</span><span class="sxs-lookup"><span data-stu-id="7fe86-110">By default, the system account is granted full control to all files on an NTFS file system volume, which means that the system account has the same functional privileges as the administrator account.</span></span>

<span data-ttu-id="7fe86-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7fe86-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7fe86-112">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7fe86-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fe86-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fe86-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemAccount : Win32_Account
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  LocalAccount;
  string   SID;
  uint8    SIDType;
  string   Domain;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="7fe86-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="7fe86-114">Members</span></span>

<span data-ttu-id="7fe86-115">La **clase \_ SystemAccount de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7fe86-115">The **Win32\_SystemAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="7fe86-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7fe86-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fe86-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7fe86-117">Properties</span></span>

<span data-ttu-id="7fe86-118">La **clase \_ SystemAccount de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7fe86-118">The **Win32\_SystemAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fe86-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7fe86-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe86-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7fe86-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7fe86-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-122">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7fe86-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7fe86-123">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7fe86-123">A short textual description of the object.</span></span>

<span data-ttu-id="7fe86-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7fe86-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fe86-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fe86-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe86-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7fe86-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7fe86-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-128">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7fe86-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7fe86-129">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7fe86-129">A textual description of the object.</span></span>

<span data-ttu-id="7fe86-130">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7fe86-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fe86-131">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="7fe86-131">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe86-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7fe86-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7fe86-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-134">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Functions \| domainname")</span><span class="sxs-lookup"><span data-stu-id="7fe86-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="7fe86-135">Nombre del dominio de Windows al que pertenece la cuenta del sistema.</span><span class="sxs-lookup"><span data-stu-id="7fe86-135">Name of the Windows domain to which the system account belongs.</span></span>

<span data-ttu-id="7fe86-136">Ejemplo: "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="7fe86-136">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="7fe86-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7fe86-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe86-138">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7fe86-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7fe86-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-140">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7fe86-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7fe86-141">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="7fe86-141">Indicates when the object was installed.</span></span> <span data-ttu-id="7fe86-142">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="7fe86-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7fe86-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7fe86-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fe86-144">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="7fe86-144">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe86-145">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7fe86-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7fe86-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-147">Calificadores: [ **fijos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7fe86-147">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7fe86-148">Si es **true**, la cuenta se define en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="7fe86-148">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="7fe86-149">Para recuperar solo las cuentas definidas en el equipo local, diseñe una consulta que incluya la condición "LocalAccount =**true**".</span><span class="sxs-lookup"><span data-stu-id="7fe86-149">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="7fe86-150">Esta propiedad se hereda de [**la \_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="7fe86-150">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fe86-151">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7fe86-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe86-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7fe86-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7fe86-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-154">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structure \| Name")</span><span class="sxs-lookup"><span data-stu-id="7fe86-154">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="7fe86-155">Nombre de la cuenta del sistema de Windows en el dominio especificado por la propiedad de **dominio** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="7fe86-155">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="7fe86-156">**SID**</span><span class="sxs-lookup"><span data-stu-id="7fe86-156">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe86-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7fe86-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7fe86-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-159">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| (identificadores de seguridad (SID)")</span><span class="sxs-lookup"><span data-stu-id="7fe86-159">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="7fe86-160">Identificador de seguridad (SID) para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="7fe86-160">Security identifier (SID) for this account.</span></span> <span data-ttu-id="7fe86-161">Un SID es un valor de cadena de longitud variable que se usa para identificar un administrador de confianza.</span><span class="sxs-lookup"><span data-stu-id="7fe86-161">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="7fe86-162">Cada cuenta tiene un SID único emitido por una autoridad (como un dominio de Windows), almacenado en una base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7fe86-162">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="7fe86-163">Cuando un usuario inicia sesión, el sistema recupera el SID del usuario de la base de datos y lo coloca en el token de acceso del usuario.</span><span class="sxs-lookup"><span data-stu-id="7fe86-163">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="7fe86-164">El sistema utiliza el SID en el token de acceso del usuario para identificar al usuario en todas las interacciones posteriores con la seguridad de Windows.</span><span class="sxs-lookup"><span data-stu-id="7fe86-164">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="7fe86-165">Cuando se ha usado un SID como identificador único para un usuario o grupo, no se puede volver a usar para identificar a otro usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="7fe86-165">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="7fe86-166">Esta propiedad se hereda de [**la \_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="7fe86-166">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fe86-167">**SID**</span><span class="sxs-lookup"><span data-stu-id="7fe86-167">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe86-168">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7fe86-168">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7fe86-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-170">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Access Control tipos de enumeración \| \_ nombre SID \_ usar")</span><span class="sxs-lookup"><span data-stu-id="7fe86-170">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="7fe86-171">Valores enumerados que especifican el tipo de identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="7fe86-171">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="7fe86-172">Esta propiedad se hereda de [**la \_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="7fe86-172">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="7fe86-173">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="7fe86-173">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="7fe86-174">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="7fe86-174">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="7fe86-175">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="7fe86-175">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="7fe86-176">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="7fe86-176">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="7fe86-177">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="7fe86-177">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="7fe86-178">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="7fe86-178">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="7fe86-179">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="7fe86-179">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="7fe86-180">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="7fe86-180">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="7fe86-181">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="7fe86-181">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7fe86-182">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7fe86-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe86-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7fe86-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7fe86-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe86-185">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="7fe86-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7fe86-186">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7fe86-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="7fe86-187">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="7fe86-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7fe86-188">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="7fe86-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7fe86-189">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="7fe86-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7fe86-190">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="7fe86-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7fe86-191">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="7fe86-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7fe86-192">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="7fe86-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7fe86-193">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7fe86-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7fe86-194">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7fe86-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7fe86-195">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7fe86-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7fe86-196">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7fe86-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7fe86-197">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7fe86-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7fe86-198">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7fe86-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7fe86-199">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7fe86-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7fe86-200">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7fe86-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7fe86-201">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7fe86-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7fe86-202">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7fe86-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7fe86-203">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7fe86-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7fe86-204">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7fe86-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7fe86-205">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7fe86-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7fe86-206">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7fe86-206">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="7fe86-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7fe86-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7fe86-208">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fe86-208">Remarks</span></span>

<span data-ttu-id="7fe86-209">La clase **Win32 \_ SystemAccount** se deriva de la [**\_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="7fe86-209">The **Win32\_SystemAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe86-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fe86-210">Requirements</span></span>



| <span data-ttu-id="7fe86-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fe86-211">Requirement</span></span> | <span data-ttu-id="7fe86-212">Value</span><span class="sxs-lookup"><span data-stu-id="7fe86-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe86-213">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fe86-213">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe86-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fe86-214">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7fe86-215">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fe86-215">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe86-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fe86-216">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7fe86-217">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7fe86-217">Namespace</span></span><br/>                | <span data-ttu-id="7fe86-218">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7fe86-218">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7fe86-219">MOF</span><span class="sxs-lookup"><span data-stu-id="7fe86-219">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fe86-220"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fe86-220"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fe86-221">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7fe86-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fe86-222"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fe86-222"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fe86-223">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fe86-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe86-224">**\_Cuenta Win32**</span><span class="sxs-lookup"><span data-stu-id="7fe86-224">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="7fe86-225">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="7fe86-225">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
