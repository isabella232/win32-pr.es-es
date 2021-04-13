---
description: El elemento booleano opcional <isDefaultSaveLocation> especifica si la ubicación descrita en el conector de búsqueda debe usarse como ubicación de almacenamiento predeterminada. Este elemento no tiene ningún elemento secundario y no tiene atributos.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: Elemento isDefaultSaveLocation (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b664e4cd6f7c88f1dfbeb44ba23faee5d24a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360181"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a><span data-ttu-id="2f8f5-104">Elemento isDefaultSaveLocation (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="2f8f5-104">isDefaultSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="2f8f5-105">El elemento booleano opcional <isDefaultSaveLocation> especifica si la ubicación descrita en el conector de búsqueda debe usarse como ubicación de almacenamiento predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2f8f5-105">The optional Boolean <isDefaultSaveLocation> element specifies whether the location described in the search connector should be used as the default save location.</span></span> <span data-ttu-id="2f8f5-106">Este elemento no tiene ningún elemento secundario y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2f8f5-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f8f5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f8f5-107">Syntax</span></span>


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="2f8f5-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2f8f5-108">Element Information</span></span>



| <span data-ttu-id="2f8f5-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2f8f5-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="2f8f5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2f8f5-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="2f8f5-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="2f8f5-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="2f8f5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f8f5-112">Remarks</span></span>

<span data-ttu-id="2f8f5-113">Cuando un usuario elige guardar un elemento, el explorador de Windows guarda el elemento en la ubicación especificada en el <simpleLocation> elemento.</span><span class="sxs-lookup"><span data-stu-id="2f8f5-113">When a user chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span> <span data-ttu-id="2f8f5-114">Los usuarios pueden cambiar esta configuración mediante el cuadro de diálogo Propiedades del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2f8f5-114">Users can change this setting using the Properties dialog for the search connector.</span></span>

## <a name="example"></a><span data-ttu-id="2f8f5-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2f8f5-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



