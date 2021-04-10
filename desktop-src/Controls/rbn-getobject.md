---
title: Código de notificación de RBN_GETOBJECT (commctrl. h)
description: Enviado por un control rebar creado con el \_ estilo REGISTERDROP de RBS cuando se arrastra un objeto sobre una banda en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- RBN_GETOBJECT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150651"
---
# <a name="rbn_getobject-notification-code"></a><span data-ttu-id="eb364-105">RBN \_ código de notificación GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="eb364-105">RBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="eb364-106">Enviado por un control rebar creado con el [**estilo \_ REGISTERDROP de RBS**](rebar-control-styles.md) cuando se arrastra un objeto sobre una banda en el control.</span><span class="sxs-lookup"><span data-stu-id="eb364-106">Sent by a rebar control created with the [**RBS\_REGISTERDROP**](rebar-control-styles.md) style when an object is dragged over a band in the control.</span></span> <span data-ttu-id="eb364-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="eb364-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="eb364-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb364-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb364-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb364-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb364-110">Puntero a una estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contiene información sobre la banda sobre la que se arrastra el objeto y también recibe los datos proporcionados por la aplicación receptora en respuesta a este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="eb364-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the band that the object is dragged over and also receives the data provided by the receiving application in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb364-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb364-111">Return value</span></span>

<span data-ttu-id="eb364-112">El valor devuelto para este código de notificación debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="eb364-112">The return value for this notification code must be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb364-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb364-113">Remarks</span></span>

<span data-ttu-id="eb364-114">Para recibir el \_ código de notificación GETOBJECT de RBN, INICIALICE OLE con una llamada a [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) o [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span><span class="sxs-lookup"><span data-stu-id="eb364-114">To receive the RBN\_GETOBJECT notification code, initialize OLE with a call to [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) or [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb364-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb364-115">Requirements</span></span>



| <span data-ttu-id="eb364-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb364-116">Requirement</span></span> | <span data-ttu-id="eb364-117">Value</span><span class="sxs-lookup"><span data-stu-id="eb364-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb364-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb364-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eb364-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eb364-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb364-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb364-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eb364-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb364-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb364-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb364-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb364-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb364-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

