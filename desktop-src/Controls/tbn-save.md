---
title: Código de notificación de TBN_SAVE (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de guardarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804003"
---
# <a name="tbn_save-notification-code"></a><span data-ttu-id="1a64e-105">TBN \_ Guardar código de notificación</span><span class="sxs-lookup"><span data-stu-id="1a64e-105">TBN\_SAVE notification code</span></span>

<span data-ttu-id="1a64e-106">Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de guardarse.</span><span class="sxs-lookup"><span data-stu-id="1a64e-106">Notifies a toolbar's parent window that a toolbar is in the process of being saved.</span></span> <span data-ttu-id="1a64e-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1a64e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1a64e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a64e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a64e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a64e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a64e-110">Puntero a una estructura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) .</span><span class="sxs-lookup"><span data-stu-id="1a64e-110">Pointer to an [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a64e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a64e-111">Return value</span></span>

<span data-ttu-id="1a64e-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1a64e-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a64e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a64e-113">Remarks</span></span>

<span data-ttu-id="1a64e-114">La aplicación recibirá este código de notificación una vez al inicio del proceso de guardado y una vez para cada botón.</span><span class="sxs-lookup"><span data-stu-id="1a64e-114">The application will receive this notification code once at the start of the save process and once for each button.</span></span> <span data-ttu-id="1a64e-115">Este código de notificación le ofrece la oportunidad de agregar su propia información a que haya guardado el shell.</span><span class="sxs-lookup"><span data-stu-id="1a64e-115">This notification code gives you an opportunity to add your own information to that saved by the Shell.</span></span> <span data-ttu-id="1a64e-116">Si no desea agregar información, omita el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="1a64e-116">If you do not wish to add information, ignore the notification code.</span></span> <span data-ttu-id="1a64e-117">Consulte [Personalización](toolbar-controls-overview.md) de la barra de herramientas para obtener una explicación más detallada de cómo controlar el almacenamiento de TBN \_ .</span><span class="sxs-lookup"><span data-stu-id="1a64e-117">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle TBN\_SAVE.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a64e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a64e-118">Requirements</span></span>



| <span data-ttu-id="1a64e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a64e-119">Requirement</span></span> | <span data-ttu-id="1a64e-120">Value</span><span class="sxs-lookup"><span data-stu-id="1a64e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a64e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a64e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1a64e-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1a64e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a64e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a64e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1a64e-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1a64e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a64e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a64e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a64e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a64e-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a64e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a64e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a64e-128">restauración de TBN \_</span><span class="sxs-lookup"><span data-stu-id="1a64e-128">TBN\_RESTORE</span></span>](tbn-restore.md)
</dt> </dl>

 

 





