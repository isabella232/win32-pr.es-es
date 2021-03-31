---
title: Obtener acceso a los métodos, propiedades y eventos de los controles
description: Obtener acceso a los métodos, propiedades y eventos de los controles
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ad6280b521cf50c2ecd1fb7f1fcec3e2c4164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418633"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a><span data-ttu-id="ab289-103">Obtener acceso a los métodos, propiedades y eventos de los controles</span><span class="sxs-lookup"><span data-stu-id="ab289-103">Accessing the Controls Methods, Properties, and Events</span></span>

<span data-ttu-id="ab289-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ab289-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="ab289-105">El uso del control de Microsoft Agent con Visual Basic es muy similar al uso del control con VBScript, salvo que los eventos de Visual Basic deben incluir el tipo de datos de los parámetros pasados.</span><span class="sxs-lookup"><span data-stu-id="ab289-105">Using Microsoft Agent's control with Visual Basic is very similar to using the control with VBScript, except that events in Visual Basic must include the data type of passed parameters.</span></span> <span data-ttu-id="ab289-106">Al agregar el control de agente de Microsoft a un formulario, se incluirán automáticamente los eventos del agente de Microsoft con los parámetros correspondientes.</span><span class="sxs-lookup"><span data-stu-id="ab289-106">Adding the Microsoft Agent control to a form will automatically include Microsoft Agent's events with their appropriate parameters.</span></span> <span data-ttu-id="ab289-107">También creará automáticamente una conexión al servidor del agente cuando se ejecute la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab289-107">It will also automatically create a connection to the Agent server when the application runs.</span></span>

<span data-ttu-id="ab289-108">También puede usar la sintaxis de creación de object's del lenguaje de programación para crear una instancia del control en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ab289-108">You may also be able to use your programming language's object's creation syntax to create an instance of the control at runtime.</span></span> <span data-ttu-id="ab289-109">Por ejemplo, en Visual Basic (5,0 o posterior), si incluye el control Microsoft Agent 2,0 en las referencias del proyecto, puede usar una [**con eventos**](https://www.bing.com/search?q=**With+Events**). [**Nueva**](https://www.bing.com/search?q=**New**) declaración.</span><span class="sxs-lookup"><span data-stu-id="ab289-109">For example, in Visual Basic (5.0 or later), if you include the Microsoft Agent 2.0 Control in your project's references, you can use a [**With Events**](https://www.bing.com/search?q=**With+Events**)..[**New**](https://www.bing.com/search?q=**New**) declaration.</span></span> <span data-ttu-id="ab289-110">Si no incluye la referencia, VB genera un error que indica que el agente de Microsoft no se pudo iniciar (código de error 80042502).</span><span class="sxs-lookup"><span data-stu-id="ab289-110">If you do not include the reference, VB raises an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

<span data-ttu-id="ab289-111">En el caso de las versiones de VB anteriores a 5,0, puede utilizar la palabra clave [**New**](https://www.bing.com/search?q=**New**) de VB sin la declaración [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) o la función [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) de VB, pero estas convenciones no expondrán los eventos del control del agente.</span><span class="sxs-lookup"><span data-stu-id="ab289-111">For versions of VB prior to 5.0, you can use the VB [**New**](https://www.bing.com/search?q=**New**) keyword without [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) declaration or the VB [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) function, but these conventions will not expose the Agent control's events.</span></span> <span data-ttu-id="ab289-112">También debe usar la propiedad [**Connected**](https://www.bing.com/search?q=**Connected**) antes de hacer referencia a cualquier método o propiedad del agente.</span><span class="sxs-lookup"><span data-stu-id="ab289-112">You also need to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property before you reference any Agent methods or properties.</span></span> <span data-ttu-id="ab289-113">Si no se hace esto, VB producirá un error que indica que el agente de Microsoft no se pudo iniciar (código de error 80042502).</span><span class="sxs-lookup"><span data-stu-id="ab289-113">If this is not done, VB will raise an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

<span data-ttu-id="ab289-114">De forma similar a otros lenguajes de programación, puede que tenga que utilizar la propiedad [**Connected**](https://www.bing.com/search?q=**Connected**) para establecer una conexión con el servidor del modelo de objetos componentes (com) del agente antes de que el código pueda llamar a cualquiera de los métodos o propiedades del control del agente.</span><span class="sxs-lookup"><span data-stu-id="ab289-114">Similarly for other programming languages, you may have to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property to establish a connection to the Agent Component Object Model (COM) server before your code can call any of the Agent control's methods or properties.</span></span> <span data-ttu-id="ab289-115">Además, en algunos lenguajes de programación, es posible que los métodos y las propiedades del agente no se expongan directamente a menos que se declare el control del agente mediante su tipo.</span><span class="sxs-lookup"><span data-stu-id="ab289-115">In addition, for some programming languages, Agent's methods and properties may not be directly exposed unless you declare the Agent control using its type.</span></span> <span data-ttu-id="ab289-116">Por ejemplo, en Microsoft Access 97, debe declarar el objeto como Type Agent para ver los métodos y las propiedades que se muestran en el cuadro desplegable lista de miembros automática al escribir.</span><span class="sxs-lookup"><span data-stu-id="ab289-116">For example, in Microsoft Access 97, you will need to declare the object as type Agent to see the methods and properties display in the Auto List Members drop-down box when you type.</span></span>

<span data-ttu-id="ab289-117">La mayoría de los lenguajes de programación que admiten controles ActiveX siguen convenciones similares a las de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ab289-117">Most programming languages that support ActiveX controls follow conventions similar to Visual Basic.</span></span> <span data-ttu-id="ab289-118">Para los lenguajes de programación que no admiten colecciones de objetos, puede utilizar el método de [**carácter**](https://www.bing.com/search?q=**Character**) y el método de [**comando**](https://www.bing.com/search?q=**Command**) para tener acceso a los métodos y las propiedades de los elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="ab289-118">For programming languages that do not support object collections, you can use the [**Character**](https://www.bing.com/search?q=**Character**) method and [**Command**](https://www.bing.com/search?q=**Command**) method to access methods and properties of items in the collection.</span></span>

<span data-ttu-id="ab289-119">Los lenguajes de programación como Visual Basic, que proporcionan acceso a los tipos de objeto expuestos por el control de agente, permiten utilizarlos en las declaraciones de objeto.</span><span class="sxs-lookup"><span data-stu-id="ab289-119">Programming languages like Visual Basic, that provide access to the object types exposed by the Agent control, enable you to use these in your object declarations.</span></span> <span data-ttu-id="ab289-120">Por ejemplo, en lugar de declarar un objeto como un tipo genérico:</span><span class="sxs-lookup"><span data-stu-id="ab289-120">For example, instead of declaring an object as a generic type:</span></span>

``` syntax
   Dim Genie as Object
```

<span data-ttu-id="ab289-121">Puede declarar un objeto como un tipo específico:</span><span class="sxs-lookup"><span data-stu-id="ab289-121">You can declare an object as a specific type:</span></span>

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

<span data-ttu-id="ab289-122">Esto puede mejorar el rendimiento general de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab289-122">This may improve the overall performance of your application.</span></span>

<span data-ttu-id="ab289-123">En algunos tipos de objetos, puede encontrar dos tipos que son iguales, salvo el sufijo "ex".</span><span class="sxs-lookup"><span data-stu-id="ab289-123">For some object types, you may find two types that are the same except for the "Ex" suffix.</span></span> <span data-ttu-id="ab289-124">Cuando ambos existan, use el tipo "ex", ya que proporciona toda la funcionalidad del agente.</span><span class="sxs-lookup"><span data-stu-id="ab289-124">Where both exist, use the "Ex" type because this provides the full functionality of Agent.</span></span> <span data-ttu-id="ab289-125">Los homólogos que no son "ex" solo se incluyen para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="ab289-125">The non-"Ex" counterparts are included only for backward compatibility.</span></span>

 

 




