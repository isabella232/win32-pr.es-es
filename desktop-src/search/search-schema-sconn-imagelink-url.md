---
description: El <url> elemento especifica una dirección URL a la miniatura de este conector de búsqueda. Si <imageLink> existe, este elemento es obligatorio. No tiene elementos secundarios ni atributos.
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: imageLink URL (elemento) (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696269"
---
# <a name="imagelink-url-element-search-connector-schema"></a><span data-ttu-id="56464-105">imageLink URL (elemento) (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="56464-105">imageLink url Element (Search Connector Schema)</span></span>

<span data-ttu-id="56464-106">El <url> elemento especifica una dirección URL a la miniatura de este conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="56464-106">The <url> element specifies a URL to the thumbnail for this search connector.</span></span> <span data-ttu-id="56464-107">Si <imageLink> existe, este elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="56464-107">If <imageLink> exists, this element is required.</span></span> <span data-ttu-id="56464-108">No tiene elementos secundarios ni atributos.</span><span class="sxs-lookup"><span data-stu-id="56464-108">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="56464-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56464-109">Syntax</span></span>


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="56464-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="56464-110">Element Information</span></span>



| <span data-ttu-id="56464-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="56464-111">Parent Element</span></span>                                                                   | <span data-ttu-id="56464-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="56464-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="56464-113">Elemento imageLink (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="56464-113">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="56464-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56464-114">Remarks</span></span>

<span data-ttu-id="56464-115">El valor puede ser una ruta de acceso del sistema de archivos local o una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="56464-115">The value can be a local file system path or a URL.</span></span> <span data-ttu-id="56464-116">El archivo de imagen puede ser cualquiera de los tipos de imagen básicos compatibles con Windows 7 (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="56464-116">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelinkurl-element"></a><span data-ttu-id="56464-117">Ejemplo de un elemento imageLinkurl</span><span class="sxs-lookup"><span data-stu-id="56464-117">Example of an imageLinkurl Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



