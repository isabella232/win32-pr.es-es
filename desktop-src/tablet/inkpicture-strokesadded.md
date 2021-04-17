---
description: Se produce cuando se agregan uno o más objetos IInkStrokeDisp a la colección InkStrokes.
ms.assetid: 577ad52b-ecd3-4a49-8997-481ebdb47203
title: Evento InkPicture. StrokesAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e79d87a4315068cbb0cf9db25b6532bc4c09943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716588"
---
# <a name="inkpicturestrokesadded-event"></a><span data-ttu-id="2f88f-103">Evento InkPicture. StrokesAdded</span><span class="sxs-lookup"><span data-stu-id="2f88f-103">InkPicture.StrokesAdded event</span></span>

<span data-ttu-id="2f88f-104">Se produce cuando se agregan uno o más objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) a la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2f88f-104">Occurs when one or more [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f88f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f88f-105">Syntax</span></span>


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="2f88f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f88f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f88f-107">*StrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f88f-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f88f-108">La matriz de enteros de los identificadores de cada objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) agregado cuando se produce este evento.</span><span class="sxs-lookup"><span data-stu-id="2f88f-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object added when this event occurs.</span></span>

<span data-ttu-id="2f88f-109">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="2f88f-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f88f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f88f-110">Return value</span></span>

<span data-ttu-id="2f88f-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="2f88f-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f88f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f88f-112">Remarks</span></span>

<span data-ttu-id="2f88f-113">Este método de evento se define en la interfaz **\_ IInkStrokesEvents** .</span><span class="sxs-lookup"><span data-stu-id="2f88f-113">This event method is defined in the **\_IInkStrokesEvents** interface.</span></span> <span data-ttu-id="2f88f-114">La interfaz **\_ IInkStrokesEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ SEStrokesAdded.</span><span class="sxs-lookup"><span data-stu-id="2f88f-114">The **\_IInkStrokesEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f88f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f88f-115">Requirements</span></span>



| <span data-ttu-id="2f88f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f88f-116">Requirement</span></span> | <span data-ttu-id="2f88f-117">Value</span><span class="sxs-lookup"><span data-stu-id="2f88f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f88f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f88f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2f88f-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2f88f-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2f88f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f88f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2f88f-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2f88f-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2f88f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f88f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f88f-123"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2f88f-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2f88f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f88f-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f88f-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f88f-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2f88f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f88f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f88f-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="2f88f-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

