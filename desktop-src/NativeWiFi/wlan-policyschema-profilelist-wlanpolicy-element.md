---
description: Contiene una lista de perfiles que se van a aplicar en el nivel de dominio o de equipo.
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: profileList (WLANPolicy), elemento
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
ms.openlocfilehash: 9c11fbeb41b43faa31b170dcc856bb0823631001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678305"
---
# <a name="profilelist-wlanpolicy-element"></a><span data-ttu-id="2041b-103">profileList (WLANPolicy), elemento</span><span class="sxs-lookup"><span data-stu-id="2041b-103">profileList (WLANPolicy) Element</span></span>

<span data-ttu-id="2041b-104">El elemento profileList (WLANPolicy) contiene una lista de perfiles que se van a aplicar en el nivel de dominio o de equipo.</span><span class="sxs-lookup"><span data-stu-id="2041b-104">The profileList (WLANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="2041b-105">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="2041b-105">This element is optional.</span></span> <span data-ttu-id="2041b-106">Si este elemento está presente, debe contener al menos un perfil.</span><span class="sxs-lookup"><span data-stu-id="2041b-106">If this element is present, it must contain at least one profile.</span></span>

<span data-ttu-id="2041b-107">Los perfiles deben basarse en [el \_ esquema de Perfil de WLAN](wlan-profileschema-schema.md), con un elemento raíz de [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="2041b-107">Profiles should be based on the [WLAN\_profile schema](wlan-profileschema-schema.md), with a root element of [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span></span>

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

<span data-ttu-id="2041b-108">El elemento **profileList** se define mediante el elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2041b-108">The **profileList** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2041b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2041b-109">Requirements</span></span>



| <span data-ttu-id="2041b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="2041b-110">Requirement</span></span> | <span data-ttu-id="2041b-111">Value</span><span class="sxs-lookup"><span data-stu-id="2041b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2041b-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2041b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2041b-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2041b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2041b-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2041b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2041b-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2041b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2041b-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="2041b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="2041b-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="2041b-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2041b-118">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="2041b-118">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="2041b-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="2041b-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2041b-120">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="2041b-120">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




