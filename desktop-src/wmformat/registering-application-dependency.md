---
title: Registro de dependencias de aplicación (Windows Media Format SDK 11)
description: Obtenga información sobre cómo registrar la aplicación con los componentes en tiempo de ejecución de las API proporcionadas por el SDK Windows Media Format 11.
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK, registro de dependencias de aplicación
- registro de dependencias de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd546ee9b162652f00a131e87561a7e34f7e3a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406168"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a><span data-ttu-id="23b94-105">Registro de dependencias de aplicación (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="23b94-105">Registering Application Dependency (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="23b94-106">Las aplicaciones que usan las API proporcionadas por Windows Media Format SDK o Reproductor de Windows Media SDK dependen de los componentes en tiempo de ejecución de esas tecnologías.</span><span class="sxs-lookup"><span data-stu-id="23b94-106">Applications that use APIs provided by the Windows Media Format SDK or Windows Media Player SDK are dependent upon the run-time components of those technologies.</span></span> <span data-ttu-id="23b94-107">Puede registrar la aplicación como dependiente de esos componentes como parte de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23b94-107">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="23b94-108">Al registrar la aplicación, puede elegir uno de los dos niveles de dependencia: bloqueo o dependiente.</span><span class="sxs-lookup"><span data-stu-id="23b94-108">When you register your application, you can choose one of two levels of dependency: blocking, or dependent.</span></span> <span data-ttu-id="23b94-109">Cuando una o varias aplicaciones se registran con una dependencia de bloqueo en uno de los componentes en tiempo de ejecución, se bloqueará el componente de una reversión a una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="23b94-109">When one or more applications are registered with a blocking dependency on one of the run-time components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="23b94-110">Las aplicaciones dependientes que no están registradas como bloqueo, no bloquean la reversión.</span><span class="sxs-lookup"><span data-stu-id="23b94-110">Dependent applications that are not registered as blocking, do not block rollback.</span></span> <span data-ttu-id="23b94-111">En su lugar, antes de realizar la reversión, se le pide al usuario un mensaje que indica que las aplicaciones dependen del componente.</span><span class="sxs-lookup"><span data-stu-id="23b94-111">Instead, before the rollback is performed, the user is prompted with a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="23b94-112">Para registrar la aplicación, debe establecer un valor en el registro que identifique la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23b94-112">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="23b94-113">El valor del Registro que se va a establecer depende del componente del que depende la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23b94-113">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="23b94-114">También puede establecer dos valores adicionales por dependencia para proporcionar información adicional sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23b94-114">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="23b94-115">Los siguientes valores del Registro se usan para registrar la dependencia del entorno de ejecución Windows Media Format SDK:</span><span class="sxs-lookup"><span data-stu-id="23b94-115">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="23b94-116">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="23b94-116">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="23b94-117">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="23b94-117">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="23b94-118">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="23b94-118">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="23b94-119">El siguiente valor del Registro se usa para registrar la dependencia de Reproductor de Windows Media runtime del SDK:</span><span class="sxs-lookup"><span data-stu-id="23b94-119">The following registry value are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="23b94-120">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="23b94-120">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="23b94-121">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="23b94-121">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="23b94-122">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="23b94-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="23b94-123">Las siguientes variables se usan en los valores del Registro enumerados anteriormente:</span><span class="sxs-lookup"><span data-stu-id="23b94-123">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="23b94-124">*TIPO \_ REF*</span><span class="sxs-lookup"><span data-stu-id="23b94-124">*REF\_TYPE*</span></span>

<span data-ttu-id="23b94-125">Reemplace por BlockingRefCounts para bloquear la dependencia o por DependentRefCounts para la dependencia sin bloqueo.</span><span class="sxs-lookup"><span data-stu-id="23b94-125">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="23b94-126">*APP*</span><span class="sxs-lookup"><span data-stu-id="23b94-126">*APP*</span></span>

<span data-ttu-id="23b94-127">Nombre o descriptor corto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23b94-127">Name or short descriptor of your application.</span></span> <span data-ttu-id="23b94-128">Esta cadena no se usará en los mensajes que se muestran para el usuario.</span><span class="sxs-lookup"><span data-stu-id="23b94-128">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="23b94-129">Este valor es el identificador utilizado en los tres valores del Registro asociados a cada uno de los componentes en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="23b94-129">This value is the identifier used in all three registry values associated with each of the run-time components.</span></span>

<span data-ttu-id="23b94-130">*CADENA DE \_ APLICACIÓN*</span><span class="sxs-lookup"><span data-stu-id="23b94-130">*APP\_STRING*</span></span>

<span data-ttu-id="23b94-131">Descriptor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23b94-131">Descriptor of your application.</span></span> <span data-ttu-id="23b94-132">Esta cadena se puede usar en los mensajes que se muestran para el usuario.</span><span class="sxs-lookup"><span data-stu-id="23b94-132">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="23b94-133">*REF \_ DESCRIPTOR*</span><span class="sxs-lookup"><span data-stu-id="23b94-133">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="23b94-134">Descripción de cómo la aplicación usa el componente.</span><span class="sxs-lookup"><span data-stu-id="23b94-134">Description of how your application uses the component.</span></span> <span data-ttu-id="23b94-135">Este valor puede incluir un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="23b94-135">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="23b94-136">*VERSIÓN DE \_ WMP*</span><span class="sxs-lookup"><span data-stu-id="23b94-136">*WMP\_VERSION*</span></span>

<span data-ttu-id="23b94-137">Versión de Reproductor de Windows Media requiere la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23b94-137">Version of Windows Media Player required by your application.</span></span>

<span data-ttu-id="23b94-138">*VERSIÓN DE \_ WMF*</span><span class="sxs-lookup"><span data-stu-id="23b94-138">*WMF\_VERSION*</span></span>

<span data-ttu-id="23b94-139">Versión del SDK Windows Media Format que requiere la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23b94-139">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="23b94-140">Los tres valores del Registro de ejemplo siguientes muestran cómo configurar los valores de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="23b94-140">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="23b94-141">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsConfiguración de \\ \\ MicrosoftMedia DependentRefCounts \\ App, "Southvideo", "Southhkey Video Player"</span><span class="sxs-lookup"><span data-stu-id="23b94-141">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="23b94-142">HKEY CLASSES ROOT Software Microsoft WindowsConfiguración de MicrosoftMedia \_ \_ \\ \\ \\ \\ \\ \\ DescriptorRefCounts, "Southvideo", "Southvideo Video Player usa el SDK de Windows Media Format para reproducir archivos de vídeo".</span><span class="sxs-lookup"><span data-stu-id="23b94-142">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="23b94-143">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Version, "Southvideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="23b94-143">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="23b94-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23b94-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23b94-145">**Consideraciones sobre el proyecto**</span><span class="sxs-lookup"><span data-stu-id="23b94-145">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




