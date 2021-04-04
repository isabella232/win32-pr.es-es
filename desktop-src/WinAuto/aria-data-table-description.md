---
title: ADVERTENCIA de la tabla de datos ARIA
description: ADVERTENCIA de la tabla de datos ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076244"
---
# <a name="aria-data-table-warning"></a><span data-ttu-id="541c0-104">ADVERTENCIA de la tabla de datos ARIA</span><span class="sxs-lookup"><span data-stu-id="541c0-104">ARIA Data Table Warning</span></span>

## <a name="text"></a><span data-ttu-id="541c0-105">Texto</span><span class="sxs-lookup"><span data-stu-id="541c0-105">Text</span></span>

<span data-ttu-id="541c0-106">La tabla contiene datos, pero no tiene ningún Resumen ni un atributo **Aria-describedby** válido.</span><span class="sxs-lookup"><span data-stu-id="541c0-106">Table contains data but has neither summary nor a valid **aria-describedby** attribute.</span></span>

## <a name="type"></a><span data-ttu-id="541c0-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="541c0-107">Type</span></span>

<span data-ttu-id="541c0-108">Advertencia</span><span class="sxs-lookup"><span data-stu-id="541c0-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="541c0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="541c0-109">Description</span></span>

<span data-ttu-id="541c0-110">Esta advertencia se aplica a las tablas HTML con más de una celda.</span><span class="sxs-lookup"><span data-stu-id="541c0-110">This warning applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="541c0-111">No se aplica a las tablas con `role="presentation"` , ya que se consideran tablas de diseño.</span><span class="sxs-lookup"><span data-stu-id="541c0-111">It does not apply to tables with `role="presentation"` since these are considered to be layout tables.</span></span>

<span data-ttu-id="541c0-112">Esta advertencia indica que la tabla se identifica como una tabla de datos, pero no tiene definida una descripción accesible.</span><span class="sxs-lookup"><span data-stu-id="541c0-112">This warning indicates that the table is identified as a data table but it doesn’t have an accessible description defined.</span></span>

> [!Note]  
> <span data-ttu-id="541c0-113">No es necesario que todas las tablas de datos tengan una descripción accesible.</span><span class="sxs-lookup"><span data-stu-id="541c0-113">Not all data tables are required to have an accessible description.</span></span> <span data-ttu-id="541c0-114">Debe definir una descripción accesible si los usuarios necesitan más información para entender la estructura y el contenido de la tabla de datos.</span><span class="sxs-lookup"><span data-stu-id="541c0-114">You should define an accessible description if users need more information to understand the data table structure and content.</span></span>

 

<span data-ttu-id="541c0-115">Para solucionar esta advertencia, defina una descripción accesible de tabla mediante el atributo Summary o el atributo **Aria-describedby** .</span><span class="sxs-lookup"><span data-stu-id="541c0-115">To address this warning, define a table accessible description by using the summary attribute or the **aria-describedby** attribute.</span></span>

## <a name="example"></a><span data-ttu-id="541c0-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="541c0-116">Example</span></span>


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




