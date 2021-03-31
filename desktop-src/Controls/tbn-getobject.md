---
title: Código de notificación de TBN_GETOBJECT (commctrl. h)
description: Se envía mediante un control de barra de herramientas que usa el \_ estilo TBSTYLE REGISTERDROP para solicitar un objeto de destino de colocación cuando el puntero pasa sobre uno de sus botones. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- TBN_GETOBJECT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149883"
---
# <a name="tbn_getobject-notification-code"></a><span data-ttu-id="c6e8f-105">TBN \_ código de notificación GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="c6e8f-105">TBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="c6e8f-106">Se envía mediante un control de barra de herramientas que usa el estilo [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) para solicitar un objeto de destino de colocación cuando el puntero pasa sobre uno de sus botones.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-106">Sent by a toolbar control that uses the [**TBSTYLE\_REGISTERDROP**](toolbar-control-and-button-styles.md) style to request a drop target object when the pointer passes over one of its buttons.</span></span> <span data-ttu-id="c6e8f-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c6e8f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c6e8f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6e8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6e8f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6e8f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6e8f-110">Puntero a una estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contiene información sobre el botón que el puntero pasó y recibe los datos que proporciona la aplicación en respuesta a este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the button that the pointer passed over and receives data the application provides in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6e8f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6e8f-111">Return value</span></span>

<span data-ttu-id="c6e8f-112">El procesamiento de la aplicación en este código de notificación debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e8f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6e8f-113">Remarks</span></span>

<span data-ttu-id="c6e8f-114">Para proporcionar un objeto, una aplicación debe establecer valores en algunos miembros de la estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-114">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="c6e8f-115">El miembro **pObject** debe establecerse en un puntero de objeto válido y el miembro **hResult** debe establecerse en una marca Success.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-115">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="c6e8f-116">Para cumplir los estándares del modelo de objetos componentes (COM), aumente siempre el recuento de referencias del objeto al proporcionar un puntero de objeto.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-116">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="c6e8f-117">Si una aplicación no proporciona un objeto, debe establecer **pObject** en **null** y **hResult** en una marca de error.</span><span class="sxs-lookup"><span data-stu-id="c6e8f-117">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e8f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6e8f-118">Requirements</span></span>



| <span data-ttu-id="c6e8f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6e8f-119">Requirement</span></span> | <span data-ttu-id="c6e8f-120">Value</span><span class="sxs-lookup"><span data-stu-id="c6e8f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e8f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6e8f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e8f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c6e8f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6e8f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6e8f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e8f-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6e8f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6e8f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6e8f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6e8f-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6e8f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





