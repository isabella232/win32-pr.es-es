---
title: Código de notificación de LVN_LINKCLICK (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista en el que se ha realizado un vínculo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- LVN_LINKCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd69fb463e71523fcbd4eeb65a6a718d27847c09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493324"
---
# <a name="lvn_linkclick-notification-code"></a><span data-ttu-id="37c87-105">Código de notificación de LINKCLICK de LVN \_</span><span class="sxs-lookup"><span data-stu-id="37c87-105">LVN\_LINKCLICK notification code</span></span>

<span data-ttu-id="37c87-106">Notifica a la ventana primaria de un control de vista de lista en el que se ha realizado un vínculo.</span><span class="sxs-lookup"><span data-stu-id="37c87-106">Notifies a list-view control's parent window that a link has been clicked on.</span></span> <span data-ttu-id="37c87-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="37c87-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a><span data-ttu-id="37c87-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37c87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37c87-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37c87-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37c87-110">Puntero a una estructura [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) .</span><span class="sxs-lookup"><span data-stu-id="37c87-110">Pointer to an [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) structure.</span></span> <span data-ttu-id="37c87-111">El identificador del grupo que contiene el vínculo está en el miembro **iSubItem** .</span><span class="sxs-lookup"><span data-stu-id="37c87-111">The identifier of the group containing the link is in the **iSubItem** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37c87-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37c87-112">Return value</span></span>

<span data-ttu-id="37c87-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="37c87-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37c87-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37c87-114">Remarks</span></span>

<span data-ttu-id="37c87-115">En el ejemplo siguiente se muestra cómo una aplicación puede responder a este código de notificación en su controlador de mensajes de notificación de [**WM \_**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="37c87-115">The following example shows how an application might respond to this notification code in its [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="37c87-116">En el ejemplo se alterna el estado contraído del grupo y se establece el texto del vínculo adecuado.</span><span class="sxs-lookup"><span data-stu-id="37c87-116">The example toggles the collapsed state of the group and sets the appropriate link text.</span></span>

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a><span data-ttu-id="37c87-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37c87-117">Requirements</span></span>



| <span data-ttu-id="37c87-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="37c87-118">Requirement</span></span> | <span data-ttu-id="37c87-119">Value</span><span class="sxs-lookup"><span data-stu-id="37c87-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37c87-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37c87-120">Minimum supported client</span></span><br/> | <span data-ttu-id="37c87-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="37c87-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37c87-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37c87-122">Minimum supported server</span></span><br/> | <span data-ttu-id="37c87-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="37c87-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37c87-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37c87-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="37c87-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="37c87-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





