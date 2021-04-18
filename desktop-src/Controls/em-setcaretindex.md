---
title: Mensaje de EM_SETCARETINDEX (CommCtrl. h)
description: Establece el valor de índice de base cero de la posición del símbolo de intercalación en un control de edición.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETCARETINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492472"
---
# <a name="em_setcaretindex-message"></a><span data-ttu-id="4189b-104">\_Mensaje SETCARETINDEX em</span><span class="sxs-lookup"><span data-stu-id="4189b-104">EM\_SETCARETINDEX message</span></span>

<span data-ttu-id="4189b-105">Establece el valor de índice de base cero de la posición del símbolo de intercalación en un control de edición.</span><span class="sxs-lookup"><span data-stu-id="4189b-105">Sets the zero-based index value of the position of the caret in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4189b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4189b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4189b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4189b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4189b-108">Nuevo valor de índice de base cero de la posición del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="4189b-108">The new zero-based index value of the position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="4189b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4189b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4189b-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4189b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4189b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4189b-111">Return value</span></span>

<span data-ttu-id="4189b-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4189b-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4189b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4189b-113">Remarks</span></span>

<span data-ttu-id="4189b-114">Si el índice está fuera del intervalo del texto en un control de edición, el índice se ajustará para que quepa en el intervalo del texto.</span><span class="sxs-lookup"><span data-stu-id="4189b-114">If the index is out of the range of the text in an edit control, the index will be adjusted to fit inside the range of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="4189b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4189b-115">Requirements</span></span>



| <span data-ttu-id="4189b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4189b-116">Requirement</span></span> | <span data-ttu-id="4189b-117">Value</span><span class="sxs-lookup"><span data-stu-id="4189b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4189b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4189b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4189b-119">Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="4189b-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4189b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4189b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4189b-121">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="4189b-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4189b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4189b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4189b-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4189b-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4189b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="4189b-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="4189b-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4189b-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4189b-126">**\_GETCARETINDEX em**</span><span class="sxs-lookup"><span data-stu-id="4189b-126">**EM\_GETCARETINDEX**</span></span>](em-getcaretindex.md)
</dt> </dl>

 

 





