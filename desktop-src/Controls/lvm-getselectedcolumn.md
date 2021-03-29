---
title: Mensaje de LVM_GETSELECTEDCOLUMN (commctrl. h)
description: Recupera un entero que especifica la columna seleccionada.
ms.assetid: 5aba5d96-50fd-439b-9782-fd5d8684b17f
keywords:
- LVM_GETSELECTEDCOLUMN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ffae9a9c7812f025241f5b46f3b1ea61bb88bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359798"
---
# <a name="lvm_getselectedcolumn-message"></a><span data-ttu-id="cc8d4-104">\_Mensaje GETSELECTEDCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="cc8d4-104">LVM\_GETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="cc8d4-105">Recupera un entero que especifica la columna seleccionada.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-105">Retrieves an integer that specifies the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc8d4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc8d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc8d4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc8d4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cc8d4-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cc8d4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc8d4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cc8d4-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc8d4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc8d4-111">Return value</span></span>

<span data-ttu-id="cc8d4-112">Devuelve un **uint** que especifica la columna seleccionada.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-112">Returns an **UINT** that specifies the selected column.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc8d4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc8d4-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cc8d4-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="cc8d4-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cc8d4-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc8d4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc8d4-116">Requirements</span></span>



| <span data-ttu-id="cc8d4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc8d4-117">Requirement</span></span> | <span data-ttu-id="cc8d4-118">Value</span><span class="sxs-lookup"><span data-stu-id="cc8d4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8d4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc8d4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cc8d4-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cc8d4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc8d4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc8d4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cc8d4-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc8d4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc8d4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc8d4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc8d4-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc8d4-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





