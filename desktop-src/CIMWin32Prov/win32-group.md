---
description: Representa los datos de una cuenta de grupo.
ms.assetid: a53d1276-3dc9-419a-bbb8-5dd07794a971
ms.tgt_platform: multiple
title: Win32_Group (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group
- Win32_Group.Caption
- Win32_Group.Description
- Win32_Group.InstallDate
- Win32_Group.Status
- Win32_Group.LocalAccount
- Win32_Group.SID
- Win32_Group.SIDType
- Win32_Group.Domain
- Win32_Group.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8849ba149e0de570150682d3afbad3a4ee33f36
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153352"
---
# <a name="win32_group-class"></a><span data-ttu-id="b3c7f-103">Clase de grupo de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="b3c7f-103">Win32\_Group class</span></span>

<span data-ttu-id="b3c7f-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ Grupo Win32** representa datos sobre una cuenta de grupo.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-104">The **Win32\_Group** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents data about a group account.</span></span> <span data-ttu-id="b3c7f-105">Una cuenta de grupo permite cambiar los privilegios de acceso para una lista de usuarios.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-105">A group account allows access privileges to be changed for a list of users.</span></span> <span data-ttu-id="b3c7f-106">Ejemplo: Marketing2.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-106">Example: Marketing2.</span></span>

<span data-ttu-id="b3c7f-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b3c7f-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c7f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3c7f-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Group : Win32_Account
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

## <a name="members"></a><span data-ttu-id="b3c7f-110">Members</span><span class="sxs-lookup"><span data-stu-id="b3c7f-110">Members</span></span>

<span data-ttu-id="b3c7f-111">La clase de **\_ Grupo Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b3c7f-111">The **Win32\_Group** class has these types of members:</span></span>

-   [<span data-ttu-id="b3c7f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b3c7f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b3c7f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b3c7f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b3c7f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b3c7f-114">Methods</span></span>

<span data-ttu-id="b3c7f-115">La clase de **\_ Grupo Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-115">The **Win32\_Group** class has these methods.</span></span>



| <span data-ttu-id="b3c7f-116">Método</span><span class="sxs-lookup"><span data-stu-id="b3c7f-116">Method</span></span>                                               | <span data-ttu-id="b3c7f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3c7f-117">Description</span></span>                        |
|:-----------------------------------------------------|:-----------------------------------|
| [<span data-ttu-id="b3c7f-118">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-118">**Rename**</span></span>](rename-method-in-class-win32-group.md) | <span data-ttu-id="b3c7f-119">Cambia el nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-119">Changes the group name.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b3c7f-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b3c7f-120">Properties</span></span>

<span data-ttu-id="b3c7f-121">La clase de **\_ Grupo Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-121">The **Win32\_Group** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3c7f-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c7f-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c7f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-125">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b3c7f-126">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-126">A short textual description of the object.</span></span>

<span data-ttu-id="b3c7f-127">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3c7f-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3c7f-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c7f-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c7f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-131">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b3c7f-132">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-132">A textual description of the object.</span></span>

<span data-ttu-id="b3c7f-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3c7f-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3c7f-134">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-134">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c7f-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c7f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-137">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Network Management Functions \| domainname")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-137">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="b3c7f-138">Nombre del dominio de Windows al que pertenece la cuenta de grupo.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-138">Name of the Windows domain to which the group account belongs.</span></span>

<span data-ttu-id="b3c7f-139">Ejemplo: "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="b3c7f-139">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="b3c7f-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c7f-141">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c7f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-143">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b3c7f-144">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-144">Indicates when the object was installed.</span></span> <span data-ttu-id="b3c7f-145">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-145">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b3c7f-146">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3c7f-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3c7f-147">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-147">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c7f-148">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c7f-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-150">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b3c7f-150">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b3c7f-151">Si es **true**, la cuenta se define en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-151">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="b3c7f-152">Para recuperar solo las cuentas definidas en el equipo local, diseñe una consulta que incluya la condición "LocalAccount =**true**".</span><span class="sxs-lookup"><span data-stu-id="b3c7f-152">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="b3c7f-153">Esta propiedad se hereda de [**la \_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="b3c7f-153">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3c7f-154">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c7f-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c7f-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-157">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Network Management Structure \| Name")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="b3c7f-158">Nombre de la cuenta de grupo de Windows en el dominio especificado por la propiedad de **dominio** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-158">Name of the Windows group account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="b3c7f-159">**SID**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-159">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c7f-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c7f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-162">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| (identificadores de seguridad (SID)")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-162">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="b3c7f-163">Identificador de seguridad (SID) para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-163">Security identifier (SID) for this account.</span></span> <span data-ttu-id="b3c7f-164">Un SID es un valor de cadena de longitud variable que se usa para identificar un administrador de confianza.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-164">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="b3c7f-165">Cada cuenta tiene un SID único emitido por una autoridad (como un dominio de Windows), almacenado en una base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-165">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="b3c7f-166">Cuando un usuario inicia sesión, el sistema recupera el SID del usuario de la base de datos y lo coloca en el token de acceso del usuario.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-166">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="b3c7f-167">El sistema utiliza el SID en el token de acceso del usuario para identificar al usuario en todas las interacciones posteriores con la seguridad de Windows.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-167">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="b3c7f-168">Cuando se ha usado un SID como identificador único para un usuario o grupo, no se puede volver a usar para identificar a otro usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-168">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="b3c7f-169">Esta propiedad se hereda de [**la \_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="b3c7f-169">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3c7f-170">**SID**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-170">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c7f-171">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c7f-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-173">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Access Control tipos de enumeración \| \_ nombre SID \_ usar")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-173">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="b3c7f-174">Valores enumerados que especifican el tipo de identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="b3c7f-174">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="b3c7f-175">Esta propiedad se hereda de [**la \_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="b3c7f-175">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="b3c7f-176">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="b3c7f-176">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="b3c7f-177">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="b3c7f-177">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="b3c7f-178">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="b3c7f-178">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="b3c7f-179">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="b3c7f-179">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="b3c7f-180">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="b3c7f-180">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="b3c7f-181">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="b3c7f-181">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="b3c7f-182">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="b3c7f-182">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="b3c7f-183">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="b3c7f-183">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="b3c7f-184">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="b3c7f-184">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b3c7f-185">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-185">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c7f-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3c7f-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c7f-188">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b3c7f-189">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-189">String that indicates the current status of the object.</span></span> <span data-ttu-id="b3c7f-190">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-190">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b3c7f-191">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="b3c7f-191">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b3c7f-192">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="b3c7f-192">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b3c7f-193">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="b3c7f-193">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b3c7f-194">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-194">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b3c7f-195">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-195">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b3c7f-196">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3c7f-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b3c7f-197">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b3c7f-197">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b3c7f-198">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-198">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b3c7f-199">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-199">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b3c7f-200">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-200">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b3c7f-201">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-201">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b3c7f-202">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-202">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b3c7f-203">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-203">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b3c7f-204">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-204">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b3c7f-205">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-205">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b3c7f-206">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-206">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b3c7f-207">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-207">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b3c7f-208">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-208">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b3c7f-209">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="b3c7f-209">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b3c7f-210"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b3c7f-210"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b3c7f-211">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3c7f-211">Remarks</span></span>

<span data-ttu-id="b3c7f-212">La clase de **\_ grupo de Win32** se deriva de la [**\_ cuenta de Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="b3c7f-212">The **Win32\_Group** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b3c7f-213">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b3c7f-213">Examples</span></span>

<span data-ttu-id="b3c7f-214">El código siguiente, tomado del ejemplo de [lista de grupos locales que usan](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) el código VBScript de WMI en la galería de TechNet, usa el **\_ Grupo Win32** para devolver información acerca de los grupos locales encontrados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="b3c7f-214">The following code, taken from the [List Local Groups Using WMI](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) VBScript code example on TechNet Gallery, uses **Win32\_Group** to return information about the local groups found on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_Group  Where LocalAccount = True") 
 
For Each objItem in colItems 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Domain: " & objItem.Domain 
    Wscript.Echo "Local Account: " & objItem.LocalAccount 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "SID: " & objItem.SID 
    Wscript.Echo "SID Type: " & objItem.SIDType 
    Wscript.Echo "Status: " & objItem.Status 
    Wscript.Echo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="b3c7f-215">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3c7f-215">Requirements</span></span>



| <span data-ttu-id="b3c7f-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c7f-216">Requirement</span></span> | <span data-ttu-id="b3c7f-217">Value</span><span class="sxs-lookup"><span data-stu-id="b3c7f-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c7f-218">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3c7f-218">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c7f-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3c7f-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3c7f-220">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3c7f-220">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c7f-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3c7f-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3c7f-222">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b3c7f-222">Namespace</span></span><br/>                | <span data-ttu-id="b3c7f-223">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b3c7f-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b3c7f-224">MOF</span><span class="sxs-lookup"><span data-stu-id="b3c7f-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3c7f-225"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3c7f-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3c7f-226">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3c7f-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3c7f-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3c7f-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c7f-228">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b3c7f-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c7f-229">**\_Cuenta Win32**</span><span class="sxs-lookup"><span data-stu-id="b3c7f-229">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

<span data-ttu-id="b3c7f-230">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b3c7f-230">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

