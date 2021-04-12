---
title: Mensaje de RB_SETWINDOWTHEME (commctrl. h)
description: Establece el estilo visual de un control rebar.
ms.assetid: 5b32b354-3e25-4d02-9334-cc57acf41a73
keywords:
- RB_SETWINDOWTHEME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e136562394d26dd56d8d4c0c9ae916948144dbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150652"
---
# <a name="rb_setwindowtheme-message"></a><span data-ttu-id="f58fc-104">Mensaje de SETWINDOWTHEME de RB \_</span><span class="sxs-lookup"><span data-stu-id="f58fc-104">RB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="f58fc-105">Establece el estilo visual de un control rebar.</span><span class="sxs-lookup"><span data-stu-id="f58fc-105">Sets the visual style of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f58fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f58fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f58fc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f58fc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f58fc-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f58fc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f58fc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f58fc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f58fc-110">Puntero a una cadena Unicode que contiene el estilo visual de Rebar que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="f58fc-110">Pointer to a Unicode string that contains the rebar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f58fc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f58fc-111">Return value</span></span>

<span data-ttu-id="f58fc-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f58fc-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f58fc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f58fc-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f58fc-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="f58fc-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f58fc-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f58fc-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f58fc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f58fc-116">Requirements</span></span>



| <span data-ttu-id="f58fc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f58fc-117">Requirement</span></span> | <span data-ttu-id="f58fc-118">Value</span><span class="sxs-lookup"><span data-stu-id="f58fc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f58fc-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f58fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f58fc-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f58fc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f58fc-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f58fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f58fc-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f58fc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f58fc-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f58fc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f58fc-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f58fc-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





