---
title: Propiedad SystemMonitor. BorderStyle
description: Recupera o establece el estilo de borde del control.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- Propiedad BorderStyle SysMon
- Propiedad BorderStyle SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad BorderStyle
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905194"
---
# <a name="systemmonitorborderstyle-property"></a><span data-ttu-id="be8ea-106">Propiedad SystemMonitor. BorderStyle</span><span class="sxs-lookup"><span data-stu-id="be8ea-106">SystemMonitor.BorderStyle property</span></span>

<span data-ttu-id="be8ea-107">Recupera o establece el estilo de borde del control.</span><span class="sxs-lookup"><span data-stu-id="be8ea-107">Retrieves or sets the border style of the control.</span></span>

<span data-ttu-id="be8ea-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="be8ea-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8ea-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be8ea-109">Syntax</span></span>


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="be8ea-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="be8ea-110">Property value</span></span>

<span data-ttu-id="be8ea-111">Estilo de borde del control.</span><span class="sxs-lookup"><span data-stu-id="be8ea-111">Border style of the control.</span></span>

<span data-ttu-id="be8ea-112">Puede establecer esta propiedad en uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="be8ea-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="be8ea-113">Value</span><span class="sxs-lookup"><span data-stu-id="be8ea-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="be8ea-114">Significado</span><span class="sxs-lookup"><span data-stu-id="be8ea-114">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <span data-ttu-id="be8ea-115"><dt>**System. Windows. Forms. FormBorderStyle. VbBSNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="be8ea-115"><dt>**System.Windows.Forms.FormBorderStyle.VbBSNone**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="be8ea-116">Sin borde.</span><span class="sxs-lookup"><span data-stu-id="be8ea-116">No border.</span></span> <span data-ttu-id="be8ea-117">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="be8ea-117">This is the default value.</span></span><br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <span data-ttu-id="be8ea-118"><dt>**System. Windows. Forms. FormBorderStyle. VbFixedSingle**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="be8ea-118"><dt>**System.Windows.Forms.FormBorderStyle.VbFixedSingle**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="be8ea-119">Borde fijo único.</span><span class="sxs-lookup"><span data-stu-id="be8ea-119">Fixed, single border.</span></span><br/>                 |



 

## <a name="exceptions"></a><span data-ttu-id="be8ea-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="be8ea-120">Exceptions</span></span>



| <span data-ttu-id="be8ea-121">Tipo de excepción</span><span class="sxs-lookup"><span data-stu-id="be8ea-121">Exception type</span></span>               | <span data-ttu-id="be8ea-122">Condición</span><span class="sxs-lookup"><span data-stu-id="be8ea-122">Condition</span></span>                                |
|------------------------------|------------------------------------------|
| <span data-ttu-id="be8ea-123">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="be8ea-123">**System.ArgumentException**</span></span> | <span data-ttu-id="be8ea-124">El estilo de borde especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="be8ea-124">The specified border style is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="be8ea-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be8ea-125">Requirements</span></span>



| <span data-ttu-id="be8ea-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="be8ea-126">Requirement</span></span> | <span data-ttu-id="be8ea-127">Value</span><span class="sxs-lookup"><span data-stu-id="be8ea-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be8ea-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be8ea-128">Minimum supported client</span></span><br/> | <span data-ttu-id="be8ea-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="be8ea-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="be8ea-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be8ea-130">Minimum supported server</span></span><br/> | <span data-ttu-id="be8ea-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="be8ea-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be8ea-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be8ea-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be8ea-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="be8ea-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be8ea-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="be8ea-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8ea-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="be8ea-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





