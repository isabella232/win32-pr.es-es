---
title: Estados de elemento de control de pestaña (CommCtrl. h)
description: Los elementos de control de pestaña ahora admiten un estado de elemento para admitir el \_ mensaje DESELECTALL de TCM. Además, la estructura TCITEM admite valores de estado del elemento.
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660471"
---
# <a name="tab-control-item-states"></a><span data-ttu-id="a6337-104">Estados de elemento de control de pestaña</span><span class="sxs-lookup"><span data-stu-id="a6337-104">Tab Control Item States</span></span>

<span data-ttu-id="a6337-105">Los elementos de control de pestaña ahora admiten un estado de elemento para admitir el mensaje [**\_ DESELECTALL de TCM**](tcm-deselectall.md) .</span><span class="sxs-lookup"><span data-stu-id="a6337-105">Tab control items now support an item state to support the [**TCM\_DESELECTALL**](tcm-deselectall.md) message.</span></span> <span data-ttu-id="a6337-106">Además, la estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) admite valores de estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="a6337-106">Additionally, the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure supports item state values.</span></span>



| <span data-ttu-id="a6337-107">Constante</span><span class="sxs-lookup"><span data-stu-id="a6337-107">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="a6337-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6337-108">Description</span></span>                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <span data-ttu-id="a6337-109"><dt>**TCIS \_ BUTTONPRESSED**</dt></span><span class="sxs-lookup"><span data-stu-id="a6337-109"><dt>**TCIS\_BUTTONPRESSED**</dt></span></span> </dl> | <span data-ttu-id="a6337-110">[Versión 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a6337-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="a6337-111">Se selecciona el elemento de control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="a6337-111">The tab control item is selected.</span></span> <span data-ttu-id="a6337-112">Este estado solo es significativo si se ha establecido la marca de estilo [**\_ botones de TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a6337-112">This state is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span><br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <span data-ttu-id="a6337-113"><dt>**TCIS \_ resaltado**</dt></span><span class="sxs-lookup"><span data-stu-id="a6337-113"><dt>**TCIS\_HIGHLIGHTED**</dt></span></span> </dl>       | <span data-ttu-id="a6337-114">[Versión 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a6337-114">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="a6337-115">Se resalta el elemento de control de pestaña y la pestaña y el texto se dibujan con el color de resaltado actual.</span><span class="sxs-lookup"><span data-stu-id="a6337-115">The tab control item is highlighted, and the tab and text are drawn using the current highlight color.</span></span> <span data-ttu-id="a6337-116">Cuando se usa el color de alta densidad, se trata de una interpolación verdadera, no de un color interpolado.</span><span class="sxs-lookup"><span data-stu-id="a6337-116">When using high-color, this will be a true interpolation, not a dithered color.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a6337-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6337-117">Requirements</span></span>



| <span data-ttu-id="a6337-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6337-118">Requirement</span></span> | <span data-ttu-id="a6337-119">Value</span><span class="sxs-lookup"><span data-stu-id="a6337-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6337-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6337-120">Header</span></span><br/> | <dl> <span data-ttu-id="a6337-121"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6337-121"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





