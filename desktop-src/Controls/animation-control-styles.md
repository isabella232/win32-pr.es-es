---
title: Estilos de control de animación (CommCtrl. h)
description: En esta sección se enumeran los estilos de ventana utilizados con los controles de animación.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d779b92c51420bc6bd9ad238bcff538dbc85841f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660539"
---
# <a name="animation-control-styles"></a><span data-ttu-id="48771-103">Estilos de control de animación</span><span class="sxs-lookup"><span data-stu-id="48771-103">Animation Control Styles</span></span>

<span data-ttu-id="48771-104">En esta sección se enumeran los estilos de ventana utilizados con los controles de animación.</span><span class="sxs-lookup"><span data-stu-id="48771-104">This section lists the window styles used with animation controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="48771-105">Constante</span><span class="sxs-lookup"><span data-stu-id="48771-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="48771-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="48771-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <span data-ttu-id="48771-107"><dt><strong>ACS_AUTOPLAY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="48771-107"><dt><strong>ACS_AUTOPLAY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48771-108">Comienza a reproducir la animación en cuanto se abre el clip AVI.</span><span class="sxs-lookup"><span data-stu-id="48771-108">Starts playing the animation as soon as the AVI clip is opened.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <span data-ttu-id="48771-109"><dt><strong>ACS_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="48771-109"><dt><strong>ACS_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48771-110">Centra la animación en la ventana del control de animación.</span><span class="sxs-lookup"><span data-stu-id="48771-110">Centers the animation in the animation control's window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <span data-ttu-id="48771-111"><dt><strong>ACS_TIMER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="48771-111"><dt><strong>ACS_TIMER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48771-112">De forma predeterminada, el control crea un subproceso para reproducir el clip AVI.</span><span class="sxs-lookup"><span data-stu-id="48771-112">By default, the control creates a thread to play the AVI clip.</span></span> <span data-ttu-id="48771-113">Si establece esta marca, el control reproduce el clip sin crear un subproceso; internamente, el control usa un temporizador Win32 para sincronizar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="48771-113">If you set this flag, the control plays the clip without creating a thread; internally the control uses a Win32 timer to synchronize playback.</span></span> <br/> <span data-ttu-id="48771-114"><strong>Comctl32.dll versión 6 y posteriores:</strong> Este estilo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="48771-114"><strong>Comctl32.dll version 6 and later:</strong> This style is not supported.</span></span> <span data-ttu-id="48771-115">De forma predeterminada, el control reproduce el clip AVI sin crear un subproceso.</span><span class="sxs-lookup"><span data-stu-id="48771-115">By default, the control plays the AVI clip without creating a thread.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="48771-116">Comctl32.dll versión 6 no es redistribuible.</span><span class="sxs-lookup"><span data-stu-id="48771-116">Comctl32.dll version 6 is not redistributable.</span></span> <span data-ttu-id="48771-117">Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="48771-117">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="48771-118">Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.</span><span class="sxs-lookup"><span data-stu-id="48771-118">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <span data-ttu-id="48771-119"><dt><strong>ACS_TRANSPARENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="48771-119"><dt><strong>ACS_TRANSPARENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48771-120">Permite hacer coincidir el color de fondo de una animación con el de la ventana subyacente, creando un &quot; &quot; fondo transparente.</span><span class="sxs-lookup"><span data-stu-id="48771-120">Allows you to match an animation's background color to that of the underlying window, creating a &quot;transparent&quot; background.</span></span> <span data-ttu-id="48771-121">El elemento primario del control Animation no debe tener el estilo WS_CLIPCHILDREN (vea <a href="/windows/desktop/winmsg/window-styles">estilos de ventana</a>).</span><span class="sxs-lookup"><span data-stu-id="48771-121">The parent of the animation control must not have the WS_CLIPCHILDREN style (see <a href="/windows/desktop/winmsg/window-styles">Window Styles</a>).</span></span> <span data-ttu-id="48771-122">El control envía un mensaje <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> a su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="48771-122">The control sends a <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> message to its parent.</span></span> <span data-ttu-id="48771-123">Use <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> para establecer el color de fondo del contexto de dispositivo en un valor adecuado.</span><span class="sxs-lookup"><span data-stu-id="48771-123">Use <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> to set the background color for the device context to an appropriate value.</span></span> <span data-ttu-id="48771-124">El control interpreta el píxel superior izquierdo del primer fotograma como el color de fondo predeterminado de la animación.</span><span class="sxs-lookup"><span data-stu-id="48771-124">The control interprets the upper-left pixel of the first frame as the animation's default background color.</span></span> <span data-ttu-id="48771-125">Reasignará todos los píxeles con ese color al valor proporcionado en respuesta a WM_CTLCOLORSTATIC.</span><span class="sxs-lookup"><span data-stu-id="48771-125">It will remap all pixels with that color to the value you supplied in response to WM_CTLCOLORSTATIC.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="48771-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48771-126">Requirements</span></span>



| <span data-ttu-id="48771-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="48771-127">Requirement</span></span> | <span data-ttu-id="48771-128">Value</span><span class="sxs-lookup"><span data-stu-id="48771-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48771-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48771-129">Header</span></span><br/> | <dl> <span data-ttu-id="48771-130"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="48771-130"><dt>CommCtrl.h</dt></span></span> </dl> |



