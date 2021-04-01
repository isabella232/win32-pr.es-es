---
title: Mensaje de LVN_ENDSCROLL (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista cuando finaliza una operación de desplazamiento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- LVN_ENDSCROLL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9dcdcff2d0bcfc28e1818d5add6d37838e5f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905697"
---
# <a name="lvn_endscroll-message"></a><span data-ttu-id="8d9c2-105">LVN \_ ENDSCROLL</span><span class="sxs-lookup"><span data-stu-id="8d9c2-105">LVN\_ENDSCROLL message</span></span>

<span data-ttu-id="8d9c2-106">Notifica a la ventana primaria de un control de vista de lista cuando finaliza una operación de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="8d9c2-106">Notifies a list-view control's parent window when a scrolling operation ends.</span></span> <span data-ttu-id="8d9c2-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8d9c2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8d9c2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d9c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d9c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d9c2-110">Puntero a una estructura [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) que contiene la posición horizontal o vertical de donde finaliza la operación de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="8d9c2-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation ends.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d9c2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d9c2-111">Return value</span></span>

<span data-ttu-id="8d9c2-112">No se usa el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="8d9c2-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d9c2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d9c2-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8d9c2-114">Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="8d9c2-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="8d9c2-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8d9c2-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8d9c2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d9c2-116">Requirements</span></span>



| <span data-ttu-id="8d9c2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d9c2-117">Requirement</span></span> | <span data-ttu-id="8d9c2-118">Value</span><span class="sxs-lookup"><span data-stu-id="8d9c2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9c2-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d9c2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d9c2-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8d9c2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d9c2-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d9c2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d9c2-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d9c2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d9c2-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d9c2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d9c2-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d9c2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





