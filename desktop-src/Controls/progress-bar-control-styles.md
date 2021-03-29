---
title: Estilos de control de barra de progreso (CommCtrl. h)
description: Los controles de barra de progreso admiten los siguientes estilos de control
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660559"
---
# <a name="progress-bar-control-styles"></a><span data-ttu-id="89610-103">Estilos de control de barra de progreso</span><span class="sxs-lookup"><span data-stu-id="89610-103">Progress Bar Control Styles</span></span>

<span data-ttu-id="89610-104">Los controles de [barra de progreso](progress-bar-control.md) admiten los siguientes estilos de control:</span><span class="sxs-lookup"><span data-stu-id="89610-104">The following control styles are supported by [Progress Bar](progress-bar-control.md) controls:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="89610-105">Constante</span><span class="sxs-lookup"><span data-stu-id="89610-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="89610-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="89610-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <span data-ttu-id="89610-107"><dt><strong>PBS_MARQUEE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="89610-107"><dt><strong>PBS_MARQUEE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="89610-108"><a href="common-control-versions.md">Versión 6,0</a> o posterior.</span><span class="sxs-lookup"><span data-stu-id="89610-108"><a href="common-control-versions.md">Version 6.0</a> or later.</span></span> <span data-ttu-id="89610-109">El indicador de progreso no aumenta de tamaño, sino que se mueve repetidamente a lo largo de la longitud de la barra, lo que indica una actividad sin especificar la proporción del progreso que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="89610-109">The progress indicator does not grow in size but instead moves repeatedly along the length of the bar, indicating activity without specifying what proportion of the progress is complete.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89610-110">Comctl32.dll versión 6 no es redistribuible, pero se incluye en Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="89610-110">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="89610-111">Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="89610-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="89610-112">Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.</span><span class="sxs-lookup"><span data-stu-id="89610-112">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <span data-ttu-id="89610-113"><dt><strong>PBS_SMOOTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="89610-113"><dt><strong>PBS_SMOOTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="89610-114"><a href="common-control-versions.md">Versión 4,70</a> o posterior.</span><span class="sxs-lookup"><span data-stu-id="89610-114"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="89610-115">La barra de progreso muestra el estado del progreso en una barra de desplazamiento suave en lugar de en la barra segmentada predeterminada.</span><span class="sxs-lookup"><span data-stu-id="89610-115">The progress bar displays progress status in a smooth scrolling bar instead of the default segmented bar.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89610-116">Este estilo solo se admite en el tema clásico de Windows.</span><span class="sxs-lookup"><span data-stu-id="89610-116">This style is supported only in the Windows Classic theme.</span></span> <span data-ttu-id="89610-117">Todos los demás temas invalidan este estilo.</span><span class="sxs-lookup"><span data-stu-id="89610-117">All other themes override this style.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <span data-ttu-id="89610-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="89610-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="89610-119"><a href="common-control-versions.md">Versión 6,0</a> o posterior y <strong>Windows Vista.</strong></span><span class="sxs-lookup"><span data-stu-id="89610-119"><a href="common-control-versions.md">Version 6.0</a> or later and <strong>Windows Vista.</strong></span></span> <span data-ttu-id="89610-120">Determina el comportamiento de animación que la barra de progreso debe utilizar al retroceder (de un valor superior a un valor inferior).</span><span class="sxs-lookup"><span data-stu-id="89610-120">Determines the animation behavior that the progress bar should use when moving backward (from a higher value to a lower value).</span></span> <span data-ttu-id="89610-121">Si se establece, se &quot; &quot; producirá una transición suave; de lo contrario, el control &quot; saltará &quot; al valor inferior.</span><span class="sxs-lookup"><span data-stu-id="89610-121">If this is set, then a &quot;smooth&quot; transition will occur, otherwise the control will &quot;jump&quot; to the lower value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <span data-ttu-id="89610-122"><dt><strong>PBS_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="89610-122"><dt><strong>PBS_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="89610-123"><a href="common-control-versions.md">Versión 4,70</a> o posterior.</span><span class="sxs-lookup"><span data-stu-id="89610-123"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="89610-124">La barra de progreso muestra el estado de progreso verticalmente, de abajo a arriba.</span><span class="sxs-lookup"><span data-stu-id="89610-124">The progress bar displays progress status vertically, from bottom to top.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="89610-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89610-125">Remarks</span></span>

<span data-ttu-id="89610-126">Puede establecer estilos de barra de progreso, de la misma manera que otros controles comunes, con [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="89610-126">You can set progress bar styles, in the same way as other common controls, with [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga), or [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="89610-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89610-127">Requirements</span></span>



| <span data-ttu-id="89610-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="89610-128">Requirement</span></span> | <span data-ttu-id="89610-129">Value</span><span class="sxs-lookup"><span data-stu-id="89610-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89610-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89610-130">Header</span></span><br/> | <dl> <span data-ttu-id="89610-131"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="89610-131"><dt>CommCtrl.h</dt></span></span> </dl> |



 

