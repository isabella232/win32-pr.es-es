---
title: Código de notificación de TBN_QUERYDELETE (commctrl. h)
description: Notifica a la ventana primaria de la barra de herramientas si se puede eliminar un botón de una barra de herramientas mientras el usuario está personalizando la barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533747"
---
# <a name="tbn_querydelete-notification-code"></a><span data-ttu-id="a9cb5-105">Código de notificación de QUERYDELETE de TBN \_</span><span class="sxs-lookup"><span data-stu-id="a9cb5-105">TBN\_QUERYDELETE notification code</span></span>

<span data-ttu-id="a9cb5-106">Notifica a la ventana primaria de la barra de herramientas si se puede eliminar un botón de una barra de herramientas mientras el usuario está personalizando la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="a9cb5-106">Notifies the toolbar's parent window whether a button may be deleted from a toolbar while the user is customizing the toolbar.</span></span> <span data-ttu-id="a9cb5-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a9cb5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a9cb5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9cb5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9cb5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9cb5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9cb5-110">Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="a9cb5-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="a9cb5-111">El miembro **iItem** contiene el índice basado en cero del botón que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="a9cb5-111">The **iItem** member contains the zero-based index of the button to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9cb5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9cb5-112">Return value</span></span>

<span data-ttu-id="a9cb5-113">Devuelve **true** para permitir que el botón se elimine o **false** para impedir que se elimine el botón.</span><span class="sxs-lookup"><span data-stu-id="a9cb5-113">Returns **TRUE** to allow the button to be deleted, or **FALSE** to prevent the button from being deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9cb5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9cb5-114">Requirements</span></span>



| <span data-ttu-id="a9cb5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9cb5-115">Requirement</span></span> | <span data-ttu-id="a9cb5-116">Value</span><span class="sxs-lookup"><span data-stu-id="a9cb5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9cb5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9cb5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a9cb5-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a9cb5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9cb5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9cb5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a9cb5-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9cb5-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9cb5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9cb5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9cb5-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9cb5-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





