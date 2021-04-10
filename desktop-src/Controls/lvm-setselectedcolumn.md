---
title: Mensaje de LVM_SETSELECTEDCOLUMN (commctrl. h)
description: Establece el índice de la columna seleccionada.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- LVM_SETSELECTEDCOLUMN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827c41fabaea722bb2372c6bd3f7c3a54bee92f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905701"
---
# <a name="lvm_setselectedcolumn-message"></a><span data-ttu-id="f573a-104">\_Mensaje SETSELECTEDCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="f573a-104">LVM\_SETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="f573a-105">Establece el índice de la columna seleccionada.</span><span class="sxs-lookup"><span data-stu-id="f573a-105">Sets the index of the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="f573a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f573a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f573a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f573a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f573a-108">Valor de tipo **int** que especifica el índice de columna.</span><span class="sxs-lookup"><span data-stu-id="f573a-108">Value of type **int** that specifies the column index.</span></span></dd> <dt>

<span data-ttu-id="f573a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f573a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f573a-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f573a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f573a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f573a-111">Return value</span></span>

<span data-ttu-id="f573a-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f573a-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f573a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f573a-113">Remarks</span></span>

<span data-ttu-id="f573a-114">Los índices de columna se almacenan en una matriz **int** .</span><span class="sxs-lookup"><span data-stu-id="f573a-114">The column indices are stored in an **int** array.</span></span> <span data-ttu-id="f573a-115">Vea el miembro **puColumns** de [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span><span class="sxs-lookup"><span data-stu-id="f573a-115">See the **puColumns** member of [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span></span>

> [!Note]  
> <span data-ttu-id="f573a-116">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="f573a-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f573a-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f573a-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f573a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f573a-118">Requirements</span></span>



| <span data-ttu-id="f573a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f573a-119">Requirement</span></span> | <span data-ttu-id="f573a-120">Value</span><span class="sxs-lookup"><span data-stu-id="f573a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f573a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f573a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f573a-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f573a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f573a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f573a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f573a-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f573a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f573a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f573a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f573a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f573a-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





