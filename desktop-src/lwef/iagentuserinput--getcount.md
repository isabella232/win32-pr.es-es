---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268202"
---
# <a name="iagentuserinputgetcount"></a><span data-ttu-id="f4e7b-103">IAgentUserInput:: GetCount</span><span class="sxs-lookup"><span data-stu-id="f4e7b-103">IAgentUserInput::GetCount</span></span>

<span data-ttu-id="f4e7b-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f4e7b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

<span data-ttu-id="f4e7b-105">Recupera el número de alternativas de [**comando**](command-event.md) que se pasan a una devolución de llamada de [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="f4e7b-105">Retrieves the number of [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="f4e7b-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f4e7b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f4e7b-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span><span class="sxs-lookup"><span data-stu-id="f4e7b-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span></span>
</dt> <dd>

<span data-ttu-id="f4e7b-108">Dirección de una variable que recibe el recuento de alternativas de [**comandos**](command-event.md) identificadas por el servidor.</span><span class="sxs-lookup"><span data-stu-id="f4e7b-108">Address of a variable that receives the count of [**Commands**](command-event.md) alternatives identified by the server.</span></span>

</dd> </dl>

<span data-ttu-id="f4e7b-109">Si la entrada de voz no era el origen del comando, por ejemplo, si el usuario selecciona el comando en el menú emergente del carácter, **getCount** devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="f4e7b-109">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, **GetCount** returns 1.</span></span> <span data-ttu-id="f4e7b-110">Si **getCount** devuelve cero (0), el motor de reconocimiento de voz detectó una entrada oral pero determinó que no había ningún comando coincidente.</span><span class="sxs-lookup"><span data-stu-id="f4e7b-110">If **GetCount** returns zero (0), the speech recognition engine detected spoken input but determined that there was no matching command.</span></span>

 

 




