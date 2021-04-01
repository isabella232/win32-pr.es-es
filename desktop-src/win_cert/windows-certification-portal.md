---
title: Certifique su aplicación de escritorio
description: Siga estos pasos para obtener la certificación de su aplicación de escritorio para Windows 7, Windows 8, Windows 8.1 y Windows 10. Si quiere convertir la aplicación de escritorio para que sea compatible con el Plataforma universal de Windows y la tienda Windows, usará el puente de escritorio de Windows, en cuyo caso debe seguir los pasos de la guía de puente de Desktop para obtener información sobre los pasos de certificación. Si va a desarrollar y certificar una aplicación para UWP desde el principio, consulte la guía de certificación de aplicaciones de Windows en UWP para obtener información sobre la certificación.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797068"
---
# <a name="certify-your-desktop-application"></a><span data-ttu-id="23484-103">Certifique su aplicación de escritorio</span><span class="sxs-lookup"><span data-stu-id="23484-103">Certify your desktop application</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23484-104">La certificación para las aplicaciones de escritorio de Win32 está en [desuso](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span><span class="sxs-lookup"><span data-stu-id="23484-104">Certification for Win32 desktop apps is [deprecated](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span></span> <span data-ttu-id="23484-105">En su lugar, [envíe los archivos aquí](https://www.microsoft.com/wdsi/filesubmission/).</span><span class="sxs-lookup"><span data-stu-id="23484-105">Instead, [submit files here](https://www.microsoft.com/wdsi/filesubmission/).</span></span>

<span data-ttu-id="23484-106">Siga estos pasos para obtener la certificación de su aplicación de escritorio para Windows 7, Windows 8, Windows 8.1 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="23484-106">Follow these steps to get your desktop app certified for Windows 7, Windows 8, Windows 8.1, and Windows 10.</span></span>

<span data-ttu-id="23484-107">Si quiere convertir la aplicación de escritorio para que sea compatible con el Plataforma universal de Windows y la tienda Windows, usará el [puente de escritorio de Windows](https://developer.microsoft.com/windows/bridges/desktop), en cuyo caso debe seguir los pasos de la guía de puente de [Desktop](/windows/uwp/porting/desktop-to-uwp-root) para obtener información sobre los pasos de certificación.</span><span class="sxs-lookup"><span data-stu-id="23484-107">If you wish to convert your desktop app to be compatible with the Universal Windows Platform and Windows Store, you will use the [Windows Desktop Bridge](https://developer.microsoft.com/windows/bridges/desktop), in which case you should follow the [Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root) guidance for certification steps.</span></span>

<span data-ttu-id="23484-108">Si va a desarrollar y certificar una aplicación para UWP desde el principio, consulte la [Guía de certificación de aplicaciones de Windows en UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) para obtener información sobre la certificación.</span><span class="sxs-lookup"><span data-stu-id="23484-108">If you are developing and certifying a UWP app from the start, see [Guidance for Windows App Certification in UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) for info on certification.</span></span>

## <a name="step-1-prepare-for-certification"></a><span data-ttu-id="23484-109">Paso 1: preparación para la certificación</span><span class="sxs-lookup"><span data-stu-id="23484-109">Step 1: Prepare for certification</span></span>



| <span data-ttu-id="23484-110">Tema</span><span class="sxs-lookup"><span data-stu-id="23484-110">Topic</span></span>                                                                                       | <span data-ttu-id="23484-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="23484-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23484-112">¿Cuáles son las ventajas?</span><span class="sxs-lookup"><span data-stu-id="23484-112">What are the benefits?</span></span>](what-are-the-benefits-.md)<br/>                             | <span data-ttu-id="23484-113">La certificación de su aplicación de escritorio proporciona varias ventajas a usted y a sus clientes.</span><span class="sxs-lookup"><span data-stu-id="23484-113">Certifying your desktop app provides several benefits for you and your customers.</span></span>              |
| [<span data-ttu-id="23484-114">Lea los requisitos</span><span class="sxs-lookup"><span data-stu-id="23484-114">Read the requirements</span></span>](certification-requirements-for-windows-desktop-apps.md)<br/> | <span data-ttu-id="23484-115">Revise los requisitos técnicos y las calificaciones de elegibilidad que una aplicación de escritorio debe cumplir.</span><span class="sxs-lookup"><span data-stu-id="23484-115">Review the technical requirements and eligibility qualifications that a desktop app must meet.</span></span> |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a><span data-ttu-id="23484-116">Paso 2: probar la aplicación con el kit de certificación de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="23484-116">Step 2: Test your app with the Windows App Certification Kit</span></span>



| <span data-ttu-id="23484-117">Tema</span><span class="sxs-lookup"><span data-stu-id="23484-117">Topic</span></span>                                                          | <span data-ttu-id="23484-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="23484-118">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23484-119">Obtener el kit</span><span class="sxs-lookup"><span data-stu-id="23484-119">Get the Kit</span></span>](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | <span data-ttu-id="23484-120">Para certificar la aplicación, tiene que instalar y ejecutar el kit de certificación de aplicaciones de Windows (incluido en el Windows SDK).</span><span class="sxs-lookup"><span data-stu-id="23484-120">To certify your app, you have to install and run the Windows App Certification Kit (included in the Windows SDK).</span></span>                                                                     |
| [<span data-ttu-id="23484-121">Uso del kit</span><span class="sxs-lookup"><span data-stu-id="23484-121">Using the Kit</span></span>](using-the-windows-app-certification-kit.md)   | <span data-ttu-id="23484-122">Antes de enviar la aplicación, debe probarla para su preparación.</span><span class="sxs-lookup"><span data-stu-id="23484-122">Before you can submit your app, you must test it for readiness.</span></span> <span data-ttu-id="23484-123">También puede descargar una copia de las notas del [producto de certificación](https://www.microsoft.com/download/details.aspx?id=27414)de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23484-123">You can also download a copy of the [app certification white paper](https://www.microsoft.com/download/details.aspx?id=27414).</span></span> |
| [<span data-ttu-id="23484-124">Revisar los detalles de la prueba</span><span class="sxs-lookup"><span data-stu-id="23484-124">Review test details</span></span>](windows-app-certification-kit-tests.md) | <span data-ttu-id="23484-125">Obtenga la lista de las pruebas que la aplicación debe pasar para que sea apta para la compatibilidad con el sistema operativo Windows más reciente.</span><span class="sxs-lookup"><span data-stu-id="23484-125">Get the list of the tests your app needs to pass to qualify for compatibility with the latest Windows operating system.</span></span>                                                               |



 

<span data-ttu-id="23484-126">Nota: los controladores de filtro también deben pasar el [Kit de certificación de hardware](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span><span class="sxs-lookup"><span data-stu-id="23484-126">Note: Filter drivers must also pass the [Hardware Certification Kit](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span></span> <span data-ttu-id="23484-127">(Consulte [requisitos de certificación para aplicaciones de escritorio de Windows, sección 6,2](certification-requirements-for-windows-desktop-apps.md)).</span><span class="sxs-lookup"><span data-stu-id="23484-127">(See [Certification requirements for Windows desktop apps, section 6.2](certification-requirements-for-windows-desktop-apps.md).)</span></span>

## <a name="step-3-use-the-windows-certification-dashboard"></a><span data-ttu-id="23484-128">Paso 3: uso del panel de certificación de Windows</span><span class="sxs-lookup"><span data-stu-id="23484-128">Step 3: Use the Windows Certification Dashboard</span></span>

<span data-ttu-id="23484-129">Para enviar la aplicación para la certificación, debe iniciar sesión o registrar una cuenta de empresa en el [Panel de certificación de Windows](/previous-versions/hh833792(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="23484-129">To submit your app for certification, you'll need to log in or register a company account on the [Windows Certification Dashboard](/previous-versions/hh833792(v=msdn.10)).</span></span> <span data-ttu-id="23484-130">Una vez hecho, no solo podrá obtener la certificación de la aplicación, sino que también tendrá acceso a las herramientas para revisar y administrar la aplicación en todas las fases del proceso.</span><span class="sxs-lookup"><span data-stu-id="23484-130">Once you do, not only will you be able to get your app certified, but you'll also gain access to tools to review and manage your app at all stages of the process.</span></span>



| <span data-ttu-id="23484-131">Tema</span><span class="sxs-lookup"><span data-stu-id="23484-131">Topic</span></span>                                                                                                                   | <span data-ttu-id="23484-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="23484-132">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23484-133">Configuración de la cuenta</span><span class="sxs-lookup"><span data-stu-id="23484-133">Set up your account</span></span>](/windows-hardware/drivers/dashboard/)                 | <span data-ttu-id="23484-134">Si su empresa no está registrada, debe registrarla a través del panel de certificación de Windows.</span><span class="sxs-lookup"><span data-stu-id="23484-134">If your company isn't already registered, you must register it through the Windows Certification Dashboard.</span></span>                                        |
| [<span data-ttu-id="23484-135">Obtención de un certificado de firma de código</span><span class="sxs-lookup"><span data-stu-id="23484-135">Get a code signing certificate</span></span>](/windows-hardware/drivers/dashboard/)      | <span data-ttu-id="23484-136">Antes de poder establecer una cuenta del panel de certificación de Windows, debe obtener un certificado de firma de código para proteger la información digital.</span><span class="sxs-lookup"><span data-stu-id="23484-136">Before you can establish a Windows Certification Dashboard account, you need to get a code signing certificate to secure your digital information.</span></span> |
| [<span data-ttu-id="23484-137">Probar localmente y cargar los resultados</span><span class="sxs-lookup"><span data-stu-id="23484-137">Test locally and upload the results</span></span>](/windows-hardware/drivers/dashboard/) | <span data-ttu-id="23484-138">Después de ejecutar las pruebas del kit de certificación de aplicaciones de Windows, cargue los resultados en el panel de certificación de Windows.</span><span class="sxs-lookup"><span data-stu-id="23484-138">After your run the Windows App Certification Kit tests, upload the results to the Windows Certification Dashboard.</span></span>                                 |
| [<span data-ttu-id="23484-139">Administrar el envío</span><span class="sxs-lookup"><span data-stu-id="23484-139">Manage your submission</span></span>](/windows-hardware/drivers/dashboard/)              | <span data-ttu-id="23484-140">Después de enviar la aplicación para la certificación, puede revisar el envío a través del panel de certificación de Windows.</span><span class="sxs-lookup"><span data-stu-id="23484-140">After you submit your app for certification, you can review your submission through the Windows Certification Dashboard.</span></span>                           |



 

## <a name="step-4-promote-your-desktop-app"></a><span data-ttu-id="23484-141">Paso 4: promoción de la aplicación de escritorio</span><span class="sxs-lookup"><span data-stu-id="23484-141">Step 4: Promote your desktop app</span></span>



| <span data-ttu-id="23484-142">Tema</span><span class="sxs-lookup"><span data-stu-id="23484-142">Topic</span></span>                                                                      | <span data-ttu-id="23484-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="23484-143">Description</span></span>                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23484-144">Comprobar la compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="23484-144">Check app compatibility</span></span>](/windows/compatibility/windows-8-1-introduction) | <span data-ttu-id="23484-145">Si va a compilar una aplicación para Windows 8.1, investigue los problemas de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="23484-145">If you are building an app for Windows 8.1, investigate compatibility concerns.</span></span>                                           |
| [<span data-ttu-id="23484-146">Usar el logotipo con la aplicación</span><span class="sxs-lookup"><span data-stu-id="23484-146">Use the logo with your app</span></span>](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | <span data-ttu-id="23484-147">Mostrar el logotipo en el embalaje y en los anuncios y otros materiales promocionales de acuerdo con las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="23484-147">Display the logo on packaging and in ads and other promotional materials according to the guidelines.</span></span> <span data-ttu-id="23484-148">Solo para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="23484-148">For Windows 7 only.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="23484-149">Consulte también:</span><span class="sxs-lookup"><span data-stu-id="23484-149">See also:</span></span>

<span data-ttu-id="23484-150">[Foro de compatibilidad de aplicaciones](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): encuentre soporte técnico de la comunidad sobre compatibilidad y certificación del logotipo.</span><span class="sxs-lookup"><span data-stu-id="23484-150">[App compatibility forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): Find support from the community about compatibility and logo certification.</span></span>

<span data-ttu-id="23484-151">[Blog de Windows SDK](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Busque sugerencias y noticias relacionadas con la certificación de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="23484-151">[Windows SDK blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Find tips and news related to app certification.</span></span>

<span data-ttu-id="23484-152">[Foro de Windows Server]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): visite el foro de certificación para obtener respuestas.</span><span class="sxs-lookup"><span data-stu-id="23484-152">[Windows Server forum]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): Visit the Certification forum to get answers.</span></span>

<span data-ttu-id="23484-153">[Guía de compatibilidad](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Obtenga información sobre las novedades o los cambios en la versión más reciente de Windows.</span><span class="sxs-lookup"><span data-stu-id="23484-153">[Compatibility cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Get info about what's new or changed in the latest version of Windows.</span></span>

 

