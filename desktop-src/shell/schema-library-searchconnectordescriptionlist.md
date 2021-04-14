---
description: Este <searchConnectorDescriptionList> elemento contiene una lista de conectores de búsqueda que se asignan a ubicaciones incluidas en esta biblioteca. Cada conector de búsqueda se define mediante un <searchConnectorDescription> elemento. Este elemento es opcional y no tiene atributos.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Elemento searchConnectorDescriptionList (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985891"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a><span data-ttu-id="26b61-105">Elemento searchConnectorDescriptionList (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="26b61-105">searchConnectorDescriptionList Element (Library Schema)</span></span>

<span data-ttu-id="26b61-106">Este <searchConnectorDescriptionList> elemento contiene una lista de conectores de búsqueda que se asignan a ubicaciones incluidas en esta biblioteca.</span><span class="sxs-lookup"><span data-stu-id="26b61-106">This <searchConnectorDescriptionList> element contains a list of search connectors that map to locations included in this library.</span></span> <span data-ttu-id="26b61-107">Cada conector de búsqueda se define mediante un <searchConnectorDescription> elemento.</span><span class="sxs-lookup"><span data-stu-id="26b61-107">Each search connector is defined by a <searchConnectorDescription> element.</span></span> <span data-ttu-id="26b61-108">Este elemento es opcional y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="26b61-108">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b61-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26b61-109">Syntax</span></span>

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a><span data-ttu-id="26b61-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="26b61-110">Element Information</span></span>



| <span data-ttu-id="26b61-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="26b61-111">Parent Element</span></span>                                                               | <span data-ttu-id="26b61-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26b61-112">Child Elements</span></span>                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26b61-113">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="26b61-113">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="26b61-114">Elemento searchConnectorDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="26b61-114">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a><span data-ttu-id="26b61-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26b61-115">Remarks</span></span>

<span data-ttu-id="26b61-116">Los conectores de búsqueda para los ámbitos de búsqueda federada de Windows y de controlador de Protocolo no se pueden incluir en una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="26b61-116">Search connectors for Windows Federated Search and protocol handler scopes cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26b61-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26b61-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26b61-118">Esquema de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="26b61-118">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="26b61-119">[Esquema de Descripción del conector de búsqueda](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="26b61-119">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
