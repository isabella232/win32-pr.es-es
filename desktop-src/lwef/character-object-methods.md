---
title: Métodos de objetos de carácter
description: Métodos de objetos de carácter
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bb0dbb256c99660cbce1613c9fdd27d85a92dc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995120"
---
# <a name="character-object-methods"></a><span data-ttu-id="8f15e-103">Métodos de objetos de carácter</span><span class="sxs-lookup"><span data-stu-id="8f15e-103">Character Object Methods</span></span>

<span data-ttu-id="8f15e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8f15e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="8f15e-105">El servidor también expone métodos para cada carácter de una colección de [**caracteres**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="8f15e-105">The server also exposes methods for each character in a [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span> <span data-ttu-id="8f15e-106">Se admiten los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8f15e-106">The following methods are supported:</span></span>

-   [<span data-ttu-id="8f15e-107">**Activar**</span><span class="sxs-lookup"><span data-stu-id="8f15e-107">**Activate**</span></span>](activate-method.md)
-   [<span data-ttu-id="8f15e-108">**GestureAt**</span><span class="sxs-lookup"><span data-stu-id="8f15e-108">**GestureAt**</span></span>](gestureat-method.md)
-   [<span data-ttu-id="8f15e-109">**Obtener**</span><span class="sxs-lookup"><span data-stu-id="8f15e-109">**Get**</span></span>](get-method.md)
-   [<span data-ttu-id="8f15e-110">**Ocultar**</span><span class="sxs-lookup"><span data-stu-id="8f15e-110">**Hide**</span></span>](hide-method.md)
-   [<span data-ttu-id="8f15e-111">**Interrupción**</span><span class="sxs-lookup"><span data-stu-id="8f15e-111">**Interrupt**</span></span>](interrupt-method.md)
-   [<span data-ttu-id="8f15e-112">**Escuchar**</span><span class="sxs-lookup"><span data-stu-id="8f15e-112">**Listen**</span></span>](listen-method.md)
-   [<span data-ttu-id="8f15e-113">**MoveTo**</span><span class="sxs-lookup"><span data-stu-id="8f15e-113">**MoveTo**</span></span>](moveto-method.md)
-   [<span data-ttu-id="8f15e-114">**Reproducir**</span><span class="sxs-lookup"><span data-stu-id="8f15e-114">**Play**</span></span>](play-method.md)
-   [<span data-ttu-id="8f15e-115">**Feria**</span><span class="sxs-lookup"><span data-stu-id="8f15e-115">**Show**</span></span>](show-method.md)
-   [<span data-ttu-id="8f15e-116">**ShowPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="8f15e-116">**ShowPopupMenu**</span></span>](showpopupmenu-method.md)
-   [<span data-ttu-id="8f15e-117">**Speak**</span><span class="sxs-lookup"><span data-stu-id="8f15e-117">**Speak**</span></span>](speak-method.md)
-   [<span data-ttu-id="8f15e-118">**Stop**</span><span class="sxs-lookup"><span data-stu-id="8f15e-118">**Stop**</span></span>](stop-method.md)
-   [<span data-ttu-id="8f15e-119">**StopAll**</span><span class="sxs-lookup"><span data-stu-id="8f15e-119">**StopAll**</span></span>](stopall-method.md)
-   [<span data-ttu-id="8f15e-120">**Opina**</span><span class="sxs-lookup"><span data-stu-id="8f15e-120">**Think**</span></span>](think-method.md)
-   [<span data-ttu-id="8f15e-121">**Esperar**</span><span class="sxs-lookup"><span data-stu-id="8f15e-121">**Wait**</span></span>](wait-method.md)

<span data-ttu-id="8f15e-122">Para usar un método, haga referencia al carácter de la colección.</span><span class="sxs-lookup"><span data-stu-id="8f15e-122">To use a method, reference the character in the collection.</span></span> <span data-ttu-id="8f15e-123">En VBScript y Visual Basic, esto se hace especificando el identificador de un carácter:</span><span class="sxs-lookup"><span data-stu-id="8f15e-123">In VBScript and Visual Basic, you do this by specifying the ID for a character:</span></span>


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



<span data-ttu-id="8f15e-124">Para simplificar la sintaxis del código, puede definir una variable de objeto y establecerla para que haga referencia a un objeto de carácter de la colección de [**caracteres**](/windows/desktop/lwef/the-characters-object) . a continuación, puede usar la variable para hacer referencia a métodos o propiedades del carácter.</span><span class="sxs-lookup"><span data-stu-id="8f15e-124">To simplify the syntax of your code, you can define an object variable and set it to reference a character object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection; then you can use your variable to reference methods or properties of the character.</span></span> <span data-ttu-id="8f15e-125">En el ejemplo siguiente se muestra cómo puede hacerlo con la Visual Basic instrucción set:</span><span class="sxs-lookup"><span data-stu-id="8f15e-125">The following example demonstrates how you can do this using the Visual Basic Set statement:</span></span>


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



<span data-ttu-id="8f15e-126">En Visual Basic 5,0, también puede crear la referencia declarando la variable como un objeto de [**carácter**](/windows/desktop/lwef/the-characters-object):</span><span class="sxs-lookup"><span data-stu-id="8f15e-126">In Visual Basic 5.0, you can also create your reference by declaring your variable as a [**Character**](/windows/desktop/lwef/the-characters-object)object:</span></span>


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



<span data-ttu-id="8f15e-127">Declarar el objeto de tipo IAgentCtlCharacterEx permite el enlace temprano en el objeto, lo que da como resultado un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8f15e-127">Declaring your object of type IAgentCtlCharacterEx enables early binding on the object, which results in better performance.</span></span>

<span data-ttu-id="8f15e-128">En VBScript, no se puede declarar una referencia como un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="8f15e-128">In VBScript, you cannot declare a reference as a particular type.</span></span> <span data-ttu-id="8f15e-129">Sin embargo, simplemente puede declarar la referencia a la variable:</span><span class="sxs-lookup"><span data-stu-id="8f15e-129">However, you can simply declare the variable reference:</span></span>


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



<span data-ttu-id="8f15e-130">Algunos lenguajes de programación no admiten colecciones.</span><span class="sxs-lookup"><span data-stu-id="8f15e-130">Some programming languages do not support collections.</span></span> <span data-ttu-id="8f15e-131">Sin embargo, puede tener acceso a los métodos de un objeto de [**carácter**](/windows/desktop/lwef/the-characters-object) con el método de [**caracteres**](character-method.md) :</span><span class="sxs-lookup"><span data-stu-id="8f15e-131">However, you can access a [**Character**](/windows/desktop/lwef/the-characters-object) object's methods with the [**Character**](character-method.md) method:</span></span>


```
   agent.Characters.Character("CharacterID").method
```



<span data-ttu-id="8f15e-132">Además, también puede crear una referencia al objeto de [**carácter**](/windows/desktop/lwef/the-characters-object) para que el código de script sea más fácil de seguir:</span><span class="sxs-lookup"><span data-stu-id="8f15e-132">In addition, you can also create a reference to the [**Character**](/windows/desktop/lwef/the-characters-object) object to make your script code easier to follow:</span></span>


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 