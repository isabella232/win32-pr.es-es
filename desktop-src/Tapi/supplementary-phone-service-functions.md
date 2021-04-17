---
description: Las funciones de servicio de teléfono complementarias se enumeran por Categoría en los temas siguientes.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Funciones de servicio de teléfono complementarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c39441a924a4f9787d22bf8db596882e7f257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677795"
---
# <a name="supplementary-phone-service-functions"></a><span data-ttu-id="6cea7-103">Funciones de servicio de teléfono complementarias</span><span class="sxs-lookup"><span data-stu-id="6cea7-103">Supplementary Phone Service Functions</span></span>

<span data-ttu-id="6cea7-104">Las funciones de servicio de teléfono complementarias se enumeran por Categoría en los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="6cea7-104">The supplementary phone service functions are listed by category in the following topics.</span></span> <span data-ttu-id="6cea7-105">Una función se identifica como [*asincrónica*](a-tapgloss.md) si indica la finalización en un mensaje de respuesta a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6cea7-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="6cea7-106">Si la función devuelve siempre su resultado a la aplicación inmediatamente, la función se considera [*sincrónica*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="6cea7-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="6cea7-107">A continuación se encuentra una agrupación funcional de las funciones de servicio de teléfono complementarias:</span><span class="sxs-lookup"><span data-stu-id="6cea7-107">Following is a functional grouping of the supplementary phone service functions:</span></span>

-   [<span data-ttu-id="6cea7-108">Botones</span><span class="sxs-lookup"><span data-stu-id="6cea7-108">Buttons</span></span>](#buttons)
-   [<span data-ttu-id="6cea7-109">Áreas de datos</span><span class="sxs-lookup"><span data-stu-id="6cea7-109">Data areas</span></span>](#data-areas)
-   [<span data-ttu-id="6cea7-110">Pantalla</span><span class="sxs-lookup"><span data-stu-id="6cea7-110">Display</span></span>](#display)
-   [<span data-ttu-id="6cea7-111">Dispositivos conmutador</span><span class="sxs-lookup"><span data-stu-id="6cea7-111">Hookswitch devices</span></span>](#hookswitch-devices)
-   [<span data-ttu-id="6cea7-112">Lámparas</span><span class="sxs-lookup"><span data-stu-id="6cea7-112">Lamps</span></span>](#lamps)
-   [<span data-ttu-id="6cea7-113">Apertura y cierre de dispositivos telefónicos</span><span class="sxs-lookup"><span data-stu-id="6cea7-113">Opening and closing phone devices</span></span>](#opening-and-closing-phone-devices)
-   [<span data-ttu-id="6cea7-114">Inicialización y cierre del teléfono</span><span class="sxs-lookup"><span data-stu-id="6cea7-114">Phone initialization and shutdown</span></span>](#phone-initialization-and-shutdown)
-   [<span data-ttu-id="6cea7-115">Estado y capacidades del teléfono</span><span class="sxs-lookup"><span data-stu-id="6cea7-115">Phone status and capabilities</span></span>](#phone-status-and-capabilities)
-   [<span data-ttu-id="6cea7-116">Negociación de la versión de teléfono</span><span class="sxs-lookup"><span data-stu-id="6cea7-116">Phone version negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="6cea7-117">Pistón</span><span class="sxs-lookup"><span data-stu-id="6cea7-117">Ring</span></span>](#ring)
-   [<span data-ttu-id="6cea7-118">Estado</span><span class="sxs-lookup"><span data-stu-id="6cea7-118">Status</span></span>](#status)

## <a name="phone-initialization-and-shutdown"></a><span data-ttu-id="6cea7-119">Inicialización y cierre del teléfono</span><span class="sxs-lookup"><span data-stu-id="6cea7-119">Phone Initialization and Shutdown</span></span>



| <span data-ttu-id="6cea7-120">Función</span><span class="sxs-lookup"><span data-stu-id="6cea7-120">Function</span></span>                                       | <span data-ttu-id="6cea7-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cea7-121">Description</span></span>                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cea7-122">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="6cea7-122">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | <span data-ttu-id="6cea7-123">Inicializa la abstracción del teléfono TAPI para su uso por parte de la aplicación que invoca.</span><span class="sxs-lookup"><span data-stu-id="6cea7-123">Initializes TAPI phone abstraction for use by the invoking application.</span></span> <span data-ttu-id="6cea7-124">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-124">Synchronous.</span></span> |
| [<span data-ttu-id="6cea7-125">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="6cea7-125">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | <span data-ttu-id="6cea7-126">Cierra el uso de una aplicación de la abstracción de teléfono de TAPI.</span><span class="sxs-lookup"><span data-stu-id="6cea7-126">Shuts down an application's use of TAPI's phone abstraction.</span></span> <span data-ttu-id="6cea7-127">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-127">Synchronous.</span></span>            |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="6cea7-128">Negociación de la versión de teléfono</span><span class="sxs-lookup"><span data-stu-id="6cea7-128">Phone Version Negotiation</span></span>



| <span data-ttu-id="6cea7-129">Función</span><span class="sxs-lookup"><span data-stu-id="6cea7-129">Function</span></span>                                                     | <span data-ttu-id="6cea7-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cea7-130">Description</span></span>                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="6cea7-131">**phoneNegotiateAPIVersion**</span><span class="sxs-lookup"><span data-stu-id="6cea7-131">**phoneNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | <span data-ttu-id="6cea7-132">Permite a una aplicación negociar una versión de TAPI para usarla.</span><span class="sxs-lookup"><span data-stu-id="6cea7-132">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="6cea7-133">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-133">Synchronous.</span></span> |



 

## <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="6cea7-134">Apertura y cierre de dispositivos telefónicos</span><span class="sxs-lookup"><span data-stu-id="6cea7-134">Opening and Closing Phone Devices</span></span>



| <span data-ttu-id="6cea7-135">Función</span><span class="sxs-lookup"><span data-stu-id="6cea7-135">Function</span></span>                         | <span data-ttu-id="6cea7-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cea7-136">Description</span></span>                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cea7-137">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="6cea7-137">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | <span data-ttu-id="6cea7-138">Abre el dispositivo de teléfono especificado, lo que permite a la aplicación tener privilegios de propietario o de supervisión.</span><span class="sxs-lookup"><span data-stu-id="6cea7-138">Opens the specified phone device, giving the application either owner or monitor privileges.</span></span> <span data-ttu-id="6cea7-139">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-139">Synchronous.</span></span> |
| [<span data-ttu-id="6cea7-140">**phoneClose**</span><span class="sxs-lookup"><span data-stu-id="6cea7-140">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | <span data-ttu-id="6cea7-141">Cierra un dispositivo telefónico abierto especificado.</span><span class="sxs-lookup"><span data-stu-id="6cea7-141">Closes a specified open phone device.</span></span> <span data-ttu-id="6cea7-142">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-142">Synchronous.</span></span>                                                        |



 

## <a name="phone-status-and-capabilities"></a><span data-ttu-id="6cea7-143">Estado y capacidades del teléfono</span><span class="sxs-lookup"><span data-stu-id="6cea7-143">Phone Status and Capabilities</span></span>



| <span data-ttu-id="6cea7-144">Función</span><span class="sxs-lookup"><span data-stu-id="6cea7-144">Function</span></span>                                       | <span data-ttu-id="6cea7-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cea7-145">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cea7-146">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="6cea7-146">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | <span data-ttu-id="6cea7-147">Devuelve las capacidades de un dispositivo telefónico determinado.</span><span class="sxs-lookup"><span data-stu-id="6cea7-147">Returns the capabilities of a given phone device.</span></span> <span data-ttu-id="6cea7-148">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-148">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="6cea7-149">**phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="6cea7-149">**phoneGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | <span data-ttu-id="6cea7-150">Devuelve un identificador de dispositivo para la clase de dispositivo especificada asociada al dispositivo telefónico especificado.</span><span class="sxs-lookup"><span data-stu-id="6cea7-150">Returns a device ID for the given device class associated with the specified phone device.</span></span> <span data-ttu-id="6cea7-151">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-151">Synchronous.</span></span>                                                          |
| [<span data-ttu-id="6cea7-152">**phoneGetIcon**</span><span class="sxs-lookup"><span data-stu-id="6cea7-152">**phoneGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | <span data-ttu-id="6cea7-153">Permite que una aplicación recupere un icono para mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="6cea7-153">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="6cea7-154">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-154">Synchronous.</span></span>                                                                                  |
| [<span data-ttu-id="6cea7-155">**phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="6cea7-155">**phoneConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | <span data-ttu-id="6cea7-156">Hace que el proveedor del dispositivo telefónico especificado muestre un cuadro de diálogo que permite al usuario configurar los parámetros relacionados con el dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="6cea7-156">Causes the provider of the specified phone device to display a dialog box that allows the user to configure parameters related to the phone device.</span></span> <span data-ttu-id="6cea7-157">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-157">Synchronous.</span></span> |



 

## <a name="hookswitch-devices"></a><span data-ttu-id="6cea7-158">Dispositivos conmutador</span><span class="sxs-lookup"><span data-stu-id="6cea7-158">Hookswitch Devices</span></span>



| <span data-ttu-id="6cea7-159">Función</span><span class="sxs-lookup"><span data-stu-id="6cea7-159">Function</span></span>                                         | <span data-ttu-id="6cea7-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cea7-160">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cea7-161">**phoneSetHookSwitch**</span><span class="sxs-lookup"><span data-stu-id="6cea7-161">**phoneSetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | <span data-ttu-id="6cea7-162">Establece el estado de enlace de los dispositivos conmutador de un teléfono abierto en un modo especificado.</span><span class="sxs-lookup"><span data-stu-id="6cea7-162">Sets the hook state of an open phone's hookswitch devices to a specified mode.</span></span> <span data-ttu-id="6cea7-163">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="6cea7-163">Asynchronous.</span></span>      |
| [<span data-ttu-id="6cea7-164">**phoneGetHookSwitch**</span><span class="sxs-lookup"><span data-stu-id="6cea7-164">**phoneGetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | <span data-ttu-id="6cea7-165">Consulta el modo conmutador de un dispositivo conmutador de un dispositivo teléfono abierto.</span><span class="sxs-lookup"><span data-stu-id="6cea7-165">Queries the hookswitch mode of a hookswitch device of an open phone device.</span></span> <span data-ttu-id="6cea7-166">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-166">Synchronous.</span></span>          |
| [<span data-ttu-id="6cea7-167">**phoneSetVolume**</span><span class="sxs-lookup"><span data-stu-id="6cea7-167">**phoneSetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | <span data-ttu-id="6cea7-168">Establece el volumen del altavoz de un dispositivo conmutador de un dispositivo teléfono abierto.</span><span class="sxs-lookup"><span data-stu-id="6cea7-168">Sets the volume of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="6cea7-169">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="6cea7-169">Asynchronous.</span></span>           |
| [<span data-ttu-id="6cea7-170">**phoneGetVolume**</span><span class="sxs-lookup"><span data-stu-id="6cea7-170">**phoneGetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | <span data-ttu-id="6cea7-171">Devuelve la configuración del volumen del altavoz de un dispositivo conmutador de un dispositivo teléfono abierto.</span><span class="sxs-lookup"><span data-stu-id="6cea7-171">Returns the volume setting of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="6cea7-172">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-172">Synchronous.</span></span> |
| [<span data-ttu-id="6cea7-173">**phoneSetGain**</span><span class="sxs-lookup"><span data-stu-id="6cea7-173">**phoneSetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | <span data-ttu-id="6cea7-174">Establece la ganancia del MIC de un dispositivo conmutador de un dispositivo telefónico abierto.</span><span class="sxs-lookup"><span data-stu-id="6cea7-174">Sets the gain of a hookswitch device's mic of an open phone device.</span></span> <span data-ttu-id="6cea7-175">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="6cea7-175">Asynchronous.</span></span>                 |
| [<span data-ttu-id="6cea7-176">**phoneGetGain**</span><span class="sxs-lookup"><span data-stu-id="6cea7-176">**phoneGetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | <span data-ttu-id="6cea7-177">Devuelve el valor de ganancia del MIC de un dispositivo conmutador de un teléfono abierto.</span><span class="sxs-lookup"><span data-stu-id="6cea7-177">Returns the gain setting of a hookswitch device's mic of an open phone.</span></span> <span data-ttu-id="6cea7-178">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-178">Synchronous.</span></span>              |



 

## <a name="display"></a><span data-ttu-id="6cea7-179">Pantalla</span><span class="sxs-lookup"><span data-stu-id="6cea7-179">Display</span></span>



| <span data-ttu-id="6cea7-180">Función</span><span class="sxs-lookup"><span data-stu-id="6cea7-180">Function</span></span>                                   | <span data-ttu-id="6cea7-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cea7-181">Description</span></span>                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="6cea7-182">**phoneSetDisplay**</span><span class="sxs-lookup"><span data-stu-id="6cea7-182">**phoneSetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | <span data-ttu-id="6cea7-183">Escribe información en la pantalla de un dispositivo telefónico abierto.</span><span class="sxs-lookup"><span data-stu-id="6cea7-183">Writes information to the display of an open phone device.</span></span> <span data-ttu-id="6cea7-184">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="6cea7-184">Asynchronous.</span></span> |
| [<span data-ttu-id="6cea7-185">**phoneGetDisplay**</span><span class="sxs-lookup"><span data-stu-id="6cea7-185">**phoneGetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | <span data-ttu-id="6cea7-186">Devuelve el contenido actual de la pantalla de un teléfono.</span><span class="sxs-lookup"><span data-stu-id="6cea7-186">Returns the current contents of a phone's display.</span></span> <span data-ttu-id="6cea7-187">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-187">Synchronous.</span></span>          |



 

## <a name="ring"></a><span data-ttu-id="6cea7-188">En anillo</span><span class="sxs-lookup"><span data-stu-id="6cea7-188">Ring</span></span>



| <span data-ttu-id="6cea7-189">Función</span><span class="sxs-lookup"><span data-stu-id="6cea7-189">Function</span></span>                             | <span data-ttu-id="6cea7-190">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cea7-190">Description</span></span>                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="6cea7-191">**phoneSetRing**</span><span class="sxs-lookup"><span data-stu-id="6cea7-191">**phoneSetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | <span data-ttu-id="6cea7-192">Suena un dispositivo teléfono abierto según un modo de anillo determinado.</span><span class="sxs-lookup"><span data-stu-id="6cea7-192">Rings an open phone device according to a given ring mode.</span></span> <span data-ttu-id="6cea7-193">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="6cea7-193">Asynchronous.</span></span> |
| [<span data-ttu-id="6cea7-194">**phoneGetRing**</span><span class="sxs-lookup"><span data-stu-id="6cea7-194">**phoneGetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | <span data-ttu-id="6cea7-195">Devuelve el modo de anillo actual de un dispositivo telefónico abierto.</span><span class="sxs-lookup"><span data-stu-id="6cea7-195">Returns the current ring mode of an opened phone device.</span></span> <span data-ttu-id="6cea7-196">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-196">Synchronous.</span></span>    |



 

## <a name="buttons"></a><span data-ttu-id="6cea7-197">Botones</span><span class="sxs-lookup"><span data-stu-id="6cea7-197">Buttons</span></span>



| <span data-ttu-id="6cea7-198">Función</span><span class="sxs-lookup"><span data-stu-id="6cea7-198">Function</span></span>                                         | <span data-ttu-id="6cea7-199">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cea7-199">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="6cea7-200">**phoneSetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="6cea7-200">**phoneSetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | <span data-ttu-id="6cea7-201">Establece la información asociada a un botón en un dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="6cea7-201">Sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="6cea7-202">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="6cea7-202">Asynchronous.</span></span> |
| [<span data-ttu-id="6cea7-203">**phoneGetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="6cea7-203">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | <span data-ttu-id="6cea7-204">Devuelve información asociada a un botón en un dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="6cea7-204">Returns information associated with a button on a phone device.</span></span> <span data-ttu-id="6cea7-205">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-205">Synchronous.</span></span>   |



 

## <a name="lamps"></a><span data-ttu-id="6cea7-206">Lámparas</span><span class="sxs-lookup"><span data-stu-id="6cea7-206">Lamps</span></span>



| <span data-ttu-id="6cea7-207">Función</span><span class="sxs-lookup"><span data-stu-id="6cea7-207">Function</span></span>                             | <span data-ttu-id="6cea7-208">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cea7-208">Description</span></span>                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cea7-209">**phoneSetLamp**</span><span class="sxs-lookup"><span data-stu-id="6cea7-209">**phoneSetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | <span data-ttu-id="6cea7-210">Enciende una lámpara en un dispositivo telefónico abierto específico en un modo de iluminación de lámpara determinado.</span><span class="sxs-lookup"><span data-stu-id="6cea7-210">Lights a lamp on a specified open phone device in a given lamp lighting mode.</span></span> <span data-ttu-id="6cea7-211">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="6cea7-211">Asynchronous.</span></span> |
| [<span data-ttu-id="6cea7-212">**phoneGetLamp**</span><span class="sxs-lookup"><span data-stu-id="6cea7-212">**phoneGetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | <span data-ttu-id="6cea7-213">Devuelve el modo de lámpara actual de la lámpara especificada.</span><span class="sxs-lookup"><span data-stu-id="6cea7-213">Returns the current lamp mode of the specified lamp.</span></span> <span data-ttu-id="6cea7-214">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-214">Synchronous.</span></span>                           |



 

## <a name="data-areas"></a><span data-ttu-id="6cea7-215">Áreas de datos</span><span class="sxs-lookup"><span data-stu-id="6cea7-215">Data Areas</span></span>



| <span data-ttu-id="6cea7-216">Función</span><span class="sxs-lookup"><span data-stu-id="6cea7-216">Function</span></span>                             | <span data-ttu-id="6cea7-217">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cea7-217">Description</span></span>                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cea7-218">**phoneSetData**</span><span class="sxs-lookup"><span data-stu-id="6cea7-218">**phoneSetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | <span data-ttu-id="6cea7-219">Descarga un búfer de datos en un área de datos determinada del dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="6cea7-219">Downloads a buffer of data to a given data area in the phone device.</span></span> <span data-ttu-id="6cea7-220">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="6cea7-220">Asynchronous.</span></span>      |
| [<span data-ttu-id="6cea7-221">**phoneGetData**</span><span class="sxs-lookup"><span data-stu-id="6cea7-221">**phoneGetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | <span data-ttu-id="6cea7-222">Carga el contenido de un área de datos determinada en el dispositivo telefónico en un búfer.</span><span class="sxs-lookup"><span data-stu-id="6cea7-222">Uploads the contents of a given data area in the phone device to a buffer.</span></span> <span data-ttu-id="6cea7-223">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-223">Synchronous.</span></span> |



 

## <a name="status"></a><span data-ttu-id="6cea7-224">Status</span><span class="sxs-lookup"><span data-stu-id="6cea7-224">Status</span></span>



| <span data-ttu-id="6cea7-225">Función</span><span class="sxs-lookup"><span data-stu-id="6cea7-225">Function</span></span>                                                 | <span data-ttu-id="6cea7-226">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cea7-226">Description</span></span>                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cea7-227">**phoneSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="6cea7-227">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | <span data-ttu-id="6cea7-228">Especifica los cambios de estado para los que la aplicación desea recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="6cea7-228">Specifies the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="6cea7-229">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-229">Synchronous.</span></span> |
| [<span data-ttu-id="6cea7-230">**phoneGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="6cea7-230">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | <span data-ttu-id="6cea7-231">Devuelve los cambios de estado para los que la aplicación desea recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="6cea7-231">Returns the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="6cea7-232">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-232">Synchronous.</span></span>   |
| [<span data-ttu-id="6cea7-233">**phoneGetStatus**</span><span class="sxs-lookup"><span data-stu-id="6cea7-233">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | <span data-ttu-id="6cea7-234">Devuelve el estado completo de un dispositivo telefónico abierto.</span><span class="sxs-lookup"><span data-stu-id="6cea7-234">Returns the complete status of an open phone device.</span></span> <span data-ttu-id="6cea7-235">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="6cea7-235">Synchronous.</span></span>                         |



 

 

 



