---
description: Identifica el nombre y el identificador de proveedor de una red de telefonía móvil.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Elemento Provider (DataRoamingPartners)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: b5b36c973bf44175b90e25fd2a141fed3624d8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154192"
---
# <a name="provider-dataroamingpartners-element"></a><span data-ttu-id="b010f-103">Elemento Provider (DataRoamingPartners)</span><span class="sxs-lookup"><span data-stu-id="b010f-103">Provider (DataRoamingPartners) Element</span></span>

<span data-ttu-id="b010f-104">El elemento **Provider (DataRoamingPartners)** identifica el nombre y el identificador de proveedor de una red de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="b010f-104">The **Provider (DataRoamingPartners)** element identifies the name and provider ID for a cellular network.</span></span>

<span data-ttu-id="b010f-105">Este elemento tiene los siguientes elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b010f-105">This element has the following child elements.</span></span>

-   [<span data-ttu-id="b010f-106">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="b010f-106">**ProviderID**</span></span>](schema-providerid-providertype-element.md)
-   [<span data-ttu-id="b010f-107">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="b010f-107">**ProviderName**</span></span>](schema-providername-providertype-element.md)

<span data-ttu-id="b010f-108">Este elemento se puede definir varias veces dentro del elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b010f-108">This element can be defined multiple times within the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span> <span data-ttu-id="b010f-109">Debe definirse al menos una vez.</span><span class="sxs-lookup"><span data-stu-id="b010f-109">It must be defined at least once.</span></span>

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

<span data-ttu-id="b010f-110">El elemento de **proveedor** se define mediante el elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b010f-110">The **Provider** element is defined by the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b010f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b010f-111">Requirements</span></span>



| <span data-ttu-id="b010f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b010f-112">Requirement</span></span> | <span data-ttu-id="b010f-113">Value</span><span class="sxs-lookup"><span data-stu-id="b010f-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="b010f-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b010f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b010f-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="b010f-115">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="b010f-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b010f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b010f-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b010f-117">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="b010f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b010f-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="b010f-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="b010f-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b010f-120">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="b010f-120">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="b010f-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="b010f-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b010f-122">**DataRoamingPartners (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="b010f-122">**DataRoamingPartners (MBNProfile)**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




