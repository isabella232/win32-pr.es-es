---
description: El <iconReference> elemento opcional especifica un icono personalizado para esta ubicación. Este elemento no tiene atributos ni elementos secundarios.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Elemento iconReference (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c181efe3bb8ac04f08d4fa16016d3468af6f10c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540643"
---
# <a name="iconreference-element-search-connector-schema"></a><span data-ttu-id="f12bb-104">Elemento iconReference (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="f12bb-104">iconReference Element (Search Connector Schema)</span></span>

<span data-ttu-id="f12bb-105">El <iconReference> elemento opcional especifica un icono personalizado para esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="f12bb-105">The optional <iconReference> element specifies a custom icon for this location.</span></span> <span data-ttu-id="f12bb-106">Este elemento no tiene atributos ni elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="f12bb-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="f12bb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f12bb-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="f12bb-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f12bb-108">Element Information</span></span>



| <span data-ttu-id="f12bb-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="f12bb-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="f12bb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f12bb-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="f12bb-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="f12bb-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="f12bb-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f12bb-112">Remarks</span></span>

<span data-ttu-id="f12bb-113">El formato de la referencia debe especificarse en un formato adecuado para la función [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) : (por ejemplo, <dll file name> , <icon index> ).</span><span class="sxs-lookup"><span data-stu-id="f12bb-113">The format of the reference must be specified in a form suitable for the [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) function: (for example, <dll file name>,<icon index>).</span></span>

## <a name="example"></a><span data-ttu-id="f12bb-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f12bb-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
