---
description: Describe un conjunto de clases con las propiedades y los métodos necesarios para administrar una entidad del mundo real o para admitir un escenario de uso, de manera interoperable.
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Msvm_RegisteredProfile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a7014687355524fbe10ff01869cac6c3fd35a894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082717"
---
# <a name="msvm_registeredprofile-class"></a><span data-ttu-id="b7d2a-103">MSVM \_ RegisteredProfile (clase)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-103">Msvm\_RegisteredProfile class</span></span>

<span data-ttu-id="b7d2a-104">Describe un conjunto de clases con las propiedades y los métodos necesarios para administrar una entidad del mundo real o para admitir un escenario de uso, de manera interoperable.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-104">Describes a set of classes with required properties and methods, necessary to manage a real-world entity or to support a usage scenario, in an interoperable fashion.</span></span>

<span data-ttu-id="b7d2a-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d2a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7d2a-106">Syntax</span></span>

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="b7d2a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7d2a-107">Members</span></span>

<span data-ttu-id="b7d2a-108">La clase **MSVM \_ RegisteredProfile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b7d2a-108">The **Msvm\_RegisteredProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="b7d2a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7d2a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7d2a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7d2a-110">Properties</span></span>

<span data-ttu-id="b7d2a-111">La clase **MSVM \_ RegisteredProfile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-111">The **Msvm\_RegisteredProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7d2a-112">**AdvertiseTypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-112">**AdvertiseTypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d2a-113">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d2a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7d2a-115">Matriz de cadenas que proporciona información adicional relacionada con la propiedad **AdvertiseType** .</span><span class="sxs-lookup"><span data-stu-id="b7d2a-115">An array of strings that provides additional information related to the **AdvertiseType** property.</span></span> <span data-ttu-id="b7d2a-116">Se debe proporcionar una descripción cuando el **AdvertiseType** es 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-116">A description must be provided when the **AdvertiseType** is 1 (Other).</span></span> <span data-ttu-id="b7d2a-117">Una entrada de esta matriz se corresponde con el mismo índice de la matriz **AdvertiseTypes** .</span><span class="sxs-lookup"><span data-stu-id="b7d2a-117">An entry in this array corresponds to the same index in the **AdvertiseTypes** array.</span></span> <span data-ttu-id="b7d2a-118">Esta propiedad se hereda de [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-118">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b7d2a-119">**AdvertiseTypes**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-119">**AdvertiseTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d2a-120">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d2a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7d2a-122">Especifica el anuncio para la información de perfil.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-122">Specifies the advertisement for the profile information.</span></span> <span data-ttu-id="b7d2a-123">Los servicios de publicidad de la infraestructura de WBEM lo usan para determinar lo que se debe anunciar, a través de los mecanismos.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-123">It is used by the advertising services of the WBEM infrastructure to determine what should be advertised, through what mechanisms.</span></span> <span data-ttu-id="b7d2a-124">La propiedad es una matriz para que el perfil se pueda anunciar usando varios mecanismos.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-124">The property is an array so that the profile can be advertised using several mechanisms.</span></span> <span data-ttu-id="b7d2a-125">Si esta propiedad es **null**, equivale a especificar el valor 2 (no anunciado).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-125">If this property is **Null**, this is equivalent to specifying the value 2 (Not Advertised).</span></span> <span data-ttu-id="b7d2a-126">Esta propiedad se hereda de [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-126">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b7d2a-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**No anunciado** (2)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Not Advertised** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b7d2a-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d2a-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d2a-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7d2a-133">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-133">A short description of the object.</span></span> <span data-ttu-id="b7d2a-134">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7d2a-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d2a-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d2a-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7d2a-138">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-138">A description of the object.</span></span> <span data-ttu-id="b7d2a-139">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7d2a-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d2a-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d2a-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7d2a-143">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-143">A display name for the object.</span></span> <span data-ttu-id="b7d2a-144">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7d2a-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d2a-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d2a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-148">Calificadores: **clave**, **invalidación**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-148">Qualifiers: **Key**, **Override**</span></span>
</dt> </dl>

<span data-ttu-id="b7d2a-149">Cadena que identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-149">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b7d2a-150">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7d2a-151">**OtherRegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-151">**OtherRegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d2a-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d2a-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-154">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-154">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="b7d2a-155">Una cadena que proporciona una descripción de la organización cuando **RegisteredOrganization** contiene 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-155">A string that provides a description of the organization when **RegisteredOrganization** contains 1 (Other).</span></span> <span data-ttu-id="b7d2a-156">Esta propiedad se hereda de [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-156">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b7d2a-157">**RegisteredName**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-157">**RegisteredName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d2a-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d2a-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-160">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-160">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="b7d2a-161">Nombre de este perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-161">The name of this registered profile.</span></span> <span data-ttu-id="b7d2a-162">Puesto que pueden existir varias versiones para el mismo **RegisteredName**, la combinación de **RegisteredName**, **RegisteredOrganization** y **RegisteredVersion** debe identificar de forma única el perfil registrado en el ámbito de la organización.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-162">Since multiple versions can exist for the same **RegisteredName**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="b7d2a-163">Esta propiedad se hereda de [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-163">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b7d2a-164">**RegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-164">**RegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d2a-165">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d2a-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7d2a-167">La organización que define este perfil.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-167">The organization that defines this profile.</span></span> <span data-ttu-id="b7d2a-168">Esta propiedad se hereda de [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-168">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b7d2a-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consorcio for Service Innovation** (4)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consortium for Service Innovation** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-173"><span id="FAST"></span><span id="fast"></span>**Rápido** (5)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-173"><span id="FAST"></span><span id="fast"></span>**FAST** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-174"><span id="GGF"></span><span id="ggf"></span>**GGF** (6)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-174"><span id="GGF"></span><span id="ggf"></span>**GGF** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-175"><span id="INTAP"></span><span id="intap"></span>**INTAP** (7)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-175"><span id="INTAP"></span><span id="intap"></span>**INTAP** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10 noroeste de eficacia energética** (10)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10 Northwest Energy Efficiency Alliance** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**Foro de TM** (12)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**TM Forum** (12)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**Grupo abierto** (13)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**The Open Group** (13)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**//20 OGF** (20)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**//20 OGF** (20)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**La cuadrícula verde** (21)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**The Green Grid** (21)</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="b7d2a-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="b7d2a-191">)</span><span class="sxs-lookup"><span data-stu-id="b7d2a-191">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b7d2a-192">**RegisteredVersion**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-192">**RegisteredVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d2a-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d2a-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d2a-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d2a-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7d2a-195">Versión de este perfil.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-195">The version of this profile.</span></span> <span data-ttu-id="b7d2a-196">La cadena debe tener el formato: "*M*. *N*. *U*"Dónde:</span><span class="sxs-lookup"><span data-stu-id="b7d2a-196">The string must be in the form: "*M*.*N*.*U*" Where:</span></span>

-   <span data-ttu-id="b7d2a-197">*M* es la versión principal (en formato numérico) que describe la creación o última modificación del perfil.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-197">*M* is the major version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="b7d2a-198">*N* es la versión secundaria (en formato numérico) que describe la creación o la última modificación del perfil.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-198">*N* is the minor version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="b7d2a-199">*U* es la actualización (en formato numérico) que describe la creación o última modificación del perfil.</span><span class="sxs-lookup"><span data-stu-id="b7d2a-199">*U* is the update (in numeric form) describing the profile's creation or last modification.</span></span>

<span data-ttu-id="b7d2a-200">Esta propiedad se hereda de [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7d2a-200">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7d2a-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7d2a-201">Requirements</span></span>



| <span data-ttu-id="b7d2a-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7d2a-202">Requirement</span></span> | <span data-ttu-id="b7d2a-203">Value</span><span class="sxs-lookup"><span data-stu-id="b7d2a-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d2a-204">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7d2a-204">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d2a-205">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b7d2a-205">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b7d2a-206">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7d2a-206">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d2a-207">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7d2a-207">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b7d2a-208">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b7d2a-208">Namespace</span></span><br/>                | <span data-ttu-id="b7d2a-209">\\Interoperabilidad raíz</span><span class="sxs-lookup"><span data-stu-id="b7d2a-209">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="b7d2a-210">MOF</span><span class="sxs-lookup"><span data-stu-id="b7d2a-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7d2a-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7d2a-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7d2a-212">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7d2a-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7d2a-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7d2a-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

