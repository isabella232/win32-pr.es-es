---
description: Describe cómo el perfil controla la itinerancia.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simple de roamControlType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911e379773e7d8eabfb7a1524b1a21ba16718a53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705713"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span data-ttu-id="575f0-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>Tipo simple de roamControlType</span><span class="sxs-lookup"><span data-stu-id="575f0-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamControlType Simple Type</span></span>

<span data-ttu-id="575f0-104">Describe cómo el perfil controla la itinerancia.</span><span class="sxs-lookup"><span data-stu-id="575f0-104">Describes how the profile controls roaming.</span></span>

<span data-ttu-id="575f0-105">Hay dos Estados posibles de registro de itinerancia:</span><span class="sxs-lookup"><span data-stu-id="575f0-105">There are two possible roam registration states:</span></span>

-   <span data-ttu-id="575f0-106">Asociado: registrado en una red estrechamente ligada a la red doméstica</span><span class="sxs-lookup"><span data-stu-id="575f0-106">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="575f0-107">No asociado: registrado en una red que no está estrechamente asociada con la red doméstica</span><span class="sxs-lookup"><span data-stu-id="575f0-107">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="575f0-108">El significado preciso de "asociado" varía en función de la red, pero representa una relación más estrecha con las tarifas más favorables que un no asociado.</span><span class="sxs-lookup"><span data-stu-id="575f0-108">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="575f0-109">Este podría ser el caso si un operador basado en regiones tiene un acuerdo empresarial para usar la red de acceso de radio de otro operador fuera de su área principal.</span><span class="sxs-lookup"><span data-stu-id="575f0-109">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="575f0-110">También podría representar la diferencia entre la itinerancia dentro de una región (por ejemplo, la Unión Europea) y fuera de ella.</span><span class="sxs-lookup"><span data-stu-id="575f0-110">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

<span data-ttu-id="575f0-111">Tenga en cuenta que [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) es un atributo más expresivo que **roamControlType** y un perfil debe utilizar **roamControlType** o **roamApplicabilityType**, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="575f0-111">Note that [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) is a more expressive attribute than **roamControlType**, and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="575f0-112">(Si un perfil usa ambos, se aplican ambos.</span><span class="sxs-lookup"><span data-stu-id="575f0-112">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="575f0-113">El resultado es la intersección de los dos.</span><span class="sxs-lookup"><span data-stu-id="575f0-113">The result is the intersection of the two.)</span></span>

``` syntax
<xs:simpleType name="roamControlType">
    <xs:restriction>
        <xs:enumeration
            value="AllRoamAllowed"
         />
        <xs:enumeration
            value="PartnerRoamAllowed"
         />
        <xs:enumeration
            value="NoRoamAllowed"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="575f0-114">Valores de enumeración</span><span class="sxs-lookup"><span data-stu-id="575f0-114">Enumeration values</span></span>

<span data-ttu-id="575f0-115">El tipo simple **roamControlType** define los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="575f0-115">The **roamControlType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="575f0-116">Value</span><span class="sxs-lookup"><span data-stu-id="575f0-116">Value</span></span></th>
<th><span data-ttu-id="575f0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="575f0-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="575f0-118">AllRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="575f0-118">AllRoamAllowed</span></span></td>
<td><p><span data-ttu-id="575f0-119">La itinerancia se permite en redes asociadas y no asociadas.</span><span class="sxs-lookup"><span data-stu-id="575f0-119">Roaming is allowed on Partner and Non-Partner networks.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="575f0-120">PartnerRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="575f0-120">PartnerRoamAllowed</span></span></td>
<td><p><span data-ttu-id="575f0-121">La itinerancia solo se permite en redes de asociados.</span><span class="sxs-lookup"><span data-stu-id="575f0-121">Roaming is allowed only on Partner networks.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="575f0-122">NoRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="575f0-122">NoRoamAllowed</span></span></td>
<td><p><span data-ttu-id="575f0-123">No se permite la itinerancia.</span><span class="sxs-lookup"><span data-stu-id="575f0-123">No roaming is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



