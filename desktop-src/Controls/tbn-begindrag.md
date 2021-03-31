---
title: Código de notificación de TBN_BEGINDRAG (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que el usuario ha empezado a arrastrar un botón en una barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 244406e5-e13d-4c80-81fa-81b018b29ec1
keywords:
- TBN_BEGINDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cfa7325d1a8e1eab27383d7df918c8896933bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150062"
---
# <a name="tbn_begindrag-notification-code"></a><span data-ttu-id="bf628-105">Código de notificación de BEGINDRAG de TBN \_</span><span class="sxs-lookup"><span data-stu-id="bf628-105">TBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="bf628-106">Notifica a la ventana primaria de una barra de herramientas que el usuario ha empezado a arrastrar un botón en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bf628-106">Notifies a toolbar's parent window that the user has begun dragging a button in a toolbar.</span></span> <span data-ttu-id="bf628-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bf628-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_BEGINDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bf628-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf628-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf628-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf628-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf628-110">Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="bf628-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="bf628-111">El miembro **iItem** contiene el identificador de comando del botón que se está arrastrando.</span><span class="sxs-lookup"><span data-stu-id="bf628-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf628-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf628-112">Return value</span></span>

<span data-ttu-id="bf628-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bf628-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf628-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf628-114">Requirements</span></span>



| <span data-ttu-id="bf628-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf628-115">Requirement</span></span> | <span data-ttu-id="bf628-116">Value</span><span class="sxs-lookup"><span data-stu-id="bf628-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf628-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf628-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf628-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bf628-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf628-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf628-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf628-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf628-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf628-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf628-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf628-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf628-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





