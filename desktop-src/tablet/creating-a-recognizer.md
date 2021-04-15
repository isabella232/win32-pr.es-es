---
description: Si decide hacerlo, la aplicación puede proporcionar sus propias implementaciones de reconocedor. En esta sección se describen los requisitos para crear un reconocedor de aplicación personalizado para la aplicación que se puede usar con la API de la plataforma de Tablet PC.
ms.assetid: 502ef3fb-ba45-4f8b-bbd5-19c24e313439
title: Crear un reconocedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc71f56dc7095c6c72d18b36c3a12caa493ec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696139"
---
# <a name="creating-a-recognizer"></a><span data-ttu-id="f42d6-104">Crear un reconocedor</span><span class="sxs-lookup"><span data-stu-id="f42d6-104">Creating a Recognizer</span></span>

<span data-ttu-id="f42d6-105">Si decide hacerlo, la aplicación puede proporcionar sus propias implementaciones de reconocedor.</span><span class="sxs-lookup"><span data-stu-id="f42d6-105">If you choose to do so, your application can provide its own recognizer implementations.</span></span> <span data-ttu-id="f42d6-106">En esta sección se describen los requisitos para crear un reconocedor de aplicación personalizado para la aplicación que se puede usar con la API de la plataforma de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="f42d6-106">This section describes the requirements for creating a custom application recognizer for your application that you can use with the Tablet PC Platform API.</span></span>

> [!Note]  
> <span data-ttu-id="f42d6-107">Los reconocedores de aplicaciones personalizados no se usan en el panel de entrada de Tablet PC ni en Microsoft Windows Journal.</span><span class="sxs-lookup"><span data-stu-id="f42d6-107">Custom application recognizers are not used by the Tablet PC Input Panel or Microsoft Windows Journal.</span></span> <span data-ttu-id="f42d6-108">Estos accesorios usan solo los reconocedores con los que se han probado.</span><span class="sxs-lookup"><span data-stu-id="f42d6-108">These accessories use only recognizers with which they have been tested.</span></span>

 

<span data-ttu-id="f42d6-109">En las secciones siguientes se detallan las implementaciones de un reconocedor personalizado:</span><span class="sxs-lookup"><span data-stu-id="f42d6-109">The following sections detail the implementation of a custom recognizer:</span></span>

-   [<span data-ttu-id="f42d6-110">Arquitectura de la API de reconocimiento</span><span class="sxs-lookup"><span data-stu-id="f42d6-110">Recognition API Architecture</span></span>](recognition-api-architecture.md)
-   <span data-ttu-id="f42d6-111">[API de reconocimiento necesarias](/previous-versions//ms701664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f42d6-111">[Required Recognition APIs](/previous-versions//ms701664(v=vs.85))</span></span>
-   [<span data-ttu-id="f42d6-112">HRECOGNIZER y HRECOCONTEXT</span><span class="sxs-lookup"><span data-stu-id="f42d6-112">HRECOGNIZER and HRECOCONTEXT</span></span>](hrecognizer-and-hrecocontext.md)
-   [<span data-ttu-id="f42d6-113">Estructura Lattice del reconocedor</span><span class="sxs-lookup"><span data-stu-id="f42d6-113">Recognizer Lattice Structure</span></span>](recognizer-lattice-structure.md)
-   [<span data-ttu-id="f42d6-114">Registro de la DLL del reconocedor</span><span class="sxs-lookup"><span data-stu-id="f42d6-114">Registering Your Recognizer DLL</span></span>](registering-your-recognizer-dll.md)
-   [<span data-ttu-id="f42d6-115">Consideraciones sobre los subprocesos del reconocedor</span><span class="sxs-lookup"><span data-stu-id="f42d6-115">Recognizer Threading Considerations</span></span>](recognizer-threading-considerations.md)
-   [<span data-ttu-id="f42d6-116">Secuencia de llamada típica</span><span class="sxs-lookup"><span data-stu-id="f42d6-116">Typical Calling Sequence</span></span>](typical-calling-sequence.md)
-   [<span data-ttu-id="f42d6-117">Plantilla de ejemplo de DLL de reconocedor</span><span class="sxs-lookup"><span data-stu-id="f42d6-117">Recognizer DLL Sample Template</span></span>](recognizer-dll-sample-template.md)
-   [<span data-ttu-id="f42d6-118">Valores de intervalo Unicode de gestos</span><span class="sxs-lookup"><span data-stu-id="f42d6-118">Unicode Range Values of Gestures</span></span>](unicode-range-values-of-gestures.md)
-   [<span data-ttu-id="f42d6-119">API de reconocedor</span><span class="sxs-lookup"><span data-stu-id="f42d6-119">Recognizer APIs</span></span>](recognizer-apis.md)

 

 
