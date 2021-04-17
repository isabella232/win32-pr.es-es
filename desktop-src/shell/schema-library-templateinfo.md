---
description: El <templateInfo> elemento es un contenedor para el elemento folderType, que especifica un tipo de carpeta para mostrar los resultados de una consulta en esta biblioteca. Este elemento es opcional y no tiene atributos.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Elemento templateInfo (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543099"
---
# <a name="templateinfo-element-library-schema"></a><span data-ttu-id="14283-104">Elemento templateInfo (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="14283-104">templateInfo Element (Library Schema)</span></span>

<span data-ttu-id="14283-105">El <templateInfo> elemento es un contenedor para el elemento [folderType](schema-library-foldertype.md) , que especifica un tipo de carpeta para mostrar los resultados de una consulta en esta biblioteca.</span><span class="sxs-lookup"><span data-stu-id="14283-105">The <templateInfo> element is a container for the [folderType](schema-library-foldertype.md) element, which specifies a folder type for displaying the results from a query over this library.</span></span> <span data-ttu-id="14283-106">Este elemento es opcional y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="14283-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="14283-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14283-107">Syntax</span></span>

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="14283-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="14283-108">Element Information</span></span>



| <span data-ttu-id="14283-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="14283-109">Parent Element</span></span>                                                               | <span data-ttu-id="14283-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="14283-110">Child Elements</span></span>                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="14283-111">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="14283-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="14283-112">Elemento folderType (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="14283-112">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)       |
|                                                                              | [<span data-ttu-id="14283-113">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="14283-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) |



 

## <a name="related-topics"></a><span data-ttu-id="14283-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14283-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14283-115">Esquema de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="14283-115">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="14283-116">[Esquema de Descripción del conector de búsqueda](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14283-116">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
