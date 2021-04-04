---
description: Utilice el procedimiento siguiente para desarrollar una nueva aplicación, o actualizar una aplicación existente, para usar los ensamblados en paralelo disponibles de Microsoft u otros publicadores de ensamblados en paralelo.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Usar ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1992562a0868918de2901a7ca88033784af6ef1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907831"
---
# <a name="using-side-by-side-assemblies"></a><span data-ttu-id="3d12c-103">Usar ensamblados en paralelo</span><span class="sxs-lookup"><span data-stu-id="3d12c-103">Using Side-by-side Assemblies</span></span>

<span data-ttu-id="3d12c-104">Utilice el procedimiento siguiente para desarrollar una nueva aplicación, o actualizar una aplicación existente, para usar los [ensamblados en paralelo](about-side-by-side-assemblies-.md) disponibles de Microsoft u otros publicadores de ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="3d12c-104">Use the following procedure to develop a new application, or update an existing application, to use the [side-by-side assemblies](about-side-by-side-assemblies-.md) available from Microsoft or other side-by-side assembly publishers.</span></span> <span data-ttu-id="3d12c-105">Para obtener una lista de los ensamblados en paralelo proporcionados por Microsoft actualmente, consulte [ensamblados en paralelo de Microsoft compatibles](supported-microsoft-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="3d12c-105">For a list of the side-by-side assemblies currently provided by Microsoft, see [Supported Microsoft Side-by-side Assemblies](supported-microsoft-side-by-side-assemblies.md).</span></span> <span data-ttu-id="3d12c-106">Tenga en cuenta que la aplicación debe ejecutarse al menos en Windows XP para instalar los ensamblados como ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="3d12c-106">Note that the application must be run on at least Windows XP to install the assemblies as side-by-side assemblies.</span></span> <span data-ttu-id="3d12c-107">Para obtener más información, vea [instrucciones para crear ensamblados en paralelo](guidelines-for-creating-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="3d12c-107">For more information, see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

<span data-ttu-id="3d12c-108">**Para agregar un ensamblado en paralelo a una aplicación**</span><span class="sxs-lookup"><span data-stu-id="3d12c-108">**To add a side-by-side assembly to an application**</span></span>

1.  <span data-ttu-id="3d12c-109">Identificar los ensamblados en paralelo que requiere la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d12c-109">Identify the side-by-side assemblies that your application requires.</span></span> <span data-ttu-id="3d12c-110">A partir de Windows XP, estos ensamblados en paralelo y sus manifiestos de ensamblado se instalan con el sistema operativo, pero no se registran de forma global.</span><span class="sxs-lookup"><span data-stu-id="3d12c-110">Starting with Windows XP, these side-by-side assemblies and their assembly manifests are installed with the operating system but are not globally registered.</span></span>
2.  <span data-ttu-id="3d12c-111">Use un editor XML para crear un [manifiesto de aplicación](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="3d12c-111">Use an XML editor to create an [application manifest](application-manifests.md).</span></span> <span data-ttu-id="3d12c-112">Vea el siguiente manifiesto de aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3d12c-112">See the example application manifest below.</span></span> <span data-ttu-id="3d12c-113">Para obtener más información, consulte [manifiestos de aplicación](application-manifests.md) en la [referencia de archivos de manifiesto](manifest-files-reference.md).</span><span class="sxs-lookup"><span data-stu-id="3d12c-113">For more information, see [Application Manifests](application-manifests.md) in the [Manifest Files Reference](manifest-files-reference.md).</span></span>
3.  <span data-ttu-id="3d12c-114">Escriba los valores de atributo en el subelemento [*assemblyIdentity del contexto de Def*](d-sbscs-gly.md) del manifiesto de aplicación que define la aplicación de forma única.</span><span class="sxs-lookup"><span data-stu-id="3d12c-114">Enter attribute values in the [*DEF-context assemblyIdentity*](d-sbscs-gly.md) subelement of the application manifest that uniquely defines the application.</span></span> <span data-ttu-id="3d12c-115">Para obtener más información sobre el **assemblyIdentity** de Def-context, consulte [manifiestos de aplicación](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="3d12c-115">For more information about the DEF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>
4.  <span data-ttu-id="3d12c-116">Si el ensamblado contiene ensamblados dependientes, escriba los valores de atributo en los subelementos de [*assemblyIdentity de contexto de referencia*](r-sbscs-gly.md) correspondientes del manifiesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d12c-116">If the assembly contains any dependent assemblies, enter attribute values into the corresponding [*REF-context assemblyIdentity*](r-sbscs-gly.md) subelements of the application manifest.</span></span> <span data-ttu-id="3d12c-117">Para obtener más información sobre el **assemblyIdentity** de referencia, vea [manifiestos de aplicación](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="3d12c-117">For more information about the REF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  <span data-ttu-id="3d12c-118">Puede incluir el manifiesto de aplicación en el archivo de encabezado ejecutable binario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d12c-118">You may include the application manifest in the application's binary executable header file.</span></span>

    <span data-ttu-id="3d12c-119">En este caso, agregue también la siguiente línea al archivo de encabezado de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="3d12c-119">In this case, also add the following line to the application header file:</span></span>

    <dl> <span data-ttu-id="3d12c-120">Manifiesto del manifiesto de CREATEPROCESS ID. de recurso de manifiesto \_ \_ \_ RT \_ "YourApp.exe. manifest"</span><span class="sxs-lookup"><span data-stu-id="3d12c-120">CREATEPROCESS\_MANIFEST\_RESOURCE\_ID RT\_MANIFEST "YourApp.exe.manifest"</span></span>  
    </dl>

    <span data-ttu-id="3d12c-121">Como alternativa, puede colocar un archivo de manifiesto independiente en el mismo directorio que el archivo ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d12c-121">As an alternative, you can place a separate manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="3d12c-122">El sistema operativo carga primero el manifiesto del sistema de archivos y, a continuación, comprueba la sección de recursos del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="3d12c-122">The operating system loads the manifest from the file system first, and then checks the resource section of the executable.</span></span> <span data-ttu-id="3d12c-123">La versión del sistema de archivos tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="3d12c-123">The file system version takes precedence.</span></span>

6.  <span data-ttu-id="3d12c-124">Los [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies) deben instalarse con la versión [Windows Installer](../msi/windows-installer-portal.md) 2,0.</span><span class="sxs-lookup"><span data-stu-id="3d12c-124">[Shared assemblies](/windows/desktop/Msi/shared-assemblies) should be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="3d12c-125">Cree un paquete de Windows Installer como se describe en [¿cómo se instalan los ensamblados Win32 para el uso compartido simultáneo en Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span><span class="sxs-lookup"><span data-stu-id="3d12c-125">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for Side-by-side Sharing on Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span></span>
7.  <span data-ttu-id="3d12c-126">Los [ensamblados privados](/windows/desktop/Msi/private-assemblies) se pueden instalar con la versión [Windows Installer](../msi/windows-installer-portal.md) 2,0.</span><span class="sxs-lookup"><span data-stu-id="3d12c-126">[Private assemblies](/windows/desktop/Msi/private-assemblies) can be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="3d12c-127">Cree un paquete de Windows Installer como se describe en [¿cómo se instalan los ensamblados Win32 para el uso privado de una aplicación en Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span><span class="sxs-lookup"><span data-stu-id="3d12c-127">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for the Private Use of an Application on Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span></span> <span data-ttu-id="3d12c-128">También puede usar cualquier otro instalador para copiar un ensamblado privado y su manifiesto en la misma carpeta que el archivo ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d12c-128">You can also use any other installer to copy a private assembly and its manifest into the same folder as the application's executable file.</span></span>
8.  <span data-ttu-id="3d12c-129">Pruebe la aplicación para garantizar los resultados.</span><span class="sxs-lookup"><span data-stu-id="3d12c-129">Test your application to ensure the results.</span></span> <span data-ttu-id="3d12c-130">Tenga en cuenta que el equipo de prueba no debe tener el ensamblado en paralelo registrado.</span><span class="sxs-lookup"><span data-stu-id="3d12c-130">Note that your test computer should not have the side-by-side assembly registered.</span></span>
9.  <span data-ttu-id="3d12c-131">Implemente la aplicación o actualice como un paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3d12c-131">Deploy your application or update as a Windows Installer package.</span></span>

## <a name="example-application-manifest"></a><span data-ttu-id="3d12c-132">Ejemplo de manifiesto de aplicación</span><span class="sxs-lookup"><span data-stu-id="3d12c-132">Example Application Manifest</span></span>

<span data-ttu-id="3d12c-133">El siguiente es un ejemplo de un manifiesto de aplicación:</span><span class="sxs-lookup"><span data-stu-id="3d12c-133">The following is an example of an application manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
