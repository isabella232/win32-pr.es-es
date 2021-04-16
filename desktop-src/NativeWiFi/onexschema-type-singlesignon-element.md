---
description: Especifica cuándo se realiza el inicio de sesión único.
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: Elemento Type (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 947c8801e5b2534f4c3b4e548a2a2f2c7a4250d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677429"
---
# <a name="type-singlesignon-element"></a><span data-ttu-id="7e9a3-103">Elemento Type (singleSignOn)</span><span class="sxs-lookup"><span data-stu-id="7e9a3-103">type (singleSignOn) Element</span></span>

<span data-ttu-id="7e9a3-104">El elemento Type (singleSignOn) especifica cuándo se realiza el inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="7e9a3-104">The type (singleSignOn) element specifies when single sign on is performed.</span></span> <span data-ttu-id="7e9a3-105">Cuando se establece en `preLogon` , el inicio de sesión único se realiza antes de que el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="7e9a3-105">When set to `preLogon`, single sign on is performed before the user logs on.</span></span> <span data-ttu-id="7e9a3-106">Cuando se establece en `postLogon` , el inicio de sesión único se realiza inmediatamente después de que el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="7e9a3-106">When set to `postLogon`, single sign on is performed immediately after the user logs on.</span></span>

<span data-ttu-id="7e9a3-107">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="7e9a3-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="type"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="preLogon"
             />
            <xs:enumeration
                value="postLogon"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="7e9a3-108">El elemento de **tipo** se define mediante el elemento [**singleSignOn**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7e9a3-108">The **type** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e9a3-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e9a3-109">Requirements</span></span>



| <span data-ttu-id="7e9a3-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e9a3-110">Requirement</span></span> | <span data-ttu-id="7e9a3-111">Value</span><span class="sxs-lookup"><span data-stu-id="7e9a3-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e9a3-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e9a3-112">Minimum supported client</span></span><br/> | <span data-ttu-id="7e9a3-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7e9a3-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7e9a3-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e9a3-114">Minimum supported server</span></span><br/> | <span data-ttu-id="7e9a3-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e9a3-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e9a3-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e9a3-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e9a3-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="7e9a3-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7e9a3-118">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="7e9a3-118">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="7e9a3-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="7e9a3-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7e9a3-120">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="7e9a3-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 




