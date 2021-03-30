---
title: Tipo complejo de MapType
description: Define una lista de pares de nombre/valor.
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- MapType tipo complejo EventLog
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4daf6cfe677ab5585ac580e19c868f1bba17de45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801442"
---
# <a name="maptype-complex-type"></a><span data-ttu-id="6ca67-104">Tipo complejo de MapType</span><span class="sxs-lookup"><span data-stu-id="6ca67-104">MapType Complex Type</span></span>

<span data-ttu-id="6ca67-105">Define una lista de pares de nombre/valor.</span><span class="sxs-lookup"><span data-stu-id="6ca67-105">Defines a list of name/value pairs.</span></span>

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6ca67-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6ca67-106">Child elements</span></span>



| <span data-ttu-id="6ca67-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6ca67-107">Element</span></span>                                                          | <span data-ttu-id="6ca67-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ca67-108">Type</span></span>                                                                 | <span data-ttu-id="6ca67-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ca67-109">Description</span></span>                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ca67-110">**myBitmap**</span><span class="sxs-lookup"><span data-stu-id="6ca67-110">**bitMap**</span></span>](eventmanifestschema-bitmap-maptype-element.md)     | [<span data-ttu-id="6ca67-111">**BitMapType**</span><span class="sxs-lookup"><span data-stu-id="6ca67-111">**BitMapType**</span></span>](eventmanifestschema-bitmaptype-complextype.md)     | <span data-ttu-id="6ca67-112">Define una lista de pares de nombre/valor que asignan valores de bit y valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="6ca67-112">Defines a list of name/value pairs that map bit values and string values.</span></span><br/>     |
| [<span data-ttu-id="6ca67-113">**valueMap**</span><span class="sxs-lookup"><span data-stu-id="6ca67-113">**valueMap**</span></span>](eventmanifestschema-valuemap-maptype-element.md) | [<span data-ttu-id="6ca67-114">**ValueMapType**</span><span class="sxs-lookup"><span data-stu-id="6ca67-114">**ValueMapType**</span></span>](eventmanifestschema-valuemaptype-complextype.md) | <span data-ttu-id="6ca67-115">Define una lista de pares de nombre y valor que asignan valores enteros y valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="6ca67-115">Defines a list of name/value pairs that map integer values and string values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6ca67-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ca67-116">Remarks</span></span>

<span data-ttu-id="6ca67-117">Normalmente, se crean asignaciones para proporcionar valores de cadena enumerados para los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="6ca67-117">Typically, you create maps to provide enumerated string values for event data.</span></span>

## <a name="examples"></a><span data-ttu-id="6ca67-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6ca67-118">Examples</span></span>

<span data-ttu-id="6ca67-119">En el ejemplo siguiente se muestra cómo especificar un mapa de valores y un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6ca67-119">The following example shows how to specify a value map and bitmap.</span></span>


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a><span data-ttu-id="6ca67-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ca67-120">Requirements</span></span>



| <span data-ttu-id="6ca67-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ca67-121">Requirement</span></span> | <span data-ttu-id="6ca67-122">Value</span><span class="sxs-lookup"><span data-stu-id="6ca67-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6ca67-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ca67-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca67-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6ca67-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6ca67-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ca67-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca67-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ca67-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





