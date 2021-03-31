---
description: Contiene los detalles sobre una página individual en una nota de Journal.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911393"
---
# <a name="journalpage-element"></a><span data-ttu-id="7dfc7-103">Elemento JournalPage</span><span class="sxs-lookup"><span data-stu-id="7dfc7-103">JournalPage Element</span></span>

<span data-ttu-id="7dfc7-104">Contiene los detalles sobre una página individual en una nota de Journal.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="7dfc7-105">Definición</span><span class="sxs-lookup"><span data-stu-id="7dfc7-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="7dfc7-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="7dfc7-106">Parent Elements</span></span>

[<span data-ttu-id="7dfc7-107">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="7dfc7-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7dfc7-108">Child Elements</span></span>

[<span data-ttu-id="7dfc7-109">**Inmóvil**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="7dfc7-110">**DocImage**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="7dfc7-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="7dfc7-112">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="7dfc7-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="7dfc7-113">Attributes</span></span>



| <span data-ttu-id="7dfc7-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="7dfc7-114">Attribute</span></span>      | <span data-ttu-id="7dfc7-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="7dfc7-115">Type</span></span>                      | <span data-ttu-id="7dfc7-116">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7dfc7-116">Required</span></span> | <span data-ttu-id="7dfc7-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dfc7-117">Description</span></span>                                                                        | <span data-ttu-id="7dfc7-118">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="7dfc7-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="7dfc7-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-119">**Number**</span></span>     | <span data-ttu-id="7dfc7-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="7dfc7-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7dfc7-121">Required</span></span> | <span data-ttu-id="7dfc7-122">Número ordinal de la página dentro del documento de diario, comenzando por uno (1).</span><span class="sxs-lookup"><span data-stu-id="7dfc7-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="7dfc7-123">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="7dfc7-124">**Width**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-124">**Width**</span></span>      | <span data-ttu-id="7dfc7-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="7dfc7-126">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7dfc7-126">Required</span></span> | <span data-ttu-id="7dfc7-127">Ancho de la página.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-127">The width of the page.</span></span>                                                             | <span data-ttu-id="7dfc7-128">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="7dfc7-129">**Height**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-129">**Height**</span></span>     | <span data-ttu-id="7dfc7-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="7dfc7-131">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7dfc7-131">Required</span></span> | <span data-ttu-id="7dfc7-132">Alto de la página.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-132">The height of the page.</span></span>                                                            | <span data-ttu-id="7dfc7-133">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="7dfc7-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-134">**LineHeight**</span></span> | <span data-ttu-id="7dfc7-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="7dfc7-136">Opcionales</span><span class="sxs-lookup"><span data-stu-id="7dfc7-136">Optional</span></span> | <span data-ttu-id="7dfc7-137">Alto de la línea utilizada en la página.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="7dfc7-138">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="7dfc7-139">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-139">**LanguageId**</span></span> | <span data-ttu-id="7dfc7-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="7dfc7-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="7dfc7-141">Opcionales</span><span class="sxs-lookup"><span data-stu-id="7dfc7-141">Optional</span></span> | <span data-ttu-id="7dfc7-142">Identificador de idioma que se usa para la página.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="7dfc7-143">Entero no negativo que representa un identificador de idioma válido.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="7dfc7-144">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7dfc7-144">Element Information</span></span>



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="7dfc7-145">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7dfc7-145">Element type</span></span> | <span data-ttu-id="7dfc7-146">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="7dfc7-146">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="7dfc7-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7dfc7-147">Namespace</span></span>    | <span data-ttu-id="7dfc7-148">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="7dfc7-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="7dfc7-149">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="7dfc7-149">Schema name</span></span>  | <span data-ttu-id="7dfc7-150">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="7dfc7-150">Journal Reader</span></span>                                                      |



 

 

 



