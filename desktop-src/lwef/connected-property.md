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
# <a name="connected-property"></a>Propiedad connected

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece si el control actual está conectado al servidor de agente de Microsoft.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente. * * * conectado* *  \[  =  *valor booleano*\]



| Parte      | Descripción                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *boolean* | Una expresión booleana que especifica si el control está conectado. **True** El control está conectado.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

En muchas situaciones, al especificar el control, se crea automáticamente una conexión con el servidor de agente de Microsoft. Por ejemplo, si se especifica el CLSID del control del agente de Microsoft en la <OBJECT> etiqueta de una página web, se abre automáticamente una conexión al servidor y se cierra la página. De forma similar, para Visual Basic u otros lenguajes que le permitan quitar un control de un formulario, al ejecutar el programa se abre automáticamente una conexión y al salir el programa se cierra la conexión. Si el servidor no se está ejecutando, se inicia automáticamente.

Sin embargo, si desea crear un control de agente en tiempo de ejecución, es posible que también necesite abrir explícitamente una nueva conexión al servidor mediante la propiedad **Connected** . Por ejemplo, en Visual Basic puede crear un objeto ActiveX en tiempo de ejecución mediante la instrucción set con la palabra clave **New** (o la función CreateObject). Aunque esto crea el objeto, es posible que no cree la conexión al servidor. Puede usar la propiedad **Connected** antes del código que llama a la interfaz de programación de Microsoft Agent, como se muestra en el ejemplo siguiente:


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



La creación de un control con esta técnica no expone los eventos del control del agente. En Visual Basic 5,0 (y versiones posteriores), puede tener acceso a los eventos del control incluyendo el control en las referencias del proyecto y usar la palabra clave **WithEvents** en la declaración de variable:


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



Al utilizar **WithEvents** para crear una instancia del control del agente en tiempo de ejecución, se abre automáticamente la conexión con el servidor del agente de Microsoft. Por lo tanto, no es necesario incluir una instrucción **conectada** .

Puede cerrar la conexión al servidor liberando todas las referencias que creó a objetos de agente, como IAgentCtlCharacterEx y IAgentCtlCommandEx. También debe liberar su referencia al propio control del agente. En Visual Basic, puede liberar una referencia a un objeto estableciendo su variable en **Nothing**. Si ha cargado caracteres, descárguelos antes de liberar el objeto de carácter.


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
> No se puede cerrar la conexión al servidor si se liberan las referencias a las que se ha agregado el componente. Por ejemplo, no se puede cerrar la conexión al servidor en páginas web en las que se usa la <OBJECT> etiqueta para declarar el control o en una aplicación Visual Basic en la que se coloca el control en un formulario. Mientras se liberan todas las referencias del agente, se reducirá el espacio de trabajo del agente, la conexión permanecerá hasta que vaya a la página siguiente o salga de la aplicación.

 

 

 





