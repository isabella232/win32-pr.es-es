---
description: Aplicación WpdServicesApiSample
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Aplicación WpdServicesApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659887"
---
# <a name="wpdservicesapisample-application"></a><span data-ttu-id="dc27b-103">Aplicación WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="dc27b-103">WpdServicesApiSample Application</span></span>

<span data-ttu-id="dc27b-104">Un servicio de dispositivo es una extensión de un objeto funcional: además de la Agrupación lógica de las capacidades del dispositivo, un servicio de dispositivo proporciona a las aplicaciones la capacidad de detectar dichas capacidades mediante programación.</span><span class="sxs-lookup"><span data-stu-id="dc27b-104">A device service is an extension of a functional object: In addition to logically grouping device capabilities, a device service provides applications with the ability to programmatically discover those capabilities.</span></span>

<span data-ttu-id="dc27b-105">La aplicación de ejemplo WpdServicesApiSample es una aplicación de escritorio de línea de comandos que puede usar para explorar los servicios de contactos en los dispositivos conectados al equipo.</span><span class="sxs-lookup"><span data-stu-id="dc27b-105">The WpdServicesApiSample sample application is a command-line desktop application that you can use to explore Contacts services on devices attached to your computer.</span></span> <span data-ttu-id="dc27b-106">Puede explorar estos servicios mediante la lista de compatibles: formatos, eventos, métodos y servicios abstractos.</span><span class="sxs-lookup"><span data-stu-id="dc27b-106">You can explore these services by listing supported: formats, events, methods, and abstract services.</span></span> <span data-ttu-id="dc27b-107">También puede usar esta aplicación para recuperar las propiedades de un servicio de contacto determinado e invocar los métodos admitidos por ese servicio.</span><span class="sxs-lookup"><span data-stu-id="dc27b-107">You can also use this application retrieve the properties on a given Contact service and to invoke methods supported by that service.</span></span>

<span data-ttu-id="dc27b-108">Si aún no tiene un dispositivo que admita servicios de contactos, puede ejecutar WpdServicesApiSample si instala por primera vez el WpdServiceSampleDriver que se incluye en el kit de controladores de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc27b-108">If you don't yet have a device that supports Contacts services, you can still run the WpdServicesApiSample if you first install the WpdServiceSampleDriver that is included in the Windows Driver Kit.</span></span>

<span data-ttu-id="dc27b-109">La aplicación de ejemplo WpdServicesApiSample incluye los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="dc27b-109">The WpdServicesApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="dc27b-110">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="dc27b-110">**File**</span></span>                | <span data-ttu-id="dc27b-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dc27b-111">**Description**</span></span>                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc27b-112">ContentEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="dc27b-112">ContentEnumeration.cpp</span></span>  | <span data-ttu-id="dc27b-113">Contiene métodos que enumeran el contenido de un servicio de contactos determinado.</span><span class="sxs-lookup"><span data-stu-id="dc27b-113">Contains methods that enumerate the content on a given Contacts service.</span></span>                                                                                                                                  |
| <span data-ttu-id="dc27b-114">ContentProperties. cpp</span><span class="sxs-lookup"><span data-stu-id="dc27b-114">ContentProperties.cpp</span></span>   | <span data-ttu-id="dc27b-115">Contiene métodos que leen y escriben propiedades en un servicio de contactos determinado.</span><span class="sxs-lookup"><span data-stu-id="dc27b-115">Contains methods that read and write properties on a given Contacts service.</span></span>                                                                                                                              |
| <span data-ttu-id="dc27b-116">ServiceCapabilities. cpp</span><span class="sxs-lookup"><span data-stu-id="dc27b-116">ServiceCapabilities.cpp</span></span> | <span data-ttu-id="dc27b-117">Contiene los métodos que recuperan los formatos admitidos, los eventos y los servicios abstractos admitidos por un servicio de contactos determinado.</span><span class="sxs-lookup"><span data-stu-id="dc27b-117">Contains the methods that retrieve the supported formats, events, and abstract services that are supported by a given Contacts service.</span></span>                                                                   |
| <span data-ttu-id="dc27b-118">ServiceEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="dc27b-118">ServiceEnumeration.cpp</span></span>  | <span data-ttu-id="dc27b-119">Contiene las funciones auxiliares que recuperan información del dispositivo, como el nombre descriptivo del dispositivo o los servicios de contactos admitidos.</span><span class="sxs-lookup"><span data-stu-id="dc27b-119">Contains the helper functions that retrieve device information such as the device-friendly name or the supported Contacts services.</span></span>                                                                       |
| <span data-ttu-id="dc27b-120">ServiceMethods. cpp</span><span class="sxs-lookup"><span data-stu-id="dc27b-120">ServiceMethods.cpp</span></span>      | <span data-ttu-id="dc27b-121">Contiene los métodos que recuperan e invocan los métodos admitidos por un servicio de contactos determinado.</span><span class="sxs-lookup"><span data-stu-id="dc27b-121">Contains the methods that retrieve and invoke methods supported by a given Contacts service.</span></span>                                                                                                              |
| <span data-ttu-id="dc27b-122">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="dc27b-122">Stdafx.cpp</span></span>              | <span data-ttu-id="dc27b-123">Incluye los archivos estándar.</span><span class="sxs-lookup"><span data-stu-id="dc27b-123">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="dc27b-124">WpdServiceApiSample. cpp</span><span class="sxs-lookup"><span data-stu-id="dc27b-124">WpdServiceApiSample.cpp</span></span> | <span data-ttu-id="dc27b-125">Hospeda la función de inicio **\_ tmain** , que llama a la función local del **menú** , que muestra una lista de los dispositivos y las tareas disponibles y llama a la función adecuada para la selección del menú del usuario.</span><span class="sxs-lookup"><span data-stu-id="dc27b-125">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 


## <a name="related-topics"></a><span data-ttu-id="dc27b-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc27b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc27b-127">Muestras</span><span class="sxs-lookup"><span data-stu-id="dc27b-127">Samples</span></span>](sample.md)
</dt> </dl>

 

 



