---
description: Compatibilidad con proxy para orígenes de red
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Compatibilidad con proxy para orígenes de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696678"
---
# <a name="proxy-support-for-network-sources"></a><span data-ttu-id="6390d-103">Compatibilidad con proxy para orígenes de red</span><span class="sxs-lookup"><span data-stu-id="6390d-103">Proxy Support for Network Sources</span></span>

<span data-ttu-id="6390d-104">Un servidor proxy es un servidor intermedio entre la intranet e Internet, que enruta las solicitudes de la aplicación cliente al servidor multimedia y recupera los archivos del servidor multimedia.</span><span class="sxs-lookup"><span data-stu-id="6390d-104">A proxy server is an intermediate server between your intranet and the Internet, which routes requests from the client application to the media server and retrieves files from the media server.</span></span>

<span data-ttu-id="6390d-105">Media Foundation crea implícitamente un objeto de *localizador proxy* cuando una aplicación cliente intenta obtener acceso a una dirección URL de origen.</span><span class="sxs-lookup"><span data-stu-id="6390d-105">Media Foundation implicitly creates a *proxy locator* object when a client application tries to access a source URL.</span></span> <span data-ttu-id="6390d-106">El objeto localizador proxy expone la interfaz [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="6390d-106">The proxy locator object exposes the [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) interface.</span></span> <span data-ttu-id="6390d-107">Durante la resolución del código fuente, Media Foundation comprueba el almacén de propiedades pasado al método de resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="6390d-107">During source resolution, Media Foundation checks the property store passed to the source resolver method.</span></span>

<span data-ttu-id="6390d-108">Si el almacén de propiedades contiene la propiedad [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) establecida en un objeto de generador de localizador proxy implementado por la aplicación, invoca el método [**IMFNetProxyLocatorFactory:: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) para crear un localizador proxy con opciones de configuración personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6390d-108">If the property store contains the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property set to a proxy locator factory object implemented by the application then, it invokes the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method to create a proxy locator with custom configuration settings.</span></span>

<span data-ttu-id="6390d-109">Si no se establece el almacén de propiedades, Media Foundation crea el localizador de proxy con la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6390d-109">If the property store is not set, then Media Foundation creates the proxy locator with default configuration.</span></span> <span data-ttu-id="6390d-110">Estos valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6390d-110">These settings are as follows:</span></span>

-   <span data-ttu-id="6390d-111">Si se establece la Directiva de usuario, el localizador proxy utiliza los valores especificados en el registro.</span><span class="sxs-lookup"><span data-stu-id="6390d-111">If user policy is set, then the proxy locator uses settings specified in the registry.</span></span>

-   <span data-ttu-id="6390d-112">Para HTTP, el localizador proxy usa la configuración de proxy del explorador.</span><span class="sxs-lookup"><span data-stu-id="6390d-112">For HTTP, the proxy locator uses browser proxy settings.</span></span>

-   <span data-ttu-id="6390d-113">En el caso de RTSP, el localizador proxy está configurado para omitir los servidores proxy al conectarse al servidor multimedia.</span><span class="sxs-lookup"><span data-stu-id="6390d-113">For RTSP, the proxy locator is configured to bypass proxy servers when connecting to the media server.</span></span>

<span data-ttu-id="6390d-114">La aplicación puede cambiar esta configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6390d-114">This default configuration can be changed by the application.</span></span> <span data-ttu-id="6390d-115">Los temas siguientes contienen información acerca de los valores de configuración de un localizador proxy:</span><span class="sxs-lookup"><span data-stu-id="6390d-115">The following topics contain information about the configuration settings for a proxy locator:</span></span>

-   [<span data-ttu-id="6390d-116">Opciones de configuración del localizador proxy</span><span class="sxs-lookup"><span data-stu-id="6390d-116">Proxy Locator Configuration Settings</span></span>](proxy-locator-configuration-settings.md)

-   [<span data-ttu-id="6390d-117">Cómo configurar el localizador de proxy</span><span class="sxs-lookup"><span data-stu-id="6390d-117">How to Configure the Proxy Locator</span></span>](how-to-configure-the-proxy-locator.md)

<span data-ttu-id="6390d-118">Media Foundation inicializa el localizador de proxy para la dirección URL de origen especificada para la [resolución de origen](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="6390d-118">Media Foundation initializes the proxy locator for the source URL specified to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="6390d-119">El localizador proxy detecta un servidor proxy para usarlo en función de los valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="6390d-119">The proxy locator detects a proxy server to use based on configuration settings.</span></span> <span data-ttu-id="6390d-120">Cuando el localizador proxy intenta establecer un servidor proxy, registra el resultado de éxito o error en el registro.</span><span class="sxs-lookup"><span data-stu-id="6390d-120">When the proxy locator attempts the set a proxy server, it records the success or failure result in the registry.</span></span> <span data-ttu-id="6390d-121">Este valor se comprueba durante el siguiente proceso de detección del proxy.</span><span class="sxs-lookup"><span data-stu-id="6390d-121">This value is checked during the next proxy detection process.</span></span> <span data-ttu-id="6390d-122">Si se sabe que un determinado servidor proxy ha causado errores en el pasado, el localizador proxy lo omite.</span><span class="sxs-lookup"><span data-stu-id="6390d-122">If a certain proxy server is known to have caused failures in the past, the proxy locator skips it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6390d-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6390d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6390d-124">Atributos y propiedades</span><span class="sxs-lookup"><span data-stu-id="6390d-124">Attributes and Properties</span></span>](attributes-and-properties.md)
</dt> <dt>

[<span data-ttu-id="6390d-125">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6390d-125">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



