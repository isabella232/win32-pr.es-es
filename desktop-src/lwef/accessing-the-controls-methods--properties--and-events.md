---
title: Acceso a los métodos, propiedades y eventos de controles
description: Acceso a los métodos, propiedades y eventos de controles
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed14138da0e6aef0bba46be796813cbe0945195dec2243bbb8bb763ddfb47517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480751"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a>Acceso a los métodos, propiedades y eventos de controles

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El uso del control de Microsoft Agent con Visual Basic es muy similar al uso del control con VBScript, salvo que los eventos de Visual Basic deben incluir el tipo de datos de los parámetros pasados. Al agregar el control Microsoft Agent a un formulario, se incluirán automáticamente los eventos de Microsoft Agent con los parámetros adecuados. También creará automáticamente una conexión al servidor del Agente cuando se ejecute la aplicación.

También puede usar la sintaxis de creación del objeto del lenguaje de programación para crear una instancia del control en tiempo de ejecución. Por ejemplo, en Visual Basic (5.0 o posterior), si incluye el control de Microsoft Agent 2.0 en las referencias del proyecto, puede usar con [**eventos**](https://www.bing.com/search?q=**With+Events**). [**Nueva**](https://www.bing.com/search?q=**New**) declaración. Si no incluye la referencia, VB genera un error que indica que microsoft Agent no se pudo iniciar (código de error 80042502).

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

Para las versiones de VB anteriores a la 5.0, puede usar la palabra clave VB [**New**](https://www.bing.com/search?q=**New**) sin la declaración [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) o la función [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) de VB, pero estas convenciones no expondrán los eventos del control Agente. También debe usar la propiedad [**Connected**](https://www.bing.com/search?q=**Connected**) antes de hacer referencia a cualquier método o propiedad del Agente . Si esto no se hace, VB producirá un error que indica que microsoft Agent no se pudo iniciar (código de error 80042502).

De forma similar para otros lenguajes de programación, es posible que tenga que usar la propiedad [**Connected**](https://www.bing.com/search?q=**Connected**) para establecer una conexión con el servidor del Modelo de objetos componentes (COM) del Agente para que el código pueda llamar a cualquiera de los métodos o propiedades del control Agente. Además, para algunos lenguajes de programación, es posible que los métodos y propiedades del Agente no se exponán directamente a menos que declare el control Agente mediante su tipo. Por ejemplo, en Microsoft Access 97, deberá declarar el objeto como tipo Agente para ver los métodos y propiedades que se muestran en el cuadro desplegable Lista automática de miembros al escribir.

La mayoría de los lenguajes de programación que admiten controles ActiveX siguen convenciones similares a Visual Basic. Para los lenguajes de programación que no admiten colecciones de objetos, puede usar el método [**Character**](https://www.bing.com/search?q=**Character**) y el método [**Command**](https://www.bing.com/search?q=**Command**) para tener acceso a métodos y propiedades de elementos de la colección.

Los lenguajes de programación como Visual Basic, que proporcionan acceso a los tipos de objeto expuestos por el control Agente , permiten usarlos en las declaraciones de objeto. Por ejemplo, en lugar de declarar un objeto como un tipo genérico:

``` syntax
   Dim Genie as Object
```

Puede declarar un objeto como un tipo específico:

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

Esto puede mejorar el rendimiento general de la aplicación.

Para algunos tipos de objeto, puede encontrar dos tipos que son iguales, excepto el sufijo "Ex". Si ambos existen, use el tipo "Ex", ya que proporciona toda la funcionalidad del Agente . Los homólogos que no son "Ex" solo se incluyen por compatibilidad con versiones anteriores.

 

 




