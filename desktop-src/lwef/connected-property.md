---
title: Propiedad Connected
description: Propiedad Connected
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af3a44e97236060733adc55ec6e44eddd0b1d8879250b2a28b54c0bca384cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726110"
---
# <a name="connected-property"></a>Propiedad Connected

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece si el control actual está conectado al servidor de Microsoft Agent.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.:Connected* *  \[  =  *booleano*\]



| Parte      | Descripción                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si el control está conectado. **True** El control está conectado.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

En muchas situaciones, al especificar el control se crea automáticamente una conexión con el servidor de Microsoft Agent. Por ejemplo, si se especifica el CLSID del control Microsoft Agent en la etiqueta de una página web, se abre automáticamente una conexión de servidor y al salir de la página se <OBJECT> cierra la conexión. De forma similar, para Visual Basic u otros lenguajes que le permiten quitar un control en un formulario, al ejecutar el programa se abre automáticamente una conexión y al salir del programa se cierra la conexión. Si el servidor no se está ejecutando actualmente, se inicia automáticamente.

Sin embargo, si desea crear un control agente en tiempo de ejecución, es posible que también tenga que abrir explícitamente una nueva conexión al servidor mediante la **propiedad Conectado.** Por ejemplo, en Visual Basic puede crear un objeto ActiveX en tiempo de ejecución mediante la instrucción Set con la palabra clave **New** (o la función CreateObject). Aunque esto crea el objeto , es posible que no cree la conexión al servidor. Puede usar la propiedad **Connected antes** de cualquier código que llame a la interfaz de programación de Microsoft Agent, como se muestra en el ejemplo siguiente:


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



La creación de un control mediante esta técnica no expone los eventos del control Agente . En Visual Basic 5.0 (y versiones posteriores), puede acceder a los eventos del control incluyendo el control en las referencias del proyecto y usar la palabra clave **WithEvents** en la declaración de variable:


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



Al **usar WithEvents** para crear una instancia del control Agente en tiempo de ejecución, se abre automáticamente la conexión con el servidor de Microsoft Agent. Por lo tanto, no es necesario incluir una **instrucción Connected.**

Puede cerrar la conexión con el servidor liberando todas las referencias que creó a objetos del Agente, como IAgentCtlCharacterEx e IAgentCtlCommandEx. También debe liberar la referencia al propio control agente. En Visual Basic, puede liberar una referencia a un objeto estableciendo su variable en **Nothing**. Si ha cargado caracteres, debe descargarlos antes de liberar el objeto de carácter.


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
> No se puede cerrar la conexión al servidor mediante la publicación de referencias donde se ha agregado el componente. Por ejemplo, no puede cerrar la conexión al servidor en páginas web donde use la etiqueta para declarar el control o en una aplicación Visual Basic donde coloque el control en <OBJECT> un formulario. Aunque liberar todas las referencias del Agente reducirá el conjunto de trabajo del Agente, la conexión permanecerá hasta que vaya a la página siguiente o salga de la aplicación.

 

 

 





