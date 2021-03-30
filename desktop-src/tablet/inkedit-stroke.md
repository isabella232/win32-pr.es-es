---
description: Se produce cuando el usuario dibuja un nuevo objeto IInkStrokeDisp en cualquier objeto IInkTablet.
ms.assetid: fac5104d-d0da-40b1-a4a6-00a34718d09f
title: Evento InkEdit. Stroke (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d21abde9deb565f207a44ddd44b51681f1bfa6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817742"
---
# <a name="inkeditstroke-event"></a><span data-ttu-id="3da81-103">Evento InkEdit. Stroke</span><span class="sxs-lookup"><span data-stu-id="3da81-103">InkEdit.Stroke event</span></span>

<span data-ttu-id="3da81-104">Se produce cuando el usuario dibuja un nuevo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) en cualquier objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .</span><span class="sxs-lookup"><span data-stu-id="3da81-104">Occurs when the user draws a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object on any [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da81-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3da81-105">Syntax</span></span>


```C++
HRESULT Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="3da81-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3da81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da81-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3da81-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3da81-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="3da81-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="3da81-109">*Trazo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3da81-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3da81-110">Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado.</span><span class="sxs-lookup"><span data-stu-id="3da81-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="3da81-111">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3da81-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3da81-112">**Variante \_ TRUE** para cancelar la colección del objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ; **Variante \_ FALSE** para recopilar el objeto **IInkStrokeDisp** y continuar con el **trazo** incluso.</span><span class="sxs-lookup"><span data-stu-id="3da81-112">**VARIANT\_TRUE** to cancel the collection of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object; **VARIANT\_FALSE** to collect the **IInkStrokeDisp** object and continue with the **Stroke** even.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da81-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3da81-113">Return value</span></span>

<span data-ttu-id="3da81-114">Si este evento se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3da81-114">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3da81-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3da81-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3da81-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3da81-116">Remarks</span></span>

<span data-ttu-id="3da81-117">Este método de evento se define en la interfaz **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="3da81-117">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="3da81-118">La interfaz **\_ IInkEditEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeStroke.</span><span class="sxs-lookup"><span data-stu-id="3da81-118">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeStroke.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da81-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3da81-119">Requirements</span></span>



| <span data-ttu-id="3da81-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3da81-120">Requirement</span></span> | <span data-ttu-id="3da81-121">Value</span><span class="sxs-lookup"><span data-stu-id="3da81-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3da81-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3da81-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3da81-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3da81-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3da81-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3da81-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3da81-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3da81-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3da81-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3da81-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3da81-127"><dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3da81-127"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3da81-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3da81-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="3da81-129"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3da81-129"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3da81-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3da81-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da81-131">InkEdit</span><span class="sxs-lookup"><span data-stu-id="3da81-131">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="3da81-132">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="3da81-132">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="3da81-133">**Interfaz IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="3da81-133">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

