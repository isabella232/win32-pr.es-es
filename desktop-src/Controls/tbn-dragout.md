---
title: Código de notificación de TBN_DRAGOUT (commctrl. h)
description: Se envía por un control de barra de herramientas cuando el usuario hace clic en un botón y, a continuación, mueve el cursor fuera del botón. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- TBN_DRAGOUT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079119"
---
# <a name="tbn_dragout-notification-code"></a><span data-ttu-id="f91d1-105">Código de notificación de DRAGOUT de TBN \_</span><span class="sxs-lookup"><span data-stu-id="f91d1-105">TBN\_DRAGOUT notification code</span></span>

<span data-ttu-id="f91d1-106">Se envía por un control de barra de herramientas cuando el usuario hace clic en un botón y, a continuación, mueve el cursor fuera del botón.</span><span class="sxs-lookup"><span data-stu-id="f91d1-106">Sent by a toolbar control when the user clicks a button and then moves the cursor off the button.</span></span> <span data-ttu-id="f91d1-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f91d1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f91d1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f91d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f91d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f91d1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f91d1-110">Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="f91d1-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="f91d1-111">En este código de notificación, solo son válidos los miembros **HDR** y **iItem** de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="f91d1-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="f91d1-112">El miembro **iItem** de esta estructura contiene el identificador de comando del botón que se está arrastrando.</span><span class="sxs-lookup"><span data-stu-id="f91d1-112">The **iItem** member of this structure contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f91d1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f91d1-113">Return value</span></span>

<span data-ttu-id="f91d1-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f91d1-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f91d1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f91d1-115">Remarks</span></span>

<span data-ttu-id="f91d1-116">Este código de notificación permite a una aplicación implementar la funcionalidad de arrastrar y colocar para los botones de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f91d1-116">This notification code allows an application to implement drag-and-drop functionality for toolbar buttons.</span></span> <span data-ttu-id="f91d1-117">Al procesar este código de notificación, la aplicación iniciará la operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="f91d1-117">When processing this notification code, the application will begin the drag-and-drop operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f91d1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f91d1-118">Requirements</span></span>



| <span data-ttu-id="f91d1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f91d1-119">Requirement</span></span> | <span data-ttu-id="f91d1-120">Value</span><span class="sxs-lookup"><span data-stu-id="f91d1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f91d1-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f91d1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f91d1-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f91d1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f91d1-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f91d1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f91d1-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f91d1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f91d1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f91d1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f91d1-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f91d1-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





