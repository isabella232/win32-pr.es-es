---
title: Propiedad connected
description: Propiedad connected
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bba78358c7c42f0754da017aa0c188d41acd189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357375"
---
# <a name="connected-property"></a><span data-ttu-id="c74ef-103">Propiedad connected</span><span class="sxs-lookup"><span data-stu-id="c74ef-103">Connected Property</span></span>

<span data-ttu-id="c74ef-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c74ef-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c74ef-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="c74ef-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c74ef-106">Devuelve o establece si el control actual está conectado al servidor de agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c74ef-106">Returns or sets whether the current control is connected to the Microsoft Agent server.</span></span>

</dd> <dt>

<span data-ttu-id="c74ef-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="c74ef-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c74ef-108">*agente. \* \* \* conectado* \*  \[  =  *valor booleano*\]</span><span class="sxs-lookup"><span data-stu-id="c74ef-108">*agent.\*\*\*Connected*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="c74ef-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c74ef-109">Part</span></span>      | <span data-ttu-id="c74ef-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c74ef-110">Description</span></span>                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c74ef-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="c74ef-111">*boolean*</span></span> | <span data-ttu-id="c74ef-112">Una expresión booleana que especifica si el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="c74ef-112">A Boolean expression specifying whether the control is connected.</span></span> <span data-ttu-id="c74ef-113">**True** El control está conectado.</span><span class="sxs-lookup"><span data-stu-id="c74ef-113">**True** The control is connected.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c74ef-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c74ef-114">Remarks</span></span>

<span data-ttu-id="c74ef-115">En muchas situaciones, al especificar el control, se crea automáticamente una conexión con el servidor de agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c74ef-115">In many situations, specifying the control automatically creates a connection with the Microsoft Agent server.</span></span> <span data-ttu-id="c74ef-116">Por ejemplo, si se especifica el CLSID del control del agente de Microsoft en la <OBJECT> etiqueta de una página web, se abre automáticamente una conexión al servidor y se cierra la página.</span><span class="sxs-lookup"><span data-stu-id="c74ef-116">For example, specifying the Microsoft Agent control's CLSID in the <OBJECT> tag in a webpage automatically opens a server connection and exiting the page closes the connection.</span></span> <span data-ttu-id="c74ef-117">De forma similar, para Visual Basic u otros lenguajes que le permitan quitar un control de un formulario, al ejecutar el programa se abre automáticamente una conexión y al salir el programa se cierra la conexión.</span><span class="sxs-lookup"><span data-stu-id="c74ef-117">Similarly, for Visual Basic or other languages that enable you to drop a control on a form, running the program automatically opens a connection and exiting the program closes the connection.</span></span> <span data-ttu-id="c74ef-118">Si el servidor no se está ejecutando, se inicia automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c74ef-118">If the server isn't currently running, it automatically starts.</span></span>

<span data-ttu-id="c74ef-119">Sin embargo, si desea crear un control de agente en tiempo de ejecución, es posible que también necesite abrir explícitamente una nueva conexión al servidor mediante la propiedad **Connected** .</span><span class="sxs-lookup"><span data-stu-id="c74ef-119">However, if you want to create an Agent control at run time, you may also need to explicitly open a new connection to the server using the **Connected** property.</span></span> <span data-ttu-id="c74ef-120">Por ejemplo, en Visual Basic puede crear un objeto ActiveX en tiempo de ejecución mediante la instrucción set con la palabra clave **New** (o la función CreateObject).</span><span class="sxs-lookup"><span data-stu-id="c74ef-120">For example, in Visual Basic you can create an ActiveX object at run time using the Set statement with the **New** keyword (or CreateObject function).</span></span> <span data-ttu-id="c74ef-121">Aunque esto crea el objeto, es posible que no cree la conexión al servidor.</span><span class="sxs-lookup"><span data-stu-id="c74ef-121">While this creates the object, it may not create the connection to the server.</span></span> <span data-ttu-id="c74ef-122">Puede usar la propiedad **Connected** antes del código que llama a la interfaz de programación de Microsoft Agent, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c74ef-122">You can use the **Connected** property before any code that calls into Microsoft Agent's programming interface, as shown in the following example:</span></span>


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



<span data-ttu-id="c74ef-123">La creación de un control con esta técnica no expone los eventos del control del agente.</span><span class="sxs-lookup"><span data-stu-id="c74ef-123">Creating a control using this technique does not expose the Agent control's events.</span></span> <span data-ttu-id="c74ef-124">En Visual Basic 5,0 (y versiones posteriores), puede tener acceso a los eventos del control incluyendo el control en las referencias del proyecto y usar la palabra clave **WithEvents** en la declaración de variable:</span><span class="sxs-lookup"><span data-stu-id="c74ef-124">In Visual Basic 5.0 (and later), you can access the control's events by including the control in your project's references, and use the **WithEvents** keyword in your variable declaration:</span></span>


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



<span data-ttu-id="c74ef-125">Al utilizar **WithEvents** para crear una instancia del control del agente en tiempo de ejecución, se abre automáticamente la conexión con el servidor del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c74ef-125">Using **WithEvents** to create an instance of the Agent control at run time automatically opens the connection with the Microsoft Agent server.</span></span> <span data-ttu-id="c74ef-126">Por lo tanto, no es necesario incluir una instrucción **conectada** .</span><span class="sxs-lookup"><span data-stu-id="c74ef-126">Therefore, you don't need to include a **Connected** statement.</span></span>

<span data-ttu-id="c74ef-127">Puede cerrar la conexión al servidor liberando todas las referencias que creó a objetos de agente, como IAgentCtlCharacterEx y IAgentCtlCommandEx.</span><span class="sxs-lookup"><span data-stu-id="c74ef-127">You can close your connection to the server by releasing all references you created to Agent objects, such as IAgentCtlCharacterEx and IAgentCtlCommandEx.</span></span> <span data-ttu-id="c74ef-128">También debe liberar su referencia al propio control del agente.</span><span class="sxs-lookup"><span data-stu-id="c74ef-128">You must also release your reference to the Agent control itself.</span></span> <span data-ttu-id="c74ef-129">En Visual Basic, puede liberar una referencia a un objeto estableciendo su variable en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="c74ef-129">In Visual Basic, you can release a reference to an object by setting its variable to **Nothing**.</span></span> <span data-ttu-id="c74ef-130">Si ha cargado caracteres, descárguelos antes de liberar el objeto de carácter.</span><span class="sxs-lookup"><span data-stu-id="c74ef-130">If you have loaded characters, unload them before releasing the character object.</span></span>


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> <span data-ttu-id="c74ef-131">No se puede cerrar la conexión al servidor si se liberan las referencias a las que se ha agregado el componente.</span><span class="sxs-lookup"><span data-stu-id="c74ef-131">You cannot close your connection to the server by releasing references where the component has been added.</span></span> <span data-ttu-id="c74ef-132">Por ejemplo, no se puede cerrar la conexión al servidor en páginas web en las que se usa la <OBJECT> etiqueta para declarar el control o en una aplicación Visual Basic en la que se coloca el control en un formulario.</span><span class="sxs-lookup"><span data-stu-id="c74ef-132">For example, you cannot close your connection to the server on webpages where you use the <OBJECT> tag to declare the control or in a Visual Basic application where you drop the control on a form.</span></span> <span data-ttu-id="c74ef-133">Mientras se liberan todas las referencias del agente, se reducirá el espacio de trabajo del agente, la conexión permanecerá hasta que vaya a la página siguiente o salga de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c74ef-133">While releasing all Agent references will reduce Agent's working set, the connection remains until you navigate to the next page or exit the application.</span></span>

 

 

 





