---
title: Seleccionar objetos secundarios
description: Los clientes llaman al método IAccessible accSelect para modificar la selección o el foco del teclado entre los elementos secundarios de un objeto. Las constantes SELFLAG especificadas con la llamada definen la operación que se va a realizar.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356831"
---
# <a name="selecting-child-objects"></a><span data-ttu-id="aaa2f-104">Seleccionar objetos secundarios</span><span class="sxs-lookup"><span data-stu-id="aaa2f-104">Selecting Child Objects</span></span>

<span data-ttu-id="aaa2f-105">Los clientes llaman al método [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) para modificar la selección o el foco del teclado entre los elementos secundarios de un objeto.</span><span class="sxs-lookup"><span data-stu-id="aaa2f-105">Clients call the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method to modify selection or keyboard focus among the children in an object.</span></span> <span data-ttu-id="aaa2f-106">Las [constantes SELFLAG](selflag.md) especificadas con la llamada definen la operación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="aaa2f-106">The [SELFLAG Constants](selflag.md) specified with the call define the operation to perform.</span></span>

<span data-ttu-id="aaa2f-107">Si se llama a [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) con la marca [**\_ TAKEFOCUS de SELFLAG**](selflag.md) en un objeto secundario que tiene un **hWnd**, la marca solo surte efecto si el elemento primario del objeto tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="aaa2f-107">If [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) is called with the [**SELFLAG\_TAKEFOCUS**](selflag.md) flag on a child object that has an **HWND**, the flag takes effect only if the object's parent has the focus.</span></span>

## <a name="performing-complex-selection-operations"></a><span data-ttu-id="aaa2f-108">Realización de operaciones de selección complejas</span><span class="sxs-lookup"><span data-stu-id="aaa2f-108">Performing Complex Selection Operations</span></span>

<span data-ttu-id="aaa2f-109">A continuación se describen los valores de SELFLAG que se especifican al llamar a [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) para realizar operaciones de selección complejas.</span><span class="sxs-lookup"><span data-stu-id="aaa2f-109">The following describes which SELFLAG values to specify when calling [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) to perform complex selection operations.</span></span>

<span data-ttu-id="aaa2f-110">**Para simular un clic**</span><span class="sxs-lookup"><span data-stu-id="aaa2f-110">**To simulate a click**</span></span>

-   <span data-ttu-id="aaa2f-111">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="aaa2f-111">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_TAKESELECTION**](selflag.md)</span></span>

<span data-ttu-id="aaa2f-112">**Para seleccionar un elemento de destino simulando CTRL + clic**</span><span class="sxs-lookup"><span data-stu-id="aaa2f-112">**To select a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="aaa2f-113">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ ADDSELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="aaa2f-113">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_ADDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="aaa2f-114">**Para cancelar la selección de un elemento de destino simulando CTRL + clic**</span><span class="sxs-lookup"><span data-stu-id="aaa2f-114">**To cancel selection of a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="aaa2f-115">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="aaa2f-115">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_REMOVESELECTION**](selflag.md)</span></span>

<span data-ttu-id="aaa2f-116">**Para simular Mayús + clic**</span><span class="sxs-lookup"><span data-stu-id="aaa2f-116">**To simulate SHIFT + click**</span></span>

-   <span data-ttu-id="aaa2f-117">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="aaa2f-117">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_EXTENDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="aaa2f-118">**Para seleccionar un intervalo de objetos y colocar el foco en el último objeto**</span><span class="sxs-lookup"><span data-stu-id="aaa2f-118">**To select a range of objects and put focus on the last object**</span></span>

1.  <span data-ttu-id="aaa2f-119">Especifique [**SELFLAG \_ TAKEFOCUS**](selflag.md) en el objeto de inicio para establecer el delimitador de selección.</span><span class="sxs-lookup"><span data-stu-id="aaa2f-119">Specify [**SELFLAG\_TAKEFOCUS**](selflag.md) on the starting object to set the selection anchor.</span></span>
2.  <span data-ttu-id="aaa2f-120">Vuelva a llamar a [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) y especifique [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) en el último objeto.</span><span class="sxs-lookup"><span data-stu-id="aaa2f-120">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_EXTENDSELECTION**](selflag.md) \| [**SELFLAG\_TAKEFOCUS**](selflag.md) on the last object.</span></span>

<span data-ttu-id="aaa2f-121">**Para anular la selección de todos los objetos**</span><span class="sxs-lookup"><span data-stu-id="aaa2f-121">**To deselect all objects**</span></span>

1.  <span data-ttu-id="aaa2f-122">Especifique [**SELFLAG \_ TAKESELECTION**](selflag.md) en cualquier objeto.</span><span class="sxs-lookup"><span data-stu-id="aaa2f-122">Specify [**SELFLAG\_TAKESELECTION**](selflag.md) on any object.</span></span> <span data-ttu-id="aaa2f-123">Esta marca anula la selección de todos los objetos seleccionados excepto el que acaba de seleccionar.</span><span class="sxs-lookup"><span data-stu-id="aaa2f-123">This flag deselects all selected objects except the one just selected.</span></span>
2.  <span data-ttu-id="aaa2f-124">Vuelva a llamar a [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) y especifique [**SELFLAG \_ REMOVESELECTION**](selflag.md) en el objeto restante.</span><span class="sxs-lookup"><span data-stu-id="aaa2f-124">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_REMOVESELECTION**](selflag.md) on the remaining object.</span></span>

 

 




