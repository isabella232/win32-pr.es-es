---
title: Código de notificación de TBN_RESTORE (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de restauración. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- TBN_RESTORE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491975"
---
# <a name="tbn_restore-notification-code"></a><span data-ttu-id="40d2e-105">TBN \_ código de notificación de restauración</span><span class="sxs-lookup"><span data-stu-id="40d2e-105">TBN\_RESTORE notification code</span></span>

<span data-ttu-id="40d2e-106">Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="40d2e-106">Notifies a toolbar's parent window that a toolbar is in the process of being restored.</span></span> <span data-ttu-id="40d2e-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="40d2e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="40d2e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40d2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40d2e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40d2e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40d2e-110">Puntero a una estructura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) .</span><span class="sxs-lookup"><span data-stu-id="40d2e-110">Pointer to an [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40d2e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40d2e-111">Return value</span></span>

<span data-ttu-id="40d2e-112">La aplicación debe devolver cero en respuesta al primer código de notificación de **\_ restauración de TBN** recibido al inicio del proceso de restauración para seguir restaurando la información del botón.</span><span class="sxs-lookup"><span data-stu-id="40d2e-112">The application should return zero in response to the first **TBN\_RESTORE** notification code received at the start of the restore process to continue restoring the button information.</span></span> <span data-ttu-id="40d2e-113">Si la aplicación devuelve un valor distinto de cero, se cancela el proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="40d2e-113">If the application returns a nonzero value, the restore process is canceled.</span></span>

## <a name="remarks"></a><span data-ttu-id="40d2e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40d2e-114">Remarks</span></span>

<span data-ttu-id="40d2e-115">La aplicación recibirá este código de notificación una vez al inicio del proceso de restauración y otra para cada botón.</span><span class="sxs-lookup"><span data-stu-id="40d2e-115">The application will receive this notification code once at the start of the restore process and once for each button.</span></span> <span data-ttu-id="40d2e-116">Este código de notificación ofrece la oportunidad de extraer la información del flujo de datos que guardó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="40d2e-116">This notification code gives you an opportunity to extract the information from the data stream that you saved previously.</span></span> <span data-ttu-id="40d2e-117">Si no ha guardado ninguna información, omita el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="40d2e-117">If you haven't saved any information, ignore the notification code.</span></span> <span data-ttu-id="40d2e-118">Consulte [Personalización](toolbar-controls-overview.md) de la barra de herramientas para obtener una explicación más detallada de cómo controlar la **\_ restauración de TBN**.</span><span class="sxs-lookup"><span data-stu-id="40d2e-118">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle **TBN\_RESTORE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="40d2e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40d2e-119">Requirements</span></span>



| <span data-ttu-id="40d2e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="40d2e-120">Requirement</span></span> | <span data-ttu-id="40d2e-121">Value</span><span class="sxs-lookup"><span data-stu-id="40d2e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40d2e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40d2e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="40d2e-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="40d2e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40d2e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40d2e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="40d2e-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="40d2e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40d2e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40d2e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="40d2e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="40d2e-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





