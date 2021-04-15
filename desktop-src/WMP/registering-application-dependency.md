---
title: Registrar la dependencia de la aplicación (SDK de Windows Media Player)
description: Registrando la dependencia de la aplicación
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player, configuración del registro de dependencia de la aplicación
- Windows Media Player, configuración del registro de dependencias
- Media Player de Windows, registro
- registro, configuración de dependencia de la aplicación
- registro, configuración de dependencia
- registro, configuración para Windows Media Player
- configuración del registro de dependencias
- configuración del registro de dependencia de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67aac78417f5ec8e4347b97a5c2b5f37db20183e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488878"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a><span data-ttu-id="4831b-111">Registrar la dependencia de la aplicación (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="4831b-111">Registering Application Dependency (Windows Media Player SDK)</span></span>

<span data-ttu-id="4831b-112">Las aplicaciones que usan las API proporcionadas por el SDK de Windows Media Player o el SDK de Windows Media Format dependen de los componentes en tiempo de ejecución de esas tecnologías.</span><span class="sxs-lookup"><span data-stu-id="4831b-112">Applications that use APIs provided by the Windows Media Player SDK or Windows Media Format SDK are dependent upon the runtime components of those technologies.</span></span> <span data-ttu-id="4831b-113">Puede registrar la aplicación como dependiente de esos componentes como parte de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4831b-113">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="4831b-114">Al registrar la aplicación, puede elegir uno de los dos niveles de dependencia: bloqueo o dependiente.</span><span class="sxs-lookup"><span data-stu-id="4831b-114">When you register your application, you can choose one of two levels of dependency: blocking or dependent.</span></span> <span data-ttu-id="4831b-115">Cuando una o más aplicaciones se registran con una dependencia de bloqueo en uno de los componentes de tiempo de ejecución, el componente se bloqueará de una reversión a una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="4831b-115">When one or more application is registered with a blocking dependency on one of the runtime components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="4831b-116">Las aplicaciones dependientes que no están registradas como bloqueo no bloquean la reversión.</span><span class="sxs-lookup"><span data-stu-id="4831b-116">Dependent applications that are not registered as blocking do not block rollback.</span></span> <span data-ttu-id="4831b-117">En su lugar, antes de que se lleve a cabo la reversión, se muestra al usuario un mensaje que indica que las aplicaciones dependen del componente.</span><span class="sxs-lookup"><span data-stu-id="4831b-117">Instead, before the rollback is performed, the user is displayed a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="4831b-118">Para registrar la aplicación, debe establecer un valor en el registro que identifique la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4831b-118">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="4831b-119">El valor del registro que se va a establecer depende del componente del que dependa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4831b-119">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="4831b-120">También puede establecer dos valores adicionales por dependencia para proporcionar información adicional sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4831b-120">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="4831b-121">Los siguientes valores del registro se usan para registrar la dependencia del tiempo de ejecución del SDK de Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="4831b-121">The following registry values are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="4831b-122">HKEY \_ classes \_ raíz \\ software \\ Microsoft \\ MediaPlayer \\ setup \\ *ref \_ tipo* \\ de aplicación, "*aplicación*", "*\_ cadena de aplicación*"</span><span class="sxs-lookup"><span data-stu-id="4831b-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="4831b-123">HKEY \_ clases \_ raíz \\ software \\ Microsoft \\ MediaPlayer \\ configuración \\ *ref \_* \\ descriptor de tipo, "*App*", "*ref \_ descriptor*"</span><span class="sxs-lookup"><span data-stu-id="4831b-123">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="4831b-124">HKEY \_ classes \_ raíz \\ software \\ Microsoft \\ MediaPlayer \\ setup \\ *ref \_ tipo* \\ version, "*App*", "*WMP \_ version*"</span><span class="sxs-lookup"><span data-stu-id="4831b-124">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="4831b-125">Los siguientes valores del registro se utilizan para registrar la dependencia del tiempo de ejecución del SDK de Windows Media Format:</span><span class="sxs-lookup"><span data-stu-id="4831b-125">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="4831b-126">HKEY \_ classes \_ root \\ software \\ Microsoft \\ windowsmedia \\ setup \\ *ref \_ tipo* \\ de la aplicación, "*aplicación*", "*\_ cadena de aplicación*"</span><span class="sxs-lookup"><span data-stu-id="4831b-126">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="4831b-127">HKEY \_ classes \_ \\ software raíz \\ Microsoft \\ windowsmedia \\ setup \\ descriptor de *\_ tipo REF* \\ , "*App*", "*ref \_ descriptor*"</span><span class="sxs-lookup"><span data-stu-id="4831b-127">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="4831b-128">HKEY \_ classes \_ raíz \\ software \\ Microsoft \\ windowsmedia \\ setup \\ *ref \_ Type* \\ version, "*App*", "*WMF \_ version*"</span><span class="sxs-lookup"><span data-stu-id="4831b-128">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="4831b-129">Las siguientes variables se usan en los valores del registro enumerados anteriormente:</span><span class="sxs-lookup"><span data-stu-id="4831b-129">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="4831b-130">*tipo de referencia \_*</span><span class="sxs-lookup"><span data-stu-id="4831b-130">*REF\_TYPE*</span></span>

<span data-ttu-id="4831b-131">Reemplazar por BlockingRefCounts para la dependencia de bloqueo o con DependentRefCounts para la dependencia sin bloqueo.</span><span class="sxs-lookup"><span data-stu-id="4831b-131">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="4831b-132">*APP*</span><span class="sxs-lookup"><span data-stu-id="4831b-132">*APP*</span></span>

<span data-ttu-id="4831b-133">Nombre o descriptor corto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4831b-133">Name or short descriptor of your application.</span></span> <span data-ttu-id="4831b-134">Esta cadena no se utilizará en los mensajes mostrados para el usuario.</span><span class="sxs-lookup"><span data-stu-id="4831b-134">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="4831b-135">Este valor es el identificador que se usa en los tres valores del registro asociados a cada uno de los componentes en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4831b-135">This value is the identifier used in all three registry values associated with each of the runtime components.</span></span>

<span data-ttu-id="4831b-136">*cadena de aplicación \_*</span><span class="sxs-lookup"><span data-stu-id="4831b-136">*APP\_STRING*</span></span>

<span data-ttu-id="4831b-137">Descriptor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4831b-137">Descriptor of your application.</span></span> <span data-ttu-id="4831b-138">Esta cadena se puede usar en los mensajes mostrados para el usuario.</span><span class="sxs-lookup"><span data-stu-id="4831b-138">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="4831b-139">*descriptor de referencia \_*</span><span class="sxs-lookup"><span data-stu-id="4831b-139">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="4831b-140">Descripción del modo en que la aplicación usa el componente.</span><span class="sxs-lookup"><span data-stu-id="4831b-140">Description of how your application uses the component.</span></span> <span data-ttu-id="4831b-141">Este valor puede incluir un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4831b-141">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="4831b-142">*versión de WMP \_*</span><span class="sxs-lookup"><span data-stu-id="4831b-142">*WMP\_VERSION*</span></span>

<span data-ttu-id="4831b-143">Versión de Windows Media Player requerida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4831b-143">Version of Windows Media Player required by your application.</span></span> <span data-ttu-id="4831b-144">Si no se especifica ninguna versión, se supone que el valor predeterminado es 9.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="4831b-144">If no version is specified, the default value is assumed to be 9.0.0.0.</span></span>

<span data-ttu-id="4831b-145">*\_versión WMF*</span><span class="sxs-lookup"><span data-stu-id="4831b-145">*WMF\_VERSION*</span></span>

<span data-ttu-id="4831b-146">Versión del SDK de Windows Media Format que requiere la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4831b-146">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="4831b-147">En los siguientes tres valores del registro de ejemplo se muestra cómo configurar los valores de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="4831b-147">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="4831b-148">HKEY \_ classes \_ root \\ software \\ Microsoft \\ MediaPlayer \\ setup \\ DependentRefCounts \\ App, "SouthridgeVideo", "Southridge Video Player"</span><span class="sxs-lookup"><span data-stu-id="4831b-148">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="4831b-149">HKEY \_ classes \_ root \\ software \\ Microsoft \\ MediaPlayer \\ setup \\ DependentRefCounts \\ descriptor, "SouthridgeVideo", "Southridge Video Player usa el SDK de Windows Media Format para reproducir archivos de vídeo".</span><span class="sxs-lookup"><span data-stu-id="4831b-149">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="4831b-150">HKEY \_ classes \_ root \\ software \\ Microsoft \\ MediaPlayer \\ setup \\ DependentRefCounts \\ version, "SouthridgeVideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="4831b-150">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="4831b-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4831b-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4831b-152">**Configuración del registro**</span><span class="sxs-lookup"><span data-stu-id="4831b-152">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




