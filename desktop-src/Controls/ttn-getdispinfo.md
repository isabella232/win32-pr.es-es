---
title: Código de notificación de TTN_GETDISPINFO (commctrl. h)
description: Lo envía un control ToolTip para recuperar la información necesaria para mostrar una ventana de información sobre herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6
keywords:
- TTN_GETDISPINFO controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TTN_GETDISPINFO
- TTN_GETDISPINFOA
- TTN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc1fe07d12331e523fed9e1ff46b9e265487bc31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905398"
---
# <a name="ttn_getdispinfo-notification-code"></a><span data-ttu-id="fe50a-105">Código de notificación de GETDISPINFO de TTN \_</span><span class="sxs-lookup"><span data-stu-id="fe50a-105">TTN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="fe50a-106">Lo envía un control ToolTip para recuperar la información necesaria para mostrar una ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="fe50a-106">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="fe50a-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fe50a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_GETDISPINFO

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fe50a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe50a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe50a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe50a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe50a-110">Puntero a una estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) que identifica la herramienta que necesita texto y recibe la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="fe50a-110">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe50a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe50a-111">Return value</span></span>

<span data-ttu-id="fe50a-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="fe50a-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe50a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe50a-113">Remarks</span></span>

<span data-ttu-id="fe50a-114">Rellene los miembros adecuados de la estructura para devolver la información solicitada al control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="fe50a-114">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="fe50a-115">Si el controlador de mensajes establece el miembro **uFlags** de la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) en ttf \_ di \_ SETITEM, el control ToolTip almacena la información y no la volverá a solicitar.</span><span class="sxs-lookup"><span data-stu-id="fe50a-115">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe50a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe50a-116">Requirements</span></span>



| <span data-ttu-id="fe50a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe50a-117">Requirement</span></span> | <span data-ttu-id="fe50a-118">Value</span><span class="sxs-lookup"><span data-stu-id="fe50a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe50a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe50a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fe50a-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fe50a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe50a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe50a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fe50a-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe50a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe50a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe50a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe50a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe50a-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fe50a-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="fe50a-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fe50a-126">**TTN \_ GETDISPINFOW** (Unicode) y **TTN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fe50a-126">**TTN\_GETDISPINFOW** (Unicode) and **TTN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





