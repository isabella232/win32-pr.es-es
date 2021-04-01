---
title: Código de notificación de TBN_QUERYINSERT (commctrl. h)
description: Notifica a la ventana primaria de la barra de herramientas si se puede insertar un botón a la izquierda del botón especificado mientras el usuario está personalizando una barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997025"
---
# <a name="tbn_queryinsert-notification-code"></a><span data-ttu-id="fc4f0-105">Código de notificación de QUERYINSERT de TBN \_</span><span class="sxs-lookup"><span data-stu-id="fc4f0-105">TBN\_QUERYINSERT notification code</span></span>

<span data-ttu-id="fc4f0-106">Notifica a la ventana primaria de la barra de herramientas si se puede insertar un botón a la izquierda del botón especificado mientras el usuario está personalizando una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="fc4f0-106">Notifies the toolbar's parent window whether a button may be inserted to the left of the specified button while the user is customizing a toolbar.</span></span> <span data-ttu-id="fc4f0-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4f0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fc4f0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc4f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc4f0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc4f0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc4f0-110">Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="fc4f0-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="fc4f0-111">El miembro **iItem** contiene el índice basado en cero del botón que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="fc4f0-111">The **iItem** member contains the zero-based index of the button to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc4f0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc4f0-112">Return value</span></span>

<span data-ttu-id="fc4f0-113">Devuelva **true** para permitir que un botón se inserte delante del botón especificado o **false** para impedir que se inserte el botón.</span><span class="sxs-lookup"><span data-stu-id="fc4f0-113">Return **TRUE** to allow a button to be inserted in front of the given button, or **FALSE** to prevent the button from being inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc4f0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc4f0-114">Requirements</span></span>



| <span data-ttu-id="fc4f0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc4f0-115">Requirement</span></span> | <span data-ttu-id="fc4f0-116">Value</span><span class="sxs-lookup"><span data-stu-id="fc4f0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc4f0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc4f0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fc4f0-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fc4f0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc4f0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc4f0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fc4f0-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc4f0-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc4f0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc4f0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc4f0-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc4f0-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





