---
title: Código de notificación de TBN_BEGINADJUST (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que el usuario ha empezado a personalizar una barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 689aeda3-5051-4422-9e66-64557b263943
keywords:
- TBN_BEGINADJUST controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_BEGINADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4708cd205461e3117432cec25e0e4256a6b0d87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905105"
---
# <a name="tbn_beginadjust-notification-code"></a><span data-ttu-id="b4f12-105">Código de notificación de BEGINADJUST de TBN \_</span><span class="sxs-lookup"><span data-stu-id="b4f12-105">TBN\_BEGINADJUST notification code</span></span>

<span data-ttu-id="b4f12-106">Notifica a la ventana primaria de una barra de herramientas que el usuario ha empezado a personalizar una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="b4f12-106">Notifies a toolbar's parent window that the user has begun customizing a toolbar.</span></span> <span data-ttu-id="b4f12-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b4f12-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_BEGINADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b4f12-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4f12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4f12-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4f12-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4f12-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="b4f12-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4f12-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4f12-111">Return value</span></span>

<span data-ttu-id="b4f12-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b4f12-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f12-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4f12-113">Requirements</span></span>



| <span data-ttu-id="b4f12-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4f12-114">Requirement</span></span> | <span data-ttu-id="b4f12-115">Value</span><span class="sxs-lookup"><span data-stu-id="b4f12-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f12-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4f12-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b4f12-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b4f12-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4f12-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4f12-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b4f12-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4f12-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4f12-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4f12-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4f12-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4f12-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





