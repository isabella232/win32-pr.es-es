---
title: Mensaje de PSM_SETTITLE (Prsht. h)
description: Establece el título de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetTitle.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- PSM_SETTITLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995971"
---
# <a name="psm_settitle-message"></a><span data-ttu-id="ba7a7-105">Mensaje de PSM \_ SETTITLE</span><span class="sxs-lookup"><span data-stu-id="ba7a7-105">PSM\_SETTITLE message</span></span>

<span data-ttu-id="ba7a7-106">Establece el título de una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ba7a7-106">Sets the title of a property sheet.</span></span> <span data-ttu-id="ba7a7-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .</span><span class="sxs-lookup"><span data-stu-id="ba7a7-107">You can send this message explicitly or by using the [**PropSheet\_SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba7a7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba7a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba7a7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba7a7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba7a7-110">Marca que indica si se deben incluir el prefijo "propiedades para" o el sufijo "propiedades" (dependiendo de la versión) con la cadena de título especificada.</span><span class="sxs-lookup"><span data-stu-id="ba7a7-110">Flag that indicates whether to include the prefix "Properties for" or the suffix "Properties" (depending on the version) with the specified title string.</span></span> <span data-ttu-id="ba7a7-111">Si este valor es PSH \_ PROPTITLE, se incluye el prefijo o el sufijo.</span><span class="sxs-lookup"><span data-stu-id="ba7a7-111">If this value is PSH\_PROPTITLE, the prefix or suffix is included.</span></span>

</dd> <dt>

<span data-ttu-id="ba7a7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba7a7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba7a7-113">Puntero a un búfer que contiene la cadena de título.</span><span class="sxs-lookup"><span data-stu-id="ba7a7-113">Pointer to a buffer that contains the title string.</span></span> <span data-ttu-id="ba7a7-114">Si el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de este parámetro es **null**, la hoja de propiedades carga el recurso de cadena especificado en [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ba7a7-114">If the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this parameter is **NULL**, the property sheet loads the string resource specified in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba7a7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba7a7-115">Return value</span></span>

<span data-ttu-id="ba7a7-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ba7a7-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba7a7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba7a7-117">Remarks</span></span>

<span data-ttu-id="ba7a7-118">En un asistente de Aero, este mensaje se puede usar para cambiar dinámicamente el título de una página interior. por ejemplo, al controlar la notificación de [ \_ SETACTIVE de PSN](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="ba7a7-118">In an Aero Wizard, this message can be used to change the title of an interior page dynamically; for example, when handling the [PSN\_SETACTIVE](psn-setactive.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba7a7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba7a7-119">Requirements</span></span>



| <span data-ttu-id="ba7a7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba7a7-120">Requirement</span></span> | <span data-ttu-id="ba7a7-121">Value</span><span class="sxs-lookup"><span data-stu-id="ba7a7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7a7-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba7a7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ba7a7-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ba7a7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ba7a7-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba7a7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ba7a7-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba7a7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ba7a7-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba7a7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba7a7-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba7a7-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="ba7a7-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ba7a7-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ba7a7-129">**PSM \_ SETTITLEW** (Unicode) y **PSM \_ SETTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ba7a7-129">**PSM\_SETTITLEW** (Unicode) and **PSM\_SETTITLEA** (ANSI)</span></span><br/>              |



 

