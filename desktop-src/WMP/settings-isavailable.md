---
title: Settings. isAvailable
description: La propiedad isAvailable indica si un tipo especificado de información está disponible o se puede realizar una acción especificada. | Settings. isAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Settings. isAvailable Windows Media Player
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649753"
---
# <a name="settingsisavailable"></a><span data-ttu-id="03c70-105">Settings. isAvailable</span><span class="sxs-lookup"><span data-stu-id="03c70-105">Settings.isAvailable</span></span>

<span data-ttu-id="03c70-106">La propiedad **isavailable** indica si un tipo especificado de información está disponible o se puede realizar una acción especificada.</span><span class="sxs-lookup"><span data-stu-id="03c70-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c70-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03c70-107">Syntax</span></span>

<span data-ttu-id="03c70-108">Player. Settings. isAvailable (nombre)</span><span class="sxs-lookup"><span data-stu-id="03c70-108">player.settings.isAvailable( name )</span></span>

## <a name="parameters"></a><span data-ttu-id="03c70-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03c70-109">Parameters</span></span>

<span data-ttu-id="03c70-110">*name*</span><span class="sxs-lookup"><span data-stu-id="03c70-110">*name*</span></span>

<span data-ttu-id="03c70-111">Cadena que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="03c70-111">String containing one of the following values.</span></span>



| <span data-ttu-id="03c70-112">String</span><span class="sxs-lookup"><span data-stu-id="03c70-112">String</span></span>             | <span data-ttu-id="03c70-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="03c70-113">Description</span></span>                                                    |
|--------------------|----------------------------------------------------------------|
| <span data-ttu-id="03c70-114">AutoStart</span><span class="sxs-lookup"><span data-stu-id="03c70-114">AutoStart</span></span>          | <span data-ttu-id="03c70-115">Determina si se puede establecer la propiedad autoStart.</span><span class="sxs-lookup"><span data-stu-id="03c70-115">Determines whether the autoStart property can be set.</span></span>          |
| <span data-ttu-id="03c70-116">Saldo</span><span class="sxs-lookup"><span data-stu-id="03c70-116">Balance</span></span>            | <span data-ttu-id="03c70-117">Determina si se puede establecer la propiedad de saldo.</span><span class="sxs-lookup"><span data-stu-id="03c70-117">Determines whether the balance property can be set.</span></span>            |
| <span data-ttu-id="03c70-118">BaseURL</span><span class="sxs-lookup"><span data-stu-id="03c70-118">BaseURL</span></span>            | <span data-ttu-id="03c70-119">Determina si se puede establecer la propiedad baseURL.</span><span class="sxs-lookup"><span data-stu-id="03c70-119">Determines whether the baseURL property can be set.</span></span>            |
| <span data-ttu-id="03c70-120">DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="03c70-120">DefaultFrame</span></span>       | <span data-ttu-id="03c70-121">Determina si se puede establecer la propiedad defaultFrame.</span><span class="sxs-lookup"><span data-stu-id="03c70-121">Determines whether the defaultFrame property can be set.</span></span>       |
| <span data-ttu-id="03c70-122">EnableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="03c70-122">EnableErrorDialogs</span></span> | <span data-ttu-id="03c70-123">Determina si se puede establecer la propiedad enableErrorDialogs.</span><span class="sxs-lookup"><span data-stu-id="03c70-123">Determines whether the enableErrorDialogs property can be set.</span></span> |
| <span data-ttu-id="03c70-124">GetMode</span><span class="sxs-lookup"><span data-stu-id="03c70-124">GetMode</span></span>            | <span data-ttu-id="03c70-125">Determina si se puede llamar al método getMode.</span><span class="sxs-lookup"><span data-stu-id="03c70-125">Determines whether the getMode method can be called.</span></span>           |
| <span data-ttu-id="03c70-126">InvokeURLs</span><span class="sxs-lookup"><span data-stu-id="03c70-126">InvokeURLs</span></span>         | <span data-ttu-id="03c70-127">Determina si se puede establecer la propiedad invokeURLs.</span><span class="sxs-lookup"><span data-stu-id="03c70-127">Determines whether the invokeURLs property can be set.</span></span>         |
| <span data-ttu-id="03c70-128">Silencio</span><span class="sxs-lookup"><span data-stu-id="03c70-128">Mute</span></span>               | <span data-ttu-id="03c70-129">Determina si se puede establecer la propiedad MUTE.</span><span class="sxs-lookup"><span data-stu-id="03c70-129">Determines whether the mute property can be set.</span></span>               |
| <span data-ttu-id="03c70-130">PlayCount</span><span class="sxs-lookup"><span data-stu-id="03c70-130">PlayCount</span></span>          | <span data-ttu-id="03c70-131">Determina si se puede establecer la propiedad playCount.</span><span class="sxs-lookup"><span data-stu-id="03c70-131">Determines whether the playCount property can be set.</span></span>          |
| <span data-ttu-id="03c70-132">Tarifa</span><span class="sxs-lookup"><span data-stu-id="03c70-132">Rate</span></span>               | <span data-ttu-id="03c70-133">Determina si se puede establecer la propiedad Rate.</span><span class="sxs-lookup"><span data-stu-id="03c70-133">Determines whether the rate property can be set.</span></span>               |
| <span data-ttu-id="03c70-134">SetMode</span><span class="sxs-lookup"><span data-stu-id="03c70-134">SetMode</span></span>            | <span data-ttu-id="03c70-135">Determina si se puede llamar al método setMode.</span><span class="sxs-lookup"><span data-stu-id="03c70-135">Determines whether the setMode method can be called.</span></span>           |
| <span data-ttu-id="03c70-136">Volumen</span><span class="sxs-lookup"><span data-stu-id="03c70-136">Volume</span></span>             | <span data-ttu-id="03c70-137">Determina si se puede establecer la propiedad de volumen.</span><span class="sxs-lookup"><span data-stu-id="03c70-137">Determines whether the volume property can be set.</span></span>             |



 

## <a name="return-values"></a><span data-ttu-id="03c70-138">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="03c70-138">Return Values</span></span>

<span data-ttu-id="03c70-139">Este método devuelve un valor **booleano** .</span><span class="sxs-lookup"><span data-stu-id="03c70-139">This method returns a **Boolean** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03c70-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03c70-140">Requirements</span></span>



| <span data-ttu-id="03c70-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c70-141">Requirement</span></span> | <span data-ttu-id="03c70-142">Value</span><span class="sxs-lookup"><span data-stu-id="03c70-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03c70-143">Versión</span><span class="sxs-lookup"><span data-stu-id="03c70-143">Version</span></span><br/> | <span data-ttu-id="03c70-144">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="03c70-144">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="03c70-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03c70-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="03c70-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03c70-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03c70-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="03c70-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c70-148">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="03c70-148">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





