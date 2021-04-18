---
description: Crear paquetes de instalación para aplicaciones COM+
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Crear paquetes de instalación para aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705304"
---
# <a name="creating-installation-packages-for-com-applications"></a><span data-ttu-id="af435-103">Crear paquetes de instalación para aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="af435-103">Creating Installation Packages for COM+ Applications</span></span>

<span data-ttu-id="af435-104">Puede usar la herramienta administrativa Servicios de componentes o la biblioteca de administración de COM+ para crear paquetes de instalación para aplicaciones COM+ y proxies de aplicación.</span><span class="sxs-lookup"><span data-stu-id="af435-104">You can use the Component Services administrative tool or the COM+ Administration Library to create installation packages for COM+ applications and application proxies.</span></span>

<span data-ttu-id="af435-105">COM+ genera paquetes de instalación de Windows Installer, que en un único archivo contiene todos los componentes necesarios para instalar una aplicación COM+ en otro equipo.</span><span class="sxs-lookup"><span data-stu-id="af435-105">COM+ generates Windows Installer installation packages, which in a single file contain all the necessary pieces to install a COM+ application on another computer.</span></span>

<span data-ttu-id="af435-106">Al exportar una aplicación COM+, la herramienta administrativa Servicios de componentes determina el conjunto de clases, componentes y atributos de la aplicación, así como los atributos de nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="af435-106">When exporting a COM+ application, the Component Services administrative tool determines the application's set of classes, components, and their attributes, as well as application-level attributes.</span></span> <span data-ttu-id="af435-107">A partir de esta información, la herramienta administrativa Servicios de componentes genera un único archivo. msi, que contiene lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="af435-107">From this information, the Component Services administrative tool generates a single .msi file, which contains the following:</span></span>

-   <span data-ttu-id="af435-108">Windows Installer tablas con información de registro COM (consulte la documentación de Windows Installer para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="af435-108">Windows Installer tables with COM registration information (see the Windows Installer documentation for details).</span></span>
-   <span data-ttu-id="af435-109">Un archivo. APL que contiene los atributos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="af435-109">An .apl file containing the application's attributes.</span></span> <span data-ttu-id="af435-110">(Este es un archivo interno; el formato de este archivo no está documentado).</span><span class="sxs-lookup"><span data-stu-id="af435-110">(This is an internal file; the format of this file is not documented.)</span></span>
-   <span data-ttu-id="af435-111">Dll y bibliotecas de tipos que describen las interfaces implementadas por las clases de la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="af435-111">DLLs and type libraries that describe the interfaces implemented by the COM+ application's classes.</span></span>

<span data-ttu-id="af435-112">Además del archivo. msi, la herramienta administrativa Servicios de componentes genera un archivo contenedor (. cab).</span><span class="sxs-lookup"><span data-stu-id="af435-112">In addition to the .msi file, the Component Services administrative tool generates a cabinet (.cab) file.</span></span> <span data-ttu-id="af435-113">Este archivo encapsula el archivo. msi, lo que permite al desarrollador implementar la aplicación COM+ a través de Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="af435-113">This file wraps the .msi file, allowing the developer to deploy the COM+ application through Microsoft Internet Explorer.</span></span>

> [!Note]  
> <span data-ttu-id="af435-114">Al exportar una aplicación COM+, la herramienta administrativa Servicios de componentes solo empaqueta las partes estándar de COM+ de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="af435-114">When exporting a COM+ application, the Component Services administrative tool packages only the standard COM+ parts of the application.</span></span> <span data-ttu-id="af435-115">No empaqueta, por ejemplo, los archivos DLL o de datos dependientes.</span><span class="sxs-lookup"><span data-stu-id="af435-115">It does not package, for example, any dependent DLL or data files.</span></span> <span data-ttu-id="af435-116">Los archivos DLL dependientes deben instalarse primero en un equipo antes de instalar la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="af435-116">The dependent DLL files must first be installed on a computer prior to installing the COM+ application.</span></span> <span data-ttu-id="af435-117">Como alternativa, puede usar la herramienta de creación de Windows Installer para agregar estos archivos dependientes al archivo. msi generado por la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="af435-117">Alternatively, you can use the Windows Installer authoring tool to add these dependent files to the .msi file generated by the Component Services administrative tool.</span></span> <span data-ttu-id="af435-118">(Consulte la documentación de Windows Installer para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="af435-118">(See the Windows Installer documentation for details.)</span></span>

 

## <a name="installing-com-applications-on-other-computers"></a><span data-ttu-id="af435-119">Instalación de aplicaciones COM+ en otros equipos</span><span class="sxs-lookup"><span data-stu-id="af435-119">Installing COM+ Applications on Other Computers</span></span>

<span data-ttu-id="af435-120">El archivo Windows Installer (. msi) generado por la herramienta administrativa Servicios de componentes se puede usar para instalar la aplicación COM+ en otro equipo.</span><span class="sxs-lookup"><span data-stu-id="af435-120">The Windows Installer (.msi) file generated by the Component Services administrative tool can be used to install the COM+ application on another computer.</span></span> <span data-ttu-id="af435-121">El archivo. msi que contiene una aplicación COM+ solo se puede instalar en equipos que admitan servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="af435-121">The .msi file containing a COM+ application can be installed only on computers that support COM+ services.</span></span> <span data-ttu-id="af435-122">Para obtener procedimientos detallados sobre la implementación de aplicaciones COM+, vea "instalar aplicaciones COM+" en la ayuda de administración de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="af435-122">For detailed procedures on deploying COM+ applications, see "Installing COM+ Applications," in the Component Services Administration Help.</span></span>

<span data-ttu-id="af435-123">A menos que se modifique el archivo. msi mediante una herramienta de creación de Windows Installer, las aplicaciones COM+ instaladas mediante el Windows Installer aparecen en el panel de control Agregar o quitar programas.</span><span class="sxs-lookup"><span data-stu-id="af435-123">Unless the .msi file is modified using a Windows Installer authoring tool, COM+ applications installed by using the Windows Installer appear in the Add/Remove Programs control panel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af435-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af435-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af435-125">Implementación de servidores proxy de aplicación</span><span class="sxs-lookup"><span data-stu-id="af435-125">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="af435-126">El catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="af435-126">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 



