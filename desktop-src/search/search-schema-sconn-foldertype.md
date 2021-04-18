---
description: El <folderType> elemento especifica el GUID para el tipo de carpeta. Este elemento es necesario si el <templateInfo> elemento existe. No tiene atributos ni elementos secundarios.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Elemento folderType (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7d2a9e7f83dbe225427a8370cd8f5e948a46cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497056"
---
# <a name="foldertype-element-search-connector-schema"></a><span data-ttu-id="821a0-105">Elemento folderType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="821a0-105">folderType Element (Search Connector Schema)</span></span>

<span data-ttu-id="821a0-106">El <folderType> elemento especifica el GUID para el tipo de carpeta.</span><span class="sxs-lookup"><span data-stu-id="821a0-106">The <folderType> element specifies GUID for the folder type.</span></span> <span data-ttu-id="821a0-107">Este elemento es necesario si el <templateInfo> elemento existe.</span><span class="sxs-lookup"><span data-stu-id="821a0-107">This element is required if the <templateInfo> element exists.</span></span> <span data-ttu-id="821a0-108">No tiene atributos ni elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="821a0-108">It has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="821a0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="821a0-109">Syntax</span></span>


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="821a0-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="821a0-110">Element Information</span></span>



| <span data-ttu-id="821a0-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="821a0-111">Parent Element</span></span>                                                                         | <span data-ttu-id="821a0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="821a0-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="821a0-113">Elemento templateInfo (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="821a0-113">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="821a0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="821a0-114">Remarks</span></span>

<span data-ttu-id="821a0-115">El GUID predeterminado es {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, un tipo de carpeta general para conectores de búsqueda federada (OpenSearch).</span><span class="sxs-lookup"><span data-stu-id="821a0-115">The default GUID is {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, a general folder type for federated search (OpenSearch) connectors.</span></span>

## <a name="example-of-a-foldertype-element"></a><span data-ttu-id="821a0-116">Ejemplo de un elemento folderType</span><span class="sxs-lookup"><span data-stu-id="821a0-116">Example of a folderType Element</span></span>


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



