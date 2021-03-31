---
description: Desusado. El PenInputPanel se ha reemplazado por el panel de entrada de texto (TIP). Se produce cuando cambia el objeto PenInputPanel entre diseños.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Evento PenInputPanel. PanelChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361173"
---
# <a name="peninputpanelpanelchanged-event"></a><span data-ttu-id="58fe3-104">Evento PenInputPanel. PanelChanged</span><span class="sxs-lookup"><span data-stu-id="58fe3-104">PenInputPanel.PanelChanged event</span></span>

<span data-ttu-id="58fe3-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="58fe3-105">Deprecated.</span></span> <span data-ttu-id="58fe3-106">El [**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por el [Panel de entrada de texto (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="58fe3-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="58fe3-107">Se produce cuando cambia el objeto [**PenInputPanel**](peninputpanel-class.md) entre diseños.</span><span class="sxs-lookup"><span data-stu-id="58fe3-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object changes between layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="58fe3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58fe3-108">Syntax</span></span>


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a><span data-ttu-id="58fe3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58fe3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58fe3-110">*NewPanelType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58fe3-110">*NewPanelType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fe3-111">El nuevo tipo de panel que se usa para la entrada dentro del objeto [**PenInputPanel**](peninputpanel-class.md) , después de que se desencadene el evento **PanelChanged** .</span><span class="sxs-lookup"><span data-stu-id="58fe3-111">The new panel type used for input within the [**PenInputPanel**](peninputpanel-class.md) object, after the **PanelChanged** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58fe3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58fe3-112">Return value</span></span>

<span data-ttu-id="58fe3-113">Si este evento se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="58fe3-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="58fe3-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="58fe3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="58fe3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58fe3-115">Remarks</span></span>

<span data-ttu-id="58fe3-116">Al crear un objeto [**PenInputPanel**](peninputpanel-class.md) , la [**escritura a mano**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) es el valor predeterminado de **PanelType**.</span><span class="sxs-lookup"><span data-stu-id="58fe3-116">When creating a [**PenInputPanel**](peninputpanel-class.md) object, [**Handwriting**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) is the default **PanelType**.</span></span> <span data-ttu-id="58fe3-117">Si cambia el panel estableciendo la propiedad [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) antes de que el panel de entrada del lápiz se active por primera vez, se produce un evento **PanelChanged** .</span><span class="sxs-lookup"><span data-stu-id="58fe3-117">If you change the panel by setting the [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) property before the pen input panel becomes active for the first time, a **PanelChanged** event occurs.</span></span>

<span data-ttu-id="58fe3-118">El evento **PanelChanged** no se genera cuando el usuario cambia entre los paneles de escritura con líneas y con conversión boxing.</span><span class="sxs-lookup"><span data-stu-id="58fe3-118">The **PanelChanged** event is not raised when the user changes between Lined and Boxed writing pads.</span></span>

## <a name="requirements"></a><span data-ttu-id="58fe3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58fe3-119">Requirements</span></span>



| <span data-ttu-id="58fe3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="58fe3-120">Requirement</span></span> | <span data-ttu-id="58fe3-121">Value</span><span class="sxs-lookup"><span data-stu-id="58fe3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58fe3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58fe3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="58fe3-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="58fe3-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="58fe3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58fe3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="58fe3-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="58fe3-125">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="58fe3-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58fe3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="58fe3-127"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="58fe3-127"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="58fe3-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58fe3-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="58fe3-129"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58fe3-129"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="58fe3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="58fe3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58fe3-131">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="58fe3-131">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 
