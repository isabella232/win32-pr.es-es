---
description: Elemento de nivel superior de un archivo XML de nota de diario.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432177"
---
# <a name="journaldocument-element"></a><span data-ttu-id="4ec2f-103">Elemento JournalDocument</span><span class="sxs-lookup"><span data-stu-id="4ec2f-103">JournalDocument Element</span></span>

<span data-ttu-id="4ec2f-104">Elemento de nivel superior de un archivo XML de nota de diario.</span><span class="sxs-lookup"><span data-stu-id="4ec2f-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="4ec2f-105">Definición</span><span class="sxs-lookup"><span data-stu-id="4ec2f-105">Definition</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="4ec2f-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="4ec2f-106">Parent Elements</span></span>

<span data-ttu-id="4ec2f-107">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4ec2f-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4ec2f-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4ec2f-108">Child Elements</span></span>

[<span data-ttu-id="4ec2f-109">**Diseño de fondo**</span><span class="sxs-lookup"><span data-stu-id="4ec2f-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="4ec2f-110">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="4ec2f-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="4ec2f-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="4ec2f-111">Attributes</span></span>



| <span data-ttu-id="4ec2f-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="4ec2f-112">Attribute</span></span>             | <span data-ttu-id="4ec2f-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="4ec2f-113">Type</span></span>                      | <span data-ttu-id="4ec2f-114">Requerido</span><span class="sxs-lookup"><span data-stu-id="4ec2f-114">Required</span></span> | <span data-ttu-id="4ec2f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ec2f-115">Description</span></span>                                                      | <span data-ttu-id="4ec2f-116">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="4ec2f-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="4ec2f-117">**Versión**</span><span class="sxs-lookup"><span data-stu-id="4ec2f-117">**Version**</span></span>           | <span data-ttu-id="4ec2f-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="4ec2f-118">**xs:string**</span></span>             | <span data-ttu-id="4ec2f-119">Requerido</span><span class="sxs-lookup"><span data-stu-id="4ec2f-119">Required</span></span> | <span data-ttu-id="4ec2f-120">La versión del documento Journal representada en el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="4ec2f-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="4ec2f-121">1.0</span><span class="sxs-lookup"><span data-stu-id="4ec2f-121">1.0</span></span>                       |
| <span data-ttu-id="4ec2f-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="4ec2f-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="4ec2f-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="4ec2f-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="4ec2f-124">Requerido</span><span class="sxs-lookup"><span data-stu-id="4ec2f-124">Required</span></span> | <span data-ttu-id="4ec2f-125">Ancho predeterminado de la página para el documento Journal.</span><span class="sxs-lookup"><span data-stu-id="4ec2f-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="4ec2f-126">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="4ec2f-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="4ec2f-127">**DefaultPageHeight**</span><span class="sxs-lookup"><span data-stu-id="4ec2f-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="4ec2f-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="4ec2f-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="4ec2f-129">Requerido</span><span class="sxs-lookup"><span data-stu-id="4ec2f-129">Required</span></span> | <span data-ttu-id="4ec2f-130">Alto predeterminado de la página para el documento Journal.</span><span class="sxs-lookup"><span data-stu-id="4ec2f-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="4ec2f-131">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="4ec2f-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="4ec2f-132">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4ec2f-132">Element Information</span></span>



|  <span data-ttu-id="4ec2f-133">Elemento</span><span class="sxs-lookup"><span data-stu-id="4ec2f-133">Element</span></span>     | <span data-ttu-id="4ec2f-134">Value</span><span class="sxs-lookup"><span data-stu-id="4ec2f-134">Value</span></span>                                                     |
|--------------|--------------------------------------------|
| <span data-ttu-id="4ec2f-135">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4ec2f-135">Element type</span></span> | <span data-ttu-id="4ec2f-136">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="4ec2f-136">**JournalDocument**</span></span>                        |
| <span data-ttu-id="4ec2f-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4ec2f-137">Namespace</span></span>    | <span data-ttu-id="4ec2f-138">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="4ec2f-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="4ec2f-139">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="4ec2f-139">Schema name</span></span>  | <span data-ttu-id="4ec2f-140">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="4ec2f-140">Journal Reader</span></span>                             |



 

 

 



