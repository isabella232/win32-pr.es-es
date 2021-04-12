---
title: Mensaje EM_GETWORDWRAPMODE (RichEdit. h)
description: Obtiene las opciones de ajuste de palabras y de salto de palabra actuales para el control Rich Edit.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- EM_GETWORDWRAPMODE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489460"
---
# <a name="em_getwordwrapmode-message"></a><span data-ttu-id="cfb45-104">\_Mensaje GETWORDWRAPMODE em</span><span class="sxs-lookup"><span data-stu-id="cfb45-104">EM\_GETWORDWRAPMODE message</span></span>

<span data-ttu-id="cfb45-105">Obtiene las opciones de ajuste de palabras y de salto de palabra actuales para el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="cfb45-105">Gets the current word wrap and word-break options for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="cfb45-106">Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="cfb45-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="cfb45-107">No se admite en las versiones posteriores de Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="cfb45-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="cfb45-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfb45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb45-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfb45-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb45-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cfb45-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cfb45-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfb45-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb45-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cfb45-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfb45-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfb45-113">Return value</span></span>

<span data-ttu-id="cfb45-114">El mensaje devuelve las opciones de ajuste de palabra y de salto de palabra actuales.</span><span class="sxs-lookup"><span data-stu-id="cfb45-114">The message returns the current word wrap and word-break options.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfb45-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfb45-115">Remarks</span></span>

<span data-ttu-id="cfb45-116">Este mensaje no se debe enviar mediante el procedimiento de separación de palabras definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cfb45-116">This message must not be sent by the application-defined, word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb45-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfb45-117">Requirements</span></span>



| <span data-ttu-id="cfb45-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfb45-118">Requirement</span></span> | <span data-ttu-id="cfb45-119">Value</span><span class="sxs-lookup"><span data-stu-id="cfb45-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb45-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfb45-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb45-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cfb45-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfb45-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfb45-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb45-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cfb45-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfb45-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfb45-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfb45-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb45-125"><dt>Richedit.h</dt></span></span> </dl> |



 

 





