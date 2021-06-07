---
description: Contiene los detalles de una página individual en una nota de diario.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0939194585b067525fa841d6d41674180a40adb9
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432147"
---
# <a name="journalpage-element"></a><span data-ttu-id="19297-103">Elemento JournalPage</span><span class="sxs-lookup"><span data-stu-id="19297-103">JournalPage Element</span></span>

<span data-ttu-id="19297-104">Contiene los detalles de una página individual en una nota de diario.</span><span class="sxs-lookup"><span data-stu-id="19297-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="19297-105">Definición</span><span class="sxs-lookup"><span data-stu-id="19297-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="19297-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="19297-106">Parent Elements</span></span>

[<span data-ttu-id="19297-107">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="19297-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="19297-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="19297-108">Child Elements</span></span>

[<span data-ttu-id="19297-109">**Inmóvil**</span><span class="sxs-lookup"><span data-stu-id="19297-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="19297-110">**DocImage**</span><span class="sxs-lookup"><span data-stu-id="19297-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="19297-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="19297-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="19297-112">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="19297-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="19297-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="19297-113">Attributes</span></span>



| <span data-ttu-id="19297-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="19297-114">Attribute</span></span>      | <span data-ttu-id="19297-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="19297-115">Type</span></span>                      | <span data-ttu-id="19297-116">Requerido</span><span class="sxs-lookup"><span data-stu-id="19297-116">Required</span></span> | <span data-ttu-id="19297-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="19297-117">Description</span></span>                                                                        | <span data-ttu-id="19297-118">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="19297-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="19297-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="19297-119">**Number**</span></span>     | <span data-ttu-id="19297-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="19297-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="19297-121">Requerido</span><span class="sxs-lookup"><span data-stu-id="19297-121">Required</span></span> | <span data-ttu-id="19297-122">Número ordinal de la página dentro del documento Diario, empezando por uno (1).</span><span class="sxs-lookup"><span data-stu-id="19297-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="19297-123">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="19297-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="19297-124">**Width**</span><span class="sxs-lookup"><span data-stu-id="19297-124">**Width**</span></span>      | <span data-ttu-id="19297-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="19297-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="19297-126">Requerido</span><span class="sxs-lookup"><span data-stu-id="19297-126">Required</span></span> | <span data-ttu-id="19297-127">Ancho de la página.</span><span class="sxs-lookup"><span data-stu-id="19297-127">The width of the page.</span></span>                                                             | <span data-ttu-id="19297-128">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="19297-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="19297-129">**Height**</span><span class="sxs-lookup"><span data-stu-id="19297-129">**Height**</span></span>     | <span data-ttu-id="19297-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="19297-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="19297-131">Requerido</span><span class="sxs-lookup"><span data-stu-id="19297-131">Required</span></span> | <span data-ttu-id="19297-132">Alto de la página.</span><span class="sxs-lookup"><span data-stu-id="19297-132">The height of the page.</span></span>                                                            | <span data-ttu-id="19297-133">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="19297-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="19297-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="19297-134">**LineHeight**</span></span> | <span data-ttu-id="19297-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="19297-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="19297-136">Opcionales</span><span class="sxs-lookup"><span data-stu-id="19297-136">Optional</span></span> | <span data-ttu-id="19297-137">Alto de la línea utilizada en la página.</span><span class="sxs-lookup"><span data-stu-id="19297-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="19297-138">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="19297-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="19297-139">**Languageid**</span><span class="sxs-lookup"><span data-stu-id="19297-139">**LanguageId**</span></span> | <span data-ttu-id="19297-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="19297-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="19297-141">Opcionales</span><span class="sxs-lookup"><span data-stu-id="19297-141">Optional</span></span> | <span data-ttu-id="19297-142">Identificador de idioma usado para la página.</span><span class="sxs-lookup"><span data-stu-id="19297-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="19297-143">Entero no negativo que representa un identificador de idioma válido.</span><span class="sxs-lookup"><span data-stu-id="19297-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="19297-144">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="19297-144">Element Information</span></span>



|  <span data-ttu-id="19297-145">Elemento</span><span class="sxs-lookup"><span data-stu-id="19297-145">Element</span></span>     | <span data-ttu-id="19297-146">Value</span><span class="sxs-lookup"><span data-stu-id="19297-146">Value</span></span>                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="19297-147">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="19297-147">Element type</span></span> | <span data-ttu-id="19297-148">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="19297-148">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="19297-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="19297-149">Namespace</span></span>    | <span data-ttu-id="19297-150">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="19297-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="19297-151">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="19297-151">Schema name</span></span>  | <span data-ttu-id="19297-152">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="19297-152">Journal Reader</span></span>                                                      |



 

 

 



