---
description: En este ejemplo se muestra cómo implementar una aplicación de Tablet PC administrada en la web mediante una implementación sin interacción.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: Ejemplo de Web de implementación de No-Touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0742deef8ea9b418fba6de4724975ee27693f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104547283"
---
# <a name="no-touch-deployment-web-sample"></a><span data-ttu-id="af5ec-103">Ejemplo de Web de implementación de No-Touch</span><span class="sxs-lookup"><span data-stu-id="af5ec-103">No-Touch Deployment Web Sample</span></span>

<span data-ttu-id="af5ec-104">En este ejemplo se muestra cómo implementar una aplicación de Tablet PC administrada en la web mediante una implementación sin interacción.</span><span class="sxs-lookup"><span data-stu-id="af5ec-104">This sample shows how to deploy a managed Tablet PC application over the Web by using no-touch deployment.</span></span> <span data-ttu-id="af5ec-105">Debe estar familiarizado con los conceptos descritos en [implementación no táctil en el .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).</span><span class="sxs-lookup"><span data-stu-id="af5ec-105">You should be familiar with the concepts discussed in [No-Touch Deployment in the .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).</span></span> <span data-ttu-id="af5ec-106">El equipo debe tener instalado Microsoft Internet Information Services (IIS) para ejecutar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="af5ec-106">Your computer must have Microsoft Internet Information Services (IIS) installed to run this sample.</span></span>

## <a name="overview"></a><span data-ttu-id="af5ec-107">Información general</span><span class="sxs-lookup"><span data-stu-id="af5ec-107">Overview</span></span>

<span data-ttu-id="af5ec-108">Con una implementación sin intervención del usuario, las aplicaciones de Windows Forms de Tablet PCWindows se crean mediante las clases del espacio de nombres System. Windows. Forms del marco Microsoft .NET y el kit de desarrollo 1,7 de Microsoft Windows XP Tablet PC Edition, se pueden descargar, instalar y ejecutar directamente en los equipos de los usuarios sin alterar los componentes del registro o del sistema compartido.</span><span class="sxs-lookup"><span data-stu-id="af5ec-108">With no-touch deployment, Tablet PCWindows Forms applications-desktop applications built by using the classes in the System.Windows.Forms namespace of the Microsoft .NET Framework and the Microsoft Windows XP Tablet PC Edition Development Kit 1.7-can be downloaded, installed, and run directly on users' computers without any alteration of the registry or shared system components.</span></span>

<span data-ttu-id="af5ec-109">Este ejemplo toma el proyecto original para el [ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md), las notificaciones automáticas y proporciona un proyecto de instalador, autoclaims \_ NoTouchWeb.</span><span class="sxs-lookup"><span data-stu-id="af5ec-109">This sample takes the original project for [Auto Claims Form Sample](auto-claims-form-sample.md), AutoClaims, and provides an installer project, AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="af5ec-110">Una vez compilada y ejecutada, el proyecto del instalador crea una nueva raíz virtual, también denominada autoclaims \_ NoTouchWeb.</span><span class="sxs-lookup"><span data-stu-id="af5ec-110">Once compiled and run, the installer project creates a new virtual root, also called AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="af5ec-111">El instalador copia un archivo, default.htm, que incluye un vínculo al ensamblado de AutoClaims.exe.</span><span class="sxs-lookup"><span data-stu-id="af5ec-111">The installer copies a file, default.htm, that includes a link to the AutoClaims.exe assembly.</span></span> <span data-ttu-id="af5ec-112">Para iniciar la aplicación cliente enriquecida, vaya a la raíz virtual con Microsoft Internet Explorer y, a continuación, haga clic en el vínculo de la página default.htm.</span><span class="sxs-lookup"><span data-stu-id="af5ec-112">To launch the rich client application, navigate to the virtual root with Microsoft Internet Explorer, and then click the link in the default.htm page.</span></span>

> [!Note]  
> <span data-ttu-id="af5ec-113">Debe desplazarse a la raíz virtual mediante IIS (por ejemplo, https://localhost/AutoClaims\_NoTouchWeb/default.htm) y no directamente a través del sistema de archivos para que la aplicación funcione en el dominio de aplicación de Internet Explorer).</span><span class="sxs-lookup"><span data-stu-id="af5ec-113">You must navigate to the virtual root by way of IIS (for example, https://localhost/AutoClaims\_NoTouchWeb/default.htm) and not directly through the file system in order for the application to work in the Internet Explorer application domain.</span></span>

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a><span data-ttu-id="af5ec-114">Requisitos de implementación de No-Touch</span><span class="sxs-lookup"><span data-stu-id="af5ec-114">No-Touch Deployment Requirements</span></span>

<span data-ttu-id="af5ec-115">Todos los ensamblados dependientes deben encontrarse en la ruta de búsqueda del ensamblado o en la raíz del directorio virtual del sitio Web.</span><span class="sxs-lookup"><span data-stu-id="af5ec-115">All dependent assemblies must be located either in the assembly search path or the root of the virtual directory of the Web site.</span></span> <span data-ttu-id="af5ec-116">El proyecto de implementación de autoclaims \_ NoTouchWeb instala el ensamblado y la página de referencia, default.htm, en la misma raíz virtual (Autoclaims \_ NoTouchWeb).</span><span class="sxs-lookup"><span data-stu-id="af5ec-116">The AutoClaims\_NoTouchWeb deployment project installs the assembly and the referring page, default.htm, into the same virtual root (AutoClaims\_NoTouchWeb).</span></span>

> [!Note]  
> <span data-ttu-id="af5ec-117">Los ejemplos web compilados no se instalan con la opción de instalación predeterminada para el SDK.</span><span class="sxs-lookup"><span data-stu-id="af5ec-117">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="af5ec-118">Debe completar una instalación personalizada y seleccionar la subopción "ejemplos web precompilados" para instalarlas.</span><span class="sxs-lookup"><span data-stu-id="af5ec-118">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="af5ec-119">Para obtener más información sobre el uso de entradas manuscritas en la web, consulte [entrada de lápiz en la web](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="af5ec-119">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

 

 