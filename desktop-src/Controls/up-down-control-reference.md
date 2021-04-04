---
title: Control de Up-Down
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de flechas.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075559"
---
# <a name="up-down-control"></a><span data-ttu-id="62193-103">Control de Up-Down</span><span class="sxs-lookup"><span data-stu-id="62193-103">Up-Down Control</span></span>

<span data-ttu-id="62193-104">Esta sección contiene información sobre los elementos de programación utilizados con controles de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-104">This section contains information about the programming elements used with up-down controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="62193-105">Temas de introducción</span><span class="sxs-lookup"><span data-stu-id="62193-105">Overviews</span></span>



| <span data-ttu-id="62193-106">Tema</span><span class="sxs-lookup"><span data-stu-id="62193-106">Topic</span></span>                                    | <span data-ttu-id="62193-107">Contenido</span><span class="sxs-lookup"><span data-stu-id="62193-107">Contents</span></span>                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62193-108">Controles de flechas</span><span class="sxs-lookup"><span data-stu-id="62193-108">Up-Down Controls</span></span>](up-down-controls.md) | <span data-ttu-id="62193-109">Un control de flechas es un par de botones de flecha en los que el usuario puede hacer clic para aumentar o disminuir un valor, como una posición de desplazamiento o un número mostrado en un control complementario (denominado ventana relacionada).</span><span class="sxs-lookup"><span data-stu-id="62193-109">An up-down control is a pair of arrow buttons that the user can click to increment or decrement a value, such as a scroll position or a number displayed in a companion control (called a buddy window).</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="62193-110">Functions</span><span class="sxs-lookup"><span data-stu-id="62193-110">Functions</span></span>



| <span data-ttu-id="62193-111">Tema</span><span class="sxs-lookup"><span data-stu-id="62193-111">Topic</span></span>                                              | <span data-ttu-id="62193-112">Contenido</span><span class="sxs-lookup"><span data-stu-id="62193-112">Contents</span></span>                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62193-113">**CreateUpDownControl**</span><span class="sxs-lookup"><span data-stu-id="62193-113">**CreateUpDownControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | <span data-ttu-id="62193-114">Crea un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-114">Creates an up-down control.</span></span> <span data-ttu-id="62193-115">Nota: esta función está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="62193-115">Note: This function is obsolete.</span></span> <span data-ttu-id="62193-116">Es una función de 16 bits y no puede controlar valores de 32 bits para el intervalo y la posición.</span><span class="sxs-lookup"><span data-stu-id="62193-116">It is a 16 bit function and cannot handle 32 bit values for range and position.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="62193-117">error de Hadoop</span><span class="sxs-lookup"><span data-stu-id="62193-117">Messages</span></span>



| <span data-ttu-id="62193-118">Tema</span><span class="sxs-lookup"><span data-stu-id="62193-118">Topic</span></span>                                                 | <span data-ttu-id="62193-119">Contenido</span><span class="sxs-lookup"><span data-stu-id="62193-119">Contents</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62193-120">**UDM \_ GETACCEL**</span><span class="sxs-lookup"><span data-stu-id="62193-120">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)                 | <span data-ttu-id="62193-121">Recupera información de aceleración de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-121">Retrieves acceleration information for an up-down control.</span></span> <br/>                                                                                                                                                                 |
| [<span data-ttu-id="62193-122">**UDM \_ GETBASE**</span><span class="sxs-lookup"><span data-stu-id="62193-122">**UDM\_GETBASE**</span></span>](udm-getbase.md)                   | <span data-ttu-id="62193-123">Recupera la base de base actual (es decir, base 10 o 16) para un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-123">Retrieves the current radix base (that is, either base 10 or 16) for an up-down control.</span></span> <br/>                                                                                                                                   |
| [<span data-ttu-id="62193-124">**UDM \_ GETBUDDY**</span><span class="sxs-lookup"><span data-stu-id="62193-124">**UDM\_GETBUDDY**</span></span>](udm-getbuddy.md)                 | <span data-ttu-id="62193-125">Recupera el identificador de la ventana relacionada actual.</span><span class="sxs-lookup"><span data-stu-id="62193-125">Retrieves the handle to the current buddy window.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="62193-126">**UDM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="62193-126">**UDM\_GETPOS**</span></span>](udm-getpos.md)                     | <span data-ttu-id="62193-127">Recupera la posición actual de un control de flechas con una precisión de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="62193-127">Retrieves the current position of an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="62193-128">**UDM \_ GETPOS32**</span><span class="sxs-lookup"><span data-stu-id="62193-128">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)                 | <span data-ttu-id="62193-129">Devuelve la posición de 32 bits de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-129">Returns the 32-bit position of an up-down control.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="62193-130">**UDM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="62193-130">**UDM\_GETRANGE**</span></span>](udm-getrange.md)                 | <span data-ttu-id="62193-131">Recupera las posiciones mínima y máxima (intervalo) de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-131">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="62193-132">**UDM \_ GETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="62193-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)             | <span data-ttu-id="62193-133">Recupera el intervalo de 32 bits de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-133">Retrieves the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="62193-134">**UDM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="62193-134">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md) | <span data-ttu-id="62193-135">Recupera la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="62193-135">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                                                               |
| [<span data-ttu-id="62193-136">**UDM \_ SETACCEL**</span><span class="sxs-lookup"><span data-stu-id="62193-136">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)                 | <span data-ttu-id="62193-137">Establece la aceleración para un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-137">Sets the acceleration for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="62193-138">**UDM \_ SETBASE**</span><span class="sxs-lookup"><span data-stu-id="62193-138">**UDM\_SETBASE**</span></span>](udm-setbase.md)                   | <span data-ttu-id="62193-139">Establece la base de base de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-139">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="62193-140">El valor base determina si la ventana relacionada muestra números en dígitos decimales o hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="62193-140">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="62193-141">Los números hexadecimales siempre están sin signo y los números decimales están firmados.</span><span class="sxs-lookup"><span data-stu-id="62193-141">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span> <br/> |
| [<span data-ttu-id="62193-142">**UDM \_ SETBUDDY**</span><span class="sxs-lookup"><span data-stu-id="62193-142">**UDM\_SETBUDDY**</span></span>](udm-setbuddy.md)                 | <span data-ttu-id="62193-143">Establece la ventana relacionada para un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-143">Sets the buddy window for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="62193-144">**UDM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="62193-144">**UDM\_SETPOS**</span></span>](udm-setpos.md)                     | <span data-ttu-id="62193-145">Establece la posición actual de un control de flechas con una precisión de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="62193-145">Sets the current position for an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                    |
| [<span data-ttu-id="62193-146">**UDM \_ SETPOS32**</span><span class="sxs-lookup"><span data-stu-id="62193-146">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)                 | <span data-ttu-id="62193-147">Establece la posición de un control de flechas con una precisión de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="62193-147">Sets the position of an up-down control with 32-bit precision.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="62193-148">**UDM \_ SetRange**</span><span class="sxs-lookup"><span data-stu-id="62193-148">**UDM\_SETRANGE**</span></span>](udm-setrange.md)                 | <span data-ttu-id="62193-149">Establece las posiciones mínima y máxima (intervalo) de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-149">Sets the minimum and maximum positions (range) for an up-down control.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="62193-150">**UDM \_ SETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="62193-150">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)             | <span data-ttu-id="62193-151">Establece el intervalo de 32 bits de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-151">Sets the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                               |
| [<span data-ttu-id="62193-152">**UDM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="62193-152">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md) | <span data-ttu-id="62193-153">Establece la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="62193-153">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="62193-154">Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="62193-154">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/>                                   |



 

### <a name="notifications"></a><span data-ttu-id="62193-155">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="62193-155">Notifications</span></span>



| <span data-ttu-id="62193-156">Tema</span><span class="sxs-lookup"><span data-stu-id="62193-156">Topic</span></span>                                                            | <span data-ttu-id="62193-157">Contenido</span><span class="sxs-lookup"><span data-stu-id="62193-157">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62193-158">NM \_ RELEASEDCAPTURE (arriba-abajo)</span><span class="sxs-lookup"><span data-stu-id="62193-158">NM\_RELEASEDCAPTURE (up-down)</span></span>](nm-releasedcapture-up-down-.md) | <span data-ttu-id="62193-159">Notifica a la ventana primaria de un control de flechas que el control está liberando la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="62193-159">Notifies an up-down control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="62193-160">Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="62193-160">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                                                                                                                                       |
| [<span data-ttu-id="62193-161">UDN \_ DELTAPOS</span><span class="sxs-lookup"><span data-stu-id="62193-161">UDN\_DELTAPOS</span></span>](udn-deltapos.md)                                | <span data-ttu-id="62193-162">Lo envía el sistema operativo a la ventana primaria de un control de flechas cuando la posición del control está a punto de cambiar.</span><span class="sxs-lookup"><span data-stu-id="62193-162">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="62193-163">Esto sucede cuando el usuario solicita un cambio en el valor presionando la flecha arriba o abajo del control.</span><span class="sxs-lookup"><span data-stu-id="62193-163">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="62193-164">El mensaje [UDN \_ DELTAPOS](udn-deltapos.md) se envía con el formato de un mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="62193-164">The [UDN\_DELTAPOS](udn-deltapos.md) message is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="62193-165">Estructuras</span><span class="sxs-lookup"><span data-stu-id="62193-165">Structures</span></span>



| <span data-ttu-id="62193-166">Tema</span><span class="sxs-lookup"><span data-stu-id="62193-166">Topic</span></span>                        | <span data-ttu-id="62193-167">Contenido</span><span class="sxs-lookup"><span data-stu-id="62193-167">Contents</span></span>                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62193-168">**NMUPDOWN**</span><span class="sxs-lookup"><span data-stu-id="62193-168">**NMUPDOWN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | <span data-ttu-id="62193-169">Contiene información específica de los mensajes de notificación de control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-169">Contains information specific to up-down control notification messages.</span></span> <span data-ttu-id="62193-170">Es idéntico a y reemplaza a la estructura up de **nm \_** .</span><span class="sxs-lookup"><span data-stu-id="62193-170">It is identical to and replaces the **NM\_UPDOWN** structure.</span></span> <br/> |
| [<span data-ttu-id="62193-171">**UDACCEL**</span><span class="sxs-lookup"><span data-stu-id="62193-171">**UDACCEL**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | <span data-ttu-id="62193-172">Contiene información de aceleración de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-172">Contains acceleration information for an up-down control.</span></span> <br/>                                                                             |



 

### <a name="constants"></a><span data-ttu-id="62193-173">Constantes</span><span class="sxs-lookup"><span data-stu-id="62193-173">Constants</span></span>



| <span data-ttu-id="62193-174">Tema</span><span class="sxs-lookup"><span data-stu-id="62193-174">Topic</span></span>                                                | <span data-ttu-id="62193-175">Contenido</span><span class="sxs-lookup"><span data-stu-id="62193-175">Contents</span></span>                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="62193-176">Estilos de control de flechas</span><span class="sxs-lookup"><span data-stu-id="62193-176">Up-Down Control Styles</span></span>](up-down-control-styles.md) | <span data-ttu-id="62193-177">En esta sección se enumeran los estilos usados al crear controles de flechas.</span><span class="sxs-lookup"><span data-stu-id="62193-177">This section lists the styles used when creating up-down controls.</span></span><br/> |



 

 

 





