---
title: Mensaje de IPM_SETFOCUS (commctrl. h)
description: Establece el foco de teclado en el campo especificado en el control de dirección IP. Se seleccionará todo el texto de ese campo.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- IPM_SETFOCUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150546"
---
# <a name="ipm_setfocus-message"></a><span data-ttu-id="29147-105">Mensaje de SETFOCUS de IPM \_</span><span class="sxs-lookup"><span data-stu-id="29147-105">IPM\_SETFOCUS message</span></span>

<span data-ttu-id="29147-106">Establece el foco de teclado en el campo especificado en el control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="29147-106">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="29147-107">Se seleccionará todo el texto de ese campo.</span><span class="sxs-lookup"><span data-stu-id="29147-107">All of the text in that field will be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="29147-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29147-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29147-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29147-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29147-110">Índice de campo basado en cero en el que se debe establecer el foco.</span><span class="sxs-lookup"><span data-stu-id="29147-110">A zero-based field index to which the focus should be set.</span></span> <span data-ttu-id="29147-111">Si este valor es mayor que el número de campos, el foco se establece en el primer campo en blanco.</span><span class="sxs-lookup"><span data-stu-id="29147-111">If this value is greater than the number of fields, focus is set to the first blank field.</span></span> <span data-ttu-id="29147-112">Si todos los campos no están en blanco, el foco se establece en el primer campo.</span><span class="sxs-lookup"><span data-stu-id="29147-112">If all fields are nonblank, focus is set to the first field.</span></span>

</dd> <dt>

<span data-ttu-id="29147-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29147-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="29147-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="29147-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29147-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29147-115">Return value</span></span>

<span data-ttu-id="29147-116">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="29147-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="29147-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29147-117">Requirements</span></span>



| <span data-ttu-id="29147-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="29147-118">Requirement</span></span> | <span data-ttu-id="29147-119">Value</span><span class="sxs-lookup"><span data-stu-id="29147-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29147-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29147-120">Minimum supported client</span></span><br/> | <span data-ttu-id="29147-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="29147-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29147-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29147-122">Minimum supported server</span></span><br/> | <span data-ttu-id="29147-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="29147-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29147-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29147-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="29147-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="29147-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





