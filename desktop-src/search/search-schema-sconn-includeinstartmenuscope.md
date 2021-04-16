---
description: El elemento booleano opcional <includeInStartMenuScope> especifica si este conector de búsqueda debe incluirse en el ámbito de búsqueda del menú Inicio.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Elemento includeInStartMenuScope (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126d10a2b69dcec5057e732679c8531fd6e82bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696267"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a><span data-ttu-id="a1868-103">Elemento includeInStartMenuScope (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="a1868-103">includeInStartMenuScope Element (Search Connector Schema)</span></span>

<span data-ttu-id="a1868-104">El elemento booleano opcional <includeInStartMenuScope> especifica si este conector de búsqueda debe incluirse en el ámbito de búsqueda del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="a1868-104">The optional Boolean <includeInStartMenuScope> element specifies whether this search connector should be included in the Start menu search scope.</span></span> <span data-ttu-id="a1868-105">El valor predeterminado es true para los conectores de búsqueda que usan el sistema de archivos como origen de datos y false para los conectores de búsqueda utilizados por los controladores de propiedades.</span><span class="sxs-lookup"><span data-stu-id="a1868-105">The default value is true for search connectors using the file system as a data source, and false for search connectors used by property handlers.</span></span> <span data-ttu-id="a1868-106">Este elemento no tiene ningún elemento secundario y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="a1868-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1868-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1868-107">Syntax</span></span>


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="a1868-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a1868-108">Element Information</span></span>



| <span data-ttu-id="a1868-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="a1868-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="a1868-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a1868-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="a1868-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="a1868-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="a1868-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1868-112">Remarks</span></span>

<span data-ttu-id="a1868-113">Si incluye el conector de búsqueda en el ámbito del menú Inicio, los usuarios pueden buscar en su ubicación en el cuadro de búsqueda del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="a1868-113">If you include the search connector in the Start menu scope, users can search your location from the search box in the Start menu.</span></span>

## <a name="example"></a><span data-ttu-id="a1868-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1868-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



