---
description: La de Win32 \_ cuentadeusuario&\# 32; La clase WMI contiene información acerca de una cuenta de usuario en un equipo que ejecuta Windows.
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Win32_UserAccount (clase)
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080137"
---
# <a name="win32_useraccount-class"></a><span data-ttu-id="10298-103">Win32 \_ cuentadeusuario (clase)</span><span class="sxs-lookup"><span data-stu-id="10298-103">Win32\_UserAccount class</span></span>

<span data-ttu-id="10298-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ cuentadeusuario de Win32** contiene información acerca de una cuenta de usuario en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="10298-104">The **Win32\_UserAccount** [WMI class](../wmisdk/retrieving-a-class.md) contains information about a user account on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="10298-105">Dado que el **nombre** y el **dominio** son propiedades clave, la enumeración de **Win32 \_ cuentadeusuario** en una red de gran tamaño puede afectar negativamente al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="10298-105">Because both the **Name** and **Domain** are key properties, enumerating **Win32\_UserAccount** on a large network can negatively affect performance.</span></span> <span data-ttu-id="10298-106">Llamar a **GetObject** o consultar una instancia específica tiene menos impacto.</span><span class="sxs-lookup"><span data-stu-id="10298-106">Calling **GetObject** or querying for a specific instance has less impact.</span></span>

 

<span data-ttu-id="10298-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="10298-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="10298-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="10298-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="10298-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10298-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="10298-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="10298-110">Members</span></span>

<span data-ttu-id="10298-111">La clase **Win32 \_ cuentadeusuario** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="10298-111">The **Win32\_UserAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="10298-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="10298-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="10298-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10298-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="10298-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="10298-114">Methods</span></span>

<span data-ttu-id="10298-115">La clase **Win32 \_ cuentadeusuario** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="10298-115">The **Win32\_UserAccount** class has these methods.</span></span>



| <span data-ttu-id="10298-116">Método</span><span class="sxs-lookup"><span data-stu-id="10298-116">Method</span></span>                                                     | <span data-ttu-id="10298-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="10298-117">Description</span></span>                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="10298-118">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="10298-118">**Rename**</span></span>](rename-method-in-class-win32-useraccount.md) | <span data-ttu-id="10298-119">Permite cambiar el nombre de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="10298-119">Allows for the renaming of the user account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="10298-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10298-120">Properties</span></span>

<span data-ttu-id="10298-121">La clase **Win32 \_ cuentadeusuario** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="10298-121">The **Win32\_UserAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10298-122">**AccountType**</span><span class="sxs-lookup"><span data-stu-id="10298-122">**AccountType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-123">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10298-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10298-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10298-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10298-125">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ flags")</span><span class="sxs-lookup"><span data-stu-id="10298-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|usri2\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="10298-126">Marcas que describen las características de una cuenta de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="10298-126">Flags that describe the characteristics of a Windows user account.</span></span>

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="10298-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Cuenta duplicada temporal** (256)</span><span class="sxs-lookup"><span data-stu-id="10298-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Temporary duplicate account** (256)</span></span>


</dt> <dd>

<span data-ttu-id="10298-128">**FI \_ - \_ cuenta duplicada temporal \_**</span><span class="sxs-lookup"><span data-stu-id="10298-128">**UF\_TEMP\_DUPLICATE\_ACCOUNT**</span></span>

<span data-ttu-id="10298-129">Cuenta de usuario local para los usuarios que tienen una cuenta principal en otro dominio.</span><span class="sxs-lookup"><span data-stu-id="10298-129">Local user account for users who have a primary account in another domain.</span></span> <span data-ttu-id="10298-130">Esta cuenta solo proporciona acceso de usuario a este dominio, no a ningún dominio que confíe en este dominio.</span><span class="sxs-lookup"><span data-stu-id="10298-130">This account provides user access to this domain only—not to any domain that trusts this domain.</span></span>

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="10298-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Cuenta normal** (512)</span><span class="sxs-lookup"><span data-stu-id="10298-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Normal account** (512)</span></span>


</dt> <dd>

<span data-ttu-id="10298-132">**\_cuenta normal de fi \_**</span><span class="sxs-lookup"><span data-stu-id="10298-132">**UF\_NORMAL\_ACCOUNT**</span></span>

<span data-ttu-id="10298-133">Tipo de cuenta predeterminado que representa a un usuario típico.</span><span class="sxs-lookup"><span data-stu-id="10298-133">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="10298-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Cuenta de confianza entre dominios** (2048)</span><span class="sxs-lookup"><span data-stu-id="10298-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Interdomain trust account** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="10298-135">**cuenta de confianza entre \_ dominios \_ \_**</span><span class="sxs-lookup"><span data-stu-id="10298-135">**UF\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="10298-136">Cuenta para un dominio del sistema que confía en otros dominios.</span><span class="sxs-lookup"><span data-stu-id="10298-136">Account for a system domain that trusts other domains.</span></span>

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="10298-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Cuenta de confianza de estación de trabajo** (4096)</span><span class="sxs-lookup"><span data-stu-id="10298-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Workstation trust account** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="10298-138">**cuenta de confianza de estación de trabajo de fi \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="10298-138">**UF\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="10298-139">Cuenta de equipo para un equipo que ejecuta Windows y que es miembro de este dominio.</span><span class="sxs-lookup"><span data-stu-id="10298-139">Computer account for a computer system running Windows that is a member of this domain.</span></span>

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="10298-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Cuenta de confianza de servidor** (8192)</span><span class="sxs-lookup"><span data-stu-id="10298-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Server trust account** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="10298-141">**\_cuenta de \_ confianza de servidor de up \_**</span><span class="sxs-lookup"><span data-stu-id="10298-141">**UF\_SERVER\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="10298-142">Cuenta para un controlador de dominio de copia de seguridad del sistema que es miembro de este dominio.</span><span class="sxs-lookup"><span data-stu-id="10298-142">Account for a system backup domain controller that is a member of this domain.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10298-143">**Caption**</span><span class="sxs-lookup"><span data-stu-id="10298-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10298-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10298-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10298-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10298-146">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="10298-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="10298-147">Dominio y nombre de usuario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="10298-147">Domain and username of the account.</span></span>

<span data-ttu-id="10298-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10298-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10298-149">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="10298-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10298-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10298-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10298-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10298-152">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="10298-152">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="10298-153">Descripción de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="10298-153">Description of the account.</span></span>

<span data-ttu-id="10298-154">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10298-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10298-155">**Deshabilitada**</span><span class="sxs-lookup"><span data-stu-id="10298-155">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-156">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="10298-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10298-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10298-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10298-158">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| User \_ info \| fi \_ ACCOUNTDISABLE")</span><span class="sxs-lookup"><span data-stu-id="10298-158">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|USER\_INFO\|UF\_ACCOUNTDISABLE")</span></span>
</dt> </dl>

<span data-ttu-id="10298-159">La cuenta de usuario de Windows está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="10298-159">Windows user account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="10298-160">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="10298-160">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10298-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10298-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10298-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10298-163">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Functions \| domainname")</span><span class="sxs-lookup"><span data-stu-id="10298-163">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="10298-164">Nombre del dominio de Windows al que pertenece una cuenta de usuario, por ejemplo: "NA-SALES".</span><span class="sxs-lookup"><span data-stu-id="10298-164">Name of the Windows domain to which a user account belongs, for example: "NA-SALES".</span></span>

</dd> <dt>

<span data-ttu-id="10298-165">**FullName**</span><span class="sxs-lookup"><span data-stu-id="10298-165">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10298-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10298-167">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10298-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10298-168">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ Full \_ Name**")</span><span class="sxs-lookup"><span data-stu-id="10298-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**usri2\_full\_name**")</span></span>
</dt> </dl>

<span data-ttu-id="10298-169">Nombre completo de un usuario local, por ejemplo: "dan Wilson".</span><span class="sxs-lookup"><span data-stu-id="10298-169">Full name of a local user, for example: "Dan Wilson".</span></span>

</dd> <dt>

<span data-ttu-id="10298-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="10298-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-171">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10298-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10298-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10298-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10298-173">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="10298-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="10298-174">Fecha en que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="10298-174">Date the object is installed.</span></span> <span data-ttu-id="10298-175">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="10298-175">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="10298-176">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10298-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10298-177">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="10298-177">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-178">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="10298-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10298-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10298-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10298-180">Calificadores: [ **fijos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="10298-180">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="10298-181">Si es **true**, la cuenta se define en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="10298-181">If **true**, the account is defined on the local computer.</span></span>

<span data-ttu-id="10298-182">Esta propiedad se hereda de [**la \_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="10298-182">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="10298-183">**Bloqueo**</span><span class="sxs-lookup"><span data-stu-id="10298-183">**Lockout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-184">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="10298-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10298-185">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10298-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10298-186">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **up \_ bloqueos**")</span><span class="sxs-lookup"><span data-stu-id="10298-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_LOCKOUT**")</span></span>
</dt> </dl>

<span data-ttu-id="10298-187">Si es **true**, la cuenta de usuario está bloqueada en el sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="10298-187">If **true**, the user account is locked out of the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="10298-188">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="10298-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10298-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10298-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10298-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10298-191">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structure \| Name")</span><span class="sxs-lookup"><span data-stu-id="10298-191">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="10298-192">Nombre de la cuenta de usuario de Windows en el dominio que especifica la propiedad de **dominio** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="10298-192">Name of the Windows user account on the domain that the **Domain** property of this class specifies.</span></span>

<span data-ttu-id="10298-193">Ejemplo: "danwilson".</span><span class="sxs-lookup"><span data-stu-id="10298-193">Example: "danwilson".</span></span>

<span data-ttu-id="10298-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10298-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10298-195">**PasswordChangeable**</span><span class="sxs-lookup"><span data-stu-id="10298-195">**PasswordChangeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-196">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="10298-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10298-197">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10298-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10298-198">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**\_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **up \_ passwd \_ peralte \_ perchange**")</span><span class="sxs-lookup"><span data-stu-id="10298-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_CANT\_CHANGE**")</span></span>
</dt> </dl>

<span data-ttu-id="10298-199">Si **es true**, se puede cambiar la contraseña de esta cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="10298-199">If **true**, the password on this user account can be changed.</span></span>

</dd> <dt>

<span data-ttu-id="10298-200">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="10298-200">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-201">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="10298-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10298-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10298-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10298-203">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **up not \_ \_ expiren \_ passwd**")</span><span class="sxs-lookup"><span data-stu-id="10298-203">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_DONT\_EXPIRE\_PASSWD**")</span></span>
</dt> </dl>

<span data-ttu-id="10298-204">Si **es true**, la contraseña de esta cuenta de usuario expira.</span><span class="sxs-lookup"><span data-stu-id="10298-204">If **true**, the password on this user account expires.</span></span>

</dd> <dt>

<span data-ttu-id="10298-205">**PasswordRequired**</span><span class="sxs-lookup"><span data-stu-id="10298-205">**PasswordRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-206">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="10298-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10298-207">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10298-207">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10298-208">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**User \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **up \_ passwd \_ NOTREQD**")</span><span class="sxs-lookup"><span data-stu-id="10298-208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_NOTREQD**")</span></span>
</dt> </dl>

<span data-ttu-id="10298-209">Si es **true**, se requiere una contraseña en una cuenta de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="10298-209">If **true**, a password is required on a Windows user account.</span></span> <span data-ttu-id="10298-210">Si **es false**, esta cuenta no requiere una contraseña.</span><span class="sxs-lookup"><span data-stu-id="10298-210">If **false**, this account does not require a password.</span></span>

</dd> <dt>

<span data-ttu-id="10298-211">**SID**</span><span class="sxs-lookup"><span data-stu-id="10298-211">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-212">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10298-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10298-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10298-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10298-214">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| (identificadores de seguridad (SID)")</span><span class="sxs-lookup"><span data-stu-id="10298-214">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="10298-215">Identificador de seguridad (SID) para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="10298-215">Security identifier (SID) for this account.</span></span> <span data-ttu-id="10298-216">Un SID es un valor de cadena de longitud variable que se usa para identificar un administrador de confianza.</span><span class="sxs-lookup"><span data-stu-id="10298-216">A SID is a string value of variable length that is used to identify a trustee.</span></span> <span data-ttu-id="10298-217">Cada cuenta tiene un SID único que emite una autoridad, como un dominio de Windows.</span><span class="sxs-lookup"><span data-stu-id="10298-217">Each account has a unique SID that an authority, such as a Windows domain, issues.</span></span> <span data-ttu-id="10298-218">El SID se almacena en la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="10298-218">The SID is stored in the security database.</span></span> <span data-ttu-id="10298-219">Cuando un usuario inicia sesión, el sistema recupera el SID del usuario de la base de datos, coloca el SID en el token de acceso del usuario y, a continuación, usa el SID en el token de acceso del usuario para identificar al usuario en todas las interacciones posteriores con la seguridad de Windows.</span><span class="sxs-lookup"><span data-stu-id="10298-219">When a user logs on, the system retrieves the user SID from the database, places the SID in the user access token, and then uses the SID in the user access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="10298-220">Cada SID es un identificador único para un usuario o grupo, y otro usuario o grupo no puede tener el mismo SID.</span><span class="sxs-lookup"><span data-stu-id="10298-220">Each SID is a unique identifier for a user or group, and a different user or group cannot have the same SID.</span></span>

<span data-ttu-id="10298-221">Esta propiedad se hereda de [**la \_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="10298-221">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="10298-222">**SID**</span><span class="sxs-lookup"><span data-stu-id="10298-222">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-223">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="10298-223">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="10298-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10298-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10298-225">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Access Control tipos de enumeración \| [**\_ nombre SID \_ usar**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span><span class="sxs-lookup"><span data-stu-id="10298-225">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|[**SID\_NAME\_USE**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span></span>
</dt> </dl>

<span data-ttu-id="10298-226">Valor enumerado que especifica el tipo de SID.</span><span class="sxs-lookup"><span data-stu-id="10298-226">Enumerated value that specifies the type of SID.</span></span>

<span data-ttu-id="10298-227">Esta propiedad se hereda de [**la \_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="10298-227">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="10298-228">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="10298-228">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="10298-229">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="10298-229">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="10298-230">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="10298-230">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="10298-231">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="10298-231">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="10298-232">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="10298-232">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="10298-233">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="10298-233">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="10298-234">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="10298-234">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="10298-235">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="10298-235">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="10298-236">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="10298-236">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10298-237">**Estado**</span><span class="sxs-lookup"><span data-stu-id="10298-237">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10298-238">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10298-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10298-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10298-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10298-240">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="10298-240">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="10298-241">Estado actual de un objeto.</span><span class="sxs-lookup"><span data-stu-id="10298-241">Current status of an object.</span></span> <span data-ttu-id="10298-242">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="10298-242">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="10298-243">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL", que es un elemento como una unidad de disco duro habilitada para SMART que puede estar funcionando correctamente, pero predice un error en un futuro próximo.</span><span class="sxs-lookup"><span data-stu-id="10298-243">Operational statuses include: "OK", "Degraded", and "Pred Fail", which is an element such as a SMART-enabled hard disk drive that may be functioning properly, but predicts a failure in the near future.</span></span> <span data-ttu-id="10298-244">Los Estados no operativos incluyen: "error", "iniciando", "detención" y "servicio", que se puede aplicar durante la resilverización de reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="10298-244">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service", which can apply during mirror resilvering of a disk, reloading a user permissions list, or other administrative work.</span></span>

<span data-ttu-id="10298-245">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10298-245">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="10298-246">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="10298-246">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="10298-247">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="10298-247">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="10298-248">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="10298-248">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="10298-249">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="10298-249">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10298-250">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="10298-250">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="10298-251">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="10298-251">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="10298-252">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="10298-252">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="10298-253">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="10298-253">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="10298-254">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="10298-254">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="10298-255">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="10298-255">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="10298-256">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="10298-256">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="10298-257">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="10298-257">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="10298-258">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="10298-258">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="10298-259"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="10298-259"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="10298-260">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10298-260">Remarks</span></span>

<span data-ttu-id="10298-261">La clase **Win32 \_ cuentadeusuario** se deriva de la [**\_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="10298-261">The **Win32\_UserAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

> [!Note]  
> <span data-ttu-id="10298-262">No se devuelve un error para un intento de escribir en una propiedad de solo lectura, y el valor de la propiedad permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="10298-262">An error is not returned for an attempt to write to a read-only property, and the value of the property remains unchanged.</span></span>

 

## <a name="examples"></a><span data-ttu-id="10298-263">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="10298-263">Examples</span></span>

<span data-ttu-id="10298-264">El ejemplo de la [lista de cuentas de usuario locales que usan](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) código de VBScript de WMI en la galería de TechNet usa **Win32 \_ cuentadeusuario** para devolver información acerca de las cuentas de usuario local que se encuentran en un equipo.</span><span class="sxs-lookup"><span data-stu-id="10298-264">The [List Local User Accounts Using WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript code sample on TechNet Gallery uses **Win32\_UserAccount** to Returns information about the local user accounts found on a computer.</span></span>

<span data-ttu-id="10298-265">[Convertir el SID en la cuenta de usuario y la cuenta de usuario en SID](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) El ejemplo de código de PowerShell en la galería de TechNet usa **Win32 \_ cuentadeusuario** para traducir un SID a una cuenta de usuario o una cuenta de usuario a Sid.</span><span class="sxs-lookup"><span data-stu-id="10298-265">[The Translate SID to User Account and User Account to SID](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) PowerShell code sample on TechNet Gallery uses **Win32\_UserAccount** to translate a SID to User Account and/or a User Account to SID.</span></span>

<span data-ttu-id="10298-266">En el ejemplo de código de VBScript siguiente se muestra cómo obtener el nombre completo de un usuario en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="10298-266">The following VBScript code example shows you how to get the full name of a user on a local computer.</span></span> <span data-ttu-id="10298-267">El nombre completo es el nombre de idioma, por ejemplo, una persona puede tener el nombre de usuario "kensanchez" y el nombre completo puede ser "Ken Sánchez", por lo que debe sustituir el nombre de dominio real y el nombre de usuario de "MyDomainName" y "nombre de usuario".</span><span class="sxs-lookup"><span data-stu-id="10298-267">The full name is the human language name, for example, a person may have the user name of "kensanchez" and the full name may be "Ken Sanchez", so you substitute the real domain name and user name for "MyDomainName" and "MyUserName".</span></span> <span data-ttu-id="10298-268">Para una consulta eficaz, debe especificar las propiedades de dominio y nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="10298-268">For an efficient query, you must specify both the domain and user name properties.</span></span>

<span data-ttu-id="10298-269">Si es administrador de un equipo remoto, puede asignar el nombre del equipo remoto para strComputer (en lugar de ".") y, a continuación, usar el siguiente tipo de script para obtener el nombre completo de una cuenta de usuario en un equipo local, desde un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="10298-269">If you are an administrator on a remote computer, you can assign the name of the remote computer for strComputer (instead of "."), and then use the following type of script to get the full name of a user account on a local computer—from a remote computer.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="10298-270">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10298-270">Requirements</span></span>



| <span data-ttu-id="10298-271">Requisito</span><span class="sxs-lookup"><span data-stu-id="10298-271">Requirement</span></span> | <span data-ttu-id="10298-272">Value</span><span class="sxs-lookup"><span data-stu-id="10298-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10298-273">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10298-273">Minimum supported client</span></span><br/> | <span data-ttu-id="10298-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10298-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10298-275">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10298-275">Minimum supported server</span></span><br/> | <span data-ttu-id="10298-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10298-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10298-277">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="10298-277">Namespace</span></span><br/>                | <span data-ttu-id="10298-278">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="10298-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10298-279">MOF</span><span class="sxs-lookup"><span data-stu-id="10298-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10298-280"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10298-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10298-281">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="10298-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10298-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10298-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10298-283">Vea también</span><span class="sxs-lookup"><span data-stu-id="10298-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10298-284">**\_Cuenta Win32**</span><span class="sxs-lookup"><span data-stu-id="10298-284">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="10298-285">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="10298-285">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
