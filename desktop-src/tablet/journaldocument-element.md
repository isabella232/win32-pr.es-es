---
description: El elemento de nivel superior de un archivo XML de notas de Journal.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408df14347c130e6b0a73ba869b634ca2493fb56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546918"
---
# <a name="journaldocument-element"></a><span data-ttu-id="aca32-103">Elemento JournalDocument</span><span class="sxs-lookup"><span data-stu-id="aca32-103">JournalDocument Element</span></span>

<span data-ttu-id="aca32-104">El elemento de nivel superior de un archivo XML de notas de Journal.</span><span class="sxs-lookup"><span data-stu-id="aca32-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="aca32-105">Definición</span><span class="sxs-lookup"><span data-stu-id="aca32-105">Definition</span></span>

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a><span data-ttu-id="aca32-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="aca32-106">Parent Elements</span></span>

<span data-ttu-id="aca32-107">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aca32-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="aca32-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aca32-108">Child Elements</span></span>

[<span data-ttu-id="aca32-109">**Diseño de fondo**</span><span class="sxs-lookup"><span data-stu-id="aca32-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="aca32-110">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="aca32-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="aca32-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="aca32-111">Attributes</span></span>



| <span data-ttu-id="aca32-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="aca32-112">Attribute</span></span>             | <span data-ttu-id="aca32-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="aca32-113">Type</span></span>                      | <span data-ttu-id="aca32-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="aca32-114">Required</span></span> | <span data-ttu-id="aca32-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="aca32-115">Description</span></span>                                                      | <span data-ttu-id="aca32-116">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="aca32-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="aca32-117">**Versión**</span><span class="sxs-lookup"><span data-stu-id="aca32-117">**Version**</span></span>           | <span data-ttu-id="aca32-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="aca32-118">**xs:string**</span></span>             | <span data-ttu-id="aca32-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="aca32-119">Required</span></span> | <span data-ttu-id="aca32-120">Versión del documento de diario representada en el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="aca32-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="aca32-121">1,0</span><span class="sxs-lookup"><span data-stu-id="aca32-121">1.0</span></span>                       |
| <span data-ttu-id="aca32-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="aca32-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="aca32-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="aca32-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="aca32-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="aca32-124">Required</span></span> | <span data-ttu-id="aca32-125">El ancho predeterminado de la página del documento de diario.</span><span class="sxs-lookup"><span data-stu-id="aca32-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="aca32-126">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="aca32-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="aca32-127">**DefaultPageHeight**</span><span class="sxs-lookup"><span data-stu-id="aca32-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="aca32-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="aca32-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="aca32-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="aca32-129">Required</span></span> | <span data-ttu-id="aca32-130">El alto predeterminado de la página del documento de diario.</span><span class="sxs-lookup"><span data-stu-id="aca32-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="aca32-131">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="aca32-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="aca32-132">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="aca32-132">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="aca32-133">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="aca32-133">Element type</span></span> | <span data-ttu-id="aca32-134">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="aca32-134">**JournalDocument**</span></span>                        |
| <span data-ttu-id="aca32-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aca32-135">Namespace</span></span>    | <span data-ttu-id="aca32-136">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="aca32-136">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="aca32-137">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="aca32-137">Schema name</span></span>  | <span data-ttu-id="aca32-138">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="aca32-138">Journal Reader</span></span>                             |



 

 

 



