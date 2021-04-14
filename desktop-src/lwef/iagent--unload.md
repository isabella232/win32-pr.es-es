---
title: Descarga de IAgent
description: Descarga de IAgent
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358945"
---
# <a name="iagentunload"></a><span data-ttu-id="32fc2-103">IAgent:: Unload</span><span class="sxs-lookup"><span data-stu-id="32fc2-103">IAgent::UnLoad</span></span>

<span data-ttu-id="32fc2-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="32fc2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

<span data-ttu-id="32fc2-105">Descarga los datos de caracteres para el carácter especificado de la colección de [**caracteres**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="32fc2-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="32fc2-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="32fc2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="32fc2-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="32fc2-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="32fc2-108">IDENTIFICADOR del carácter.</span><span class="sxs-lookup"><span data-stu-id="32fc2-108">The character's ID.</span></span>

</dd> </dl>

<span data-ttu-id="32fc2-109">Utilice este método cuando ya no necesite un carácter, para liberar memoria que se utiliza para almacenar información sobre el carácter.</span><span class="sxs-lookup"><span data-stu-id="32fc2-109">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="32fc2-110">Si vuelve a tener acceso al carácter, utilice el método [**Load**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="32fc2-110">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="32fc2-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="32fc2-111">See Also</span></span>

[<span data-ttu-id="32fc2-112">**IAgent:: Load**</span><span class="sxs-lookup"><span data-stu-id="32fc2-112">**IAgent::Load**</span></span>](iagent--load.md)


 

 