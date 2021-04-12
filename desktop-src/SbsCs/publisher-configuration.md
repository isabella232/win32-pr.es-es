---
description: Un archivo de configuración de publicador redirige globalmente aplicaciones y ensamblados que dependen de una versión de un ensamblado en paralelo para usar otra versión del mismo ensamblado.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Configuración del publicador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50ceb5263830cb1778aaaede673974cd7faca75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278599"
---
# <a name="publisher-configuration"></a><span data-ttu-id="a9bdc-103">Configuración del publicador</span><span class="sxs-lookup"><span data-stu-id="a9bdc-103">Publisher Configuration</span></span>

<span data-ttu-id="a9bdc-104">Un [archivo de configuración de publicador](publisher-configuration-files.md) redirige globalmente aplicaciones y ensamblados que dependen de una versión de un ensamblado en paralelo para usar otra versión del mismo ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-104">A [publisher configuration file](publisher-configuration-files.md) globally redirects applications and assemblies having a dependence on one version of a side-by-side assembly to use another version of the same assembly.</span></span> <span data-ttu-id="a9bdc-105">Esto permite a las aplicaciones y ensamblados usar el ensamblado actualizado sin tener que volver a generar todas las aplicaciones afectadas.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-105">This enables applications and assemblies to use the updated assembly without having to rebuild all of the affected applications.</span></span>

<span data-ttu-id="a9bdc-106">El publicador de un ensamblado puede proporcionar [archivos de configuración del publicador](publisher-configuration-files.md) al emitir una nueva versión del ensamblado con correcciones de errores o actualizaciones de seguridad compatibles.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-106">[Publisher configuration files](publisher-configuration-files.md) may be provided by the publisher of an assembly when issuing a new version of the assembly with compatible bug fixes or security updates.</span></span> <span data-ttu-id="a9bdc-107">La versión actualizada debe ser totalmente compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-107">The updated version should be fully backward compatible.</span></span> <span data-ttu-id="a9bdc-108">Nunca se debe usar un archivo de configuración de publicador para agregar nuevas características a menos que la actualización sea totalmente compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-108">A publisher configuration file should never be used to add new features unless the update is fully backward compatible.</span></span> <span data-ttu-id="a9bdc-109">Los archivos de configuración del publicador nunca deben usarse para incrementar la versión principal o secundaria de un ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-109">Publisher configuration files should never be used to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="a9bdc-110">Por ejemplo, no redirija la versión de ensamblado 6.0.0.0 a 7.0.0.0 o a 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-110">For example, do not redirect assembly version 6.0.0.0 to 7.0.0.0 or to 6.1.0.0.</span></span>

<span data-ttu-id="a9bdc-111">Los archivos de configuración del publicador solo deben ser emitidos por el publicador del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-111">Publisher configuration files should only be issued by the publisher of the assembly.</span></span> <span data-ttu-id="a9bdc-112">Los desarrolladores de ensamblados deben firmar los ensamblados en paralelo y los archivos de configuración del publicador compartidos.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-112">Assembly developers should sign shared side-by-side assemblies and publisher configuration files.</span></span> <span data-ttu-id="a9bdc-113">Use la misma clave para firmar el ensamblado y los archivos de configuración del publicador asociados.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-113">Use the same key to sign the assembly and the associated publisher configuration files.</span></span> <span data-ttu-id="a9bdc-114">Los archivos de configuración del publicador deben firmarse con las mismas herramientas que se usan para los ensamblados, vea [ejemplo de firma de ensamblados](assembly-signing-example.md) y [crear archivos y catálogos firmados](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="a9bdc-114">Publisher configuration files should be signed using the same tools as used for assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

<span data-ttu-id="a9bdc-115">Normalmente, la nueva versión de un ensamblado y el archivo de configuración del publicador asociado se instalarán en una actualización de Service Pack.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-115">Typically, the new version of an assembly and the associated publisher configuration file will be installed in a service pack update.</span></span> <span data-ttu-id="a9bdc-116">Los archivos de configuración del publicador nunca deben proporcionarse con las aplicaciones como un redistribuible porque la instalación de un archivo de configuración del publicador redirige globalmente los ensamblados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-116">Publisher configuration files should never be provided with applications as a redistributable because installing a publisher configuration file globally redirects assemblies on the system.</span></span> <span data-ttu-id="a9bdc-117">Si el ensamblado que se está actualizando se proporciona como un redistribuible, el publicador debe proporcionar los dos elementos siguientes.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-117">If the assembly being updated is provided as a redistributable, the publisher should provide both of the following.</span></span>

-   <span data-ttu-id="a9bdc-118">Un paquete de Windows Installer (archivo. msi) que incluye la nueva versión del ensamblado con la configuración del publicador.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-118">A Windows Installer package (.msi file) that includes the new version of the assembly with publisher configuration.</span></span> <span data-ttu-id="a9bdc-119">Esto puede instalarse como un Service Pack o QFE porque, en este caso, el cliente ha elegido actualizar globalmente el sistema.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-119">This may be installed as a service pack or QFE because in this case the customer has chosen to globally update the system.</span></span> <span data-ttu-id="a9bdc-120">Las aplicaciones nunca deben instalar esta versión del paquete.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-120">This version of the package should never be installed by applications.</span></span>
-   <span data-ttu-id="a9bdc-121">Un módulo de combinación de Windows Installer (archivo. MSM) que solo incluye la nueva versión del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-121">A Windows Installer merge module (.msm file) that only includes the new version of the assembly.</span></span> <span data-ttu-id="a9bdc-122">Esta versión se puede incluir en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-122">This version may be included with applications.</span></span>

<span data-ttu-id="a9bdc-123">Las aplicaciones que requieren una versión mínima del ensamblado deben indicar su dependencia en la versión mínima; si la versión mínima no está disponible en un sistema, la aplicación no se iniciará.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-123">Applications requiring a minimum version of the assembly should state their dependency on the minimum version, if the minimum version is unavailable on a system then the application will fail to start.</span></span> <span data-ttu-id="a9bdc-124">Si está disponible como redistribuible, debe incluirse en la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-124">If it is available as a redistributable then it should be included in the application setup.</span></span>

<span data-ttu-id="a9bdc-125">Por ejemplo, al instalar el siguiente [archivo de configuración de publicador](publisher-configuration-files.md) , se redirige el enlace desde la versión 2.0.0.0 de Microsoft. Windows. SampleAssembly a la versión 2.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-125">For example, installing the following [publisher configuration file](publisher-configuration-files.md) redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.1.0.</span></span> <span data-ttu-id="a9bdc-126">Esto agrega una nueva Directiva, denominada 1.1.0.0. Policy, en% systemDrive% \\ Windows \\ WinSxS \\ Policies \\ x86 \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*>.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-126">This adds a new policy, named 1.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="1.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

<span data-ttu-id="a9bdc-127">La instalación del siguiente archivo de configuración de publicador para el mismo ensamblado redirige el enlace de la versión 2.0.0.0 de Microsoft. Windows. SampleAssembly a la versión 2.0.3.0.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-127">Installing the following publisher configuration file for the same assembly redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.3.0.</span></span> <span data-ttu-id="a9bdc-128">Esto agrega otra directiva, denominada 2.1.0.0. Policy, en% systemDrive% \\ Windows \\ WinSxS \\ Policies \\ x86 \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*>.</span><span class="sxs-lookup"><span data-stu-id="a9bdc-128">This adds another policy, named 2.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="2.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.3.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

 

 



