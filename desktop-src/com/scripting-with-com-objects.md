---
title: Scripting con objetos COM
description: Scripting con objetos COM
ms.assetid: d99a561b-67dc-4fc9-adfa-cd7350eb16ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2b00380a14db2d254675a5826b61f262e8cfe8
ms.sourcegitcommit: 8c981a2f4149b4a9d605ffb71fefda8d82bc696e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/24/2019
ms.locfileid: "103783202"
---
# <a name="scripting-with-com-objects"></a>Scripting con objetos COM

Un *lenguaje de scripting* es un lenguaje de programación que se analiza en tiempo de ejecución mediante un *motor de scripting*, un componente que convierte los scripts escritos en ese lenguaje en código máquina. Cada motor de scripting convierte un lenguaje de scripting específico. Un *host de scripting* es una aplicación, como un explorador Web, que hospeda un motor de scripting para ejecutar scripts. Si el host de scripting admite COM, puede escribir scripts que utilicen objetos COM. En los temas siguientes se describen los hosts de scripting que admiten objetos COM, lenguajes de scripting comunes y cómo traducir entre lenguajes de scripting.

Un lenguaje de scripting se diferencia de un lenguaje compilado en que se traduce en código máquina en tiempo de ejecución. Esto significa que cada vez que se ejecuta un script, el motor de scripting analiza primero el código y, a continuación, lo ejecuta. En cambio, los lenguajes compilados, como C++, se traducen en el código máquina una vez, durante la compilación. Al ejecutar una aplicación compilada, el sistema operativo simplemente ejecuta el código precompilado.

Dado que un motor de scripting debe volver a analizar un script cada vez que se ejecuta, los lenguajes de scripting suelen ser más lentos y menos eficientes que sus homólogos precompilados. Sin embargo, la ventaja de los scripts es que son fáciles de escribir y mantener. Los lenguajes de scripting suelen ser más sencillos que los lenguajes precompilados y, cuando un script cambia, no es necesario volver a compilarlos. Para aplicaciones ligeras y que cambian rápidamente, como páginas web, los lenguajes de scripting son ideales.

Hay varios entornos de host en los que se pueden escribir scripts que usan objetos COM, como se describe a continuación:

-   [Incrustar objetos COM en páginas web](embedding-com-objects-in-web-pages.md)
-   [Usar objetos COM en páginas Active Server](using-com-objects-in-active-server-pages.md)
-   [Usar objetos COM en Windows Script Host](using-com-objects-in-windows-script-host.md)
-   [Scripting de objetos COM en aplicaciones personalizadas](scripting-com-objects-in-custom-applications.md)

En cada uno de los entornos de host mencionados anteriormente, un motor de scripting analiza y ejecuta el script. Dado que el motor de cada lenguaje de scripting es un componente independiente, puede Agregar un nuevo lenguaje de scripting a un entorno agregando un nuevo motor.

Los lenguajes de scripting que se usan con más frecuencia son:

-   Microsoft Visual Basic Scripting Edition (VBScript), un subconjunto de Visual Basic.
-   JavaScript, el lenguaje de scripting de Netscape, conocido anteriormente como LiveScript.
-   Software de desarrollo de Microsoft JScript, la implementación de Microsoft de la especificación del lenguaje ECMA 262.

Microsoft proporciona motores de scripting para JScript y VBScript. Otras compañías de software proporcionan motores de scripting ActiveX para lenguajes como PerlScript, PScript, Python y otros.

Para obtener más información, vea la [especificación del lenguaje ECMA 262](https://www.ecma-international.org/publications/standards/Ecma-262.htm).

Tenga en cuenta que la mayoría de los lenguajes de scripting, como VBScript y JScript, no pueden tener acceso a los archivos ni modificarlos. Esta incapacidad impide que el script modifique los datos en los equipos cliente. Sin embargo, los objetos COM no tienen estas limitaciones. Una vez que se descargan e instalan en los equipos cliente, pueden realizar cualquier acción de aplicación estándar. Por lo tanto, los usuarios solo deben descargar y ejecutar controles ActiveX desde orígenes de confianza.

Para obtener información sobre cómo traducir entre lenguajes de scripting, vea los temas siguientes:

-   [Traducir a VBScript](translating-to-vbscript.md)
-   [Traducir a JScript](translating-to-jscript.md)
-   [Traducir a JavaScript](translating-to-javascript.md)

 

 




