---
title: Código de notificación de EN_ENDCOMPOSITION (RichEdit. h)
description: Notifica a una ventana primaria de un control Rich Edit que el usuario ha escrito nuevos datos o que ha terminado de escribir datos mientras usa el marco de trabajo de servicios de texto o IME.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489281"
---
# <a name="en_endcomposition-notification-code"></a><span data-ttu-id="f3745-104">\_Código de notificación en ENDCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="f3745-104">EN\_ENDCOMPOSITION notification code</span></span>

<span data-ttu-id="f3745-105">Notifica a una ventana primaria de un control Rich Edit que el usuario ha escrito nuevos datos o que ha terminado de escribir datos mientras usa el [marco de trabajo de servicios de texto](/windows/desktop/TSF/text-services-framework)o IME.</span><span class="sxs-lookup"><span data-stu-id="f3745-105">Notifies a rich edit control parent window that the user has entered new data or has finished entering data while using IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a><span data-ttu-id="f3745-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3745-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3745-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3745-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3745-108">Una estructura [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) que recibe información sobre la condición de finalización de composición.</span><span class="sxs-lookup"><span data-stu-id="f3745-108">A [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) structure that receives information about the end composition condition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3745-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3745-109">Requirements</span></span>



| <span data-ttu-id="f3745-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3745-110">Requirement</span></span> | <span data-ttu-id="f3745-111">Value</span><span class="sxs-lookup"><span data-stu-id="f3745-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3745-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3745-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f3745-113">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3745-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f3745-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3745-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f3745-115">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3745-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3745-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3745-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3745-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3745-117"><dt>Richedit.h</dt></span></span> </dl> |



 

