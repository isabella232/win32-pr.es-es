---
title: Diseño de interfaces compatibles con 64 bits
description: Los problemas de compatibilidad con versiones anteriores surgen cuando se agregan nuevos tipos de datos o métodos a una interfaz, se cambian los tipos de datos antiguos o se usan los tipos de datos de forma inadecuada.
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- compatibilidad con versiones anteriores de 64 bits programación de Windows
- interfaces compatibles con 64 bits de programación de Windows de 64 bits
- Guía de programación de Windows de 64 bits, programación de Windows de 64 bits, compatibilidad
- compatibilidad con la programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357056"
---
# <a name="designing-64-bit-compatible-interfaces"></a><span data-ttu-id="195cb-107">Diseño de interfaces compatibles con 64 bits</span><span class="sxs-lookup"><span data-stu-id="195cb-107">Designing 64-bit-Compatible Interfaces</span></span>

<span data-ttu-id="195cb-108">La migración de Windows de 32 bits a Windows de 64 bits no debe, por sí misma, crear problemas para las aplicaciones distribuidas, independientemente de si usan llamadas a procedimiento remoto (RPC) directamente o a través de DCOM.</span><span class="sxs-lookup"><span data-stu-id="195cb-108">Porting from 32-bit Windows to 64-bit Windows should not, by itself, create any problems for distributed applications, whether they use Remote Procedure Calls (RPC) directly or through DCOM.</span></span> <span data-ttu-id="195cb-109">El modelo de programación RPC especifica tamaños de datos bien definidos y tipos enteros que tienen el mismo tamaño en cada extremo de la conexión.</span><span class="sxs-lookup"><span data-stu-id="195cb-109">The RPC programming model specifies well-defined data sizes and integer types that are the same size on each end of the connection.</span></span> <span data-ttu-id="195cb-110">Además, en el modelo de datos Abstract LLP64 desarrollado para Windows de 64 bits, solo los punteros se expanden a 64 bits, todos los demás tipos de datos enteros siguen siendo 32 bits.</span><span class="sxs-lookup"><span data-stu-id="195cb-110">Also, in the LLP64 abstract data model developed for 64-bit Windows, only the pointers expand to 64 bits—all other integer data types remain 32 bits.</span></span> <span data-ttu-id="195cb-111">Dado que los punteros son locales para cada lado de la conexión cliente/servidor y normalmente se transmiten como marcadores **nulos** o no **nulos** , el motor de serialización puede administrar distintos tamaños de puntero en cualquier extremo de una conexión de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="195cb-111">Because pointers are local to each side of the client/server connection and are usually transmitted as **NULL** or non-**NULL** markers, the marshaling engine can handle different pointer sizes on either end of a connection transparently.</span></span>

<span data-ttu-id="195cb-112">Sin embargo, surgen problemas de compatibilidad con versiones anteriores cuando se agregan nuevos tipos de datos o métodos a una interfaz, se cambian los tipos de datos antiguos o se usan los tipos de datos de forma inadecuada.</span><span class="sxs-lookup"><span data-stu-id="195cb-112">However, backward compatibility issues arise when you add new data types or methods to an interface, change old data types, or use data types inappropriately.</span></span> <span data-ttu-id="195cb-113">En los temas siguientes se explica cómo evitar estas situaciones (cuando sea posible) y cómo diseñar soluciones sólidas cuando no es posible evitarlas.</span><span class="sxs-lookup"><span data-stu-id="195cb-113">The following topics discuss how to avoid these situations (when possible) and how to design robust workarounds when it is not possible to avoid them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="195cb-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="195cb-114">In this Section</span></span>

-   [<span data-ttu-id="195cb-115">Cambiar una interfaz existente</span><span class="sxs-lookup"><span data-stu-id="195cb-115">Changing an Existing Interface</span></span>](changing-an-existing-interface.md)
-   [<span data-ttu-id="195cb-116">Evitar la ocultación de información</span><span class="sxs-lookup"><span data-stu-id="195cb-116">Avoiding Information Hiding</span></span>](avoiding-information-hiding.md)
-   [<span data-ttu-id="195cb-117">Evitar el polimorfismo</span><span class="sxs-lookup"><span data-stu-id="195cb-117">Avoiding Polymorphism</span></span>](avoiding-polymorphism.md)
-   [<span data-ttu-id="195cb-118">Usar nuevos tipos de datos en el archivo IDL</span><span class="sxs-lookup"><span data-stu-id="195cb-118">Using New Data Types in Your IDL File</span></span>](using-new-data-types-in-your-idl-file.md)
-   [<span data-ttu-id="195cb-119">Preparación de la aplicación para Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="195cb-119">Preparing Your Application for 64-bit Windows</span></span>](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a><span data-ttu-id="195cb-120">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="195cb-120">Related Sections</span></span>

<span data-ttu-id="195cb-121">Si no está familiarizado con los nuevos tipos de datos, el entorno de trabajo y los cambios de API para Windows de 64 bits, consulte [preparación para Windows de 64](getting-ready-for-64-bit-windows.md)bits.</span><span class="sxs-lookup"><span data-stu-id="195cb-121">If you are not already familiar with the new data types, working environment, and API changes for 64-bit Windows, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

 

 




