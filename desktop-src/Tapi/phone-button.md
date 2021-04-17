---
description: Se envía el mensaje del botón del teléfono TAPI \_ para notificar a la aplicación que la supervisión de la pulsación de botones está habilitada si ha detectado una pulsación de botón en el teléfono local.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: Mensaje de PHONE_BUTTON (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680427"
---
# <a name="phone_button-message"></a><span data-ttu-id="93f19-103">Mensaje de botón de teléfono \_</span><span class="sxs-lookup"><span data-stu-id="93f19-103">PHONE\_BUTTON message</span></span>

<span data-ttu-id="93f19-104">Se envía el mensaje del **\_ botón del teléfono** TAPI para notificar a la aplicación que la supervisión de la pulsación de botones está habilitada si ha detectado una pulsación de botón en el teléfono local.</span><span class="sxs-lookup"><span data-stu-id="93f19-104">The TAPI **PHONE\_BUTTON** message is sent to notify the application that button press monitoring is enabled if it has detected a button press on the local phone.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="93f19-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93f19-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93f19-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="93f19-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="93f19-107">Identificador del dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="93f19-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="93f19-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="93f19-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="93f19-109">Instancia de devolución de llamada de la aplicación que se proporciona al abrir el dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="93f19-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="93f19-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="93f19-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="93f19-111">El identificador de botón o lámpara del botón que se presionó.</span><span class="sxs-lookup"><span data-stu-id="93f19-111">The button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="93f19-112">Tenga en cuenta que los identificadores de botón del 0 al 11 siempre son los botones del teclado, donde "0" es el identificador de botón cero, "1" es el identificador de botón 1 (y así sucesivamente hasta el identificador de botón 9) y "" es el identificador de \* botón 10, y " \# " es el identificador de botón 11.</span><span class="sxs-lookup"><span data-stu-id="93f19-112">Note that button identifiers zero through 11 are always the KEYPAD buttons, with '0' being button identifier zero, '1' being button identifier 1 (and so on through button identifier 9), and with '\*' being button identifier 10, and '\#' being button identifier 11.</span></span> <span data-ttu-id="93f19-113">La información adicional sobre un identificador de botón está disponible con [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) y [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span><span class="sxs-lookup"><span data-stu-id="93f19-113">Additional information about a button identifier is available with [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span></span>

</dd> <dt>

<span data-ttu-id="93f19-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="93f19-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="93f19-115">Modo de botón del botón.</span><span class="sxs-lookup"><span data-stu-id="93f19-115">The button mode of the button.</span></span> <span data-ttu-id="93f19-116">Este parámetro utiliza una de las [**\_ constantes de PHONEBUTTONMODE**](phonebuttonmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="93f19-116">This parameter uses one of the [**PHONEBUTTONMODE\_ constants**](phonebuttonmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="93f19-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="93f19-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="93f19-118">Especifica si se trata de un evento de botón o un evento de botón.</span><span class="sxs-lookup"><span data-stu-id="93f19-118">Specifies whether this is a button-down event or a button-up event.</span></span> <span data-ttu-id="93f19-119">Este parámetro utiliza una de las [**\_ constantes de PHONEBUTTONSTATE**](phonebuttonstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="93f19-119">This parameter uses one of the [**PHONEBUTTONSTATE\_ constants**](phonebuttonstate--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93f19-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93f19-120">Return value</span></span>

<span data-ttu-id="93f19-121">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="93f19-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93f19-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93f19-122">Remarks</span></span>

<span data-ttu-id="93f19-123">Se envía un mensaje de **\_ botón de teléfono** cada vez que un botón cambia de estado.</span><span class="sxs-lookup"><span data-stu-id="93f19-123">A **PHONE\_BUTTON** message is sent whenever a button changes state.</span></span> <span data-ttu-id="93f19-124">Se garantiza que una aplicación para cada evento de presionar el botón, se envía un evento Button up correspondiente.</span><span class="sxs-lookup"><span data-stu-id="93f19-124">An application is guaranteed that for each button down event, it is eventually sent a corresponding button up event.</span></span> <span data-ttu-id="93f19-125">Un proveedor de servicios que no es capaz de detectar el botón real es necesario para generar el mensaje de botón arriba justo después del mensaje de botón abajo para cada pulsación de botón.</span><span class="sxs-lookup"><span data-stu-id="93f19-125">A service provider that is incapable of detecting the actual button up is required to generate the button up message shortly after the button down message for each button press.</span></span>

## <a name="requirements"></a><span data-ttu-id="93f19-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93f19-126">Requirements</span></span>



| <span data-ttu-id="93f19-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="93f19-127">Requirement</span></span> | <span data-ttu-id="93f19-128">Value</span><span class="sxs-lookup"><span data-stu-id="93f19-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="93f19-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="93f19-129">TAPI version</span></span><br/> | <span data-ttu-id="93f19-130">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="93f19-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="93f19-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93f19-131">Header</span></span><br/>       | <dl> <span data-ttu-id="93f19-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="93f19-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93f19-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="93f19-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f19-134">**phoneGetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="93f19-134">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[<span data-ttu-id="93f19-135">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="93f19-135">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




