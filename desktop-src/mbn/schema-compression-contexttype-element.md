---
description: Especifica si se usará la compresión en el vínculo de datos para el encabezado y la transferencia de datos.
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: Elemento Compression (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908047"
---
# <a name="compression-contexttype-element"></a><span data-ttu-id="18c38-103">Elemento Compression (contextType)</span><span class="sxs-lookup"><span data-stu-id="18c38-103">Compression (contextType) Element</span></span>

<span data-ttu-id="18c38-104">El elemento **Compression (contextType)** especifica si se usará la compresión en el vínculo de datos para el encabezado y la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="18c38-104">The **Compression (contextType)** element specifies if compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="18c38-105">Este elemento puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="18c38-105">This element can be one of the following values.</span></span>

| <span data-ttu-id="18c38-106">Value</span><span class="sxs-lookup"><span data-stu-id="18c38-106">Value</span></span>     | <span data-ttu-id="18c38-107">Significado</span><span class="sxs-lookup"><span data-stu-id="18c38-107">Meaning</span></span>                       |
|-----------|-------------------------------|
| <span data-ttu-id="18c38-108">PERMITE</span><span class="sxs-lookup"><span data-stu-id="18c38-108">"ENABLE"</span></span>  | <span data-ttu-id="18c38-109">Se usará la compresión.</span><span class="sxs-lookup"><span data-stu-id="18c38-109">Compression will be used.</span></span>     |
| <span data-ttu-id="18c38-110">ACTIVA</span><span class="sxs-lookup"><span data-stu-id="18c38-110">"DISABLE"</span></span> | <span data-ttu-id="18c38-111">No se usará la compresión.</span><span class="sxs-lookup"><span data-stu-id="18c38-111">Compression will not be used.</span></span> |



 

<span data-ttu-id="18c38-112">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="18c38-112">This element is optional.</span></span> <span data-ttu-id="18c38-113">Si no se especifica este elemento, el sistema de banda ancha móvil no usará la compresión.</span><span class="sxs-lookup"><span data-stu-id="18c38-113">If this element is not specified, then the Mobile Broadband system will not use compression.</span></span>

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="18c38-114">El elemento **Compression** se define mediante el tipo complejo de [**contextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="18c38-114">The **Compression** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="18c38-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18c38-115">Requirements</span></span>



| <span data-ttu-id="18c38-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="18c38-116">Requirement</span></span> | <span data-ttu-id="18c38-117">Value</span><span class="sxs-lookup"><span data-stu-id="18c38-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="18c38-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18c38-118">Minimum supported client</span></span><br/> | <span data-ttu-id="18c38-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="18c38-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="18c38-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18c38-120">Minimum supported server</span></span><br/> | <span data-ttu-id="18c38-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="18c38-121">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="18c38-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="18c38-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="18c38-123">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="18c38-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="18c38-124">**contextType**</span><span class="sxs-lookup"><span data-stu-id="18c38-124">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="18c38-125">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="18c38-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="18c38-126">**Contexto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="18c38-126">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




