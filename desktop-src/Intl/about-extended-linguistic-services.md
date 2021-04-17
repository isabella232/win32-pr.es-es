---
description: Los servicios lingüísticos extendidos (ELS) se implementan como una biblioteca de vínculos dinámicos (DLL) que proporciona una gran variedad de funciones de compatibilidad lingüística para el texto que especifica la aplicación.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: Acerca de los servicios lingüísticos extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687835"
---
# <a name="about-extended-linguistic-services"></a><span data-ttu-id="6d24a-103">Acerca de los servicios lingüísticos extendidos</span><span class="sxs-lookup"><span data-stu-id="6d24a-103">About Extended Linguistic Services</span></span>

<span data-ttu-id="6d24a-104">Los servicios lingüísticos extendidos (ELS) se implementan como una biblioteca de vínculos dinámicos (DLL) que proporciona una gran variedad de funciones de compatibilidad lingüística para el texto que especifica la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6d24a-104">Extended Linguistic Services (ELS) is implemented as a dynamic-link library (DLL) that provides a variety of linguistic support functionality for text that the application specifies.</span></span> <span data-ttu-id="6d24a-105">La tecnología incluye los complementos y la plataforma ELS para varios tipos de servicio lingüístico predefinidos a los que puede tener acceso la aplicación a través de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="6d24a-105">The technology includes the ELS platform and plug-ins for several predefined linguistic service types accessible to the application through the platform.</span></span>

> [!Note]  
> <span data-ttu-id="6d24a-106">El módulo ELS se instala automáticamente con Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="6d24a-106">The ELS module is installed automatically with Windows 7 and later.</span></span>

 

## <a name="els-platform"></a><span data-ttu-id="6d24a-107">Plataforma ELS</span><span class="sxs-lookup"><span data-stu-id="6d24a-107">ELS Platform</span></span>

<span data-ttu-id="6d24a-108">La plataforma ELS es la interfaz entre la aplicación y los servicios de ELS.</span><span class="sxs-lookup"><span data-stu-id="6d24a-108">The ELS platform is the interface between your application and the ELS services.</span></span> <span data-ttu-id="6d24a-109">Proporciona una manera sencilla de implementar varios tipos de funcionalidad lingüística a través de la misma API, que permite a la aplicación tener acceso a servicios específicos y usarlos.</span><span class="sxs-lookup"><span data-stu-id="6d24a-109">It provides a simple way to implement several kinds of linguistic functionality through the same API, which allows the application to access and use specific services.</span></span> <span data-ttu-id="6d24a-110">Para obtener más información sobre la API, consulte [Extended lingüística Services Reference.](extended-linguistic-services-reference.md)</span><span class="sxs-lookup"><span data-stu-id="6d24a-110">For more information about the API, see [Extended Linguistic Services Reference.](extended-linguistic-services-reference.md)</span></span>

> [!Note]  
> <span data-ttu-id="6d24a-111">Cuando la aplicación llama a cualquiera de las funciones de la API de ELS, la plataforma asigna memoria y recursos según sea necesario para la comunicación con los servicios.</span><span class="sxs-lookup"><span data-stu-id="6d24a-111">When the application calls any of the ELS API functions, the platform allocates memory and resources as needed for communication with the services.</span></span> <span data-ttu-id="6d24a-112">La aplicación es responsable de volver a llamar a la plataforma para liberar estos recursos.</span><span class="sxs-lookup"><span data-stu-id="6d24a-112">The application is responsible for calling the platform again to free these resources.</span></span>

 

<span data-ttu-id="6d24a-113">La plataforma se ejecuta dentro del espacio de memoria virtual de la aplicación y toda la memoria asignada forma parte de este espacio.</span><span class="sxs-lookup"><span data-stu-id="6d24a-113">The platform runs inside the application virtual memory space, and all allocated memory is part of this space.</span></span> <span data-ttu-id="6d24a-114">Por lo tanto, la aplicación solo necesita vincularse al archivo DLL del componente ELS (Elscore.dll) mediante la vinculación a Elscore. lib o mediante la carga dinámica de Elscore.dll.</span><span class="sxs-lookup"><span data-stu-id="6d24a-114">Thus your application only needs to link to the ELS component DLL (Elscore.dll) by linking to Elscore.lib or by dynamically loading Elscore.dll.</span></span>

## <a name="els-services"></a><span data-ttu-id="6d24a-115">Servicios ELS</span><span class="sxs-lookup"><span data-stu-id="6d24a-115">ELS Services</span></span>

<span data-ttu-id="6d24a-116">En Windows 7 y versiones posteriores, la plataforma ELS solo admite los siguientes servicios predefinidos.</span><span class="sxs-lookup"><span data-stu-id="6d24a-116">For Windows 7 and later, the ELS platform supports only the following predefined services.</span></span>

-   [<span data-ttu-id="6d24a-117">Microsoft Detección de idioma</span><span class="sxs-lookup"><span data-stu-id="6d24a-117">Microsoft Language Detection</span></span>](microsoft-language-detection.md)
-   [<span data-ttu-id="6d24a-118">Detección de scripts de Microsoft</span><span class="sxs-lookup"><span data-stu-id="6d24a-118">Microsoft Script Detection</span></span>](microsoft-script-detection.md)
-   [<span data-ttu-id="6d24a-119">Servicios de transliteración</span><span class="sxs-lookup"><span data-stu-id="6d24a-119">Transliteration services</span></span>](transliteration-services.md)

> [!Note]  
> <span data-ttu-id="6d24a-120">Las versiones futuras de ELS serán compatibles con los servicios adicionales proporcionados por Microsoft o los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="6d24a-120">Future versions of ELS will support additional services provided by Microsoft or service providers.</span></span>

 

<span data-ttu-id="6d24a-121">Cada servicio está asociado a una categoría de servicio que describe lo que hace el servicio.</span><span class="sxs-lookup"><span data-stu-id="6d24a-121">Each service is associated with a service category describing what the service does.</span></span> <span data-ttu-id="6d24a-122">La categoría se representa mediante una cadena no localizable.</span><span class="sxs-lookup"><span data-stu-id="6d24a-122">The category is represented by a nonlocalizable string.</span></span> <span data-ttu-id="6d24a-123">Lo usan las aplicaciones para enumerar los servicios disponibles.</span><span class="sxs-lookup"><span data-stu-id="6d24a-123">It is used by applications to enumerate available services.</span></span> <span data-ttu-id="6d24a-124">Las categorías de servicio actuales son:</span><span class="sxs-lookup"><span data-stu-id="6d24a-124">The current service categories are:</span></span>

-   <span data-ttu-id="6d24a-125">"Detección de idioma"</span><span class="sxs-lookup"><span data-stu-id="6d24a-125">"Language Detection"</span></span>
-   <span data-ttu-id="6d24a-126">"Detección de scripts"</span><span class="sxs-lookup"><span data-stu-id="6d24a-126">"Script Detection"</span></span>
-   <span data-ttu-id="6d24a-127">Litera</span><span class="sxs-lookup"><span data-stu-id="6d24a-127">"Transliteration"</span></span>

<span data-ttu-id="6d24a-128">La plataforma utiliza metadatos de servicio para enumerar los servicios solicitados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6d24a-128">The platform uses service metadata to enumerate the services requested by the application.</span></span> <span data-ttu-id="6d24a-129">La aplicación puede usar las propiedades como el identificador único global (GUID) del servicio, los lenguajes y los scripts de entrada y salida admitidos, y la categoría de servicio para enumerar los servicios de ELS deseados.</span><span class="sxs-lookup"><span data-stu-id="6d24a-129">Properties such as the service globally unique identifier (GUID), supported input and output languages and scripts, and the service category can be used by the application to enumerate the desired ELS services.</span></span>

<span data-ttu-id="6d24a-130">Cada servicio ELS se implementa como un complemento compatible con un archivo DLL que se puede instalar en el sistema operativo para que la plataforma ELS pueda detectarlo y usarlo.</span><span class="sxs-lookup"><span data-stu-id="6d24a-130">Each ELS service is implemented as a plug-in supported by a DLL that can be installed on the operating system so that the ELS platform can detect and use it.</span></span> <span data-ttu-id="6d24a-131">Los servicios pueden exponer sus propios subservicios, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="6d24a-131">Services can expose their own subservices, if required.</span></span>

## <a name="main-els-operations"></a><span data-ttu-id="6d24a-132">Principales operaciones de ELS</span><span class="sxs-lookup"><span data-stu-id="6d24a-132">Main ELS Operations</span></span>

<span data-ttu-id="6d24a-133">En esta sección se describen las operaciones principales admitidas por la plataforma ELS.</span><span class="sxs-lookup"><span data-stu-id="6d24a-133">This section describes the main operations supported by the ELS platform.</span></span> <span data-ttu-id="6d24a-134">La plataforma admite modos de llamada sincrónicos y asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="6d24a-134">The platform supports both synchronous and asynchronous calling modes.</span></span> <span data-ttu-id="6d24a-135">El modo de llamada asincrónica utiliza un grupo de subprocesos de aplicación para programar subprocesos para el procesamiento de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="6d24a-135">The asynchronous calling mode uses an application thread pool to schedule threads for processing requests.</span></span>

> [!Note]  
> <span data-ttu-id="6d24a-136">Dado que la plataforma admite un modo asincrónico, los servicios de ELS no tienen que implementar este tipo de funcionalidad por sí solos.</span><span class="sxs-lookup"><span data-stu-id="6d24a-136">Since the platform supports an asynchronous mode, ELS services do not have to implement this type of functionality on their own.</span></span>

 

### <a name="service-enumeration"></a><span data-ttu-id="6d24a-137">Enumeración de servicios</span><span class="sxs-lookup"><span data-stu-id="6d24a-137">Service Enumeration</span></span>

<span data-ttu-id="6d24a-138">La plataforma ELS carga y administra todos los servicios de ELS, lo que permite que la operación sea transparente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6d24a-138">The ELS platform loads and manages all ELS services, making operation transparent to the application.</span></span> <span data-ttu-id="6d24a-139">La aplicación enumera los servicios disponibles mediante una llamada a [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span><span class="sxs-lookup"><span data-stu-id="6d24a-139">The application enumerates the available services by calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span></span> <span data-ttu-id="6d24a-140">Para obtener instrucciones de programación, consulte [enumeración y liberación de servicios](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="6d24a-140">For programming instructions, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="6d24a-141">Se recomienda por motivos de rendimiento que la aplicación Enumere los servicios disponibles una sola vez.</span><span class="sxs-lookup"><span data-stu-id="6d24a-141">It is advisable for performance reasons to have your application enumerate the available services only once.</span></span> <span data-ttu-id="6d24a-142">La plataforma ELS comprueba los servicios de nuevo en la siguiente enumeración para asegurarse de que los resultados de la enumeración siempre están actualizados.</span><span class="sxs-lookup"><span data-stu-id="6d24a-142">The ELS platform checks the services again on the next enumeration to ensure that its enumeration results are always current.</span></span>

 

### <a name="text-recognition"></a><span data-ttu-id="6d24a-143">Reconocimiento de texto</span><span class="sxs-lookup"><span data-stu-id="6d24a-143">Text Recognition</span></span>

<span data-ttu-id="6d24a-144">Después de la enumeración de servicio, la aplicación llama a la función [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) para usar un servicio Els determinado para asignar cualquier intervalo de texto de texto de entrada al texto de salida.</span><span class="sxs-lookup"><span data-stu-id="6d24a-144">After service enumeration, the application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to use a particular ELS service to map any text range of input text to output text.</span></span> <span data-ttu-id="6d24a-145">Un ejemplo de reconocimiento de texto es el uso de un servicio de detección de idiomas que recibe un segmento de texto y detecta su lenguaje más probable.</span><span class="sxs-lookup"><span data-stu-id="6d24a-145">An example of text recognition is the use of a language detection service that receives a text segment and detects its most probable language.</span></span>

<span data-ttu-id="6d24a-146">Una vez que el servicio reconoce el texto, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) devuelve con una estructura de [**\_ \_ contenedor de propiedades de asignación**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) rellenada con los datos de salida y las propiedades generadas por el servicio.</span><span class="sxs-lookup"><span data-stu-id="6d24a-146">After the service has recognized the text, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns with a [**MAPPING\_PROPERTY\_BAG**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) structure populated with output data and properties produced by the service.</span></span> <span data-ttu-id="6d24a-147">Para evitar pérdidas de memoria, la aplicación debe liberar el contenedor de propiedades mediante una llamada a [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) para cada vez que [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) devuelva S \_ .</span><span class="sxs-lookup"><span data-stu-id="6d24a-147">To avoid memory leaks, the application must free the property bag by calling [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) for each time that the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns S\_OK.</span></span> <span data-ttu-id="6d24a-148">Normalmente, la aplicación realiza esta acción cuando finaliza el uso de los datos de salida o cuando los datos de salida ya no son relevantes porque la región de entrada de texto se ha modificado, por ejemplo, editada o eliminada.</span><span class="sxs-lookup"><span data-stu-id="6d24a-148">Usually the application does this either when it finishes using the output data or when the output data is no longer relevant because the input region of text has been modified, for example, edited or deleted.</span></span> <span data-ttu-id="6d24a-149">Cuando se libera el contenedor de propiedades, **MappingFreePropertyBag** devuelve.</span><span class="sxs-lookup"><span data-stu-id="6d24a-149">When the property bag is released, **MappingFreePropertyBag** returns.</span></span>

<span data-ttu-id="6d24a-150">Se proporcionan instrucciones de programación para el reconocimiento de texto en la [solicitud de reconocimiento de texto](requesting-text-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="6d24a-150">Programming instructions for text recognition are provided in [Requesting Text Recognition](requesting-text-recognition.md).</span></span>

### <a name="service-termination"></a><span data-ttu-id="6d24a-151">Terminación del servicio</span><span class="sxs-lookup"><span data-stu-id="6d24a-151">Service Termination</span></span>

<span data-ttu-id="6d24a-152">Cuando la aplicación ya no necesita los servicios de ELS, llama a [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) antes de finalizar.</span><span class="sxs-lookup"><span data-stu-id="6d24a-152">When your application no longer requires ELS services, it calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) before it terminates.</span></span> <span data-ttu-id="6d24a-153">Para obtener más información, consulte [enumeración y liberación de servicios](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="6d24a-153">For more information, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

### <a name="versioning"></a><span data-ttu-id="6d24a-154">Control de versiones</span><span class="sxs-lookup"><span data-stu-id="6d24a-154">Versioning</span></span>

<span data-ttu-id="6d24a-155">Las versiones futuras de ELS permitirán la actualización de los servicios de ELS.</span><span class="sxs-lookup"><span data-stu-id="6d24a-155">Future versions of ELS will allow the ELS services to be updated.</span></span> <span data-ttu-id="6d24a-156">La aplicación podrá comprobar los números de versión de la estructura de [**\_ \_ información del servicio de asignación**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) para detectar los cambios en los servicios.</span><span class="sxs-lookup"><span data-stu-id="6d24a-156">The application will be able to check the version numbers of the [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure to detect any changes in the services.</span></span>

> [!Note]  
> <span data-ttu-id="6d24a-157">La aplicación ELS no debe suponer que las distintas versiones del mismo servicio puedan recuperar exactamente los mismos resultados.</span><span class="sxs-lookup"><span data-stu-id="6d24a-157">Your ELS application should not make the assumption that different versions of the same service can retrieve exactly the same results.</span></span>

 

 

 



