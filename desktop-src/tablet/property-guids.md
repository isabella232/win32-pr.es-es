---
description: Los reconocedores de Microsoft usan los siguientes GUID.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: GUID de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156873"
---
# <a name="property-guids"></a><span data-ttu-id="f1297-103">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="f1297-103">Property GUIDs</span></span>

<span data-ttu-id="f1297-104">Los reconocedores de Microsoft usan los siguientes GUID.</span><span class="sxs-lookup"><span data-stu-id="f1297-104">The Microsoft recognizers use the following GUIDs.</span></span> <span data-ttu-id="f1297-105">Siempre que sea posible, las aplicaciones deben usar estos GUID.</span><span class="sxs-lookup"><span data-stu-id="f1297-105">Whenever possible, applications should use these GUIDs.</span></span> <span data-ttu-id="f1297-106">Sin embargo, se espera y se recomienda que otros reconocedores usen GUID adicionales para las propiedades que no son compatibles con los reconocedores de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f1297-106">However, it is expected and encouraged that other recognizers will use additional GUIDs for properties that are not supported by the Microsoft recognizers.</span></span>

<span data-ttu-id="f1297-107">Todas las funciones de propiedad se han desarrollado con la comprensión de que otros reconocedores pueden extender la lista de GUID.</span><span class="sxs-lookup"><span data-stu-id="f1297-107">All property functions have been developed with the understanding that the list of GUIDs may be extended by other recognizers.</span></span> <span data-ttu-id="f1297-108">Estas funciones de propiedad incluyen:</span><span class="sxs-lookup"><span data-stu-id="f1297-108">These property functions include:</span></span>

-   [<span data-ttu-id="f1297-109">**GetContextPropertyList función)**</span><span class="sxs-lookup"><span data-stu-id="f1297-109">**GetContextPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [<span data-ttu-id="f1297-110">**GetContextPropertyValue función)**</span><span class="sxs-lookup"><span data-stu-id="f1297-110">**GetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [<span data-ttu-id="f1297-111">**GetResultPropertyList función)**</span><span class="sxs-lookup"><span data-stu-id="f1297-111">**GetResultPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [<span data-ttu-id="f1297-112">**SetContextPropertyValue función)**</span><span class="sxs-lookup"><span data-stu-id="f1297-112">**SetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

<span data-ttu-id="f1297-113">En la tabla siguiente se enumeran los GUID de propiedades de Tablet PC definidos en msinkaut. h (instalado en c: \\ archivos de programa \\ Microsoft Tablet PC Platform SDK \\ incluir de forma predeterminada).</span><span class="sxs-lookup"><span data-stu-id="f1297-113">The following table lists Tablet PC property GUIDs defined in msinkaut.h (installed in c:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include by default).</span></span>



| <span data-ttu-id="f1297-114">GUID</span><span class="sxs-lookup"><span data-stu-id="f1297-114">GUID</span></span>                                                  | <span data-ttu-id="f1297-115">Definición</span><span class="sxs-lookup"><span data-stu-id="f1297-115">Definition</span></span>                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1297-116">INKRECOGNITIONPROPERTY \_ BOXNUMBER</span><span class="sxs-lookup"><span data-stu-id="f1297-116">INKRECOGNITIONPROPERTY\_BOXNUMBER</span></span><br/>          | <span data-ttu-id="f1297-117">Índice de cuadro alternativo del reconocedor en modo de cuadro</span><span class="sxs-lookup"><span data-stu-id="f1297-117">The recognizer alternate box index in box mode</span></span><br/>                                    |
| <span data-ttu-id="f1297-118">INKRECOGNITIONPROPERTY \_ LINENUMBER</span><span class="sxs-lookup"><span data-stu-id="f1297-118">INKRECOGNITIONPROPERTY\_LINENUMBER</span></span><br/>         | <span data-ttu-id="f1297-119">El número de línea</span><span class="sxs-lookup"><span data-stu-id="f1297-119">The line number</span></span><br/>                                                                   |
| <span data-ttu-id="f1297-120">\_segmentación INKRECOGNITIONPROPERTY</span><span class="sxs-lookup"><span data-stu-id="f1297-120">INKRECOGNITIONPROPERTY\_SEGMENTATION</span></span><br/>       | <span data-ttu-id="f1297-121">Cómo el reconocedor segmenta las palabras y los caracteres</span><span class="sxs-lookup"><span data-stu-id="f1297-121">How the recognizer segments words and characters</span></span><br/>                                  |
| <span data-ttu-id="f1297-122">INKRECOGNITIONPROPERTY \_ Hotpoint</span><span class="sxs-lookup"><span data-stu-id="f1297-122">INKRECOGNITIONPROPERTY\_HOTPOINT</span></span><br/>           | <span data-ttu-id="f1297-123">El punto de acceso directo del gesto</span><span class="sxs-lookup"><span data-stu-id="f1297-123">The gesture hot point</span></span><br/>                                                             |
| <span data-ttu-id="f1297-124">INKRECOGNITIONPROPERTY \_ MAXIMUMSTROKECOUNT</span><span class="sxs-lookup"><span data-stu-id="f1297-124">INKRECOGNITIONPROPERTY\_MAXIMUMSTROKECOUNT</span></span><br/> | <span data-ttu-id="f1297-125">Número máximo de trazos para un segmento</span><span class="sxs-lookup"><span data-stu-id="f1297-125">Maximum number of strokes for a segment</span></span><br/>                                           |
| <span data-ttu-id="f1297-126">INKRECOGNITIONPROPERTY \_ POINTSPERINCH</span><span class="sxs-lookup"><span data-stu-id="f1297-126">INKRECOGNITIONPROPERTY\_POINTSPERINCH</span></span><br/>      | <span data-ttu-id="f1297-127">La métrica de puntos por pulgada</span><span class="sxs-lookup"><span data-stu-id="f1297-127">The points-per-inch metric</span></span><br/>                                                        |
| <span data-ttu-id="f1297-128">INKRECOGNITIONPROPERTY \_ CONFIDENCELEVEL</span><span class="sxs-lookup"><span data-stu-id="f1297-128">INKRECOGNITIONPROPERTY\_CONFIDENCELEVEL</span></span><br/>    | <span data-ttu-id="f1297-129">[**Confianza \_**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) Enumeración de nivel</span><span class="sxs-lookup"><span data-stu-id="f1297-129">[**CONFIDENCE\_LEVEL**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) enumeration</span></span><br/>                         |
| <span data-ttu-id="f1297-130">INKRECOGNITIONPROPERTY \_ LINEMETRICS</span><span class="sxs-lookup"><span data-stu-id="f1297-130">INKRECOGNITIONPROPERTY\_LINEMETRICS</span></span><br/>        | <span data-ttu-id="f1297-131">Información sobre el cálculo de la línea base, la línea media o ambas, que se usa en el Lattice</span><span class="sxs-lookup"><span data-stu-id="f1297-131">Information for computing baseline, midline, or both, that is used in the lattice</span></span><br/> |



 

 

 




