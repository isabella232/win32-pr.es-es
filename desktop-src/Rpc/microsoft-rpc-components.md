---
title: Componentes de RPC
description: Componentes de llamada a procedimiento remoto (RPC).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- RPC llamada a procedimiento remoto, descripción, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994282"
---
# <a name="rpc-components"></a><span data-ttu-id="d1a06-104">Componentes de RPC</span><span class="sxs-lookup"><span data-stu-id="d1a06-104">RPC Components</span></span>

<span data-ttu-id="d1a06-105">RPC incluye los componentes principales siguientes:</span><span class="sxs-lookup"><span data-stu-id="d1a06-105">RPC includes the following major components:</span></span>

-   <span data-ttu-id="d1a06-106">Compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="d1a06-106">MIDL compiler</span></span>
-   <span data-ttu-id="d1a06-107">Bibliotecas en tiempo de ejecución y archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d1a06-107">Run-time libraries and header files</span></span>
-   <span data-ttu-id="d1a06-108">Proveedor de servicios de nombres (a veces conocido como localizador)</span><span class="sxs-lookup"><span data-stu-id="d1a06-108">Name service provider (sometimes referred to as the Locator)</span></span>
-   <span data-ttu-id="d1a06-109">Asignador de extremos (a veces denominado asignador de puertos)</span><span class="sxs-lookup"><span data-stu-id="d1a06-109">Endpoint mapper (sometimes referred to as the port mapper)</span></span>

<span data-ttu-id="d1a06-110">En el modelo RPC, puede especificar formalmente una interfaz para los procedimientos remotos mediante un lenguaje diseñado para este fin.</span><span class="sxs-lookup"><span data-stu-id="d1a06-110">In the RPC model, you can formally specify an interface to the remote procedures using a language designed for this purpose.</span></span> <span data-ttu-id="d1a06-111">Este lenguaje se denomina lenguaje de definición de interfaz o IDL.</span><span class="sxs-lookup"><span data-stu-id="d1a06-111">This language is called the Interface Definition Language, or IDL.</span></span> <span data-ttu-id="d1a06-112">La implementación de Microsoft de este lenguaje se denomina Lenguaje de definición de interfaz de Microsoft, o MIDL.</span><span class="sxs-lookup"><span data-stu-id="d1a06-112">The Microsoft implementation of this language is called the Microsoft Interface Definition Language, or MIDL.</span></span>

<span data-ttu-id="d1a06-113">Después de crear una interfaz, debe pasarla a través del compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="d1a06-113">After you create an interface, you must pass it through the MIDL compiler.</span></span> <span data-ttu-id="d1a06-114">Este compilador genera los códigos auxiliares que traducen las llamadas a procedimientos locales en llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="d1a06-114">This compiler generates the stubs that translate local procedure calls into remote procedure calls.</span></span> <span data-ttu-id="d1a06-115">Los códigos auxiliares son funciones de marcador de posición que realizan las llamadas a las funciones de la biblioteca en tiempo de ejecución, que administran la llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="d1a06-115">Stubs are placeholder functions that make the calls to the run-time library functions, which manage the remote procedure call.</span></span> <span data-ttu-id="d1a06-116">La ventaja de este enfoque es que la red es casi completamente transparente para la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="d1a06-116">The advantage of this approach is that the network becomes almost completely transparent to your distributed application.</span></span> <span data-ttu-id="d1a06-117">El programa cliente llama a lo que parece ser un procedimiento local; el trabajo de convertirlos en llamadas remotas se realiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d1a06-117">Your client program calls what appear to be local procedures; the work of turning them into remote calls is done for you automatically.</span></span> <span data-ttu-id="d1a06-118">Todo el código que traduce los datos, accede a la red y recupera los resultados se generan automáticamente mediante el compilador de MIDL y es invisible para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d1a06-118">All the code that translates data, accesses the network, and retrieves results is generated for you by the MIDL compiler and is invisible to your application.</span></span>

 

 




