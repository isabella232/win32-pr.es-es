---
title: Código de notificación de EN_PARAGRAPHEXPANDED (RichEdit. h)
description: Notifica a un elemento primario del control Rich Edit que se ha expandido un esquema. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: D33EB118-FC79-4284-820B-3424F13722C4
keywords:
- EN_PARAGRAPHEXPANDED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_PARAGRAPHEXPANDEDC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f862260c0653d23b0b53649a2c05e59820e3808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490871"
---
# <a name="en_paragraphexpanded-notification-code"></a><span data-ttu-id="c2cf7-105">\_Código de notificación en PARAGRAPHEXPANDED</span><span class="sxs-lookup"><span data-stu-id="c2cf7-105">EN\_PARAGRAPHEXPANDED notification code</span></span>

<span data-ttu-id="c2cf7-106">Notifica a un elemento primario del control Rich Edit que se ha expandido un esquema.</span><span class="sxs-lookup"><span data-stu-id="c2cf7-106">Notifies a rich edit control's parent that an outline has been expanded.</span></span> <span data-ttu-id="c2cf7-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c2cf7-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PARAGRAPHEXPANDED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c2cf7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2cf7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2cf7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2cf7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cf7-110">Una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="c2cf7-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2cf7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2cf7-111">Requirements</span></span>



| <span data-ttu-id="c2cf7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2cf7-112">Requirement</span></span> | <span data-ttu-id="c2cf7-113">Value</span><span class="sxs-lookup"><span data-stu-id="c2cf7-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cf7-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2cf7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c2cf7-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c2cf7-115">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2cf7-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2cf7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c2cf7-117">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2cf7-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2cf7-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2cf7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2cf7-119"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2cf7-119"><dt>Richedit.h</dt></span></span> </dl> |



 

 





