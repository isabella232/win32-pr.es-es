---
description: Conceptos fundamentales de MUI explicados
ms.assetid: 9ab19a56-4d31-471d-949e-a539751b62e3
title: Conceptos fundamentales de MUI explicados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dbeedb246944bef6c23c739eafddff86423b35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001394"
---
# <a name="mui-fundamental-concepts-explained"></a>Conceptos fundamentales de MUI explicados

-   [Requisito previo para MUI](#prerequisite-for-mui)
-   [Separación del código fuente de recursos específicos del lenguaje](#separation-of-source-code-from-language-specific-resources)
    -   [Los primeros días: código y recursos en directo](#the-early-days-code-and-resources-live-together)
    -   [Separación lógica del código y recursos localizables](#logically-separating-code-and-localizable-resources)
    -   [Separación física de código y recursos](#physically-separating-code-and-resources)
-   [Cargar dinámicamente recursos específicos del idioma](#dynamically-loading-language-specific-resources)
-   [Compilar aplicaciones de MUI](#building-mui-applications)

## <a name="prerequisite-for-mui"></a>Requisito previo para MUI

El requisito previo básico para crear una aplicación compatible con MUI para Windows Vista y más allá es diseñar la aplicación de acuerdo con las [directrices de globalización](https://msdn.microsoft.com/goglobal/bb688110.aspx)de Windows.

## <a name="separation-of-source-code-from-language-specific-resources"></a>Separación del código fuente de recursos específicos del lenguaje

Una de las instalaciones fundamentales de la tecnología MUI es la separación del código fuente de la aplicación de los recursos específicos del lenguaje, para habilitar escenarios multilingües en las aplicaciones de forma más eficaz. La separación del código y los recursos se ha logrado a través de diferentes mecanismos y a distintos grados a lo largo del tiempo, como se describe en las secciones siguientes. Cada método proporcionaba distintos grados de flexibilidad a la hora de compilar, implementar y dar servicio a la aplicación.

La solución recomendada para las aplicaciones compatibles con MUI es el último método que se describe aquí, es decir, la separación física de los recursos y el código fuente de la aplicación, con los propios recursos divididos en un archivo por cada idioma admitido para obtener la máxima flexibilidad en la compilación, implementación y mantenimiento.

### <a name="the-early-days-code-and-resources-live-together"></a>Los primeros días: código y recursos en directo

Inicialmente, las aplicaciones localizadas se crearon editando el código fuente y cambiando los recursos (normalmente cadenas) en el propio código y volviendo a compilar las aplicaciones. Esto significaba que para generar una versión localizada, una tenía que copiar el código fuente original, trasladar los elementos de texto (recursos) dentro del código fuente y volver a compilar el código. En la imagen siguiente se muestra el código de aplicación con texto que debe localizarse.

![diagrama conceptual en el que se muestra una aplicación que contiene unidades de recursos de texto incrustado](images/mui-fundamental-concepts-explained-fig3.gif)

Aunque este enfoque permite la creación de aplicaciones localizadas, también tiene importantes desventajas:

-   Requiere varias versiones del código fuente, al menos una para el lenguaje de origen y otra para cada uno de los idiomas de destino. Esto crea problemas significativos al sincronizar las diferentes versiones de idioma de la aplicación. En concreto, cuando es necesario corregir un defecto en el código, el defecto debe corregirse en cada copia del código fuente (uno por idioma).
-   También es extremadamente propenso a errores, ya que los localizadores necesarios, que no son desarrolladores, pueden realizar modificaciones en el código fuente, lo que crea un riesgo considerable en términos de integridad del código.

La combinación de estos inconvenientes hace que esta sea una propuesta muy ineficaz y se necesitaba un modelo mejor.

### <a name="logically-separating-code-and-localizable-resources"></a>Separación lógica del código y recursos localizables

Una mejora significativa con respecto al modelo anterior es la separación lógica del código y los recursos localizables de una aplicación. De este modo, se aísla el código de los recursos y se asegura de que el código permanezca intacto cuando la localización cambie los recursos. Desde el punto de vista de la implementación, las cadenas y otros elementos de la interfaz de usuario se almacenan en archivos de recursos, que son relativamente fáciles de traducir y se separan lógicamente de las secciones de código.

Idealmente, agregar compatibilidad para cualquier lenguaje determinado puede ser tan sencillo como traducir los recursos localizables en este nuevo lenguaje y usar estos recursos traducidos para crear una nueva versión localizada de la aplicación, sin necesidad de modificar el código. En la imagen siguiente se muestra cómo el código y los recursos localizables se deben separar lógicamente dentro de una aplicación.

![diagrama conceptual en el que se muestra una aplicación que contiene recursos localizables independientes del código](images/mui-fundamental-concepts-explained-fig4.gif)

Este modelo permite una creación más sencilla de las versiones localizadas de una aplicación y es una mejora significativa del modelo anterior. Este modelo, implementado mediante el uso de las herramientas de administración de recursos, ha sido muy satisfactorio durante los años y, en la actualidad, muchas aplicaciones lo usan actualmente. Sin embargo, tiene importantes desventajas:

-   Durante la separación lógica, el código y los recursos localizados siguen Unidas físicamente en un archivo ejecutable. En concreto, la capacidad de servicio sigue siendo problemática, ya que el mismo defecto de código (idéntico en todas las versiones de idioma) requiere una revisión por idioma. Por lo tanto, si una de ellas envía la aplicación en 20 idiomas, debe emitirse una revisión de servicio 20 veces (una para cada idioma), aunque el código solo se corrija una vez.
-   Este modelo no admite adecuadamente la distribución y el uso de aplicaciones multilingües. Puede tratarse de un problema importante en los escenarios de OEM y Enterprise. Por ejemplo, si un equipo se va a compartir entre dos usuarios que usan distintos idiomas, las aplicaciones deberán instalarse dos veces con este modelo y, a continuación, se deberá habilitar algún mecanismo para alternar entre las dos instalaciones. Se supone que no hay dependencias adicionales que impidan que se implemente incluso este escenario. La imagen siguiente muestra un ejemplo de un defecto de código único que requiere dos revisiones.

![diagrama conceptual que muestra dos aplicaciones localizadas que tienen el mismo defecto de código](images/mui-fundamental-concepts-explained-fig5.gif)

Es evidente que aunque este modelo funciona bien en algunos escenarios, las limitaciones de las aplicaciones multilingües y sus implementaciones pueden ser muy problemáticas.

Una variación de este modelo que alivia algunos de los problemas de aplicaciones multilingües es el modelo en el que los recursos localizables contienen un conjunto de recursos de lenguaje diferentes. Este modelo tiene una base de código común y varios recursos para diferentes idiomas de la misma aplicación. Por ejemplo, una aplicación se puede enviar con inglés, alemán, Francés, español, holandés e italiano en el mismo paquete. En la imagen siguiente se muestra una aplicación que contiene varios recursos de idioma.

![diagrama conceptual en el que se muestra una aplicación con código independiente de dos recursos específicos de la configuración regional](images/mui-fundamental-concepts-explained-fig6.gif)

Este modelo facilita el servicio de la aplicación cuando es necesario corregir un defecto de código (lo que supone una mejora), pero no mejora en comparación con los modelos anteriores cuando se trata de admitir idiomas adicionales. En este caso, es necesario liberar una nueva versión de la aplicación (y ese lanzamiento es potencialmente complicado por la necesidad de asegurarse de que todos los recursos de idioma se sincronizan dentro de la misma distribución).

### <a name="physically-separating-code-and-resources"></a>Separación física de código y recursos

El siguiente paso evolutivo es separar físicamente el código y los recursos. En este modelo, los recursos se abstraen del código y se separan físicamente en distintos archivos de implementación. En concreto, esto significa que el código puede ser realmente independiente del lenguaje; el mismo código físico se incluye realmente para todas las versiones localizadas de una aplicación. En la imagen siguiente se muestra que el código y los recursos localizables se deben separar físicamente.

![diagrama conceptual en el que se muestra una aplicación independiente de sus recursos localizables](images/mui-fundamental-concepts-explained-fig7.gif)

Este enfoque tiene varias ventajas con respecto a los enfoques anteriores:

-   La implementación de soluciones multilingües se ha simplificado en gran medida. Para agregar compatibilidad con cualquier idioma determinado, solo es necesario enviar e instalar un nuevo conjunto de recursos de idioma para este idioma en particular. Esto es especialmente importante cuando los recursos de idioma no están todos disponibles simultáneamente. Con este modelo, se puede implementar una aplicación en un conjunto de idiomas principales y aumentar el número de idiomas admitidos a lo largo del tiempo sin tener que modificar o volver a implementar el código real. Esta ventaja se extiende más mediante un mecanismo de reserva que permite la localización parcial de las aplicaciones y los componentes del sistema en un lenguaje determinado, ya que garantiza que los recursos que no se encuentran en este idioma preferido se "revierten" a otro idioma que los usuarios también entienden. En general, este modelo ayuda a mitigar la pesada carga que tienen las empresas globales en la implementación de aplicaciones en varios idiomas, ya que permite la implementación de una sola imagen de una manera mucho más eficaz.
-   Se ha mejorado la capacidad de servicio. Un defecto de código solo debe corregirse e implementarse una vez, ya que el código es totalmente independiente de la localización. Con este modelo, que emite una corrección para un defecto de código, siempre que el cambio no esté relacionado con la interfaz de usuario, es mucho más sencillo y rentable que en cualquiera de los modelos anteriores.

## <a name="dynamically-loading-language-specific-resources"></a>Cargar dinámicamente recursos específicos del idioma

Los conceptos fundamentales de MUI de [separar físicamente el código fuente de los recursos específicos del lenguaje](#physically-separating-code-and-resources)y la creación de un archivo binario principal independiente del lenguaje para una aplicación, básicamente configuran una arquitectura que favorece la implementación dinámica de recursos específicos del lenguaje según la configuración de idioma del usuario y del sistema.

El código fuente de la aplicación incluido en el archivo binario principal independiente del lenguaje puede emplear las API de MUI en la plataforma Windows para abstraer la selección del idioma de la interfaz de usuario de visualización adecuado para un contexto determinado. MUI lo admite:

-   Construir una lista de prioridades de los idiomas de la interfaz de usuario en función de la configuración del sistema, el usuario y el nivel de aplicación, nivel de usuario y nivel de sistema.
-   Implementación de un mecanismo de reserva que elige un candidato adecuado de esta lista de idiomas priorizada, en función de la disponibilidad de los recursos localizados.

Las ventajas de cargar dinámicamente los recursos de la interfaz de usuario con reserva priorizada son:

-   Permite la localización parcial de las aplicaciones y los componentes del sistema en un idioma determinado, ya que los recursos que no se encuentran en este idioma preferido volverán automáticamente al siguiente idioma de la lista de prioridades.
-   Permite escenarios como el cambio dinámico de un idioma a otro.
-   Permite crear imágenes de implementación única regional o internacional que cubren un conjunto de idiomas para OEM y empresas.

## <a name="building-mui-applications"></a>Compilar aplicaciones de MUI

En las secciones anteriores se describen las opciones para separar el código fuente de los recursos específicos del lenguaje y la ventaja resultante de poder emplear las API básicas de la plataforma Windows para cargar dinámicamente los recursos localizados. Aunque se trata de directrices, también debe señalarse que no hay ninguna manera preceptiva específica de desarrollar una aplicación MUI para la plataforma Windows.

Los desarrolladores de aplicaciones tienen plena elección en el modo en que controlan la configuración del idioma de la interfaz de usuario, las opciones de creación de recursos y los métodos de carga de recursos. Los desarrolladores pueden evaluar las instrucciones proporcionadas en este documento y elegir una combinación que se ajuste a sus requisitos y entorno de desarrollo.

En la tabla siguiente se resumen las distintas opciones de diseño disponibles para los desarrolladores de aplicaciones que buscan crear una aplicación MUI para la plataforma Windows.



<table>
<thead>
<tr class="header">
<th>Configuración del idioma de la interfaz de usuario</th>
<th>Creación de recursos</th>
<th>Carga de recursos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">Siga la configuración del idioma de la interfaz de usuario en el sistema operativo $ {REMOVE} $<br />
</td>
<td>Lenguaje único en un archivo binario de recursos dividido (tecnología de recursos MUI)<br/> O bien<br/> Varios idiomas en un archivo binario de recursos no divididos<br/></td>
<td>La aplicación llama a las funciones estándar de carga de recursos. Los recursos se devuelven en los idiomas que coinciden con la configuración del sistema operativo.<br/></td>
</tr>
<tr class="even">
<td>Mecanismo de recursos específico de la aplicación<br/></td>
<td>La aplicación llama a la API de MUI para recuperar los idiomas de interfaz de usuario preferidos para el subproceso o los idiomas de interfaz de usuario preferidos para el proceso del sistema operativo y usar estos valores para cargar sus propios recursos.<br/></td>

</tr>
<tr class="odd">
<td rowspan="2">Configuración de idioma de interfaz de usuario específica de la aplicación $ {REMOVE} $<br />
</td>
<td>Un solo idioma en un archivo binario de recursos divididos<br/> O bien<br/> Varios idiomas en un archivo binario de recursos no divididos<br/></td>
<td>La aplicación llama a la API de MUI para establecer los lenguajes de interfaz de usuario específicos de la aplicación o los lenguajes de interfaz de usuario preferidos del proceso y llama a las funciones estándar de carga Los recursos se devuelven en los idiomas establecidos por la aplicación o los idiomas del sistema.<br/> O bien<br/> La aplicación sondea los recursos en un lenguaje específico y controla su propia extracción de recursos a partir de los datos binarios recuperados.<br/></td>
</tr>
<tr class="even">
<td>Mecanismo de recursos específico de la aplicación<br/></td>
<td>La aplicación administra su propia carga de recursos.<br/></td>

</tr>
</tbody>
</table>



 

 

 




