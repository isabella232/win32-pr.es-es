---
description: Indica que el número de botones de menú del DVD ha cambiado o que la selección del botón ha cambiado.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653856"
---
# <a name="ec_dvd_button_change"></a><span data-ttu-id="091c4-103">\_cambio de \_ botón de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="091c4-103">EC\_DVD\_BUTTON\_CHANGE</span></span>

<span data-ttu-id="091c4-104">Indica que el número de botones de menú del DVD ha cambiado o que la selección del botón ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="091c4-104">Signals that the number of DVD menu buttons has changed, or that the button selection has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="091c4-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="091c4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="091c4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="091c4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="091c4-107">Valor **DWORD** que indica el número de botones disponibles.</span><span class="sxs-lookup"><span data-stu-id="091c4-107">**DWORD** value indicating the number of available buttons.</span></span>

</dd> <dt>

<span data-ttu-id="091c4-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="091c4-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="091c4-109">Valor **DWORD** que indica el número de botón seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="091c4-109">**DWORD** value indicating the currently selected button number.</span></span> <span data-ttu-id="091c4-110">El botón número cero indica que no hay ningún botón seleccionado.</span><span class="sxs-lookup"><span data-stu-id="091c4-110">Selected button number zero implies that no button is selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="091c4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="091c4-111">Remarks</span></span>

<span data-ttu-id="091c4-112">Los números de botón oscilan entre 1 y 36.</span><span class="sxs-lookup"><span data-stu-id="091c4-112">Button numbers range from 1 to 36.</span></span>

<span data-ttu-id="091c4-113">El botón seleccionado actualmente puede cambiar automáticamente con un comando de navegación creado en el disco, así como a través del control de la aplicación mediante la interfaz [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="091c4-113">The currently selected button can change automatically with a navigation command authored on the disc as well as through application control by using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="091c4-114">Este evento puede indicar cualquiera de los números de botón disponibles.</span><span class="sxs-lookup"><span data-stu-id="091c4-114">This event can signal any of the available button numbers.</span></span> <span data-ttu-id="091c4-115">Estos números no siempre se corresponden con los números de botón usados para [**IDvdControl2:: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) porque ese método solo puede activar un subconjunto de botones.</span><span class="sxs-lookup"><span data-stu-id="091c4-115">These numbers do not always correspond to button numbers used for [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) because that method can activate only a subset of buttons.</span></span>

<span data-ttu-id="091c4-116">Este evento se desencadena en todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="091c4-116">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="091c4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="091c4-117">Requirements</span></span>



| <span data-ttu-id="091c4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="091c4-118">Requirement</span></span> | <span data-ttu-id="091c4-119">Value</span><span class="sxs-lookup"><span data-stu-id="091c4-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="091c4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="091c4-120">Header</span></span><br/> | <dl> <span data-ttu-id="091c4-121"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="091c4-121"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="091c4-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="091c4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="091c4-123">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="091c4-123">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="091c4-124">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="091c4-124">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="091c4-125">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="091c4-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




