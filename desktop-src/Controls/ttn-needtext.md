---
title: Código de notificación de TTN_NEEDTEXT (commctrl. h)
description: Lo envía un control ToolTip para recuperar la información necesaria para mostrar una ventana de información sobre herramientas. Este código de notificación es idéntico a TTN \_ GETDISPINFO. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150534"
---
# <a name="ttn_needtext-notification-code"></a><span data-ttu-id="b14de-106">Código de notificación de NEEDTEXT de TTN \_</span><span class="sxs-lookup"><span data-stu-id="b14de-106">TTN\_NEEDTEXT notification code</span></span>

<span data-ttu-id="b14de-107">Lo envía un control ToolTip para recuperar la información necesaria para mostrar una ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="b14de-107">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="b14de-108">Este código de notificación es idéntico a [TTN \_ GETDISPINFO](ttn-getdispinfo.md).</span><span class="sxs-lookup"><span data-stu-id="b14de-108">This notification code is identical to [TTN\_GETDISPINFO](ttn-getdispinfo.md).</span></span> <span data-ttu-id="b14de-109">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b14de-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b14de-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b14de-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b14de-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b14de-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b14de-112">Puntero a una estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) que identifica la herramienta que necesita texto y recibe la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="b14de-112">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b14de-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b14de-113">Return value</span></span>

<span data-ttu-id="b14de-114">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="b14de-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b14de-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b14de-115">Remarks</span></span>

<span data-ttu-id="b14de-116">Rellene los miembros adecuados de la estructura para devolver la información solicitada al control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="b14de-116">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="b14de-117">Si el controlador de mensajes establece el miembro **uFlags** de la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) en ttf \_ di \_ SETITEM, el control ToolTip almacena la información y no la volverá a solicitar.</span><span class="sxs-lookup"><span data-stu-id="b14de-117">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="b14de-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b14de-118">Requirements</span></span>



| <span data-ttu-id="b14de-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b14de-119">Requirement</span></span> | <span data-ttu-id="b14de-120">Value</span><span class="sxs-lookup"><span data-stu-id="b14de-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b14de-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b14de-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b14de-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b14de-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b14de-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b14de-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b14de-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b14de-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b14de-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b14de-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b14de-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b14de-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b14de-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="b14de-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b14de-128">**TTN \_ NEEDTEXTW** (Unicode) y **TTN \_ NEEDTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b14de-128">**TTN\_NEEDTEXTW** (Unicode) and **TTN\_NEEDTEXTA** (ANSI)</span></span><br/>                 |



 

 





