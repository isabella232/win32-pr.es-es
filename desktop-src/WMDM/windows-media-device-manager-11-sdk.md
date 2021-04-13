---
title: SDK de Windows Media Administrador de dispositivos 11
description: SDK de Windows Media Administrador de dispositivos 11
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media Administrador de dispositivos, acerca de
- Administrador de dispositivos, acerca de
- Protocolo de transferencia multimedia (MTP)
- MTP (Protocolo de transferencia multimedia)
- Clase de almacenamiento masivo (MSC)
- MSC (clase de almacenamiento masivo)
- Windows Media Administrador de dispositivos, aplicaciones de escritorio
- Administrador de dispositivos, aplicaciones de escritorio
- aplicaciones de escritorio, acerca de
- Windows Media Administrador de dispositivos, proveedores de servicios
- Administrador de dispositivos, proveedores de servicios
- proveedores de servicios, acerca de
- Administrador de dispositivos de Windows Media, Complementos
- Administrador de dispositivos, INSP
- complementos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421544"
---
# <a name="windows-media-device-manager-11-sdk"></a><span data-ttu-id="34e92-118">SDK de Windows Media Administrador de dispositivos 11</span><span class="sxs-lookup"><span data-stu-id="34e92-118">Windows Media Device Manager 11 SDK</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34e92-119">Las API de Windows Media Administrador de dispositivos se incluyen ahora en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="34e92-119">The Windows Media Device Manager APIs are now included in the Windows SDK.</span></span> <span data-ttu-id="34e92-120">No es necesario descargar ningún SDK adicional.</span><span class="sxs-lookup"><span data-stu-id="34e92-120">No additional SDK downloads are required.</span></span>

 

<span data-ttu-id="34e92-121">El kit de desarrollo de software (SDK) de Microsoft Windows Media Administrador de dispositivos le permite crear aplicaciones de escritorio y componentes que pueden comunicarse con dispositivos portátiles conectados.</span><span class="sxs-lookup"><span data-stu-id="34e92-121">The Microsoft Windows Media Device Manager Software Development Kit (SDK) enables you to build desktop applications and components that can communicate with connected portable devices.</span></span> <span data-ttu-id="34e92-122">Windows Media Administrador de dispositivos permite que su aplicación o componente Enumere, explore y intercambie archivos con un dispositivo, consulte los metadatos y solicite información de recuento de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="34e92-122">Windows Media Device Manager enables your application or component to enumerate, explore, and exchange files with a device, query for metadata, and request play count information.</span></span> <span data-ttu-id="34e92-123">Las aplicaciones o componentes basados en Windows Media Administrador de dispositivos tienen una API coherente para comunicarse con una amplia gama de dispositivos, como el protocolo de transferencia multimedia (MTP), la clase de almacenamiento masivo (MSC), la RAPI y otros dispositivos creados en las versiones más recientes y anteriores de la tecnología de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="34e92-123">Applications or components built on Windows Media Device Manager have a consistent API for communicating with a wide range of devices including Media Transfer Protocol (MTP), Mass Storage Class (MSC), RAPI, and other devices built on both the latest and previous versions of Windows Media technology.</span></span>

<span data-ttu-id="34e92-124">Puede compilar los siguientes elementos mediante el SDK de Administrador de dispositivos de Windows Media:</span><span class="sxs-lookup"><span data-stu-id="34e92-124">You can build the following items using the Windows Media Device Manager SDK:</span></span>

-   <span data-ttu-id="34e92-125">Aplicaciones de escritorio, como reproductores multimedia personalizados.</span><span class="sxs-lookup"><span data-stu-id="34e92-125">Desktop applications, such as custom media players.</span></span> <span data-ttu-id="34e92-126">Toda la comunicación entre una aplicación y un dispositivo portátil debe pasar a través de Windows Media Administrador de dispositivos, que actúa como agente entre la aplicación, el sistema de administración de derechos digitales de Microsoft y el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="34e92-126">All communication between an application and a portable device must go through Windows Media Device Manager, which acts as a broker between the application, the Microsoft digital rights management system, and the service provider.</span></span>
-   <span data-ttu-id="34e92-127">Proveedores de servicios, que actúan como vínculo de comunicación entre un dispositivo personalizado y una aplicación de escritorio.</span><span class="sxs-lookup"><span data-stu-id="34e92-127">Service providers, which act as the communication link between a custom device and a desktop application.</span></span> <span data-ttu-id="34e92-128">Aunque Microsoft proporciona varios proveedores de servicios que pueden comunicarse con la mayoría de los dispositivos de la caja, puede crear un proveedor de servicios personalizado para personalizar la comunicación entre un dispositivo y una aplicación de escritorio.</span><span class="sxs-lookup"><span data-stu-id="34e92-128">Although Microsoft provides a number of service providers that can communicate with most devices out of the box, you can build a custom service provider to customize the communication between a device and a desktop application.</span></span>
-   <span data-ttu-id="34e92-129">Complementos, que pueden realizar tareas como la solicitud y el registro de recuentos de reproducción en dispositivos.</span><span class="sxs-lookup"><span data-stu-id="34e92-129">Plug-ins, which can perform tasks such as requesting and logging play counts on devices.</span></span> <span data-ttu-id="34e92-130">Estos complementos se pueden adjuntar a otras aplicaciones de escritorio, como Windows Media Player para enviar información a los proveedores de contenido con el fin de controlar los pagos de regalías a artistas.</span><span class="sxs-lookup"><span data-stu-id="34e92-130">These plug-ins can be attached to other desktop applications, such as the Windows Media Player to send information to content providers to handle royalty payments to artists.</span></span>

<span data-ttu-id="34e92-131">Para descargar el SDK de Windows Media Administrador de dispositivos, consulte [la página de descarga de Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) en el sitio web de MSDN.</span><span class="sxs-lookup"><span data-stu-id="34e92-131">To download the Windows Media Device Manager SDK, see [the Windows Media Download page](https://msdn.microsoft.com/windows/desktop/aa904949) on the MSDN Web site.</span></span>

<span data-ttu-id="34e92-132">Este SDK es un componente del kit de desarrollo de software de Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="34e92-132">This SDK is a component of the Microsoft Windows Media Software Development Kit.</span></span> <span data-ttu-id="34e92-133">Otros componentes son el SDK de Windows Media Format, el SDK de Windows Media Services, el SDK de Windows Media Encoder, el SDK de Windows Media Rights Manager y el SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="34e92-133">Other components include the Windows Media Format SDK, the Windows Media Services SDK, the Windows Media Encoder SDK, the Windows Media Rights Manager SDK, and the Windows Media Player SDK.</span></span>

<span data-ttu-id="34e92-134">En esta documentación se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="34e92-134">This documentation includes the following sections.</span></span>



| <span data-ttu-id="34e92-135">Sección</span><span class="sxs-lookup"><span data-stu-id="34e92-135">Section</span></span>                                            | <span data-ttu-id="34e92-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="34e92-136">Description</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34e92-137">Introducción</span><span class="sxs-lookup"><span data-stu-id="34e92-137">Getting Started</span></span>](getting-started.md)             | <span data-ttu-id="34e92-138">Se describen las novedades de esta versión de Windows Media Administrador de dispositivos, se ofrece información general sobre cómo funciona Windows Media Administrador de dispositivos, se describe lo que se necesita para desarrollar una aplicación o un proveedor de servicios, y se explican los ejemplos que se incluyen con el SDK.</span><span class="sxs-lookup"><span data-stu-id="34e92-138">Describes what is new in this version of Windows Media Device Manager, gives an overview of how Windows Media Device Manager works, describes what will be needed to develop an application or service provider, and explains the samples shipped with the SDK.</span></span> |
| [<span data-ttu-id="34e92-139">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="34e92-139">Programming Guide</span></span>](programming-guide.md)         | <span data-ttu-id="34e92-140">Describe cómo crear aplicaciones y proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="34e92-140">Discusses how to build applications and service providers.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="34e92-141">Referencia de programación</span><span class="sxs-lookup"><span data-stu-id="34e92-141">Programming Reference</span></span>](programming-reference.md) | <span data-ttu-id="34e92-142">Proporciona información de referencia de C++ para las interfaces, los métodos, las clases y las estructuras compatibles con el SDK de Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="34e92-142">Provides C++ reference information for the interfaces, methods, classes, and structures supported by the Windows Media Device Manager SDK.</span></span>                                                                                                                      |
| [<span data-ttu-id="34e92-143">*Glosario*</span><span class="sxs-lookup"><span data-stu-id="34e92-143">*Glossary*</span></span>](wmdm-glossary.md)                    | <span data-ttu-id="34e92-144">Define los términos que se usan en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="34e92-144">Defines terms used in this documentation.</span></span>                                                                                                                                                                                                                       |



 

 

 




