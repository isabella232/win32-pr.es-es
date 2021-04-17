---
title: Player. fullScreen
description: La propiedad fullScreen especifica o recupera un valor que indica si el contenido de vídeo se reproduce en el modo de pantalla completa.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player. fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698671"
---
# <a name="playerfullscreen"></a><span data-ttu-id="c954b-104">Player. fullScreen</span><span class="sxs-lookup"><span data-stu-id="c954b-104">Player.fullScreen</span></span>

<span data-ttu-id="c954b-105">La propiedad **Fullscreen** especifica o recupera un valor que indica si el contenido de vídeo se reproduce en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="c954b-105">The **fullScreen** property specifies or retrieves a value indicating whether video content is played back in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="c954b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c954b-106">Syntax</span></span>

<span data-ttu-id="c954b-107">*reproductor* . **pantalla completa**</span><span class="sxs-lookup"><span data-stu-id="c954b-107">*player* .**fullScreen**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c954b-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="c954b-108">Possible Values</span></span>

<span data-ttu-id="c954b-109">Esta propiedad es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="c954b-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="c954b-110">Value</span><span class="sxs-lookup"><span data-stu-id="c954b-110">Value</span></span> | <span data-ttu-id="c954b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c954b-111">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="c954b-112">true</span><span class="sxs-lookup"><span data-stu-id="c954b-112">true</span></span>  | <span data-ttu-id="c954b-113">El contenido de vídeo se reproduce en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="c954b-113">Video content is played back in full-screen mode.</span></span>              |
| <span data-ttu-id="c954b-114">false</span><span class="sxs-lookup"><span data-stu-id="c954b-114">false</span></span> | <span data-ttu-id="c954b-115">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c954b-115">Default.</span></span> <span data-ttu-id="c954b-116">El contenido de vídeo no se reproduce en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="c954b-116">Video content is not played back in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c954b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c954b-117">Remarks</span></span>

<span data-ttu-id="c954b-118">Para que el modo de pantalla completa funcione correctamente al insertar el control Media Player de Windows, el área de presentación del vídeo debe tener un alto y un ancho de al menos un píxel.</span><span class="sxs-lookup"><span data-stu-id="c954b-118">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="c954b-119">Si **uiMode** se establece en "mini" o "Full", el alto del propio control debe ser 65 o superior para dar cabida al área de presentación de vídeo además de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c954b-119">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="c954b-120">Si **uiMode** se establece en "invisible", al establecer esta propiedad en true se genera un error y no se ve afectado el comportamiento del control.</span><span class="sxs-lookup"><span data-stu-id="c954b-120">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="c954b-121">Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".</span><span class="sxs-lookup"><span data-stu-id="c954b-121">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="c954b-122">Si **uiMode** se establece en "Full" o "mini", Windows Media Player muestra los controles de transporte en modo de pantalla completa cuando se mueve el cursor del mouse.</span><span class="sxs-lookup"><span data-stu-id="c954b-122">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="c954b-123">Después de un breve intervalo de ausencia de movimiento del mouse, se ocultan los controles de transporte.</span><span class="sxs-lookup"><span data-stu-id="c954b-123">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="c954b-124">Si **uiMode** se establece en "none", no se muestra ningún control en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="c954b-124">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="c954b-125">**Note**</span><span class="sxs-lookup"><span data-stu-id="c954b-125">**Note**</span></span>

<span data-ttu-id="c954b-126">Para mostrar los controles de transporte en modo de pantalla completa, se requiere el sistema operativo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c954b-126">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

<span data-ttu-id="c954b-127">Si los controles de transporte no se muestran en el modo de pantalla completa, Windows Media Player sale automáticamente del modo de pantalla completa cuando se detiene la reproducción.</span><span class="sxs-lookup"><span data-stu-id="c954b-127">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

<span data-ttu-id="c954b-128">**Note**</span><span class="sxs-lookup"><span data-stu-id="c954b-128">**Note**</span></span>

<span data-ttu-id="c954b-129">Asegúrese siempre de informar al usuario de cómo volver del modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="c954b-129">Always be sure to inform the user how to return from full-screen mode.</span></span>

## <a name="examples"></a><span data-ttu-id="c954b-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c954b-130">Examples</span></span>

<span data-ttu-id="c954b-131">En el ejemplo siguiente se crea un botón de entrada HTML que usa *Player*. **pantalla** completa: cambiar un objeto reproductor incrustado al modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="c954b-131">The following example creates an HTML input button that uses *Player*.**fullScreen** to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="c954b-132">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c954b-132">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a><span data-ttu-id="c954b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c954b-133">Requirements</span></span>



| <span data-ttu-id="c954b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c954b-134">Requirement</span></span> | <span data-ttu-id="c954b-135">Value</span><span class="sxs-lookup"><span data-stu-id="c954b-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c954b-136">Versión</span><span class="sxs-lookup"><span data-stu-id="c954b-136">Version</span></span><br/> | <span data-ttu-id="c954b-137">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="c954b-137">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c954b-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c954b-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="c954b-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c954b-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c954b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c954b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c954b-141">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="c954b-141">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





