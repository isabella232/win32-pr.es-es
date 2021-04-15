---
title: Media. Duration
description: La propiedad duration recupera la duración del elemento multimedia actual en segundos.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media Player de Windows Media. Duration
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71586f6aa37401d56a9e9537bfbea6c5af23f318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709098"
---
# <a name="mediaduration"></a><span data-ttu-id="ce194-104">Media. Duration</span><span class="sxs-lookup"><span data-stu-id="ce194-104">Media.duration</span></span>

<span data-ttu-id="ce194-105">La propiedad **Duration** recupera la duración del elemento multimedia actual en segundos.</span><span class="sxs-lookup"><span data-stu-id="ce194-105">The **duration** property retrieves the duration of the current media item in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce194-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce194-106">Syntax</span></span>

<span data-ttu-id="ce194-107">*reproductor*. *currentMedia*. **duración** de</span><span class="sxs-lookup"><span data-stu-id="ce194-107">*player*.*currentMedia*.**duration**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ce194-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="ce194-108">Possible Values</span></span>

<span data-ttu-id="ce194-109">Esta propiedad es un **número** de solo lectura ( **Double**).</span><span class="sxs-lookup"><span data-stu-id="ce194-109">This property is a read-only **Number** ( **double**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce194-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce194-110">Remarks</span></span>

<span data-ttu-id="ce194-111">Si esta propiedad se utiliza con un elemento multimedia distinto del especificado en el *reproductor*. **currentMedia**, puede que no contenga un valor válido.</span><span class="sxs-lookup"><span data-stu-id="ce194-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span>

<span data-ttu-id="ce194-112">Para recuperar la duración de los archivos que no están en la biblioteca del usuario, debe esperar a que Windows Media Player Abra el archivo; es decir, el OpenState actual debe ser igual a MediaOpen.</span><span class="sxs-lookup"><span data-stu-id="ce194-112">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current OpenState must equal MediaOpen.</span></span> <span data-ttu-id="ce194-113">Para comprobarlo, controle el *reproductor*. Evento **OpenStateChange** o comprobando periódicamente el valor de *Player*. **openState**.</span><span class="sxs-lookup"><span data-stu-id="ce194-113">You can verify this by handling the *Player*.**OpenStateChange** event or by periodically checking the value of *Player*.**openState**.</span></span>

<span data-ttu-id="ce194-114">En las listas de reproducción, la duración de cada elemento multimedia se puede recuperar cuando se abre el elemento multimedia individual, en lugar de cuando se abre la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="ce194-114">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="ce194-115">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ce194-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="ce194-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ce194-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ce194-117">En el siguiente ejemplo de JScript se utiliza el *medio*. **duración** para mostrar el tiempo restante en el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="ce194-117">The following JScript example uses *Media*.**duration** to display the time remaining in the current media item.</span></span> <span data-ttu-id="ce194-118">Un elemento HTML DIV denominado RemTime muestra la información.</span><span class="sxs-lookup"><span data-stu-id="ce194-118">An HTML DIV element named RemTime displays the information.</span></span> <span data-ttu-id="ce194-119">Un temporizador HTML actualiza el texto del elemento DIV cada segundo.</span><span class="sxs-lookup"><span data-stu-id="ce194-119">An HTML timer updates the text in the DIV element every second.</span></span>

<span data-ttu-id="ce194-120">El siguiente código JScript inicia el temporizador:</span><span class="sxs-lookup"><span data-stu-id="ce194-120">The following JScript code starts the timer:</span></span>


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



<span data-ttu-id="ce194-121">El siguiente código JScript detiene el temporizador:</span><span class="sxs-lookup"><span data-stu-id="ce194-121">The following JScript code stops the timer:</span></span>


```JScript
window.clearInterval(idTmr);
```



<span data-ttu-id="ce194-122">Use el *reproductor*. Evento **PlayStateChange** con una instrucción **Switch** para determinar cuándo iniciar y detener el temporizador.</span><span class="sxs-lookup"><span data-stu-id="ce194-122">Use the *Player*.**PlayStateChange** event with a **switch** statement to determine when to start and stop the timer.</span></span>

<span data-ttu-id="ce194-123">El siguiente código JScript se ejecuta cada vez que el temporizador llama a la función de actualización:</span><span class="sxs-lookup"><span data-stu-id="ce194-123">The following JScript code executes each time the timer calls the update function:</span></span>


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
```



## <a name="requirements"></a><span data-ttu-id="ce194-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce194-124">Requirements</span></span>



| <span data-ttu-id="ce194-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce194-125">Requirement</span></span> | <span data-ttu-id="ce194-126">Value</span><span class="sxs-lookup"><span data-stu-id="ce194-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce194-127">Versión</span><span class="sxs-lookup"><span data-stu-id="ce194-127">Version</span></span><br/> | <span data-ttu-id="ce194-128">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ce194-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ce194-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ce194-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="ce194-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce194-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce194-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce194-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce194-132">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="ce194-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="ce194-133">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="ce194-133">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="ce194-134">**Evento Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="ce194-134">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="ce194-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ce194-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ce194-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ce194-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





