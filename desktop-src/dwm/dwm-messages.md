---
title: Mensajes DWM
description: Esta sección contiene información sobre los mensajes de Administrador de ventanas de escritorio (DWM).
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Administrador de ventanas de escritorio (DWM), referencia
- DWM (Administrador de ventanas de escritorio), referencia
- Administrador de ventanas de escritorio (DWM), mensajes
- DWM (Administrador de ventanas de escritorio), mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "105714323"
---
# <a name="dwm-messages"></a><span data-ttu-id="3f85f-107">Mensajes DWM</span><span class="sxs-lookup"><span data-stu-id="3f85f-107">DWM Messages</span></span>

<span data-ttu-id="3f85f-108">Esta sección contiene información sobre los mensajes de Administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="3f85f-108">This section contains information about the Desktop Window Manager (DWM) messages.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3f85f-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3f85f-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f85f-110">Tema</span><span class="sxs-lookup"><span data-stu-id="3f85f-110">Topic</span></span></th>
<th><span data-ttu-id="3f85f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f85f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3f85f-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f85f-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="3f85f-113">Informa a todas las ventanas de nivel superior que el color de coloración ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3f85f-113">Informs all top-level windows that the colorization color has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f85f-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f85f-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="3f85f-115">Informa a todas las ventanas de nivel superior que la composición DWM se ha habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="3f85f-115">Informs all top-level windows that DWM composition has been enabled or disabled.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3f85f-116">A partir de Windows 8, la composición DWM siempre está habilitada, por lo que este mensaje no se envía independientemente de los cambios en el modo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3f85f-116">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f85f-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f85f-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="3f85f-118">Se envía cuando cambia la Directiva de representación del área que no es de cliente.</span><span class="sxs-lookup"><span data-stu-id="3f85f-118">Sent when the non-client area rendering policy has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f85f-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f85f-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span></span><br/></td>
<td><span data-ttu-id="3f85f-120">Indica a una ventana que proporcione un mapa de bits estático para usarlo como <em>vista previa dinámica</em> (también conocida como <em>vista previa de PEEK</em>) de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="3f85f-120">Instructs a window to provide a static bitmap to use as a <em>live preview</em> (also known as a <em>Peek preview</em>) of that window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f85f-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f85f-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span></span><br/></td>
<td><span data-ttu-id="3f85f-122">Indica a una ventana que proporcione un mapa de bits estático para usarlo como representación en miniatura de la ventana.</span><span class="sxs-lookup"><span data-stu-id="3f85f-122">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f85f-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f85f-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="3f85f-124">Se envía cuando una ventana compuesta de DWM está maximizada.</span><span class="sxs-lookup"><span data-stu-id="3f85f-124">Sent when a DWM composed window is maximized.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





