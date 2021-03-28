---
description: El <name> elemento especifica el nombre de esta biblioteca. Este elemento es obligatorio y no tiene atributos ni elementos secundarios.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Name (elemento, esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997956"
---
# <a name="name-element-library-schema"></a><span data-ttu-id="8e0a0-104">Name (elemento, esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8e0a0-104">name Element (Library Schema)</span></span>

<span data-ttu-id="8e0a0-105">El <name> elemento especifica el nombre de esta biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8e0a0-105">The <name> element specifies the name of this library.</span></span> <span data-ttu-id="8e0a0-106">Este elemento es obligatorio y no tiene atributos ni elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="8e0a0-106">This element is required and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e0a0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e0a0-107">Syntax</span></span>

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a><span data-ttu-id="8e0a0-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8e0a0-108">Element Information</span></span>



| <span data-ttu-id="8e0a0-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="8e0a0-109">Parent Element</span></span>                                                               | <span data-ttu-id="8e0a0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8e0a0-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="8e0a0-111">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8e0a0-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="8e0a0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e0a0-112">Remarks</span></span>

<span data-ttu-id="8e0a0-113">El nombre es el nombre descriptivo de la biblioteca que se muestra en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="8e0a0-113">The name is the friendly library name that is displayed in Windows Explorer.</span></span> <span data-ttu-id="8e0a0-114">El nombre se puede especificar en un <dllname> <index> formato, como en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="8e0a0-114">The name can be specified in a <dllname>,<index> format, as in the following example.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="8e0a0-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e0a0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e0a0-116">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8e0a0-116">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="8e0a0-117">Esquema de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="8e0a0-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
