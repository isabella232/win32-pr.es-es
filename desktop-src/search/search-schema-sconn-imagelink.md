---
description: El <imageLink> elemento opcional especifica una miniatura para este conector de búsqueda. Este elemento tiene un elemento secundario obligatorio y ningún atributo.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Elemento imageLink (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b2e5cbbfc8bbd98557ebd0405a09cf998e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696268"
---
# <a name="imagelink-element-search-connector-schema"></a><span data-ttu-id="28e6d-104">Elemento imageLink (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="28e6d-104">imageLink Element (Search Connector Schema)</span></span>

<span data-ttu-id="28e6d-105">El <imageLink> elemento opcional especifica una miniatura para este conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="28e6d-105">The optional <imageLink> element specifies a thumbnail for this search connector.</span></span> <span data-ttu-id="28e6d-106">Este elemento tiene un elemento secundario obligatorio y ningún atributo.</span><span class="sxs-lookup"><span data-stu-id="28e6d-106">This element has one mandatory child element and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e6d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28e6d-107">Syntax</span></span>


```
<!-- imageLink -->
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



## <a name="element-information"></a><span data-ttu-id="28e6d-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="28e6d-108">Element Information</span></span>



| <span data-ttu-id="28e6d-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="28e6d-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="28e6d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="28e6d-110">Child Elements</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28e6d-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="28e6d-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="28e6d-112">imageLink URL (elemento) (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="28e6d-112">imageLink url Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a><span data-ttu-id="28e6d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28e6d-113">Remarks</span></span>

<span data-ttu-id="28e6d-114">El valor de imageLink puede ser una ruta de acceso del sistema de archivos local o una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="28e6d-114">The imageLink value can be a local file system path or a URL.</span></span> <span data-ttu-id="28e6d-115">El archivo de imagen puede ser cualquiera de los tipos de imagen básicos compatibles con Windows 7 (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="28e6d-115">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelink-element"></a><span data-ttu-id="28e6d-116">Ejemplo de un elemento imageLink</span><span class="sxs-lookup"><span data-stu-id="28e6d-116">Example of an imageLink Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



