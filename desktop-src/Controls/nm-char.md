---
title: Código de notificación de NM_CHAR (commctrl. h)
description: '\_Un control envía el código de notificación nm char cuando se procesa una tecla de carácter. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.'
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658412"
---
# <a name="nm_char-notification-code"></a><span data-ttu-id="5268b-105">\_Código de notificación nm Char</span><span class="sxs-lookup"><span data-stu-id="5268b-105">NM\_CHAR notification code</span></span>

<span data-ttu-id="5268b-106">\_Un control envía el código de notificación nm char cuando se procesa una tecla de carácter.</span><span class="sxs-lookup"><span data-stu-id="5268b-106">The NM\_CHAR notification code is sent by a control when a character key is processed.</span></span> <span data-ttu-id="5268b-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5268b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5268b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5268b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5268b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5268b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5268b-110">Puntero a una estructura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contiene información adicional sobre el carácter que causó el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="5268b-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5268b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5268b-111">Return value</span></span>

<span data-ttu-id="5268b-112">La mayoría de los controles omiten el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="5268b-112">The return value is ignored by most controls.</span></span> <span data-ttu-id="5268b-113">Para obtener más información, consulte la documentación de los controles individuales.</span><span class="sxs-lookup"><span data-stu-id="5268b-113">For more information, see the documentation for the individual controls.</span></span>

## <a name="requirements"></a><span data-ttu-id="5268b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5268b-114">Requirements</span></span>



| <span data-ttu-id="5268b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5268b-115">Requirement</span></span> | <span data-ttu-id="5268b-116">Value</span><span class="sxs-lookup"><span data-stu-id="5268b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5268b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5268b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5268b-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5268b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5268b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5268b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5268b-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5268b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5268b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5268b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5268b-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5268b-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5268b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5268b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5268b-124">NM \_ Char (barra de herramientas)</span><span class="sxs-lookup"><span data-stu-id="5268b-124">NM\_CHAR (toolbar)</span></span>](nm-char-toolbar.md)
</dt> </dl>

 

 





