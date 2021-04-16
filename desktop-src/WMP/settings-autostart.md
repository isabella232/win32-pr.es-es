---
title: Configuración. Inicio automático
description: La propiedad autoStart especifica o recupera un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Configuración. Inicio automático de Windows Media Player
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649559"
---
# <a name="settingsautostart"></a><span data-ttu-id="fad87-104">Configuración. Inicio automático</span><span class="sxs-lookup"><span data-stu-id="fad87-104">Settings.autoStart</span></span>

<span data-ttu-id="fad87-105">La propiedad **autoStart** especifica o recupera un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fad87-105">The **autoStart** property specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad87-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fad87-106">Syntax</span></span>

<span data-ttu-id="fad87-107">Player. Settings. autoStart</span><span class="sxs-lookup"><span data-stu-id="fad87-107">player.settings.autoStart</span></span>

## <a name="possible-values"></a><span data-ttu-id="fad87-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="fad87-108">Possible Values</span></span>

<span data-ttu-id="fad87-109">Esta propiedad es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="fad87-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="fad87-110">Value</span><span class="sxs-lookup"><span data-stu-id="fad87-110">Value</span></span> | <span data-ttu-id="fad87-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fad87-111">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="fad87-112">true</span><span class="sxs-lookup"><span data-stu-id="fad87-112">true</span></span>  | <span data-ttu-id="fad87-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fad87-113">Default.</span></span> <span data-ttu-id="fad87-114">El elemento multimedia comienza a reproducirse automáticamente (vea la sección comentarios).</span><span class="sxs-lookup"><span data-stu-id="fad87-114">The media item begins playing automatically (see Remarks).</span></span> |
| <span data-ttu-id="fad87-115">false</span><span class="sxs-lookup"><span data-stu-id="fad87-115">false</span></span> | <span data-ttu-id="fad87-116">El elemento multimedia no empieza a reproducirse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fad87-116">The media item does not begin playing automatically.</span></span>                |



 

## <a name="remarks"></a><span data-ttu-id="fad87-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fad87-117">Remarks</span></span>

<span data-ttu-id="fad87-118">Si **autoStart** se establece en true, el elemento multimedia empezará a reproducirse cuando el *reproductor*. **Dirección URL**, *reproductor*. **currentPlaylist** o *Player*. **currentMedia** está establecido.</span><span class="sxs-lookup"><span data-stu-id="fad87-118">If **autoStart** is set to true, the media item will begin playing when *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** is set.</span></span> <span data-ttu-id="fad87-119">De lo contrario, no empezará a reproducirse hasta que los *controles*. se llama al método **Play** .</span><span class="sxs-lookup"><span data-stu-id="fad87-119">Otherwise, it will not start playing until the *Controls*.**play** method is called.</span></span>

<span data-ttu-id="fad87-120">Dado que la propiedad **autoStart** para el modo completo de Windows Media Player se puede establecer globalmente mediante eventos externos (como cargar un CD), no hay ningún valor predeterminado confiable para las máscaras y los controles del reproductor remoto.</span><span class="sxs-lookup"><span data-stu-id="fad87-120">Because the **autoStart** property for the full mode of Windows Media Player can be set globally by external events (such as loading a CD), there is no reliable default value for skins and remoted Player controls.</span></span> <span data-ttu-id="fad87-121">Esto se debe a que el motor de reproducción del reproductor en modo completo se usa en ambos casos.</span><span class="sxs-lookup"><span data-stu-id="fad87-121">This is because the playback engine of the full mode Player is used in both cases.</span></span>

<span data-ttu-id="fad87-122">Debe establecer **autoStart** en false inmediatamente antes de configurar el *reproductor*. **Dirección URL**, *reproductor*. **currentPlaylist** o *Player*. **currentMedia** en máscaras y controles de Windows Media Player remotos si desea asegurarse de que el elemento multimedia no empiece a reproducirse inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="fad87-122">You should set **autoStart** to false immediately before you set *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** in skins and remoted Windows Media Player controls if you want to ensure that the media item does not start playing immediately.</span></span> <span data-ttu-id="fad87-123">Además, a menos que establezca **AutoStart** en true inmediatamente antes de especificar un elemento multimedia, no debe confiar en este valor como sustituto para usar los *controles*. método **Play** .</span><span class="sxs-lookup"><span data-stu-id="fad87-123">Also, unless you set **autostart** to true immediately before specifying a media item, you should not rely on this setting as a substitute for using the *Controls*.**play** method.</span></span>

## <a name="examples"></a><span data-ttu-id="fad87-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fad87-124">Examples</span></span>

<span data-ttu-id="fad87-125">En el ejemplo siguiente se crea un elemento CHECKBOX HTML que permite al usuario especificar si el control Player reproduce automáticamente el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="fad87-125">The following example creates an HTML CHECKBOX element that allows the user to specify whether the Player control plays the current media item automatically.</span></span> <span data-ttu-id="fad87-126">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="fad87-126">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a><span data-ttu-id="fad87-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fad87-127">Requirements</span></span>



| <span data-ttu-id="fad87-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fad87-128">Requirement</span></span> | <span data-ttu-id="fad87-129">Value</span><span class="sxs-lookup"><span data-stu-id="fad87-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fad87-130">Versión</span><span class="sxs-lookup"><span data-stu-id="fad87-130">Version</span></span><br/> | <span data-ttu-id="fad87-131">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fad87-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fad87-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fad87-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="fad87-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fad87-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad87-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="fad87-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad87-135">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="fad87-135">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="fad87-136">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="fad87-136">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="fad87-137">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="fad87-137">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





