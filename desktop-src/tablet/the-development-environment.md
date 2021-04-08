---
description: No necesita un Tablet PC para desarrollar aplicaciones de Tablet PC, pero sí necesita un equipo personal capaz de ejecutar el software que se muestra más adelante en este tema.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: El entorno de desarrollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefa29a518beaf21aa8b2457abf17d9581075f73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003067"
---
# <a name="the-development-environment"></a><span data-ttu-id="16418-103">El entorno de desarrollo</span><span class="sxs-lookup"><span data-stu-id="16418-103">The Development Environment</span></span>

<span data-ttu-id="16418-104">No necesita un Tablet PC para desarrollar aplicaciones de Tablet PC, pero sí necesita un equipo personal capaz de ejecutar el software que se muestra más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="16418-104">You do not need a Tablet PC to develop Tablet PC applications, but you do need a personal computer capable of running the software listed later in this topic.</span></span>

<span data-ttu-id="16418-105">Se recomienda encarecidamente que pruebe la aplicación en un Tablet PC real para asegurarse de que se tienen en cuenta todas las diferencias en el hardware, como el digitalizador de mayor resolución.</span><span class="sxs-lookup"><span data-stu-id="16418-105">We strongly recommend that you test your application on an actual Tablet PC to ensure that all differences in hardware, such as the higher resolution digitizer, are accounted for.</span></span>

<span data-ttu-id="16418-106">Un sistema de desarrollo típico y mínimo consta del siguiente hardware y software.</span><span class="sxs-lookup"><span data-stu-id="16418-106">A typical, minimal development system consists of the following hardware and software.</span></span>

## <a name="hardware"></a><span data-ttu-id="16418-107">Hardware</span><span class="sxs-lookup"><span data-stu-id="16418-107">Hardware</span></span>

-   <span data-ttu-id="16418-108">8 MB de espacio en disco duro para una instalación completa.</span><span class="sxs-lookup"><span data-stu-id="16418-108">8 MB of hard disk space for a complete installation.</span></span>
-   <span data-ttu-id="16418-109">Un dispositivo señalador para la entrada.</span><span class="sxs-lookup"><span data-stu-id="16418-109">A pointing device for input.</span></span> <span data-ttu-id="16418-110">Esto incluye dispositivos como un mouse, una tableta externa o un Tablet PC con un digitalizador HID.</span><span class="sxs-lookup"><span data-stu-id="16418-110">This includes devices such as a mouse, an external tablet, or a Tablet PC with an HID digitizer.</span></span>

<span data-ttu-id="16418-111">HID significa Dispositivo de interfaz humana, un estándar para dispositivos de entrada.</span><span class="sxs-lookup"><span data-stu-id="16418-111">HID stands for Human Interface Device, a standard for input devices.</span></span> <span data-ttu-id="16418-112">Los digitalizadores que no son compatibles con HID se tratan como un mouse normal, mientras que los digitalizadores compatibles con HID tienen una mayor resolución y más metadatos en los trazos, como la presión, similar a los que están instalados en el hardware de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="16418-112">Non-HID compliant digitizers are treated like a regular mouse, while HID compliant digitizers have higher resolution and more metadata on strokes, such as pressure, similar to those that are installed on Tablet PC hardware.</span></span>

## <a name="software"></a><span data-ttu-id="16418-113">Software</span><span class="sxs-lookup"><span data-stu-id="16418-113">Software</span></span>

<span data-ttu-id="16418-114">Los siguientes sistemas operativos se pueden usar para desarrollar aplicaciones de Tablet PC:</span><span class="sxs-lookup"><span data-stu-id="16418-114">The following operating systems can be used to develop Tablet PC applications:</span></span>

-   <span data-ttu-id="16418-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="16418-115">Windows 7</span></span>
-   <span data-ttu-id="16418-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16418-116">Windows Vista</span></span>
-   <span data-ttu-id="16418-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16418-117">Windows Server 2008</span></span>
-   <span data-ttu-id="16418-118">Windows XP Tablet PC Edition 2005</span><span class="sxs-lookup"><span data-stu-id="16418-118">Windows XP Tablet PC Edition 2005</span></span>
-   <span data-ttu-id="16418-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="16418-119">Windows Server 2003</span></span>
-   <span data-ttu-id="16418-120">Windows XP Professional</span><span class="sxs-lookup"><span data-stu-id="16418-120">Windows XP Professional</span></span>

<span data-ttu-id="16418-121">También necesita lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="16418-121">You also need:</span></span>

-   <span data-ttu-id="16418-122">Visual Studio versión 6 con Service Pack 5, Visual Studio .NET o Visual Studio .NET 2005</span><span class="sxs-lookup"><span data-stu-id="16418-122">Visual Studio version 6 with Service Pack 5, or Visual Studio .NET, or Visual Studio .NET 2005</span></span>
-   <span data-ttu-id="16418-123">Microsoft Internet Explorer 6 o posterior (recomendado)</span><span class="sxs-lookup"><span data-stu-id="16418-123">Microsoft Internet Explorer 6, or higher (recommended)</span></span>

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a><span data-ttu-id="16418-124">Detalles sobre el desarrollo en SKU que no son de Tablet PC de Windows</span><span class="sxs-lookup"><span data-stu-id="16418-124">Details on Developing on Non-Tablet PC SKUs of Windows</span></span>

<span data-ttu-id="16418-125">Los componentes de la plataforma de Tablet PC se pueden instalar en Windows XP Professional con Service Pack 2 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="16418-125">The Tablet PC platform components can be installed on Windows XP Professional with Service Pack 2 or Windows Server 2003.</span></span> <span data-ttu-id="16418-126">En estos sistemas operativos, la aplicación puede recopilar entradas manuscritas con la clase [**InkCollector**](inkcollector-class.md) y se puede probar y depurar.</span><span class="sxs-lookup"><span data-stu-id="16418-126">On these operating systems, your application can collect ink with the [**InkCollector**](inkcollector-class.md) class and can be tested and debugged.</span></span> <span data-ttu-id="16418-127">Sin embargo, no hay ningún reconocimiento disponible a menos que también Instale el paquete de reconocimiento de Microsoft Windows XP Tablet PC Edition 2005.</span><span class="sxs-lookup"><span data-stu-id="16418-127">However, no recognition is available unless you also install the Microsoft Windows XP Tablet PC Edition 2005 Recognizer Pack.</span></span> <span data-ttu-id="16418-128">Puede descargar ese paquete desde el centro de descarga de en MSDN.</span><span class="sxs-lookup"><span data-stu-id="16418-128">You can download that pack from the Download Center on MSDN.</span></span>

<span data-ttu-id="16418-129">Después de instalar el Windows SDK en un sistema Windows XP Professional o Windows Server 2003, tendrá todos los archivos de desarrollo necesarios para compilar aplicaciones de entrada manuscrita (como msinkaut. h para un desarrollador COM).</span><span class="sxs-lookup"><span data-stu-id="16418-129">After installing the Windows SDK on to a Windows XP Professional or Windows Server 2003 system, you will have all the development files necessary to build ink applications (such as msinkaut.h for a COM developer).</span></span> <span data-ttu-id="16418-130">Sin embargo, no podrá ejecutar ni depurar la aplicación en ese sistema hasta que instale los archivos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="16418-130">However, you will be unable to run or debug your application on that system until you install the runtime files.</span></span> <span data-ttu-id="16418-131">Por ejemplo, en el caso de un desarrollador COM, inkobj.dll se debe instalar y registrar.</span><span class="sxs-lookup"><span data-stu-id="16418-131">For instance, in the case of a COM developer, inkobj.dll must be installed and registered.</span></span> <span data-ttu-id="16418-132">Dado que no está en un sistema donde existan estos archivos de plataforma, debe instalar los componentes de la plataforma de Tablet PC del módulo de combinación redistribuible, mstpcrt. MSM, para obtener los archivos en tiempo de ejecución en el sistema.</span><span class="sxs-lookup"><span data-stu-id="16418-132">Because you are not on a system where these platform files exist, you must install the Tablet PC platform components from the redistributable merge module, mstpcrt.msm, to get the runtime files on your system.</span></span>

<span data-ttu-id="16418-133">La manera más sencilla de obtener los tiempos de ejecución de la plataforma instalados en un sistema Windows XP Professional o Windows 2000 con fines de desarrollo consiste en compilar el proyecto de instalación de ejemplo que se proporciona con los ejemplos de PC móvil y Tablet PC e implementarlo en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="16418-133">The simplest way to get the platform runtimes installed on a Windows XP Professional or Windows 2000 system for development purposes is to compile the sample setup project provided with the Mobile PC and Tablet PC Samples and deploy it to the development machine.</span></span>

> [!Note]  
> <span data-ttu-id="16418-134">Windows Vista y Windows XP Tablet PC Edition 2005 ya tienen instalados los componentes de la plataforma, por lo que no requieren pasos adicionales para ejecutar y depurar aplicaciones de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="16418-134">Windows Vista and Windows XP Tablet PC Edition 2005 already have the platform components installed, so they do not require additional steps to run and debug Tablet PC applications.</span></span>

 

<span data-ttu-id="16418-135">Los controles [InkEdit](inkedit-control-reference.md) y [InkPicture](inkpicture-control-reference.md) se pueden usar para recopilar la entrada de lápiz en Windows 2000 con Service Pack 4 o Windows XP Professional con Service Pack 2 cuando los componentes de la plataforma de Tablet PC están presentes instalando la versión 1,7 del SDK de Tablet PC, pero no pueden recopilar entradas de lápiz en sistemas que no son de Tablet PC y que no tienen instalados los componentes de la plataforma de Tablet</span><span class="sxs-lookup"><span data-stu-id="16418-135">The [InkEdit](inkedit-control-reference.md) and [InkPicture](inkpicture-control-reference.md) controls can be used to collect ink on Windows 2000 with Service Pack 4 or Windows XP Professional with Service Pack 2 when the Tablet PC platform components are present by installing the Tablet PC SDK version 1.7, but are not able to collect ink on non-Tablet PC systems that do not have the Tablet PC platform components installed.</span></span>

<span data-ttu-id="16418-136">La Windows SDK proporciona todos los componentes necesarios para desarrollar aplicaciones de Tablet PC en SKU que no son de Tablet PC de Windows.</span><span class="sxs-lookup"><span data-stu-id="16418-136">The Windows SDK provides all the necessary components to develop Tablet PC applications on non-Tablet SKUs of Windows.</span></span> <span data-ttu-id="16418-137">Establezca la siguiente clave **DWORD** del registro en 1 para recopilar la entrada de lápiz en las SKU de Windows que no son de Tablet PC:</span><span class="sxs-lookup"><span data-stu-id="16418-137">Set the following **DWORD** registry key to 1 in order to collect ink on non-Tablet SKUs of Windows:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

<span data-ttu-id="16418-138">Esta clave está pensada solo para fines de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="16418-138">This key is intended for development purposes only.</span></span>

 

 



