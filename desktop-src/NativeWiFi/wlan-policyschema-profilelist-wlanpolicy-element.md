---
description: 'Elemento profileList (WLANPolicy): contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo.'
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: Elemento profileList (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4c7478f38ba7336738325bac6872866cd570288b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109203"
---
# <a name="profilelist-wlanpolicy-element"></a><span data-ttu-id="94c4e-103">Elemento profileList (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="94c4e-103">profileList (WLANPolicy) Element</span></span>

<span data-ttu-id="94c4e-104">El elemento profileList (WLANPolicy) contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo.</span><span class="sxs-lookup"><span data-stu-id="94c4e-104">The profileList (WLANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="94c4e-105">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="94c4e-105">This element is optional.</span></span> <span data-ttu-id="94c4e-106">Si este elemento está presente, debe contener al menos un perfil.</span><span class="sxs-lookup"><span data-stu-id="94c4e-106">If this element is present, it must contain at least one profile.</span></span>

<span data-ttu-id="94c4e-107">Los perfiles deben basarse en el esquema [de \_ perfil WLAN](wlan-profileschema-schema.md), con un elemento raíz [**de WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="94c4e-107">Profiles should be based on the [WLAN\_profile schema](wlan-profileschema-schema.md), with a root element of [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span></span>

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="94c4e-108">El **elemento profileList** se define mediante el [**elemento WLANPolicy.**](wlan-policyschema-wlanpolicy-element.md)</span><span class="sxs-lookup"><span data-stu-id="94c4e-108">The **profileList** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="94c4e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94c4e-109">Requirements</span></span>



| <span data-ttu-id="94c4e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="94c4e-110">Requirement</span></span> | <span data-ttu-id="94c4e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="94c4e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94c4e-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94c4e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="94c4e-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="94c4e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94c4e-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94c4e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="94c4e-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="94c4e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94c4e-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="94c4e-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="94c4e-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="94c4e-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="94c4e-118">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="94c4e-118">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="94c4e-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="94c4e-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="94c4e-120">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="94c4e-120">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




