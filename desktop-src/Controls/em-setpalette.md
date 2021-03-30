---
title: Mensaje EM_SETPALETTE (RichEdit. h)
description: Cambia la paleta que un control Rich Edit utiliza para la ventana de presentación.
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- EM_SETPALETTE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026a0a85001818b6f69366e8dba80ef56a7a8f20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079272"
---
# <a name="em_setpalette-message"></a><span data-ttu-id="16fbf-104">\_Mensaje SETPALETTE em</span><span class="sxs-lookup"><span data-stu-id="16fbf-104">EM\_SETPALETTE message</span></span>

<span data-ttu-id="16fbf-105">Cambia la paleta que un control Rich Edit utiliza para la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="16fbf-105">Changes the palette that a rich edit control uses for its display window.</span></span>

## <a name="parameters"></a><span data-ttu-id="16fbf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16fbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16fbf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16fbf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16fbf-108">Identificador de la nueva paleta utilizada por el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="16fbf-108">Handle to the new palette used by the rich edit control.</span></span>

</dd> <dt>

<span data-ttu-id="16fbf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16fbf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16fbf-110">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="16fbf-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16fbf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16fbf-111">Return value</span></span>

<span data-ttu-id="16fbf-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="16fbf-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16fbf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16fbf-113">Remarks</span></span>

<span data-ttu-id="16fbf-114">El control Rich Edit no comprueba si la nueva paleta es válida.</span><span class="sxs-lookup"><span data-stu-id="16fbf-114">The rich edit control does not check whether the new palette is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="16fbf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16fbf-115">Requirements</span></span>



| <span data-ttu-id="16fbf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="16fbf-116">Requirement</span></span> | <span data-ttu-id="16fbf-117">Value</span><span class="sxs-lookup"><span data-stu-id="16fbf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16fbf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16fbf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="16fbf-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="16fbf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16fbf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16fbf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="16fbf-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="16fbf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16fbf-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16fbf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="16fbf-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="16fbf-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 





