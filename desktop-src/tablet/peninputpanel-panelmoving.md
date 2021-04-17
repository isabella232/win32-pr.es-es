---
description: Desusado. El PenInputPanel se ha reemplazado por el panel de entrada de texto (TIP). Se produce cuando se mueve el objeto PenInputPanel.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Evento PenInputPanel. PanelMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697817"
---
# <a name="peninputpanelpanelmoving-event"></a><span data-ttu-id="cf9a8-104">Evento PenInputPanel. PanelMoving</span><span class="sxs-lookup"><span data-stu-id="cf9a8-104">PenInputPanel.PanelMoving event</span></span>

<span data-ttu-id="cf9a8-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="cf9a8-105">Deprecated.</span></span> <span data-ttu-id="cf9a8-106">El [**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por el [Panel de entrada de texto (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="cf9a8-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="cf9a8-107">Se produce cuando se mueve el objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="cf9a8-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object is moving.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9a8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf9a8-108">Syntax</span></span>


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a><span data-ttu-id="cf9a8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf9a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf9a8-110">*Izquierda* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cf9a8-110">*Left* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf9a8-111">La nueva posición horizontal, o eje x, del borde izquierdo del objeto [**PenInputPanel**](peninputpanel-class.md) , en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="cf9a8-111">The new horizontal, or x-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="cf9a8-112">*Parte superior* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cf9a8-112">*Top* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf9a8-113">Nuevo eje vertical, o y, posición del borde izquierdo del objeto [**PenInputPanel**](peninputpanel-class.md) , en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="cf9a8-113">The new vertical, or y-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf9a8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf9a8-114">Return value</span></span>

<span data-ttu-id="cf9a8-115">Si este evento se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="cf9a8-115">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf9a8-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf9a8-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf9a8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf9a8-117">Remarks</span></span>

<span data-ttu-id="cf9a8-118">El evento **PanelMoving** está diseñado para cambiar la posición del panel de entrada del lápiz cambiando los parámetros *izquierdo* y *superior* .</span><span class="sxs-lookup"><span data-stu-id="cf9a8-118">The **PanelMoving** event is designed to be used to change the position of the pen input panel by changing the *Left* and *Top* parameters.</span></span>

<span data-ttu-id="cf9a8-119">Los métodos [**moveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) y [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) hacen que el objeto [**PenInputPanel**](peninputpanel-class.md) llame a su código de posicionamiento automático que desencadena un evento **PanelMoving** .</span><span class="sxs-lookup"><span data-stu-id="cf9a8-119">The [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) and [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) methods cause the [**PenInputPanel**](peninputpanel-class.md) object to call its auto-positioning code which triggers a **PanelMoving** event.</span></span> <span data-ttu-id="cf9a8-120">Por consiguiente, llamar a estos métodos dentro de un controlador **PanelMoving** puede producir un bucle infinito recursivo.</span><span class="sxs-lookup"><span data-stu-id="cf9a8-120">Consequently, calling these methods inside a **PanelMoving** handler can result in a recursive endless loop.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf9a8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf9a8-121">Requirements</span></span>



| <span data-ttu-id="cf9a8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf9a8-122">Requirement</span></span> | <span data-ttu-id="cf9a8-123">Value</span><span class="sxs-lookup"><span data-stu-id="cf9a8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9a8-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf9a8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cf9a8-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cf9a8-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cf9a8-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf9a8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cf9a8-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cf9a8-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="cf9a8-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf9a8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf9a8-129"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cf9a8-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cf9a8-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf9a8-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf9a8-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf9a8-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="cf9a8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf9a8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf9a8-133">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="cf9a8-133">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




