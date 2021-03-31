---
title: Mensaje EM_SETUIANAME (RichEdit. h)
description: Establece el nombre de un control Rich Edit para la automatización de la interfaz de usuario (UIA).
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- EM_SETUIANAME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996558"
---
# <a name="em_setuianame-message"></a><span data-ttu-id="5dba3-104">\_Mensaje SETUIANAME em</span><span class="sxs-lookup"><span data-stu-id="5dba3-104">EM\_SETUIANAME message</span></span>

<span data-ttu-id="5dba3-105">Establece el nombre de un control Rich Edit para la automatización de la interfaz de usuario (UIA).</span><span class="sxs-lookup"><span data-stu-id="5dba3-105">Sets the name of a rich edit control for UI Automation (UIA).</span></span>


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a><span data-ttu-id="5dba3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5dba3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dba3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5dba3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5dba3-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5dba3-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5dba3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5dba3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5dba3-110">Puntero a la cadena de nombre terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="5dba3-110">A pointer to the null-terminated name string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dba3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5dba3-111">Return value</span></span>

<span data-ttu-id="5dba3-112">TRUE si el nombre de UIA se ha establecido correctamente; de lo contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="5dba3-112">TRUE if the name for UIA is successfully set, otherwise FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dba3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dba3-113">Requirements</span></span>



| <span data-ttu-id="5dba3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dba3-114">Requirement</span></span> | <span data-ttu-id="5dba3-115">Value</span><span class="sxs-lookup"><span data-stu-id="5dba3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5dba3-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dba3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5dba3-117">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5dba3-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5dba3-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dba3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5dba3-119">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5dba3-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5dba3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5dba3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dba3-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dba3-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





