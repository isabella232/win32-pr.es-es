---
description: Notación de objetos JavaScript (JSON)
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: Notación de objetos JavaScript (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1b5f12a2c4e3a4cd0a66a8f917c3cdf41ed17d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088193"
---
# <a name="javascript-object-notation-json"></a>Notación de objetos JavaScript (JSON)

[notación de objetos JavaScript (JSON)](https://www.json.org/) es un formato de intercambio de datos sencillo y ligero que se basa en un subconjunto de la notación literal de objeto del lenguaje JavaScript. El motor de JavaScript de Windows Internet Explorer 8 implementa la propuesta [DE JSON de ECMAScript 3.1](https://www.ecma-international.org/) para funciones nativas de control de JSON (que usa la API de json2.js [de Douglas Crockford).](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)

Internet Explorer 8 incluye un objeto JSON nativo que cumple con la compatibilidad con JSON que se describe en el borrador de trabajo de propuestas [de ES3.1](https://www.ecma-international.org/). Algunas páginas web detectan el objeto JSON nativo y, a continuación, lo usan de forma no estándar. Este uso suele provocar un error de script e interrumpe el control de las solicitudes AJAX. En el ejemplo de código siguiente se muestra la manera incorrecta de usar el objeto JSON.


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



En su lugar, en el ejemplo de código siguiente se muestra una buena manera de usar el objeto JSON.


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



Windows Internet Explorer compatibilidad nativa con JSON mediante la introducción de un objeto JSON global que tiene dos métodos integrados: **stringify** **y parse**. El objeto JSON global se define en el motor de JavaScript y se crea durante la fase de inicialización del motor. Para mantener la compatibilidad con versiones anteriores, esta característica solo está disponible cuando un sitio web usa la versión más reciente de las características de JavaScript mediante el modo de diseño "Internet Explorer 8 Estándares" (documento). Esta característica también puede afectar al comportamiento de las páginas web que dependen de una variable global JSON o usan [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).

Puede invalidar el objeto JSON global. Pero cuando una página web usa el modo de diseño "Internet Explorer 8 Estándares" (documento), ya no es un objeto indefinido. Dado que el motor de JavaScript crea instancias de JSON como un nombre global, las comprobaciones como "if(!this.JSON)" se evalúan como False y deben cambiarse en el código de usuario.

Las páginas web que [ usanjson2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) probablemente no se verán afectadas. Con pocas excepciones, estas páginas deberían funcionar más rápido. Las excepciones se debe a las diferencias entre la implementación Internet Explorer JSON nativa y json2.js. Por ejemplo, durante la serialización, la implementación json nativa detecta ciclos y no entra en recursividad infinita como json.js. Para obtener más información sobre estas excepciones, vea los [blogs de JavaScript](/archive/blogs/jscript/).

Para más información, consulte [Documentación y](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) control de versiones de JSON y Compatibilidad con versiones del motor de [JavaScript.](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
