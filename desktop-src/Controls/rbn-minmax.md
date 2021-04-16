---
title: Código de notificación de RBN_MINMAX (commctrl. h)
description: Se envía por un control rebar antes de maximizar o minimizar una banda. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- RBN_MINMAX controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658219"
---
# <a name="rbn_minmax-notification-code"></a><span data-ttu-id="3dc6f-105">Código de notificación de MinMax de RBN \_</span><span class="sxs-lookup"><span data-stu-id="3dc6f-105">RBN\_MINMAX notification code</span></span>

<span data-ttu-id="3dc6f-106">Se envía por un control rebar antes de maximizar o minimizar una banda.</span><span class="sxs-lookup"><span data-stu-id="3dc6f-106">Sent by a rebar control prior to maximizing or minimizing a band.</span></span> <span data-ttu-id="3dc6f-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3dc6f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_MINMAX
```



## <a name="parameters"></a><span data-ttu-id="3dc6f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3dc6f-108">Parameters</span></span>

<span data-ttu-id="3dc6f-109">Este código de notificación no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3dc6f-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3dc6f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3dc6f-110">Return value</span></span>

<span data-ttu-id="3dc6f-111">Devuelve un valor distinto de cero para evitar que la operación tenga lugar, cero para permitir que continúe.</span><span class="sxs-lookup"><span data-stu-id="3dc6f-111">Return a nonzero value to prevent the operation from taking place, zero to allow it to continue.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc6f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dc6f-112">Requirements</span></span>



| <span data-ttu-id="3dc6f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dc6f-113">Requirement</span></span> | <span data-ttu-id="3dc6f-114">Value</span><span class="sxs-lookup"><span data-stu-id="3dc6f-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc6f-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dc6f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3dc6f-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3dc6f-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3dc6f-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dc6f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3dc6f-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3dc6f-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3dc6f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3dc6f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dc6f-120"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dc6f-120"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





