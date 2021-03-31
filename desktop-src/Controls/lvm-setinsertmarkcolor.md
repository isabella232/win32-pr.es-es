---
title: Mensaje de LVM_SETINSERTMARKCOLOR (commctrl. h)
description: Establece el color del punto de inserción.
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- LVM_SETINSERTMARKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260d21d083e2c70d8e82a27628e42596bd1b37eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995933"
---
# <a name="lvm_setinsertmarkcolor-message"></a><span data-ttu-id="c5b8a-104">\_Mensaje SETINSERTMARKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="c5b8a-104">LVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="c5b8a-105">Establece el color del punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="c5b8a-105">Sets the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5b8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5b8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b8a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5b8a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c5b8a-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c5b8a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c5b8a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5b8a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c5b8a-110">Estructura **COLORREF** que especifica el color para establecer el punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="c5b8a-110">**COLORREF** structure that specifies the color to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b8a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5b8a-111">Return value</span></span>

<span data-ttu-id="c5b8a-112">Devuelve la estructura **COLORREF** establecida en el color anterior.</span><span class="sxs-lookup"><span data-stu-id="c5b8a-112">Returns **COLORREF** structure set to the previous color.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5b8a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5b8a-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c5b8a-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="c5b8a-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c5b8a-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c5b8a-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c5b8a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5b8a-116">Requirements</span></span>



| <span data-ttu-id="c5b8a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5b8a-117">Requirement</span></span> | <span data-ttu-id="c5b8a-118">Value</span><span class="sxs-lookup"><span data-stu-id="c5b8a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b8a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5b8a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b8a-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c5b8a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5b8a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5b8a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b8a-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5b8a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5b8a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5b8a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5b8a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5b8a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





