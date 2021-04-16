---
description: Especifica el número máximo de errores de autenticación permitido para un conjunto de credenciales.
ms.assetid: 191b6b03-8b27-4b35-8623-1ccec632f208
title: Elemento maxAuthFailures (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxAuthFailures
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 31dae7a8805275254a1d398108128380b1aa2e54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545398"
---
# <a name="maxauthfailures-onex-element"></a><span data-ttu-id="917fd-103">Elemento maxAuthFailures (OneX)</span><span class="sxs-lookup"><span data-stu-id="917fd-103">maxAuthFailures (OneX) Element</span></span>

<span data-ttu-id="917fd-104">El elemento maxAuthFailures (OneX) especifica el número máximo de errores de autenticación permitido para un conjunto de credenciales.</span><span class="sxs-lookup"><span data-stu-id="917fd-104">The maxAuthFailures (OneX) element specifies the maximum number of authentication failures allowed for a set of credentials.</span></span>

<span data-ttu-id="917fd-105">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="917fd-105">This element is optional.</span></span> <span data-ttu-id="917fd-106">Cuando maxAuthFailures no se especifica en un perfil, se usa un valor de uno.</span><span class="sxs-lookup"><span data-stu-id="917fd-106">When maxAuthFailures is not specified in a profile, a value of one is used.</span></span>

<span data-ttu-id="917fd-107">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="917fd-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxAuthFailures">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="917fd-108">El elemento **maxAuthFailures** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="917fd-108">The **maxAuthFailures** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="917fd-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="917fd-109">Requirements</span></span>



| <span data-ttu-id="917fd-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="917fd-110">Requirement</span></span> | <span data-ttu-id="917fd-111">Value</span><span class="sxs-lookup"><span data-stu-id="917fd-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="917fd-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="917fd-112">Minimum supported client</span></span><br/> | <span data-ttu-id="917fd-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="917fd-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="917fd-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="917fd-114">Minimum supported server</span></span><br/> | <span data-ttu-id="917fd-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="917fd-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="917fd-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="917fd-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="917fd-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="917fd-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="917fd-118">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="917fd-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="917fd-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="917fd-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="917fd-120">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="917fd-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




