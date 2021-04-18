---
title: SystemMonitor. Appearance (propiedad)
description: Recupera o establece la apariencia del control para incluir u omitir los efectos de visualización tridimensionales.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Propiedad de apariencia SysMon
- Propiedad Appearance SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad Appearance
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200c66f83a47f15421480967e8ea1ae9509b13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665925"
---
# <a name="systemmonitorappearance-property"></a><span data-ttu-id="2de45-106">SystemMonitor. Appearance (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2de45-106">SystemMonitor.Appearance property</span></span>

<span data-ttu-id="2de45-107">Recupera o establece la apariencia del control para incluir u omitir los efectos de visualización tridimensionales.</span><span class="sxs-lookup"><span data-stu-id="2de45-107">Retrieves or sets the control's appearance to include or omit three-dimensional display effects.</span></span>

<span data-ttu-id="2de45-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2de45-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de45-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2de45-109">Syntax</span></span>


```VB
Property Appearance As Long
```



## <a name="property-value"></a><span data-ttu-id="2de45-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2de45-110">Property value</span></span>

<span data-ttu-id="2de45-111">Valor de apariencia que determina si el control se dibuja con efectos tridimensionales.</span><span class="sxs-lookup"><span data-stu-id="2de45-111">Appearance value that determines if the control is painted with three-dimensional effects.</span></span>

<span data-ttu-id="2de45-112">Puede establecer esta propiedad en uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="2de45-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="2de45-113">Value</span><span class="sxs-lookup"><span data-stu-id="2de45-113">Value</span></span>                                                                        | <span data-ttu-id="2de45-114">Significado</span><span class="sxs-lookup"><span data-stu-id="2de45-114">Meaning</span></span>                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2de45-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2de45-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="2de45-116">Pinta el control sin efectos visuales.</span><span class="sxs-lookup"><span data-stu-id="2de45-116">Paints the control without visual effects.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2de45-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2de45-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="2de45-118">Pinta el control con efectos tridimensionales.</span><span class="sxs-lookup"><span data-stu-id="2de45-118">Paints the control with three-dimensional effects.</span></span> <span data-ttu-id="2de45-119">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2de45-119">This is the default value.</span></span><br/> |



 

## <a name="exceptions"></a><span data-ttu-id="2de45-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="2de45-120">Exceptions</span></span>



| <span data-ttu-id="2de45-121">Tipo de excepción</span><span class="sxs-lookup"><span data-stu-id="2de45-121">Exception type</span></span>               | <span data-ttu-id="2de45-122">Condición</span><span class="sxs-lookup"><span data-stu-id="2de45-122">Condition</span></span>                                    |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="2de45-123">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="2de45-123">**System.ArgumentException**</span></span> | <span data-ttu-id="2de45-124">El valor de apariencia especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="2de45-124">The specified appearance value is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2de45-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2de45-125">Remarks</span></span>

<span data-ttu-id="2de45-126">Se trata de una propiedad de ambiente.</span><span class="sxs-lookup"><span data-stu-id="2de45-126">This is an ambient property.</span></span> <span data-ttu-id="2de45-127">El valor de esta propiedad viene determinado por el contenedor.</span><span class="sxs-lookup"><span data-stu-id="2de45-127">The value of this property is determined by the container.</span></span> <span data-ttu-id="2de45-128">Establecer el valor de esta propiedad puede afectar a la ilusión del control y el contenedor como una sola aplicación.</span><span class="sxs-lookup"><span data-stu-id="2de45-128">Setting the value of this property could affect the illusion of the control and container being a single application.</span></span>

## <a name="requirements"></a><span data-ttu-id="2de45-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2de45-129">Requirements</span></span>



| <span data-ttu-id="2de45-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2de45-130">Requirement</span></span> | <span data-ttu-id="2de45-131">Value</span><span class="sxs-lookup"><span data-stu-id="2de45-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2de45-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2de45-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2de45-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2de45-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2de45-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2de45-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2de45-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2de45-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2de45-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2de45-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2de45-137"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2de45-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2de45-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2de45-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de45-139">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="2de45-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





