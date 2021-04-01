---
title: Código de notificación de NM_SETCURSOR (vista de árbol) (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que el control está estableciendo el cursor en respuesta a un mensaje de SETCURSOR de WM \_ . Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 2b2f2e90-edef-484d-b67a-12983a1cde29
keywords:
- Código de notificación de NM_SETCURSOR (vista de árbol) controles de Windows
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40b733e32c72abc9620e0fd18a6ef554aee9214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996814"
---
# <a name="nm_setcursor-tree-view-notification-code"></a><span data-ttu-id="381eb-105">NM \_ SETCURSOR (vista de árbol) código de notificación</span><span class="sxs-lookup"><span data-stu-id="381eb-105">NM\_SETCURSOR (tree view) notification code</span></span>

<span data-ttu-id="381eb-106">Notifica a la ventana primaria de un control de vista de árbol que el control está estableciendo el cursor en respuesta a un mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) .</span><span class="sxs-lookup"><span data-stu-id="381eb-106">Notifies a tree-view control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="381eb-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="381eb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="381eb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="381eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="381eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="381eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="381eb-110">Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="381eb-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="381eb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="381eb-111">Return value</span></span>

<span data-ttu-id="381eb-112">Devuelve cero para permitir que el control establezca el cursor o un valor distinto de cero para evitar que el control establezca el cursor.</span><span class="sxs-lookup"><span data-stu-id="381eb-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="381eb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="381eb-113">Requirements</span></span>



| <span data-ttu-id="381eb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="381eb-114">Requirement</span></span> | <span data-ttu-id="381eb-115">Value</span><span class="sxs-lookup"><span data-stu-id="381eb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="381eb-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="381eb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="381eb-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="381eb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="381eb-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="381eb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="381eb-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="381eb-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="381eb-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="381eb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="381eb-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="381eb-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

