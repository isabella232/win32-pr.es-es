---
title: Código de notificación de TBN_HOTITEMCHANGE (commctrl. h)
description: Se envía por un control de barra de herramientas cuando cambia el elemento activo (resaltado). Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- TBN_HOTITEMCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801069"
---
# <a name="tbn_hotitemchange-notification-code"></a><span data-ttu-id="9516a-105">Código de notificación de HOTITEMCHANGE de TBN \_</span><span class="sxs-lookup"><span data-stu-id="9516a-105">TBN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="9516a-106">Se envía por un control de barra de herramientas cuando cambia el elemento activo (resaltado).</span><span class="sxs-lookup"><span data-stu-id="9516a-106">Sent by a toolbar control when the hot (highlighted) item changes.</span></span> <span data-ttu-id="9516a-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9516a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9516a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9516a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9516a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9516a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9516a-110">Puntero a una estructura [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="9516a-110">Pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9516a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9516a-111">Return value</span></span>

<span data-ttu-id="9516a-112">Devuelve cero para permitir que se resalte el elemento, o un valor distinto de cero, para evitar que se resalte el elemento.</span><span class="sxs-lookup"><span data-stu-id="9516a-112">Return zero to allow the item to be highlighted, or nonzero to prevent the item from being highlighted.</span></span>

## <a name="requirements"></a><span data-ttu-id="9516a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9516a-113">Requirements</span></span>



| <span data-ttu-id="9516a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9516a-114">Requirement</span></span> | <span data-ttu-id="9516a-115">Value</span><span class="sxs-lookup"><span data-stu-id="9516a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9516a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9516a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9516a-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9516a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9516a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9516a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9516a-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9516a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9516a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9516a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9516a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9516a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





