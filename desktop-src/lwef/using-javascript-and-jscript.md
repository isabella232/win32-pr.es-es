---
title: Uso de JavaScript y JScript
description: Uso de JavaScript y JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3b32fd3d8e2c8ce9e337f489c27dadaa32bb379d6bc90c6083d62af52bee24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960685"
---
# <a name="using-javascript-and-jscript"></a>Uso de JavaScript y JScript

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Si usa JavaScript o Microsoft JScript para acceder a la interfaz de programación de Microsoft Agent, siga las convenciones de este lenguaje para especificar métodos o propiedades:

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

JavaScript no tiene actualmente sintaxis de eventos para objetos que no son HTML. Sin embargo, Internet Explorer puede usar la `<SCRIPT>` etiqueta **For... Sintaxis de** eventos:

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

Dado que no todos los exploradores admiten actualmente esta sintaxis de eventos, es posible que desee usar JavaScript solo para las páginas que admiten Microsoft Internet Explorer o para el código que no requiere control de eventos.

Para acceder a las colecciones de objetos del Agente , use la JScript [**Enumerator.**](https://www.bing.com/search?q=**Enumerator**) Sin embargo, las versiones JScript incluidas antes de Internet Explorer 4.0 no admiten esta función y no admiten colecciones. Para tener acceso a métodos y propiedades del [**objeto Character,**](/windows/desktop/lwef/the-characters-object) use el [**método Character.**](character-method.md) De forma similar, para acceder a las propiedades de [**un objeto Command,**](/windows/desktop/lwef/the-command-object) use el [**método Command.**](command-method.md)

 

 