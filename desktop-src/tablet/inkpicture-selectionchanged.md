---
description: Se produce cuando la selección de tinta dentro del control InkPicture ha cambiado, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de selección.
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: Evento InkPicture. SelectionChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14594efe4e5ecda64167ec9a0e075fc60d8e9a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659965"
---
# <a name="inkpictureselectionchanged-event"></a><span data-ttu-id="355c0-103">Evento InkPicture. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="355c0-103">InkPicture.SelectionChanged event</span></span>

<span data-ttu-id="355c0-104">Se produce cuando la selección de tinta dentro del control [InkPicture](inkpicture-control-reference.md) ha cambiado, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="355c0-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="355c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="355c0-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="355c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="355c0-106">Parameters</span></span>

<span data-ttu-id="355c0-107">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="355c0-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="355c0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="355c0-108">Return value</span></span>

<span data-ttu-id="355c0-109">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="355c0-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="355c0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="355c0-110">Remarks</span></span>

<span data-ttu-id="355c0-111">Para obtener más detalles sobre este evento, consulte el evento [**SelectionChanged**](inkoverlay-selectionchanged.md) del objeto [**InkOverlay**](inkoverlay-class.md) , que tiene la misma funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="355c0-111">For further details about this event, refer to the [**InkOverlay**](inkoverlay-class.md) object's [**SelectionChanged**](inkoverlay-selectionchanged.md) event, which has the same functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="355c0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="355c0-112">Requirements</span></span>



| <span data-ttu-id="355c0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="355c0-113">Requirement</span></span> | <span data-ttu-id="355c0-114">Value</span><span class="sxs-lookup"><span data-stu-id="355c0-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="355c0-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="355c0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="355c0-116">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="355c0-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="355c0-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="355c0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="355c0-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="355c0-118">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="355c0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="355c0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="355c0-120"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="355c0-120"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="355c0-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="355c0-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="355c0-122"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="355c0-122"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="355c0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="355c0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="355c0-124">InkPicture</span><span class="sxs-lookup"><span data-stu-id="355c0-124">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="355c0-125">[**Propiedad de selección \[ InkPicture (control)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="355c0-125">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

 




