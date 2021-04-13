---
description: El <simpleLocation> elemento especifica la ubicación de los conectores de búsqueda basados en el sistema de archivos o en el controlador de protocolo. Este elemento tiene dos elementos secundarios y ningún atributo.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: Elemento simpleLocation (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12c17ace36314ceb180f14b6de0eb7a890a385b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360179"
---
# <a name="simplelocation-element-search-connector-schema"></a><span data-ttu-id="a9546-104">Elemento simpleLocation (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="a9546-104">simpleLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="a9546-105">El <simpleLocation> elemento especifica la ubicación de los conectores de búsqueda basados en el sistema de archivos o en el controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="a9546-105">The <simpleLocation> element specifies the location for search connectors that are file-system based or protocol-handler based.</span></span> <span data-ttu-id="a9546-106">Este elemento tiene dos elementos secundarios y ningún atributo.</span><span class="sxs-lookup"><span data-stu-id="a9546-106">This element has two child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9546-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9546-107">Syntax</span></span>


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="a9546-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a9546-108">Element Information</span></span>



| <span data-ttu-id="a9546-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="a9546-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="a9546-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a9546-110">Child Elements</span></span>                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9546-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="a9546-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="a9546-112">simpleLocation URL (elemento) (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="a9546-112">simpleLocation url Element (Search Connector Schema)</span></span>](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | <span data-ttu-id="a9546-113">serializado: este elemento contiene la ShellLink con codificación Base64 que apunta a la ubicación definida en el <url> elemento.</span><span class="sxs-lookup"><span data-stu-id="a9546-113">serialized: This element contains the base64-encoded ShellLink pointing to the location defined in the <url> element.</span></span> <span data-ttu-id="a9546-114">Windows 7 crea el ShellLink a partir del valor del <url> elemento y actualiza correctamente este campo en la primera carga de esta biblioteca, por lo que el autor debe dejarlo vacío.</span><span class="sxs-lookup"><span data-stu-id="a9546-114">Windows 7 creates the ShellLink from the value of the <url> element and properly updates this field on the first load of this library, so it should be left empty by the author.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a9546-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9546-115">Remarks</span></span>

<span data-ttu-id="a9546-116">Este elemento se puede usar en lugar de <locationProvider> cuando la ubicación está en el sistema de archivos o el conector es un controlador de protocolo conocido (como MAPI:).</span><span class="sxs-lookup"><span data-stu-id="a9546-116">This element can be used instead of <locationProvider> when the location is on the file system or the connector is a known protocol handler (like mapi:).</span></span> <span data-ttu-id="a9546-117">Si <simpleLocation> está presente, no debe haber un <locationProvider> elemento.</span><span class="sxs-lookup"><span data-stu-id="a9546-117">If <simpleLocation> is present, there MUST NOT be a <locationProvider> element.</span></span> <span data-ttu-id="a9546-118">En el caso de los conectores de búsqueda de proveedores de servicios Web, use el [<locationProvider>](search-schema-sconn-locationprovider.md) elemento en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a9546-118">For web service provider search connectors, use the [<locationProvider>](search-schema-sconn-locationprovider.md) element instead.</span></span>

## <a name="examples"></a><span data-ttu-id="a9546-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a9546-119">Examples</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 



