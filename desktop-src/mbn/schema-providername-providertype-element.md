---
description: Contiene el nombre de la red de telefonía móvil.
ms.assetid: 4169babb-7616-468a-93f0-de25cce0c88b
title: ProviderName (providerType) (elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderName
api_type:
- Schema
ms.openlocfilehash: 47929d508ad6d3a6567c1b52e720360f4e7cfbda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648211"
---
# <a name="providername-providertype-element"></a><span data-ttu-id="bdd18-103">ProviderName (providerType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="bdd18-103">ProviderName (providerType) Element</span></span>

<span data-ttu-id="bdd18-104">El elemento **providerName (providerType)** contiene el nombre de la red de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="bdd18-104">The **ProviderName (providerType)** element contains the name of the cellular network.</span></span>

<span data-ttu-id="bdd18-105">El elemento es una cadena con un máximo de 20 caracteres.</span><span class="sxs-lookup"><span data-stu-id="bdd18-105">The element is a string with a maximum of 20 characters.</span></span>

<span data-ttu-id="bdd18-106">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="bdd18-106">This element is optional.</span></span>

``` syntax
<xs:element name="ProviderName"
    type="providerNameType"
 />
```

<span data-ttu-id="bdd18-107">El elemento **providerName** se define mediante el tipo complejo de [**providerType**](schema-providertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bdd18-107">The **ProviderName** element is defined by the [**providerType**](schema-providertype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd18-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdd18-108">Requirements</span></span>



| <span data-ttu-id="bdd18-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdd18-109">Requirement</span></span> | <span data-ttu-id="bdd18-110">Value</span><span class="sxs-lookup"><span data-stu-id="bdd18-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="bdd18-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdd18-111">Minimum supported client</span></span><br/> | <span data-ttu-id="bdd18-112">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="bdd18-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="bdd18-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdd18-113">Minimum supported server</span></span><br/> | <span data-ttu-id="bdd18-114">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bdd18-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="bdd18-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdd18-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="bdd18-116">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="bdd18-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bdd18-117">**providerType**</span><span class="sxs-lookup"><span data-stu-id="bdd18-117">**providerType**</span></span>](schema-providertype-complextype.md)
</dt> <dt>

<span data-ttu-id="bdd18-118">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="bdd18-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bdd18-119">**Proveedor (DataRoamingPartners)**</span><span class="sxs-lookup"><span data-stu-id="bdd18-119">**Provider (DataRoamingPartners)**</span></span>](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




