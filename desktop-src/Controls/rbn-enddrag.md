---
title: Código de notificación de RBN_ENDDRAG (commctrl. h)
description: Lo envía un control Rebar cuando el usuario deja de arrastrar una banda. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 24b06144-6a4c-46a4-bef1-d6592f72a2c0
keywords:
- RBN_ENDDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb6c538679d793ed2407775b4238cea475ba4ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079555"
---
# <a name="rbn_enddrag-notification-code"></a><span data-ttu-id="2721c-105">Código de notificación de ENDDRAG de RBN \_</span><span class="sxs-lookup"><span data-stu-id="2721c-105">RBN\_ENDDRAG notification code</span></span>

<span data-ttu-id="2721c-106">Lo envía un control Rebar cuando el usuario deja de arrastrar una banda.</span><span class="sxs-lookup"><span data-stu-id="2721c-106">Sent by a rebar control when the user stops dragging a band.</span></span> <span data-ttu-id="2721c-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2721c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_ENDDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2721c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2721c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2721c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2721c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2721c-110">Puntero a una estructura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="2721c-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2721c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2721c-111">Return value</span></span>

<span data-ttu-id="2721c-112">No se utiliza el valor devuelto para este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="2721c-112">The return value for this notification code is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2721c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2721c-113">Requirements</span></span>



| <span data-ttu-id="2721c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2721c-114">Requirement</span></span> | <span data-ttu-id="2721c-115">Value</span><span class="sxs-lookup"><span data-stu-id="2721c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2721c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2721c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2721c-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2721c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2721c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2721c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2721c-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2721c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2721c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2721c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2721c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2721c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





