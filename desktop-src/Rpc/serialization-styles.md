---
title: Estilos de serialización
description: Hay tres estilos que puede usar para manipular los identificadores de serialización.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418909"
---
# <a name="serialization-styles"></a><span data-ttu-id="6c956-103">Estilos de serialización</span><span class="sxs-lookup"><span data-stu-id="6c956-103">Serialization Styles</span></span>

<span data-ttu-id="6c956-104">Hay tres estilos que puede usar para manipular los identificadores de serialización.</span><span class="sxs-lookup"><span data-stu-id="6c956-104">There are three styles you can use to manipulate serialization handles.</span></span> <span data-ttu-id="6c956-105">Dichos componentes son:</span><span class="sxs-lookup"><span data-stu-id="6c956-105">These are:</span></span>

-   [<span data-ttu-id="6c956-106">Serialización de búfer fijo</span><span class="sxs-lookup"><span data-stu-id="6c956-106">Fixed Buffer Serialization</span></span>](fixed-buffer-serialization.md)
-   [<span data-ttu-id="6c956-107">Serialización de búfer dinámico</span><span class="sxs-lookup"><span data-stu-id="6c956-107">Dynamic Buffer Serialization</span></span>](dynamic-buffer-serialization.md)
-   [<span data-ttu-id="6c956-108">Serialización incremental</span><span class="sxs-lookup"><span data-stu-id="6c956-108">Incremental Serialization</span></span>](incremental-serialization.md)

<span data-ttu-id="6c956-109">Independientemente del estilo que use, debe crear un identificador de serialización, serializar los datos y, a continuación, liberar el identificador.</span><span class="sxs-lookup"><span data-stu-id="6c956-109">Regardless of the style you use, you must create a serialization handle, serialize the data, and then free the handle.</span></span> <span data-ttu-id="6c956-110">El estilo se establece cuando el programa crea el identificador y define el modo en que se manipula un búfer.</span><span class="sxs-lookup"><span data-stu-id="6c956-110">The style is set when your program creates the handle and defines the way a buffer is manipulated.</span></span> <span data-ttu-id="6c956-111">El identificador mantiene el contexto adecuado asociado a cada uno de los tres estilos de serialización.</span><span class="sxs-lookup"><span data-stu-id="6c956-111">The handle maintains the appropriate context associated with each of the three serialization styles.</span></span>

 

 




