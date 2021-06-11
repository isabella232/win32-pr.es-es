---
title: Elemento AcceptServerName (PeapExtensionsType)
description: El elemento AcceptServerName (PeapExtensionsType) indica si el nombre del servidor se valida con la cadena de nombre especificada en ServerNames en el esquema mspeapconnectionpropertiesv2.
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Elemento AcceptServerName EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64e82defae9c5ae9f7cf60056cfdac8b58373602
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989480"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="797f4-104">Elemento AcceptServerName (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="797f4-104">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="797f4-105">El **elemento AcceptServerName (PeapExtensionsType)** indica si el nombre del servidor se valida con la cadena de nombre especificada en el elemento [**ServerNames (ServerValidationParameters).**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)</span><span class="sxs-lookup"><span data-stu-id="797f4-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="797f4-106">El **elemento AcceptServerName** se define mediante el [**elemento PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="797f4-106">The **AcceptServerName** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="797f4-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="797f4-107">Remarks</span></span>

<span data-ttu-id="797f4-108">El **elemento AcceptServerName** es opcional.</span><span class="sxs-lookup"><span data-stu-id="797f4-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="797f4-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="797f4-109">Requirements</span></span>



| <span data-ttu-id="797f4-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="797f4-110">Requirement</span></span> | <span data-ttu-id="797f4-111">Valor</span><span class="sxs-lookup"><span data-stu-id="797f4-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="797f4-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="797f4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="797f4-113">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="797f4-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="797f4-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="797f4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="797f4-115">Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="797f4-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="797f4-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="797f4-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="797f4-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="797f4-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="797f4-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="797f4-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="797f4-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="797f4-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="797f4-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="797f4-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="797f4-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="797f4-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="797f4-122">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="797f4-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="797f4-123">Mspeapconnectionpropertiesv2 Schema</span><span class="sxs-lookup"><span data-stu-id="797f4-123">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="797f4-124">Elementos de esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="797f4-124">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





