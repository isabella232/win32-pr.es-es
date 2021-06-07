---
description: Todos los proveedores de servicios deben implementar funciones de telefonía básica.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Funciones básicas de telefonía de TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5308def0c94df9fa59f2022bf25c4dbb1843e2f8
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524159"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="99fe2-103">Funciones básicas de telefonía de TSPI</span><span class="sxs-lookup"><span data-stu-id="99fe2-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="99fe2-104">Todos los proveedores de servicios deben implementar funciones de telefonía básica.</span><span class="sxs-lookup"><span data-stu-id="99fe2-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="99fe2-105">A continuación se muestra una lista de estas funciones por categoría.</span><span class="sxs-lookup"><span data-stu-id="99fe2-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="99fe2-106">Una función se identifica como *asincrónica* si indica la finalización en un mensaje REPLY a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="99fe2-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="99fe2-107">Si la función siempre devuelve su resultado inmediatamente, la función se considera *sincrónica.*</span><span class="sxs-lookup"><span data-stu-id="99fe2-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="99fe2-108">Direcciones</span><span class="sxs-lookup"><span data-stu-id="99fe2-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="99fe2-109">Respuesta a llamadas entrantes</span><span class="sxs-lookup"><span data-stu-id="99fe2-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="99fe2-110">Llamar a funciones de colocación</span><span class="sxs-lookup"><span data-stu-id="99fe2-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="99fe2-111">Llamar a estados y eventos</span><span class="sxs-lookup"><span data-stu-id="99fe2-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="99fe2-112">Estado y funcionalidades de la línea</span><span class="sxs-lookup"><span data-stu-id="99fe2-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="99fe2-113">Negociación de versiones de línea</span><span class="sxs-lookup"><span data-stu-id="99fe2-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="99fe2-114">Realizar llamadas</span><span class="sxs-lookup"><span data-stu-id="99fe2-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="99fe2-115">Apertura y cierre de dispositivos de línea</span><span class="sxs-lookup"><span data-stu-id="99fe2-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="99fe2-116">Negociación de versiones de teléfono</span><span class="sxs-lookup"><span data-stu-id="99fe2-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="99fe2-117">Inicialización y apagado de TSP</span><span class="sxs-lookup"><span data-stu-id="99fe2-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="99fe2-118">Inicialización y apagado de TSP</span><span class="sxs-lookup"><span data-stu-id="99fe2-118">TSP Initialization and Shutdown</span></span>



|  <span data-ttu-id="99fe2-119">Función</span><span class="sxs-lookup"><span data-stu-id="99fe2-119">Function</span></span>                                                         |   <span data-ttu-id="99fe2-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="99fe2-120">Description</span></span>                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="99fe2-121">**Proveedor de \_ TUISPIInstalar**</span><span class="sxs-lookup"><span data-stu-id="99fe2-121">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="99fe2-122">Instala un TSP.</span><span class="sxs-lookup"><span data-stu-id="99fe2-122">Installs a TSP.</span></span> <span data-ttu-id="99fe2-123">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-123">Synchronous.</span></span>                              |
| [<span data-ttu-id="99fe2-124">**Proveedor \_ TSPIInstalar**</span><span class="sxs-lookup"><span data-stu-id="99fe2-124">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="99fe2-125">Instala el TSP.</span><span class="sxs-lookup"><span data-stu-id="99fe2-125">Installs the TSP.</span></span> <span data-ttu-id="99fe2-126">Obsoleto con la versión 2.0.</span><span class="sxs-lookup"><span data-stu-id="99fe2-126">Obsolete with Version 2.0.</span></span> <span data-ttu-id="99fe2-127">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-127">Synchronous.</span></span> |
| [<span data-ttu-id="99fe2-128">**Proveedor \_ TSPIInit**</span><span class="sxs-lookup"><span data-stu-id="99fe2-128">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="99fe2-129">Inicializa el TSP.</span><span class="sxs-lookup"><span data-stu-id="99fe2-129">Initializes the TSP.</span></span> <span data-ttu-id="99fe2-130">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-130">Synchronous.</span></span>                         |
| [<span data-ttu-id="99fe2-131">**Proveedor de \_ TSPIShutdown**</span><span class="sxs-lookup"><span data-stu-id="99fe2-131">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="99fe2-132">Cierra el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="99fe2-132">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="99fe2-133">**Proveedor de \_ TUISPIRemove**</span><span class="sxs-lookup"><span data-stu-id="99fe2-133">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="99fe2-134">Quita un TSP.</span><span class="sxs-lookup"><span data-stu-id="99fe2-134">Removes a TSP.</span></span> <span data-ttu-id="99fe2-135">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-135">Synchronous.</span></span>                               |
| [<span data-ttu-id="99fe2-136">**Proveedor \_ TSPIRemove**</span><span class="sxs-lookup"><span data-stu-id="99fe2-136">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="99fe2-137">Quita un TSP.</span><span class="sxs-lookup"><span data-stu-id="99fe2-137">Removes a TSP.</span></span> <span data-ttu-id="99fe2-138">Obsoleto con la versión 2.0.</span><span class="sxs-lookup"><span data-stu-id="99fe2-138">Obsolete with Version 2.0.</span></span> <span data-ttu-id="99fe2-139">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-139">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="99fe2-140">Negociación de versiones de teléfono</span><span class="sxs-lookup"><span data-stu-id="99fe2-140">Phone Version Negotiation</span></span>



|  <span data-ttu-id="99fe2-141">Función</span><span class="sxs-lookup"><span data-stu-id="99fe2-141">Function</span></span>                                                         |   <span data-ttu-id="99fe2-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="99fe2-142">Description</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="99fe2-143">**TSPI \_ phoneNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="99fe2-143">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="99fe2-144">Devuelve la versión spi más alta con la que el proveedor de servicios puede funcionar para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99fe2-144">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="99fe2-145">Negociación de versiones de línea</span><span class="sxs-lookup"><span data-stu-id="99fe2-145">Line Version Negotiation</span></span>



|  <span data-ttu-id="99fe2-146">Función</span><span class="sxs-lookup"><span data-stu-id="99fe2-146">Function</span></span>                                                         |   <span data-ttu-id="99fe2-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="99fe2-147">Description</span></span>                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99fe2-148">**TSPI \_ lineNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="99fe2-148">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="99fe2-149">Permite que una aplicación negocie una versión de TSPI para usarla con un dispositivo de línea determinado.</span><span class="sxs-lookup"><span data-stu-id="99fe2-149">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="99fe2-150">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-150">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="99fe2-151">Estado y funcionalidades de la línea</span><span class="sxs-lookup"><span data-stu-id="99fe2-151">Line Status and Capabilities</span></span>



|  <span data-ttu-id="99fe2-152">Función</span><span class="sxs-lookup"><span data-stu-id="99fe2-152">Function</span></span>                                                         |   <span data-ttu-id="99fe2-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="99fe2-153">Description</span></span>                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99fe2-154">**TSPI \_ lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="99fe2-154">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="99fe2-155">Devuelve las funcionalidades de un dispositivo de línea determinado.</span><span class="sxs-lookup"><span data-stu-id="99fe2-155">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="99fe2-156">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-156">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="99fe2-157">**TSPI \_ lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="99fe2-157">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="99fe2-158">Devuelve la configuración de un dispositivo de flujo multimedia.</span><span class="sxs-lookup"><span data-stu-id="99fe2-158">Returns configuration of a media stream device.</span></span> <span data-ttu-id="99fe2-159">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-159">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="99fe2-160">**TSPI \_ lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="99fe2-160">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="99fe2-161">Devuelve el estado actual del dispositivo de línea abierta especificado.</span><span class="sxs-lookup"><span data-stu-id="99fe2-161">Returns current status of the specified open line device.</span></span> <span data-ttu-id="99fe2-162">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-162">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="99fe2-163">**LineSetDevConfig de TSPI \_**</span><span class="sxs-lookup"><span data-stu-id="99fe2-163">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="99fe2-164">Establece la configuración del dispositivo de flujo multimedia especificado.</span><span class="sxs-lookup"><span data-stu-id="99fe2-164">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="99fe2-165">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-165">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="99fe2-166">**\_LineSetStatusMessages de TSPI**</span><span class="sxs-lookup"><span data-stu-id="99fe2-166">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="99fe2-167">Especifica los cambios de estado para los que se debe notificar a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="99fe2-167">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="99fe2-168">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-168">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="99fe2-169">**LineGetID de TSPI \_**</span><span class="sxs-lookup"><span data-stu-id="99fe2-169">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="99fe2-170">Recupera un identificador de dispositivo asociado a la línea abierta, la dirección o la llamada especificadas.</span><span class="sxs-lookup"><span data-stu-id="99fe2-170">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="99fe2-171">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-171">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="99fe2-172">**LineGetIcon de TSPI \_**</span><span class="sxs-lookup"><span data-stu-id="99fe2-172">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="99fe2-173">Permite que una aplicación recupere un icono para mostrarlo al usuario.</span><span class="sxs-lookup"><span data-stu-id="99fe2-173">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="99fe2-174">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-174">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="99fe2-175">**TUISPI \_ lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="99fe2-175">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="99fe2-176">Hace que el proveedor del dispositivo de línea especificado muestre un cuadro de diálogo que permite al usuario configurar parámetros relacionados con el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="99fe2-176">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="99fe2-177">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-177">Synchronous.</span></span> |
| [<span data-ttu-id="99fe2-178">**LÍNEA DE \_ TUISPIConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="99fe2-178">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="99fe2-179">Muestra un cuadro de diálogo que permite al usuario cambiar la información de configuración de un dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="99fe2-179">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="99fe2-180">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-180">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="99fe2-181">Direcciones</span><span class="sxs-lookup"><span data-stu-id="99fe2-181">Addresses</span></span>



|  <span data-ttu-id="99fe2-182">Función</span><span class="sxs-lookup"><span data-stu-id="99fe2-182">Function</span></span>                                                         |   <span data-ttu-id="99fe2-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="99fe2-183">Description</span></span>                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99fe2-184">**TSPI \_ lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="99fe2-184">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="99fe2-185">Devuelve las funcionalidades de telefonía de una dirección.</span><span class="sxs-lookup"><span data-stu-id="99fe2-185">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="99fe2-186">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-186">Synchronous.</span></span>                           |
| [<span data-ttu-id="99fe2-187">**TSPI \_ lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="99fe2-187">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="99fe2-188">Devuelve el estado actual de una dirección especificada.</span><span class="sxs-lookup"><span data-stu-id="99fe2-188">Returns current status of a specified address.</span></span> <span data-ttu-id="99fe2-189">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-189">Synchronous.</span></span>                              |
| [<span data-ttu-id="99fe2-190">**\_LineGetNumAddressIDs de TSPI**</span><span class="sxs-lookup"><span data-stu-id="99fe2-190">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="99fe2-191">Recupera el número de identificadores de dirección admitidos en la línea indicada.</span><span class="sxs-lookup"><span data-stu-id="99fe2-191">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="99fe2-192">**TSPI \_ lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="99fe2-192">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="99fe2-193">Recupera el identificador de dirección de una dirección especificada mediante un formato alternativo.</span><span class="sxs-lookup"><span data-stu-id="99fe2-193">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="99fe2-194">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-194">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="99fe2-195">Apertura y cierre de dispositivos de línea</span><span class="sxs-lookup"><span data-stu-id="99fe2-195">Opening and Closing Line Devices</span></span>



|  <span data-ttu-id="99fe2-196">Función</span><span class="sxs-lookup"><span data-stu-id="99fe2-196">Function</span></span>                                                         |   <span data-ttu-id="99fe2-197">Descripción</span><span class="sxs-lookup"><span data-stu-id="99fe2-197">Description</span></span>                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99fe2-198">**Línea \_ TSPIAbrir**</span><span class="sxs-lookup"><span data-stu-id="99fe2-198">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="99fe2-199">Abre un dispositivo de línea especificado para proporcionar la supervisión posterior o el control de la línea.</span><span class="sxs-lookup"><span data-stu-id="99fe2-199">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="99fe2-200">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-200">Synchronous.</span></span> |
| [<span data-ttu-id="99fe2-201">**TSPI \_ lineClose**</span><span class="sxs-lookup"><span data-stu-id="99fe2-201">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="99fe2-202">Cierra un dispositivo de línea abierto especificado.</span><span class="sxs-lookup"><span data-stu-id="99fe2-202">Closes a specified opened line device.</span></span> <span data-ttu-id="99fe2-203">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-203">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="99fe2-204">Llamar a estados y eventos</span><span class="sxs-lookup"><span data-stu-id="99fe2-204">Call States and Events</span></span>



|  <span data-ttu-id="99fe2-205">Función</span><span class="sxs-lookup"><span data-stu-id="99fe2-205">Function</span></span>                                                         |   <span data-ttu-id="99fe2-206">Descripción</span><span class="sxs-lookup"><span data-stu-id="99fe2-206">Description</span></span>                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="99fe2-207">**Línea \_ TSPIGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="99fe2-207">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="99fe2-208">Devuelve información fija sobre una llamada.</span><span class="sxs-lookup"><span data-stu-id="99fe2-208">Returns fixed information about a call.</span></span> <span data-ttu-id="99fe2-209">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-209">Synchronous.</span></span>                                |
| [<span data-ttu-id="99fe2-210">**TSPI \_ lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="99fe2-210">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="99fe2-211">Devuelve información de estado de llamada completa para la llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="99fe2-211">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="99fe2-212">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-212">Synchronous.</span></span>       |
| [<span data-ttu-id="99fe2-213">**LineSetAppSpecific de TSPI \_**</span><span class="sxs-lookup"><span data-stu-id="99fe2-213">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="99fe2-214">Establece el campo específico de la aplicación de la estructura de información de una llamada.</span><span class="sxs-lookup"><span data-stu-id="99fe2-214">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="99fe2-215">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="99fe2-215">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="99fe2-216">Realizar llamadas</span><span class="sxs-lookup"><span data-stu-id="99fe2-216">Making Calls</span></span>



|  <span data-ttu-id="99fe2-217">Función</span><span class="sxs-lookup"><span data-stu-id="99fe2-217">Function</span></span>                                                         |   <span data-ttu-id="99fe2-218">Descripción</span><span class="sxs-lookup"><span data-stu-id="99fe2-218">Description</span></span>                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="99fe2-219">**Línea \_ TSPIMakeCall**</span><span class="sxs-lookup"><span data-stu-id="99fe2-219">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="99fe2-220">Realiza una llamada saliente y devuelve un identificador de llamada para ella.</span><span class="sxs-lookup"><span data-stu-id="99fe2-220">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="99fe2-221">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="99fe2-221">Asynchronous.</span></span> |
| [<span data-ttu-id="99fe2-222">**LineDial de TSPI \_**</span><span class="sxs-lookup"><span data-stu-id="99fe2-222">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="99fe2-223">Marcas (partes de una o varias) direcciones que se pueden marcar.</span><span class="sxs-lookup"><span data-stu-id="99fe2-223">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="99fe2-224">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="99fe2-224">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="99fe2-225">Respuesta a llamadas entrantes</span><span class="sxs-lookup"><span data-stu-id="99fe2-225">Answering Incoming Calls</span></span>



|  <span data-ttu-id="99fe2-226">Función</span><span class="sxs-lookup"><span data-stu-id="99fe2-226">Function</span></span>                                                         |   <span data-ttu-id="99fe2-227">Descripción</span><span class="sxs-lookup"><span data-stu-id="99fe2-227">Description</span></span>                                                        |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="99fe2-228">**Línea de \_ TSPIAnswer**</span><span class="sxs-lookup"><span data-stu-id="99fe2-228">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="99fe2-229">Responde a una llamada entrante.</span><span class="sxs-lookup"><span data-stu-id="99fe2-229">Answers an incoming call.</span></span> <span data-ttu-id="99fe2-230">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="99fe2-230">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="99fe2-231">Llamar a funciones drop</span><span class="sxs-lookup"><span data-stu-id="99fe2-231">Call Drop Functions</span></span>



|  <span data-ttu-id="99fe2-232">Función</span><span class="sxs-lookup"><span data-stu-id="99fe2-232">Function</span></span>                                                         |   <span data-ttu-id="99fe2-233">Descripción</span><span class="sxs-lookup"><span data-stu-id="99fe2-233">Description</span></span>                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="99fe2-234">**TSPI \_ lineDrop**</span><span class="sxs-lookup"><span data-stu-id="99fe2-234">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="99fe2-235">Desconecta una llamada o abandona un intento de llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="99fe2-235">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="99fe2-236">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="99fe2-236">Asynchronous.</span></span> |



 

 

 
