---
title: Evento DragComplete
description: Evento DragComplete
ms.assetid: b48e7097-9d9d-4eab-9dfc-68dbc9793382
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a02fe98e4cf3cdefc1b7734305067550e4923
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695344"
---
# <a name="dragcomplete-event"></a><span data-ttu-id="28253-103">Evento DragComplete</span><span class="sxs-lookup"><span data-stu-id="28253-103">DragComplete Event</span></span>

<span data-ttu-id="28253-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="28253-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="28253-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="28253-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="28253-106">Se produce cuando el usuario completa el arrastre de un carácter.</span><span class="sxs-lookup"><span data-stu-id="28253-106">Occurs when the user completes dragging a character.</span></span>

</dd> <dt>

<span data-ttu-id="28253-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="28253-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="28253-108">**Sub** *Agent \* \* \* \_ DragComplete* \*  **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="28253-108">**Sub** *agent\*\*\*\_DragComplete*\* **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y\*\*\*)*\*</span></span>



| <span data-ttu-id="28253-109">Parte</span><span class="sxs-lookup"><span data-stu-id="28253-109">Part</span></span>          | <span data-ttu-id="28253-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="28253-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28253-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="28253-111">*CharacterID*</span></span> | <span data-ttu-id="28253-112">Devuelve el identificador del carácter arrastrado como una cadena.</span><span class="sxs-lookup"><span data-stu-id="28253-112">Returns the ID of the dragged character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="28253-113">*Botón*</span><span class="sxs-lookup"><span data-stu-id="28253-113">*Button*</span></span>      | <span data-ttu-id="28253-114">Devuelve un entero que identifica el botón que se presionó y liberó para provocar el evento.</span><span class="sxs-lookup"><span data-stu-id="28253-114">Returns an integer that identifies the button that was pressed and released to cause the event.</span></span> <span data-ttu-id="28253-115">El argumento del botón es un campo de bits que se corresponde con el botón izquierdo (bit 0), el botón derecho (bit 1) y el botón central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="28253-115">The button argument is a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="28253-116">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="28253-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="28253-117">Solo se establece uno de los bits, que indica el botón que causó el evento.</span><span class="sxs-lookup"><span data-stu-id="28253-117">Only one of the bits is set, indicating the button that caused the event.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="28253-118">*Shift*</span><span class="sxs-lookup"><span data-stu-id="28253-118">*Shift*</span></span>       | <span data-ttu-id="28253-119">Devuelve un entero que corresponde al estado de las teclas Mayús, CTRL y ALT cuando el botón especificado en el argumento de botón se presiona o se suelta.</span><span class="sxs-lookup"><span data-stu-id="28253-119">Returns an integer that corresponds to the state of the SHIFT, CTRL, and ALT keys when the button specified in the button argument is pressed or released.</span></span> <span data-ttu-id="28253-120">Un bit se establece si la tecla está presionada.</span><span class="sxs-lookup"><span data-stu-id="28253-120">A bit is set if the key is down.</span></span> <span data-ttu-id="28253-121">El argumento Shift es un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="28253-121">The shift argument is a bitfield with the least-significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="28253-122">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="28253-122">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="28253-123">El argumento Shift indica el estado de estas claves.</span><span class="sxs-lookup"><span data-stu-id="28253-123">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="28253-124">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.</span><span class="sxs-lookup"><span data-stu-id="28253-124">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span> <span data-ttu-id="28253-125">Por ejemplo, si se presionó CTRL y ALT, el valor de Shift sería 6.</span><span class="sxs-lookup"><span data-stu-id="28253-125">For example, if both CTRL and ALT were pressed, the value of shift would be 6.</span></span> |
| <span data-ttu-id="28253-126">*X, Y*</span><span class="sxs-lookup"><span data-stu-id="28253-126">*X,Y*</span></span>         | <span data-ttu-id="28253-127">Devuelve un entero que especifica la ubicación actual del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="28253-127">Returns an integer that specifies the current location of the mouse pointer.</span></span> <span data-ttu-id="28253-128">Los valores X e y se expresan siempre en píxeles, con respecto a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="28253-128">The X and Y values are always expressed in pixels, relative to the upper left corner of the screen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="28253-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28253-129">Remarks</span></span>

<span data-ttu-id="28253-130">Este evento solo se envía al cliente de entrada-activo de un carácter.</span><span class="sxs-lookup"><span data-stu-id="28253-130">This event is sent only to the input-active client of a character.</span></span> <span data-ttu-id="28253-131">Cuando el usuario arrastra un carácter sin ningún cliente de entrada-activo, el servidor establece su último cliente de entrada-activo como el cliente de entrada-activo actual, enviando el evento [**ActivateInput**](activateinput-event.md) a ese cliente y, a continuación, enviando los eventos [**DragStart**](dragstart-event.md) y **DragComplete** .</span><span class="sxs-lookup"><span data-stu-id="28253-131">When the user drags a character with no input-active client, the server sets its last input-active client as the current input-active client, sending the [**ActivateInput**](activateinput-event.md) event to that client, and then sending the [**DragStart**](dragstart-event.md) and **DragComplete** events.</span></span>

### <a name="see-also"></a><span data-ttu-id="28253-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="28253-132">See Also</span></span>

[<span data-ttu-id="28253-133">**Evento DragStart**</span><span class="sxs-lookup"><span data-stu-id="28253-133">**DragStart event**</span></span>](dragstart-event.md)


 

 




