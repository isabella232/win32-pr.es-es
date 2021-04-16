---
title: Settings. getMode (método)
description: El método getMode determina si el modo de bucle o el modo de orden aleatorio está activo.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- método getMode de Windows Media Player
- método getMode de Windows Media Player, clase de configuración
- Clase de configuración Windows Media Player, método getMode
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649755"
---
# <a name="settingsgetmode-method"></a><span data-ttu-id="d6970-106">Settings. getMode (método)</span><span class="sxs-lookup"><span data-stu-id="d6970-106">Settings.getMode method</span></span>

<span data-ttu-id="d6970-107">El método **getMode** determina si el modo de bucle o el modo de orden aleatorio está activo.</span><span class="sxs-lookup"><span data-stu-id="d6970-107">The **getMode** method determines whether the loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6970-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6970-108">Syntax</span></span>


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a><span data-ttu-id="d6970-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6970-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6970-110">*modeName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d6970-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6970-111">**Cadena** que especifica el nombre del modo en cuestión, que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d6970-111">**String** specifying the name of the mode in question, containing one of the following values.</span></span>



| <span data-ttu-id="d6970-112">String</span><span class="sxs-lookup"><span data-stu-id="d6970-112">String</span></span>     | <span data-ttu-id="d6970-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6970-113">Description</span></span>                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6970-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="d6970-114">autoRewind</span></span> | <span data-ttu-id="d6970-115">Las pistas se reinician al principio después de reproducirse hasta el final.</span><span class="sxs-lookup"><span data-stu-id="d6970-115">Tracks are restarted at the beginning after playing to the end.</span></span>                                                          |
| <span data-ttu-id="d6970-116">bucle</span><span class="sxs-lookup"><span data-stu-id="d6970-116">loop</span></span>       | <span data-ttu-id="d6970-117">La secuencia de pistas se repite.</span><span class="sxs-lookup"><span data-stu-id="d6970-117">The sequence of tracks repeats itself.</span></span>                                                                                   |
| <span data-ttu-id="d6970-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="d6970-118">showFrame</span></span>  | <span data-ttu-id="d6970-119">El fotograma clave más cercano se muestra en la posición actual cuando no se reproduce.</span><span class="sxs-lookup"><span data-stu-id="d6970-119">The nearest key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="d6970-120">Este modo no es relevante para las pistas de audio.</span><span class="sxs-lookup"><span data-stu-id="d6970-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="d6970-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="d6970-121">shuffle</span></span>    | <span data-ttu-id="d6970-122">Las pistas se reproducen en orden aleatorio.</span><span class="sxs-lookup"><span data-stu-id="d6970-122">Tracks are played in random order.</span></span>                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6970-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6970-123">Return value</span></span>

<span data-ttu-id="d6970-124">Este método devuelve un valor **booleano** que indica si el modo especificado está activo.</span><span class="sxs-lookup"><span data-stu-id="d6970-124">This method returns a **Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6970-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6970-125">Requirements</span></span>



| <span data-ttu-id="d6970-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6970-126">Requirement</span></span> | <span data-ttu-id="d6970-127">Value</span><span class="sxs-lookup"><span data-stu-id="d6970-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6970-128">Versión</span><span class="sxs-lookup"><span data-stu-id="d6970-128">Version</span></span><br/> | <span data-ttu-id="d6970-129">En los modos de bucle y orden aleatorio, Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d6970-129">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="d6970-130">En los modos autoRewind y showFrame, Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="d6970-130">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="d6970-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6970-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="d6970-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6970-132"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="d6970-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6970-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6970-134">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="d6970-134">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="d6970-135">**Settings. setMode**</span><span class="sxs-lookup"><span data-stu-id="d6970-135">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





