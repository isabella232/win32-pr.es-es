---
title: Mensaje de RB_GETBANDBORDERS (commctrl. h)
description: Recupera los bordes de una banda. El resultado de este mensaje se puede usar para calcular el área utilizable en una banda.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- RB_GETBANDBORDERS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996724"
---
# <a name="rb_getbandborders-message"></a><span data-ttu-id="dbe23-105">Mensaje de GETBANDBORDERS de RB \_</span><span class="sxs-lookup"><span data-stu-id="dbe23-105">RB\_GETBANDBORDERS message</span></span>

<span data-ttu-id="dbe23-106">Recupera los bordes de una banda.</span><span class="sxs-lookup"><span data-stu-id="dbe23-106">Retrieves the borders of a band.</span></span> <span data-ttu-id="dbe23-107">El resultado de este mensaje se puede usar para calcular el área utilizable en una banda.</span><span class="sxs-lookup"><span data-stu-id="dbe23-107">The result of this message can be used to calculate the usable area in a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="dbe23-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dbe23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbe23-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dbe23-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe23-110">Índice de base cero de la banda para la que se van a recuperar los bordes.</span><span class="sxs-lookup"><span data-stu-id="dbe23-110">Zero-based index of the band for which the borders will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="dbe23-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbe23-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe23-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá los bordes de banda.</span><span class="sxs-lookup"><span data-stu-id="dbe23-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the band borders.</span></span> <span data-ttu-id="dbe23-113">Si el control rebar tiene el [**estilo \_ BANDBORDERS de RBS**](rebar-control-styles.md) , cada miembro de esta estructura recibirá el número de píxeles, en el lado correspondiente de la banda, que conforman el borde.</span><span class="sxs-lookup"><span data-stu-id="dbe23-113">If the rebar control has the [**RBS\_BANDBORDERS**](rebar-control-styles.md) style, each member of this structure will receive the number of pixels, on the corresponding side of the band, that constitute the border.</span></span> <span data-ttu-id="dbe23-114">Si el control rebar no tiene el estilo **\_ BANDBORDERS de RBS** , solo el miembro **izquierdo** de esta estructura recibe información válida.</span><span class="sxs-lookup"><span data-stu-id="dbe23-114">If the rebar control does not have the **RBS\_BANDBORDERS** style, only the **left** member of this structure receives valid information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbe23-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbe23-115">Return value</span></span>

<span data-ttu-id="dbe23-116">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="dbe23-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe23-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbe23-117">Requirements</span></span>



| <span data-ttu-id="dbe23-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbe23-118">Requirement</span></span> | <span data-ttu-id="dbe23-119">Value</span><span class="sxs-lookup"><span data-stu-id="dbe23-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe23-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbe23-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe23-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dbe23-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dbe23-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbe23-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe23-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dbe23-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dbe23-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbe23-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbe23-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe23-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

