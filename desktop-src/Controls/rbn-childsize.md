---
title: Código de notificación de RBN_CHILDSIZE (commctrl. h)
description: Se envía por un control Rebar cuando se cambia el tamaño de la ventana secundaria de una banda. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ba64d21a-e568-4894-8007-be644ae4f54a
keywords:
- RBN_CHILDSIZE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_CHILDSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d505d13048d96783d53b9b1a821d80712597da4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905352"
---
# <a name="rbn_childsize-notification-code"></a><span data-ttu-id="c6240-105">Código de notificación de CHILDSIZE de RBN \_</span><span class="sxs-lookup"><span data-stu-id="c6240-105">RBN\_CHILDSIZE notification code</span></span>

<span data-ttu-id="c6240-106">Se envía por un control Rebar cuando se cambia el tamaño de la ventana secundaria de una banda.</span><span class="sxs-lookup"><span data-stu-id="c6240-106">Sent by a rebar control when a band's child window is resized.</span></span> <span data-ttu-id="c6240-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c6240-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHILDSIZE

    lprbcs = (LPNMREBARCHILDSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c6240-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6240-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6240-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6240-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6240-110">Puntero a una estructura [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="c6240-110">Pointer to an [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6240-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6240-111">Return value</span></span>

<span data-ttu-id="c6240-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="c6240-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6240-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6240-113">Requirements</span></span>



| <span data-ttu-id="c6240-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6240-114">Requirement</span></span> | <span data-ttu-id="c6240-115">Value</span><span class="sxs-lookup"><span data-stu-id="c6240-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6240-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6240-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c6240-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c6240-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6240-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6240-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c6240-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6240-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6240-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6240-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6240-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6240-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





