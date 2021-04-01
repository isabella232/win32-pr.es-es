---
description: A partir de Windows XP, puede crear un ensamblado privado y hacer que esté disponible para una aplicación específica.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Corregir una aplicación existente mediante un ensamblado privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082062"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a><span data-ttu-id="7ac48-103">Corregir una aplicación existente mediante un ensamblado privado</span><span class="sxs-lookup"><span data-stu-id="7ac48-103">Fixing an Existing Application Using a Private Assembly</span></span>

<span data-ttu-id="7ac48-104">A partir de Windows XP, puede crear un ensamblado privado y hacer que esté disponible para una aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="7ac48-104">Beginning with Windows XP, you can create a private assembly and make it available to a specific application.</span></span> <span data-ttu-id="7ac48-105">Esta capacidad se puede utilizar para corregir una aplicación que es incompatible con una actualización.</span><span class="sxs-lookup"><span data-stu-id="7ac48-105">This capability can be used to fix an application that becomes incompatible with an update.</span></span> <span data-ttu-id="7ac48-106">Un ejemplo sería una aplicación que sea incompatible con la versión más reciente de MSVCRT.DLL después de actualizar el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7ac48-106">An example would be an application that becomes incompatible with the latest version of MSVCRT.DLL after upgrading the operating system.</span></span> <span data-ttu-id="7ac48-107">En este caso, no tiene la opción de reemplazar la versión del sistema porque MSVCRT.DLL es un archivo protegido de Windows.</span><span class="sxs-lookup"><span data-stu-id="7ac48-107">In this case, you do not have the option of replacing the system version because MSVCRT.DLL is a Windows Protected File.</span></span> <span data-ttu-id="7ac48-108">En lugar de tener que volver a escribir la aplicación para que funcione con la nueva versión de MSVCRT, puede crear un ensamblado privado para MSVCRT e instalarlo en la carpeta de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7ac48-108">Rather than having to rewrite the application to work with the new version of MSVCRT, you can create a private assembly for MSVCRT and install this in your application folder.</span></span> <span data-ttu-id="7ac48-109">Tenga en cuenta que no todos los componentes compartidos son un candidato adecuado para un ensamblado en paralelo privado y algunos componentes tienen restricciones de licencia sobre dónde se pueden instalar sus componentes.</span><span class="sxs-lookup"><span data-stu-id="7ac48-109">Note that not every shared component is a suitable candidate for a private side-by-side assembly, and some components have licensing restrictions about where their components can be installed.</span></span> <span data-ttu-id="7ac48-110">El componente debe cumplir los criterios de un componente en paralelo.</span><span class="sxs-lookup"><span data-stu-id="7ac48-110">The component needs to meet the criteria for a side-by-side component.</span></span> <span data-ttu-id="7ac48-111">Pregunte al publicador del componente si puede proporcionar un ensamblado adecuado.</span><span class="sxs-lookup"><span data-stu-id="7ac48-111">Ask the publisher of the component if they can provide a suitable assembly.</span></span>

<span data-ttu-id="7ac48-112">El manifiesto del ensamblado privado y el manifiesto de la aplicación deben instalarse en la misma carpeta que el ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7ac48-112">The private assembly's manifest and the application's manifest should both be installed in the same folder as the application's executable.</span></span> <span data-ttu-id="7ac48-113">Cuando se ejecuta la aplicación, consulta el manifiesto de aplicación y carga la versión de MSVCRT que es privada para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7ac48-113">When the application runs, it consults the application manifest and load the version of MSVCRT that is private to the application.</span></span>

<span data-ttu-id="7ac48-114">En este ejemplo, el ensamblado privado incluiría MSVCRT.DLL y MSVCIRT.DLL como en el siguiente manifiesto del ensamblado:</span><span class="sxs-lookup"><span data-stu-id="7ac48-114">For this example, the private assembly would include both MSVCRT.DLL and MSVCIRT.DLL as in the following assembly manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

<span data-ttu-id="7ac48-115">El siguiente es un ejemplo de un posible manifiesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="7ac48-115">The following is an example of a possible application manifest.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



