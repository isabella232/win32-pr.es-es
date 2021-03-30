---
title: Mensaje de PGN_HOTITEMCHANGE (commctrl. h)
description: Notifica a la ventana primaria de un control de paginación que el elemento activo (resaltado) ha cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- PGN_HOTITEMCHANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 573f3dd93a6e4b0b3db6682d36804416d6f6f1e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079265"
---
# <a name="pgn_hotitemchange-message"></a><span data-ttu-id="65e85-105">PGN \_ HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="65e85-105">PGN\_HOTITEMCHANGE message</span></span>

<span data-ttu-id="65e85-106">Notifica a la ventana primaria de un control de paginación que el elemento activo (resaltado) ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="65e85-106">Notifies a pager control's parent window that the hot (highlighted) item has change.</span></span> <span data-ttu-id="65e85-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="65e85-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="65e85-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65e85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65e85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65e85-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65e85-110">Puntero a una estructura [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="65e85-110">Pointer to a [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65e85-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65e85-111">Return value</span></span>

<span data-ttu-id="65e85-112">Devuelve cero para resaltar el elemento o un valor distinto de cero para evitar el resaltado.</span><span class="sxs-lookup"><span data-stu-id="65e85-112">Return zero to highlight the item or nonzero to prevent highlighting.</span></span>

## <a name="remarks"></a><span data-ttu-id="65e85-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65e85-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="65e85-114">Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="65e85-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="65e85-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="65e85-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65e85-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65e85-116">Requirements</span></span>



| <span data-ttu-id="65e85-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="65e85-117">Requirement</span></span> | <span data-ttu-id="65e85-118">Value</span><span class="sxs-lookup"><span data-stu-id="65e85-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65e85-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65e85-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65e85-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="65e85-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65e85-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65e85-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65e85-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="65e85-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65e85-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65e85-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="65e85-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="65e85-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





