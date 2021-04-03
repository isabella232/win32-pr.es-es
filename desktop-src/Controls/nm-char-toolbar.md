---
title: Código de notificación de NM_CHAR (barra de herramientas) (commctrl. h)
description: Se envía mediante una barra de herramientas cuando recibe un mensaje de tipo WM \_ Char. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- Código de notificación de NM_CHAR (barra de herramientas) controles de Windows
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
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905692"
---
# <a name="nm_char-toolbar-notification-code"></a><span data-ttu-id="c66ae-105">NM \_ Char (barra de herramientas) código de notificación</span><span class="sxs-lookup"><span data-stu-id="c66ae-105">NM\_CHAR (toolbar) notification code</span></span>

<span data-ttu-id="c66ae-106">Se envía mediante una barra de herramientas cuando recibe un mensaje de tipo [**WM \_ Char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="c66ae-106">Sent by a toolbar when it receives a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span> <span data-ttu-id="c66ae-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c66ae-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c66ae-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c66ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c66ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c66ae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c66ae-110">Puntero a una estructura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contiene información adicional sobre el carácter que causó el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="c66ae-110">Pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span> <span data-ttu-id="c66ae-111">El miembro **dwItemPrev** de esta estructura contiene el identificador de comando del elemento activo actualmente o-1 si no hay ningún elemento activo actualmente.</span><span class="sxs-lookup"><span data-stu-id="c66ae-111">The **dwItemPrev** member of this structure contains the command identifier of the item that is currently hot or -1 if no item is currently hot.</span></span> <span data-ttu-id="c66ae-112">El miembro **dwItemNext** de esta estructura contiene el identificador de comando del elemento que volverá a estar activo o-1 si la clave no coincide con el acelerador de cualquier elemento.</span><span class="sxs-lookup"><span data-stu-id="c66ae-112">The **dwItemNext** member of this structure contains the command identifier of the item that will become hot or -1 if the key does not match any item's accelerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c66ae-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c66ae-113">Return value</span></span>

<span data-ttu-id="c66ae-114">Devuelve **true** para indicar que la barra de herramientas no debe procesar el carácter y **false** para que la barra de herramientas procese el carácter.</span><span class="sxs-lookup"><span data-stu-id="c66ae-114">Returns **TRUE** to indicate that the toolbar should not process the character and **FALSE** to have the toolbar process the character.</span></span>

## <a name="requirements"></a><span data-ttu-id="c66ae-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c66ae-115">Requirements</span></span>



| <span data-ttu-id="c66ae-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c66ae-116">Requirement</span></span> | <span data-ttu-id="c66ae-117">Value</span><span class="sxs-lookup"><span data-stu-id="c66ae-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c66ae-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c66ae-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c66ae-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c66ae-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c66ae-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c66ae-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c66ae-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c66ae-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c66ae-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c66ae-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c66ae-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c66ae-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

