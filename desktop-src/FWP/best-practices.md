---
title: Procedimientos recomendados (plataforma de filtrado de Windows)
description: La lista siguiente contiene los procedimientos recomendados para desarrollar aplicaciones mediante la API de la plataforma de filtrado de Windows (WFP).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533675"
---
# <a name="best-practices-windows-filtering-platform"></a><span data-ttu-id="a9eca-103">Procedimientos recomendados (plataforma de filtrado de Windows)</span><span class="sxs-lookup"><span data-stu-id="a9eca-103">Best Practices (Windows Filtering Platform)</span></span>

<span data-ttu-id="a9eca-104">La lista siguiente contiene los procedimientos recomendados para desarrollar aplicaciones mediante la API de la plataforma de filtrado de Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="a9eca-104">The following list contains best practices for developing applications using the Windows Filtering Platform (WFP) API.</span></span>

-   <span data-ttu-id="a9eca-105">Usar sesiones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="a9eca-105">Use dynamic sessions.</span></span>

    <span data-ttu-id="a9eca-106">Muchas aplicaciones agregan objetos de directiva de filtrado en el inicio y, a continuación, eliminan estos objetos en la detención.</span><span class="sxs-lookup"><span data-stu-id="a9eca-106">Many applications add filtering policy objects at start, and then delete these objects at stop.</span></span> <span data-ttu-id="a9eca-107">Mediante el uso de una sesión dinámica, garantiza que estos objetos se eliminan incluso si se bloquea la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a9eca-107">By using a dynamic session, you guarantee that these objects are deleted even if the application crashes.</span></span> <span data-ttu-id="a9eca-108">Además, simplemente cerrar el identificador del motor en la detención es más eficaz que realizar llamadas individuales para eliminar cada objeto.</span><span class="sxs-lookup"><span data-stu-id="a9eca-108">Furthermore, simply closing the engine handle at stop is more efficient than making individual calls to delete each object.</span></span>

-   <span data-ttu-id="a9eca-109">Controlar los tiempos de espera de la transacción correctamente o establecer la **txnWaitTimeoutInMSec** de sesión en infinita para evitar Tiempos de espera.</span><span class="sxs-lookup"><span data-stu-id="a9eca-109">Either handle transaction timeouts gracefully or set the session **txnWaitTimeoutInMSec** to infinite to prevent timeouts.</span></span>

    <span data-ttu-id="a9eca-110">Incluso si no utiliza transacciones explícitas, la mayoría de las llamadas se siguen ejecutando en una transacción implícita y, por tanto, pueden agotar el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="a9eca-110">Even if you do not use explicit transactions, most calls are still executed under an implicit transaction and thus can timeout.</span></span>

-   <span data-ttu-id="a9eca-111">Use transacciones explícitas para combinar operaciones de adición o eliminación relacionadas en una única transacción.</span><span class="sxs-lookup"><span data-stu-id="a9eca-111">Use explicit transactions to combine related add or delete operations into a single transaction.</span></span>

    <span data-ttu-id="a9eca-112">Esto es más eficaz y facilita la limpieza de los resultados parciales en rutas de acceso de error.</span><span class="sxs-lookup"><span data-stu-id="a9eca-112">This is more efficient and makes it easy to clean up partial results in error paths.</span></span>

-   <span data-ttu-id="a9eca-113">Usar cadenas compatibles con MUI.</span><span class="sxs-lookup"><span data-stu-id="a9eca-113">Use MUI compliant strings.</span></span>

    <span data-ttu-id="a9eca-114">Todas las cadenas localizables se almacenan en una estructura de datos común: [**FWPM \_ Display \_ Data0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span><span class="sxs-lookup"><span data-stu-id="a9eca-114">All the localizable strings are stored in a common data structure: [**FWPM\_DISPLAY\_DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span></span> <span data-ttu-id="a9eca-115">Las cadenas dentro de esta estructura pueden ser cadenas indirectas del tipo admitido por [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span><span class="sxs-lookup"><span data-stu-id="a9eca-115">The strings within this structure can be indirect strings of the type supported by [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span> <span data-ttu-id="a9eca-116">Antes de que una de las funciones devuelva una estructura **FWPM \_ Display \_ Data0** , las cadenas indirectas se resuelven en el recurso de cadena especificado mediante la configuración regional del llamador.</span><span class="sxs-lookup"><span data-stu-id="a9eca-116">Before an **FWPM\_DISPLAY\_DATA0** structure is returned by any of the functions, the indirect strings are resolved to the specified string resource using the caller's locale.</span></span>

-   <span data-ttu-id="a9eca-117">Asociar todos los objetos a un proveedor.</span><span class="sxs-lookup"><span data-stu-id="a9eca-117">Associate all objects to a provider.</span></span>

    <span data-ttu-id="a9eca-118">Cuando hay varios proveedores instalados en el sistema, esto hace que sea más fácil para las herramientas de diagnóstico determinar quién agregó qué.</span><span class="sxs-lookup"><span data-stu-id="a9eca-118">When multiple providers are installed on the system, this makes it is easier for diagnostic tools to determine who added what.</span></span>

-   <span data-ttu-id="a9eca-119">Agregue filtros a su propia subcapa.</span><span class="sxs-lookup"><span data-stu-id="a9eca-119">Add filters to your own sublayer.</span></span>

    <span data-ttu-id="a9eca-120">Una vez que se alcanza un filtro de terminación en una subcapa, no se evalúan más filtros en esa subcapa.</span><span class="sxs-lookup"><span data-stu-id="a9eca-120">Once a terminating filter in a sublayer is hit, no more filters in that sublayer are evaluated.</span></span> <span data-ttu-id="a9eca-121">Por lo tanto, si agrega los filtros a la misma subcapa que otro proveedor, puede impedir que se invoquen los filtros de los demás, lo que produce resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="a9eca-121">Thus, if you add your filters to the same sublayer as another provider, you may prevent each other's filters from being invoked, resulting in unexpected results.</span></span>

-   <span data-ttu-id="a9eca-122">Use el cumplimiento del nivel de aplicación (ALE) en lugar del filtrado orientado a paquetes.</span><span class="sxs-lookup"><span data-stu-id="a9eca-122">Use Application Layer Enforcement (ALE) rather than packet-oriented filtering.</span></span>

    <span data-ttu-id="a9eca-123">El filtrado en la capa de paquetes es lento.</span><span class="sxs-lookup"><span data-stu-id="a9eca-123">Filtering at the packet layer is slow.</span></span>

-   <span data-ttu-id="a9eca-124">Filtre los errores ICMP y los eventos RST antes de que se generen.</span><span class="sxs-lookup"><span data-stu-id="a9eca-124">Filter ICMP errors and RST events before they are generated.</span></span>

    <span data-ttu-id="a9eca-125">Esto es más eficaz que filtrar estos eventos una vez que se generan.</span><span class="sxs-lookup"><span data-stu-id="a9eca-125">This is more efficient that filtering these events after they are generated.</span></span>

-   <span data-ttu-id="a9eca-126">Realizar la inspección de paquetes en el nivel de datos de flujo/datagrama en lugar de en el nivel de transporte.</span><span class="sxs-lookup"><span data-stu-id="a9eca-126">Perform packet inspection at Stream/Datagram Data layer rather than at the Transport layer.</span></span>

    <span data-ttu-id="a9eca-127">Esto se aplica al desarrollo de llamadas.</span><span class="sxs-lookup"><span data-stu-id="a9eca-127">This applies to developing callouts.</span></span> <span data-ttu-id="a9eca-128">Para obtener más información, consulte [consideraciones sobre la programación de controladores de llamada](/windows-hardware/drivers/network/callout-driver-programming-considerations) en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="a9eca-128">For more information, see [Callout Driver Programming Considerations](/windows-hardware/drivers/network/callout-driver-programming-considerations) in the Windows Driver Kit (WDK).</span></span>

-   <span data-ttu-id="a9eca-129">Tenga en cuenta las implicaciones de rendimiento al usar filtros complejos.</span><span class="sxs-lookup"><span data-stu-id="a9eca-129">Consider performance implications when using complex filters.</span></span>

    <span data-ttu-id="a9eca-130">A partir de Windows 7 y Windows Server 2008 R2, los filtros se pueden crear con varias condiciones que usan la misma clave de campo.</span><span class="sxs-lookup"><span data-stu-id="a9eca-130">Starting in Windows 7 and Windows Server 2008 R2, filters can be created with multiple conditions which use the same field key.</span></span> <span data-ttu-id="a9eca-131">Esto permite crear directivas complejas con menos filtros.</span><span class="sxs-lookup"><span data-stu-id="a9eca-131">This allows complex policies to be created with fewer filters.</span></span> <span data-ttu-id="a9eca-132">Sin embargo, estos filtros complejos pueden incurrir en un rendimiento más lento para que el motor de filtro WFP los clasifique.</span><span class="sxs-lookup"><span data-stu-id="a9eca-132">However such complex filters might incur a slower performance for the WFP filter engine to classify.</span></span> <span data-ttu-id="a9eca-133">Se debe realizar una evaluación para determinar si el uso de estos filtros provoca un efecto adverso en el rendimiento general de la solución.</span><span class="sxs-lookup"><span data-stu-id="a9eca-133">An evaluation should be made to determine whether use of such filters causes an adverse effect on the overall performance of your solution.</span></span>

 

 
