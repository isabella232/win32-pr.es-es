---
description: Si la aplicación no hospeda un archivo DLL, una extensión, un complemento o un panel de control, puede usar el método descrito en esta sección para habilitar un ensamblado para la aplicación.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Habilitar un ensamblado en una aplicación sin extensiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1bbcfe510f5a3cdbce323f01cb9342ce236c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653033"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a><span data-ttu-id="e2dbe-103">Habilitar un ensamblado en una aplicación sin extensiones</span><span class="sxs-lookup"><span data-stu-id="e2dbe-103">Enabling an Assembly in an Application Without Extensions</span></span>

<span data-ttu-id="e2dbe-104">Si la aplicación no hospeda un archivo DLL, una extensión, un complemento o un panel de control, puede usar el método descrito en esta sección para habilitar un ensamblado para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-104">If your application does not host a DLL, extension, plug-in, or control panel, you can use the method described in this section to enable an assembly for your application.</span></span> <span data-ttu-id="e2dbe-105">Para obtener más información sobre cómo agregar un ensamblado a las aplicaciones con extensiones, vea [habilitar un ensamblado en una aplicación que hospeda un archivo dll, una extensión o un panel de control](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span><span class="sxs-lookup"><span data-stu-id="e2dbe-105">For more information about adding an assembly to applications with extensions, see [Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span></span>

<span data-ttu-id="e2dbe-106">**Para habilitar un ensamblado en una aplicación sin componentes hospedados**</span><span class="sxs-lookup"><span data-stu-id="e2dbe-106">**To enable an assembly in an application without any hosted components**</span></span>

1.  <span data-ttu-id="e2dbe-107">Cree un manifiesto que describa la dependencia de la aplicación o extensión en el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-107">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="e2dbe-108">Por ejemplo, el manifiesto de "YourApplication" se puede crear copiando el siguiente manifiesto de ejemplo y sustituyendo los valores correctos para **assemblyIdentity**, **processorArchitecture** y **Description**.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-108">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="e2dbe-109">Establezca el valor de **processorArchitecture** en x86 si se compila en una plataforma de 32 bits y en IA64 si se compila en una plataforma de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-109">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform, and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="e2dbe-110">El elemento **Description** contiene una descripción de la opción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-110">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="e2dbe-111">Para obtener más información sobre el formato de manifiesto, consulte [manifiestos de aplicación](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="e2dbe-111">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  <span data-ttu-id="e2dbe-112">Agregue el manifiesto a la aplicación como un recurso en el archivo de encabezado ejecutable binario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-112">Add the manifest to the application as a resource in the application's binary executable header file.</span></span> <span data-ttu-id="e2dbe-113">No se recomienda agregar el manifiesto a la aplicación como un archivo de manifiesto externo.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-113">It is not recommended that you add the manifest to the application as an external manifest file.</span></span>

    <span data-ttu-id="e2dbe-114">Para agregar el manifiesto como un recurso, cree un recurso en la aplicación de tipo RT \_ manifest ID 1.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-114">To add the manifest as a resource, create a resource in the application of type RT\_MANIFEST id 1.</span></span> <span data-ttu-id="e2dbe-115">Por ejemplo, si el nombre de la aplicación es sufile, el archivo de encabezado de la aplicación debe contener lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e2dbe-115">For example, if the application's name is YourApp, the application's header file should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    <span data-ttu-id="e2dbe-116">Si en su lugar agrega el manifiesto como un archivo de manifiesto externo, asegúrese de que la instalación copie el archivo de manifiesto en la carpeta que contiene el archivo ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-116">If you instead add the manifest as an external manifest file, be sure that the installation copies the manifest file into the folder containing the application's executable file.</span></span>

3.  <span data-ttu-id="e2dbe-117">Pruebe para asegurarse de que los ensamblados utilizados por la aplicación funcionan correctamente en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-117">Test to ensure that assemblies used by the application work correctly in the application.</span></span>

 

 



