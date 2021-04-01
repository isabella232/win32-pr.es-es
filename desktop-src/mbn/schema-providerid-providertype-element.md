---
description: Especifica el identificador del proveedor de la red de telefonía móvil.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: ProviderID (providerType) (elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275503"
---
# <a name="providerid-providertype-element"></a><span data-ttu-id="a53d3-103">ProviderID (providerType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="a53d3-103">ProviderID (providerType) Element</span></span>

<span data-ttu-id="a53d3-104">El elemento **ProviderID (providerType)** especifica el identificador del proveedor de la red de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="a53d3-104">The **ProviderID (providerType)** element specifies the provider ID of the cellular network.</span></span>

<span data-ttu-id="a53d3-105">El elemento es una secuencia de dígitos con un máximo de 6 dígitos.</span><span class="sxs-lookup"><span data-stu-id="a53d3-105">The element is a sequence of digits with a maximum of 6 digits.</span></span>

<span data-ttu-id="a53d3-106">Este elemento es necesario en el elemento de [**proveedor**](schema-provider-dataroamingpartners-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a53d3-106">This element is required within the [**Provider**](schema-provider-dataroamingpartners-element.md) element.</span></span>

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

<span data-ttu-id="a53d3-107">El elemento **ProviderID** se define mediante el tipo complejo de [**providerType**](schema-providertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a53d3-107">The **ProviderID** element is defined by the [**providerType**](schema-providertype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a53d3-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a53d3-108">Requirements</span></span>



| <span data-ttu-id="a53d3-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a53d3-109">Requirement</span></span> | <span data-ttu-id="a53d3-110">Value</span><span class="sxs-lookup"><span data-stu-id="a53d3-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="a53d3-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a53d3-111">Minimum supported client</span></span><br/> | <span data-ttu-id="a53d3-112">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="a53d3-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a53d3-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a53d3-113">Minimum supported server</span></span><br/> | <span data-ttu-id="a53d3-114">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a53d3-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="a53d3-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="a53d3-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="a53d3-116">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="a53d3-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a53d3-117">**providerType**</span><span class="sxs-lookup"><span data-stu-id="a53d3-117">**providerType**</span></span>](schema-providertype-complextype.md)
</dt> <dt>

<span data-ttu-id="a53d3-118">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="a53d3-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a53d3-119">**Proveedor (DataRoamingPartners)**</span><span class="sxs-lookup"><span data-stu-id="a53d3-119">**Provider (DataRoamingPartners)**</span></span>](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




