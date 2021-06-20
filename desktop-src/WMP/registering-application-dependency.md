---
title: Registro de dependencias de aplicación (Reproductor de Windows Media SDK)
description: Obtenga información sobre cómo registrar la aplicación con los componentes en tiempo de ejecución de las API proporcionadas por el SDK Reproductor de Windows Media.
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Reproductor de Windows Media,application dependency registry settings
- Reproductor de Windows Media,configuración del Registro de dependencias
- Reproductor de Windows Media,registry
- registry,application dependency settings
- registro, configuración de dependencia
- registry,settings for Reproductor de Windows Media
- configuración del registro de dependencias
- configuración del registro de dependencias de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b1692c6a4e1a8274472bbe9d718721c1ab4f1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407368"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a><span data-ttu-id="e9e73-111">Registro de dependencias de aplicación (Reproductor de Windows Media SDK)</span><span class="sxs-lookup"><span data-stu-id="e9e73-111">Registering Application Dependency (Windows Media Player SDK)</span></span>

<span data-ttu-id="e9e73-112">Las aplicaciones que usan las API proporcionadas por Reproductor de Windows Media SDK o Windows Media Format SDK dependen de los componentes en tiempo de ejecución de esas tecnologías.</span><span class="sxs-lookup"><span data-stu-id="e9e73-112">Applications that use APIs provided by the Windows Media Player SDK or Windows Media Format SDK are dependent upon the runtime components of those technologies.</span></span> <span data-ttu-id="e9e73-113">Puede registrar la aplicación como dependiente de esos componentes como parte de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e73-113">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="e9e73-114">Al registrar la aplicación, puede elegir uno de estos dos niveles de dependencia: bloqueo o dependiente.</span><span class="sxs-lookup"><span data-stu-id="e9e73-114">When you register your application, you can choose one of two levels of dependency: blocking or dependent.</span></span> <span data-ttu-id="e9e73-115">Cuando se registra una o varias aplicaciones con una dependencia de bloqueo en uno de los componentes en tiempo de ejecución, se bloqueará el componente de una reversión a una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="e9e73-115">When one or more application is registered with a blocking dependency on one of the runtime components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="e9e73-116">Las aplicaciones dependientes que no están registradas como bloqueo no bloquean la reversión.</span><span class="sxs-lookup"><span data-stu-id="e9e73-116">Dependent applications that are not registered as blocking do not block rollback.</span></span> <span data-ttu-id="e9e73-117">En su lugar, antes de realizar la reversión, se muestra al usuario un mensaje que indica que las aplicaciones dependen del componente.</span><span class="sxs-lookup"><span data-stu-id="e9e73-117">Instead, before the rollback is performed, the user is displayed a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="e9e73-118">Para registrar la aplicación, debe establecer un valor en el registro que identifique la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e73-118">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="e9e73-119">El valor del Registro que se va a establecer depende del componente del que depende la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e73-119">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="e9e73-120">También puede establecer dos valores adicionales por dependencia para proporcionar información adicional sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e73-120">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="e9e73-121">Los siguientes valores del Registro se usan para registrar la dependencia en Reproductor de Windows Media runtime del SDK:</span><span class="sxs-lookup"><span data-stu-id="e9e73-121">The following registry values are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="e9e73-122">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="e9e73-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="e9e73-123">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="e9e73-123">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="e9e73-124">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="e9e73-124">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="e9e73-125">Los siguientes valores del Registro se usan para registrar la dependencia en el entorno de ejecución Windows Media Format SDK:</span><span class="sxs-lookup"><span data-stu-id="e9e73-125">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="e9e73-126">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="e9e73-126">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="e9e73-127">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="e9e73-127">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="e9e73-128">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF TYPE \\ \\ *\_ Version,* \\ "*APP*", "*WMF \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="e9e73-128">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="e9e73-129">Las siguientes variables se usan en los valores del Registro enumerados anteriormente:</span><span class="sxs-lookup"><span data-stu-id="e9e73-129">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="e9e73-130">*TIPO \_ REF*</span><span class="sxs-lookup"><span data-stu-id="e9e73-130">*REF\_TYPE*</span></span>

<span data-ttu-id="e9e73-131">Reemplace por BlockingRefCounts para bloquear la dependencia o por DependentRefCounts para la dependencia sin bloqueo.</span><span class="sxs-lookup"><span data-stu-id="e9e73-131">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="e9e73-132">*APP*</span><span class="sxs-lookup"><span data-stu-id="e9e73-132">*APP*</span></span>

<span data-ttu-id="e9e73-133">Nombre o descriptor corto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e73-133">Name or short descriptor of your application.</span></span> <span data-ttu-id="e9e73-134">Esta cadena no se usará en los mensajes que se muestran para el usuario.</span><span class="sxs-lookup"><span data-stu-id="e9e73-134">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="e9e73-135">Este valor es el identificador utilizado en los tres valores del Registro asociados a cada uno de los componentes en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e9e73-135">This value is the identifier used in all three registry values associated with each of the runtime components.</span></span>

<span data-ttu-id="e9e73-136">*CADENA DE \_ APLICACIÓN*</span><span class="sxs-lookup"><span data-stu-id="e9e73-136">*APP\_STRING*</span></span>

<span data-ttu-id="e9e73-137">Descriptor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e73-137">Descriptor of your application.</span></span> <span data-ttu-id="e9e73-138">Esta cadena se puede usar en los mensajes que se muestran para el usuario.</span><span class="sxs-lookup"><span data-stu-id="e9e73-138">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="e9e73-139">*DESCRIPTOR \_ DE REFERENCIA*</span><span class="sxs-lookup"><span data-stu-id="e9e73-139">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="e9e73-140">Descripción de cómo la aplicación usa el componente.</span><span class="sxs-lookup"><span data-stu-id="e9e73-140">Description of how your application uses the component.</span></span> <span data-ttu-id="e9e73-141">Este valor puede incluir un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e9e73-141">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="e9e73-142">*VERSIÓN DE \_ WMP*</span><span class="sxs-lookup"><span data-stu-id="e9e73-142">*WMP\_VERSION*</span></span>

<span data-ttu-id="e9e73-143">Versión de Reproductor de Windows Media requiere la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e73-143">Version of Windows Media Player required by your application.</span></span> <span data-ttu-id="e9e73-144">Si no se especifica ninguna versión, se supone que el valor predeterminado es 9.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="e9e73-144">If no version is specified, the default value is assumed to be 9.0.0.0.</span></span>

<span data-ttu-id="e9e73-145">*VERSIÓN DE \_ WMF*</span><span class="sxs-lookup"><span data-stu-id="e9e73-145">*WMF\_VERSION*</span></span>

<span data-ttu-id="e9e73-146">Versión del SDK Windows Media Format que requiere la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9e73-146">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="e9e73-147">Los tres valores del Registro de ejemplo siguientes muestran cómo configurar los valores de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="e9e73-147">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="e9e73-148">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ App, "Southvideo", "Southplayer Video Player"</span><span class="sxs-lookup"><span data-stu-id="e9e73-148">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="e9e73-149">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ Descriptor, "Southvideo", "Southvideo Player uses the Windows Media Format SDK to play video files".</span><span class="sxs-lookup"><span data-stu-id="e9e73-149">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="e9e73-150">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ Version, "Southvideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="e9e73-150">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9e73-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9e73-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9e73-152">**Configuración del Registro**</span><span class="sxs-lookup"><span data-stu-id="e9e73-152">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




