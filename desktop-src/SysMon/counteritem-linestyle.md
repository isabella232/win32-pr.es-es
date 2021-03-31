---
title: Propiedad de contraelemento. LineStyle
description: Recupera o establece el estilo de línea que se usa para representar el valor del contador.
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- Propiedad LineStyle SysMon
- Propiedad LineStyle SysMon, clase de contraelemento
- Clase de contraelemento SysMon, propiedad LineStyle
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff1dd78c6fd65d72c28fe8f13f7bbf5603c75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996353"
---
# <a name="counteritemlinestyle-property"></a><span data-ttu-id="f4f8b-106">Propiedad de contraelemento. LineStyle</span><span class="sxs-lookup"><span data-stu-id="f4f8b-106">CounterItem.LineStyle property</span></span>

<span data-ttu-id="f4f8b-107">Recupera o establece el estilo de línea que se usa para representar el valor del contador.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-107">Retrieves or sets the line style used to graph the counter value.</span></span>

<span data-ttu-id="f4f8b-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f8b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4f8b-109">Syntax</span></span>


```VB
Property LineStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="f4f8b-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f4f8b-110">Property value</span></span>

<span data-ttu-id="f4f8b-111">Estilo de línea que se usa para representar el valor del contador.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-111">The line style used to graph the counter value.</span></span> <span data-ttu-id="f4f8b-112">Los valores corresponden a las constantes del sistema que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-112">The values correspond to system constants shown in the following table.</span></span>



| <span data-ttu-id="f4f8b-113">Value</span><span class="sxs-lookup"><span data-stu-id="f4f8b-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="f4f8b-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f4f8b-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <span data-ttu-id="f4f8b-115"><dt>**System. Drawing. Drawing2D. DashStyle. Solid**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f4f8b-115"><dt>**System.Drawing.Drawing2D.DashStyle.Solid**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="f4f8b-116">Línea continua.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-116">Solid line.</span></span> <span data-ttu-id="f4f8b-117">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-117">This is the default value.</span></span><br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <span data-ttu-id="f4f8b-118"><dt>**System. Drawing. Drawing2D. DashStyle. Dash**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f4f8b-118"><dt>**System.Drawing.Drawing2D.DashStyle.Dash**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="f4f8b-119">Línea de puntos con segmentos largos y espacios estrechos.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-119">Dotted line with long segments and narrow spaces.</span></span><br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <span data-ttu-id="f4f8b-120"><dt>**System. Drawing. Drawing2D. DashStyle. dot**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f4f8b-120"><dt>**System.Drawing.Drawing2D.DashStyle.Dot**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="f4f8b-121">Línea de puntos con segmentos uniformes y espacios.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-121">Dotted line with uniform segments and spaces.</span></span><br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <span data-ttu-id="f4f8b-122"><dt>**System. Drawing. Drawing2D. DashStyle. DashDot**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f4f8b-122"><dt>**System.Drawing.Drawing2D.DashStyle.DashDot**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="f4f8b-123">Línea de puntos con segmentos cortos y largos alternos.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-123">Dotted line with alternating short and long segments.</span></span><br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <span data-ttu-id="f4f8b-124"><dt>**System. Drawing. Drawing2D. DashStyle. DashDotDot**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f4f8b-124"><dt>**System.Drawing.Drawing2D.DashStyle.DashDotDot**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="f4f8b-125">Línea de puntos con guiones alternos y puntos dobles.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-125">Dotted line with alternating dashes and double dots.</span></span><br/>  |



 

## <a name="exceptions"></a><span data-ttu-id="f4f8b-126">Excepciones</span><span class="sxs-lookup"><span data-stu-id="f4f8b-126">Exceptions</span></span>



| <span data-ttu-id="f4f8b-127">Tipo de excepción</span><span class="sxs-lookup"><span data-stu-id="f4f8b-127">Exception type</span></span>               | <span data-ttu-id="f4f8b-128">Condición</span><span class="sxs-lookup"><span data-stu-id="f4f8b-128">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="f4f8b-129">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="f4f8b-129">**System.ArgumentException**</span></span> | <span data-ttu-id="f4f8b-130">El estilo de línea especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-130">The specified line style is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f4f8b-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4f8b-131">Remarks</span></span>

<span data-ttu-id="f4f8b-132">Para especificar un valor distinto de DashStyle. [**Solid, debe**](counteritem-width.md) establecerse un valor en 1.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-132">To specify a value other than DashStyle.Solid, [**CounterItem.Width**](counteritem-width.md) must be set to 1.</span></span> <span data-ttu-id="f4f8b-133">Si el ancho es mayor que 1, SYSMON omite el estilo de línea especificado y usa DashStyle. Solid.</span><span class="sxs-lookup"><span data-stu-id="f4f8b-133">If the width is greater than 1, SYSMON ignores the specified line style and uses DashStyle.Solid.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f8b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4f8b-134">Requirements</span></span>



| <span data-ttu-id="f4f8b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4f8b-135">Requirement</span></span> | <span data-ttu-id="f4f8b-136">Value</span><span class="sxs-lookup"><span data-stu-id="f4f8b-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f8b-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4f8b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f4f8b-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f4f8b-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f4f8b-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4f8b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f4f8b-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f4f8b-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4f8b-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f4f8b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4f8b-142"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f4f8b-142"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f8b-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4f8b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f8b-144">**Elemento de**</span><span class="sxs-lookup"><span data-stu-id="f4f8b-144">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





