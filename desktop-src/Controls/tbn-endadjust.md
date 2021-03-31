---
title: Código de notificación de TBN_ENDADJUST (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que el usuario ha detenido la personalización de una barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 9a7496ec-787d-4571-8eca-50d60383519b
keywords:
- TBN_ENDADJUST controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_ENDADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec420c535a207f02d12e17901efab1c18a11bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079262"
---
# <a name="tbn_endadjust-notification-code"></a><span data-ttu-id="358bc-105">Código de notificación de ENDADJUST de TBN \_</span><span class="sxs-lookup"><span data-stu-id="358bc-105">TBN\_ENDADJUST notification code</span></span>

<span data-ttu-id="358bc-106">Notifica a la ventana primaria de una barra de herramientas que el usuario ha detenido la personalización de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="358bc-106">Notifies a toolbar's parent window that the user has stopped customizing a toolbar.</span></span> <span data-ttu-id="358bc-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="358bc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="358bc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="358bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="358bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="358bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="358bc-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="358bc-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="358bc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="358bc-111">Return value</span></span>

<span data-ttu-id="358bc-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="358bc-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="358bc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="358bc-113">Requirements</span></span>



| <span data-ttu-id="358bc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="358bc-114">Requirement</span></span> | <span data-ttu-id="358bc-115">Value</span><span class="sxs-lookup"><span data-stu-id="358bc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="358bc-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="358bc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="358bc-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="358bc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="358bc-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="358bc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="358bc-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="358bc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="358bc-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="358bc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="358bc-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="358bc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





