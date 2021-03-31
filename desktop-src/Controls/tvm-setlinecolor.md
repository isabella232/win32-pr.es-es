---
title: Mensaje de TVM_SETLINECOLOR (commctrl. h)
description: El \_ mensaje TVM SETLINECOLOR establece el color de línea actual.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- TVM_SETLINECOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079483"
---
# <a name="tvm_setlinecolor-message"></a><span data-ttu-id="7fc20-104">\_Mensaje de SETLINECOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="7fc20-104">TVM\_SETLINECOLOR message</span></span>

<span data-ttu-id="7fc20-105">El mensaje **TVM \_ SETLINECOLOR** establece el color de línea actual.</span><span class="sxs-lookup"><span data-stu-id="7fc20-105">The **TVM\_SETLINECOLOR** message sets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="7fc20-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fc20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fc20-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fc20-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7fc20-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7fc20-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7fc20-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fc20-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fc20-110">Nuevo color de línea.</span><span class="sxs-lookup"><span data-stu-id="7fc20-110">New line color.</span></span> <span data-ttu-id="7fc20-111">Use el \_ valor predeterminado de CLR para restaurar los colores predeterminados del sistema.</span><span class="sxs-lookup"><span data-stu-id="7fc20-111">Use the CLR\_DEFAULT value to restore the system default colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fc20-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fc20-112">Return value</span></span>

<span data-ttu-id="7fc20-113">Devuelve el color de línea anterior.</span><span class="sxs-lookup"><span data-stu-id="7fc20-113">Returns the previous line color.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fc20-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fc20-114">Remarks</span></span>

<span data-ttu-id="7fc20-115">Este mensaje solo cambia los colores de línea.</span><span class="sxs-lookup"><span data-stu-id="7fc20-115">This message only changes line colors.</span></span> <span data-ttu-id="7fc20-116">Para cambiar los colores de los "+" y "-" dentro de los botones, use el mensaje [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc20-116">To change the colors of the '+' and '-' inside the buttons, use the [**TVM\_SETTEXTCOLOR**](tvm-settextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fc20-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fc20-117">Requirements</span></span>



| <span data-ttu-id="7fc20-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fc20-118">Requirement</span></span> | <span data-ttu-id="7fc20-119">Value</span><span class="sxs-lookup"><span data-stu-id="7fc20-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc20-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fc20-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7fc20-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7fc20-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fc20-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fc20-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7fc20-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7fc20-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fc20-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fc20-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fc20-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fc20-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fc20-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fc20-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc20-127">**TVM \_ GETLINECOLOR**</span><span class="sxs-lookup"><span data-stu-id="7fc20-127">**TVM\_GETLINECOLOR**</span></span>](tvm-getlinecolor.md)
</dt> </dl>

 

 





