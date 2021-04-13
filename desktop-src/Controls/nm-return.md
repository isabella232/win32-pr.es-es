---
title: Código de notificación de NM_RETURN (commctrl. h)
description: Notifica a la ventana primaria de un control que el control tiene el foco de entrada y que el usuario ha presionado la tecla entrar. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 2c4839bc-6b23-469b-978f-cdf5f7bc0549
keywords:
- NM_RETURN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c6cebd089873df5471c9b25710efafaab4d246f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534840"
---
# <a name="nm_return-notification-code"></a><span data-ttu-id="dbbfd-105">NM \_ devuelve código de notificación</span><span class="sxs-lookup"><span data-stu-id="dbbfd-105">NM\_RETURN notification code</span></span>

<span data-ttu-id="dbbfd-106">Notifica a la ventana primaria de un control que el control tiene el foco de entrada y que el usuario ha presionado la tecla entrar.</span><span class="sxs-lookup"><span data-stu-id="dbbfd-106">Notifies a control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="dbbfd-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="dbbfd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="dbbfd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dbbfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbbfd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbbfd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbbfd-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="dbbfd-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbbfd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbbfd-111">Return value</span></span>

<span data-ttu-id="dbbfd-112">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="dbbfd-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbbfd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbbfd-113">Requirements</span></span>



| <span data-ttu-id="dbbfd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbbfd-114">Requirement</span></span> | <span data-ttu-id="dbbfd-115">Value</span><span class="sxs-lookup"><span data-stu-id="dbbfd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbbfd-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbbfd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dbbfd-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dbbfd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dbbfd-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbbfd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dbbfd-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dbbfd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dbbfd-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbbfd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbbfd-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbbfd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





