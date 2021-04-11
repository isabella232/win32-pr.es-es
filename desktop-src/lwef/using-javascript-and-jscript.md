---
title: Usar JavaScript y JScript
description: Usar JavaScript y JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fbac6d69de69daecbf21c50aafdafce81ed9d95
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149248"
---
# <a name="using-javascript-and-jscript"></a>Usar JavaScript y JScript

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Si usa JavaScript o Microsoft JScript para tener acceso a la interfaz de programación de Microsoft Agent, siga las convenciones de este lenguaje para especificar métodos o propiedades:

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

JavaScript no tiene actualmente sintaxis de eventos para objetos no HTML. Sin embargo, con Internet Explorer puede usar la `<SCRIPT>` etiqueta **for...** Sintaxis del evento:

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

Dado que no todos los exploradores admiten actualmente esta sintaxis de eventos, puede que desee usar JavaScript solo para las páginas que admiten Microsoft Internet Explorer o para el código que no requiere el control de eventos.

Para obtener acceso a las colecciones de objetos del agente, utilice la función de [**enumerador**](https://www.bing.com/search?q=**Enumerator**) de JScript. Sin embargo, las versiones de JScript incluidas antes de Internet Explorer 4,0 no admiten esta función y no admiten colecciones. Para tener acceso a los métodos y las propiedades del objeto de [**carácter**](/windows/desktop/lwef/the-characters-object) , utilice el método de [**caracteres**](character-method.md) . Del mismo modo, para obtener acceso a las propiedades de un objeto [**Command**](/windows/desktop/lwef/the-command-object) , use el método [**Command**](command-method.md) .

 

 