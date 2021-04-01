---
title: Error de estructura de cuadrícula ARIA
description: Error de estructura de cuadrícula ARIA
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd692c5fb82675b8fdcc6bf88fe35695113c9ef0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797097"
---
# <a name="aria-grid-structure-error"></a><span data-ttu-id="6efa9-104">Error de estructura de cuadrícula ARIA</span><span class="sxs-lookup"><span data-stu-id="6efa9-104">ARIA Grid Structure Error</span></span>

## <a name="text"></a><span data-ttu-id="6efa9-105">Texto</span><span class="sxs-lookup"><span data-stu-id="6efa9-105">Text</span></span>

<span data-ttu-id="6efa9-106">El elemento con el rol de **cuadrícula** no tiene una estructura de cuadrícula correspondiente o un marcado accesible.</span><span class="sxs-lookup"><span data-stu-id="6efa9-106">Element with the **grid** role doesn't have a corresponding grid structure or accessible markup.</span></span>

## <a name="type"></a><span data-ttu-id="6efa9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6efa9-107">Type</span></span>

<span data-ttu-id="6efa9-108">Error</span><span class="sxs-lookup"><span data-stu-id="6efa9-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="6efa9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6efa9-109">Description</span></span>

<span data-ttu-id="6efa9-110">Este error se aplica a los elementos personalizados que tienen el atributo **role** establecido en "Grid".</span><span class="sxs-lookup"><span data-stu-id="6efa9-110">This error applies to custom elements that have the **role** attribute set to "grid".</span></span> <span data-ttu-id="6efa9-111">No se aplica a las etiquetas de tabla HTML que tienen un **rol** implícito de "Grid".</span><span class="sxs-lookup"><span data-stu-id="6efa9-111">It does not apply to HTML table tags that have an implicit **role** of "grid".</span></span>

<span data-ttu-id="6efa9-112">Un elemento que tiene el atributo **role** establecido en "Grid" debe tener la estructura definida por el rol de cuadrícula de aplicaciones de Internet enriquecidas (WAI-ARIA) accesible desde la iniciativa Web Accessibility, incluido el nombre accesible para la cuadrícula y sus subelementos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="6efa9-112">An element that has its **role** attribute set to "grid" must have the structure defined by the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) grid role, including the accessible name for the grid and its header subelements.</span></span>

<span data-ttu-id="6efa9-113">Para corregir este error, revise la implementación para asegurarse de que cumple con la especificación WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="6efa9-113">To fix this error, review your implementation to ensure that it complies with the WAI-ARIA specification.</span></span> <span data-ttu-id="6efa9-114">En concreto, asegúrese de que la estructura cumple las siguientes reglas.</span><span class="sxs-lookup"><span data-stu-id="6efa9-114">Specifically, ensure that the structure meets the following rules.</span></span>

-   <span data-ttu-id="6efa9-115">**Grid** contiene elementos **Row** o **filas** .</span><span class="sxs-lookup"><span data-stu-id="6efa9-115">**grid** contains **row** or **rowgroup** elements.</span></span>
-   <span data-ttu-id="6efa9-116">**filas** contiene elementos **Row** .</span><span class="sxs-lookup"><span data-stu-id="6efa9-116">**rowgroup** contains **row** elements.</span></span>
-   <span data-ttu-id="6efa9-117">los elementos **Row** contienen elementos **ColumnHeader** o **gridcell** o **rowheader** .</span><span class="sxs-lookup"><span data-stu-id="6efa9-117">**row** elements contain **columnheader** or **gridcell** or **rowheader** elements.</span></span>

<span data-ttu-id="6efa9-118">Se debe definir un nombre accesible para los elementos **Grid**, **ColumnHeader**, **gridcell** y **rowheader** mediante uno de los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="6efa9-118">An accessible name should be defined for **grid**, **columnheader**, **gridcell** and **rowheader** elements by using one of the following attributes.</span></span>

-   <span data-ttu-id="6efa9-119">el atributo [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para hacer referencia al elemento que contiene el texto.</span><span class="sxs-lookup"><span data-stu-id="6efa9-119">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute for referencing the element containing text.</span></span>
-   <span data-ttu-id="6efa9-120">[**Aria:**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) atributo de etiqueta para establecer el nombre accesible directamente.</span><span class="sxs-lookup"><span data-stu-id="6efa9-120">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to set the accessible name directly.</span></span>
-   <span data-ttu-id="6efa9-121">[**título**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) para crear una información sobre herramientas que se usa al mismo tiempo que el nombre.</span><span class="sxs-lookup"><span data-stu-id="6efa9-121">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) for creating a tooltip which is at the same time used as a name.</span></span>

 

 




