---
title: Código de notificación de TBN_INITCUSTOMIZE (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que se ha iniciado la personalización. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- TBN_INITCUSTOMIZE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656463"
---
# <a name="tbn_initcustomize-notification-code"></a><span data-ttu-id="fea7f-105">Código de notificación de INITCUSTOMIZE de TBN \_</span><span class="sxs-lookup"><span data-stu-id="fea7f-105">TBN\_INITCUSTOMIZE notification code</span></span>

<span data-ttu-id="fea7f-106">Notifica a la ventana primaria de una barra de herramientas que se ha iniciado la personalización.</span><span class="sxs-lookup"><span data-stu-id="fea7f-106">Notifies a toolbar's parent window that customizing has started.</span></span> <span data-ttu-id="fea7f-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fea7f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fea7f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fea7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fea7f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fea7f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fea7f-110">Puntero a la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="fea7f-110">Pointer to the toolbar's [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fea7f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fea7f-111">Return value</span></span>

<span data-ttu-id="fea7f-112">Devuelve TBNRF \_ HIDEHELP para suprimir el botón ayuda.</span><span class="sxs-lookup"><span data-stu-id="fea7f-112">Returns TBNRF\_HIDEHELP to suppress the Help button.</span></span>

## <a name="requirements"></a><span data-ttu-id="fea7f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fea7f-113">Requirements</span></span>



| <span data-ttu-id="fea7f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fea7f-114">Requirement</span></span> | <span data-ttu-id="fea7f-115">Value</span><span class="sxs-lookup"><span data-stu-id="fea7f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fea7f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fea7f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fea7f-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fea7f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fea7f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fea7f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fea7f-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fea7f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fea7f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fea7f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fea7f-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fea7f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





