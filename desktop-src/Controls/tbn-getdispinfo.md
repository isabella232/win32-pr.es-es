---
title: Código de notificación de TBN_GETDISPINFO (commctrl. h)
description: Recupera información de presentación de un elemento de la barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- TBN_GETDISPINFO controles de código de notificación de Windows
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150735"
---
# <a name="tbn_getdispinfo-notification-code"></a><span data-ttu-id="3d6e7-105">Código de notificación de GETDISPINFO de TBN \_</span><span class="sxs-lookup"><span data-stu-id="3d6e7-105">TBN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="3d6e7-106">Recupera información de presentación de un elemento de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-106">Retrieves display information for a toolbar item.</span></span> <span data-ttu-id="3d6e7-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3d6e7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3d6e7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d6e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d6e7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d6e7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d6e7-110">Puntero a una estructura [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="3d6e7-110">Pointer to an [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) structure.</span></span> <span data-ttu-id="3d6e7-111">El miembro **idCommand** especifica el identificador de comando del elemento, el miembro **lParam** contiene los datos definidos por la aplicación del elemento y el miembro **dwMask** especifica qué información se solicita.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-111">The **idCommand** member specifies the item's command identifier, the **lParam** member contains the item's application-defined data, and the **dwMask** member specifies what information is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d6e7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d6e7-112">Return value</span></span>

<span data-ttu-id="3d6e7-113">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-113">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d6e7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d6e7-114">Requirements</span></span>



| <span data-ttu-id="3d6e7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d6e7-115">Requirement</span></span> | <span data-ttu-id="3d6e7-116">Value</span><span class="sxs-lookup"><span data-stu-id="3d6e7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6e7-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d6e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3d6e7-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3d6e7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d6e7-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d6e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3d6e7-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d6e7-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d6e7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d6e7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d6e7-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d6e7-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3d6e7-123">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="3d6e7-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3d6e7-124">**TBN \_ GETDISPINFOW** (Unicode) y **TBN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3d6e7-124">**TBN\_GETDISPINFOW** (Unicode) and **TBN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





