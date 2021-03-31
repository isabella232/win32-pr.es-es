---
title: Suppress (QueryType) (elemento)
description: Consulta XPath que identifica los eventos que se van a excluir del conjunto de resultados de la consulta.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Elemento suprimir EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151169"
---
# <a name="suppress-querytype-element"></a><span data-ttu-id="af53a-104">Suppress (QueryType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="af53a-104">Suppress (QueryType) Element</span></span>

<span data-ttu-id="af53a-105">Consulta XPath que identifica los eventos que se van a excluir del conjunto de resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="af53a-105">An XPath query that identifies the events to exclude from the query result set.</span></span>

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="af53a-106">El elemento **Suppress** se define mediante el tipo complejo [**QueryType**](queryschema-querytype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="af53a-106">The **Suppress** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="af53a-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="af53a-107">Attributes</span></span>



| <span data-ttu-id="af53a-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="af53a-108">Name</span></span> | <span data-ttu-id="af53a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="af53a-109">Type</span></span>   | <span data-ttu-id="af53a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="af53a-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af53a-111">Path</span><span class="sxs-lookup"><span data-stu-id="af53a-111">Path</span></span> | <span data-ttu-id="af53a-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="af53a-112">anyURI</span></span> | <span data-ttu-id="af53a-113">El nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.</span><span class="sxs-lookup"><span data-stu-id="af53a-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="af53a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af53a-114">Requirements</span></span>



| <span data-ttu-id="af53a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="af53a-115">Requirement</span></span> | <span data-ttu-id="af53a-116">Value</span><span class="sxs-lookup"><span data-stu-id="af53a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af53a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af53a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="af53a-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="af53a-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af53a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af53a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="af53a-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="af53a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af53a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="af53a-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="af53a-122">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="af53a-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="af53a-123">**Consulta (QueryListType)**</span><span class="sxs-lookup"><span data-stu-id="af53a-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





