---
description: Especifica el método de transmisión utilizado para los mensajes de EAPOL-Start.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: Elemento supplicantMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677748"
---
# <a name="supplicantmode-onex-element"></a><span data-ttu-id="f30bf-103">Elemento supplicantMode (OneX)</span><span class="sxs-lookup"><span data-stu-id="f30bf-103">supplicantMode (OneX) Element</span></span>

<span data-ttu-id="f30bf-104">El elemento supplicantMode (OneX) especifica el método de transmisión que se usa para los mensajes de EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="f30bf-104">The supplicantMode (OneX) element specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="f30bf-105">La siguiente tabla describe los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="f30bf-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="f30bf-106">Value</span><span class="sxs-lookup"><span data-stu-id="f30bf-106">Value</span></span>               | <span data-ttu-id="f30bf-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f30bf-107">Description</span></span>                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f30bf-108">inhibitTransmission</span><span class="sxs-lookup"><span data-stu-id="f30bf-108">inhibitTransmission</span></span> | <span data-ttu-id="f30bf-109">No se transmiten los mensajes de EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="f30bf-109">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="f30bf-110">Válido solo para perfiles de LAN con cable.</span><span class="sxs-lookup"><span data-stu-id="f30bf-110">Valid for wired LAN profiles only.</span></span>                                                                                             |
| <span data-ttu-id="f30bf-111">includeLearning</span><span class="sxs-lookup"><span data-stu-id="f30bf-111">includeLearning</span></span>     | <span data-ttu-id="f30bf-112">El cliente determina cuándo se deben enviar los paquetes de EAPOL-Start en función de la capacidad de la red.</span><span class="sxs-lookup"><span data-stu-id="f30bf-112">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="f30bf-113">EAPOL-Start mensajes solo se envían cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="f30bf-113">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="f30bf-114">Válido solo para perfiles de LAN con cable.</span><span class="sxs-lookup"><span data-stu-id="f30bf-114">Valid for wired LAN profiles only.</span></span> |
| <span data-ttu-id="f30bf-115">compliant</span><span class="sxs-lookup"><span data-stu-id="f30bf-115">compliant</span></span>           | <span data-ttu-id="f30bf-116">EAPOL-Start mensajes se transmiten según lo especificado por 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="f30bf-116">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="f30bf-117">Válido para perfiles de LAN inalámbrica y cableada.</span><span class="sxs-lookup"><span data-stu-id="f30bf-117">Valid for both wired and wireless LAN profiles.</span></span>                                                             |



 

<span data-ttu-id="f30bf-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f30bf-118">This element is optional.</span></span> <span data-ttu-id="f30bf-119">Cuando supplicantMode no se especifica en un perfil, se usa un valor de `compliant` para los perfiles de LAN inalámbrica y cableada.</span><span class="sxs-lookup"><span data-stu-id="f30bf-119">When supplicantMode is not specified in a profile, a value of `compliant` is used for both wired and wireless LAN profiles.</span></span>

<span data-ttu-id="f30bf-120">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="f30bf-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="f30bf-121">El elemento **supplicantMode** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f30bf-121">The **supplicantMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="f30bf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f30bf-122">Requirements</span></span>



| <span data-ttu-id="f30bf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f30bf-123">Requirement</span></span> | <span data-ttu-id="f30bf-124">Value</span><span class="sxs-lookup"><span data-stu-id="f30bf-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f30bf-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f30bf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f30bf-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f30bf-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f30bf-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f30bf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f30bf-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f30bf-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f30bf-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f30bf-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="f30bf-130">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="f30bf-130">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f30bf-131">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="f30bf-131">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="f30bf-132">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="f30bf-132">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f30bf-133">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="f30bf-133">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




