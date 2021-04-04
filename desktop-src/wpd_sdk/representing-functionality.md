---
description: Representar la funcionalidad
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Representar la funcionalidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911122"
---
# <a name="representing-functionality"></a><span data-ttu-id="15b83-103">Representar la funcionalidad</span><span class="sxs-lookup"><span data-stu-id="15b83-103">Representing Functionality</span></span>

<span data-ttu-id="15b83-104">Existen objetos funcionales para identificar o agrupar lógicamente las capacidades de características de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15b83-104">Functional objects exist to identify or logically group feature capabilities of a device.</span></span> <span data-ttu-id="15b83-105">Por ejemplo, una aplicación puede ver que un dispositivo admite SMS buscando el objeto funcional de SMS.</span><span class="sxs-lookup"><span data-stu-id="15b83-105">For example, an application can see that a device supports SMS by looking for the SMS functional object.</span></span> <span data-ttu-id="15b83-106">Del mismo modo, la aplicación puede ver que un dispositivo tiene capacidades de cámara buscando el objeto funcional de captura de imagen fija.</span><span class="sxs-lookup"><span data-stu-id="15b83-106">Similarly, the application can see that a device has camera capabilities by looking for the Still Image Capture functional object.</span></span>

<span data-ttu-id="15b83-107">Esta representación de objeto flexible ayuda a facilitar la compatibilidad con dispositivos con funciones multifunción.</span><span class="sxs-lookup"><span data-stu-id="15b83-107">This flexible object representation helps enable easy support for devices with multi-function capabilities.</span></span> <span data-ttu-id="15b83-108">Los controladores pueden exponer simplemente los objetos funcionales que representan su dispositivo, lo que es más granular que el uso de las clases de dispositivos tradicionales.</span><span class="sxs-lookup"><span data-stu-id="15b83-108">Drivers can simply expose whatever functional objects represent their device, which is more granular than using traditional device classes.</span></span> <span data-ttu-id="15b83-109">La representación del objeto también ayuda a aislar las partes funcionales superpuestas. por ejemplo, algunos teléfonos pueden tener dos cámaras o cuatro almacenamientos.</span><span class="sxs-lookup"><span data-stu-id="15b83-109">The object representation also helps isolate overlapping functional pieces; for example, some phones may have two cameras or four storages.</span></span>

<span data-ttu-id="15b83-110">En el sistema operativo Windows 7, los servicios amplían los objetos funcionales proporcionando consultas enriquecidas de capacidades y una agrupación abstracta de contenido.</span><span class="sxs-lookup"><span data-stu-id="15b83-110">In the Windows 7 operating system, services extend functional objects by providing rich queries of capabilities and an abstract grouping of content.</span></span> <span data-ttu-id="15b83-111">Las aplicaciones pueden usar los servicios para detectar funcionalidades del dispositivo e interactuar con el contenido de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="15b83-111">Applications can use services to discover device capabilities and to interact with content more efficiently.</span></span> <span data-ttu-id="15b83-112">Por ejemplo, una aplicación puede ver que un dispositivo es compatible con las funcionalidades de sincronización de contactos buscando un objeto de servicio de contactos y puede buscar todos los contactos como objetos secundarios del objeto de servicio, sin tener que buscar de forma recursiva en la jerarquía de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="15b83-112">For example, an application can see that a device supports the contacts-synchronization capabilities by looking for a Contacts service object, and can find all contacts as child objects of the service object, without having to recursively search the storage hierarchy.</span></span>

<span data-ttu-id="15b83-113">Los servicios también permiten a las aplicaciones detectar e invocar el comportamiento personalizado en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15b83-113">Services also allow applications to discover and invoke custom behavior on a device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15b83-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="15b83-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15b83-115">**Información general de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="15b83-115">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



