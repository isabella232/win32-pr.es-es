---
title: Código de notificación de CBEN_BEGINEDIT (commctrl. h)
description: Se envía cuando el usuario activa la lista desplegable o hace clic en el cuadro de edición del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 77236471-b1c0-4679-b7b8-93e85867fe3b
keywords:
- CBEN_BEGINEDIT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBEN_BEGINEDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d4cc80d12b01b9374173f413f0aee3701e5040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658361"
---
# <a name="cben_beginedit-notification-code"></a><span data-ttu-id="63437-105">Código de notificación de CBEN \_ BEGINEDIT</span><span class="sxs-lookup"><span data-stu-id="63437-105">CBEN\_BEGINEDIT notification code</span></span>

<span data-ttu-id="63437-106">Se envía cuando el usuario activa la lista desplegable o hace clic en el cuadro de edición del control.</span><span class="sxs-lookup"><span data-stu-id="63437-106">Sent when the user activates the drop-down list or clicks in the control's edit box.</span></span> <span data-ttu-id="63437-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="63437-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_BEGINEDIT

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="63437-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63437-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63437-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63437-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63437-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="63437-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63437-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63437-111">Return value</span></span>

<span data-ttu-id="63437-112">El procesamiento de la aplicación en este código de notificación debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="63437-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="63437-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63437-113">Requirements</span></span>



| <span data-ttu-id="63437-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="63437-114">Requirement</span></span> | <span data-ttu-id="63437-115">Value</span><span class="sxs-lookup"><span data-stu-id="63437-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63437-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63437-116">Minimum supported client</span></span><br/> | <span data-ttu-id="63437-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="63437-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63437-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63437-118">Minimum supported server</span></span><br/> | <span data-ttu-id="63437-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="63437-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63437-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63437-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="63437-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="63437-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





