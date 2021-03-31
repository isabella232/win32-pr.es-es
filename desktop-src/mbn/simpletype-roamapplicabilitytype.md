---
description: RoamApplicabilityType describe las condiciones de itinerancia para las que se aplica un perfil móvil.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simple de roamApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d81214ab5a44dcac60bb5e1a6accc81b0d0418
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907918"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span data-ttu-id="b0b6e-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Tipo simple de roamApplicabilityType</span><span class="sxs-lookup"><span data-stu-id="b0b6e-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>roamApplicabilityType Simple Type</span></span>

<span data-ttu-id="b0b6e-104">RoamApplicabilityType describe las condiciones de itinerancia para las que se aplica un perfil móvil.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-104">The roamApplicabilityType describes the roaming conditions for which a roaming profile applies.</span></span>

<span data-ttu-id="b0b6e-105">Este atributo es más expresivo que [**roamControlType**](simpletype-roamcontroltype.md)y un perfil debe utilizar **roamControlType** o **roamApplicabilityType**, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-105">This is a more expressive attribute than [**roamControlType**](simpletype-roamcontroltype.md), and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="b0b6e-106">(Si un perfil usa ambos, se aplican ambos.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-106">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="b0b6e-107">El resultado es la intersección de los dos.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-107">The result is the intersection of the two.)</span></span>

<span data-ttu-id="b0b6e-108">Use este atributo para diferenciar entre varios perfiles con condiciones de itinerancia no contiguas, para especificar atributos de perfil diferentes para, por ejemplo, Inicio o itinerancia.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-108">Use this attribute to differentiate between multiple profiles with disjoint roaming conditions, to specify different profile attributes for, for example, home versus roaming.</span></span>

<span data-ttu-id="b0b6e-109">Hay tres Estados posibles de registro en casa/móvil:</span><span class="sxs-lookup"><span data-stu-id="b0b6e-109">There are three possible home/roam registration states:</span></span>

-   <span data-ttu-id="b0b6e-110">Inicio: registrado en la red doméstica</span><span class="sxs-lookup"><span data-stu-id="b0b6e-110">Home: registered on the home network</span></span>
-   <span data-ttu-id="b0b6e-111">Asociado: registrado en una red estrechamente ligada a la red doméstica</span><span class="sxs-lookup"><span data-stu-id="b0b6e-111">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="b0b6e-112">No asociado: registrado en una red que no está estrechamente asociada con la red doméstica</span><span class="sxs-lookup"><span data-stu-id="b0b6e-112">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="b0b6e-113">El significado preciso de "asociado" varía en función de la red, pero representa una relación más estrecha con las tarifas más favorables que un no asociado.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-113">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="b0b6e-114">Este podría ser el caso si un operador basado en regiones tiene un acuerdo empresarial para usar la red de acceso de radio de otro operador fuera de su área principal.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-114">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="b0b6e-115">También podría representar la diferencia entre la itinerancia dentro de una región (por ejemplo, la Unión Europea) y fuera de ella.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-115">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

``` syntax
<xs:simpleType name="roamApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="NonPartnerOnly"
         />
        <xs:enumeration
            value="PartnerOnly"
         />
        <xs:enumeration
            value="HomeOnly"
         />
        <xs:enumeration
            value="HomeAndPartner"
         />
        <xs:enumeration
            value="PartnerAndNonpartner"
         />
        <xs:enumeration
            value="AllRoaming"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="b0b6e-116">Valores de enumeración</span><span class="sxs-lookup"><span data-stu-id="b0b6e-116">Enumeration values</span></span>

<span data-ttu-id="b0b6e-117">El tipo simple **roamApplicabilityType** define los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-117">The **roamApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0b6e-118">Value</span><span class="sxs-lookup"><span data-stu-id="b0b6e-118">Value</span></span></th>
<th><span data-ttu-id="b0b6e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0b6e-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b0b6e-120">NonPartnerOnly</span><span class="sxs-lookup"><span data-stu-id="b0b6e-120">NonPartnerOnly</span></span></td>
<td><p><span data-ttu-id="b0b6e-121">Este perfil solo se utiliza cuando se usa la itinerancia en una red no asociada.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-121">This profile is used only when roaming on a non-partner network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0b6e-122">PartnerOnly</span><span class="sxs-lookup"><span data-stu-id="b0b6e-122">PartnerOnly</span></span></td>
<td><p><span data-ttu-id="b0b6e-123">Este perfil solo se utiliza cuando se usa la itinerancia en una red de asociados</span><span class="sxs-lookup"><span data-stu-id="b0b6e-123">This profile is used only when roaming on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0b6e-124">HomeOnly</span><span class="sxs-lookup"><span data-stu-id="b0b6e-124">HomeOnly</span></span></td>
<td><p><span data-ttu-id="b0b6e-125">Este perfil solo se usa cuando se está en la red doméstica.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-125">This profile is used only when on the home network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0b6e-126">HomeAndPartner</span><span class="sxs-lookup"><span data-stu-id="b0b6e-126">HomeAndPartner</span></span></td>
<td><p><span data-ttu-id="b0b6e-127">Este perfil se usa solo cuando está en casa o en una red de asociados.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-127">This profile is used only when at home or on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0b6e-128">PartnerAndNonpartner</span><span class="sxs-lookup"><span data-stu-id="b0b6e-128">PartnerAndNonpartner</span></span></td>
<td><p><span data-ttu-id="b0b6e-129">Este perfil se usa cuando no está en casa (itinerancia en cualquier red)</span><span class="sxs-lookup"><span data-stu-id="b0b6e-129">This profile is used when not at home (roaming on any network)</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0b6e-130">AllRoaming</span><span class="sxs-lookup"><span data-stu-id="b0b6e-130">AllRoaming</span></span></td>
<td><p><span data-ttu-id="b0b6e-131">Este perfil se usa en todas las redes</span><span class="sxs-lookup"><span data-stu-id="b0b6e-131">This profile is used on all networks</span></span></p></td>
</tr>
</tbody>
</table>

 

 



