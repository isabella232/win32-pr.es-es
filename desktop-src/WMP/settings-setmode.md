---
title: Settings. setMode (método)
description: El método setMode establece varios modos en activo o inactivo.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- método setMode de Windows Media Player
- método setMode de Windows Media Player, clase de configuración
- Clase de configuración Windows Media Player, método setMode
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653571"
---
# <a name="settingssetmode-method"></a><span data-ttu-id="a01e9-106">Settings. setMode (método)</span><span class="sxs-lookup"><span data-stu-id="a01e9-106">Settings.setMode method</span></span>

<span data-ttu-id="a01e9-107">El método **setMode** establece varios modos en activo o inactivo.</span><span class="sxs-lookup"><span data-stu-id="a01e9-107">The **setMode** method sets various modes to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a01e9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a01e9-108">Syntax</span></span>


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a><span data-ttu-id="a01e9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a01e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a01e9-110">*modeName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a01e9-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a01e9-111">**Cadena** que especifica el nombre del modo que se va a cambiar, que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a01e9-111">**String** specifying the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="a01e9-112">String</span><span class="sxs-lookup"><span data-stu-id="a01e9-112">String</span></span>     | <span data-ttu-id="a01e9-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a01e9-113">Description</span></span>                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a01e9-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="a01e9-114">autoRewind</span></span> | <span data-ttu-id="a01e9-115">Modo que indica si las pistas se rebobinan al principio después de reproducirse hasta el final.</span><span class="sxs-lookup"><span data-stu-id="a01e9-115">Mode indicating whether the tracks are rewound to the beginning after playing to the end.</span></span> <span data-ttu-id="a01e9-116">El estado predeterminado es true.</span><span class="sxs-lookup"><span data-stu-id="a01e9-116">Default state is true.</span></span>                                                  |
| <span data-ttu-id="a01e9-117">bucle</span><span class="sxs-lookup"><span data-stu-id="a01e9-117">loop</span></span>       | <span data-ttu-id="a01e9-118">Modo que indica si la secuencia de pistas se repite.</span><span class="sxs-lookup"><span data-stu-id="a01e9-118">Mode indicating whether the sequence of tracks repeats itself.</span></span> <span data-ttu-id="a01e9-119">El estado predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="a01e9-119">Default state is false.</span></span>                                                                            |
| <span data-ttu-id="a01e9-120">showFrame</span><span class="sxs-lookup"><span data-stu-id="a01e9-120">showFrame</span></span>  | <span data-ttu-id="a01e9-121">Modo que indica si se muestra el fotograma clave de vídeo más próximo en la posición actual cuando no se reproduce.</span><span class="sxs-lookup"><span data-stu-id="a01e9-121">Mode indicating whether the nearest video key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="a01e9-122">El estado predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="a01e9-122">Default state is false.</span></span> <span data-ttu-id="a01e9-123">No tiene ningún efecto en las pistas de audio.</span><span class="sxs-lookup"><span data-stu-id="a01e9-123">Has no effect on audio tracks.</span></span> |
| <span data-ttu-id="a01e9-124">shuffle</span><span class="sxs-lookup"><span data-stu-id="a01e9-124">shuffle</span></span>    | <span data-ttu-id="a01e9-125">Modo que indica si las pistas se reproducen en orden aleatorio.</span><span class="sxs-lookup"><span data-stu-id="a01e9-125">Mode indicating whether the tracks are played in random order.</span></span> <span data-ttu-id="a01e9-126">El estado predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="a01e9-126">Default state is false.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="a01e9-127">*Estado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a01e9-127">*state* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a01e9-128">**Valor booleano** que especifica si el nuevo modo especificado está activo o no.</span><span class="sxs-lookup"><span data-stu-id="a01e9-128">**Boolean** specifying whether the new specified mode is active or not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a01e9-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a01e9-129">Return value</span></span>

<span data-ttu-id="a01e9-130">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a01e9-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a01e9-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a01e9-131">Remarks</span></span>

<span data-ttu-id="a01e9-132">Cuando el modo showFrame está activo, el reproductor debe tener acceso al contenido de Track para recuperar el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a01e9-132">When the showFrame mode is active, the Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="a01e9-133">Debido a las consideraciones de ancho de banda, use este modo con precaución al reproducir contenido no local.</span><span class="sxs-lookup"><span data-stu-id="a01e9-133">Due to bandwidth considerations, use this mode cautiously when playing non-local content.</span></span>

## <a name="requirements"></a><span data-ttu-id="a01e9-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a01e9-134">Requirements</span></span>



| <span data-ttu-id="a01e9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a01e9-135">Requirement</span></span> | <span data-ttu-id="a01e9-136">Value</span><span class="sxs-lookup"><span data-stu-id="a01e9-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a01e9-137">Versión</span><span class="sxs-lookup"><span data-stu-id="a01e9-137">Version</span></span><br/> | <span data-ttu-id="a01e9-138">En los modos de bucle y orden aleatorio, Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a01e9-138">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="a01e9-139">En los modos autoRewind y showFrame, Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="a01e9-139">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="a01e9-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a01e9-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="a01e9-141"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a01e9-141"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="a01e9-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="a01e9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a01e9-143">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="a01e9-143">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="a01e9-144">**Settings. getMode**</span><span class="sxs-lookup"><span data-stu-id="a01e9-144">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> </dl>

 

 





