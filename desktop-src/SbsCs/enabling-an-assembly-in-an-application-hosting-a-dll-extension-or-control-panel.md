---
description: Si la aplicación hospeda un archivo DLL, una extensión, un complemento o un panel de control de terceros, es posible que desee habilitar un ensamblado en la aplicación&\# 8212; sin habilitar también este ensamblado para los componentes hospedados.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Habilitar un ensamblado en una aplicación que hospeda un archivo DLL, una extensión o un panel de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b04dd19b18c2cdce4783be47333b9afe53dd1ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648429"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a><span data-ttu-id="66cf3-103">Habilitar un ensamblado en una aplicación que hospeda un archivo DLL, una extensión o un panel de control</span><span class="sxs-lookup"><span data-stu-id="66cf3-103">Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel</span></span>

<span data-ttu-id="66cf3-104">Si la aplicación hospeda un archivo DLL, una extensión, un complemento o un panel de control de terceros, es posible que desee habilitar un ensamblado en la aplicación, sin habilitar también este ensamblado para los componentes hospedados.</span><span class="sxs-lookup"><span data-stu-id="66cf3-104">If your application hosts a third-party DLL, extension, plug-in, or control panel, you may want to enable an assembly in your application—without also enabling this assembly for the hosted components.</span></span> <span data-ttu-id="66cf3-105">Este puede ser el caso cuando un componente hospedado requiere cambios en el código para usar el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="66cf3-105">This can be the case when a hosted component requires code changes to use the assembly.</span></span> <span data-ttu-id="66cf3-106">Como desarrollador de la aplicación, es posible que no pueda realizar cambios en estos componentes de terceros.</span><span class="sxs-lookup"><span data-stu-id="66cf3-106">As the application developer, you may be unable to make changes to these third-party components.</span></span> <span data-ttu-id="66cf3-107">En este caso, debe seguir el procedimiento descrito en esta sección para que la aplicación pueda utilizar el ensamblado sin que afecte a los componentes hospedados.</span><span class="sxs-lookup"><span data-stu-id="66cf3-107">In this case, you should follow the procedure described in this section so that your application can use the assembly without affecting the hosted components.</span></span>

-   <span data-ttu-id="66cf3-108">Para habilitar un ensamblado en una aplicación sin afectar a los archivos dll, extensiones, complementos o paneles de control hospedados, se debe incluir en la aplicación como un recurso un manifiesto que describa la dependencia de la aplicación en el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="66cf3-108">To enable an assembly in an application without affecting any hosted DLLs, extensions, plug-ins, or control panels, a manifest that describes the application's dependence on the assembly should be included in the application as a resource.</span></span> <span data-ttu-id="66cf3-109">Los componentes hospedados que no se habilitan con el ensamblado no deben incluir manifiestos que describan esta dependencia.</span><span class="sxs-lookup"><span data-stu-id="66cf3-109">The hosted components that are not being enabled with the assembly should not include manifests describing this dependency.</span></span>
-   <span data-ttu-id="66cf3-110">Para habilitar un ensamblado en una aplicación y sus archivos dll, extensiones, complementos o paneles de control hospedados, incluya manifiestos como recursos tanto en la aplicación como en sus componentes hospedados.</span><span class="sxs-lookup"><span data-stu-id="66cf3-110">To enable an assembly in an application and its hosted DLLs, extensions, plug-ins, or control panels, include manifests as resources in both the application and its hosted components.</span></span> <span data-ttu-id="66cf3-111">Los manifiestos incluidos en la aplicación y en los componentes hospedados deben describir una dependencia en el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="66cf3-111">The manifests included in the application and in the hosted components should each describe a dependence on the assembly.</span></span> <span data-ttu-id="66cf3-112">Normalmente, el desarrollador de la aplicación agrega un manifiesto a la aplicación y el desarrollador del componente hospedado agrega un manifiesto al archivo DLL, la extensión, el complemento o el panel de control.</span><span class="sxs-lookup"><span data-stu-id="66cf3-112">Typically, the application developer adds a manifest to the application and the hosted component developer adds a manifest to the DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="66cf3-113">El método siguiente se puede usar para agregar un manifiesto a una aplicación o un componente hospedado que sea un archivo DLL, una extensión, un complemento o un panel de control.</span><span class="sxs-lookup"><span data-stu-id="66cf3-113">The following method can be used to add a manifest to an application or a hosted component that is a DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="66cf3-114">**Para habilitar un ensamblado en una aplicación o componente hospedado.**</span><span class="sxs-lookup"><span data-stu-id="66cf3-114">**To enable an assembly in an application or hosted component.**</span></span>

1.  <span data-ttu-id="66cf3-115">Cree un manifiesto que describa la dependencia de la aplicación o extensión en el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="66cf3-115">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="66cf3-116">Por ejemplo, el manifiesto de "YourApplication" se puede crear copiando el siguiente manifiesto de ejemplo y sustituyendo los valores correctos para **assemblyIdentity**, **processorArchitecture** y **Description**.</span><span class="sxs-lookup"><span data-stu-id="66cf3-116">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="66cf3-117">Establezca el valor de **processorArchitecture** en x86 si se compila en una plataforma de 32 bits y en IA64 si se compila en una plataforma de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="66cf3-117">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="66cf3-118">El elemento **Description** contiene una descripción de la opción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="66cf3-118">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="66cf3-119">Para obtener más información sobre el formato de manifiesto, consulte [manifiestos de aplicación](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="66cf3-119">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

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

2.  <span data-ttu-id="66cf3-120">Cree un recurso en la aplicación o la extensión de tipo RT \_ manifest ID 2.</span><span class="sxs-lookup"><span data-stu-id="66cf3-120">Create a resource in the application or extension of type RT\_MANIFEST id 2.</span></span>

    <span data-ttu-id="66cf3-121">Por ejemplo, si el nombre de la aplicación es outName, la aplicación debe contener lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="66cf3-121">For example, if the application's name is YourApp, the application should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  <span data-ttu-id="66cf3-122">Compile la aplicación con la marca-DISOLATION \_ compatible \_ habilitada o inserte esta instrucción antes de la \# instrucción include "Windows. h".</span><span class="sxs-lookup"><span data-stu-id="66cf3-122">Compile the application with the -DISOLATION\_AWARE\_ENABLED flag, or insert this statement before the \#include "Windows.h" statement.</span></span> <span data-ttu-id="66cf3-123">En el caso de una aplicación con varios módulos, \_ se requiere la marca-DISOLATION compatible \_ habilitada en todos los módulos.</span><span class="sxs-lookup"><span data-stu-id="66cf3-123">In the case of an application with multiple modules, the -DISOLATION\_AWARE\_ENABLED flag is required on all modules.</span></span>

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  <span data-ttu-id="66cf3-124">Pruebe para asegurarse de que los ensamblados utilizados por la aplicación funcionan correctamente en la aplicación y en el componente hospedado.</span><span class="sxs-lookup"><span data-stu-id="66cf3-124">Test to ensure that assemblies that are used by the application work correctly in the application and hosted component.</span></span>

<span data-ttu-id="66cf3-125">Para obtener más información sobre cómo agregar un ensamblado a aplicaciones sin extensiones, vea [habilitar un ensamblado en una aplicación sin extensiones](enabling-an-assembly-in-an-application-without-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="66cf3-125">For more information about adding an assembly to applications without extensions, see [Enabling an Assembly in an Application Without Extensions](enabling-an-assembly-in-an-application-without-extensions.md).</span></span>

 

 



