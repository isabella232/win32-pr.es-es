---
title: NM_NCHITTEST de notificación (rebar) (Commctrl.h)
description: 'NM_NCHITTEST de notificación (rebar): enviado por un control rebar cuando el control recibe un mensaje \_ WM NCHITTEST. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.'
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- NM_NCHITTEST de notificación (rebar) Controles de Windows
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7935f1b3e990db55518c9d22537e8fb6db97962
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112333"
---
# <a name="nm_nchittest-rebar-notification-code"></a><span data-ttu-id="e311e-105">Código \_ de notificación de NM NCHITTEST (rebar)</span><span class="sxs-lookup"><span data-stu-id="e311e-105">NM\_NCHITTEST (rebar) notification code</span></span>

<span data-ttu-id="e311e-106">Enviado por un control rebar cuando el control recibe un [**mensaje \_ WM NCHITTEST.**](/windows/desktop/inputdev/wm-nchittest)</span><span class="sxs-lookup"><span data-stu-id="e311e-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="e311e-107">Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="e311e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e311e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e311e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e311e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e311e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e311e-110">Puntero a una [**estructura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="e311e-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="e311e-111">El **miembro dwItemSpec** contiene el índice de banda sobre el que se produjo el mensaje de la prueba de impacto, y el miembro **pt** contiene las coordenadas del mouse del mensaje de la prueba de impacto.</span><span class="sxs-lookup"><span data-stu-id="e311e-111">The **dwItemSpec** member contains the band index over which the hit test message occurred, and the **pt** member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e311e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e311e-112">Return value</span></span>

<span data-ttu-id="e311e-113">Devuelve cero para permitir que la barra de rebar realice el procesamiento predeterminado del mensaje de la prueba de acceso o devuelva uno de los valores ht documentados en \* [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) para invalidar el procesamiento predeterminado de la prueba de acceso.</span><span class="sxs-lookup"><span data-stu-id="e311e-113">Return zero to allow the rebar to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e311e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e311e-114">Requirements</span></span>



| <span data-ttu-id="e311e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e311e-115">Requirement</span></span> | <span data-ttu-id="e311e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e311e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e311e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e311e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e311e-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e311e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e311e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e311e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e311e-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e311e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e311e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e311e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e311e-122"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="e311e-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

