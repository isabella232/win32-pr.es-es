---
title: Select (QueryType) (elemento)
description: Consulta XPath que identifica los eventos que se van a incluir en el conjunto de resultados de la consulta.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Elemento Select EventLog
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422557"
---
# <a name="select-querytype-element"></a><span data-ttu-id="5229b-104">Select (QueryType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="5229b-104">Select (QueryType) Element</span></span>

<span data-ttu-id="5229b-105">Consulta XPath que identifica los eventos que se van a incluir en el conjunto de resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="5229b-105">An XPath query that identifies the events to include in the query result set.</span></span>

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="5229b-106">El elemento **Select** se define mediante el tipo complejo de [**QueryType**](queryschema-querytype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5229b-106">The **Select** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="5229b-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="5229b-107">Attributes</span></span>



| <span data-ttu-id="5229b-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="5229b-108">Name</span></span> | <span data-ttu-id="5229b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5229b-109">Type</span></span>   | <span data-ttu-id="5229b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5229b-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5229b-111">Path</span><span class="sxs-lookup"><span data-stu-id="5229b-111">Path</span></span> | <span data-ttu-id="5229b-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="5229b-112">anyURI</span></span> | <span data-ttu-id="5229b-113">El nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.</span><span class="sxs-lookup"><span data-stu-id="5229b-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5229b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5229b-114">Requirements</span></span>



| <span data-ttu-id="5229b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5229b-115">Requirement</span></span> | <span data-ttu-id="5229b-116">Value</span><span class="sxs-lookup"><span data-stu-id="5229b-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="5229b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5229b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5229b-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="5229b-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="5229b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5229b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5229b-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="5229b-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5229b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5229b-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="5229b-122">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="5229b-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="5229b-123">**Consulta (QueryListType)**</span><span class="sxs-lookup"><span data-stu-id="5229b-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





