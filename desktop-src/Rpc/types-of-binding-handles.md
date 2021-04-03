---
title: Tipos de identificadores de enlace
description: Los identificadores de enlace pueden ser automáticos, implícitos o explícitos.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076084"
---
# <a name="types-of-binding-handles"></a><span data-ttu-id="f0088-103">Tipos de identificadores de enlace</span><span class="sxs-lookup"><span data-stu-id="f0088-103">Types of Binding Handles</span></span>

<span data-ttu-id="f0088-104">Los identificadores de enlace pueden ser automáticos, implícitos o explícitos.</span><span class="sxs-lookup"><span data-stu-id="f0088-104">Binding handles can be automatic, implicit, or explicit.</span></span> <span data-ttu-id="f0088-105">Difieren en la cantidad de control que tiene la aplicación sobre el proceso de enlace.</span><span class="sxs-lookup"><span data-stu-id="f0088-105">They differ in the amount of control the application has over the binding process.</span></span> <span data-ttu-id="f0088-106">Como sugiere el nombre, el enlace automático controla el enlace.</span><span class="sxs-lookup"><span data-stu-id="f0088-106">As the name suggests, automatic binding handles automate binding.</span></span> <span data-ttu-id="f0088-107">Las aplicaciones de cliente y de servidor no necesitan código para controlar el proceso de enlace.</span><span class="sxs-lookup"><span data-stu-id="f0088-107">The client and server applications do not need code to handle the binding process.</span></span> <span data-ttu-id="f0088-108">Los identificadores de enlace implícitos permiten a los programas cliente configurar el identificador de enlace antes de que tenga lugar el enlace.</span><span class="sxs-lookup"><span data-stu-id="f0088-108">Implicit binding handles allow client programs to configure the binding handle before the binding takes place.</span></span> <span data-ttu-id="f0088-109">Una vez que el cliente establece un enlace, la biblioteca en tiempo de ejecución de RPC controla el resto.</span><span class="sxs-lookup"><span data-stu-id="f0088-109">After the client establishes a binding, the RPC run-time library handles the rest.</span></span> <span data-ttu-id="f0088-110">Los identificadores de enlace explícitos mueven el control completo sobre el proceso de enlace al código fuente del cliente y los programas del servidor.</span><span class="sxs-lookup"><span data-stu-id="f0088-110">Explicit binding handles move complete control over the binding process into the source code of the client and the server programs.</span></span> <span data-ttu-id="f0088-111">Con este control, se aumenta la complejidad.</span><span class="sxs-lookup"><span data-stu-id="f0088-111">With this control comes increased complexity.</span></span> <span data-ttu-id="f0088-112">La aplicación debe llamar a funciones RPC para administrar el enlace.</span><span class="sxs-lookup"><span data-stu-id="f0088-112">Your application must call RPC functions to manage the binding.</span></span> <span data-ttu-id="f0088-113">No se produce automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f0088-113">It does not happen automatically.</span></span> <span data-ttu-id="f0088-114">Se recomiendan los identificadores de enlace explícitos.</span><span class="sxs-lookup"><span data-stu-id="f0088-114">Explicit binding handles are recommended.</span></span>

<span data-ttu-id="f0088-115">En el diagrama siguiente se muestran las diferencias entre los identificadores de enlace automáticos, implícitos y explícitos.</span><span class="sxs-lookup"><span data-stu-id="f0088-115">The following diagram illustrates the differences between automatic, implicit, and explicit binding handles.</span></span>

![diferencias entre los identificadores de enlace automático, implícito y explícito](images/bhand.png)

<span data-ttu-id="f0088-117">Además, cada identificador de enlace es primitivo o personalizado.</span><span class="sxs-lookup"><span data-stu-id="f0088-117">In addition, every binding handle is either primitive or custom.</span></span> <span data-ttu-id="f0088-118">En los temas siguientes se describe cada tipo de identificador de enlace:</span><span class="sxs-lookup"><span data-stu-id="f0088-118">Each type of binding handle is discussed in the following topics:</span></span>

-   [<span data-ttu-id="f0088-119">Identificadores de enlace automáticos</span><span class="sxs-lookup"><span data-stu-id="f0088-119">Automatic Binding Handles</span></span>](automatic-binding-handles.md)
-   [<span data-ttu-id="f0088-120">Identificadores de enlace implícitos</span><span class="sxs-lookup"><span data-stu-id="f0088-120">Implicit Binding Handles</span></span>](implicit-binding-handles.md)
-   [<span data-ttu-id="f0088-121">Identificadores de enlace explícitos</span><span class="sxs-lookup"><span data-stu-id="f0088-121">Explicit Binding Handles</span></span>](explicit-binding-handles.md)
-   [<span data-ttu-id="f0088-122">Identificadores de enlace primitivos y personalizados</span><span class="sxs-lookup"><span data-stu-id="f0088-122">Primitive and Custom Binding Handles</span></span>](primitive-and-custom-binding-handles.md)

 

 




