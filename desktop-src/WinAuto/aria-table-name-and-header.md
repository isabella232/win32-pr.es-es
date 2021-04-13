---
title: Error de la tabla de datos ARIA
description: Error de la tabla de datos ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286f88a0b3a0d962fd6ac45581f94bc351cb507
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421533"
---
# <a name="aria-data-table-error"></a><span data-ttu-id="86578-104">Error de la tabla de datos ARIA</span><span class="sxs-lookup"><span data-stu-id="86578-104">ARIA Data Table Error</span></span>

## <a name="text"></a><span data-ttu-id="86578-105">Texto</span><span class="sxs-lookup"><span data-stu-id="86578-105">Text</span></span>

<span data-ttu-id="86578-106">La tabla contiene datos, pero no tiene marcado accesible definido a través de los elementos **Aria-Label**, **Aria-labelledby**, **title**, **Caption** o **TH** .</span><span class="sxs-lookup"><span data-stu-id="86578-106">Table contains data but doesn't have accessible markup defined though **aria-label**, **aria-labelledby**, **title**, **caption** or **th** elements.</span></span>

## <a name="type"></a><span data-ttu-id="86578-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="86578-107">Type</span></span>

<span data-ttu-id="86578-108">Error</span><span class="sxs-lookup"><span data-stu-id="86578-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="86578-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="86578-109">Description</span></span>

<span data-ttu-id="86578-110">Este error se aplica a las tablas HTML con más de una celda.</span><span class="sxs-lookup"><span data-stu-id="86578-110">This error applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="86578-111">Este error no se aplica a las tablas con `role="presentation"` porque se consideran tablas de diseño.</span><span class="sxs-lookup"><span data-stu-id="86578-111">This error does not apply to tables with `role="presentation"` because these are considered to be layout tables.</span></span>

<span data-ttu-id="86578-112">Este error indica que una tabla de datos no tiene un nombre accesible o información de encabezado.</span><span class="sxs-lookup"><span data-stu-id="86578-112">This error indicates that a data table doesn’t have an accessible name or header information.</span></span>

<span data-ttu-id="86578-113">Para corregir este error, defina un nombre accesible mediante la etiqueta de [**título**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) o los atributos [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) .</span><span class="sxs-lookup"><span data-stu-id="86578-113">To fix this error, define an accessible name by using the [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) tag, or the [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span> <span data-ttu-id="86578-114">Si falta información de encabezado en la tabla, use etiquetas [**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) para marcar las celdas de encabezado.</span><span class="sxs-lookup"><span data-stu-id="86578-114">If the table is missing header information, use [**THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags to mark header cells.</span></span>

## <a name="example"></a><span data-ttu-id="86578-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86578-115">Example</span></span>


```HTML
<!-- Data tables must contain an accessibile name and header information. -->
<table>
  <caption>ARIA Examples</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      ...
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Accessible tables</td>
      <td>This example illustrates how to make data tables accessible using ARIA</td>
      ...
    </tr>
  </tbody>
</table>
```



 

 




