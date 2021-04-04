---
title: Atributos de rendimiento
description: Use los atributos siguientes en un archivo IDL para reducir el tamaño del código auxiliar o mejorar el rendimiento.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- MIDL, atributos y rendimiento de IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076361"
---
# <a name="performance-attributes"></a><span data-ttu-id="6120d-104">Atributos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="6120d-104">Performance Attributes</span></span>

<span data-ttu-id="6120d-105">Use los atributos siguientes en un archivo IDL para reducir el tamaño del código auxiliar o mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="6120d-105">Use the following attributes in an IDL file to reduce the size of the stub code or otherwise improve performance.</span></span>



| <span data-ttu-id="6120d-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="6120d-106">Attribute</span></span>                             | <span data-ttu-id="6120d-107">Uso</span><span class="sxs-lookup"><span data-stu-id="6120d-107">Usage</span></span>                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6120d-108">**omitir**</span><span class="sxs-lookup"><span data-stu-id="6120d-108">**ignore**</span></span>](ignore.md)              | <span data-ttu-id="6120d-109">Designa que un puntero contenido en una estructura o Unión y el objeto indicado por el puntero no se va a transmitir.</span><span class="sxs-lookup"><span data-stu-id="6120d-109">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span>                        |
| [<span data-ttu-id="6120d-110">**localizar**</span><span class="sxs-lookup"><span data-stu-id="6120d-110">**local**</span></span>](local.md)                | <span data-ttu-id="6120d-111">Designa una función que es local para la aplicación para la que MIDL no necesita generar código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="6120d-111">Designates a function that is local to the application for which MIDL does not need to generate stub code.</span></span>                                           |
| [<span data-ttu-id="6120d-112">**\_serialización de cable**</span><span class="sxs-lookup"><span data-stu-id="6120d-112">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="6120d-113">Define un tipo de datos como un tipo más simple para la transmisión a través de una red y le permite implementar la serialización y la desserialización de rutinas para el tipo.</span><span class="sxs-lookup"><span data-stu-id="6120d-113">Defines a data type as a simpler type for transmission over a network and allows you to implement marshaling and unmarshaling routines for the type.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6120d-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6120d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6120d-115">Atributos ACF de administración de memoria</span><span class="sxs-lookup"><span data-stu-id="6120d-115">Memory Management ACF Attributes</span></span>](memory-management-acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="6120d-116">Atributos ACF de optimización de código auxiliar</span><span class="sxs-lookup"><span data-stu-id="6120d-116">Stub Optimization ACF Attributes</span></span>](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




