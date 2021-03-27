---
description: Windows GDI+ es el subsistema del sistema operativo Windows XP o Windows Server 2003, que es responsable de Mostrar información en pantallas e impresoras. GDI+ es una API que se expone a través de un conjunto de clases de C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Información general sobre GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997461"
---
# <a name="overview-of-gdi"></a><span data-ttu-id="ad7b6-104">Información general sobre GDI+</span><span class="sxs-lookup"><span data-stu-id="ad7b6-104">Overview of GDI+</span></span>

<span data-ttu-id="ad7b6-105">Windows GDI+ es el subsistema del sistema operativo Windows XP o Windows Server 2003, que es responsable de Mostrar información en pantallas e impresoras.</span><span class="sxs-lookup"><span data-stu-id="ad7b6-105">Windows GDI+ is the subsystem of the Windows XP operating system or Windows Server 2003 that is responsible for displaying information on screens and printers.</span></span> <span data-ttu-id="ad7b6-106">GDI+ es una API que se expone a través de un conjunto de clases de C++.</span><span class="sxs-lookup"><span data-stu-id="ad7b6-106">GDI+ is an API that is exposed through a set of C++ classes.</span></span>

<span data-ttu-id="ad7b6-107">Como su nombre sugiere, GDI+ es el sucesor de Windows Interfaz de dispositivo gráfico (GDI), la interfaz de dispositivo gráfico incluida en versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="ad7b6-107">As its name suggests, GDI+ is the successor to Windows Graphics Device Interface (GDI), the graphics device interface included with earlier versions of Windows.</span></span> <span data-ttu-id="ad7b6-108">Windows XP o Windows Server 2003 admiten GDI para la compatibilidad con las aplicaciones existentes, pero los programadores de aplicaciones nuevas deben usar GDI+ para todas sus necesidades de gráficos porque GDI+ optimiza muchas de las capacidades de GDI y también proporciona características adicionales.</span><span class="sxs-lookup"><span data-stu-id="ad7b6-108">Windows XP or Windows Server 2003 supports GDI for compatibility with existing applications, but programmers of new applications should use GDI+ for all their graphics needs because GDI+ optimizes many of the capabilities of GDI and also provides additional features.</span></span>

<span data-ttu-id="ad7b6-109">Una interfaz de dispositivo gráfico, como GDI+, permite a los programadores de aplicaciones Mostrar información en una pantalla o una impresora sin tener que preocuparse de los detalles de un determinado dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ad7b6-109">A graphics device interface, such as GDI+, allows application programmers to display information on a screen or printer without having to be concerned about the details of a particular display device.</span></span> <span data-ttu-id="ad7b6-110">El programador de la aplicación realiza llamadas a los métodos proporcionados por las clases de GDI+ y, a su vez, realiza las llamadas adecuadas a controladores de dispositivos específicos.</span><span class="sxs-lookup"><span data-stu-id="ad7b6-110">The application programmer makes calls to methods provided by GDI+ classes and those methods in turn make the appropriate calls to specific device drivers.</span></span> <span data-ttu-id="ad7b6-111">GDI+ aísla la aplicación del hardware de gráficos y es este aislamiento que permite a los desarrolladores crear aplicaciones independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ad7b6-111">GDI+ insulates the application from the graphics hardware, and it is this insulation that allows developers to create device-independent applications.</span></span>

 

 



