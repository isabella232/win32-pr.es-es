---
description: La sección SourceDisksNames de un archivo INF identifica los discos que contienen los archivos de origen que se están instalando.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Ejemplo de secciones SourceDisksNames y SourceDisksFiles de INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f991727a8a2ca9cce2bd2d7161dfbf27b62ce74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667996"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a><span data-ttu-id="af60e-103">Ejemplo de secciones SourceDisksNames y SourceDisksFiles de INF</span><span class="sxs-lookup"><span data-stu-id="af60e-103">INF SourceDisksNames and SourceDisksFiles Sections Example</span></span>

<span data-ttu-id="af60e-104">La sección **SourceDisksNames** de un archivo INF identifica los discos que contienen los archivos de origen que se están instalando.</span><span class="sxs-lookup"><span data-stu-id="af60e-104">The **SourceDisksNames** section of an INF file identifies the disks that contain the source files being installed.</span></span> <span data-ttu-id="af60e-105">La sección **SourceDisksFiles** identifica los archivos de origen y los discos de origen que los contienen.</span><span class="sxs-lookup"><span data-stu-id="af60e-105">The **SourceDisksFiles** section identifies the source files and the source disks that contain them.</span></span> <span data-ttu-id="af60e-106">Tenga en cuenta que las plataformas MIPS, Alpha y PPC no son compatibles con Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="af60e-106">Note that MIPS, Alpha, and PPC platforms are not supported by Windows 2000 or Windows XP.</span></span>

<span data-ttu-id="af60e-107">A partir de Windows XP, una sección **SourceDisksNames** puede especificar una etiqueta y un archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="af60e-107">Beginning with Windows XP, a **SourceDisksNames** section may specify a tag as well as cabinet file.</span></span> <span data-ttu-id="af60e-108">Por ejemplo, la siguiente sección **SourceDisksNames** se puede usar con medios extraíbles o fijos.</span><span class="sxs-lookup"><span data-stu-id="af60e-108">For example, the following **SourceDisksNames** section may be used with removable or fixed media.</span></span> <span data-ttu-id="af60e-109">Si se usa un medio extraíble, en la sección de ejemplo se comprueba la presencia del medio comprobando en primer lugar la presencia de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="af60e-109">If using removable media, the example section verifies the presence of the media by first checking for the presence of the tag.</span></span> <span data-ttu-id="af60e-110">Si usa medios fijos, en la sección de ejemplo se comprueba la presencia del medio comprobando primero la presencia del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="af60e-110">If using fixed media, the example section verifies the presence of the media by first checking for the presence of the cabinet.</span></span> <span data-ttu-id="af60e-111">Después de comprobar la presencia de un archivo. cab, el sistema intenta copiar archivos fuera del archivo. cab y solicita los archivos que no se pudieron copiar.</span><span class="sxs-lookup"><span data-stu-id="af60e-111">After verifying the presence of a cabinet, the system attempts to copy files out of the cabinet and prompts for any files it was unable to copy.</span></span>

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

<span data-ttu-id="af60e-112">Para obtener más información acerca de **SourceDisksNames** o **SourceDisksFiles**, vea las secciones "instrucciones generales para el archivo INF" y "secciones y directivas de archivos INF" del kit de desarrollo de controladores de Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="af60e-112">For more information about **SourceDisksNames** or **SourceDisksFiles**, see the "General Guidelines for INF File" and "INF File Sections and Directives" sections of the Microsoft Windows 2000 Driver Development Kit.</span></span>

 

 



