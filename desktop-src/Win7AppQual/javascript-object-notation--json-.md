---
description: .
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: Notación de objetos JavaScript (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b995edc8e83405791a1d96598b827fc77f0204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277332"
---
# <a name="javascript-object-notation-json"></a>Notación de objetos JavaScript (JSON)

[Notación de objetos JavaScript (JSON)](https://www.json.org/) es un formato de intercambio de datos simple y ligero que se basa en un subconjunto de la notación literal de objeto del lenguaje JavaScript. El motor de JavaScript en Windows Internet Explorer 8 implementa la [propuesta JSON de ECMAScript 3,1](https://www.ecma-international.org/) para las funciones nativas de control de JSON (que usa [la API json2.js de Douglas Crockford](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).

Internet Explorer 8 incluye un objeto JSON nativo que cumple con la compatibilidad de JSON que se describe en el [borrador de trabajo de la propuesta es 3.1](https://www.ecma-international.org/). Algunas páginas Web detectan el objeto JSON nativo y, a continuación, lo usan de forma no estándar. Normalmente, este uso provoca un error de script e interrumpe el control de las solicitudes AJAX. En el ejemplo de código siguiente se muestra la manera equivocada de usar el objeto JSON.


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



En su lugar, en el ejemplo de código siguiente se muestra una buena forma de usar el objeto JSON.


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



Windows Internet Explorer incluye compatibilidad nativa con JSON mediante la introducción de un objeto JSON global que tiene dos métodos integrados: **stringify** y **Parse**. El objeto JSON global se define en el motor de JavaScript y se crea durante la fase de inicialización del motor. Para mantener la compatibilidad con versiones anteriores, esta característica solo está disponible cuando un sitio Web usa la versión más reciente de las características de JavaScript mediante el modo de diseño (documento) de "estándares de Internet Explorer 8". Esta característica también podría afectar al comportamiento de las páginas web que dependen de una variable global JSON o usan [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).

Puede invalidar el objeto JSON global. Pero cuando una página Web usa el modo de diseño de "estándares de Internet Explorer 8" (documento), ya no es un objeto sin definir. Dado que el motor de JavaScript crea instancias de JSON como un nombre global, las comprobaciones como "If (! this.JSON)" se evalúan como false y deben cambiarse en el código de usuario.

Es probable que las páginas web que usan [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) no se vean afectadas. Con pocas excepciones, estas páginas deberían funcionar más rápido. Las excepciones se deben a las diferencias entre la implementación de JSON nativa de Internet Explorer y json2.js. Por ejemplo, durante la serialización, la implementación de JSON nativa detecta ciclos y no entra en una recursividad infinita como json.js. Para obtener más información sobre estas excepciones, vea los [blogs de JavaScript](/archive/blogs/jscript/).

Para obtener más información, vea la [documentación de JSON](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) y el [control de versiones y la compatibilidad de versiones del motor de JavaScript](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
