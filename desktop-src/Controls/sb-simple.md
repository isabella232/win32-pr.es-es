---
title: Mensaje de SB_SIMPLE (commctrl. h)
description: Especifica si una ventana de estado muestra texto simple o muestra todos los elementos de ventana establecidos por un mensaje SETPARTS de SB anterior \_ .
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- SB_SIMPLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150747"
---
# <a name="sb_simple-message"></a><span data-ttu-id="d9aab-104">\_Mensaje simple de SB</span><span class="sxs-lookup"><span data-stu-id="d9aab-104">SB\_SIMPLE message</span></span>

<span data-ttu-id="d9aab-105">Especifica si una ventana de estado muestra texto simple o muestra todos los elementos de ventana establecidos por un mensaje [**\_ SETPARTS de SB**](sb-setparts.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="d9aab-105">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9aab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9aab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9aab-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9aab-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9aab-108">Marca de tipo de presentación.</span><span class="sxs-lookup"><span data-stu-id="d9aab-108">Display type flag.</span></span> <span data-ttu-id="d9aab-109">Si este parámetro es **true**, la ventana muestra texto simple.</span><span class="sxs-lookup"><span data-stu-id="d9aab-109">If this parameter is **TRUE**, the window displays simple text.</span></span> <span data-ttu-id="d9aab-110">Si es **false**, muestra varias partes.</span><span class="sxs-lookup"><span data-stu-id="d9aab-110">If it is **FALSE**, it displays multiple parts.</span></span>

</dd> <dt>

<span data-ttu-id="d9aab-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9aab-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d9aab-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d9aab-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9aab-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9aab-113">Return value</span></span>

<span data-ttu-id="d9aab-114">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d9aab-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9aab-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9aab-115">Remarks</span></span>

<span data-ttu-id="d9aab-116">Si la ventana de estado se está cambiando de no simple a simple, o viceversa, la ventana se vuelve a dibujar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="d9aab-116">If the status window is being changed from nonsimple to simple, or vice versa, the window is immediately redrawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9aab-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9aab-117">Requirements</span></span>



| <span data-ttu-id="d9aab-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9aab-118">Requirement</span></span> | <span data-ttu-id="d9aab-119">Value</span><span class="sxs-lookup"><span data-stu-id="d9aab-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9aab-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9aab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d9aab-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9aab-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9aab-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9aab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d9aab-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9aab-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9aab-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9aab-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9aab-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9aab-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





