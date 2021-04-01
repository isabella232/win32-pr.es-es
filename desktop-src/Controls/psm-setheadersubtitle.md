---
title: Mensaje de PSM_SETHEADERSUBTITLE (Prsht. h)
description: Establece el texto del subtítulo para el encabezado de la página interior de un asistente. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet SetHeaderSubTitle.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- PSM_SETHEADERSUBTITLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996331"
---
# <a name="psm_setheadersubtitle-message"></a><span data-ttu-id="829ca-105">Mensaje de PSM \_ SETHEADERSUBTITLE</span><span class="sxs-lookup"><span data-stu-id="829ca-105">PSM\_SETHEADERSUBTITLE message</span></span>

<span data-ttu-id="829ca-106">Establece el texto del subtítulo para el encabezado de la página interior de un asistente.</span><span class="sxs-lookup"><span data-stu-id="829ca-106">Sets the subtitle text for the header of a wizard's interior page.</span></span> <span data-ttu-id="829ca-107">Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .</span><span class="sxs-lookup"><span data-stu-id="829ca-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="829ca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="829ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="829ca-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="829ca-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="829ca-110">Índice de base cero de la página del asistente.</span><span class="sxs-lookup"><span data-stu-id="829ca-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="829ca-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="829ca-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="829ca-112">Nuevo subtítulo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="829ca-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="829ca-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="829ca-113">Return value</span></span>

<span data-ttu-id="829ca-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="829ca-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="829ca-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="829ca-115">Remarks</span></span>

<span data-ttu-id="829ca-116">Si especifica la página actual, se volverá a dibujar inmediatamente para mostrar el nuevo subtítulo.</span><span class="sxs-lookup"><span data-stu-id="829ca-116">If you specify the current page, it will immediately be repainted to display the new subtitle.</span></span>

> [!Note]  
> <span data-ttu-id="829ca-117">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="829ca-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="829ca-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="829ca-118">Requirements</span></span>



| <span data-ttu-id="829ca-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="829ca-119">Requirement</span></span> | <span data-ttu-id="829ca-120">Value</span><span class="sxs-lookup"><span data-stu-id="829ca-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="829ca-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="829ca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="829ca-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="829ca-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="829ca-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="829ca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="829ca-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="829ca-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="829ca-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="829ca-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="829ca-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="829ca-126"><dt>Prsht.h</dt></span></span> </dl>      |
| <span data-ttu-id="829ca-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="829ca-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="829ca-128">**PSM \_ SETHEADERSUBTITLEW** (Unicode) y **PSM \_ SETHEADERSUBTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="829ca-128">**PSM\_SETHEADERSUBTITLEW** (Unicode) and **PSM\_SETHEADERSUBTITLEA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="829ca-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="829ca-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="829ca-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="829ca-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="829ca-131">**PSM \_ HWNDTOINDEX**</span><span class="sxs-lookup"><span data-stu-id="829ca-131">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="829ca-132">**PSM \_ IDTOINDEX**</span><span class="sxs-lookup"><span data-stu-id="829ca-132">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="829ca-133">**PSM \_ PAGETOINDEX**</span><span class="sxs-lookup"><span data-stu-id="829ca-133">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





