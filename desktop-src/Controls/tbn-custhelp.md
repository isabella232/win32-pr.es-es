---
title: Código de notificación de TBN_CUSTHELP (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que el usuario ha elegido el botón ayuda en el cuadro de diálogo Personalizar barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e889764b-abbd-42a6-8c13-ace6ee052039
keywords:
- TBN_CUSTHELP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_CUSTHELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89754deaef2ec4ceb020bd1572c5a419315299e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905104"
---
# <a name="tbn_custhelp-notification-code"></a><span data-ttu-id="9be87-105">Código de notificación de CUSTHELP de TBN \_</span><span class="sxs-lookup"><span data-stu-id="9be87-105">TBN\_CUSTHELP notification code</span></span>

<span data-ttu-id="9be87-106">Notifica a la ventana primaria de una barra de herramientas que el usuario ha elegido el botón ayuda en el cuadro de diálogo Personalizar barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="9be87-106">Notifies a toolbar's parent window that the user has chosen the Help button in the Customize Toolbar dialog box.</span></span> <span data-ttu-id="9be87-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9be87-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_CUSTHELP 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9be87-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9be87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9be87-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9be87-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9be87-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="9be87-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9be87-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9be87-111">Return value</span></span>

<span data-ttu-id="9be87-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9be87-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9be87-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9be87-113">Requirements</span></span>



| <span data-ttu-id="9be87-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9be87-114">Requirement</span></span> | <span data-ttu-id="9be87-115">Value</span><span class="sxs-lookup"><span data-stu-id="9be87-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9be87-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9be87-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9be87-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9be87-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9be87-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9be87-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9be87-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9be87-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9be87-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9be87-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9be87-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9be87-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





