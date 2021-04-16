---
title: Estilos de control SysLink (CommCtrl. h)
description: Al crear controles SysLink, se usan las constantes de estilo siguientes.
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 490a64a21ec81c1c91cc34ec8bebd2995476db4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649770"
---
# <a name="syslink-control-styles"></a><span data-ttu-id="13c45-103">Estilos del control SysLink</span><span class="sxs-lookup"><span data-stu-id="13c45-103">SysLink Control Styles</span></span>

<span data-ttu-id="13c45-104">Al crear controles SysLink, se usan las constantes de estilo siguientes.</span><span class="sxs-lookup"><span data-stu-id="13c45-104">The following style constants are used when creating SysLink controls.</span></span>



| <span data-ttu-id="13c45-105">Constante</span><span class="sxs-lookup"><span data-stu-id="13c45-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="13c45-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="13c45-106">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <span data-ttu-id="13c45-107"><dt>**\_transparente LWS**</dt></span><span class="sxs-lookup"><span data-stu-id="13c45-107"><dt>**LWS\_TRANSPARENT**</dt></span></span> </dl>             | <span data-ttu-id="13c45-108">El modo de combinación en segundo plano es transparente.</span><span class="sxs-lookup"><span data-stu-id="13c45-108">The background mix mode is transparent.</span></span> <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <span data-ttu-id="13c45-109"><dt>**LWS \_ IGNORERETURN**</dt></span><span class="sxs-lookup"><span data-stu-id="13c45-109"><dt>**LWS\_IGNORERETURN** </dt></span></span> </dl>       | <span data-ttu-id="13c45-110">Cuando el vínculo tiene el foco de teclado y el usuario presiona entrar, el control omite la pulsación de tecla y se pasa al cuadro de diálogo host.</span><span class="sxs-lookup"><span data-stu-id="13c45-110">When the link has keyboard focus and the user presses Enter, the keystroke is ignored by the control and passed to the host dialog box.</span></span><br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <span data-ttu-id="13c45-111"><dt>**LWS \_ NOprefix**</dt></span><span class="sxs-lookup"><span data-stu-id="13c45-111"><dt>**LWS\_NOPREFIX**</dt></span></span> </dl>                      | <span data-ttu-id="13c45-112">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="13c45-112">**Windows Vista**.</span></span> <span data-ttu-id="13c45-113">Si el texto contiene una y comercial, se trata como un carácter literal en lugar del prefijo de una tecla de método abreviado.</span><span class="sxs-lookup"><span data-stu-id="13c45-113">If the text contains an ampersand, it is treated as a literal character rather than the prefix to a shortcut key.</span></span><br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <span data-ttu-id="13c45-114"><dt>**LWS \_ USEVISUALSTYLE**</dt></span><span class="sxs-lookup"><span data-stu-id="13c45-114"><dt>**LWS\_USEVISUALSTYLE** </dt></span></span> </dl> | <span data-ttu-id="13c45-115">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="13c45-115">**Windows Vista**.</span></span> <span data-ttu-id="13c45-116">El vínculo se muestra en el estilo visual actual.</span><span class="sxs-lookup"><span data-stu-id="13c45-116">The link is displayed in the current visual style.</span></span><br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <span data-ttu-id="13c45-117"><dt>**LWS \_ USECUSTOMTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="13c45-117"><dt>**LWS\_USECUSTOMTEXT**</dt></span></span> </dl>       | <span data-ttu-id="13c45-118">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="13c45-118">**Windows Vista**.</span></span> <span data-ttu-id="13c45-119">Cuando se dibuja el control, se envía una notificación de [ \_ CUSTOMTEXT nm](nm-customtext.md) para que la aplicación pueda proporcionar texto de forma dinámica.</span><span class="sxs-lookup"><span data-stu-id="13c45-119">An [NM\_CUSTOMTEXT](nm-customtext.md) notification is sent when the control is drawn, so that the application can supply text dynamically.</span></span><br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <span data-ttu-id="13c45-120"><dt>**LWS \_ derecha**</dt></span><span class="sxs-lookup"><span data-stu-id="13c45-120"><dt>**LWS\_RIGHT**</dt></span></span> </dl>                               | <span data-ttu-id="13c45-121">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="13c45-121">**Windows Vista**.</span></span> <span data-ttu-id="13c45-122">El texto está justificado a la derecha.</span><span class="sxs-lookup"><span data-stu-id="13c45-122">The text is right-justified.</span></span><br/>                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="13c45-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13c45-123">Requirements</span></span>



| <span data-ttu-id="13c45-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="13c45-124">Requirement</span></span> | <span data-ttu-id="13c45-125">Value</span><span class="sxs-lookup"><span data-stu-id="13c45-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13c45-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13c45-126">Header</span></span><br/> | <dl> <span data-ttu-id="13c45-127"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="13c45-127"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





