---
title: Mensaje de TB_SETBOUNDINGSIZE (commctrl. h)
description: Establece el tamaño de límite de un control de barra de herramientas de varias columnas.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- TB_SETBOUNDINGSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904986"
---
# <a name="tb_setboundingsize-message"></a><span data-ttu-id="5e9e8-104">\_Mensaje SETBOUNDINGSIZE TB</span><span class="sxs-lookup"><span data-stu-id="5e9e8-104">TB\_SETBOUNDINGSIZE message</span></span>

<span data-ttu-id="5e9e8-105">\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.</span><span class="sxs-lookup"><span data-stu-id="5e9e8-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="5e9e8-106">Es posible que este mensaje no se admita en versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5e9e8-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="5e9e8-107">Establece el tamaño de límite de un control de barra de herramientas de varias columnas.</span><span class="sxs-lookup"><span data-stu-id="5e9e8-107">Sets the bounding size for a multi-column toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e9e8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e9e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e9e8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e9e8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e9e8-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5e9e8-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5e9e8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e9e8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e9e8-112">Puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) cuyo miembro **CY** contiene el alto de límite.</span><span class="sxs-lookup"><span data-stu-id="5e9e8-112">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure whose **cy** member contains the bounding height.</span></span> <span data-ttu-id="5e9e8-113">Se omite el miembro de **CX** (el ancho).</span><span class="sxs-lookup"><span data-stu-id="5e9e8-113">The **cx** member (the width) is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e9e8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e9e8-114">Return value</span></span>

<span data-ttu-id="5e9e8-115">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="5e9e8-115">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="5e9e8-116">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="5e9e8-116">Security Considerations</span></span>

<span data-ttu-id="5e9e8-117">El uso de este mensaje podría poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="5e9e8-117">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e9e8-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e9e8-118">Remarks</span></span>

<span data-ttu-id="5e9e8-119">El tamaño de límite controla cómo se organizan los botones en columnas.</span><span class="sxs-lookup"><span data-stu-id="5e9e8-119">The bounding size controls how buttons are organized into columns.</span></span> <span data-ttu-id="5e9e8-120">Si el control de barra de herramientas no tiene el estilo de [**\_ \_ varias columnas TBSTYLE**](toolbar-extended-styles.md) , este mensaje no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="5e9e8-120">If the toolbar control does not have the [**TBSTYLE\_EX\_MULTICOLUMN**](toolbar-extended-styles.md) style, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e9e8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e9e8-121">Requirements</span></span>



| <span data-ttu-id="5e9e8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e9e8-122">Requirement</span></span> | <span data-ttu-id="5e9e8-123">Value</span><span class="sxs-lookup"><span data-stu-id="5e9e8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e9e8-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e9e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5e9e8-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e9e8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e9e8-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e9e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5e9e8-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e9e8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e9e8-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e9e8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e9e8-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e9e8-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

