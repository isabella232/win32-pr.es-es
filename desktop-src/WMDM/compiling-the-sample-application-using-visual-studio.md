---
title: Compilar la aplicación de ejemplo con Visual Studio
description: Compilar la aplicación de ejemplo con Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Administrador de dispositivos de Windows Media, ejemplos
- Administrador de dispositivos, ejemplos
- aplicaciones de escritorio, ejemplos
- Windows Media Administrador de dispositivos, ejemplo de aplicación de escritorio
- Administrador de dispositivos, ejemplo de aplicación de escritorio
- ejemplos, aplicaciones de escritorio
- ejemplos, compilar con Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075492"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a><span data-ttu-id="fcecb-110">Compilar la aplicación de ejemplo con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fcecb-110">Compiling the Sample Application Using Visual Studio</span></span>

<span data-ttu-id="fcecb-111">El SDK de Administrador de dispositivos de Windows Media incluye una solución de Visual Studio que es compatible con Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="fcecb-111">The Windows Media Device Manager SDK includes a Visual Studio solution that is compatible with Microsoft Visual Studio 2005.</span></span>

<span data-ttu-id="fcecb-112">Antes de compilar la aplicación de ejemplo, debe cambiar el nombre del archivo de encabezado shtypes. h para evitar conflictos con un archivo con el mismo nombre que se encuentra en el SDK de la plataforma de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fcecb-112">Before you compile the sample application, you must rename the header file shtypes.h to prevent conflicts with a file of the same name that is found in the Microsoft Platform SDK.</span></span> <span data-ttu-id="fcecb-113">Por ejemplo, podría cambiar el nombre de <*ruta de instalación del SDK* > \\ WMFSDK11 \\ incluir \\ shtypes. h a <*ruta de instalación del SDK* > \\ WMFSDK11 \\ incluir \\ shtypes. h. backup.</span><span class="sxs-lookup"><span data-stu-id="fcecb-113">For example, you could rename <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h to <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h.backup.</span></span>

<span data-ttu-id="fcecb-114">Para compilar la aplicación, inicie una instancia de Visual Studio 2005, abra el archivo de solución wmdmapp. sln, que se encuentra en la carpeta <*ruta de instalación del SDK* > \\ WMFSDK11 \\ apps \\ wmdmapp y elija la opción **compilar/compilar solución** .</span><span class="sxs-lookup"><span data-stu-id="fcecb-114">To build the application, start an instance of Visual Studio 2005, open the solution file, wmdmapp.sln, which is found in the folder <*SDK installation path*>\\WMFSDK11\\apps\\wmdmapp and choose the **Build/Build Solution** option.</span></span> <span data-ttu-id="fcecb-115">Esto creará dos archivos de proyecto: el proyecto auxiliar, proghelp. vcproj, así como la aplicación principal wmdmapp. vcproj.</span><span class="sxs-lookup"><span data-stu-id="fcecb-115">This will create two project files: the helper project, proghelp.vcproj, as well as the main application wmdmapp.vcproj.</span></span> <span data-ttu-id="fcecb-116">Además, se creará la DLL de aplicación auxiliar de progreso y la aplicación principal (WMDMApp.exe).</span><span class="sxs-lookup"><span data-stu-id="fcecb-116">In addition, it will create the progress helper DLL and the main application (WMDMApp.exe).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcecb-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fcecb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcecb-118">**Aplicación de escritorio de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="fcecb-118">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




