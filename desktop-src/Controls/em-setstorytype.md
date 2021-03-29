---
title: Mensaje EM_SETSTORYTYPE (RichEdit. h)
description: Establece el tipo de caso.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- EM_SETSTORYTYPE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905139"
---
# <a name="em_setstorytype-message"></a><span data-ttu-id="515b5-104">\_Mensaje SETSTORYTYPE em</span><span class="sxs-lookup"><span data-stu-id="515b5-104">EM\_SETSTORYTYPE message</span></span>

<span data-ttu-id="515b5-105">Establece el tipo de caso.</span><span class="sxs-lookup"><span data-stu-id="515b5-105">Sets the story type.</span></span>


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a><span data-ttu-id="515b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="515b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="515b5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="515b5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="515b5-108">Índice del caso.</span><span class="sxs-lookup"><span data-stu-id="515b5-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="515b5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="515b5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="515b5-110">El nuevo tipo de caso.</span><span class="sxs-lookup"><span data-stu-id="515b5-110">The new story type.</span></span> <span data-ttu-id="515b5-111">Para obtener una lista de tipos de caso, consulte [**em \_ GETSTORYTYPE**](em-getstorytype.md).</span><span class="sxs-lookup"><span data-stu-id="515b5-111">For a list of story types, see [**EM\_GETSTORYTYPE**](em-getstorytype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="515b5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="515b5-112">Return value</span></span>

<span data-ttu-id="515b5-113">El tipo de caso que se estableció.</span><span class="sxs-lookup"><span data-stu-id="515b5-113">The story type that was set.</span></span>

## <a name="requirements"></a><span data-ttu-id="515b5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="515b5-114">Requirements</span></span>



| <span data-ttu-id="515b5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="515b5-115">Requirement</span></span> | <span data-ttu-id="515b5-116">Value</span><span class="sxs-lookup"><span data-stu-id="515b5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="515b5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="515b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="515b5-118">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="515b5-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="515b5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="515b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="515b5-120">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="515b5-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="515b5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="515b5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="515b5-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="515b5-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





