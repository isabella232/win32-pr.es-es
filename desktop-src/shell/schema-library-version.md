---
description: El <version> elemento especifica la versión de contenido de esta biblioteca. Este elemento no tiene atributos ni elementos secundarios.
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: version (elemento, esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7b16a6078a16f4ebbe5e995503114996572f1b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984583"
---
# <a name="version-element-library-schema"></a><span data-ttu-id="83328-104">version (elemento, esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="83328-104">version Element (Library Schema)</span></span>

<span data-ttu-id="83328-105">El <version> elemento especifica la versión de contenido de esta biblioteca.</span><span class="sxs-lookup"><span data-stu-id="83328-105">The <version> element specifies the content version of this library.</span></span> <span data-ttu-id="83328-106">Este elemento no tiene atributos ni elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="83328-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="83328-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83328-107">Syntax</span></span>

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a><span data-ttu-id="83328-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="83328-108">Element Information</span></span>



| <span data-ttu-id="83328-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="83328-109">Parent Element</span></span>                                                               | <span data-ttu-id="83328-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="83328-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="83328-111">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="83328-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | <span data-ttu-id="83328-112">Ninguno</span><span class="sxs-lookup"><span data-stu-id="83328-112">None</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="83328-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83328-113">Remarks</span></span>

<span data-ttu-id="83328-114">La versión de contenido de la biblioteca es diferente de la versión de formato de archivo ( \* . Library-MS) de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="83328-114">The content version of the library is different from the library's file format (\*.library-ms) version.</span></span> <span data-ttu-id="83328-115">La versión de formato de archivo de la biblioteca se especifica en el [espacio de nombres](library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="83328-115">The library's file format version is specified in the [namespace](library-schema-entry.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="83328-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83328-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83328-117">Esquema de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="83328-117">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="83328-118">Esquema de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="83328-118">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
