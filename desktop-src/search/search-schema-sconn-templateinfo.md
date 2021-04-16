---
description: Este <templateInfo> elemento opcional especifica un tipo de carpeta para mostrar los resultados de una consulta sobre este conector de búsqueda. Este elemento no tiene atributos y solo un elemento secundario obligatorio.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Elemento templateInfo (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696258"
---
# <a name="templateinfo-element-search-connector-schema"></a><span data-ttu-id="799e4-104">Elemento templateInfo (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="799e4-104">templateInfo Element (Search Connector Schema)</span></span>

<span data-ttu-id="799e4-105">Este <templateInfo> elemento opcional especifica un tipo de carpeta para mostrar los resultados de una consulta sobre este conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="799e4-105">This optional <templateInfo> element specifies a folder type for displaying the results from a query over this search connector.</span></span> <span data-ttu-id="799e4-106">Este elemento no tiene atributos y solo un elemento secundario obligatorio.</span><span class="sxs-lookup"><span data-stu-id="799e4-106">This element has no attributes and only one mandatory child.</span></span>

## <a name="syntax"></a><span data-ttu-id="799e4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="799e4-107">Syntax</span></span>


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="799e4-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="799e4-108">Element Information</span></span>



| <span data-ttu-id="799e4-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="799e4-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="799e4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="799e4-110">Child Elements</span></span>                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="799e4-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="799e4-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="799e4-112">Elemento folderType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="799e4-112">folderType Element (Search Connector Schema)</span></span>](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a><span data-ttu-id="799e4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="799e4-113">Remarks</span></span>

<span data-ttu-id="799e4-114">Si no especifica un tipo de carpeta determinado en el <templateInfo> elemento, Windows usa el tipo de carpeta conector de búsqueda general {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span><span class="sxs-lookup"><span data-stu-id="799e4-114">If you don't specify a particular folder type in the <templateInfo> element, Windows uses the general search connector folder type {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span></span>

## <a name="example-of-a-templateinfo-element"></a><span data-ttu-id="799e4-115">Ejemplo de un elemento templateInfo</span><span class="sxs-lookup"><span data-stu-id="799e4-115">Example of a templateInfo Element</span></span>


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



