---
title: Instrucciones generales de programación
description: Directrices para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465c658e64959eb1bfd61cf3c43f6ffd2cc6b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685742"
---
# <a name="general-programming-guidelines"></a><span data-ttu-id="2f38c-103">Instrucciones generales de programación</span><span class="sxs-lookup"><span data-stu-id="2f38c-103">General programming guidelines</span></span>

<span data-ttu-id="2f38c-104">En las secciones siguientes se proporcionan directrices generales para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2f38c-104">The following sections provide general guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2f38c-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2f38c-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2f38c-106">Capa de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="2f38c-106">Application compatibility layer</span></span>](application-compatibility-layer.md)
</dt> <dd>

<span data-ttu-id="2f38c-107">Para ejecutar aplicaciones heredadas en un entorno de Servicios de Escritorio remoto, puede usar el nivel de compatibilidad de aplicaciones de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2f38c-107">To run legacy applications in a Remote Desktop Services environment you can use the Remote Desktop Services Application Compatibility layer.</span></span>

</dd> <dt>

[<span data-ttu-id="2f38c-108">Instrucciones para aplicaciones cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="2f38c-108">Client/Server application guidelines</span></span>](client-server-application-guidelines.md)
</dt> <dd>

<span data-ttu-id="2f38c-109">Las aplicaciones cliente/servidor no deben suponer que una conexión de un solo equipo es equivalente a una sesión de un solo usuario.</span><span class="sxs-lookup"><span data-stu-id="2f38c-109">Client/server applications must not assume that a single computer connection is equivalent to a single user session.</span></span>

</dd> <dt>

[<span data-ttu-id="2f38c-110">Supervisión de conexiones y desconexiones de sesión</span><span class="sxs-lookup"><span data-stu-id="2f38c-110">Monitoring session connections and disconnections</span></span>](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

<span data-ttu-id="2f38c-111">Para registrar una aplicación con Servicios de Escritorio remoto, almacene el nombre de la aplicación de servidor de canal virtual en el registro mediante la adición de una subclave.</span><span class="sxs-lookup"><span data-stu-id="2f38c-111">To register an application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey.</span></span>

</dd> <dt>

[<span data-ttu-id="2f38c-112">Directrices de hardware de periféricos</span><span class="sxs-lookup"><span data-stu-id="2f38c-112">Peripheral hardware guidelines</span></span>](peripheral-hardware-guidelines.md)
</dt> <dd>

<span data-ttu-id="2f38c-113">Si su dispositivo de hardware no está diseñado para funcionar a través de una sesión remota, los proveedores deben asegurarse de que el software de controlador de dispositivo fuerce la deshabilitación de la redirección del dispositivo mediante una directiva del sistema o una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="2f38c-113">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

</dd> <dt>

[<span data-ttu-id="2f38c-114">Vinculación en tiempo de ejecución a Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="2f38c-114">Run-Time linking to Wtsapi32.dll</span></span>](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

<span data-ttu-id="2f38c-115">La aplicación puede usar la API de Servicios de Escritorio remoto para vincular dinámicamente al Wtsapi32.dll en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2f38c-115">Your application can use the Remote Desktop Services API to dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="2f38c-116">Para ello, la aplicación debe llamar a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="2f38c-116">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span>

</dd> </dl>

 

 