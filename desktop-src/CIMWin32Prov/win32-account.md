---
description: Contiene información acerca de las cuentas de usuario y las cuentas de grupo que conoce el equipo que ejecuta Windows.
ms.assetid: c0916f20-05be-4282-9642-28cec606bfd7
ms.tgt_platform: multiple
title: Win32_Account (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Account
- Win32_Account.Caption
- Win32_Account.Description
- Win32_Account.Domain
- Win32_Account.InstallDate
- Win32_Account.LocalAccount
- Win32_Account.Name
- Win32_Account.SID
- Win32_Account.SIDType
- Win32_Account.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2af601799095192d7af4ffedce0c8e0cd28bff21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153434"
---
# <a name="win32_account-class"></a><span data-ttu-id="ece6b-103">Win32 ( \_ clase de cuenta)</span><span class="sxs-lookup"><span data-stu-id="ece6b-103">Win32\_Account class</span></span>

<span data-ttu-id="ece6b-104">La [clase de WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstracta de la **\_ cuenta de Win32** contiene información acerca de las cuentas de usuario y las cuentas de grupo que conoce el equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="ece6b-104">The **Win32\_Account** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) contains information about user accounts and group accounts known to the computer system running Windows.</span></span> <span data-ttu-id="ece6b-105">Los nombres de usuario o grupo reconocidos por un dominio de Windows son descendientes (o miembros) de esta clase.</span><span class="sxs-lookup"><span data-stu-id="ece6b-105">User or group names recognized by a Windows domain are descendants (or members) of this class.</span></span>

<span data-ttu-id="ece6b-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ece6b-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ece6b-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ece6b-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ece6b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ece6b-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4C9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Account : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   Domain;
  datetime InstallDate;
  boolean  LocalAccount;
  string   Name;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="ece6b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ece6b-109">Members</span></span>

<span data-ttu-id="ece6b-110">La clase de **\_ cuenta de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ece6b-110">The **Win32\_Account** class has these types of members:</span></span>

-   [<span data-ttu-id="ece6b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ece6b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ece6b-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ece6b-112">Properties</span></span>

<span data-ttu-id="ece6b-113">La clase de **\_ cuenta de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ece6b-113">The **Win32\_Account** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ece6b-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ece6b-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece6b-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ece6b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ece6b-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ece6b-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ece6b-118">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ece6b-118">Short description of the object.</span></span>

<span data-ttu-id="ece6b-119">Esta propiedad se hereda de la clase del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="ece6b-119">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ece6b-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ece6b-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece6b-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ece6b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ece6b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-123">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="ece6b-123">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ece6b-124">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ece6b-124">Description of the object.</span></span>

<span data-ttu-id="ece6b-125">Esta propiedad se hereda de la clase del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="ece6b-125">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ece6b-126">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="ece6b-126">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece6b-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ece6b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ece6b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-129">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("dominio de funciones de administración de red de inesperados win32api \| \| ")</span><span class="sxs-lookup"><span data-stu-id="ece6b-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="ece6b-130">Nombre del dominio de Windows al que pertenece un grupo o usuario.</span><span class="sxs-lookup"><span data-stu-id="ece6b-130">Name of the Windows domain to which a group or user belongs.</span></span>

<span data-ttu-id="ece6b-131">Ejemplo: "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="ece6b-131">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="ece6b-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ece6b-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece6b-133">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ece6b-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ece6b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-135">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="ece6b-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ece6b-136">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="ece6b-136">Date and time that the object was installed.</span></span> <span data-ttu-id="ece6b-137">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="ece6b-137">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ece6b-138">Esta propiedad se hereda de la clase del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="ece6b-138">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ece6b-139">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="ece6b-139">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece6b-140">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ece6b-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ece6b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-142">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ece6b-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ece6b-143">Si es **true**, la cuenta se define en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="ece6b-143">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="ece6b-144">Para recuperar solo las cuentas definidas en el equipo local, diseñe una consulta que incluya la condición "LocalAccount =**true**".</span><span class="sxs-lookup"><span data-stu-id="ece6b-144">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

</dd> <dt>

<span data-ttu-id="ece6b-145">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ece6b-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece6b-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ece6b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ece6b-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-148">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de estructuras de administración de red de inesperados win32api \| \| ")</span><span class="sxs-lookup"><span data-stu-id="ece6b-148">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="ece6b-149">Nombre de la cuenta del sistema de Windows en el dominio especificado por la propiedad de **dominio** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="ece6b-149">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span> <span data-ttu-id="ece6b-150">Esta propiedad invalida la propiedad de **nombre** heredada de [**un \_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ece6b-150">This property overrides the **Name** property inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ece6b-151">**SID**</span><span class="sxs-lookup"><span data-stu-id="ece6b-151">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece6b-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ece6b-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ece6b-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-154">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| (identificadores de seguridad (SID)")</span><span class="sxs-lookup"><span data-stu-id="ece6b-154">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="ece6b-155">Identificador de seguridad (SID) para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="ece6b-155">Security identifier (SID) for this account.</span></span> <span data-ttu-id="ece6b-156">Un SID es un valor de cadena de longitud variable que se usa para identificar un administrador de confianza.</span><span class="sxs-lookup"><span data-stu-id="ece6b-156">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="ece6b-157">Cada cuenta tiene un SID único emitido por una autoridad (como un dominio de Windows), almacenado en una base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ece6b-157">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="ece6b-158">Cuando un usuario inicia sesión, el sistema recupera el SID del usuario de la base de datos y lo coloca en el token de acceso del usuario.</span><span class="sxs-lookup"><span data-stu-id="ece6b-158">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="ece6b-159">El sistema utiliza el SID en el token de acceso del usuario para identificar al usuario en todas las interacciones posteriores con la seguridad de Windows.</span><span class="sxs-lookup"><span data-stu-id="ece6b-159">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="ece6b-160">Cuando se ha usado un SID como identificador único para un usuario o grupo, no se puede volver a usar para identificar a otro usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="ece6b-160">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

</dd> <dt>

<span data-ttu-id="ece6b-161">**SID**</span><span class="sxs-lookup"><span data-stu-id="ece6b-161">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece6b-162">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ece6b-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ece6b-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-164">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Access Control tipos de enumeración \| \_ nombre SID \_ usar")</span><span class="sxs-lookup"><span data-stu-id="ece6b-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="ece6b-165">Valores enumerados que especifican el tipo de identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="ece6b-165">Enumerated values that specify the type of security identifier (SID).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="ece6b-166">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="ece6b-166">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="ece6b-167">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="ece6b-167">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="ece6b-168">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="ece6b-168">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="ece6b-169">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="ece6b-169">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="ece6b-170">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="ece6b-170">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="ece6b-171">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="ece6b-171">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="ece6b-172">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="ece6b-172">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="ece6b-173">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="ece6b-173">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="ece6b-174">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="ece6b-174">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ece6b-175">**Estado**</span><span class="sxs-lookup"><span data-stu-id="ece6b-175">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece6b-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ece6b-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ece6b-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ece6b-178">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ece6b-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ece6b-179">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="ece6b-179">Current status of the object.</span></span> <span data-ttu-id="ece6b-180">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="ece6b-180">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ece6b-181">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero predice un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="ece6b-181">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicts a failure in the near future).</span></span> <span data-ttu-id="ece6b-182">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="ece6b-182">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ece6b-183">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="ece6b-183">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ece6b-184">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="ece6b-184">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ece6b-185">Esta propiedad se hereda de la clase del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="ece6b-185">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

<span data-ttu-id="ece6b-186">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="ece6b-186">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ece6b-187">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="ece6b-187">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ece6b-188">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="ece6b-188">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ece6b-189">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="ece6b-189">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ece6b-190">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="ece6b-190">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ece6b-191">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="ece6b-191">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ece6b-192">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="ece6b-192">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ece6b-193">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="ece6b-193">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ece6b-194">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="ece6b-194">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ece6b-195">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="ece6b-195">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ece6b-196">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="ece6b-196">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ece6b-197">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="ece6b-197">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ece6b-198">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="ece6b-198">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="ece6b-199"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ece6b-199"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ece6b-200">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ece6b-200">Remarks</span></span>

<span data-ttu-id="ece6b-201">La clase de **\_ cuenta de Win32** se deriva de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ece6b-201">The **Win32\_Account** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ece6b-202">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ece6b-202">Examples</span></span>

<span data-ttu-id="ece6b-203">El siguiente código de PowerShell recupera las cuentas locales.</span><span class="sxs-lookup"><span data-stu-id="ece6b-203">The following PowerShell code retrieves the local accounts.</span></span>


```PowerShell
Get-WmiObject Win32_Account -Filter "Domain='$Env:ComputerName'"
```



<span data-ttu-id="ece6b-204">El siguiente código de PowerShell recupera las cuentas de dominio.</span><span class="sxs-lookup"><span data-stu-id="ece6b-204">The following PowerShell code retrieves the domain accounts.</span></span>


```PowerShell
 Get-WmiObject Win32_Account -Filter "Domain='$Env:UserDomain'" 
```



## <a name="requirements"></a><span data-ttu-id="ece6b-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ece6b-205">Requirements</span></span>



| <span data-ttu-id="ece6b-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="ece6b-206">Requirement</span></span> | <span data-ttu-id="ece6b-207">Value</span><span class="sxs-lookup"><span data-stu-id="ece6b-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece6b-208">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ece6b-208">Minimum supported client</span></span><br/> | <span data-ttu-id="ece6b-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ece6b-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ece6b-210">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ece6b-210">Minimum supported server</span></span><br/> | <span data-ttu-id="ece6b-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ece6b-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ece6b-212">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ece6b-212">Namespace</span></span><br/>                | <span data-ttu-id="ece6b-213">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ece6b-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ece6b-214">MOF</span><span class="sxs-lookup"><span data-stu-id="ece6b-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ece6b-215"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ece6b-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ece6b-216">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ece6b-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ece6b-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ece6b-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ece6b-218">Vea también</span><span class="sxs-lookup"><span data-stu-id="ece6b-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece6b-219">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ece6b-219">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="ece6b-220">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ece6b-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

