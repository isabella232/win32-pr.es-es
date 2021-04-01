---
title: Código de notificación de EN_STARTCOMPOSITION (RichEdit. h)
description: Notifica a una ventana primaria de un control Rich Edit que el usuario ha empezado a escribir con IME o Text Services Framework.
ms.assetid: 755C0C5F-061B-44AF-98A5-776AEE1B7AF8
keywords:
- EN_STARTCOMPOSITION controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_STARTCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a103431427a9325a6b74c27927fb56e65f6fe771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150911"
---
# <a name="en_startcomposition-notification-code"></a><span data-ttu-id="8f36a-104">\_Código de notificación en STARTCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="8f36a-104">EN\_STARTCOMPOSITION notification code</span></span>

<span data-ttu-id="8f36a-105">Notifica a una ventana primaria de un control Rich Edit que el usuario ha empezado a escribir con IME o [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span><span class="sxs-lookup"><span data-stu-id="8f36a-105">Notifies a rich edit control parent window that the user started typing with IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_STARTCOMPOSITION

    pStartComp = (NMDHR *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8f36a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f36a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f36a-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f36a-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f36a-108">Una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="8f36a-108">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f36a-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f36a-109">Requirements</span></span>



| <span data-ttu-id="8f36a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f36a-110">Requirement</span></span> | <span data-ttu-id="8f36a-111">Value</span><span class="sxs-lookup"><span data-stu-id="8f36a-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f36a-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f36a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8f36a-113">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f36a-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8f36a-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f36a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8f36a-115">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f36a-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f36a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f36a-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f36a-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f36a-117"><dt>Richedit.h</dt></span></span> </dl> |



 

