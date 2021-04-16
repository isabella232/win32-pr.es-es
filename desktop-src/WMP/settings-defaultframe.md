---
title: Settings. defaultFrame
description: La propiedad defaultFrame especifica o recupera el nombre del marco que se usa para mostrar una dirección URL que se recibe en un evento comando.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Settings. defaultFrame Windows Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649811"
---
# <a name="settingsdefaultframe"></a><span data-ttu-id="c6a0f-104">Settings. defaultFrame</span><span class="sxs-lookup"><span data-stu-id="c6a0f-104">Settings.defaultFrame</span></span>

<span data-ttu-id="c6a0f-105">La propiedad **defaultFrame** especifica o recupera el nombre del marco que se usa para mostrar una dirección URL que se recibe en un evento **comando** .</span><span class="sxs-lookup"><span data-stu-id="c6a0f-105">The **defaultFrame** property specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6a0f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6a0f-106">Syntax</span></span>

<span data-ttu-id="c6a0f-107">Player. Settings. defaultFrame</span><span class="sxs-lookup"><span data-stu-id="c6a0f-107">player.settings.defaultFrame</span></span>

## <a name="possible-values"></a><span data-ttu-id="c6a0f-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="c6a0f-108">Possible Values</span></span>

<span data-ttu-id="c6a0f-109">Esta propiedad es una **cadena** de lectura/escritura que corresponde al valor del atributo **Name** del elemento de marco de destino.</span><span class="sxs-lookup"><span data-stu-id="c6a0f-109">This property is a read/write **String** corresponding to the value of the **name** attribute of the target FRAME element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6a0f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6a0f-110">Remarks</span></span>

<span data-ttu-id="c6a0f-111">Si se especifica un marco de destino en el propio evento **comando** , se omite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c6a0f-111">If a target frame is specified in the **ScriptCommand** event itself, this property is ignored.</span></span>

<span data-ttu-id="c6a0f-112">Esta propiedad se omite cuando se usa el applet Java de Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="c6a0f-112">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="c6a0f-113">En el navegador, cada comando de script de dirección URL recibido muestra la dirección URL en una nueva ventana del explorador, independientemente del valor de *configuración*. **defaultFrame**.</span><span class="sxs-lookup"><span data-stu-id="c6a0f-113">In Navigator, each URL script command received displays the URL in a new browser window, regardless of the value of *Settings*.**defaultFrame**.</span></span>

<span data-ttu-id="c6a0f-114">**Windows Media Player 10 Mobile**: esta propiedad es de solo lectura y siempre devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="c6a0f-114">**Windows Media Player 10 Mobile**: This property is read only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a0f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6a0f-115">Requirements</span></span>



| <span data-ttu-id="c6a0f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6a0f-116">Requirement</span></span> | <span data-ttu-id="c6a0f-117">Value</span><span class="sxs-lookup"><span data-stu-id="c6a0f-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a0f-118">Versión</span><span class="sxs-lookup"><span data-stu-id="c6a0f-118">Version</span></span><br/> | <span data-ttu-id="c6a0f-119">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="c6a0f-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c6a0f-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6a0f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c6a0f-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6a0f-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a0f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6a0f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a0f-123">**Evento Player. comando**</span><span class="sxs-lookup"><span data-stu-id="c6a0f-123">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="c6a0f-124">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="c6a0f-124">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="c6a0f-125">**Uso del Reproductor de Windows Media con Netscape 7.1**</span><span class="sxs-lookup"><span data-stu-id="c6a0f-125">**Using Windows Media Player with Netscape 7.1**</span></span>](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





