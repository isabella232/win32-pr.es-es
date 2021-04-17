---
title: Mensaje de PSM_SETHEADERTITLE (Prsht. h)
description: Establece el texto del título para el encabezado de la página interior de un asistente. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet SetHeaderTitle.
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- PSM_SETHEADERTITLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656470"
---
# <a name="psm_setheadertitle-message"></a><span data-ttu-id="16f41-105">Mensaje de PSM \_ SETHEADERTITLE</span><span class="sxs-lookup"><span data-stu-id="16f41-105">PSM\_SETHEADERTITLE message</span></span>

<span data-ttu-id="16f41-106">Establece el texto del título para el encabezado de la página interior de un asistente.</span><span class="sxs-lookup"><span data-stu-id="16f41-106">Sets the title text for the header of a wizard's interior page.</span></span> <span data-ttu-id="16f41-107">Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .</span><span class="sxs-lookup"><span data-stu-id="16f41-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="16f41-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16f41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16f41-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16f41-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16f41-110">Índice de base cero de la página del asistente.</span><span class="sxs-lookup"><span data-stu-id="16f41-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="16f41-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16f41-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16f41-112">Nuevo subtítulo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="16f41-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16f41-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16f41-113">Return value</span></span>

<span data-ttu-id="16f41-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="16f41-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f41-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16f41-115">Remarks</span></span>

<span data-ttu-id="16f41-116">Si especifica la página actual, se volverá a dibujar inmediatamente para mostrar el nuevo título.</span><span class="sxs-lookup"><span data-stu-id="16f41-116">If you specify the current page, it will immediately be repainted to display the new title.</span></span>

## <a name="requirements"></a><span data-ttu-id="16f41-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16f41-117">Requirements</span></span>



| <span data-ttu-id="16f41-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="16f41-118">Requirement</span></span> | <span data-ttu-id="16f41-119">Value</span><span class="sxs-lookup"><span data-stu-id="16f41-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16f41-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16f41-120">Minimum supported client</span></span><br/> | <span data-ttu-id="16f41-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="16f41-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="16f41-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16f41-122">Minimum supported server</span></span><br/> | <span data-ttu-id="16f41-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="16f41-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="16f41-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16f41-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="16f41-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="16f41-125"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="16f41-126">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="16f41-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="16f41-127">**PSM \_ SETHEADERTITLEW** (Unicode) y **PSM \_ SETHEADERTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="16f41-127">**PSM\_SETHEADERTITLEW** (Unicode) and **PSM\_SETHEADERTITLEA** (ANSI)</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="16f41-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="16f41-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="16f41-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="16f41-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="16f41-130">**PSM \_ HWNDTOINDEX**</span><span class="sxs-lookup"><span data-stu-id="16f41-130">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="16f41-131">**PSM \_ IDTOINDEX**</span><span class="sxs-lookup"><span data-stu-id="16f41-131">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="16f41-132">**PSM \_ PAGETOINDEX**</span><span class="sxs-lookup"><span data-stu-id="16f41-132">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





