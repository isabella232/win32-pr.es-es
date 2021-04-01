---
title: Mensaje de TB_GETANCHORHIGHLIGHT (commctrl. h)
description: Recupera el valor de resaltado de delimitador de una barra de herramientas.
ms.assetid: 167d481c-8684-40eb-9323-cfa238be3643
keywords:
- TB_GETANCHORHIGHLIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bfff5ef1853bbf5657604c673dcc6a9be43af83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905682"
---
# <a name="tb_getanchorhighlight-message"></a><span data-ttu-id="ee9bd-104">\_Mensaje GETANCHORHIGHLIGHT TB</span><span class="sxs-lookup"><span data-stu-id="ee9bd-104">TB\_GETANCHORHIGHLIGHT message</span></span>

<span data-ttu-id="ee9bd-105">Recupera el valor de resaltado de delimitador de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-105">Retrieves the anchor highlight setting for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee9bd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee9bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee9bd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee9bd-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ee9bd-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ee9bd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee9bd-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ee9bd-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee9bd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee9bd-111">Return value</span></span>

<span data-ttu-id="ee9bd-112">Devuelve un valor booleano que indica si se ha establecido el resaltado de delimitadores.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-112">Returns a Boolean value that indicates if anchor highlighting is set.</span></span> <span data-ttu-id="ee9bd-113">Si este valor es distinto de cero, el resaltado de delimitadores está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-113">If this value is nonzero, anchor highlighting is enabled.</span></span> <span data-ttu-id="ee9bd-114">Si este valor es cero, se deshabilita.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-114">If this value is zero, it is disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee9bd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee9bd-115">Requirements</span></span>



| <span data-ttu-id="ee9bd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee9bd-116">Requirement</span></span> | <span data-ttu-id="ee9bd-117">Value</span><span class="sxs-lookup"><span data-stu-id="ee9bd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9bd-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee9bd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee9bd-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ee9bd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee9bd-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee9bd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee9bd-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee9bd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee9bd-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee9bd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee9bd-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee9bd-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee9bd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee9bd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee9bd-125">**TB \_ SETANCHORHIGHLIGHT**</span><span class="sxs-lookup"><span data-stu-id="ee9bd-125">**TB\_SETANCHORHIGHLIGHT**</span></span>](tb-setanchorhighlight.md)
</dt> </dl>

 

 





