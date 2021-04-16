---
title: Valores de dibujo personalizados (CommCtrl. h)
description: En esta sección se enumeran los valores que se usan para identificar las partes de un control TrackBar.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649723"
---
# <a name="custom-draw-values"></a><span data-ttu-id="a2766-103">Valores de dibujo personalizados</span><span class="sxs-lookup"><span data-stu-id="a2766-103">Custom Draw Values</span></span>

<span data-ttu-id="a2766-104">En esta sección se enumeran los valores que se usan para identificar las partes de un control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a2766-104">This section lists the values used to identify a Trackbar control's parts.</span></span>



| <span data-ttu-id="a2766-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a2766-105">Constant</span></span>                                                                                                                                                   | <span data-ttu-id="a2766-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2766-106">Description</span></span>                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="a2766-107"><dt>**\_canal TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="a2766-107"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="a2766-108">Identifica el canal en el que se desplaza el marcador de control de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="a2766-108">Identifies the channel that the trackbar control's thumb marker slides along.</span></span><br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="a2766-109"><dt>**\_Thumb TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="a2766-109"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="a2766-110">Identifica el marcador de control de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="a2766-110">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="a2766-111">Esta es la parte del control que mueve el usuario.</span><span class="sxs-lookup"><span data-stu-id="a2766-111">This is the part of the control that the user moves.</span></span><br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="a2766-112"><dt>**TBCD \_ las marcas**</dt></span><span class="sxs-lookup"><span data-stu-id="a2766-112"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="a2766-113">Identifica las marcas de graduación que se muestran a lo largo del borde del control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a2766-113">Identifies the tick marks that are displayed along the trackbar control's edge.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="a2766-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2766-114">Remarks</span></span>

<span data-ttu-id="a2766-115">Los valores de dibujo personalizados, por ejemplo, se especifican en el miembro **dwItemSpec** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) .</span><span class="sxs-lookup"><span data-stu-id="a2766-115">Custom Draw values, for example, are specified in the **dwItemSpec** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2766-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2766-116">Requirements</span></span>



| <span data-ttu-id="a2766-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2766-117">Requirement</span></span> | <span data-ttu-id="a2766-118">Value</span><span class="sxs-lookup"><span data-stu-id="a2766-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2766-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2766-119">Header</span></span><br/> | <dl> <span data-ttu-id="a2766-120"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2766-120"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





