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
# <a name="accessing-the-controls-methods-properties-and-events"></a>Obtener acceso a los métodos, propiedades y eventos de los controles

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El uso del control de Microsoft Agent con Visual Basic es muy similar al uso del control con VBScript, salvo que los eventos de Visual Basic deben incluir el tipo de datos de los parámetros pasados. Al agregar el control de agente de Microsoft a un formulario, se incluirán automáticamente los eventos del agente de Microsoft con los parámetros correspondientes. También creará automáticamente una conexión al servidor del agente cuando se ejecute la aplicación.

También puede usar la sintaxis de creación de object's del lenguaje de programación para crear una instancia del control en tiempo de ejecución. Por ejemplo, en Visual Basic (5,0 o posterior), si incluye el control Microsoft Agent 2,0 en las referencias del proyecto, puede usar una [**con eventos**](https://www.bing.com/search?q=**With+Events**). [**Nueva**](https://www.bing.com/search?q=**New**) declaración. Si no incluye la referencia, VB genera un error que indica que el agente de Microsoft no se pudo iniciar (código de error 80042502).

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

En el caso de las versiones de VB anteriores a 5,0, puede utilizar la palabra clave [**New**](https://www.bing.com/search?q=**New**) de VB sin la declaración [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) o la función [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) de VB, pero estas convenciones no expondrán los eventos del control del agente. También debe usar la propiedad [**Connected**](https://www.bing.com/search?q=**Connected**) antes de hacer referencia a cualquier método o propiedad del agente. Si no se hace esto, VB producirá un error que indica que el agente de Microsoft no se pudo iniciar (código de error 80042502).

De forma similar a otros lenguajes de programación, puede que tenga que utilizar la propiedad [**Connected**](https://www.bing.com/search?q=**Connected**) para establecer una conexión con el servidor del modelo de objetos componentes (com) del agente antes de que el código pueda llamar a cualquiera de los métodos o propiedades del control del agente. Además, en algunos lenguajes de programación, es posible que los métodos y las propiedades del agente no se expongan directamente a menos que se declare el control del agente mediante su tipo. Por ejemplo, en Microsoft Access 97, debe declarar el objeto como Type Agent para ver los métodos y las propiedades que se muestran en el cuadro desplegable lista de miembros automática al escribir.

La mayoría de los lenguajes de programación que admiten controles ActiveX siguen convenciones similares a las de Visual Basic. Para los lenguajes de programación que no admiten colecciones de objetos, puede utilizar el método de [**carácter**](https://www.bing.com/search?q=**Character**) y el método de [**comando**](https://www.bing.com/search?q=**Command**) para tener acceso a los métodos y las propiedades de los elementos de la colección.

Los lenguajes de programación como Visual Basic, que proporcionan acceso a los tipos de objeto expuestos por el control de agente, permiten utilizarlos en las declaraciones de objeto. Por ejemplo, en lugar de declarar un objeto como un tipo genérico:

``` syntax
   Dim Genie as Object
```

Puede declarar un objeto como un tipo específico:

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

Esto puede mejorar el rendimiento general de la aplicación.

En algunos tipos de objetos, puede encontrar dos tipos que son iguales, salvo el sufijo "ex". Cuando ambos existan, use el tipo "ex", ya que proporciona toda la funcionalidad del agente. Los homólogos que no son "ex" solo se incluyen para la compatibilidad con versiones anteriores.

 

 




