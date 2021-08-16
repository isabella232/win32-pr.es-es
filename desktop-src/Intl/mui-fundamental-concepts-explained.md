---
description: Conceptos fundamentales de LAIA explicados
ms.assetid: 9ab19a56-4d31-471d-949e-a539751b62e3
title: Conceptos fundamentales de LAIA explicados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88bd677d7a6b07bc4db78d733d81fc36624ddd06f9ad3014588b8e5fd0882aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390895"
---
# <a name="mui-fundamental-concepts-explained"></a>Conceptos fundamentales de LAIA explicados

-   [Requisito previo de MUI](#prerequisite-for-mui)
-   [Separación del código fuente de los recursos específicos del lenguaje](#separation-of-source-code-from-language-specific-resources)
    -   [Los primeros días: el código y los recursos se reúnen](#the-early-days-code-and-resources-live-together)
    -   [Separación lógica del código y los recursos localizables](#logically-separating-code-and-localizable-resources)
    -   [Separación física del código y los recursos](#physically-separating-code-and-resources)
-   [Carga dinámica de recursos específicos del lenguaje](#dynamically-loading-language-specific-resources)
-   [Creación de aplicaciones de MUI](#building-mui-applications)

## <a name="prerequisite-for-mui"></a>Requisito previo de LAN

El requisito previo básico para compilar una aplicación compatible con MUI para Windows Vista y versiones posteriores es diseñar la aplicación de acuerdo con Windows [de globalización.](https://msdn.microsoft.com/goglobal/bb688110.aspx)

## <a name="separation-of-source-code-from-language-specific-resources"></a>Separación del código fuente de los recursos específicos del lenguaje

Una de las instalaciones fundamentales de la tecnología DEA es la separación del código fuente de la aplicación de los recursos específicos del lenguaje, para habilitar escenarios multilingües en las aplicaciones de forma más eficaz. La separación de código y recursos se ha logrado a través de diferentes mecanismos y en distintos grados a lo largo del tiempo, como se describe en las secciones siguientes. Cada método proporcionaba distintos grados de flexibilidad en la creación, implementación y mantenimiento de la aplicación.

La solución recomendada para las aplicaciones compatibles con QR es el último método que se describe aquí, es decir, la separación física del código fuente y los recursos de la aplicación, con los propios recursos desglosados en un archivo por cada idioma admitido para obtener la máxima flexibilidad en la creación, implementación y mantenimiento.

### <a name="the-early-days-code-and-resources-live-together"></a>Los primeros días: el código y los recursos se reúnen

Inicialmente, las aplicaciones localizadas se crearon editando el código fuente y cambiando los recursos (normalmente cadenas) en el propio código y recompilando las aplicaciones. Esto significaba que para generar una versión localizada, había que copiar el código fuente original, traducir los elementos de texto (recursos) dentro del código fuente y volver a compilar el código. En la imagen siguiente se muestra el código de la aplicación con texto que debe localizarse.

![diagrama conceptual que muestra una aplicación que contiene unidades de recursos de texto insertado](images/mui-fundamental-concepts-explained-fig3.gif)

Aunque este enfoque permite la creación de aplicaciones localizadas, también tiene importantes desventajas:

-   Requiere varias versiones del código fuente, al menos una para el idioma de origen y otra para cada uno de los idiomas de destino. Esto crea problemas importantes al sincronizar las distintas versiones de lenguaje de la aplicación. En concreto, cuando es necesario solucionar un defecto en el código, el defecto debe solucionarse en cada copia del código fuente (una por idioma).
-   También es muy propenso a errores, ya que requiere que los localizadores (que no son desarrolladores) realicen modificaciones en el código fuente, lo que crea un riesgo considerable en términos de integridad del código.

La combinación de estos inconvenientes hace que sea una propuesta extremadamente ineficaz y se necesita un modelo mejor.

### <a name="logically-separating-code-and-localizable-resources"></a>Separación lógica del código y los recursos localizables

Una mejora significativa con respecto al modelo anterior es la separación lógica de código y recursos localizables para una aplicación. Esto aísla el código de los recursos y garantiza que el código permanece intacto cuando la localización cambia los recursos. Desde el punto de vista de la implementación, las cadenas y otros elementos de la interfaz de usuario se almacenan en archivos de recursos, que son relativamente fáciles de traducir y se separan lógicamente de las secciones de código.

Idealmente, agregar compatibilidad con cualquier idioma determinado puede ser tan sencillo como traducir los recursos localizables a este nuevo idioma y usar estos recursos traducidos para crear una nueva versión localizada de la aplicación, sin necesidad de ninguna modificación del código. En la imagen siguiente se muestra cómo el código y los recursos localizables deben separarse lógicamente dentro de una aplicación.

![Diagrama conceptual que muestra una aplicación que contiene recursos localizables independientes del código](images/mui-fundamental-concepts-explained-fig4.gif)

Este modelo permite una creación más sencilla de versiones localizadas de una aplicación y es una mejora significativa con respecto al modelo anterior. Este modelo, implementado mediante el uso de herramientas de administración de recursos, ha tenido mucho éxito a lo largo de los años y sigue siendo utilizado habitualmente por muchas aplicaciones en la actualidad. Sin embargo, tiene desventajas significativas:

-   Aunque están separados lógicamente, el código y los recursos localizados siguen unidos físicamente en un archivo ejecutable. En concreto, la capacidad de servicio sigue siendo problemática, ya que el mismo defecto de código (idéntico en todas las versiones de idioma) requiere una revisión por idioma. Por lo tanto, si se va a enviar la aplicación en 20 idiomas, es necesario emitir una revisión de servicio 20 veces (una para cada idioma), aunque el código solo se corrigió una vez.
-   Este modelo no admite adecuadamente la distribución y el uso de aplicaciones multilingües. Esto puede ser un problema importante en escenarios de OEM y empresariales. Por ejemplo, si un equipo se va a compartir entre dos usuarios con distintos idiomas, las aplicaciones tendrán que instalarse dos veces con este modelo y, a continuación, será necesario habilitar algún mecanismo para alternar entre las dos instalaciones. Esto supone que no hay dependencias adicionales que impidan incluso la implementación de este escenario. En la imagen siguiente se muestra un ejemplo de un defecto de código único que requiere dos revisiones.

![Diagrama conceptual que muestra dos aplicaciones localizadas que tienen el mismo defecto de código](images/mui-fundamental-concepts-explained-fig5.gif)

Está claro que aunque este modelo funciona bien en algunos escenarios, sus limitaciones para las aplicaciones multilingües y sus implementaciones pueden ser muy problemáticas.

Una variación de este modelo que mitiga algunos de los problemas de las aplicaciones multilingües es el modelo en el que los recursos localizables contienen un conjunto de recursos de lenguaje diferentes. Este modelo tiene una base de código común y varios recursos para distintos lenguajes en la misma aplicación. Por ejemplo, una aplicación puede enviarse con inglés, alemán, francés, español, neerlandés e italiano en el mismo paquete. En la imagen siguiente se muestra una aplicación que contiene varios recursos de lenguaje.

![diagrama conceptual que muestra una aplicación con código independiente de dos recursos específicos de la configuración regional](images/mui-fundamental-concepts-explained-fig6.gif)

Este modelo facilita el servicio de la aplicación cuando es necesario solucionar un defecto de código, lo que es una mejora, pero no mejora con respecto a los modelos anteriores cuando se trata de admitir lenguajes adicionales. En este caso, todavía es necesario publicar una nueva versión de la aplicación (y esa versión es potencialmente complicada por la necesidad de asegurarse de que todos los recursos de lenguaje están sincronizados dentro de la misma distribución).

### <a name="physically-separating-code-and-resources"></a>Separación física del código y los recursos

El siguiente paso evolución consiste en separar físicamente el código y los recursos. En este modelo, los recursos se abstrae del código y se separan físicamente en distintos archivos de implementación. En concreto, esto significa que el código puede ser realmente independiente del lenguaje; el mismo código físico se envía realmente para todas las versiones localizadas de una aplicación. En la imagen siguiente se muestra que el código y los recursos localizables deben estar separados físicamente.

![Diagrama conceptual que muestra una aplicación independiente de sus recursos localizables](images/mui-fundamental-concepts-explained-fig7.gif)

Este enfoque tiene varias ventajas con respecto a los enfoques anteriores:

-   La implementación de soluciones multilingües se simplifica en gran medida. Para agregar compatibilidad con cualquier idioma determinado, solo es necesario enviar e instalar un nuevo conjunto de recursos de idioma para este idioma concreto. Esto es especialmente importante cuando los recursos de lenguaje no están disponibles simultáneamente. Con este modelo, se puede implementar una aplicación en un conjunto de idiomas principales y aumentar el número de idiomas admitidos con el tiempo sin tener que modificar o volver a implementar el código real. Esta ventaja se amplía aún más mediante un mecanismo de reserva que permite la localización parcial de aplicaciones y componentes del sistema en un idioma determinado, ya que garantiza que los recursos que no se encuentran en este idioma preferido se "reversión" a otro idioma que los usuarios también entiendan. En general, este modelo ayuda a mitigar la considerable carga a la que se enfrentan las empresas globales al implementar aplicaciones en varios idiomas, ya que permite la implementación de una sola imagen de una manera mucho más eficaz.
-   Se ha mejorado la capacidad de servicio. Un defecto de código solo debe solucionarse e implementarse una vez, ya que el código es completamente independiente de la localización. Con este modelo, emitir una corrección para un defecto de código, siempre que el cambio no esté relacionado con la interfaz de usuario, es mucho más sencillo y rentable que en cualquiera de los modelos anteriores.

## <a name="dynamically-loading-language-specific-resources"></a>Carga dinámica de recursos específicos del lenguaje

Los conceptos [](#physically-separating-code-and-resources)fundamentales de MUI de separar físicamente el código fuente de los recursos específicos del lenguaje y crear un binario básico independiente del idioma para una aplicación, básicamente, configurar una arquitectura que sea propicio para implementar la carga dinámica de recursos específicos del lenguaje en función de la configuración del usuario y del lenguaje del sistema.

El código fuente de la aplicación agrupado en el binario básico neutro del lenguaje puede usar las API de KPI en la plataforma de Windows para abstraer la selección del lenguaje de interfaz de usuario para mostrar adecuado para un contexto determinado. LA PROPIEDAD admite esto mediante:

-   Crear una lista prioritaria de idiomas de interfaz de usuario para mostrar en función de la configuración de nivel de sistema, usuario y aplicación, de nivel de usuario y de nivel de sistema.
-   Implementar un mecanismo de reserva que elija un candidato adecuado de esta lista de idiomas con prioridad, en función de la disponibilidad de los recursos localizados.

Las ventajas de cargar dinámicamente recursos de interfaz de usuario con reserva prioritaria son:

-   Permite la localización parcial de aplicaciones y componentes del sistema en un idioma determinado, ya que los recursos que no se encuentran en este idioma preferido volverán automáticamente al siguiente idioma de la lista de prioridades.
-   Permite escenarios como cambiar dinámicamente de un idioma a otro.
-   Permite crear imágenes de implementación única regionales o de todo el mundo que cubren un conjunto de idiomas para oem y empresas.

## <a name="building-mui-applications"></a>Creación de aplicaciones de MUI

En las secciones anteriores se describen las opciones para separar el código fuente de los recursos específicos del lenguaje y la ventaja resultante de poder usar las API principales de la plataforma Windows para cargar dinámicamente los recursos localizados. Aunque se trata de directrices, también debe señalarse que no hay ninguna manera preceptiva específica de desarrollar una aplicación DE INTERFAZ de usuario para la Windows plataforma.

Los desarrolladores de aplicaciones tienen una opción completa sobre cómo controlan la configuración del lenguaje de interfaz de usuario, las opciones de creación de recursos y los métodos de carga de recursos. Los desarrolladores pueden evaluar las directrices proporcionadas en este documento y elegir una combinación que se ajuste a sus requisitos y entorno de desarrollo.

En la tabla siguiente se resumen las distintas opciones de diseño disponibles para los desarrolladores de aplicaciones que buscan crear una aplicación DE EXTENSIÓN para Windows plataforma.



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
<td rowspan="2">Siga la configuración del idioma de la interfaz de usuario en el sistema operativo${REMOVE}$<br />
</td>
<td>Un solo idioma en un binario de recursos divididos (tecnología de recursos de MUI)<br/> O bien<br/> Varios idiomas en un binario de recursos sin división<br/></td>
<td>La aplicación llama a las funciones de carga de recursos estándar. Los recursos se devuelven en los idiomas que coinciden con la configuración del sistema operativo.<br/></td>
</tr>
<tr class="even">
<td>Mecanismo de recursos específico de la aplicación<br/></td>
<td>La aplicación llama a la API de MUI para recuperar los idiomas de interfaz de usuario preferidos para subprocesos o los idiomas de interfaz de usuario preferidos del proceso del sistema operativo y usar esta configuración para cargar sus propios recursos.<br/></td>

</tr>
<tr class="odd">
<td rowspan="2">Configuración del idioma de la interfaz de usuario específica de la aplicación${REMOVE}$<br />
</td>
<td>Idioma único en un binario de recursos divididos<br/> O bien<br/> Varios idiomas en un archivo binario de recursos sin división<br/></td>
<td>La aplicación llama a la API DE ANDI para establecer idiomas de interfaz de usuario específicos de la aplicación o lenguajes de interfaz de usuario preferidos del proceso y, a continuación, llama a las funciones de carga de recursos estándar. Los recursos se devuelven en los idiomas establecidos por los idiomas de la aplicación o del sistema.<br/> O bien<br/> La aplicación sondea los recursos en un lenguaje específico y controla su propia extracción de recursos de los datos binarios recuperados.<br/></td>
</tr>
<tr class="even">
<td>Mecanismo de recursos específico de la aplicación<br/></td>
<td>La aplicación administra su propia carga de recursos.<br/></td>

</tr>
</tbody>
</table>



 

 

 




