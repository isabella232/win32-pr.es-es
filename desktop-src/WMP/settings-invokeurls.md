---
title: Settings. invokeURLs
description: La propiedad invokeURLs especifica o recupera un valor que indica si los eventos de dirección URL deben iniciar un explorador Web.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Settings. invokeURLs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649754"
---
# <a name="settingsinvokeurls"></a><span data-ttu-id="c9530-104">Settings. invokeURLs</span><span class="sxs-lookup"><span data-stu-id="c9530-104">Settings.invokeURLs</span></span>

<span data-ttu-id="c9530-105">La propiedad **invokeURLs** especifica o recupera un valor que indica si los eventos de dirección URL deben iniciar un explorador Web.</span><span class="sxs-lookup"><span data-stu-id="c9530-105">The **invokeURLs** property specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9530-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9530-106">Syntax</span></span>

<span data-ttu-id="c9530-107">Player. Settings. invokeURLs</span><span class="sxs-lookup"><span data-stu-id="c9530-107">player.settings.invokeURLs</span></span>

## <a name="possible-values"></a><span data-ttu-id="c9530-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="c9530-108">Possible Values</span></span>

<span data-ttu-id="c9530-109">Esta propiedad es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="c9530-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="c9530-110">Value</span><span class="sxs-lookup"><span data-stu-id="c9530-110">Value</span></span> | <span data-ttu-id="c9530-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9530-111">Description</span></span>                                  |
|-------|----------------------------------------------|
| <span data-ttu-id="c9530-112">true</span><span class="sxs-lookup"><span data-stu-id="c9530-112">true</span></span>  | <span data-ttu-id="c9530-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c9530-113">Default.</span></span> <span data-ttu-id="c9530-114">Los eventos de URL deben iniciar un explorador.</span><span class="sxs-lookup"><span data-stu-id="c9530-114">URL events should launch a browser.</span></span> |
| <span data-ttu-id="c9530-115">false</span><span class="sxs-lookup"><span data-stu-id="c9530-115">false</span></span> | <span data-ttu-id="c9530-116">Los eventos de URL no deben iniciar un explorador.</span><span class="sxs-lookup"><span data-stu-id="c9530-116">URL events should not launch a browser.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="c9530-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9530-117">Remarks</span></span>

<span data-ttu-id="c9530-118">Los archivos multimedia pueden contener direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="c9530-118">Media files can contain URLs.</span></span> <span data-ttu-id="c9530-119">Cuando se envía una dirección URL al control de Media Player de Windows, se pasa primero al controlador de eventos **comando** independientemente del valor de **invokeURLs**.</span><span class="sxs-lookup"><span data-stu-id="c9530-119">When a URL is sent to the Windows Media Player control, it is passed first to the **ScriptCommand** event handler regardless of the value in **invokeURLs**.</span></span> <span data-ttu-id="c9530-120">Después de que **comando** se cierre, Windows Media Player comprueba **invokeURLs** para determinar si se debe iniciar el explorador de Internet predeterminado con la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="c9530-120">After **ScriptCommand** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Internet browser with the URL.</span></span> <span data-ttu-id="c9530-121">Puede mostrar las direcciones URL de forma selectiva al comprobarlas en **comando** y establecer **invokeURLs** como desee.</span><span class="sxs-lookup"><span data-stu-id="c9530-121">You can selectively display URLs by checking them in **ScriptCommand** and setting **invokeURLs** as desired.</span></span>

<span data-ttu-id="c9530-122">**Windows Media Player 10 Mobile**: esta propiedad solo acepta o devuelve false.</span><span class="sxs-lookup"><span data-stu-id="c9530-122">**Windows Media Player 10 Mobile**: This property only accepts or returns false.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9530-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9530-123">Requirements</span></span>



| <span data-ttu-id="c9530-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9530-124">Requirement</span></span> | <span data-ttu-id="c9530-125">Value</span><span class="sxs-lookup"><span data-stu-id="c9530-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9530-126">Versión</span><span class="sxs-lookup"><span data-stu-id="c9530-126">Version</span></span><br/> | <span data-ttu-id="c9530-127">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="c9530-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c9530-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9530-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="c9530-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9530-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9530-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9530-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9530-131">**Evento Player. comando**</span><span class="sxs-lookup"><span data-stu-id="c9530-131">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="c9530-132">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="c9530-132">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





