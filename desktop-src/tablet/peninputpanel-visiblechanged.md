---
description: Desusado. El PenInputPanel se ha reemplazado por el panel de entrada de texto (TIP). Se produce cuando el objeto PenInputPanel se ha mostrado u oculto.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: Evento PenInputPanel. VisibleChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697816"
---
# <a name="peninputpanelvisiblechanged-event"></a><span data-ttu-id="f5f08-104">Evento PenInputPanel. VisibleChanged</span><span class="sxs-lookup"><span data-stu-id="f5f08-104">PenInputPanel.VisibleChanged event</span></span>

<span data-ttu-id="f5f08-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="f5f08-105">Deprecated.</span></span> <span data-ttu-id="f5f08-106">El [**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por el [Panel de entrada de texto (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f5f08-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="f5f08-107">Se produce cuando el objeto [**PenInputPanel**](peninputpanel-class.md) se ha mostrado u oculto.</span><span class="sxs-lookup"><span data-stu-id="f5f08-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object has shown or hidden itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5f08-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5f08-108">Syntax</span></span>


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a><span data-ttu-id="f5f08-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5f08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5f08-110">*NewVisibility* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5f08-110">*NewVisibility* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f08-111">**Variante \_ TRUE** para hacer que el objeto [**PenInputPanel**](peninputpanel-class.md) se convierta en visible; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="f5f08-111">**VARIANT\_TRUE** to cause the [**PenInputPanel**](peninputpanel-class.md) object to become visible; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5f08-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5f08-112">Return value</span></span>

<span data-ttu-id="f5f08-113">Si este evento se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f5f08-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5f08-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5f08-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5f08-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5f08-115">Remarks</span></span>

<span data-ttu-id="f5f08-116">El evento **VisibleChanged** se aplica al destino de mantener el mouse del panel de entrada de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="f5f08-116">The **VisibleChanged** event applies to the Tablet PC Input Panel hover target.</span></span> <span data-ttu-id="f5f08-117">Sin embargo, no se genera cuando el destino de mantener el mouse se expande para mostrar el panel de entrada completo de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="f5f08-117">However, it is not raised when the hover target expands to show the full Tablet PC Input Panel.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f08-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5f08-118">Requirements</span></span>



| <span data-ttu-id="f5f08-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5f08-119">Requirement</span></span> | <span data-ttu-id="f5f08-120">Value</span><span class="sxs-lookup"><span data-stu-id="f5f08-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f08-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5f08-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f5f08-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f5f08-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f5f08-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5f08-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f5f08-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f5f08-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f5f08-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5f08-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5f08-126"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f5f08-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f5f08-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5f08-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5f08-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5f08-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f5f08-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5f08-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5f08-130">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="f5f08-130">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




