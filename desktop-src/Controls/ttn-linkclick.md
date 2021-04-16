---
title: Código de notificación de TTN_LINKCLICK (commctrl. h)
description: Se envía cuando se hace clic en un vínculo de texto dentro de una información sobre herramientas de globo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658231"
---
# <a name="ttn_linkclick-notification-code"></a><span data-ttu-id="e2925-105">Código de notificación de LINKCLICK de TTN \_</span><span class="sxs-lookup"><span data-stu-id="e2925-105">TTN\_LINKCLICK notification code</span></span>

<span data-ttu-id="e2925-106">Se envía cuando se hace clic en un vínculo de texto dentro de una información sobre herramientas de globo.</span><span class="sxs-lookup"><span data-stu-id="e2925-106">Sent when a text link inside a balloon tooltip is clicked.</span></span> <span data-ttu-id="e2925-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e2925-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a><span data-ttu-id="e2925-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2925-108">Parameters</span></span>

<span data-ttu-id="e2925-109">Este código de notificación no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e2925-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2925-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2925-110">Return value</span></span>

<span data-ttu-id="e2925-111">No se usa el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e2925-111">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2925-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2925-112">Remarks</span></span>

<span data-ttu-id="e2925-113">El siguiente es un ejemplo de Cuándo se envía esta notificación.</span><span class="sxs-lookup"><span data-stu-id="e2925-113">Following is an example of when this notification is sent.</span></span> <span data-ttu-id="e2925-114">Supongamos que la información sobre herramientas de globo contiene el texto siguiente, "este es un <A>vínculo</A>".</span><span class="sxs-lookup"><span data-stu-id="e2925-114">Assume that your balloon tooltip contains the following text, "This is a <A>link</A>".</span></span> <span data-ttu-id="e2925-115">Cuando se hace clic en "link", el control ToolTip envía un \_ código de notificación TTN LINKCLICK.</span><span class="sxs-lookup"><span data-stu-id="e2925-115">When "link" is clicked, the tooltip control sends a TTN\_LINKCLICK notification code.</span></span>

> [!Note]  
> <span data-ttu-id="e2925-116">Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="e2925-116">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e2925-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e2925-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2925-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2925-118">Requirements</span></span>



| <span data-ttu-id="e2925-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2925-119">Requirement</span></span> | <span data-ttu-id="e2925-120">Value</span><span class="sxs-lookup"><span data-stu-id="e2925-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2925-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2925-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e2925-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e2925-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2925-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2925-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e2925-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2925-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2925-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2925-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2925-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2925-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





