---
description: Al crear un archivo INF para una aplicación de instalación, también debe consultar el formato de archivo INF que se documenta en las secciones instrucciones generales para archivos INF y las secciones y directivas de archivos INF del kit de desarrollo de controladores de Microsoft Windows 2000.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Creación de un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666430"
---
# <a name="authoring-an-inf-file"></a><span data-ttu-id="900fc-103">Creación de un archivo INF</span><span class="sxs-lookup"><span data-stu-id="900fc-103">Authoring an INF file</span></span>

<span data-ttu-id="900fc-104">Al crear un archivo INF para una aplicación de instalación, también debe consultar el formato de archivo INF que se documenta en las secciones *instrucciones generales para archivos INF* y las *secciones y directivas de archivos* inf del kit de desarrollo de controladores de Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="900fc-104">When authoring an INF file for a Setup application you should also refer to the INF file format documented in *General Guidelines for INF Files* and *INF File Sections and Directives* of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="900fc-105">Al crear archivos INF para una aplicación de instalación, debe cumplir las siguientes reglas.</span><span class="sxs-lookup"><span data-stu-id="900fc-105">When authoring INF files for a setup application adhere to the following rules.</span></span>

-   <span data-ttu-id="900fc-106">Se requiere una sección de **versión** en cada archivo INF.</span><span class="sxs-lookup"><span data-stu-id="900fc-106">A **Version** section is required in every INF file.</span></span>
-   <span data-ttu-id="900fc-107">Las secciones deben comenzar con el nombre de sección entre corchetes ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="900fc-107">Sections must begin with the section name enclosed by square brackets (\[\]).</span></span>
-   <span data-ttu-id="900fc-108">Los nombres de las secciones **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings** y **version** deben ser idénticos al tipo de sección.</span><span class="sxs-lookup"><span data-stu-id="900fc-108">Names of **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings**, and **Version** sections must be identical to the section type.</span></span> <span data-ttu-id="900fc-109">Por ejemplo, use \[ DestinationDirs \] .</span><span class="sxs-lookup"><span data-stu-id="900fc-109">For example use \[DestinationDirs\].</span></span> <span data-ttu-id="900fc-110">Los autores pueden especificar los nombres de otros tipos de secciones.</span><span class="sxs-lookup"><span data-stu-id="900fc-110">Authors may specify the names of other types of sections.</span></span>
-   <span data-ttu-id="900fc-111">Los nombres de las secciones **SourceDisksNames** y **SourceDisksFiles** se pueden anexar con un sufijo específico de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="900fc-111">Names of **SourceDisksNames** and **SourceDisksFiles** sections may be appended with a platform-specific suffix.</span></span> <span data-ttu-id="900fc-112">Por ejemplo, para mostrar una sección **SourceDisksNames** específica de Intel, use \[ SourceDisksNames. x86 \] .</span><span class="sxs-lookup"><span data-stu-id="900fc-112">For example, to show an Intel-specific **SourceDisksNames** section use \[SourceDisksNames.x86\].</span></span> <span data-ttu-id="900fc-113">Si las funciones de instalación buscan secciones **SourceDisksNames** y **SourceDisksFiles** específicas de la plataforma que coincidan con la plataforma del usuario, las funciones usan las secciones específicas de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="900fc-113">If the setup functions find platform-specific **SourceDisksNames** and **SourceDisksFiles** sections matching the user's platform, the functions use the platform-specific sections.</span></span> <span data-ttu-id="900fc-114">De lo contrario, las funciones de instalación usan las secciones **SourceDisksNames** y **SourceDisksFiles** sin sufijo.</span><span class="sxs-lookup"><span data-stu-id="900fc-114">Otherwise the setup functions use the non-suffixed **SourceDisksNames** and **SourceDisksFiles** sections.</span></span> <span data-ttu-id="900fc-115">Las funciones de configuración pueden determinar mediante programación el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="900fc-115">The setup functions can programmatically determine the user's system.</span></span> <span data-ttu-id="900fc-116">Vea el [ejemplo de secciones SourceDisksNames y SourceDisksFiles de INF](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span><span class="sxs-lookup"><span data-stu-id="900fc-116">See the [INF SourceDisksNames and SourceDisksFiles Sections Example](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span></span>
-   <span data-ttu-id="900fc-117">Los valores se pueden expresar como cadenas reemplazables con la forma%*strkey*%.</span><span class="sxs-lookup"><span data-stu-id="900fc-117">Values may be expressed as replaceable strings using the form %*strkey*%.</span></span> <span data-ttu-id="900fc-118">Para usar un carácter% en la cadena, use%%.</span><span class="sxs-lookup"><span data-stu-id="900fc-118">To use a % character in the string, use %%.</span></span> <span data-ttu-id="900fc-119">Strkey debe definirse en una sección **Strings** del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="900fc-119">The strkey must be defined in a **Strings** section of the INF file.</span></span>

 

 



