---
description: El <supportsAdvancedQuerySyntax> elemento booleano especifica si el proveedor de búsquedas admite la sintaxis de consulta avanzada. El valor predeterminado es false. Este elemento es opcional y no tiene ningún elemento secundario y ningún atributo.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: Elemento supportsAdvancedQuerySyntax (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d31eb96615c952f703729fd9d22f2e5d27f38b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696259"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a><span data-ttu-id="4d042-105">Elemento supportsAdvancedQuerySyntax (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="4d042-105">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>

<span data-ttu-id="4d042-106">El <supportsAdvancedQuerySyntax> elemento booleano especifica si el proveedor de búsquedas admite la [Sintaxis de consulta avanzada](-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="4d042-106">The Boolean <supportsAdvancedQuerySyntax> element specifies whether the search provider supports the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md).</span></span> <span data-ttu-id="4d042-107">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="4d042-107">The default is false.</span></span> <span data-ttu-id="4d042-108">Este elemento es opcional y no tiene ningún elemento secundario y ningún atributo.</span><span class="sxs-lookup"><span data-stu-id="4d042-108">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d042-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d042-109">Syntax</span></span>


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="4d042-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4d042-110">Element Information</span></span>



| <span data-ttu-id="4d042-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="4d042-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="4d042-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4d042-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="4d042-113">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="4d042-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="4d042-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d042-114">Remarks</span></span>

<span data-ttu-id="4d042-115">El valor `true` indica que el proveedor de búsquedas admite la sintaxis de consulta avanzada enviada en consultas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4d042-115">The value `true` indicates that the search provider supports Advanced Query Syntax sent in search queries.</span></span>

## <a name="example"></a><span data-ttu-id="4d042-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d042-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



