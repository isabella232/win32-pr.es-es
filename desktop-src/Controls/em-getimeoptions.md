---
title: Mensaje EM_GETIMEOPTIONS (RichEdit. h)
description: Recupera las opciones actuales del editor de métodos de entrada (IME).
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- EM_GETIMEOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150666"
---
# <a name="em_getimeoptions-message"></a><span data-ttu-id="3c8bd-104">\_Mensaje GETIMEOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="3c8bd-104">EM\_GETIMEOPTIONS message</span></span>

<span data-ttu-id="3c8bd-105">Recupera las opciones actuales del editor de métodos de entrada (IME).</span><span class="sxs-lookup"><span data-stu-id="3c8bd-105">Retrieves the current Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="3c8bd-106">Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="3c8bd-107">No se admite en las versiones posteriores de Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="3c8bd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c8bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8bd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c8bd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8bd-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3c8bd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c8bd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8bd-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c8bd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c8bd-113">Return value</span></span>

<span data-ttu-id="3c8bd-114">Este mensaje devuelve uno o varios de los valores de marca de la opción IME descritos en el mensaje [**\_ SETIMEOPTIONS em**](em-setimeoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="3c8bd-114">This message returns one or more of the IME option flag values described in the [**EM\_SETIMEOPTIONS**](em-setimeoptions.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c8bd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c8bd-115">Requirements</span></span>



| <span data-ttu-id="3c8bd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c8bd-116">Requirement</span></span> | <span data-ttu-id="3c8bd-117">Value</span><span class="sxs-lookup"><span data-stu-id="3c8bd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c8bd-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c8bd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3c8bd-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3c8bd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c8bd-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c8bd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3c8bd-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c8bd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c8bd-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c8bd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c8bd-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c8bd-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c8bd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c8bd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8bd-125">**\_SETIMEOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="3c8bd-125">**EM\_SETIMEOPTIONS**</span></span>](em-setimeoptions.md)
</dt> </dl>

 

 





