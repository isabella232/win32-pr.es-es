---
description: Especifica el período de tiempo, en segundos, en el que un cliente no volverá a intentar la autenticación después de un intento de autenticación erróneo.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: Elemento heldPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f8664543a9ea5b0f3b290168129e589e9ccd68ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667141"
---
# <a name="heldperiod-onex-element"></a><span data-ttu-id="5e715-103">Elemento heldPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="5e715-103">heldPeriod (OneX) Element</span></span>

<span data-ttu-id="5e715-104">El elemento heldPeriod (OneX) especifica el período de tiempo, en segundos, en el que un cliente no volverá a intentar la autenticación después de un intento de autenticación erróneo.</span><span class="sxs-lookup"><span data-stu-id="5e715-104">The heldPeriod (OneX) element specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span>

<span data-ttu-id="5e715-105">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="5e715-105">This element is optional.</span></span> <span data-ttu-id="5e715-106">Cuando heldPeriod no se especifica en un perfil, se usa un valor de 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="5e715-106">When heldPeriod is not specified in a profile, a value of 1 second is used.</span></span>

<span data-ttu-id="5e715-107">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="5e715-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="5e715-108">El elemento **heldPeriod** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5e715-108">The **heldPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e715-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e715-109">Requirements</span></span>



| <span data-ttu-id="5e715-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e715-110">Requirement</span></span> | <span data-ttu-id="5e715-111">Value</span><span class="sxs-lookup"><span data-stu-id="5e715-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e715-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e715-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5e715-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e715-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e715-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e715-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5e715-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e715-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e715-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e715-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e715-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="5e715-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5e715-118">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="5e715-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="5e715-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="5e715-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5e715-120">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="5e715-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




