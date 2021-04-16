---
title: Mensaje de TTM_GETTEXT (commctrl. h)
description: Recupera la información que un control ToolTip mantiene sobre una herramienta.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- TTM_GETTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658188"
---
# <a name="ttm_gettext-message"></a><span data-ttu-id="24343-104">Mensaje de TTM \_ GETTEXT</span><span class="sxs-lookup"><span data-stu-id="24343-104">TTM\_GETTEXT message</span></span>

<span data-ttu-id="24343-105">Recupera la información que un control ToolTip mantiene sobre una herramienta.</span><span class="sxs-lookup"><span data-stu-id="24343-105">Retrieves the information a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="24343-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24343-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24343-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24343-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="24343-108">Número de **TCHARs**, incluido el **valor null** final, que se va a copiar en el búfer al que apunta **lpszText**.</span><span class="sxs-lookup"><span data-stu-id="24343-108">The number of **TCHARs**, including the terminating **NULL**, to copy to the buffer pointed to by **lpszText**.</span></span> </dd> <dt>

<span data-ttu-id="24343-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24343-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24343-110">Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="24343-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="24343-111">Establezca el miembro **cbSize** de esta estructura en `sizeof(TOOLINFO)` antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="24343-111">Set the **cbSize** member of this structure to `sizeof(TOOLINFO)` before sending this message.</span></span> <span data-ttu-id="24343-112">Establezca los miembros **hWnd** y **uId** para identificar la herramienta para la que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="24343-112">Set the **hwnd** and **uId** members to identify the tool for which to retrieve information.</span></span> <span data-ttu-id="24343-113">Asigna un búfer de tamaño especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="24343-113">Allocate a buffer of size specified by *wParam*.</span></span> <span data-ttu-id="24343-114">Establezca el miembro **lpszText** para que apunte al búfer para recibir el texto de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="24343-114">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24343-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24343-115">Return value</span></span>

<span data-ttu-id="24343-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="24343-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24343-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24343-117">Requirements</span></span>



| <span data-ttu-id="24343-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24343-118">Requirement</span></span> | <span data-ttu-id="24343-119">Value</span><span class="sxs-lookup"><span data-stu-id="24343-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24343-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24343-120">Minimum supported client</span></span><br/> | <span data-ttu-id="24343-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="24343-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24343-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24343-122">Minimum supported server</span></span><br/> | <span data-ttu-id="24343-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="24343-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24343-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24343-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="24343-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="24343-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="24343-126">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="24343-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="24343-127">**TTM \_ GETTEXTW** (Unicode) y **TTM \_ gettexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="24343-127">**TTM\_GETTEXTW** (Unicode) and **TTM\_GETTEXTA** (ANSI)</span></span><br/>                   |



 

 





