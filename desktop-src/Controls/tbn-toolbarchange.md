---
title: Código de notificación de TBN_TOOLBARCHANGE (commctrl. h)
description: Notifica a la ventana primaria de la barra de herramientas que el usuario ha personalizado una barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 6c5127e6-391f-4592-8547-4cc3d3ed6cf0
keywords:
- TBN_TOOLBARCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_TOOLBARCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9c533a7a26dd1ed0f1938e6c5138bbae13c31f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996796"
---
# <a name="tbn_toolbarchange-notification-code"></a><span data-ttu-id="ac0c2-105">Código de notificación de TOOLBARCHANGE de TBN \_</span><span class="sxs-lookup"><span data-stu-id="ac0c2-105">TBN\_TOOLBARCHANGE notification code</span></span>

<span data-ttu-id="ac0c2-106">Notifica a la ventana primaria de la barra de herramientas que el usuario ha personalizado una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-106">Notifies the toolbar's parent window that the user has customized a toolbar.</span></span> <span data-ttu-id="ac0c2-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ac0c2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_TOOLBARCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ac0c2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac0c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac0c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac0c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac0c2-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac0c2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac0c2-111">Return value</span></span>

<span data-ttu-id="ac0c2-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac0c2-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac0c2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac0c2-113">Requirements</span></span>



| <span data-ttu-id="ac0c2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac0c2-114">Requirement</span></span> | <span data-ttu-id="ac0c2-115">Value</span><span class="sxs-lookup"><span data-stu-id="ac0c2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac0c2-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac0c2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ac0c2-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ac0c2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac0c2-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac0c2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ac0c2-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac0c2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac0c2-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac0c2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac0c2-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac0c2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





