---
title: Acerca del objeto PlayerApplication
description: Acerca del objeto PlayerApplication
ms.assetid: 4b77bf16-d7e1-4119-91c2-46136db13e81
keywords:
- Media Player de Windows, objeto PlayerApplication
- Modelo de objetos de Media Player de Windows, objeto PlayerApplication
- modelo de objetos, PlayerApplication (objeto)
- Control ActiveX de Windows Media Player, objeto PlayerApplication
- Control ActiveX, objeto PlayerApplication
- Control ActiveX de Windows Media Player Mobile, objeto PlayerApplication
- Windows Media Player Mobile, objeto PlayerApplication
- Objeto PlayerApplication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d197614ba75a51bdc8ec5398ca757e410f918a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903700"
---
# <a name="about-the-playerapplication-object"></a><span data-ttu-id="50785-111">Acerca del objeto PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="50785-111">About the PlayerApplication Object</span></span>

<span data-ttu-id="50785-112">El objeto **PlayerApplication** se usa para Windows remoting Media Player.</span><span class="sxs-lookup"><span data-stu-id="50785-112">The **PlayerApplication** object is used for remoting Windows Media Player.</span></span> <span data-ttu-id="50785-113">Proporciona la funcionalidad necesaria para cambiar entre un control de Windows Media Player remoto y el modo completo del reproductor.</span><span class="sxs-lookup"><span data-stu-id="50785-113">It provides the functionality required to switch between a remoted Windows Media Player control and the full mode of the Player.</span></span>

<span data-ttu-id="50785-114">La comunicación remota permite a un control de Windows Media Player incrustado en una aplicación de C++ usar el mismo motor de reproducción que el reproductor.</span><span class="sxs-lookup"><span data-stu-id="50785-114">Remoting enables a Windows Media Player control embedded in a C++ application to use the same playback engine as the Player.</span></span> <span data-ttu-id="50785-115">Esto significa que normalmente usará el objeto **PlayerApplication** en el código de C++ mediante las interfaces com.</span><span class="sxs-lookup"><span data-stu-id="50785-115">This means that usually you will use the **PlayerApplication** object in C++ code using the COM interfaces.</span></span> <span data-ttu-id="50785-116">Sin embargo, hay un caso especial en el que puede insertar el control Media Player de Windows que muestra una máscara de Media Player de Windows como su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="50785-116">There is a special case, however, where you can embed the Windows Media Player control that displays a Windows Media Player skin as its user interface.</span></span> <span data-ttu-id="50785-117">En este caso, **PlayerApplication** se puede programar mediante JScript en el código de máscara.</span><span class="sxs-lookup"><span data-stu-id="50785-117">In this case, **PlayerApplication** can be programmed using JScript in the skin code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50785-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50785-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50785-119">**Modelo de objetos del reproductor para lenguajes de scripting**</span><span class="sxs-lookup"><span data-stu-id="50785-119">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="50785-120">**Objeto PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="50785-120">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> </dl>

 

 




