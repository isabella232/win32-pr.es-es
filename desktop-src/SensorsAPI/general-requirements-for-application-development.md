---
description: En este tema se describe lo que debe hacer para empezar a crear programas que usan la API de sensor.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Requisitos generales para el desarrollo de aplicaciones (API de sensor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361128"
---
# <a name="general-requirements-for-application-development-sensor-api"></a><span data-ttu-id="39195-103">Requisitos generales para el desarrollo de aplicaciones (API de sensor)</span><span class="sxs-lookup"><span data-stu-id="39195-103">General Requirements for Application Development (Sensor API)</span></span>

<span data-ttu-id="39195-104">En este tema se describe lo que debe hacer para empezar a crear programas que usan la API de sensor.</span><span class="sxs-lookup"><span data-stu-id="39195-104">This topic describes what you must do to start to create programs that use the Sensor API.</span></span>

<span data-ttu-id="39195-105">Para crear una aplicación de API de sensor, debe instalar Windows 7 y el kit de desarrollo de software (SDK) de Windows 7 en el equipo.</span><span class="sxs-lookup"><span data-stu-id="39195-105">To create a Sensor API application, you must install Windows 7 and the Windows 7 Software Development Kit (SDK) on your computer.</span></span> <span data-ttu-id="39195-106">En la tabla siguiente se describen los archivos específicos que necesitará.</span><span class="sxs-lookup"><span data-stu-id="39195-106">The following table describes the specific files that you will need.</span></span>



| <span data-ttu-id="39195-107">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="39195-107">File name</span></span>               | <span data-ttu-id="39195-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="39195-108">Description</span></span>                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39195-109">Sensorsapi. h</span><span class="sxs-lookup"><span data-stu-id="39195-109">Sensorsapi.h</span></span>            | <span data-ttu-id="39195-110">El archivo de encabezado principal de la API del sensor.</span><span class="sxs-lookup"><span data-stu-id="39195-110">The main header file for the Sensor API.</span></span> <span data-ttu-id="39195-111">Este archivo de encabezado contiene las definiciones de interfaz.</span><span class="sxs-lookup"><span data-stu-id="39195-111">This header file contains the interface definitions.</span></span>               |
| <span data-ttu-id="39195-112">Sensors. h</span><span class="sxs-lookup"><span data-stu-id="39195-112">Sensors.h</span></span>               | <span data-ttu-id="39195-113">El archivo de encabezado que contiene las definiciones de las constantes definidas por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="39195-113">The header file that contains definitions of platform-defined constants.</span></span>                                    |
| <span data-ttu-id="39195-114">Initguid. h</span><span class="sxs-lookup"><span data-stu-id="39195-114">Initguid.h</span></span>              | <span data-ttu-id="39195-115">El archivo de encabezado que contiene definiciones para controlar la inicialización de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="39195-115">The header file that contains definitions for controlling **GUID** initialization.</span></span>                          |
| <span data-ttu-id="39195-116">FunctionDiscoveryKeys. h</span><span class="sxs-lookup"><span data-stu-id="39195-116">FunctionDiscoveryKeys.h</span></span> | <span data-ttu-id="39195-117">El archivo de encabezado que define las claves de propiedad de identificador de dispositivo que son necesarias cuando se conecta a sensores lógicos.</span><span class="sxs-lookup"><span data-stu-id="39195-117">The header file that defines device ID property keys that are required when you connect to logical sensors.</span></span> |
| <span data-ttu-id="39195-118">Sensorsapi. lib</span><span class="sxs-lookup"><span data-stu-id="39195-118">Sensorsapi.lib</span></span>          | <span data-ttu-id="39195-119">Biblioteca estática que contiene definiciones **GUID** para la API del sensor.</span><span class="sxs-lookup"><span data-stu-id="39195-119">A static library that contains **GUID** definitions for the Sensor API.</span></span>                                     |
| <span data-ttu-id="39195-120">PortableDeviceGuids. lib</span><span class="sxs-lookup"><span data-stu-id="39195-120">PortableDeviceGuids.lib</span></span> | <span data-ttu-id="39195-121">Biblioteca estática que contiene definiciones **GUID** para objetos de dispositivos portátiles de Windows.</span><span class="sxs-lookup"><span data-stu-id="39195-121">A static library that contains **GUID** definitions for Windows Portable Devices objects.</span></span>                   |



 

<span data-ttu-id="39195-122">El programa puede requerir archivos adicionales.</span><span class="sxs-lookup"><span data-stu-id="39195-122">Your program may require additional files.</span></span>

## <a name="supported-operating-systems"></a><span data-ttu-id="39195-123">Sistemas operativos compatibles</span><span class="sxs-lookup"><span data-stu-id="39195-123">Supported Operating Systems</span></span>

<span data-ttu-id="39195-124">Las aplicaciones de API de sensor se ejecutarán en todas las ediciones de Windows 7, excepto para Windows 7 Starter Edition.</span><span class="sxs-lookup"><span data-stu-id="39195-124">Sensor API applications will run on all editions of Windows 7, except for Windows 7 Starter edition.</span></span>

## <a name="windows-portable-devices-interfaces"></a><span data-ttu-id="39195-125">Interfaces de dispositivos portátiles de Windows</span><span class="sxs-lookup"><span data-stu-id="39195-125">Windows Portable Devices Interfaces</span></span>

<span data-ttu-id="39195-126">La API de sensor usa ciertos objetos de dispositivos portátiles de Windows (WPD) para encapsular valores y claves de propiedad.</span><span class="sxs-lookup"><span data-stu-id="39195-126">The Sensor API uses certain Windows Portable Devices (WPD) objects to encapsulate property keys and values.</span></span> <span data-ttu-id="39195-127">En la tabla siguiente se describen las interfaces de estos objetos.</span><span class="sxs-lookup"><span data-stu-id="39195-127">The following table describes the interfaces for these objects.</span></span>



| <span data-ttu-id="39195-128">Interfaz</span><span class="sxs-lookup"><span data-stu-id="39195-128">Interface</span></span>                                                                       | <span data-ttu-id="39195-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="39195-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39195-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39195-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span></span>        | <span data-ttu-id="39195-131">Esta interfaz proporciona una forma cómoda de crear un contenedor de propiedades de pares nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="39195-131">This interface provides a convenient way to create a property bag of name/value pairs.</span></span> <span data-ttu-id="39195-132">Los nombres se representan mediante **PROPERTYKEY** s y los valores se representan mediante **PROPVARIANT** s.</span><span class="sxs-lookup"><span data-stu-id="39195-132">Names are represented by **PROPERTYKEY** s and values are represented by **PROPVARIANT** s.</span></span> <br/> <span data-ttu-id="39195-133">La API usa esta interfaz para establecer y recuperar valores únicos y conjuntos de valores.</span><span class="sxs-lookup"><span data-stu-id="39195-133">The API uses this interface for setting and retrieving both single values and sets of values.</span></span> <span data-ttu-id="39195-134">Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamando a **CoCreateInstance** con CLSID \_ PortableDeviceValues.</span><span class="sxs-lookup"><span data-stu-id="39195-134">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceValues.</span></span><br/> |
| <span data-ttu-id="39195-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39195-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span></span> | <span data-ttu-id="39195-136">Esta interfaz contiene una colección de **PROPERTYKEY** s.</span><span class="sxs-lookup"><span data-stu-id="39195-136">This interface contains a collection of **PROPERTYKEY** s.</span></span> <span data-ttu-id="39195-137">Estas claves representan nombres de propiedad que pueden almacenarse mediante **IPortableDeviceValues**.</span><span class="sxs-lookup"><span data-stu-id="39195-137">These keys represent property names that can be stored by **IPortableDeviceValues**.</span></span> <span data-ttu-id="39195-138">La API usa este objeto de colección para establecer y recuperar los nombres de propiedad única y los conjuntos de nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="39195-138">The API uses this collection object for setting and retrieving both single property names and sets of property names.</span></span><br/> <span data-ttu-id="39195-139">Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamando a **CoCreateInstance** con CLSID \_ PortableDeviceKeyCollection.</span><span class="sxs-lookup"><span data-stu-id="39195-139">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceKeyCollection.</span></span> <br/>    |



 

 

