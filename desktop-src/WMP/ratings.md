---
title: Clasificaciones
description: Clasificaciones
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Aspectos de Windows Media Player Mobile, clasificaciones
- máscaras, clasificaciones
- referencia para máscaras, clasificaciones
- clasificaciones en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714217"
---
# <a name="ratings"></a><span data-ttu-id="7e46b-107">Clasificaciones</span><span class="sxs-lookup"><span data-stu-id="7e46b-107">Ratings</span></span>

<span data-ttu-id="7e46b-108">Al crear una máscara para Windows Media Player 10,1 Mobile, puede mostrar la clasificación asociada al contenido basado en Windows Media Audio que se está reproduciendo actualmente.</span><span class="sxs-lookup"><span data-stu-id="7e46b-108">When you create a skin for Windows Media Player 10.1 Mobile, you can display the rating associated with Windows Media Audio-based content that is currently playing.</span></span> <span data-ttu-id="7e46b-109">La clasificación se muestra en forma de estrella con un número.</span><span class="sxs-lookup"><span data-stu-id="7e46b-109">The rating is displayed as a star with a number on it.</span></span> <span data-ttu-id="7e46b-110">La estrella se numerará de una a cinco, lo que indica la clasificación actual del contenido.</span><span class="sxs-lookup"><span data-stu-id="7e46b-110">The star will be numbered one through five, denoting the current rating for that content.</span></span> <span data-ttu-id="7e46b-111">Si no se clasifica el contenido, la estrella se numerará como cero.</span><span class="sxs-lookup"><span data-stu-id="7e46b-111">If the content is not rated, the star will be numbered zero.</span></span>

<span data-ttu-id="7e46b-112">La sección clasificaciones del archivo de definición de máscara comienza con esta línea:</span><span class="sxs-lookup"><span data-stu-id="7e46b-112">The Ratings section of the skin definition file begins with this line:</span></span>


```C++
[ Ratings ]

```



<span data-ttu-id="7e46b-113">A continuación, debe agregar una línea que contenga información sobre el tamaño y la ubicación del icono de clasificación en la máscara.</span><span class="sxs-lookup"><span data-stu-id="7e46b-113">You then must add a line that contains information about the size and location of your ratings icon in your skin.</span></span>


```C++
147, 3, 22, 21       ratings96S.gif

```



<span data-ttu-id="7e46b-114">Puede usar la siguiente plantilla para la sección clasificaciones del archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="7e46b-114">You can use the following template for the Ratings section of your skin definition file:</span></span>


```C++
// <Location>           <Image>
// ---------------      --------------------
```



<span data-ttu-id="7e46b-115">También puede asignar un valor de clasificación a un elemento multimedia a través de la interfaz de usuario en Windows Media Player 10,1 Mobile y la próxima vez que el dispositivo se sincronice con el equipo, el nuevo valor de clasificación se propagará a ese elemento multimedia si reside en la biblioteca de Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="7e46b-115">You can also assign a ratings value to a media item through the user interface in Windows Media Player 10.1 Mobile, and the next time the device synchronizes with the a computer, the new ratings value will be propagated to that media item if it resides in the Windows Media Player 10 library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e46b-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e46b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e46b-117">**Referencia de máscara**</span><span class="sxs-lookup"><span data-stu-id="7e46b-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




