---
title: Mensaje de TVM_GETLINECOLOR (commctrl. h)
description: El \_ mensaje TVM GETLINECOLOR obtiene el color de línea actual.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- TVM_GETLINECOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079521"
---
# <a name="tvm_getlinecolor-message"></a><span data-ttu-id="8e1e9-104">\_Mensaje de GETLINECOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="8e1e9-104">TVM\_GETLINECOLOR message</span></span>

<span data-ttu-id="8e1e9-105">El mensaje **TVM \_ GETLINECOLOR** obtiene el color de línea actual.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-105">The **TVM\_GETLINECOLOR** message gets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e1e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e1e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e1e9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e1e9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8e1e9-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8e1e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e1e9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8e1e9-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e1e9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e1e9-111">Return value</span></span>

<span data-ttu-id="8e1e9-112">Devuelve el color de línea actual o el valor predeterminado de CLR si no se ha \_ especificado ninguno.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-112">Returns the current line color, or the CLR\_DEFAULT value if none has been specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e1e9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e1e9-113">Remarks</span></span>

<span data-ttu-id="8e1e9-114">Este mensaje solo recupera los colores de línea.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-114">This message only retrieves line colors.</span></span> <span data-ttu-id="8e1e9-115">Para recuperar los colores de los "+" y "-" dentro de los botones, use el mensaje [**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="8e1e9-115">To retrieve the colors of the '+' and '-' inside the buttons, use the [**TVM\_GETTEXTCOLOR**](tvm-gettextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1e9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e1e9-116">Requirements</span></span>



| <span data-ttu-id="8e1e9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e1e9-117">Requirement</span></span> | <span data-ttu-id="8e1e9-118">Value</span><span class="sxs-lookup"><span data-stu-id="8e1e9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1e9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e1e9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8e1e9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8e1e9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e1e9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e1e9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8e1e9-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e1e9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e1e9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e1e9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e1e9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e1e9-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e1e9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e1e9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1e9-126">**TVM \_ SETLINECOLOR**</span><span class="sxs-lookup"><span data-stu-id="8e1e9-126">**TVM\_SETLINECOLOR**</span></span>](tvm-setlinecolor.md)
</dt> </dl>

 

 





