---
title: Error de tabla de presentación de ARIA
description: Error de tabla de presentación de ARIA
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1ef7cae971e6dc365bd3f8ebe6135561f3ff3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797091"
---
# <a name="aria-presentation-table-error"></a><span data-ttu-id="62085-104">Error de tabla de presentación de ARIA</span><span class="sxs-lookup"><span data-stu-id="62085-104">ARIA Presentation Table Error</span></span>

## <a name="text"></a><span data-ttu-id="62085-105">Texto</span><span class="sxs-lookup"><span data-stu-id="62085-105">Text</span></span>

<span data-ttu-id="62085-106">La tabla usada para el diseño no debe tener el encabezado, el nombre accesible o la información de Resumen definida (**TH**, **Summary**, **Aria-describedby**, **Aria-labelledby**, **Aria-Label**, **title**, **Caption** ).</span><span class="sxs-lookup"><span data-stu-id="62085-106">Table used for layout must not have header, accessible name or summary information defined (**th**, **summary**, **aria-describedby**, **aria-labelledby**, **aria-label**, **title**, **caption** attributes).</span></span>

## <a name="type"></a><span data-ttu-id="62085-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="62085-107">Type</span></span>

<span data-ttu-id="62085-108">Error</span><span class="sxs-lookup"><span data-stu-id="62085-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="62085-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="62085-109">Description</span></span>

<span data-ttu-id="62085-110">Este error se aplica a las etiquetas de la tabla HTML que tienen el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) establecido en "Presentation" o con una tabla que tiene una sola celda (1 x 1 tabla).</span><span class="sxs-lookup"><span data-stu-id="62085-110">This error applies to HTML table tags that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set to "presentation", or with a table that has a single cell (1×1 table).</span></span>

<span data-ttu-id="62085-111">Este error indica que una tabla está marcada únicamente como diseño (tiene `role="presentation"` ), pero también contiene información de accesibilidad como si fuera una tabla de datos, lo que puede resultar confuso para los usuarios del lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="62085-111">This error indicates that a table is marked as layout only (has `role="presentation"`), but it also contains accessibility information as if it was a data table, which can be confusing for screen reader users.</span></span>

<span data-ttu-id="62085-112">Para solucionar este error, determine si la tabla es realmente simplemente una tabla de diseño y, si es así, quite el marcado accesible:</span><span class="sxs-lookup"><span data-stu-id="62085-112">To address this error, determine whether the table actually is just a layout table and, if so, remove the accessible markup:</span></span>

-   <span data-ttu-id="62085-113">Elemento [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) , [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) Attributes.</span><span class="sxs-lookup"><span data-stu-id="62085-113">[**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) element, [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span>
-   <span data-ttu-id="62085-114">los atributos [**Summary**](https://www.bing.com/search?q=**summary**) o [**Aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="62085-114">[**summary**](https://www.bing.com/search?q=**summary**) or [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>
-   <span data-ttu-id="62085-115">Etiquetas [**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) .</span><span class="sxs-lookup"><span data-stu-id="62085-115">[**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags.</span></span>

## <a name="example"></a><span data-ttu-id="62085-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="62085-116">Example</span></span>

![<span data-ttu-id="62085-117">HTML para un elemento de tabla, con atributos como Summary que desencadenan el error de tabla de presentación de Aria mostrado como marcado HTML de tachado</span><span class="sxs-lookup"><span data-stu-id="62085-117">html for a table element, with attributes such as summary that trigger the aria presentation table error shown as struck-out html markup</span></span> ](images/aria-layout-table.png)

## <a name="remarks"></a><span data-ttu-id="62085-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62085-118">Remarks</span></span>

<span data-ttu-id="62085-119">Si determina que una tabla necesita información de accesibilidad, quite el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) o establézcalo en un valor distinto de "Presentation".</span><span class="sxs-lookup"><span data-stu-id="62085-119">If you determine that a table does need accessibility information, remove the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute or set it to a value other than "presentation".</span></span>

 

 




