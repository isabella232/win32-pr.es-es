---
title: Tipo complejo de NamedQueryType
description: No se utiliza. Define una lista de consultas con nombre que consultan la cadena de mensaje de evento de un valor y realizan una acción especificada si se encuentran. | Tipo complejo de NamedQueryType
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- NamedQueryType tipo complejo EventLog
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698125"
---
# <a name="namedquerytype-complex-type"></a><span data-ttu-id="b6a3a-106">Tipo complejo de NamedQueryType</span><span class="sxs-lookup"><span data-stu-id="b6a3a-106">NamedQueryType Complex Type</span></span>

<span data-ttu-id="b6a3a-107">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b6a3a-107">Not used.</span></span> <span data-ttu-id="b6a3a-108">Define una lista de consultas con nombre que consultan la cadena de mensaje de evento de un valor y realizan una acción especificada si se encuentran.</span><span class="sxs-lookup"><span data-stu-id="b6a3a-108">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span>

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b6a3a-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b6a3a-109">Child elements</span></span>



| <span data-ttu-id="b6a3a-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b6a3a-110">Element</span></span>                                                                       | <span data-ttu-id="b6a3a-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6a3a-111">Type</span></span>                                                                             | <span data-ttu-id="b6a3a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6a3a-112">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6a3a-113">**patternMaps**</span><span class="sxs-lookup"><span data-stu-id="b6a3a-113">**patternMaps**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md) | [<span data-ttu-id="b6a3a-114">**PatternMapListType**</span><span class="sxs-lookup"><span data-stu-id="b6a3a-114">**PatternMapListType**</span></span>](eventmanifestschema-patternmaplisttype-complextype.md) | <span data-ttu-id="b6a3a-115">Define una lista de pares de expresiones regulares que se utilizan para modificar la cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b6a3a-115">Defines a list of regular expression pairs that are used to alter the message string.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="b6a3a-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b6a3a-116">Examples</span></span>

<span data-ttu-id="b6a3a-117">En el ejemplo siguiente se muestra cómo usar el elemento [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a3a-117">The following example shows how to use the [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) element.</span></span> <span data-ttu-id="b6a3a-118">En este ejemplo se toma el contenido de la cadena de mensaje y se inserta en la cadena https://www .*messagestring*. com.</span><span class="sxs-lookup"><span data-stu-id="b6a3a-118">This example takes the contents of the message string and inserts it into the string https://www.*messagestring*.com.</span></span> <span data-ttu-id="b6a3a-119">A continuación, reemplaza la cadena de mensaje con el resultado.</span><span class="sxs-lookup"><span data-stu-id="b6a3a-119">It then replaces the message string with the result.</span></span> <span data-ttu-id="b6a3a-120">Por ejemplo, si la cadena de mensaje contiene Microsoft, la consulta reemplazaría la cadena de mensaje de Microsoft por https://www.Microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="b6a3a-120">For example, if the message string contained Microsoft, the query would replace the Microsoft message string with https://www.Microsoft.com.</span></span>


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a><span data-ttu-id="b6a3a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6a3a-121">Requirements</span></span>



| <span data-ttu-id="b6a3a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6a3a-122">Requirement</span></span> | <span data-ttu-id="b6a3a-123">Value</span><span class="sxs-lookup"><span data-stu-id="b6a3a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b6a3a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6a3a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b6a3a-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b6a3a-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b6a3a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6a3a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b6a3a-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6a3a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





