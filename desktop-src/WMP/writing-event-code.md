---
title: Escribir código de evento
description: Escribir código de evento
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Máscaras de Media Player de Windows, escribir código
- máscaras, escribir código
- eventos, escribir código
- escribir código para máscaras, acerca de
- Aspectos de Windows Media Player, eventos
- máscaras, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076329"
---
# <a name="writing-event-code"></a><span data-ttu-id="6f10a-109">Escribir código de evento</span><span class="sxs-lookup"><span data-stu-id="6f10a-109">Writing Event Code</span></span>

<span data-ttu-id="6f10a-110">Los eventos se tratan de forma similar a los atributos.</span><span class="sxs-lookup"><span data-stu-id="6f10a-110">Events are treated similarly to attributes.</span></span> <span data-ttu-id="6f10a-111">Debe proporcionar un valor al evento y el valor es el código que desea ejecutar cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="6f10a-111">You must give the event a value, and the value is the code you want to run when the event happens.</span></span> <span data-ttu-id="6f10a-112">La palabra "ON" se agrega al principio del nombre del evento; por ejemplo, el evento click pasará a ser **onclick**.</span><span class="sxs-lookup"><span data-stu-id="6f10a-112">The word "on" is added to the front of the event name; for example, the click event will become **onclick**.</span></span>

<span data-ttu-id="6f10a-113">El valor del evento está entre comillas y empieza por la palabra JScript seguido de un signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="6f10a-113">The event value is in double quotes and starts with the word JScript followed by a colon.</span></span> <span data-ttu-id="6f10a-114">El código que desea ejecutar aparece después, seguido de un punto y coma y las comillas dobles de cierre.</span><span class="sxs-lookup"><span data-stu-id="6f10a-114">The code you want to run comes next, followed by a semicolon and the closing double quotes.</span></span> <span data-ttu-id="6f10a-115">Por ejemplo, para detener la reproducción cuando el usuario haga clic en un botón, escriba lo siguiente como un atributo en el código del elemento de **botón** :</span><span class="sxs-lookup"><span data-stu-id="6f10a-115">For example, to stop playing when the user clicks on a button, type the following as an attribute in your **BUTTON** element code:</span></span>


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



<span data-ttu-id="6f10a-116">Si tiene un código que requiere comillas, use comillas simples.</span><span class="sxs-lookup"><span data-stu-id="6f10a-116">If you have a code that requires quotes, use single quotes.</span></span> <span data-ttu-id="6f10a-117">Se debe tener cuidado al usar comillas para que se equilibren correctamente.</span><span class="sxs-lookup"><span data-stu-id="6f10a-117">Care must be taken when using quotation marks so that they are balanced properly.</span></span> <span data-ttu-id="6f10a-118">Este es un ejemplo del uso de ambos tipos:</span><span class="sxs-lookup"><span data-stu-id="6f10a-118">Here is an example of using both types:</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



<span data-ttu-id="6f10a-119">También puede cambiar los atributos de la máscara al controlar un evento externo.</span><span class="sxs-lookup"><span data-stu-id="6f10a-119">You can also change attributes of your skin when handling an external event.</span></span> <span data-ttu-id="6f10a-120">Por ejemplo, para cerrar una vista denominada mi vista, podría escribir:</span><span class="sxs-lookup"><span data-stu-id="6f10a-120">For example, to close a view named myView, you could type:</span></span>


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a><span data-ttu-id="6f10a-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6f10a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f10a-122">**Controlar eventos**</span><span class="sxs-lookup"><span data-stu-id="6f10a-122">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




