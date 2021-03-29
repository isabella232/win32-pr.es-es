---
title: Código de notificación de NM_RDBLCLK (barra de estado) (commctrl. h)
description: Notifica a las ventanas principales de un control de barra de estado que el usuario hizo doble clic con el botón secundario del mouse en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 57d8c5a7-e179-4b65-a3aa-5566d5780c18
keywords:
- Código de notificación de NM_RDBLCLK (barra de estado) controles de Windows
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18092b03a599c75a88deb56bb256d96728b96328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493312"
---
# <a name="nm_rdblclk-status-bar-notification-code"></a><span data-ttu-id="48b58-105">Código de notificación de NM \_ RDBLCLK (barra de estado)</span><span class="sxs-lookup"><span data-stu-id="48b58-105">NM\_RDBLCLK (status bar) notification code</span></span>

<span data-ttu-id="48b58-106">Notifica a las ventanas principales de un control de barra de estado que el usuario hizo doble clic con el botón secundario del mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="48b58-106">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="48b58-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="48b58-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="48b58-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48b58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b58-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48b58-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48b58-110">Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="48b58-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="48b58-111">El miembro **dwItemSpec** contiene el índice de la sección en la que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="48b58-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b58-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48b58-112">Return value</span></span>

<span data-ttu-id="48b58-113">Devuelve **true** para indicar que se controló el clic del mouse y suprime el procesamiento predeterminado por parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="48b58-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="48b58-114">Devuelve **false** para permitir el procesamiento predeterminado del clic.</span><span class="sxs-lookup"><span data-stu-id="48b58-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="48b58-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48b58-115">Requirements</span></span>



| <span data-ttu-id="48b58-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="48b58-116">Requirement</span></span> | <span data-ttu-id="48b58-117">Value</span><span class="sxs-lookup"><span data-stu-id="48b58-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48b58-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48b58-118">Minimum supported client</span></span><br/> | <span data-ttu-id="48b58-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="48b58-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48b58-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48b58-120">Minimum supported server</span></span><br/> | <span data-ttu-id="48b58-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="48b58-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48b58-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48b58-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="48b58-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="48b58-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





