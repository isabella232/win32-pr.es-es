---
title: Estilos de información sobre herramientas (CommCtrl. h)
description: En esta sección se enumeran los estilos de control utilizados con controles ToolTip.
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8b89aed88caddceae815414b9f2b4d93a550c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649684"
---
# <a name="tooltip-styles"></a><span data-ttu-id="79366-103">Estilos de información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="79366-103">Tooltip Styles</span></span>

<span data-ttu-id="79366-104">En esta sección se enumeran los estilos de control utilizados con controles ToolTip.</span><span class="sxs-lookup"><span data-stu-id="79366-104">This section lists the control styles used with tooltip controls.</span></span>



| <span data-ttu-id="79366-105">Constante</span><span class="sxs-lookup"><span data-stu-id="79366-105">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="79366-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="79366-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <span data-ttu-id="79366-107"><dt>**ALWAYSTIP de TTS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="79366-107"><dt>**TTS\_ALWAYSTIP**</dt></span></span> </dl>                | <span data-ttu-id="79366-108">Indica que el control de información sobre herramientas aparece cuando el cursor está en una herramienta, incluso si la ventana propietaria del control de información sobre herramientas está inactiva.</span><span class="sxs-lookup"><span data-stu-id="79366-108">Indicates that the tooltip control appears when the cursor is on a tool, even if the tooltip control's owner window is inactive.</span></span> <span data-ttu-id="79366-109">Sin este estilo, la información sobre herramientas solo aparece cuando la ventana propietaria de la herramienta está activa.</span><span class="sxs-lookup"><span data-stu-id="79366-109">Without this style, the tooltip appears only when the tool's owner window is active.</span></span><br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <span data-ttu-id="79366-110"><dt>**globo de TTS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="79366-110"><dt>**TTS\_BALLOON**</dt></span></span> </dl>                      | <span data-ttu-id="79366-111">[Versión 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="79366-111">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="79366-112">Indica que el control ToolTip tiene la apariencia de un "globo" animado, con esquinas redondeadas y un tallo que apunta al elemento.</span><span class="sxs-lookup"><span data-stu-id="79366-112">Indicates that the tooltip control has the appearance of a cartoon "balloon," with rounded corners and a stem pointing to the item.</span></span> <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <span data-ttu-id="79366-113"><dt>**\_cerrar TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="79366-113"><dt>**TTS\_CLOSE**</dt></span></span> </dl>                            | <span data-ttu-id="79366-114">Muestra un botón **cerrar** en la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="79366-114">Displays a **Close** button on the tooltip.</span></span> <span data-ttu-id="79366-115">Solo es válido cuando la información sobre herramientas tiene el \_ estilo de globo TTS y un título; vea [**TTM \_ SETTITLE**](ttm-settitle.md).</span><span class="sxs-lookup"><span data-stu-id="79366-115">Valid only when the tooltip has the TTS\_BALLOON style and a title; see [**TTM\_SETTITLE**](ttm-settitle.md).</span></span><br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <span data-ttu-id="79366-116"><dt>**TTS \_ NOanimate**</dt></span><span class="sxs-lookup"><span data-stu-id="79366-116"><dt>**TTS\_NOANIMATE**</dt></span></span> </dl>                | <span data-ttu-id="79366-117">[Versión 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="79366-117">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="79366-118">Deshabilita la animación deslizante de la información sobre herramientas en los sistemas Windows 98 y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="79366-118">Disables sliding tooltip animation on Windows 98 and Windows 2000 systems.</span></span> <span data-ttu-id="79366-119">Este estilo se omite en sistemas anteriores.</span><span class="sxs-lookup"><span data-stu-id="79366-119">This style is ignored on earlier systems.</span></span><br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <span data-ttu-id="79366-120"><dt>**TTS \_ NOdesvanecese**</dt></span><span class="sxs-lookup"><span data-stu-id="79366-120"><dt>**TTS\_NOFADE**</dt></span></span> </dl>                         | <span data-ttu-id="79366-121">[Versión 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="79366-121">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="79366-122">Deshabilita la animación de la información sobre herramientas de atenuación.</span><span class="sxs-lookup"><span data-stu-id="79366-122">Disables fading tooltip animation.</span></span> <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <span data-ttu-id="79366-123"><dt>**TTS \_ NOprefix**</dt></span><span class="sxs-lookup"><span data-stu-id="79366-123"><dt>**TTS\_NOPREFIX**</dt></span></span> </dl>                   | <span data-ttu-id="79366-124">Impide que el sistema elimine los caracteres de y comercial de una cadena o que termine una cadena en un carácter de tabulación.</span><span class="sxs-lookup"><span data-stu-id="79366-124">Prevents the system from stripping ampersand characters from a string or terminating a string at a tab character.</span></span> <span data-ttu-id="79366-125">Sin este estilo, el sistema quita los caracteres de y comercial automáticamente y termina una cadena en el primer carácter de tabulación.</span><span class="sxs-lookup"><span data-stu-id="79366-125">Without this style, the system automatically strips ampersand characters and terminates a string at the first tab character.</span></span> <span data-ttu-id="79366-126">Esto permite que una aplicación use la misma cadena como un elemento de menú y como texto en un control de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="79366-126">This allows an application to use the same string as both a menu item and as text in a tooltip control.</span></span><br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <span data-ttu-id="79366-127"><dt>**USEVISUALSTYLE de TTS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="79366-127"><dt>**TTS\_USEVISUALSTYLE**</dt></span></span> </dl> | <span data-ttu-id="79366-128">Utiliza hipervínculos con los mismos.</span><span class="sxs-lookup"><span data-stu-id="79366-128">Uses themed hyperlinks.</span></span> <span data-ttu-id="79366-129">El tema definirá los estilos para los vínculos de la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="79366-129">The theme will define the styles for any links in the tooltip.</span></span> <span data-ttu-id="79366-130">Este estilo siempre requiere \_ que se establezca ttf PARSELINKS.</span><span class="sxs-lookup"><span data-stu-id="79366-130">This style always requires TTF\_PARSELINKS to be set.</span></span> <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="79366-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79366-131">Remarks</span></span>

<span data-ttu-id="79366-132">Un control de información sobre herramientas siempre tiene los \_ estilos del elemento emergente WS y \_ de la \_ ventana de la ventana de herramientas de WS ex, independientemente de si se especifican al crear el control.</span><span class="sxs-lookup"><span data-stu-id="79366-132">A tooltip control always has the WS\_POPUP and WS\_EX\_TOOLWINDOW window styles, regardless of whether you specify them when creating the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="79366-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79366-133">Requirements</span></span>



| <span data-ttu-id="79366-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="79366-134">Requirement</span></span> | <span data-ttu-id="79366-135">Value</span><span class="sxs-lookup"><span data-stu-id="79366-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79366-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79366-136">Header</span></span><br/> | <dl> <span data-ttu-id="79366-137"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="79366-137"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





