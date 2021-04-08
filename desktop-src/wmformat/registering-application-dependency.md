---
title: Registrar la dependencia de la aplicación (Windows Media Format 11 SDK)
description: Registrando la dependencia de la aplicación
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- SDK de Windows Media Format, registrar dependencias de aplicaciones
- registrar las dependencias de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090cf61d32597800b52e2bc112d2bee1cc1b7cd7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078678"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a><span data-ttu-id="f0a0c-105">Registrar la dependencia de la aplicación (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="f0a0c-105">Registering Application Dependency (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="f0a0c-106">Las aplicaciones que usan las API proporcionadas por el SDK de Windows Media Format o Windows Media Player SDK dependen de los componentes en tiempo de ejecución de esas tecnologías.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-106">Applications that use APIs provided by the Windows Media Format SDK or Windows Media Player SDK are dependent upon the run-time components of those technologies.</span></span> <span data-ttu-id="f0a0c-107">Puede registrar la aplicación como dependiente de esos componentes como parte de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-107">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="f0a0c-108">Al registrar la aplicación, puede elegir uno de los dos niveles de dependencia: bloqueo o dependiente.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-108">When you register your application, you can choose one of two levels of dependency: blocking, or dependent.</span></span> <span data-ttu-id="f0a0c-109">Cuando una o varias aplicaciones se registran con una dependencia de bloqueo en uno de los componentes de tiempo de ejecución, el componente se bloqueará de una reversión a una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-109">When one or more applications are registered with a blocking dependency on one of the run-time components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="f0a0c-110">Las aplicaciones dependientes que no están registradas como bloqueo, no bloquean la reversión.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-110">Dependent applications that are not registered as blocking, do not block rollback.</span></span> <span data-ttu-id="f0a0c-111">En su lugar, antes de que se lleve a cabo la reversión, se muestra al usuario un mensaje que indica que las aplicaciones dependen del componente.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-111">Instead, before the rollback is performed, the user is prompted with a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="f0a0c-112">Para registrar la aplicación, debe establecer un valor en el registro que identifique la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-112">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="f0a0c-113">El valor del registro que se va a establecer depende del componente del que dependa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-113">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="f0a0c-114">También puede establecer dos valores adicionales por dependencia para proporcionar información adicional sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-114">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="f0a0c-115">Los siguientes valores del registro se utilizan para registrar la dependencia del tiempo de ejecución del SDK de Windows Media Format:</span><span class="sxs-lookup"><span data-stu-id="f0a0c-115">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="f0a0c-116">HKEY \_ classes \_ root \\ software \\ Microsoft \\ windowsmedia \\ setup \\ *ref \_ tipo* \\ de la aplicación, "*aplicación*", "*\_ cadena de aplicación*"</span><span class="sxs-lookup"><span data-stu-id="f0a0c-116">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="f0a0c-117">HKEY \_ classes \_ \\ software raíz \\ Microsoft \\ windowsmedia \\ setup \\ descriptor de *\_ tipo REF* \\ , "*App*", "*ref \_ descriptor*"</span><span class="sxs-lookup"><span data-stu-id="f0a0c-117">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="f0a0c-118">HKEY \_ classes \_ raíz \\ software \\ Microsoft \\ windowsmedia \\ setup \\ *ref \_ Type* \\ version, "*App*", "*WMF \_ version*"</span><span class="sxs-lookup"><span data-stu-id="f0a0c-118">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="f0a0c-119">El siguiente valor del registro se usa para registrar la dependencia del tiempo de ejecución del SDK de Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="f0a0c-119">The following registry value are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="f0a0c-120">HKEY \_ classes \_ raíz \\ software \\ Microsoft \\ MediaPlayer \\ setup \\ *ref \_ tipo* \\ de aplicación, "*aplicación*", "*\_ cadena de aplicación*"</span><span class="sxs-lookup"><span data-stu-id="f0a0c-120">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="f0a0c-121">HKEY \_ clases \_ raíz \\ software \\ Microsoft \\ MediaPlayer \\ configuración \\ *ref \_* \\ descriptor de tipo, "*App*", "*ref \_ descriptor*"</span><span class="sxs-lookup"><span data-stu-id="f0a0c-121">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="f0a0c-122">HKEY \_ classes \_ raíz \\ software \\ Microsoft \\ MediaPlayer \\ setup \\ *ref \_ tipo* \\ version, "*App*", "*WMP \_ version*"</span><span class="sxs-lookup"><span data-stu-id="f0a0c-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="f0a0c-123">Las siguientes variables se usan en los valores del registro enumerados anteriormente:</span><span class="sxs-lookup"><span data-stu-id="f0a0c-123">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="f0a0c-124">*tipo de referencia \_*</span><span class="sxs-lookup"><span data-stu-id="f0a0c-124">*REF\_TYPE*</span></span>

<span data-ttu-id="f0a0c-125">Reemplazar por BlockingRefCounts para la dependencia de bloqueo o con DependentRefCounts para la dependencia sin bloqueo.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-125">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="f0a0c-126">*APP*</span><span class="sxs-lookup"><span data-stu-id="f0a0c-126">*APP*</span></span>

<span data-ttu-id="f0a0c-127">Nombre o descriptor corto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-127">Name or short descriptor of your application.</span></span> <span data-ttu-id="f0a0c-128">Esta cadena no se utilizará en los mensajes mostrados para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-128">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="f0a0c-129">Este valor es el identificador que se usa en los tres valores del registro asociados a cada uno de los componentes en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-129">This value is the identifier used in all three registry values associated with each of the run-time components.</span></span>

<span data-ttu-id="f0a0c-130">*cadena de aplicación \_*</span><span class="sxs-lookup"><span data-stu-id="f0a0c-130">*APP\_STRING*</span></span>

<span data-ttu-id="f0a0c-131">Descriptor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-131">Descriptor of your application.</span></span> <span data-ttu-id="f0a0c-132">Esta cadena se puede usar en los mensajes mostrados para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-132">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="f0a0c-133">*descriptor de referencia \_*</span><span class="sxs-lookup"><span data-stu-id="f0a0c-133">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="f0a0c-134">Descripción del modo en que la aplicación usa el componente.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-134">Description of how your application uses the component.</span></span> <span data-ttu-id="f0a0c-135">Este valor puede incluir un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-135">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="f0a0c-136">*versión de WMP \_*</span><span class="sxs-lookup"><span data-stu-id="f0a0c-136">*WMP\_VERSION*</span></span>

<span data-ttu-id="f0a0c-137">Versión de Windows Media Player requerida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-137">Version of Windows Media Player required by your application.</span></span>

<span data-ttu-id="f0a0c-138">*\_versión WMF*</span><span class="sxs-lookup"><span data-stu-id="f0a0c-138">*WMF\_VERSION*</span></span>

<span data-ttu-id="f0a0c-139">Versión del SDK de Windows Media Format que requiere la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0a0c-139">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="f0a0c-140">En los siguientes tres valores del registro de ejemplo se muestra cómo configurar los valores de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="f0a0c-140">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="f0a0c-141">HKEY \_ classes \_ root \\ software \\ Microsoft \\ windowsmedia \\ setup \\ DependentRefCounts \\ App, "SouthridgeVideo", "Southridge Video Player"</span><span class="sxs-lookup"><span data-stu-id="f0a0c-141">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="f0a0c-142">HKEY \_ classes \_ root \\ software \\ Microsoft \\ windowsmedia \\ setup \\ DependentRefCounts \\ descriptor, "SouthridgeVideo", "Southridge Video Player usa el SDK de Windows Media Format para reproducir archivos de vídeo".</span><span class="sxs-lookup"><span data-stu-id="f0a0c-142">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="f0a0c-143">HKEY \_ classes \_ root \\ software \\ Microsoft \\ windowsmedia \\ setup \\ DependentRefCounts \\ version, "SouthridgeVideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="f0a0c-143">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0a0c-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f0a0c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0a0c-145">**Consideraciones del proyecto**</span><span class="sxs-lookup"><span data-stu-id="f0a0c-145">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




