---
description: Si desea que los usuarios de la aplicación, o el archivo DLL principal, puedan cambiar el idioma de la interfaz de usuario, considere la posibilidad de colocar los recursos de idioma en archivos dll de recursos satélite independientes.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Uso de ensamblados con una interfaz de usuario multilingüe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809361"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a><span data-ttu-id="1ab81-103">Uso de ensamblados con una interfaz de usuario multilingüe</span><span class="sxs-lookup"><span data-stu-id="1ab81-103">Using Assemblies with a Multilanguage User Interface</span></span>

<span data-ttu-id="1ab81-104">Si desea que los usuarios de la aplicación, o el archivo DLL principal, puedan cambiar el idioma de la interfaz de usuario, considere la posibilidad de colocar los recursos de idioma en archivos dll de recursos satélite independientes.</span><span class="sxs-lookup"><span data-stu-id="1ab81-104">If you want users of your application, or core DLL, to be capable of changing the language of the user interface, you should consider placing language resources into separate satellite resource DLLs.</span></span> <span data-ttu-id="1ab81-105">Para obtener más información sobre el uso de archivos dll de recursos satélite, consulte [interfaz de usuario multilingüe (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="1ab81-105">For more information about using satellite resource DLLs, see [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="1ab81-106">Cada archivo DLL satélite contiene los recursos de un idioma diferente.</span><span class="sxs-lookup"><span data-stu-id="1ab81-106">Each satellite DLL contains the resources for a different language.</span></span> <span data-ttu-id="1ab81-107">El archivo DLL principal se puede proporcionar como un ensamblado y cada uno de los archivos dll satélite se puede proporcionar como ensamblados satélite independientes.</span><span class="sxs-lookup"><span data-stu-id="1ab81-107">The core DLL may be provided as an assembly and each of the satellite DLLs may be provided as separate satellite assemblies.</span></span> <span data-ttu-id="1ab81-108">En este caso, cada ensamblado satélite debe tener su propio manifiesto de ensamblado autodescriptivo.</span><span class="sxs-lookup"><span data-stu-id="1ab81-108">In this case, each satellite assembly should have its own self-describing assembly manifest.</span></span> <span data-ttu-id="1ab81-109">El manifiesto del ensamblado satélite no debe describir ninguna dependencia de otros ensamblados.</span><span class="sxs-lookup"><span data-stu-id="1ab81-109">The satellite assembly's manifest should not describe any dependency on other assemblies.</span></span> <span data-ttu-id="1ab81-110">En su lugar, se debe describir cualquier dependencia de ensamblados satélite en otros ensamblados en el manifiesto del ensamblado principal.</span><span class="sxs-lookup"><span data-stu-id="1ab81-110">Any dependency of satellite assemblies on other assemblies should instead be described in the core assembly's manifest.</span></span>

<span data-ttu-id="1ab81-111">La versión de la [interfaz de usuario multilingüe (MUI)](/windows/desktop/Intl/multilingual-user-interface) de Windows permite a los usuarios especificar el idioma de la interfaz de usuario de acuerdo con sus preferencias, siempre que se haya agregado el idioma requerido al sistema.</span><span class="sxs-lookup"><span data-stu-id="1ab81-111">The [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface) version of Windows enables users to specify the user-interface language according to their preferences, provided the required language has been added to the system.</span></span> <span data-ttu-id="1ab81-112">Un ensamblado principal puede admitir varios idiomas mediante el uso de varios ensamblados MUI.</span><span class="sxs-lookup"><span data-stu-id="1ab81-112">A core assembly can support multiple languages by using multiple MUI assemblies.</span></span> <span data-ttu-id="1ab81-113">En este caso, cada ensamblado MUI debe tener su propio manifiesto y todas las dependencias de otros ensamblados deben describirse solo en el manifiesto del ensamblado principal.</span><span class="sxs-lookup"><span data-stu-id="1ab81-113">In this case, each MUI assembly should have its own manifest and any dependencies on other assemblies should only be described in the core assembly's manifest.</span></span>

<span data-ttu-id="1ab81-114">Por ejemplo, Proseware. sample. pop puede ser un ensamblado en paralelo básico que es dependiente del ensamblado Proseware. Research. SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="1ab81-114">For example, Proseware.Sample.Pop may be a core side-by-side assembly which happens to be dependent on the Proseware.Research.SampleAssembly assembly.</span></span> <span data-ttu-id="1ab81-115">Si Proseware. sample. pop usa MUI para admitir varios idiomas, se pueden proporcionar ensamblados MUI independientes para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="1ab81-115">If Proseware.Sample.Pop uses MUI to support multiple languages, separate MUI assemblies can be provided for each language.</span></span> <span data-ttu-id="1ab81-116">Cada ensamblado MUI debe tener su propio manifiesto que describe este archivo DLL de recursos satélite determinado.</span><span class="sxs-lookup"><span data-stu-id="1ab81-116">Each MUI assembly should have its own manifest describing this particular satellite resource DLL.</span></span> <span data-ttu-id="1ab81-117">Los manifiestos de ensamblado de MUI no deben incluir ninguna referencia a las dependencias de otros ensamblados.</span><span class="sxs-lookup"><span data-stu-id="1ab81-117">The MUI assembly manifests should not include any reference to dependencies on other assemblies.</span></span> <span data-ttu-id="1ab81-118">El manifiesto que describe el ensamblado principal, Proseware. sample. pop, debe describir la dependencia de Proseware. sample. pop en el ensamblado Proseware. Research. SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="1ab81-118">The manifest describing the core assembly, Proseware.Sample.Pop, should describe the dependency of Proseware.Sample.Pop on the Proseware.Research.SampleAssembly assembly.</span></span>

<span data-ttu-id="1ab81-119">Los atributos del elemento **assemblyIdentity** de un ensamblado satélite son similares a los del manifiesto del ensamblado base.</span><span class="sxs-lookup"><span data-stu-id="1ab81-119">The attributes of the **assemblyIdentity** element of a satellite assembly are similar to those in the manifest of the base assembly.</span></span> <span data-ttu-id="1ab81-120">El atributo **Name** debe ser el mismo que el ensamblado base con la adición de "Resources".</span><span class="sxs-lookup"><span data-stu-id="1ab81-120">The **name** attribute should be the same as the base assembly with the addition of "Resources."</span></span> <span data-ttu-id="1ab81-121">Por ejemplo, si el nombre es "Proseware. Tools. corrector. Runtime-Libraries" en el ensamblado base, el nombre en el ensamblado de recursos sería "Proseware. Tools. de corrección. Runtime-Libraries. Resources".</span><span class="sxs-lookup"><span data-stu-id="1ab81-121">For example, if the name is "Proseware.Tools.SpellCheck.Runtime-Libraries" in the base assembly, the name in the resource assembly would be "Proseware.Tools.SpellCheck.Runtime-Libraries.Resources."</span></span> <span data-ttu-id="1ab81-122">El atributo **Language** debe identificar el idioma del ensamblado del recurso.</span><span class="sxs-lookup"><span data-stu-id="1ab81-122">The **language** attribute should identify the language of the resource assembly.</span></span> <span data-ttu-id="1ab81-123">El atributo de **archivo** debe incluir la lista de archivos dll de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ab81-123">The **file** attribute should include the list of files that are resource DLLs.</span></span>

<span data-ttu-id="1ab81-124">El siguiente es un ejemplo del manifiesto del ensamblado de los recursos de Proseware. Tools. revisor. Runtime-Libraries.</span><span class="sxs-lookup"><span data-stu-id="1ab81-124">The following is an example of the manifest for Proseware.Tools.SpellCheck.Runtime-Libraries resources assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

<span data-ttu-id="1ab81-125">El ensamblado base describe una dependencia opcional en el ensamblado de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ab81-125">The base assembly describes an optional dependency on the resource assembly.</span></span> <span data-ttu-id="1ab81-126">En este ejemplo, si un usuario ejecuta Windows con la configuración regional designada como alemán, una aplicación que use el ensamblado Proseware. Tools. de ortografía mostraría el texto en alemán.</span><span class="sxs-lookup"><span data-stu-id="1ab81-126">In this example, if a user is running Windows with the locale designated as German, an application using the Proseware.Tools.SpellCheck assembly would display text in German.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
