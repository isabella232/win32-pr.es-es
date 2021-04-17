---
description: Contiene una lista de perfiles que se van a aplicar en el nivel de dominio o de equipo.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: profileList (LANPolicy), elemento
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
ms.openlocfilehash: b85c284262c070f7a9349933f99ad858cf047913
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667937"
---
# <a name="profilelist-lanpolicy-element"></a><span data-ttu-id="792ab-103">profileList (LANPolicy), elemento</span><span class="sxs-lookup"><span data-stu-id="792ab-103">profileList (LANPolicy) Element</span></span>

<span data-ttu-id="792ab-104">El elemento profileList (LANPolicy) contiene una lista de perfiles que se van a aplicar en el nivel de dominio o de equipo.</span><span class="sxs-lookup"><span data-stu-id="792ab-104">The profileList (LANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="792ab-105">Los perfiles deben basarse en [el \_ esquema de Perfil de LAN](lan-profileschema-schema.md), con un elemento raíz de [**LANProfile**](lan-profileschema-lanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="792ab-105">Profiles must be based on the [LAN\_profile schema](lan-profileschema-schema.md), with a root element of [**LANProfile**](lan-profileschema-lanprofile-element.md).</span></span> <span data-ttu-id="792ab-106">Los perfiles basados en cualquier otro esquema se omitirán.</span><span class="sxs-lookup"><span data-stu-id="792ab-106">Profiles based on any other schema will be ignored.</span></span>

<span data-ttu-id="792ab-107">Cuando [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) se establece en false, este elemento no debe estar presente en un perfil de directiva de LAN.</span><span class="sxs-lookup"><span data-stu-id="792ab-107">When [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) is set to FALSE, this element must not be present in a LAN policy profile.</span></span> <span data-ttu-id="792ab-108">Cuando **enableAutoConfig** se establece en true, este elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="792ab-108">When **enableAutoConfig** is set to TRUE, then this element is required.</span></span>

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

<span data-ttu-id="792ab-109">El elemento **profileList** se define mediante el elemento [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="792ab-109">The **profileList** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="792ab-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="792ab-110">Remarks</span></span>

<span data-ttu-id="792ab-111">Este elemento debe contener exactamente un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="792ab-111">This element should contain exactly one network profile.</span></span> <span data-ttu-id="792ab-112">Si se especifica más de un perfil en la Directiva, solo se aplicará la primera red.</span><span class="sxs-lookup"><span data-stu-id="792ab-112">If more than one profile is specified in the policy, only the first network will be applied.</span></span>

## <a name="requirements"></a><span data-ttu-id="792ab-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="792ab-113">Requirements</span></span>



| <span data-ttu-id="792ab-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="792ab-114">Requirement</span></span> | <span data-ttu-id="792ab-115">Value</span><span class="sxs-lookup"><span data-stu-id="792ab-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="792ab-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="792ab-116">Minimum supported client</span></span><br/> | <span data-ttu-id="792ab-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="792ab-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="792ab-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="792ab-118">Minimum supported server</span></span><br/> | <span data-ttu-id="792ab-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="792ab-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="792ab-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="792ab-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="792ab-121">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="792ab-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="792ab-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="792ab-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="792ab-123">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="792ab-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="792ab-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="792ab-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




