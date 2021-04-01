---
title: Código de notificación de RBN_DELETINGBAND (commctrl. h)
description: Se envía por un control Rebar cuando una banda está a punto de eliminarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 92840cb1-375e-4c37-bde4-7ba02a1ff4f1
keywords:
- RBN_DELETINGBAND controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_DELETINGBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf810fd8800d7774a0dbf9a65cdf08c2d53d92ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996719"
---
# <a name="rbn_deletingband-notification-code"></a><span data-ttu-id="cc76d-105">Código de notificación de DELETINGBAND de RBN \_</span><span class="sxs-lookup"><span data-stu-id="cc76d-105">RBN\_DELETINGBAND notification code</span></span>

<span data-ttu-id="cc76d-106">Se envía por un control Rebar cuando una banda está a punto de eliminarse.</span><span class="sxs-lookup"><span data-stu-id="cc76d-106">Sent by a rebar control when a band is about to be deleted.</span></span> <span data-ttu-id="cc76d-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cc76d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETINGBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cc76d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc76d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc76d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc76d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc76d-110">Puntero a una estructura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="cc76d-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc76d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc76d-111">Return value</span></span>

<span data-ttu-id="cc76d-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="cc76d-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc76d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc76d-113">Requirements</span></span>



| <span data-ttu-id="cc76d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc76d-114">Requirement</span></span> | <span data-ttu-id="cc76d-115">Value</span><span class="sxs-lookup"><span data-stu-id="cc76d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc76d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc76d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cc76d-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cc76d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc76d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc76d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cc76d-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc76d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc76d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc76d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc76d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc76d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





