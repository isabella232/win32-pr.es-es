---
title: Mensaje EM_EXLINEFROMCHAR (RichEdit. h)
description: Determina qué línea contiene el carácter especificado en un control Rich Edit.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- EM_EXLINEFROMCHAR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce904725c5dc63732bae07cfaa95b41558db11d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493349"
---
# <a name="em_exlinefromchar-message"></a><span data-ttu-id="e10fd-104">\_Mensaje EXLINEFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="e10fd-104">EM\_EXLINEFROMCHAR message</span></span>

<span data-ttu-id="e10fd-105">Determina qué línea contiene el carácter especificado en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="e10fd-105">Determines which line contains the specified character in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e10fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e10fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e10fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e10fd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e10fd-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e10fd-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e10fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e10fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e10fd-110">Índice de base cero del carácter.</span><span class="sxs-lookup"><span data-stu-id="e10fd-110">Zero-based index of the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e10fd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e10fd-111">Return value</span></span>

<span data-ttu-id="e10fd-112">Este mensaje devuelve el índice de base cero de la línea.</span><span class="sxs-lookup"><span data-stu-id="e10fd-112">This message returns the zero-based index of the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="e10fd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e10fd-113">Requirements</span></span>



| <span data-ttu-id="e10fd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e10fd-114">Requirement</span></span> | <span data-ttu-id="e10fd-115">Value</span><span class="sxs-lookup"><span data-stu-id="e10fd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e10fd-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e10fd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e10fd-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e10fd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e10fd-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e10fd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e10fd-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e10fd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e10fd-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e10fd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e10fd-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e10fd-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





