---
description: El elemento booleano opcional <isDefaultNonOwnerSaveLocation> especifica si la ubicación descrita en el conector de búsqueda debe usarse como ubicación de almacenamiento predeterminada cuando un usuario de otro equipo de un grupo en el hogar decide guardar un elemento.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Elemento isDefaultNonOwnerSaveLocation (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696266"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a><span data-ttu-id="6d2c3-103">Elemento isDefaultNonOwnerSaveLocation (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="6d2c3-103">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="6d2c3-104">El elemento booleano opcional <isDefaultNonOwnerSaveLocation> especifica si la ubicación descrita en el conector de búsqueda debe usarse como ubicación de almacenamiento predeterminada cuando un usuario de otro equipo de un grupo en el hogar decide guardar un elemento.</span><span class="sxs-lookup"><span data-stu-id="6d2c3-104">The optional Boolean <isDefaultNonOwnerSaveLocation> element specifies whether the location described in the search connector should be used as the default save location when a user from another computer in a Homegroup chooses to save an item.</span></span> <span data-ttu-id="6d2c3-105">Este elemento no tiene ningún elemento secundario y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="6d2c3-105">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2c3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d2c3-106">Syntax</span></span>


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="6d2c3-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6d2c3-107">Element Information</span></span>



| <span data-ttu-id="6d2c3-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="6d2c3-108">Parent Element</span></span>                                                                                                   | <span data-ttu-id="6d2c3-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d2c3-109">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="6d2c3-110">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="6d2c3-110">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="6d2c3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d2c3-111">Remarks</span></span>

<span data-ttu-id="6d2c3-112">Si es true, cuando un usuario de otro equipo de un grupo en el hogar decide guardar un elemento, el explorador de Windows guarda el elemento en la ubicación especificada en el <simpleLocation> elemento.</span><span class="sxs-lookup"><span data-stu-id="6d2c3-112">If true, when a user from another computer in a Homegroup chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span>

## <a name="example"></a><span data-ttu-id="6d2c3-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d2c3-113">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



