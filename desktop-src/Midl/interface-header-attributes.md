---
title: Atributos de encabezado de interfaz
description: Incorpore estos atributos en el encabezado de la interfaz para transmitir información sobre toda la interfaz.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- MIDL, atributos y encabezado de interfaz IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075528"
---
# <a name="interface-header-attributes"></a><span data-ttu-id="6776a-104">Atributos de encabezado de interfaz</span><span class="sxs-lookup"><span data-stu-id="6776a-104">Interface Header Attributes</span></span>

<span data-ttu-id="6776a-105">Incorpore estos atributos en el encabezado de la interfaz para transmitir información sobre toda la interfaz.</span><span class="sxs-lookup"><span data-stu-id="6776a-105">Incorporate these attributes in the interface header to convey information about the entire interface.</span></span>



| <span data-ttu-id="6776a-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="6776a-106">Attribute</span></span>                                   | <span data-ttu-id="6776a-107">Uso</span><span class="sxs-lookup"><span data-stu-id="6776a-107">Usage</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6776a-108">**\_UUID asincrónico**</span><span class="sxs-lookup"><span data-stu-id="6776a-108">**async\_uuid**</span></span>](async-uuid.md)           | <span data-ttu-id="6776a-109">Indica al compilador de MIDL que defina las versiones sincrónicas y asincrónicas de una interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="6776a-109">Directs the MIDL compiler to define both synchronous and asynchronous versions of a COM interface.</span></span>                                                                                                                                               |
| [<span data-ttu-id="6776a-110">**uuid**</span><span class="sxs-lookup"><span data-stu-id="6776a-110">**uuid**</span></span>](uuid.md)                        | <span data-ttu-id="6776a-111">Designa un valor de 128 bits que distingue una interfaz determinada de las demás.</span><span class="sxs-lookup"><span data-stu-id="6776a-111">Designates a 128-bit value that distinguishes a particular interface from all others.</span></span> <span data-ttu-id="6776a-112">El valor real puede representar un GUID, un CLSID o un IID.</span><span class="sxs-lookup"><span data-stu-id="6776a-112">The actual value may represent a GUID, a CLSID, or an IID.</span></span>                                                                                                 |
| [<span data-ttu-id="6776a-113">**localizar**</span><span class="sxs-lookup"><span data-stu-id="6776a-113">**local**</span></span>](local.md)                      | <span data-ttu-id="6776a-114">Indica al compilador de MIDL que genere solo archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="6776a-114">Directs the MIDL compiler to generate header files only.</span></span> <span data-ttu-id="6776a-115">Una interfaz debe tener un [**UUID**](uuid.md) o un atributo [**local**](local.md) .</span><span class="sxs-lookup"><span data-stu-id="6776a-115">An interface must have either a [**uuid**](uuid.md) or a [**local**](local.md) attribute.</span></span>                                                                                             |
| [<span data-ttu-id="6776a-116">**Unión de MS \_**</span><span class="sxs-lookup"><span data-stu-id="6776a-116">**ms\_union**</span></span>](-ms-union.md)              | <span data-ttu-id="6776a-117">Controla la alineación del NDR de las uniones no encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="6776a-117">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="6776a-118">Se utiliza para la compatibilidad con versiones anteriores con interfaces basadas en MIDL 1,0 o 2,0.</span><span class="sxs-lookup"><span data-stu-id="6776a-118">Use for backward compatibility with interfaces built on MIDL 1.0 or 2.0.</span></span>                                                                                                                   |
| [<span data-ttu-id="6776a-119">**objeto**</span><span class="sxs-lookup"><span data-stu-id="6776a-119">**object**</span></span>](object.md)                    | <span data-ttu-id="6776a-120">Identifica la interfaz como una interfaz COM y dirige el compilador de MIDL para que genere código de proxy o código auxiliar en lugar de los códigos auxiliares de cliente y servidor de RPC.</span><span class="sxs-lookup"><span data-stu-id="6776a-120">Identifies the interface as a COM interface and directs the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span>                                                                                                    |
| [<span data-ttu-id="6776a-121">**Versión**</span><span class="sxs-lookup"><span data-stu-id="6776a-121">**version**</span></span>](version.md)                  | <span data-ttu-id="6776a-122">Identifica una versión concreta de una interfaz en los casos en que existen varias versiones de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="6776a-122">Identifies a particular version of an interface in cases where multiple versions of the interface exist.</span></span> <span data-ttu-id="6776a-123">Dado que las interfaces COM son inmutables, no puede usar el atributo [**version**](version.md) en una interfaz de [**objeto**](object.md) .</span><span class="sxs-lookup"><span data-stu-id="6776a-123">Because COM interfaces are immutable, you cannot use the [**version**](version.md) attribute on an [**object**](object.md) interface.</span></span> |
| [<span data-ttu-id="6776a-124">**puntero \_ predeterminado**</span><span class="sxs-lookup"><span data-stu-id="6776a-124">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="6776a-125">Especifica el tipo de puntero predeterminado para todos los punteros excepto los incluidos en las listas de parámetros.</span><span class="sxs-lookup"><span data-stu-id="6776a-125">Specifies the default pointer type for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="6776a-126">El tipo predeterminado puede ser [**Unique**](unique.md), [**ref**](ref.md)o [**ptr**](ptr.md).</span><span class="sxs-lookup"><span data-stu-id="6776a-126">The default type can be [**unique**](unique.md), [**ref**](ref.md), or [**ptr**](ptr.md).</span></span>                                                   |
| [<span data-ttu-id="6776a-127">**finales**</span><span class="sxs-lookup"><span data-stu-id="6776a-127">**endpoint**</span></span>](endpoint.md)                | <span data-ttu-id="6776a-128">Especifica un punto de conexión estático (conocido) en el que una aplicación de servidor escuchará las llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="6776a-128">Specifies a static (well-known) endpoint on which a server application will listen for remote procedure calls.</span></span>                                                                                                                                   |



 

<span data-ttu-id="6776a-129">Vea [atributos](type-library-attributes.md) de la biblioteca de tipos para los atributos de interfaz, como [**dual**](dual.md) y [**oleautomation**](oleautomation.md), que son específicos de las interfaces definidas o a las que se hace referencia dentro de una instrucción Library.</span><span class="sxs-lookup"><span data-stu-id="6776a-129">See [Type Library Attributes](type-library-attributes.md) for interface attributes, such as [**dual**](dual.md) and [**oleautomation**](oleautomation.md), that are specific to interfaces defined or referenced inside a library statement.</span></span>

 

 




