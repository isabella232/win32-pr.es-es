---
title: Mensaje EM_SELECTIONTYPE (RichEdit. h)
description: Determina el tipo de selección de un control Rich Edit.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- EM_SELECTIONTYPE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535068"
---
# <a name="em_selectiontype-message"></a><span data-ttu-id="c2eb3-104">\_Mensaje SELECTIONTYPE em</span><span class="sxs-lookup"><span data-stu-id="c2eb3-104">EM\_SELECTIONTYPE message</span></span>

<span data-ttu-id="c2eb3-105">Determina el tipo de selección de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-105">Determines the selection type for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2eb3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2eb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2eb3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2eb3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2eb3-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c2eb3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2eb3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2eb3-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2eb3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2eb3-111">Return value</span></span>

<span data-ttu-id="c2eb3-112">Si la selección está vacía, el valor devuelto es SEL \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-112">If the selection is empty, the return value is SEL\_EMPTY.</span></span>

<span data-ttu-id="c2eb3-113">Si la selección no está vacía, el valor devuelto es un conjunto de marcas que contienen uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-113">If the selection is not empty, the return value is a set of flags containing one or more of the following values.</span></span>



| <span data-ttu-id="c2eb3-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c2eb3-114">Return code</span></span>                                                                                     | <span data-ttu-id="c2eb3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2eb3-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="c2eb3-116"><dt>**\_texto SEL**</dt></span><span class="sxs-lookup"><span data-stu-id="c2eb3-116"><dt>**SEL\_TEXT**</dt></span></span> </dl>        | <span data-ttu-id="c2eb3-117">Texto.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-117">Text.</span></span><br/>                            |
| <dl> <span data-ttu-id="c2eb3-118"><dt>**SEL ( \_ objeto)**</dt></span><span class="sxs-lookup"><span data-stu-id="c2eb3-118"><dt>**SEL\_OBJECT**</dt></span></span> </dl>      | <span data-ttu-id="c2eb3-119">Al menos un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-119">At least one COM object.</span></span><br/>         |
| <dl> <span data-ttu-id="c2eb3-120"><dt>**SEL \_ MULTIchar**</dt></span><span class="sxs-lookup"><span data-stu-id="c2eb3-120"><dt>**SEL\_MULTICHAR**</dt></span></span> </dl>   | <span data-ttu-id="c2eb3-121">Más de un carácter de texto.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-121">More than one character of text.</span></span><br/> |
| <dl> <span data-ttu-id="c2eb3-122"><dt>**SEL \_ MULTIobject**</dt></span><span class="sxs-lookup"><span data-stu-id="c2eb3-122"><dt>**SEL\_MULTIOBJECT**</dt></span></span> </dl> | <span data-ttu-id="c2eb3-123">Más de un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-123">More than one COM object.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="c2eb3-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2eb3-124">Remarks</span></span>

<span data-ttu-id="c2eb3-125">Este mensaje es útil durante el procesamiento de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) para el elemento primario de un control Rich Edit no completo.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-125">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2eb3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2eb3-126">Requirements</span></span>



| <span data-ttu-id="c2eb3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2eb3-127">Requirement</span></span> | <span data-ttu-id="c2eb3-128">Value</span><span class="sxs-lookup"><span data-stu-id="c2eb3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2eb3-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2eb3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c2eb3-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c2eb3-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2eb3-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2eb3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c2eb3-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2eb3-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2eb3-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2eb3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2eb3-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2eb3-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2eb3-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2eb3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2eb3-136">**tamaño de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c2eb3-136">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

