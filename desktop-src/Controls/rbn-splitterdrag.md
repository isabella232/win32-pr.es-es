---
title: Código de notificación de RBN_SPLITTERDRAG (commctrl. h)
description: Se envía por un control Rebar cuando el usuario arrastra un divisor. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 7827c971-6a92-452f-b961-1abe6ae66d2a
keywords:
- RBN_SPLITTERDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_SPLITTERDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b2d3fc00433be9cd3011f2f2b24d515b8cbd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534654"
---
# <a name="rbn_splitterdrag-notification-code"></a><span data-ttu-id="7bc44-105">Código de notificación de SPLITTERDRAG de RBN \_</span><span class="sxs-lookup"><span data-stu-id="7bc44-105">RBN\_SPLITTERDRAG notification code</span></span>

<span data-ttu-id="7bc44-106">Se envía por un control Rebar cuando el usuario arrastra un divisor.</span><span class="sxs-lookup"><span data-stu-id="7bc44-106">Sent by a rebar control when the user drags a splitter.</span></span> <span data-ttu-id="7bc44-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7bc44-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_SPLITTERDRAG

    lpnmrbspltr = (LPNMREBARSPLITTER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7bc44-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7bc44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bc44-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7bc44-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc44-110">Puntero a una estructura [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="7bc44-110">Pointer to an [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bc44-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7bc44-111">Return value</span></span>

<span data-ttu-id="7bc44-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="7bc44-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bc44-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bc44-113">Requirements</span></span>



| <span data-ttu-id="7bc44-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bc44-114">Requirement</span></span> | <span data-ttu-id="7bc44-115">Value</span><span class="sxs-lookup"><span data-stu-id="7bc44-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7bc44-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bc44-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7bc44-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7bc44-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7bc44-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bc44-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7bc44-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7bc44-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7bc44-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bc44-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bc44-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bc44-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





