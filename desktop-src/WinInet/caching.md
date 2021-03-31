---
title: Almacenamiento en caché (Internet de Windows)
description: Las funciones WinINet tienen compatibilidad con almacenamiento en caché simple, pero flexible y integrada.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149793"
---
# <a name="caching-windows-internet"></a><span data-ttu-id="0d39c-103">Almacenamiento en caché (Internet de Windows)</span><span class="sxs-lookup"><span data-stu-id="0d39c-103">Caching (Windows Internet)</span></span>

<span data-ttu-id="0d39c-104">Las funciones WinINet tienen compatibilidad con almacenamiento en caché simple, pero flexible y integrada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-104">The WinINet functions have simple, yet flexible, built-in caching support.</span></span> <span data-ttu-id="0d39c-105">Los datos recuperados de la red se almacenan en la memoria caché del disco duro y se recuperan para las solicitudes posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d39c-105">Any data retrieved from the network is cached on the hard disk and retrieved for subsequent requests.</span></span> <span data-ttu-id="0d39c-106">La aplicación puede controlar el almacenamiento en caché en cada solicitud.</span><span class="sxs-lookup"><span data-stu-id="0d39c-106">The application can control the caching on each request.</span></span> <span data-ttu-id="0d39c-107">En el caso de las solicitudes HTTP del servidor, la mayoría de los encabezados recibidos también se almacenan en caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-107">For http requests from the server, most headers received are also cached.</span></span> <span data-ttu-id="0d39c-108">Cuando se satisface una solicitud HTTP de la memoria caché, los encabezados almacenados en caché también se devuelven al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-108">When an http request is satisfied from the cache, the cached headers are also returned to the caller.</span></span> <span data-ttu-id="0d39c-109">Esto hace que los datos se descarguen sin problemas, independientemente de si los datos proceden de la memoria caché o de la red.</span><span class="sxs-lookup"><span data-stu-id="0d39c-109">This makes data download seamless, whether the data is coming from the cache or from the network.</span></span>

<span data-ttu-id="0d39c-110">Las aplicaciones deben asignar correctamente un búfer para obtener los resultados deseados al utilizar las funciones de almacenamiento en caché de URL persistentes.</span><span class="sxs-lookup"><span data-stu-id="0d39c-110">Applications must properly allocate a buffer in order to get the desired results when using the persistent URL caching functions.</span></span> <span data-ttu-id="0d39c-111">Para obtener más información, consulte [uso de búferes](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="0d39c-111">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>

## <a name="cache-behavior-during-response-processing"></a><span data-ttu-id="0d39c-112">Comportamiento de caché durante el procesamiento de la respuesta</span><span class="sxs-lookup"><span data-stu-id="0d39c-112">Cache Behavior During Response Processing</span></span>

<span data-ttu-id="0d39c-113">La caché de WinINet es compatible con las directivas de control de caché HTTP descritas en RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="0d39c-113">The WinINet cache is compliant with the HTTP cache-control directives described in RFC 2616.</span></span> <span data-ttu-id="0d39c-114">Las directivas de control de caché y las marcas de conjunto de aplicaciones determinan lo que se puede almacenar en caché. sin embargo, WinINet determina lo que realmente se almacena en la memoria caché en función del criterio siguiente:</span><span class="sxs-lookup"><span data-stu-id="0d39c-114">The cache-control directives and application set flags determine what may be cached; however, WinINet determines what is actually cached based on the following criterion:</span></span>

-   <span data-ttu-id="0d39c-115">WinINet solo almacena en caché las respuestas HTTP y FTP.</span><span class="sxs-lookup"><span data-stu-id="0d39c-115">WinINet only caches HTTP and FTP responses.</span></span>
-   <span data-ttu-id="0d39c-116">Solo las respuestas con buen comportamiento pueden almacenarse en una memoria caché y utilizarse en una respuesta a una solicitud posterior.</span><span class="sxs-lookup"><span data-stu-id="0d39c-116">Only well behaved responses may be stored by a cache and used in a reply to a subsequent Request.</span></span> <span data-ttu-id="0d39c-117">Las respuestas con buen comportamiento se definen como respuestas que se devuelven correctamente.</span><span class="sxs-lookup"><span data-stu-id="0d39c-117">Well behaved responses are defined as responses that return successfully.</span></span>
-   <span data-ttu-id="0d39c-118">De forma predeterminada, WinINet almacenará en caché las respuestas correctas a menos que una directiva cache-control del servidor o una marca definida por la aplicación denoten específicamente que la respuesta no se puede almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-118">By default, WinINet will cache successful responses unless either a cache-control directive from the server, or an application-defined flag specifically denote that the response may not be cached.</span></span>
-   <span data-ttu-id="0d39c-119">En general, las respuestas al verbo GET se almacenan en caché si se cumplen los requisitos mencionados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0d39c-119">In general, responses to the GET verb are cached if the requirements listed above are met.</span></span> <span data-ttu-id="0d39c-120">Las respuestas a los verbos PUT y POST no se almacenan en caché bajo ninguna circunstancia.</span><span class="sxs-lookup"><span data-stu-id="0d39c-120">Responses to PUT and POST verbs are not cached under any circumstances.</span></span>
-   <span data-ttu-id="0d39c-121">Los elementos se almacenarán en caché incluso cuando la memoria caché esté llena.</span><span class="sxs-lookup"><span data-stu-id="0d39c-121">Items will be cached even when the cache is full.</span></span> <span data-ttu-id="0d39c-122">Si un elemento agregado coloca la memoria caché en el límite de tamaño, se programa el borrador de caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-122">If an added item is puts the cache over the size limit, the cache scavenger is scheduled.</span></span> <span data-ttu-id="0d39c-123">De forma predeterminada, no se garantiza que los elementos sigan siendo más de 10 minutos en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-123">By default, items are not guaranteed to remain more than 10 minutes in the cache.</span></span> <span data-ttu-id="0d39c-124">Para obtener más información, vea la sección sobre el [borrador de caché](#cache-scavenger) más adelante.</span><span class="sxs-lookup"><span data-stu-id="0d39c-124">For more information, see the [Cache Scavenger](#cache-scavenger) section below.</span></span>
-   <span data-ttu-id="0d39c-125">Https está almacenado en caché de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-125">Https is cached by default.</span></span> <span data-ttu-id="0d39c-126">Se administra mediante una configuración global que no se puede invalidar mediante directivas de caché definidas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0d39c-126">This is managed by a global setting that cannot be overridden by application-defined cache directives.</span></span> <span data-ttu-id="0d39c-127">Para invalidar la configuración global, seleccione el applet opciones de Internet en el panel de control y vaya a la pestaña avanzadas. Active la casilla "no guardar páginas cifradas en el disco" en la sección "seguridad".</span><span class="sxs-lookup"><span data-stu-id="0d39c-127">To override the global setting, select the Internet Options applet in the control panel, and go to the advanced tab. Check the "Do not save encrypted pages to disk" box under the "Security" section.</span></span>

## <a name="cache-scavenger"></a><span data-ttu-id="0d39c-128">Limpieza de caché</span><span class="sxs-lookup"><span data-stu-id="0d39c-128">Cache Scavenger</span></span>

<span data-ttu-id="0d39c-129">El borrador de caché limpia periódicamente los elementos de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-129">The cache scavenger periodically cleans items from the cache.</span></span> <span data-ttu-id="0d39c-130">Si se agrega un elemento a la memoria caché y la memoria caché está llena, el elemento se agrega a la memoria caché y se programa el borrador de caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-130">If an item is added to the cache and the cache is full, the item is added to the cache and the cache scavenger is scheduled.</span></span> <span data-ttu-id="0d39c-131">Si el borrador de caché completa una ronda de eliminación de registros obsoletos y la memoria caché no alcanzó el límite de caché, el borrador se programa para otro redondeo cuando se agrega otro elemento a la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-131">If the cache scavenger completes a round of scavenging and the cache has not reached the cache limit, the scavenger is scheduled for another round when another item is added to the cache.</span></span> <span data-ttu-id="0d39c-132">En general, el borrador se programa cuando un elemento agregado coloca la memoria caché a lo largo de su límite de tamaño.</span><span class="sxs-lookup"><span data-stu-id="0d39c-132">In general, the scavenger is scheduled when an added item puts the cache over its size limit.</span></span> <span data-ttu-id="0d39c-133">De forma predeterminada, el período de vida mínimo en la memoria caché se establece en 10 minutos, a menos que se especifique lo contrario en una directiva cache-control.</span><span class="sxs-lookup"><span data-stu-id="0d39c-133">By default, the minimum time to live in the cache is set to 10 minutes unless otherwise specified in a cache-control directive.</span></span> <span data-ttu-id="0d39c-134">Cuando se inicia el borrador de caché, no hay ninguna garantía de que los elementos más antiguos sean los primeros que se eliminarán de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-134">When the cache scavenger is initiated, there is no guarantee that the oldest items are the first to be deleted from the cache.</span></span>

<span data-ttu-id="0d39c-135">La memoria caché se comparte entre todas las aplicaciones WinINet del equipo para el mismo usuario.</span><span class="sxs-lookup"><span data-stu-id="0d39c-135">The cache is shared across all WinINet applications on the computer for the same user.</span></span> <span data-ttu-id="0d39c-136">A partir de Windows Vista y Windows Server 2008, el tamaño de la caché se establece en 1/32 º el tamaño del disco, con un tamaño mínimo de 8 MB y un tamaño máximo de 50 MB.</span><span class="sxs-lookup"><span data-stu-id="0d39c-136">Starting with Windows Vista and Windows Server 2008 the cache size is set to 1/32nd the size of the disk, with a minimum size of 8MB and a maximum size of 50MB.</span></span>

## <a name="using-flags-to-control-caching"></a><span data-ttu-id="0d39c-137">Usar marcas para controlar el almacenamiento en caché</span><span class="sxs-lookup"><span data-stu-id="0d39c-137">Using Flags to Control Caching</span></span>

<span data-ttu-id="0d39c-138">Las marcas de almacenamiento en caché permiten que una aplicación controle cuándo y cómo usa la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-138">The caching flags allow an application to control when and how it uses the cache.</span></span> <span data-ttu-id="0d39c-139">Estas marcas se pueden utilizar por sí solas o en combinación con el parámetro *dwFlags* en las funciones que tienen acceso a la información o a los recursos de Internet.</span><span class="sxs-lookup"><span data-stu-id="0d39c-139">These flags can be used alone or in combination with the *dwFlags* parameter in functions that access information or resources on the Internet.</span></span> <span data-ttu-id="0d39c-140">De forma predeterminada, las funciones almacenan todos los datos descargados de Internet.</span><span class="sxs-lookup"><span data-stu-id="0d39c-140">By default, the functions store all data downloaded from the Internet.</span></span>

<span data-ttu-id="0d39c-141">Las marcas siguientes se pueden usar para controlar el almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-141">The following flags can be used to control caching.</span></span>



| <span data-ttu-id="0d39c-142">Value</span><span class="sxs-lookup"><span data-stu-id="0d39c-142">Value</span></span>                                                                                                                                                  | <span data-ttu-id="0d39c-143">Significado</span><span class="sxs-lookup"><span data-stu-id="0d39c-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d39c-144">**caché de marcas de INTERNET \_ \_ \_ asincrónica**</span><span class="sxs-lookup"><span data-stu-id="0d39c-144">**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>](api-flags.md)                                                                            | <span data-ttu-id="0d39c-145">Esta marca no tiene efecto.</span><span class="sxs-lookup"><span data-stu-id="0d39c-145">This flag has no effect.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="0d39c-146">**caché de marcas de INTERNET \_ \_ si se \_ \_ \_ produce un error de red**</span><span class="sxs-lookup"><span data-stu-id="0d39c-146">**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>](api-flags.md)                                                              | <span data-ttu-id="0d39c-147">Devuelve el recurso de la memoria caché si se produce un error en la solicitud de red para el recurso debido a un [error de restablecimiento de \_ \_ conexión \_ a Internet](wininet-errors.md) o error [ \_ Internet \_ no puede \_ conectar](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="0d39c-147">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="0d39c-148">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="0d39c-148">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                                                                              |
| [<span data-ttu-id="0d39c-149">**marca de INTERNET no \_ \_ \_ almacenar en caché**</span><span class="sxs-lookup"><span data-stu-id="0d39c-149">**INTERNET\_FLAG\_DONT\_CACHE**</span></span>](api-flags.md)                                                                              | <span data-ttu-id="0d39c-150">No almacena en caché los datos, ya sea de forma local o en cualquier puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="0d39c-150">Does not cache the data, either locally or in any gateways.</span></span> <span data-ttu-id="0d39c-151">Del mismo modo que el valor preferido, [**Internet \_ Flag \_ no \_ \_ escribir en caché**](api-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0d39c-151">Identical to the preferred value, [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | <span data-ttu-id="0d39c-152">Indica que se trata de un envío de formularios.</span><span class="sxs-lookup"><span data-stu-id="0d39c-152">Indicates that this is a Forms submission.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="0d39c-153">[**Internet \_ de marca \_ de la \_ memoria caché**](api-flags.md)[**envío de \_ \_ formularios \_ de marcas de Internet**](api-flags.md)</span><span class="sxs-lookup"><span data-stu-id="0d39c-153">[**INTERNET\_FLAG\_FROM\_CACHE**](api-flags.md)[**INTERNET\_FLAG\_FORMS\_SUBMIT**](api-flags.md)</span></span> | <span data-ttu-id="0d39c-154">No realiza solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="0d39c-154">Does not make network requests.</span></span> <span data-ttu-id="0d39c-155">Todas las entidades se devuelven desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-155">All entities are returned from the cache.</span></span> <span data-ttu-id="0d39c-156">Si el elemento solicitado no está en la memoria caché, se devuelve un error adecuado, como archivo de ERROR \_ \_ no \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="0d39c-156">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="0d39c-157">Solo la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="0d39c-157">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>                                                                                                                                                                                                       |
| [<span data-ttu-id="0d39c-158">**indicador de INTERNET de \_ \_ FWD \_ back**</span><span class="sxs-lookup"><span data-stu-id="0d39c-158">**INTERNET\_FLAG\_FWD\_BACK**</span></span>](api-flags.md)                                                                                  | <span data-ttu-id="0d39c-159">Indica que la función debe usar la copia del recurso que se encuentra actualmente en la caché de Internet.</span><span class="sxs-lookup"><span data-stu-id="0d39c-159">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="0d39c-160">La fecha de expiración y otra información sobre el recurso no se comprueban.</span><span class="sxs-lookup"><span data-stu-id="0d39c-160">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="0d39c-161">Si el elemento solicitado no se encuentra en la caché de Internet, el sistema intentará localizar el recurso en la red.</span><span class="sxs-lookup"><span data-stu-id="0d39c-161">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="0d39c-162">Este valor se presentó en Microsoft Internet Explorer 5 y está asociado a las operaciones de botón **adelante** y **atrás** de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0d39c-162">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span> |
| [<span data-ttu-id="0d39c-163">**hipervínculo de marca de INTERNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0d39c-163">**INTERNET\_FLAG\_HYPERLINK**</span></span>](api-flags.md)                                                                                 | <span data-ttu-id="0d39c-164">Fuerza a la aplicación a recargar un recurso si no hay tiempo de expiración y no se devolvió ninguna hora de última modificación cuando el recurso se almacenó en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-164">Forces the application to reload a resource if no expire time and no last-modified time were returned when the resource was stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="0d39c-165">**marca de INTERNET para \_ \_ hacer \_ persistente**</span><span class="sxs-lookup"><span data-stu-id="0d39c-165">**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>](api-flags.md)                                                                    | <span data-ttu-id="0d39c-166">Ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="0d39c-166">No longer supported.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="0d39c-167">**la \_ marca de Internet \_ debe \_ almacenar en caché la \_ solicitud**</span><span class="sxs-lookup"><span data-stu-id="0d39c-167">**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>](api-flags.md)                                                             | <span data-ttu-id="0d39c-168">Hace que se cree un archivo temporal si el archivo no se puede almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-168">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="0d39c-169">Es idéntico al valor preferido, el [**\_ \_ \_ archivo**](api-flags.md)de la marca de Internet.</span><span class="sxs-lookup"><span data-stu-id="0d39c-169">This is identical to the preferred value, [**INTERNET\_FLAG\_NEED\_FILE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="0d39c-170">**\_archivo de \_ necesidad de marca de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="0d39c-170">**INTERNET\_FLAG\_NEED\_FILE**</span></span>](api-flags.md)                                                                                | <span data-ttu-id="0d39c-171">Hace que se cree un archivo temporal si el archivo no se puede almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-171">Causes a temporary file to be created if the file cannot be cached.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="0d39c-172">**marca de INTERNET \_ \_ sin \_ escritura de caché \_**</span><span class="sxs-lookup"><span data-stu-id="0d39c-172">**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>](api-flags.md)                                                                     | <span data-ttu-id="0d39c-173">Rechaza cualquier intento por parte de la función para almacenar los datos descargados de Internet en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-173">Rejects any attempt by the function to store data downloaded from the Internet in the cache.</span></span> <span data-ttu-id="0d39c-174">Esta marca es necesaria si la aplicación no desea que los recursos descargados se almacenen localmente.</span><span class="sxs-lookup"><span data-stu-id="0d39c-174">This flag is necessary if the application does not want any downloaded resources to be stored locally.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="0d39c-175">**marca de INTERNET \_ \_ sin \_ interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="0d39c-175">**INTERNET\_FLAG\_NO\_UI**</span></span>](api-flags.md)                                                                                        | <span data-ttu-id="0d39c-176">Deshabilita el cuadro de diálogo cookie.</span><span class="sxs-lookup"><span data-stu-id="0d39c-176">Disables the cookie dialog box.</span></span> <span data-ttu-id="0d39c-177">Esta marca se puede usar en [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo solicitudes HTTP).</span><span class="sxs-lookup"><span data-stu-id="0d39c-177">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="0d39c-178">**marca de INTERNET \_ \_ sin conexión**</span><span class="sxs-lookup"><span data-stu-id="0d39c-178">**INTERNET\_FLAG\_OFFLINE**</span></span>](api-flags.md)                                                                                     | <span data-ttu-id="0d39c-179">Impide que la aplicación envíe solicitudes a la red.</span><span class="sxs-lookup"><span data-stu-id="0d39c-179">Prevents the application from sending requests to the network.</span></span> <span data-ttu-id="0d39c-180">Todas las solicitudes se resuelven mediante los recursos almacenados en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-180">All requests are resolved using the resources stored in the cache.</span></span> <span data-ttu-id="0d39c-181">Si el recurso no está en la memoria caché, se devuelve un error adecuado, como archivo de ERROR \_ \_ no \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="0d39c-181">If the resource is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span>                                                                                                                                                                                                                            |
| [<span data-ttu-id="0d39c-182">**marca de INTERNET \_ \_ pragma \_ nocache**</span><span class="sxs-lookup"><span data-stu-id="0d39c-182">**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>](api-flags.md)                                                                      | <span data-ttu-id="0d39c-183">Fuerza la resolución de la solicitud por el servidor de origen, incluso si existe una copia almacenada en caché en el proxy.</span><span class="sxs-lookup"><span data-stu-id="0d39c-183">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="0d39c-184">La función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo en solicitudes HTTP y https) y la función [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usan esta marca.</span><span class="sxs-lookup"><span data-stu-id="0d39c-184">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="0d39c-185">**RECARGA de la marca de INTERNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0d39c-185">**INTERNET\_FLAG\_RELOAD**</span></span>](api-flags.md)                                                                                       | <span data-ttu-id="0d39c-186">Fuerza a la función a recuperar el recurso solicitado directamente desde Internet.</span><span class="sxs-lookup"><span data-stu-id="0d39c-186">Forces the function to retrieve the requested resource directly from the Internet.</span></span> <span data-ttu-id="0d39c-187">La información que se descarga se almacena en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-187">The information that is downloaded is stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="0d39c-188">**marca de INTERNET volver a \_ \_ sincronizar**</span><span class="sxs-lookup"><span data-stu-id="0d39c-188">**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>](api-flags.md)                                                                         | <span data-ttu-id="0d39c-189">Hace que una aplicación realice una descarga condicional del recurso desde Internet.</span><span class="sxs-lookup"><span data-stu-id="0d39c-189">Causes an application to perform a conditional download of the resource from the Internet.</span></span> <span data-ttu-id="0d39c-190">Si la versión almacenada en la memoria caché es actual, la información se descarga de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-190">If the version stored in the cache is current, the information is downloaded from the cache.</span></span> <span data-ttu-id="0d39c-191">De lo contrario, la información se recarga desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="0d39c-191">Otherwise, the information is reloaded from the server.</span></span>                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a><span data-ttu-id="0d39c-192">Funciones persistentes de almacenamiento en caché</span><span class="sxs-lookup"><span data-stu-id="0d39c-192">Persistent Caching Functions</span></span>

<span data-ttu-id="0d39c-193">Los clientes que necesitan servicios persistentes de almacenamiento en caché usan las funciones de almacenamiento en caché persistentes para permitir que sus aplicaciones guarden datos en el sistema de archivos local para su uso posterior, como en situaciones en las que un vínculo de ancho de banda bajo limita el acceso a los datos o el acceso no está disponible en absoluto.</span><span class="sxs-lookup"><span data-stu-id="0d39c-193">Clients that need persistent caching services use the persistent caching functions to allow their applications to save data in the local file system for subsequent use, such as in situations where a low-bandwidth link limits access to the data, or the access is not available at all.</span></span>

<span data-ttu-id="0d39c-194">Las funciones de caché proporcionan almacenamiento en caché persistente y exploración sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0d39c-194">The cache functions provide persistent caching and offline browsing.</span></span> <span data-ttu-id="0d39c-195">A menos que la marca de Internet no especifique ningún marcador de [**\_ \_ \_ \_ escritura de caché**](api-flags.md) , las funciones almacenan en caché todos los datos descargados de la red.</span><span class="sxs-lookup"><span data-stu-id="0d39c-195">Unless the [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md) flag explicitly specifies no caching, the functions cache all data downloaded from the network.</span></span> <span data-ttu-id="0d39c-196">Las respuestas a los datos POST no se almacenan en caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-196">The responses to POST data are not cached.</span></span>

## <a name="using-the-persistent-url-cache-functions"></a><span data-ttu-id="0d39c-197">Usar las funciones de caché de direcciones URL persistentes</span><span class="sxs-lookup"><span data-stu-id="0d39c-197">Using the Persistent URL Cache Functions</span></span>

<span data-ttu-id="0d39c-198">Las siguientes funciones de caché de dirección URL persistente permiten a una aplicación tener acceso a la información almacenada en la memoria caché y manipularla.</span><span class="sxs-lookup"><span data-stu-id="0d39c-198">The following persistent URL cache functions allow an application to access and manipulate information stored in the cache.</span></span>



| <span data-ttu-id="0d39c-199">Función</span><span class="sxs-lookup"><span data-stu-id="0d39c-199">Function</span></span>                                                           | <span data-ttu-id="0d39c-200">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d39c-200">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d39c-201">**CommitUrlCacheEntryA**</span><span class="sxs-lookup"><span data-stu-id="0d39c-201">**CommitUrlCacheEntryA**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | <span data-ttu-id="0d39c-202">Almacena en memoria caché los datos del archivo especificado en el almacenamiento de caché y los asocia a la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-202">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="0d39c-203">**CommitUrlCacheEntryW**</span><span class="sxs-lookup"><span data-stu-id="0d39c-203">**CommitUrlCacheEntryW**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | <span data-ttu-id="0d39c-204">Almacena en memoria caché los datos del archivo especificado en el almacenamiento de caché y los asocia a la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-204">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="0d39c-205">**CreateUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="0d39c-205">**CreateUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | <span data-ttu-id="0d39c-206">Asigna el almacenamiento de caché solicitado y crea un nombre de archivo local para guardar la entrada de caché que corresponde al nombre de origen.</span><span class="sxs-lookup"><span data-stu-id="0d39c-206">Allocates the requested cache storage and creates a local file name for saving the cache entry that corresponds to the source name.</span></span>                           |
| [<span data-ttu-id="0d39c-207">**CreateUrlCacheGroup**</span><span class="sxs-lookup"><span data-stu-id="0d39c-207">**CreateUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | <span data-ttu-id="0d39c-208">Genera una identificación de grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-208">Generates a cache group identification.</span></span>                                                                                                                       |
| [<span data-ttu-id="0d39c-209">**DeleteUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="0d39c-209">**DeleteUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | <span data-ttu-id="0d39c-210">Quita el archivo asociado al nombre de origen de la memoria caché, si el archivo existe.</span><span class="sxs-lookup"><span data-stu-id="0d39c-210">Removes the file associated with the source name from the cache, if the file exists.</span></span>                                                                          |
| [<span data-ttu-id="0d39c-211">**DeleteUrlCacheGroup**</span><span class="sxs-lookup"><span data-stu-id="0d39c-211">**DeleteUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | <span data-ttu-id="0d39c-212">Libera un **GROUPID** y cualquier estado asociado en el archivo de índice de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-212">Releases a **GROUPID** and any associated state in the cache index file.</span></span>                                                                                      |
| [<span data-ttu-id="0d39c-213">**FindCloseUrlCache**</span><span class="sxs-lookup"><span data-stu-id="0d39c-213">**FindCloseUrlCache**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | <span data-ttu-id="0d39c-214">Cierra el identificador de enumeración especificado.</span><span class="sxs-lookup"><span data-stu-id="0d39c-214">Closes the specified enumeration handle.</span></span>                                                                                                                      |
| [<span data-ttu-id="0d39c-215">**FindFirstUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="0d39c-215">**FindFirstUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | <span data-ttu-id="0d39c-216">Comienza la enumeración de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-216">Begins the enumeration of the cache.</span></span>                                                                                                                          |
| [<span data-ttu-id="0d39c-217">**FindFirstUrlCacheEntryEx**</span><span class="sxs-lookup"><span data-stu-id="0d39c-217">**FindFirstUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | <span data-ttu-id="0d39c-218">Comienza una enumeración filtrada de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-218">Begins a filtered enumeration of the cache.</span></span>                                                                                                                   |
| [<span data-ttu-id="0d39c-219">**FindNextUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="0d39c-219">**FindNextUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | <span data-ttu-id="0d39c-220">Recupera la entrada siguiente en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-220">Retrieves the next entry in the cache.</span></span>                                                                                                                        |
| [<span data-ttu-id="0d39c-221">**FindNextUrlCacheEntryEx**</span><span class="sxs-lookup"><span data-stu-id="0d39c-221">**FindNextUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | <span data-ttu-id="0d39c-222">Recupera la entrada siguiente en una enumeración de caché filtrada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-222">Retrieves the next entry in a filtered cache enumeration.</span></span>                                                                                                     |
| [<span data-ttu-id="0d39c-223">**GetUrlCacheEntryInfo**</span><span class="sxs-lookup"><span data-stu-id="0d39c-223">**GetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | <span data-ttu-id="0d39c-224">Recupera información sobre una entrada de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-224">Retrieves information about a cache entry.</span></span>                                                                                                                    |
| [<span data-ttu-id="0d39c-225">**GetUrlCacheEntryInfoEx**</span><span class="sxs-lookup"><span data-stu-id="0d39c-225">**GetUrlCacheEntryInfoEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | <span data-ttu-id="0d39c-226">Busca la dirección URL después de traducir cualquier redirección almacenada en caché que se aplicaría en el modo sin conexión de [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="0d39c-226">Searches for the URL after translating any cached redirections that would be applied in offline mode by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>           |
| [<span data-ttu-id="0d39c-227">**ReadUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="0d39c-227">**ReadUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | <span data-ttu-id="0d39c-228">Lee los datos almacenados en caché de una secuencia que se ha abierto mediante [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span><span class="sxs-lookup"><span data-stu-id="0d39c-228">Reads the cached data from a stream that has been opened using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                            |
| [<span data-ttu-id="0d39c-229">**RetrieveUrlCacheEntryFile**</span><span class="sxs-lookup"><span data-stu-id="0d39c-229">**RetrieveUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | <span data-ttu-id="0d39c-230">Recupera una entrada de caché de la memoria caché en forma de archivo.</span><span class="sxs-lookup"><span data-stu-id="0d39c-230">Retrieves a cache entry from the cache in the form of a file.</span></span>                                                                                                 |
| [<span data-ttu-id="0d39c-231">**RetrieveUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="0d39c-231">**RetrieveUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | <span data-ttu-id="0d39c-232">Proporciona la manera más eficaz e independiente de la implementación de obtener acceso a los datos de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-232">Provides the most efficient and implementation-independent way of accessing the cache data.</span></span>                                                                   |
| [<span data-ttu-id="0d39c-233">**SetUrlCacheEntryGroup**</span><span class="sxs-lookup"><span data-stu-id="0d39c-233">**SetUrlCacheEntryGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | <span data-ttu-id="0d39c-234">Agrega o quita entradas de un grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-234">Adds or removes entries from a cache group.</span></span>                                                                                                                   |
| [<span data-ttu-id="0d39c-235">**SetUrlCacheEntryInfo**</span><span class="sxs-lookup"><span data-stu-id="0d39c-235">**SetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | <span data-ttu-id="0d39c-236">Establece los miembros especificados de la estructura de [**información de entrada de caché de Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .</span><span class="sxs-lookup"><span data-stu-id="0d39c-236">Sets the specified members of the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span>                                                |
| [<span data-ttu-id="0d39c-237">**UnlockUrlCacheEntryFile**</span><span class="sxs-lookup"><span data-stu-id="0d39c-237">**UnlockUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | <span data-ttu-id="0d39c-238">Desbloquea la entrada de caché que se bloqueó cuando el archivo se recuperó para su uso desde la memoria caché por parte de [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span><span class="sxs-lookup"><span data-stu-id="0d39c-238">Unlocks the cache entry that was locked when the file was retrieved for use from the cache by [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span></span> |
| [<span data-ttu-id="0d39c-239">**UnlockUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="0d39c-239">**UnlockUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | <span data-ttu-id="0d39c-240">Cierra la secuencia que se ha recuperado mediante [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span><span class="sxs-lookup"><span data-stu-id="0d39c-240">Closes the stream that has been retrieved using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                                           |



 

### <a name="enumerating-the-cache"></a><span data-ttu-id="0d39c-241">Enumerar la memoria caché</span><span class="sxs-lookup"><span data-stu-id="0d39c-241">Enumerating the Cache</span></span>

<span data-ttu-id="0d39c-242">Las funciones [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) y [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) enumeran la información almacenada en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-242">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) and [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) functions enumerate the information stored in the cache.</span></span> <span data-ttu-id="0d39c-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) inicia la enumeración tomando un patrón de búsqueda, un búfer y un tamaño de búfer para crear un identificador y devolver la primera entrada de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) starts the enumeration by taking a search pattern, a buffer, and a buffer size to create a handle and return the first cache entry.</span></span> <span data-ttu-id="0d39c-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) toma el identificador creado por [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), un búfer y un tamaño de búfer para devolver la siguiente entrada de caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) takes the handle created by [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), a buffer, and a buffer size to return the next cache entry.</span></span>

<span data-ttu-id="0d39c-245">Ambas funciones almacenan una estructura de información de entrada de caché de Internet en el búfer. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)</span><span class="sxs-lookup"><span data-stu-id="0d39c-245">Both functions store an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure in the buffer.</span></span> <span data-ttu-id="0d39c-246">El tamaño de esta estructura varía para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-246">The size of this structure varies for each entry.</span></span> <span data-ttu-id="0d39c-247">Si el tamaño de búfer que se pasa a cualquiera de las funciones es insuficiente, la función genera un error y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de \_ búfer insuficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="0d39c-247">If the buffer size passed to either function is insufficient, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="0d39c-248">La variable de tamaño de búfer contiene el tamaño de búfer necesario para recuperar esa entrada de caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-248">The buffer size variable contains the buffer size that was needed to retrieve that cache entry.</span></span> <span data-ttu-id="0d39c-249">Se debe asignar un búfer del tamaño indicado por la variable de tamaño de búfer y volver a llamar a la función con el nuevo búfer.</span><span class="sxs-lookup"><span data-stu-id="0d39c-249">A buffer of the size indicated by the buffer size variable should be allocated, and the function should be called again with the new buffer.</span></span>

<span data-ttu-id="0d39c-250">La estructura de información de entrada de caché de Internet contiene el tamaño de la estructura, la dirección URL de la información almacenada en caché, el nombre de archivo local, el tipo de entrada de caché, el recuento de uso, la tasa de aciertos, el tamaño, la hora de última modificación, la expiración, el último acceso, la hora de última sincronización, la información de encabezado [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)</span><span class="sxs-lookup"><span data-stu-id="0d39c-250">The [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="0d39c-251">La función [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) toma un patrón de búsqueda, un búfer que almacena la estructura de información de entrada de caché de [**Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) y el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="0d39c-251">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) function takes a search pattern, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="0d39c-252">Actualmente, solo se implementa el patrón de búsqueda predeterminado, que devuelve todas las entradas de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-252">Currently, only the default search pattern, which returns all cache entries, is implemented.</span></span>

<span data-ttu-id="0d39c-253">Una vez enumerada la memoria caché, la aplicación debe llamar a [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) para cerrar el identificador de la enumeración de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-253">After the cache is enumerated, the application should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) to close the cache enumeration handle.</span></span>

<span data-ttu-id="0d39c-254">En el ejemplo siguiente se muestra la dirección URL de cada entrada de caché en un cuadro de lista, **IDC \_ CacheList**.</span><span class="sxs-lookup"><span data-stu-id="0d39c-254">The following example displays each cache entry's URL in a list box, **IDC\_CacheList**.</span></span> <span data-ttu-id="0d39c-255">Utiliza el \_ tamaño máximo \_ \_ \_ de la información de entrada de caché para asignar inicialmente un búfer, ya que las versiones anteriores de la API WinInet no enumeran la caché correctamente en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0d39c-255">It uses MAX\_CACHE\_ENTRY\_INFO\_SIZE to initially allocate a buffer, since early versions of the WinINet API do not enumerate the cache properly otherwise.</span></span> <span data-ttu-id="0d39c-256">Las versiones posteriores enumeran la caché correctamente y no hay ningún límite de tamaño de caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-256">Later versions do enumerate the cache properly and there is no cache size limit.</span></span> <span data-ttu-id="0d39c-257">Todas las aplicaciones que se ejecutan en equipos con la versión de la API WinINet de Internet Explorer 4,0 deben asignar un búfer del tamaño requerido.</span><span class="sxs-lookup"><span data-stu-id="0d39c-257">All applications that run on computers with the version of the WinINet API from Internet Explorer 4.0 must allocate a buffer of the required size.</span></span> <span data-ttu-id="0d39c-258">Para obtener más información, consulte [uso de búferes](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="0d39c-258">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a><span data-ttu-id="0d39c-259">Recuperando información de entrada de caché</span><span class="sxs-lookup"><span data-stu-id="0d39c-259">Retrieving Cache Entry Information</span></span>

<span data-ttu-id="0d39c-260">La función [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) permite recuperar la estructura [**de \_ \_ \_ información de entrada de caché de Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) para la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-260">The [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) function lets you retrieve the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure for the specified URL.</span></span> <span data-ttu-id="0d39c-261">Esta estructura contiene el tamaño de la estructura, la dirección URL de la información almacenada en caché, el nombre de archivo local, el tipo de entrada de caché, el recuento de uso, la tasa de aciertos, el tamaño, la hora de última modificación, la expiración, el último acceso, la hora de última sincronización, la información de encabezado, el tamaño de la información</span><span class="sxs-lookup"><span data-stu-id="0d39c-261">This structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="0d39c-262">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) acepta una dirección URL, un búfer para una estructura de información de entrada de caché de Internet y el tamaño del búfer. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)</span><span class="sxs-lookup"><span data-stu-id="0d39c-262">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accepts a URL, a buffer for an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="0d39c-263">Si se encuentra la dirección URL, la información se copia en el búfer.</span><span class="sxs-lookup"><span data-stu-id="0d39c-263">If the URL is found, the information is copied into the buffer.</span></span> <span data-ttu-id="0d39c-264">De lo contrario, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el archivo de error \_ \_ no \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="0d39c-264">Otherwise, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="0d39c-265">Si el tamaño del búfer es insuficiente para almacenar la información de la entrada de caché, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de \_ búfer insuficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="0d39c-265">If the buffer size is insufficient to store the cache entry information, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="0d39c-266">El tamaño necesario para recuperar la información se almacena en la variable de tamaño de búfer.</span><span class="sxs-lookup"><span data-stu-id="0d39c-266">The size required to retrieve the information is stored in the buffer size variable.</span></span>

<span data-ttu-id="0d39c-267">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) no realiza ningún análisis de direcciones URL, por lo que una dirección URL que contenga un delimitador ( \# ) no se encontrará en la memoria caché, incluso si el recurso está almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-267">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="0d39c-268">Por ejemplo, si se pasa la dirección URL " https://example.com/example.htm\#sample ", la función devuelve el \_ archivo \_ de error no \_ encontrado aunque " https://example.com/example.htm " esté en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-268">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="0d39c-269">En el ejemplo siguiente se recupera la información de la entrada de caché para la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-269">The following example retrieves the cache entry information for the specified URL.</span></span> <span data-ttu-id="0d39c-270">A continuación, la función muestra la información del encabezado en el cuadro de edición **IDC \_ CacheDump** .</span><span class="sxs-lookup"><span data-stu-id="0d39c-270">The function then displays the header information in the **IDC\_CacheDump** edit box.</span></span>


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a><span data-ttu-id="0d39c-271">Crear una entrada de caché</span><span class="sxs-lookup"><span data-stu-id="0d39c-271">Creating a Cache Entry</span></span>

<span data-ttu-id="0d39c-272">Una aplicación usa las funciones [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) y [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) para crear una entrada de caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-272">An application uses the [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) and [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) functions to create a cache entry.</span></span>

<span data-ttu-id="0d39c-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) acepta la dirección URL, el tamaño de archivo esperado y la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="0d39c-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) accepts the URL, expected file size, and file name extension.</span></span> <span data-ttu-id="0d39c-274">A continuación, la función crea un nombre de archivo local para guardar la entrada de caché que corresponde a la dirección URL y la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="0d39c-274">The function then creates a local file name for saving the cache entry that corresponds to the URL and file name extension.</span></span>

<span data-ttu-id="0d39c-275">Con el nombre de archivo local, escriba los datos en el archivo local.</span><span class="sxs-lookup"><span data-stu-id="0d39c-275">Using the local file name, write the data into the local file.</span></span> <span data-ttu-id="0d39c-276">Una vez que los datos se han escrito en el archivo local, la aplicación debe llamar a [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span><span class="sxs-lookup"><span data-stu-id="0d39c-276">After the data has been written to the local file, the application should call [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>

<span data-ttu-id="0d39c-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) acepta la dirección URL, el nombre de archivo local, la expiración, la hora de última modificación, el tipo de entrada de caché, la información de encabezado, el tamaño de información de encabezado y la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="0d39c-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) accepts the URL, local file name, expiration, last modified time, cache entry type, header information, header information size, and file name extension.</span></span> <span data-ttu-id="0d39c-278">A continuación, la función almacena en caché los datos en el archivo especificado en el almacenamiento en caché y los asocia a la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-278">The function then caches data in the file specified in the cache storage and associates it with the given URL.</span></span>

<span data-ttu-id="0d39c-279">En el ejemplo siguiente se usa el nombre de archivo local, creado por una llamada anterior a [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), almacenado en el cuadro de texto **IDC \_ archivolocal**, para almacenar el texto del cuadro de texto, **IDC \_ CacheDump**, en la entrada de caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-279">The following example uses the local file name, created by a previous call to [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), stored in the text box, **IDC\_LocalFile**, to store the text from the text box, **IDC\_CacheDump**, in the cache entry.</span></span> <span data-ttu-id="0d39c-280">Una vez que los datos se han escrito en el archivo mediante **fopen**, **fprintf** y **fclose**, la entrada se confirma mediante [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span><span class="sxs-lookup"><span data-stu-id="0d39c-280">After the data has been written to the file using **fopen**, **fprintf**, and **fclose**, the entry is committed using [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a><span data-ttu-id="0d39c-281">Eliminar una entrada de caché</span><span class="sxs-lookup"><span data-stu-id="0d39c-281">Deleting a Cache Entry</span></span>

<span data-ttu-id="0d39c-282">La función [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) toma una dirección URL y quita el archivo de caché asociado a ella.</span><span class="sxs-lookup"><span data-stu-id="0d39c-282">The [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) function takes a URL and removes the cache file associated with it.</span></span> <span data-ttu-id="0d39c-283">Si el archivo caché no existe, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el archivo de error \_ \_ no \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="0d39c-283">If the cache file does not exist, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="0d39c-284">Si el archivo caché está actualmente bloqueado o en uso, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error \_ acceso \_ denegado.</span><span class="sxs-lookup"><span data-stu-id="0d39c-284">If the cache file is currently locked or in use, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="0d39c-285">El archivo se elimina cuando se desbloquea.</span><span class="sxs-lookup"><span data-stu-id="0d39c-285">The file is deleted when unlocked.</span></span>

### <a name="retrieving-cache-entry-files"></a><span data-ttu-id="0d39c-286">Recuperando archivos de entrada de caché</span><span class="sxs-lookup"><span data-stu-id="0d39c-286">Retrieving Cache Entry Files</span></span>

<span data-ttu-id="0d39c-287">En el caso de las aplicaciones que requieren el nombre de archivo de un recurso, use las funciones [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) y [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) .</span><span class="sxs-lookup"><span data-stu-id="0d39c-287">For applications that require the file name of a resource, use the [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) and [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) functions.</span></span> <span data-ttu-id="0d39c-288">Las aplicaciones que no requieren el nombre de archivo deben usar las funciones [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)y [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) para recuperar la información de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-288">Applications that do not require the file name should use the [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream), and [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) functions to retrieve the information in the cache.</span></span>

<span data-ttu-id="0d39c-289">[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) no realiza ningún análisis de direcciones URL, por lo que una dirección URL que contenga un delimitador ( \# ) no se encontrará en la memoria caché, incluso si el recurso está almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-289">[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="0d39c-290">Por ejemplo, si se pasa la dirección URL " https://example.com/example.htm\#sample ", la función devuelve el \_ archivo \_ de error no \_ encontrado aunque " https://example.com/example.htm " esté en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-290">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="0d39c-291">[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) acepta una dirección URL, un búfer que almacena la estructura de información de entrada de caché de Internet y el tamaño del búfer. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)</span><span class="sxs-lookup"><span data-stu-id="0d39c-291">[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accepts a URL, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="0d39c-292">La función se recupera y se bloquea para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-292">The function is retrieved and locked for the caller.</span></span>

<span data-ttu-id="0d39c-293">Una vez que se ha usado la información del archivo, la aplicación debe llamar a [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) para desbloquear el archivo.</span><span class="sxs-lookup"><span data-stu-id="0d39c-293">After the information in the file has been used, the application should call [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) to unlock the file.</span></span>

### <a name="cache-groups"></a><span data-ttu-id="0d39c-294">Grupos de caché</span><span class="sxs-lookup"><span data-stu-id="0d39c-294">Cache Groups</span></span>

<span data-ttu-id="0d39c-295">Para crear un grupo de caché, se debe llamar a la función [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) para generar un **GROUPID** para el grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="0d39c-295">To create a cache group, the [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) function must be called to generate a **GROUPID** for the cache group.</span></span> <span data-ttu-id="0d39c-296">Las entradas se pueden agregar al grupo de caché proporcionando la dirección URL de la entrada de caché y la marca de adición del grupo de caché de INTERNET \_ \_ \_ a la función [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) .</span><span class="sxs-lookup"><span data-stu-id="0d39c-296">Entries can be added to the cache group by supplying the cache entry's URL and the INTERNET\_CACHE\_GROUP\_ADD flag to the [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) function.</span></span> <span data-ttu-id="0d39c-297">Para quitar una entrada de la memoria caché de un grupo, pase la dirección URL de la entrada de caché y la marca de eliminación del grupo de caché de INTERNET \_ \_ \_ a [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span><span class="sxs-lookup"><span data-stu-id="0d39c-297">To remove a cache entry from a group, pass the cache entry's URL and the INTERNET\_CACHE\_GROUP\_REMOVE flag to [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span></span>

<span data-ttu-id="0d39c-298">Las funciones [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) y [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) se pueden usar para enumerar las entradas de un grupo de caché especificado.</span><span class="sxs-lookup"><span data-stu-id="0d39c-298">The [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) and [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) functions can be used to enumerate the entries in a specified cache group.</span></span> <span data-ttu-id="0d39c-299">Una vez completada la enumeración, la función debe llamar a [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span><span class="sxs-lookup"><span data-stu-id="0d39c-299">After the enumeration is complete, the function should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span></span>

## <a name="handling-structures-with-variable-size-information"></a><span data-ttu-id="0d39c-300">Controlar estructuras con información de tamaño variable</span><span class="sxs-lookup"><span data-stu-id="0d39c-300">Handling Structures with Variable Size Information</span></span>

<span data-ttu-id="0d39c-301">La memoria caché puede contener información de tamaño variable para cada dirección URL almacenada.</span><span class="sxs-lookup"><span data-stu-id="0d39c-301">The cache can contain variable size information for each URL stored.</span></span> <span data-ttu-id="0d39c-302">Esto se refleja en la estructura de [**información de entrada de caché de Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .</span><span class="sxs-lookup"><span data-stu-id="0d39c-302">This is reflected in the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span> <span data-ttu-id="0d39c-303">Cuando las funciones de caché devuelven esta estructura, crean un búfer que siempre es el tamaño de la información de entrada de caché de Internet más cualquier información de tamaño variable. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)</span><span class="sxs-lookup"><span data-stu-id="0d39c-303">When the cache functions return this structure, they create a buffer that is always the size of [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) plus any variable size information.</span></span> <span data-ttu-id="0d39c-304">Si un miembro de puntero no es **null**, apunta al área de memoria inmediatamente después de la estructura.</span><span class="sxs-lookup"><span data-stu-id="0d39c-304">If a pointer member is not **NULL**, it points to the memory area immediately after the structure.</span></span> <span data-ttu-id="0d39c-305">Mientras se copia el búfer devuelto por una función en otro búfer, los miembros de puntero deben corregirse para que apunten al lugar adecuado en el nuevo búfer, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="0d39c-305">While copying the buffer returned by a function into another buffer, the pointer members should be fixed to point to the appropriate place in the new buffer, as the following example shows.</span></span>

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

<span data-ttu-id="0d39c-306">Algunas funciones de caché generan un error con el \_ mensaje de error de búfer insuficiente \_ si especifica un búfer que es demasiado pequeño para contener la información de entrada de caché recuperada por la función.</span><span class="sxs-lookup"><span data-stu-id="0d39c-306">Some cache functions fail with the ERROR\_INSUFFICIENT\_BUFFER error message if you specify a buffer that is too small to contain the cache entry information retrieved by the function.</span></span> <span data-ttu-id="0d39c-307">En este caso, la función también devuelve el tamaño requerido del búfer.</span><span class="sxs-lookup"><span data-stu-id="0d39c-307">In this case, the function also returns the required size of the buffer.</span></span> <span data-ttu-id="0d39c-308">Después, puede asignar un búfer del tamaño adecuado y volver a llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="0d39c-308">You can then allocate a buffer of the appropriate size and call the function again.</span></span>

> [!Note]  
> <span data-ttu-id="0d39c-309">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="0d39c-309">WinINet does not support server implementations.</span></span> <span data-ttu-id="0d39c-310">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="0d39c-310">In addition, it should not be used from a service.</span></span> <span data-ttu-id="0d39c-311">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="0d39c-311">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
