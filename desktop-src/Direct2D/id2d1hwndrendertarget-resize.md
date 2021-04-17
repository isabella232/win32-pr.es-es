---
title: ID2D1HwndRenderTarget cambiar el tamaño de los métodos (D2d1. h)
description: Cambia el tamaño del destino de representación al tamaño de píxel especificado.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Cambiar el tamaño de los métodos Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f15af87c59c943bd7d5dc8ece708d3603bddce6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660915"
---
# <a name="id2d1hwndrendertargetresize-methods"></a><span data-ttu-id="ce7b8-104">ID2D1HwndRenderTarget:: Resize (métodos)</span><span class="sxs-lookup"><span data-stu-id="ce7b8-104">ID2D1HwndRenderTarget::Resize methods</span></span>

<span data-ttu-id="ce7b8-105">Cambia el tamaño del destino de representación al tamaño de píxel especificado.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-105">Changes the size of the render target to the specified pixel size.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ce7b8-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="ce7b8-106">Overload list</span></span>



| <span data-ttu-id="ce7b8-107">Método</span><span class="sxs-lookup"><span data-stu-id="ce7b8-107">Method</span></span>                                                                         | <span data-ttu-id="ce7b8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce7b8-108">Description</span></span>                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="ce7b8-109">[**Cambiar tamaño (D2D1 \_ tamaño \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span><span class="sxs-lookup"><span data-stu-id="ce7b8-109">[**Resize(D2D1\_SIZE\_U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span></span>  | <span data-ttu-id="ce7b8-110">Cambia el tamaño del destino de representación al tamaño de píxel especificado.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-110">Changes the size of the render target to the specified pixel size.</span></span> <br/> |
| <span data-ttu-id="ce7b8-111">[**Cambiar tamaño (D2D1 \_ tamaño \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span><span class="sxs-lookup"><span data-stu-id="ce7b8-111">[**Resize(D2D1\_SIZE\_U\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span></span> | <span data-ttu-id="ce7b8-112">Cambia el tamaño del destino de representación al tamaño de píxel especificado.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-112">Changes the size of the render target to the specified pixel size.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="ce7b8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce7b8-113">Remarks</span></span>

<span data-ttu-id="ce7b8-114">Una vez que se llama a este método, no se define el contenido del búfer de reserva del destino de representación, aunque se haya especificado la opción de [**\_ \_ \_ conservación \_ de las opciones presentes de D2D1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) cuando se creó el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ce7b8-114">After this method is called, the contents of the render target's back-buffer are not defined, even if the [**D2D1\_PRESENT\_OPTIONS\_RETAIN\_CONTENTS**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) option was specified when the render target was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce7b8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce7b8-115">Requirements</span></span>



| <span data-ttu-id="ce7b8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce7b8-116">Requirement</span></span> | <span data-ttu-id="ce7b8-117">Value</span><span class="sxs-lookup"><span data-stu-id="ce7b8-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7b8-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce7b8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ce7b8-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce7b8-119"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce7b8-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce7b8-120">Library</span></span><br/> | <dl> <span data-ttu-id="ce7b8-121"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce7b8-121"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="ce7b8-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ce7b8-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="ce7b8-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce7b8-123"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce7b8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce7b8-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce7b8-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce7b8-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span>
</dt> </dl>

<span data-ttu-id="ce7b8-126">�</span><span class="sxs-lookup"><span data-stu-id="ce7b8-126">�</span></span>

<span data-ttu-id="ce7b8-127">�</span><span class="sxs-lookup"><span data-stu-id="ce7b8-127">�</span></span>
