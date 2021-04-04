---
title: Propiedad de contraelemento. color
description: Recupera o establece el color utilizado para representar el valor del contador en el gráfico.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Propiedad de color SysMon
- Propiedad color SysMon, clase de contraelemento
- Clase de contraelemento SysMon, propiedad de color
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ada0a2266c4cf53e9706f1330e2336e6a38386b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802588"
---
# <a name="counteritemcolor-property"></a><span data-ttu-id="ace57-106">Propiedad de contraelemento. color</span><span class="sxs-lookup"><span data-stu-id="ace57-106">CounterItem.Color property</span></span>

<span data-ttu-id="ace57-107">Recupera o establece el color utilizado para representar el valor del contador en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="ace57-107">Retrieves or sets the color used to graph the counter value.</span></span>

<span data-ttu-id="ace57-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ace57-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace57-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ace57-109">Syntax</span></span>


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a><span data-ttu-id="ace57-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ace57-110">Property value</span></span>

<span data-ttu-id="ace57-111">Color que se usa para representar el valor del contador.</span><span class="sxs-lookup"><span data-stu-id="ace57-111">Color used to graph the counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ace57-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ace57-112">Remarks</span></span>

<span data-ttu-id="ace57-113">Si no especifica el color que se va a usar, SYSMON selecciona los colores de los primeros dieciséis contadores.</span><span class="sxs-lookup"><span data-stu-id="ace57-113">If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="ace57-114">Si especifica más de dieciséis contadores, SYSMON volverá a usar los mismos colores de los primeros dieciséis contadores.</span><span class="sxs-lookup"><span data-stu-id="ace57-114">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="ace57-115">Para ayudar a distinguir los contadores entre sí, SYSMON cambia el [**estilo de línea**](counteritem-linestyle.md) usado para cada múltiplo de dieciséis contadores hasta los primeros 80 contadores.</span><span class="sxs-lookup"><span data-stu-id="ace57-115">To help distinguish the counters from one another, SYSMON changes the [**line style**](counteritem-linestyle.md) used for each multiple of sixteen counters up to the first 80 counters.</span></span> <span data-ttu-id="ace57-116">Por ejemplo, los primeros dieciséis contadores usan un estilo de línea continua, los siguientes dieciséis usan un estilo de línea de guiones, etc.</span><span class="sxs-lookup"><span data-stu-id="ace57-116">For example, the first sixteen counters use a solid line style, the next sixteen use a dash line style, and so on.</span></span> <span data-ttu-id="ace57-117">SYSMON establece el [**ancho de línea**](counteritem-width.md) en 2 para los contadores 81-96 y en 3 para los contadores 96-112.</span><span class="sxs-lookup"><span data-stu-id="ace57-117">SYSMON then sets the [**line width**](counteritem-width.md) to 2 for counters 81 - 96 and to 3 for counters 96 - 112.</span></span> <span data-ttu-id="ace57-118">Si la colección contiene más de 112 contadores, los contadores contendrán los valores de color, estilo de línea y ancho duplicados.</span><span class="sxs-lookup"><span data-stu-id="ace57-118">If the collection contains more than 112 counters, the counters will contain duplicate color, line style, and width values.</span></span>

<span data-ttu-id="ace57-119">**Antes de Windows Vista:** Si no especifica el color que se va a usar, SYSMON selecciona los colores de los primeros dieciséis contadores.</span><span class="sxs-lookup"><span data-stu-id="ace57-119">**Prior to Windows Vista:** If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="ace57-120">Si especifica más de dieciséis contadores, SYSMON volverá a usar los mismos colores de los primeros dieciséis contadores.</span><span class="sxs-lookup"><span data-stu-id="ace57-120">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="ace57-121">Para ayudar a distinguir los contadores entre sí, SYSMON aumenta el [**ancho de línea**](counteritem-width.md) de los tres primeros contadores que reciben la misma asignación de color.</span><span class="sxs-lookup"><span data-stu-id="ace57-121">To help distinguish the counters from one another, SYSMON increases the [**line width**](counteritem-width.md) of the first three counters that receive the same color assignment.</span></span> <span data-ttu-id="ace57-122">Si más de tres contadores usan el mismo color, SYSMON elige aleatoriamente el ancho de línea que se va a usar para el contador.</span><span class="sxs-lookup"><span data-stu-id="ace57-122">If more than three counters use the same color, SYSMON randomly chooses the line width to use for the counter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace57-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ace57-123">Requirements</span></span>



| <span data-ttu-id="ace57-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ace57-124">Requirement</span></span> | <span data-ttu-id="ace57-125">Value</span><span class="sxs-lookup"><span data-stu-id="ace57-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ace57-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ace57-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ace57-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ace57-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ace57-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ace57-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ace57-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ace57-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ace57-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ace57-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ace57-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ace57-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ace57-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ace57-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace57-133">**Elemento de**</span><span class="sxs-lookup"><span data-stu-id="ace57-133">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





