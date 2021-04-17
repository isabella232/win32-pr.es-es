---
title: El objeto de solicitud
description: El objeto de solicitud
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a50d554a5799af9a434b456113d7c826d2a0aa2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704943"
---
# <a name="the-request-object"></a><span data-ttu-id="7ea9a-103">El objeto de solicitud</span><span class="sxs-lookup"><span data-stu-id="7ea9a-103">The Request Object</span></span>

<span data-ttu-id="7ea9a-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7ea9a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7ea9a-105">El servidor procesa algunos métodos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-105">The server processes some methods asynchronously.</span></span> <span data-ttu-id="7ea9a-106">Esto permite que el código de la aplicación continúe mientras el método se está completando.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-106">This enables your application code to continue while the method is completing.</span></span> <span data-ttu-id="7ea9a-107">Cuando una aplicación cliente llama a uno de estos métodos, el control crea y devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-107">When a client application calls one of these methods, the control creates and returns a [**Request**](/windows/desktop/lwef/the-request-object) object for the request.</span></span> <span data-ttu-id="7ea9a-108">Puede usar el objeto de **solicitud** para realizar el seguimiento del estado del método mediante la asignación de una variable de objeto al método.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-108">You can use the **Request** object to track the status of the method by assigning an object variable to the method.</span></span> <span data-ttu-id="7ea9a-109">En Visual Basic, en primer lugar, declare una variable de objeto:</span><span class="sxs-lookup"><span data-stu-id="7ea9a-109">In Visual Basic, first declare an object variable:</span></span>


```
   Dim MyRequest as Object
```



<span data-ttu-id="7ea9a-110">En VBScript, no se incluye el tipo de variable en la declaración:</span><span class="sxs-lookup"><span data-stu-id="7ea9a-110">In VBScript, you don't include the variable type in your declaration:</span></span>


```
   Dim MyRequest
```



<span data-ttu-id="7ea9a-111">Y use la instrucción set de Visual Basic para asignar la variable a la llamada al método:</span><span class="sxs-lookup"><span data-stu-id="7ea9a-111">And use Visual Basic's Set statement to assign the variable to the method call:</span></span>


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



<span data-ttu-id="7ea9a-112">Esto agrega una referencia al objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="7ea9a-112">This adds a reference to the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="7ea9a-113">El objeto de **solicitud** se destruirá cuando no haya más referencias a él.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-113">The **Request** object will be destroyed when there are no more references to it.</span></span> <span data-ttu-id="7ea9a-114">El punto en el que se declara el objeto de **solicitud** y cómo se usa determina su duración.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-114">Where you declare the **Request** object and how you use it determines its lifetime.</span></span> <span data-ttu-id="7ea9a-115">Si el objeto se declara local a una subrutina o función, se destruirá cuando salga del ámbito; es decir, cuando finaliza la subrutina o la función.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-115">If the object is declared local to a subroutine or function, it will be destroyed when it goes out of scope; that is, when the subroutine or function ends.</span></span> <span data-ttu-id="7ea9a-116">Si el objeto se declara globalmente, no se destruirá hasta que el programa finalice o hasta que se asigne un valor nuevo (o un valor establecido en "Empty") al objeto.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-116">If the object is declared globally, it will not be destroyed until either the program terminates or a new value (or a value set to "empty") is assigned to the object.</span></span>

<span data-ttu-id="7ea9a-117">El objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) proporciona varias propiedades que se pueden consultar.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-117">The [**Request**](/windows/desktop/lwef/the-request-object) object provides several properties you can query.</span></span> <span data-ttu-id="7ea9a-118">Por ejemplo, la propiedad [**status**](status-property.md) devuelve el estado actual de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-118">For example, the [**Status**](status-property.md) property returns the current status of the request.</span></span> <span data-ttu-id="7ea9a-119">Puede usar esta propiedad para comprobar el estado de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="7ea9a-119">You can use this property to check the status of your request:</span></span>


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



<span data-ttu-id="7ea9a-120">La propiedad [**status**](status-property.md) devuelve el estado de un objeto [**request**](/windows/desktop/lwef/the-request-object) como un valor entero largo.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-120">The [**Status**](status-property.md) property returns the status of a [**Request**](/windows/desktop/lwef/the-request-object) object as a Long integer value.</span></span>



| <span data-ttu-id="7ea9a-121">Status</span><span class="sxs-lookup"><span data-stu-id="7ea9a-121">Status</span></span> | <span data-ttu-id="7ea9a-122">Definición</span><span class="sxs-lookup"><span data-stu-id="7ea9a-122">Definition</span></span>                                        |
|--------|---------------------------------------------------|
| <span data-ttu-id="7ea9a-123">0</span><span class="sxs-lookup"><span data-stu-id="7ea9a-123">0</span></span>      | <span data-ttu-id="7ea9a-124">La solicitud se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-124">Request successfully completed.</span></span>                   |
| <span data-ttu-id="7ea9a-125">1</span><span class="sxs-lookup"><span data-stu-id="7ea9a-125">1</span></span>      | <span data-ttu-id="7ea9a-126">Error en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-126">Request failed.</span></span>                                   |
| <span data-ttu-id="7ea9a-127">2</span><span class="sxs-lookup"><span data-stu-id="7ea9a-127">2</span></span>      | <span data-ttu-id="7ea9a-128">Solicitud pendiente (en la cola, pero no completada).</span><span class="sxs-lookup"><span data-stu-id="7ea9a-128">Request pending (in the queue, but not complete).</span></span> |
| <span data-ttu-id="7ea9a-129">3</span><span class="sxs-lookup"><span data-stu-id="7ea9a-129">3</span></span>      | <span data-ttu-id="7ea9a-130">Solicitud interrumpida.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-130">Request interrupted.</span></span>                              |
| <span data-ttu-id="7ea9a-131">4</span><span class="sxs-lookup"><span data-stu-id="7ea9a-131">4</span></span>      | <span data-ttu-id="7ea9a-132">Solicitud en curso.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-132">Request in progress.</span></span>                              |



 

<span data-ttu-id="7ea9a-133">El objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) también incluye un valor entero largo en la propiedad [**Number**](https://www.bing.com/search?q=**Number**) que devuelve el error o la causa del código de [**Estado**](status-property.md) .</span><span class="sxs-lookup"><span data-stu-id="7ea9a-133">The [**Request**](/windows/desktop/lwef/the-request-object) object also includes a Long integer value in the [**Number**](https://www.bing.com/search?q=**Number**) property that returns the error or cause of the [**Status**](status-property.md) code.</span></span> <span data-ttu-id="7ea9a-134">Si no hay ninguno, este valor es cero (0).</span><span class="sxs-lookup"><span data-stu-id="7ea9a-134">If none, this value is zero (0).</span></span> <span data-ttu-id="7ea9a-135">La propiedad [**Description**](description-property.md) contiene un valor de cadena que corresponde al número de error.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-135">The [**Description**](description-property.md) property contains a string value that corresponds to the error number.</span></span> <span data-ttu-id="7ea9a-136">Si la cadena no existe, la **Descripción** contiene "error definido por la aplicación o por el objeto".</span><span class="sxs-lookup"><span data-stu-id="7ea9a-136">If the string doesn't exist, **Description** contains "Application-defined or object-defined error".</span></span>

<span data-ttu-id="7ea9a-137">Para obtener los valores y el significado devueltos por la propiedad [**Number**](https://www.bing.com/search?q=**Number**) , vea [códigos de error](microsoft-agent-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7ea9a-137">For the values and meaning returned by the [**Number**](https://www.bing.com/search?q=**Number**) property, see [Error Codes](microsoft-agent-error-codes.md).</span></span>

<span data-ttu-id="7ea9a-138">El servidor coloca las solicitudes de animación en la cola del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-138">The server places animation requests in the specified character's queue.</span></span> <span data-ttu-id="7ea9a-139">Esto permite al servidor reproducir la animación en un subproceso independiente y el código de la aplicación puede continuar mientras se reproducen las animaciones.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-139">This enables the server to play the animation on a separate thread, and your application's code can continue while animations play.</span></span> <span data-ttu-id="7ea9a-140">Si crea una referencia a un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) , el servidor le notificará automáticamente cuando se haya iniciado o completado una solicitud de animación a través de los eventos [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) y [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) .</span><span class="sxs-lookup"><span data-stu-id="7ea9a-140">If you create a [**Request**](/windows/desktop/lwef/the-request-object) object reference, the server automatically notifies you when an animation request has started or completed through the [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) and [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) events.</span></span> <span data-ttu-id="7ea9a-141">Dado que los métodos que devuelven objetos de **solicitud** son asincrónicos y puede que no se completen durante el ámbito de la función de llamada, declare la referencia al objeto de **solicitud** globalmente.</span><span class="sxs-lookup"><span data-stu-id="7ea9a-141">Because methods that return **Request** objects are asynchronous and may not complete during the scope of the calling function, declare your reference to the **Request** object globally.</span></span>

<span data-ttu-id="7ea9a-142">Los métodos siguientes se pueden usar para devolver un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) : [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**moveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md)y [**Wait**](https://www.bing.com/search?q=**Wait**).</span><span class="sxs-lookup"><span data-stu-id="7ea9a-142">The following methods can be used to return a [**Request**](/windows/desktop/lwef/the-request-object) object: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md), and [**Wait**](https://www.bing.com/search?q=**Wait**).</span></span>

 

 