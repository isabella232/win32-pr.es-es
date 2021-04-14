---
title: Mensaje de TBN_DELETINGBUTTON (commctrl. h)
description: Se envía por un control de barra de herramientas cuando un botón está a punto de eliminarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- TBN_DELETINGBUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26337fd1abc6c67351fe2b38e83ee7d90a11f6e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533897"
---
# <a name="tbn_deletingbutton-message"></a><span data-ttu-id="8e31b-105">TBN \_ DELETINGBUTTON</span><span class="sxs-lookup"><span data-stu-id="8e31b-105">TBN\_DELETINGBUTTON message</span></span>

<span data-ttu-id="8e31b-106">Se envía por un control de barra de herramientas cuando un botón está a punto de eliminarse.</span><span class="sxs-lookup"><span data-stu-id="8e31b-106">Sent by a toolbar control when a button is about to be deleted.</span></span> <span data-ttu-id="8e31b-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8e31b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8e31b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e31b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e31b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e31b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e31b-110">Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contiene información sobre el botón que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="8e31b-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about the button being deleted.</span></span> <span data-ttu-id="8e31b-111">En este código de notificación, solo son válidos los miembros **HDR** y **iItem** de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="8e31b-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="8e31b-112">El miembro **iItem** de esta estructura contiene el identificador de comando del botón que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="8e31b-112">The **iItem** member of this structure contains the command identifier of the button being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e31b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e31b-113">Return value</span></span>

<span data-ttu-id="8e31b-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="8e31b-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e31b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e31b-115">Requirements</span></span>



| <span data-ttu-id="8e31b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e31b-116">Requirement</span></span> | <span data-ttu-id="8e31b-117">Value</span><span class="sxs-lookup"><span data-stu-id="8e31b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e31b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e31b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8e31b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8e31b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e31b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e31b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8e31b-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e31b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e31b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e31b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e31b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e31b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





