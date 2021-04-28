---
title: NM_NCHITTEST de notificación (Commctrl.h)
description: 'NM_NCHITTEST de notificación: se envía mediante un control rebar cuando el control recibe un mensaje \_ WM NCHITTEST. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.'
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST código de notificación controles de Windows
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
ms.openlocfilehash: 68ede0ac017fbe5146cd68e51e2a38c7f66c7898
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112323"
---
# <a name="nm_nchittest-notification-code"></a><span data-ttu-id="151b5-105">Código de \_ notificación de NM NCHITTEST</span><span class="sxs-lookup"><span data-stu-id="151b5-105">NM\_NCHITTEST notification code</span></span>

<span data-ttu-id="151b5-106">Enviado por un control rebar cuando el control recibe un [**mensaje \_ WM NCHITTEST.**](/windows/desktop/inputdev/wm-nchittest)</span><span class="sxs-lookup"><span data-stu-id="151b5-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="151b5-107">Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="151b5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="151b5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="151b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="151b5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="151b5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="151b5-110">Puntero a una [**estructura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="151b5-110">A pointer to a [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="151b5-111">El *miembro pt* contiene las coordenadas del mouse del mensaje de la prueba de impacto.</span><span class="sxs-lookup"><span data-stu-id="151b5-111">The *pt* member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="151b5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="151b5-112">Return value</span></span>

<span data-ttu-id="151b5-113">A menos que se especifique lo contrario, devuelva cero para permitir que el control realice el procesamiento predeterminado del mensaje de la prueba de acceso o devuelva uno de los valores ht documentados en \* [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) para invalidar el procesamiento predeterminado de la prueba de acceso.</span><span class="sxs-lookup"><span data-stu-id="151b5-113">Unless otherwise specified, return zero to allow the control to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="151b5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="151b5-114">Requirements</span></span>



| <span data-ttu-id="151b5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="151b5-115">Requirement</span></span> | <span data-ttu-id="151b5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="151b5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="151b5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="151b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="151b5-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="151b5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="151b5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="151b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="151b5-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="151b5-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="151b5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="151b5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="151b5-122"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="151b5-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

