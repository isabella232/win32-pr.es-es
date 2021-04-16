---
title: Código de notificación de LVN_BEGINSCROLL (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista cuando se inicia una operación de desplazamiento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- LVN_BEGINSCROLL controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_BEGINSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae09a05525ac6e9f08d8cc7a0b7de6ef51329baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489256"
---
# <a name="lvn_beginscroll-notification-code"></a><span data-ttu-id="941ca-105">Código de notificación de BEGINSCROLL de LVN \_</span><span class="sxs-lookup"><span data-stu-id="941ca-105">LVN\_BEGINSCROLL notification code</span></span>

<span data-ttu-id="941ca-106">Notifica a la ventana primaria de un control de vista de lista cuando se inicia una operación de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="941ca-106">Notifies a list-view control's parent window when a scrolling operation starts.</span></span> <span data-ttu-id="941ca-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="941ca-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="941ca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="941ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="941ca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="941ca-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="941ca-110">Puntero a una estructura [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) que contiene la posición horizontal o vertical de donde se inicia la operación de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="941ca-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation starts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="941ca-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="941ca-111">Return value</span></span>

<span data-ttu-id="941ca-112">No se usa el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="941ca-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="941ca-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="941ca-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="941ca-114">Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="941ca-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="941ca-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="941ca-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="941ca-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="941ca-116">Requirements</span></span>



| <span data-ttu-id="941ca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="941ca-117">Requirement</span></span> | <span data-ttu-id="941ca-118">Value</span><span class="sxs-lookup"><span data-stu-id="941ca-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="941ca-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="941ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="941ca-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="941ca-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="941ca-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="941ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="941ca-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="941ca-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="941ca-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="941ca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="941ca-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="941ca-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





