---
description: En Windows Server 2003, WinHTTP se implementa como un ensamblado en paralelo y debe estar vinculado a como tal. Tenga en cuenta que esto no se aplica a Windows Vista y versiones posteriores.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Usar WinHTTP como un ensamblado en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74a0e5cf842fdd1e20c6d6d271de482e361c4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809782"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a><span data-ttu-id="3b8a9-104">Usar WinHTTP como un ensamblado en paralelo</span><span class="sxs-lookup"><span data-stu-id="3b8a9-104">Using WinHTTP as a Side-by-side Assembly</span></span>

<span data-ttu-id="3b8a9-105">En Windows Server 2003, WinHTTP se implementa como un ensamblado en paralelo y debe estar vinculado a como tal.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-105">On Windows Server 2003, WinHTTP is implemented as a side-by-side assembly, and must be linked to as such.</span></span> <span data-ttu-id="3b8a9-106">Tenga en cuenta que esto no se aplica a Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-106">Note that this does not apply to Windows Vista and later.</span></span>

## <a name="side-by-side-assemblies"></a><span data-ttu-id="3b8a9-107">Ensamblados en paralelo</span><span class="sxs-lookup"><span data-stu-id="3b8a9-107">Side-by-side Assemblies</span></span>

<span data-ttu-id="3b8a9-108">A partir de Microsoft Windows XP, se proporciona un mecanismo de ensamblados en paralelo para controlar la vinculación en tiempo de ejecución para evitar conflictos de versiones de la biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="3b8a9-108">Starting with Microsoft Windows XP, a side-by-side assemblies mechanism was provided to control run-time linking to avoid dynamic-link-library (DLL) versioning conflicts.</span></span> <span data-ttu-id="3b8a9-109">Para obtener información sobre los ensamblados en paralelo, vea [acerca de las aplicaciones aisladas y los ensamblados en paralelo](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).</span><span class="sxs-lookup"><span data-stu-id="3b8a9-109">For information about side-by-side assemblies, see [About Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).</span></span>

<span data-ttu-id="3b8a9-110">Para usar este mecanismo para vincular a la versión 5,1 de WinHTTP en Windows Server 2003, una aplicación debe incorporar un manifiesto que especifique WinHTTP como ensamblado dependiente.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-110">To use this mechanism to link to WinHTTP version 5.1 on Windows Server 2003, an application must incorporate a manifest that specifies WinHTTP as a dependent assembly.</span></span> <span data-ttu-id="3b8a9-111">Vea [usar ensamblados en paralelo](/windows/desktop/SbsCs/using-side-by-side-assemblies) para obtener más información sobre cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-111">See [Using Side-by-side Assemblies](/windows/desktop/SbsCs/using-side-by-side-assemblies) for more information about how to do this.</span></span>

## <a name="a-sample-winhttp-application-manifest"></a><span data-ttu-id="3b8a9-112">Un manifiesto de aplicación WinHTTP de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3b8a9-112">A Sample WinHTTP Application Manifest</span></span>

<span data-ttu-id="3b8a9-113">En el manifiesto de ejemplo siguiente se muestra un manifiesto de aplicación que se puede usar para vincular a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-113">The sample manifest below illustrates an application manifest that can be used for linking to WinHTTP.</span></span>

<span data-ttu-id="3b8a9-114">Todos los atributos excepto "tipo" de " <assembly> <assemblyIdentity> " se deben modificar según sea necesario para la aplicación en cuestión.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-114">All attributes except "type" of the "<assembly><assemblyIdentity>" must be modified as appropriate for your particular application.</span></span> <span data-ttu-id="3b8a9-115">Lo mismo sucede con el contenido del elemento " &lt; Description &gt; ".</span><span class="sxs-lookup"><span data-stu-id="3b8a9-115">The same goes for the contents of the "&lt;description&gt;" element.</span></span>

<span data-ttu-id="3b8a9-116">Además, asegúrese de que el atributo "processorArchitecture" de " <dependentAssembly> <assemblyIdentity> " coincide con el atributo "processorArchitecture" de " <assembly> <assemblyIdentity> ".</span><span class="sxs-lookup"><span data-stu-id="3b8a9-116">In addition, make sure that the "processorArchitecture" attribute of the "<dependentAssembly><assemblyIdentity>" matches the "processorArchitecture" attribute of the "<assembly><assemblyIdentity>".</span></span> <span data-ttu-id="3b8a9-117">A continuación, por ejemplo, ambos se establecen en "x86".</span><span class="sxs-lookup"><span data-stu-id="3b8a9-117">Below, for example, both are set to "x86".</span></span>

<span data-ttu-id="3b8a9-118">Todos los valores que no son específicos de la aplicación deben tener los formularios que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-118">All values not specific to your application should take the forms shown below.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
