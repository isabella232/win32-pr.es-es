---
description: Windows Sockets Transport y namespace&\# 8211; los proveedores de servicios son dll con un único punto de entrada de procedimiento exportado para la función de inicialización de proveedor de servicios WSPStartup o NSPStartup, respectivamente.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Modelo de interfaz de función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705618"
---
# <a name="function-interface-model"></a><span data-ttu-id="6dd7c-103">Modelo de interfaz de función</span><span class="sxs-lookup"><span data-stu-id="6dd7c-103">Function Interface Model</span></span>

<span data-ttu-id="6dd7c-104">Espacio de nombres y transporte de Windows Sockets: los proveedores de servicios son archivos DLL con un único punto de entrada de procedimiento exportado para la función de inicialización de proveedor de servicio [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) o [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-104">Windows Sockets transport and namespace–service providers are DLLs with a single exported procedure entry point for the service provider initialization function [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) or [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup), respectively.</span></span> <span data-ttu-id="6dd7c-105">Todas las demás funciones del proveedor de servicios son accesibles para el \_32.dll Ws2 a través de la tabla de envío del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-105">All other service provider functions are made accessible to the Ws2\_32.dll through the service provider's dispatch table.</span></span> <span data-ttu-id="6dd7c-106">Los archivos DLL del proveedor de servicios se cargan en la memoria mediante el \_32.dll Ws2 solo cuando sea necesario y se descargan cuando sus servicios ya no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-106">Service provider DLL's are loaded into memory by the Ws2\_32.dll only when needed, and are unloaded when their services are no longer required.</span></span>

<span data-ttu-id="6dd7c-107">El SPI también define varias circunstancias en las que un proveedor de servicios de transporte llama a Ws2 \_32.dll (llamadas) para obtener los servicios de soporte de dll.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-107">The SPI also defines several circumstances in which a transport service provider calls up into the Ws2\_32.dll (upcalls) to obtain DLL support services.</span></span> <span data-ttu-id="6dd7c-108">La DLL del proveedor de servicios de transporte recibe la \_ tabla de envío de llamadas de Ws232.dll a través del parámetro *UpcallTable* a [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span><span class="sxs-lookup"><span data-stu-id="6dd7c-108">The transport service provider DLL is given the Ws2\_32.dll's upcall dispatch table through the *UpcallTable* parameter to [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span>

<span data-ttu-id="6dd7c-109">Los proveedores de servicios deben cambiar su extensión de nombre de archivo de "DLL" a ". WSP "o". NSP ".</span><span class="sxs-lookup"><span data-stu-id="6dd7c-109">Service providers should have their file name extension changed from "DLL" to ".WSP" or ".NSP".</span></span> <span data-ttu-id="6dd7c-110">Este requisito no es estricto.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-110">This requirement is not strict.</span></span> <span data-ttu-id="6dd7c-111">Un proveedor de servicios seguirá funcionando con el \_32.dll Ws2 con cualquier extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-111">A service provider will still operate with the Ws2\_32.dll with any file name extension.</span></span>

<span data-ttu-id="6dd7c-112">El SPI de Winsock usa la siguiente Convención de nomenclatura de prefijos de función:</span><span class="sxs-lookup"><span data-stu-id="6dd7c-112">The Winsock SPI uses the following function prefix naming convention:</span></span>

| <span data-ttu-id="6dd7c-113">Prefijo</span><span class="sxs-lookup"><span data-stu-id="6dd7c-113">Prefix</span></span> | <span data-ttu-id="6dd7c-114">Significado</span><span class="sxs-lookup"><span data-stu-id="6dd7c-114">Meaning</span></span>                          | <span data-ttu-id="6dd7c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6dd7c-115">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="6dd7c-116">WSP</span><span class="sxs-lookup"><span data-stu-id="6dd7c-116">WSP</span></span>    | <span data-ttu-id="6dd7c-117">Proveedor de servicios de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6dd7c-117">Windows Sockets Service Provider</span></span> | <span data-ttu-id="6dd7c-118">Puntos de entrada del proveedor de servicios de transporte</span><span class="sxs-lookup"><span data-stu-id="6dd7c-118">Transport service provider entry points</span></span>           |
| <span data-ttu-id="6dd7c-119">WPU</span><span class="sxs-lookup"><span data-stu-id="6dd7c-119">WPU</span></span>    | <span data-ttu-id="6dd7c-120">Llamada al proveedor de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6dd7c-120">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="6dd7c-121">Ws2 \_32.dll puntos de entrada para proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="6dd7c-121">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="6dd7c-122">WSC</span><span class="sxs-lookup"><span data-stu-id="6dd7c-122">WSC</span></span>    | <span data-ttu-id="6dd7c-123">Configuración de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6dd7c-123">Windows Sockets Configuration</span></span>    | <span data-ttu-id="6dd7c-124">WS2 \_32.dll puntos de entrada para applets de instalación</span><span class="sxs-lookup"><span data-stu-id="6dd7c-124">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="6dd7c-125">NSP</span><span class="sxs-lookup"><span data-stu-id="6dd7c-125">NSP</span></span>    | <span data-ttu-id="6dd7c-126">Proveedor de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="6dd7c-126">Namespace Provider</span></span>               | <span data-ttu-id="6dd7c-127">Puntos de entrada del proveedor de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="6dd7c-127">Namespace provider entry points</span></span>                   |



 

<span data-ttu-id="6dd7c-128">Tal y como se ha descrito anteriormente, estos puntos de entrada no se exportan (con la excepción de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) y [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), pero se obtiene acceso a ellos a través de un intercambio de tablas de distribución.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-128">As described above, these entry points are not exported (with the exception of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) and [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), but are accessed through an exchange of dispatch tables.</span></span>

 

 



