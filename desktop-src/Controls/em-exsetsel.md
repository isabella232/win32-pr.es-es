---
title: Mensaje EM_EXSETSEL (RichEdit. h)
description: Selecciona un intervalo de caracteres o objetos del modelo de objetos componentes (COM) en un control Rich Edit de Microsoft.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905368"
---
# <a name="em_exsetsel-message"></a><span data-ttu-id="58642-104">\_Mensaje EXSETSEL em</span><span class="sxs-lookup"><span data-stu-id="58642-104">EM\_EXSETSEL message</span></span>

<span data-ttu-id="58642-105">Selecciona un intervalo de caracteres o objetos del modelo de objetos componentes (COM) en un control Rich Edit de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="58642-105">Selects a range of characters or Component Object Model (COM) objects in a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="58642-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58642-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58642-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58642-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58642-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="58642-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="58642-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58642-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58642-110">Estructura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que especifica el intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="58642-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that specifies the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58642-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58642-111">Return value</span></span>

<span data-ttu-id="58642-112">El valor devuelto es la selección que se establece realmente.</span><span class="sxs-lookup"><span data-stu-id="58642-112">The return value is the selection that is actually set.</span></span>

## <a name="requirements"></a><span data-ttu-id="58642-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58642-113">Requirements</span></span>



| <span data-ttu-id="58642-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="58642-114">Requirement</span></span> | <span data-ttu-id="58642-115">Value</span><span class="sxs-lookup"><span data-stu-id="58642-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58642-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58642-116">Minimum supported client</span></span><br/> | <span data-ttu-id="58642-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="58642-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58642-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58642-118">Minimum supported server</span></span><br/> | <span data-ttu-id="58642-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="58642-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58642-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58642-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="58642-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="58642-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





