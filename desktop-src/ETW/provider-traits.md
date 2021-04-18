---
description: Los rasgos de proveedor son un método para adjuntar más datos a un registro de proveedor individual.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Rasgos de proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985858"
---
# <a name="provider-traits"></a><span data-ttu-id="eb5bc-103">Rasgos de proveedor</span><span class="sxs-lookup"><span data-stu-id="eb5bc-103">Provider Traits</span></span>

<span data-ttu-id="eb5bc-104">Los rasgos de proveedor son un método para adjuntar más datos a un registro de proveedor individual.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-104">Provider Traits are a method of attaching more data to an individual provider registration.</span></span> <span data-ttu-id="eb5bc-105">Se pueden usar para los proveedores de TraceLogging o basados en manifiestos.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-105">They can be used for manifest-based or TraceLogging providers.</span></span> <span data-ttu-id="eb5bc-106">Esto incluye actualmente compatibilidad para agregar un nombre de proveedor o un grupo de proveedores a un registro de proveedor individual.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-106">This currently includes support for adding a Provider Name and/or Provider Group to an individual provider registration.</span></span> <span data-ttu-id="eb5bc-107">Es probable que se agreguen más tipos de rasgos en el futuro.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-107">More trait types are likely to be added in the future.</span></span> <span data-ttu-id="eb5bc-108">Esta información se almacena en el kernel como un BLOB binario con un formato de conjunto.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-108">This information is stored in the kernel as a binary blob of a set format.</span></span>

<span data-ttu-id="eb5bc-109">Los rasgos solo se pueden establecer una vez para un registro.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-109">Traits can only be set once for a registration.</span></span> <span data-ttu-id="eb5bc-110">Se producirá un error en cualquier intento adicional de establecer los rasgos en ese registro.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-110">Any further attempts to set the traits on that registration will fail.</span></span>

<span data-ttu-id="eb5bc-111">Para establecer rasgos de proveedor en un proveedor basado en manifiesto, llame a la función [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) con la clase de información EventProviderSetTraits.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-111">To set Provider Traits on a manifest-based provider, call the [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) function with the EventProviderSetTraits information class.</span></span> <span data-ttu-id="eb5bc-112">El búfer de EventInformation debe contener un BLOB binario con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="eb5bc-112">The EventInformation buffer should contain a binary blob of the following format:</span></span>

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

<span data-ttu-id="eb5bc-113">Los rasgos individuales deben tener el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="eb5bc-113">Individual traits should be in the following format:</span></span>

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

<span data-ttu-id="eb5bc-114">Desde el rasgo individual, el \_ tipo de rasgo del proveedor ETW \_ \_ se define como:</span><span class="sxs-lookup"><span data-stu-id="eb5bc-114">From the individual trait, ETW\_PROVIDER\_TRAIT\_TYPE is defined as:</span></span>

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

<span data-ttu-id="eb5bc-115">Los proveedores de TraceLogging establecen automáticamente los rasgos de proveedor cuando se llama a la función [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) .</span><span class="sxs-lookup"><span data-stu-id="eb5bc-115">TraceLogging providers automatically set the Provider Traits when the [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) function is called.</span></span> <span data-ttu-id="eb5bc-116">El nombre del proveedor de TraceLogging siempre se incluirá en sus rasgos.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-116">The TraceLogging provider's name will always be included in its traits.</span></span> <span data-ttu-id="eb5bc-117">Se puede establecer un grupo en un proveedor TraceLogging mediante la macro [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) en la definición del proveedor.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-117">A group can be set on a TraceLogging provider using the [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) macro in the provider definition.</span></span>

## <a name="custom-traits"></a><span data-ttu-id="eb5bc-118">Rasgos personalizados</span><span class="sxs-lookup"><span data-stu-id="eb5bc-118">Custom Traits</span></span>

<span data-ttu-id="eb5bc-119">Aunque la mayoría de los tipos de rasgos posibles de 255 aún no se han definido, los tipos de rasgos 1-127 están reservados para la definición de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-119">Although most of the 255 possible trait types are not yet defined, trait types 1-127 are reserved for definition by Microsoft.</span></span> <span data-ttu-id="eb5bc-120">Los desarrolladores externos pueden usar los valores de tipo indizados más altos, tal y como se ven.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-120">The remaining higher indexed type values can be used by external developers as they see fit.</span></span> <span data-ttu-id="eb5bc-121">Cualquier persona que considere agregar sus propios rasgos personalizados a su proveedor debe intentar mantener su tamaño total de rasgos en 256 bytes por los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="eb5bc-121">Anyone considering adding their own custom traits to their provider should try to keep their total trait size under 256 bytes for the following reasons:</span></span>

-   <span data-ttu-id="eb5bc-122">Los rasgos se incluyen en cada evento escrito para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-122">The traits are included in every event written for the provider.</span></span> <span data-ttu-id="eb5bc-123">Los rasgos grandes pueden dar lugar a archivos de registro de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-123">Large traits could lead to very large log files.</span></span>
-   <span data-ttu-id="eb5bc-124">Los rasgos se almacenan en un grupo de kernel no paginado durante la vigencia del proveedor.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-124">The traits are stored in nonpaged kernel pool for the lifetime of the provider.</span></span>

## <a name="provider-groups"></a><span data-ttu-id="eb5bc-125">Grupos de proveedores</span><span class="sxs-lookup"><span data-stu-id="eb5bc-125">Provider Groups</span></span>

<span data-ttu-id="eb5bc-126">Un grupo de proveedores es una entidad controlable por GUID muy similar a la de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-126">A provider group is a GUID-defined controllable entity much like a provider itself.</span></span> <span data-ttu-id="eb5bc-127">La principal diferencia es que, mientras que un GUID de proveedor se utiliza para controlar los registros de solo su proveedor, un grupo controlará todos sus registros de miembros.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-127">The key difference is that while a provider GUID is used to control registrations of just its provider, a group will control all of its member registrations.</span></span> <span data-ttu-id="eb5bc-128">Por ejemplo, si se habilita un grupo de proveedores con una palabra clave y un nivel determinados, se habilitarán todos los registros de miembros de grupos con esa palabra clave y el nivel.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-128">For example, enabling a provider group with a given keyword and level will enable all of the groups member registrations with that keyword and level.</span></span>

<span data-ttu-id="eb5bc-129">La pertenencia a grupos puede estar restringida por permisos.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-129">Group membership may be restricted by permissions.</span></span> <span data-ttu-id="eb5bc-130">Si el autor de la llamada de [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) no tiene permisos para unirse al grupo especificado, se denegará la pertenencia.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-130">If the caller of [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) doesn't have permissions to join the specified group, then membership will be denied.</span></span>

<span data-ttu-id="eb5bc-131">En algunos casos, es posible que el controlador de sesión de seguimiento desee excluir algunos proveedores de la habilitación de un grupo.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-131">In some cases the trace session controller may want to exclude a few providers from its enable of a group.</span></span> <span data-ttu-id="eb5bc-132">Esto puede hacerse mediante la configuración de una lista de deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-132">This can be done by setting a disallow list.</span></span> <span data-ttu-id="eb5bc-133">Una lista de no permitidos es una lista de GUID de proveedor que no se habilitará en función de la configuración de grupo para una sesión de registro única.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-133">A disallow list is a list of provider GUIDs that will not be enabled based on the group settings for a single logging session.</span></span> <span data-ttu-id="eb5bc-134">Las listas de no permitidos se pueden cambiar dinámicamente con [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) y la clase de información TraceSetDisallowList.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-134">Disallow lists can be changed dynamically with [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) and the TraceSetDisallowList information class.</span></span>

<span data-ttu-id="eb5bc-135">Aunque la mayoría de las acciones de habilitación se pueden realizar para los grupos de proveedores de una manera similar a los proveedores individuales, hay algunas excepciones.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-135">While most enable actions can be done for Provider Groups in a similar manner to individual providers, there are some exceptions.</span></span> <span data-ttu-id="eb5bc-136">Entre las excepciones se incluyen:</span><span class="sxs-lookup"><span data-stu-id="eb5bc-136">Exceptions include:</span></span>

-   <span data-ttu-id="eb5bc-137">Los grupos de proveedores no se pueden controlar mediante sesiones de seguimiento privadas.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-137">Provider Groups cannot be controlled by private trace sessions.</span></span>
-   <span data-ttu-id="eb5bc-138">Los filtros nombre de evento, ID. de evento y carga no se aplican a los grupos de proveedores cuando asumen información específica de un proveedor individual.</span><span class="sxs-lookup"><span data-stu-id="eb5bc-138">Event Name, Event ID, and Payload filters are not applicable to Provider Groups as they assume specific information of an individual provider.</span></span>

 

 
