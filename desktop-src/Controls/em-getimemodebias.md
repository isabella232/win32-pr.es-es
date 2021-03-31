---
title: Mensaje EM_GETIMEMODEBIAS (RichEdit. h)
description: Recupera el sesgo del modo editor de métodos de entrada (IME) para un control Rich Edit de Microsoft.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- EM_GETIMEMODEBIAS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079568"
---
# <a name="em_getimemodebias-message"></a><span data-ttu-id="a6dac-104">\_Mensaje GETIMEMODEBIAS em</span><span class="sxs-lookup"><span data-stu-id="a6dac-104">EM\_GETIMEMODEBIAS message</span></span>

<span data-ttu-id="a6dac-105">Recupera el sesgo del modo editor de métodos de entrada (IME) para un control Rich Edit de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a6dac-105">Retrieves the Input Method Editor (IME) mode bias for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6dac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6dac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6dac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6dac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6dac-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a6dac-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a6dac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6dac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6dac-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a6dac-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6dac-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6dac-111">Return value</span></span>

<span data-ttu-id="a6dac-112">Este mensaje devuelve la configuración de sesgo del modo IME actual.</span><span class="sxs-lookup"><span data-stu-id="a6dac-112">This message returns the current IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6dac-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6dac-113">Remarks</span></span>

<span data-ttu-id="a6dac-114">Para obtener el sesgo del modo de servicios de texto, use [**em \_ GETCTFMODEBIAS**](em-getctfmodebias.md).</span><span class="sxs-lookup"><span data-stu-id="a6dac-114">To get the Text Services Framework mode bias, use [**EM\_GETCTFMODEBIAS**](em-getctfmodebias.md).</span></span>

<span data-ttu-id="a6dac-115">La aplicación debe llamar a [**em \_ ISIME**](em-isime.md) antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="a6dac-115">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6dac-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6dac-116">Requirements</span></span>



| <span data-ttu-id="a6dac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6dac-117">Requirement</span></span> | <span data-ttu-id="a6dac-118">Value</span><span class="sxs-lookup"><span data-stu-id="a6dac-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6dac-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6dac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a6dac-120">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6dac-120">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6dac-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6dac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a6dac-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6dac-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6dac-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6dac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6dac-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6dac-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6dac-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6dac-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6dac-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a6dac-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a6dac-127">**\_ISIME em**</span><span class="sxs-lookup"><span data-stu-id="a6dac-127">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="a6dac-128">**\_GETCTFMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="a6dac-128">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> </dl>

 

 





