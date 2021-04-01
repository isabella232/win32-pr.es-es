---
title: Código de notificación de RBN_DELETEDBAND (commctrl. h)
description: Lo envía un control rebar después de que se haya eliminado una banda. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ef4aca07-de08-47de-b236-321e84e6e81c
keywords:
- RBN_DELETEDBAND controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_DELETEDBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af4e107ccb1a42b82335255f48d0328e03019a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905416"
---
# <a name="rbn_deletedband-notification-code"></a><span data-ttu-id="2e4a4-105">Código de notificación de DELETEDBAND de RBN \_</span><span class="sxs-lookup"><span data-stu-id="2e4a4-105">RBN\_DELETEDBAND notification code</span></span>

<span data-ttu-id="2e4a4-106">Lo envía un control rebar después de que se haya eliminado una banda.</span><span class="sxs-lookup"><span data-stu-id="2e4a4-106">Sent by a rebar control after a band has been deleted.</span></span> <span data-ttu-id="2e4a4-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2e4a4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETEDBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2e4a4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e4a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e4a4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e4a4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e4a4-110">Puntero a una estructura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="2e4a4-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e4a4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e4a4-111">Return value</span></span>

<span data-ttu-id="2e4a4-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="2e4a4-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e4a4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e4a4-113">Requirements</span></span>



| <span data-ttu-id="2e4a4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e4a4-114">Requirement</span></span> | <span data-ttu-id="2e4a4-115">Value</span><span class="sxs-lookup"><span data-stu-id="2e4a4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4a4-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e4a4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e4a4-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2e4a4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e4a4-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e4a4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e4a4-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e4a4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e4a4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e4a4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e4a4-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e4a4-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





