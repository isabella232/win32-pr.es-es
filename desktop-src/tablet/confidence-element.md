---
description: Contiene la clasificación de confianza devuelta por Journal Ink Analyzer para InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Elemento Confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cef4869776a6cafc4e6ef4758649b918e0b5988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153753"
---
# <a name="confidence-element"></a><span data-ttu-id="8c073-103">Elemento Confidence</span><span class="sxs-lookup"><span data-stu-id="8c073-103">Confidence Element</span></span>

<span data-ttu-id="8c073-104">Contiene la clasificación de confianza devuelta por Journal Ink Analyzer para [**InkWord**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="8c073-104">Contains the confidence rating returned by the Journal ink analyzer for the [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="8c073-105">Definición</span><span class="sxs-lookup"><span data-stu-id="8c073-105">Definition</span></span>

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="8c073-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8c073-106">Parent Elements</span></span>

[<span data-ttu-id="8c073-107">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="8c073-107">**InkWord**</span></span>](inkword-element.md)

## <a name="values"></a><span data-ttu-id="8c073-108">Valores</span><span class="sxs-lookup"><span data-stu-id="8c073-108">Values</span></span>

<span data-ttu-id="8c073-109">Los valores válidos para este campo son "0", "1" y "2".</span><span class="sxs-lookup"><span data-stu-id="8c073-109">Valid values for this field include "0", "1", and "2".</span></span> <span data-ttu-id="8c073-110">0 indica una confianza alta, 1 indica confianza intermedia y 2 indica una confianza deficiente.</span><span class="sxs-lookup"><span data-stu-id="8c073-110">0 indicates Strong confidence, 1 indicates Intermediate confidence, and 2 indicates Poor confidence.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8c073-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8c073-111">Child Elements</span></span>

<span data-ttu-id="8c073-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8c073-112">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="8c073-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="8c073-113">Attributes</span></span>

<span data-ttu-id="8c073-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8c073-114">None.</span></span>

## <a name="element-information"></a><span data-ttu-id="8c073-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8c073-115">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="8c073-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="8c073-116">Element type</span></span> | <span data-ttu-id="8c073-117">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="8c073-117">**xs:string**</span></span>                              |
| <span data-ttu-id="8c073-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c073-118">Namespace</span></span>    | <span data-ttu-id="8c073-119">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="8c073-119">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="8c073-120">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="8c073-120">Schema name</span></span>  | <span data-ttu-id="8c073-121">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="8c073-121">Journal Reader</span></span>                             |



 

 

 



