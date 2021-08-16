---
title: Scripting con objetos COM
description: Scripting con objetos COM
ms.assetid: d99a561b-67dc-4fc9-adfa-cd7350eb16ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c40d94ddd0316d3a921d5d1ecd4591775700c967008ad801cdd8439a341dd9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918386"
---
# <a name="scripting-with-com-objects"></a>Scripting con objetos COM

Un *lenguaje de scripting* es un lenguaje de programación que un motor de *scripting* analiza en tiempo de ejecución, un componente que traduce los scripts escritos en ese lenguaje en código de máquina. Cada motor de scripting traduce un lenguaje de scripting específico. Un *host de scripting* es una aplicación, como un explorador web, que hospeda un motor de scripting para ejecutar scripts. Si el host de scripting admite COM, puede escribir scripts que usen objetos COM. En los temas siguientes se describen los hosts de scripting que admiten objetos COM, lenguajes de scripting comunes y cómo traducir entre lenguajes de scripting.

Un lenguaje de scripting difiere de un lenguaje compilado en que se traduce en código de máquina en tiempo de ejecución. Esto significa que cada vez que se ejecuta un script, el motor de scripting analiza primero el código y, a continuación, lo ejecuta. Por el contrario, los lenguajes compilados, como C++, se traducen al código del equipo una vez, durante la compilación. Cuando se ejecuta una aplicación compilada, el sistema operativo simplemente ejecuta el código precompilado.

Dado que un motor de scripting debe volver a generar un script cada vez que se ejecuta, los lenguajes de scripting suelen ser más lentos y menos eficaces que sus homólogos precompilados. Sin embargo, la ventaja de los scripts es que son fáciles de escribir y mantener. Los lenguajes de scripting suelen ser más sencillos que los precompilados y, cuando cambia un script, no es necesario volver a compilarlo. Para aplicaciones ligeras y que cambian rápidamente, como páginas web, los lenguajes de scripting son ideales.

Hay varios entornos host en los que puede escribir scripts que usan objetos COM, como se describe a continuación:

-   [Insertar objetos COM en páginas web](embedding-com-objects-in-web-pages.md)
-   [Uso de objetos COM en Active Server Pages](using-com-objects-in-active-server-pages.md)
-   [Uso de objetos COM en Windows host de script](using-com-objects-in-windows-script-host.md)
-   [Scripting de objetos COM en aplicaciones personalizadas](scripting-com-objects-in-custom-applications.md)

En cada uno de los entornos de host mencionados anteriormente, un motor de scripting analiza y ejecuta el script. Dado que el motor de cada lenguaje de scripting es un componente independiente, puede agregar un nuevo lenguaje de scripting a un entorno agregando un nuevo motor.

Los lenguajes de scripting más usados son:

-   Microsoft Visual Basic Scripting Edition (VBScript), un subconjunto de Visual Basic.
-   JavaScript, el lenguaje de scripting netscape, anteriormente conocido como LiveScript.
-   Microsoft JScript software de desarrollo, la implementación de Microsoft de la especificación del lenguaje ECMA 262.

Microsoft proporciona motores de scripting para JScript y VBScript. Otras empresas de software ActiveX motores de scripting para lenguajes como PerlScript, PScript, Python y otros.

Para obtener más información, consulte la [especificación del lenguaje ECMA 262](https://www.ecma-international.org/publications/standards/Ecma-262.htm).

Tenga en cuenta que la mayoría de los lenguajes de scripting, como VBScript JScript, no pueden acceder a archivos ni modificarlos. Esta incapacidad impide que el script modifique los datos en los equipos cliente. Sin embargo, los objetos COM no tienen tales limitaciones. Una vez que se descargan e instalan en equipos cliente, pueden realizar cualquier acción de aplicación estándar. Por lo tanto, los usuarios solo deben descargar y ejecutar controles ActiveX desde orígenes de confianza.

Para obtener información sobre la traducción entre lenguajes de scripting, vea los temas siguientes:

-   [Traducción a VBScript](translating-to-vbscript.md)
-   [Traducción a JScript](translating-to-jscript.md)
-   [Traducción a JavaScript](translating-to-javascript.md)

 

 




