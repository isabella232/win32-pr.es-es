---
title: Mensaje de PSM_SETNEXTTEXT (Prsht. h)
description: Establece el texto del botón siguiente en un asistente. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetNextText.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- PSM_SETNEXTTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d781a8d76fca5c1e74bcda452b6ab7e03a32aacc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801220"
---
# <a name="psm_setnexttext-message"></a><span data-ttu-id="03fec-105">Mensaje de PSM \_ SETNEXTTEXT</span><span class="sxs-lookup"><span data-stu-id="03fec-105">PSM\_SETNEXTTEXT message</span></span>

<span data-ttu-id="03fec-106">Establece el texto del botón **siguiente** en un asistente.</span><span class="sxs-lookup"><span data-stu-id="03fec-106">Sets the text of the **Next** button in a wizard.</span></span> <span data-ttu-id="03fec-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) .</span><span class="sxs-lookup"><span data-stu-id="03fec-107">You can send this message explicitly or by using the [**PropSheet\_SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="03fec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03fec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03fec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03fec-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03fec-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="03fec-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="03fec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03fec-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03fec-112">Puntero a un búfer que contiene el texto.</span><span class="sxs-lookup"><span data-stu-id="03fec-112">Pointer to a buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03fec-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03fec-113">Return value</span></span>

<span data-ttu-id="03fec-114">No hay ningún valor devuelto significativo.</span><span class="sxs-lookup"><span data-stu-id="03fec-114">No meaningful return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03fec-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03fec-115">Requirements</span></span>



| <span data-ttu-id="03fec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="03fec-116">Requirement</span></span> | <span data-ttu-id="03fec-117">Value</span><span class="sxs-lookup"><span data-stu-id="03fec-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03fec-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03fec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="03fec-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="03fec-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="03fec-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03fec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="03fec-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="03fec-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="03fec-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03fec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="03fec-123"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="03fec-123"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="03fec-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="03fec-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="03fec-125">**PSM \_ SETNEXTTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="03fec-125">**PSM\_SETNEXTTEXTW** (Unicode)</span></span><br/>                                         |



 

 





