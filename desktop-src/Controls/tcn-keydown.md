---
title: Código de notificación de TCN_KEYDOWN (commctrl. h)
description: Notifica a la ventana primaria de un control de pestaña que se ha presionado una tecla. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 884e79cd-5732-44cd-8c7a-38bb9349ec7d
keywords:
- TCN_KEYDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TCN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1e963b11faf8f75e50e86e8c120ea0b05f0dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656455"
---
# <a name="tcn_keydown-notification-code"></a><span data-ttu-id="86bb5-105">\_Código de notificación KEYDOWN de TCN</span><span class="sxs-lookup"><span data-stu-id="86bb5-105">TCN\_KEYDOWN notification code</span></span>

<span data-ttu-id="86bb5-106">Notifica a la ventana primaria de un control de pestaña que se ha presionado una tecla.</span><span class="sxs-lookup"><span data-stu-id="86bb5-106">Notifies a tab control's parent window that a key has been pressed.</span></span> <span data-ttu-id="86bb5-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="86bb5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_KEYDOWN 

    pnm = (NMTCKEYDOWN*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="86bb5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86bb5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86bb5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86bb5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86bb5-110">Puntero a una estructura [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) .</span><span class="sxs-lookup"><span data-stu-id="86bb5-110">Pointer to an [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86bb5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86bb5-111">Return value</span></span>

<span data-ttu-id="86bb5-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="86bb5-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="86bb5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86bb5-113">Requirements</span></span>



| <span data-ttu-id="86bb5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="86bb5-114">Requirement</span></span> | <span data-ttu-id="86bb5-115">Value</span><span class="sxs-lookup"><span data-stu-id="86bb5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86bb5-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86bb5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="86bb5-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="86bb5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86bb5-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86bb5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="86bb5-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="86bb5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86bb5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86bb5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="86bb5-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="86bb5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





