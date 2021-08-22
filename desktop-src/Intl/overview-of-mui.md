---
description: En este tema se proporciona información general conceptual de la tecnología Interfaz de usuario multilingüe (IAM), la compatibilidad con la plataforma que proporciona para habilitar experiencias de usuario multilingües y las ventajas que ofrece al ecosistema de Windows.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Información general de LA INTERFAZ global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e4e92c9103b27b35be427a74174c644a285266
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625781"
---
# <a name="overview-of-mui"></a>Información general de LA INTERFAZ global

En este tema se proporciona información general conceptual de la tecnología Interfaz de usuario multilingüe (IAM), la compatibilidad con la plataforma que proporciona para habilitar experiencias de usuario multilingües y las ventajas que ofrece al ecosistema de Windows.

En esta página:

-   [La necesidad de informática multilingüe](#the-need-for-multilingual-computing)
-   [El rol de MUI en la habilitación de la computación multilingüe](#the-role-of-mui-in-enabling-multilingual-computing)
-   [Conceptos básicos de MUI](#core-concepts-of-mui)
-   [Historial de LAN en Windows](#history-of-mui-in-windows)
-   [Ventajas de la tecnología DESA](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a>La necesidad de informática multilingüe

Para beneficiarse de las oportunidades de crecimiento que presentan los mercados internacionales, las plataformas y aplicaciones de Microsoft admiten más idiomas, culturas y mercados que nunca.

El idioma, la cultura y las características específicas del mercado siguen siendo extremadamente relevantes para los usuarios internacionales, a pesar de las crecientes tendencias de globalización. En el siguiente gráfico circular se muestra que los hablantes que no son de inglés siguen representando el 91,5 por ciento de la población mundial.

![gráfico circular con tres segmentos; el que se etiqueta como "hablantes que no son del inglés 91,5 %" es mucho mayor que los otros dos combinados.](images/overview-of-mui-fig1.gif)

En todo el mundo, hay 193 países y más de 6900 idiomas de vida conocidos en uso actualmente. El inglés, a pesar de su rol como idioma empresarial del mundo, solo lo habla el 8,5 % de la población mundial como primer o segundo idioma. Para proporcionar información nativa al 94 % de la población mundial, esta información tendría que estar disponible en los 347 (aproximadamente el 5 %) de los idiomas del mundo que tienen al menos un millón de hablantes. Esto es especialmente cierto, ya que las tendencias de globalización han aumentado las expectativas de estos usuarios con respecto a la tecnología y su disponibilidad en sus mercados.

La necesidad de localización de software en más idiomas ha aumentado con los años y Microsoft ahora proporciona Windows Vista y otros productos en más idiomas que nunca. Esta evolución es especialmente clara con Microsoft Windows, ya que ha pasado de admitir 30 idiomas con Windows 98 a casi 100 con Windows Vista, como se muestra en el siguiente gráfico de barras.

![gráfico de barras que muestra que el número de idiomas es mucho mayor en Windows Vista que en Windows 98 o Windows XP](images/overview-of-mui-fig2.gif)

*Figura 2: Número de idiomas admitidos por microsoft Windows versiones*

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a>El rol de MUI en la habilitación de la computación multilingüe

Como se ha comentado en [](glossary-for-understanding-mui.md) la sección anterior, [la globalización](glossary-for-understanding-mui.md) y localización de aplicaciones se han convertido en una necesidad en un mundo más globalmente integrado. En concreto, a medida que cada vez más empresas se están globalización, ya sea internamente o a través de sus redes empresariales, la necesidad de aplicaciones multilingües aumenta drásticamente. Así son los obstáculos a los que se enfrentan actualmente estas empresas en la implementación de estas aplicaciones globalmente.

Proporcionar compatibilidad con más idiomas para sistemas operativos Windows, así como aplicaciones de software creadas para la plataforma Windows, requiere nuevas estrategias que permitan implementar todos los escenarios principales con una sobrecarga de ingeniería mínima.

La tecnología DEV está dirigida a desarrolladores e ISV con el objetivo de compilar y admitir aplicaciones multilingües para la Windows plataforma. TAMBIÉN es importante para los OEM y las empresas, que pueden aprovecharlo para implementar el sistema operativo Windows y agregar aplicaciones a equipos en distintos idiomas a través de la implementación de una sola imagen.

## <a name="core-concepts-of-mui"></a>Conceptos básicos de MUI

La idea fundamental deTRÁS de QR es separar el almacenamiento de recursos [localizables](mui-fundamental-concepts-explained.md)del código fuente de la aplicación para poder diseñar cualquier aplicación multilingüe como una combinación de un binario básico neutro del idioma y un conjunto de archivos de recursos localizados específicos del idioma.

Una vez que el código fuente de la [](mui-fundamental-concepts-explained.md) aplicación se almacena por separado de los recursos localizados, resulta fácil cargar dinámicamente los recursos localizados adecuados para un contexto de aplicación determinado en función de una lógica que tiene en cuenta la configuración de nivel de aplicación, usuario y sistema para el lenguaje de interfaz de usuario.

Estos atributos fundamentales de LAME ayudan a facilitar escenarios empresariales como:

-   Un modelo de localización mejorado para la interfaz de usuario y el contenido de ayuda, a través de la separación física del código fuente de la aplicación y los recursos localizables.
-   Tratar los recursos localizables como contenido dinámico y cargarlos según la configuración del idioma de la interfaz de usuario y las preferencias de reserva. Esto permite escenarios como:
    -   Cambio de un idioma de interfaz de usuario a otro en tiempo de ejecución.
    -   Creación de imágenes de implementación única regionales o en todo el mundo que cubren un conjunto de idiomas para oem y empresas.

## <a name="history-of-mui-in-windows"></a>Historial de LAN en Windows

El nivel de compatibilidad disponible para una experiencia de usuario multilingüe en el nivel de sistema operativo de Windows y para el desarrollo de aplicaciones multilingües en la plataforma Windows ha evolucionado con el tiempo y en las distintas versiones de Windows.

La funcionalidad admitida antes [de Windows Vista](evolution-of-mui-support-across-windows-versions.md) era bastante básica, con imágenes de Windows de un solo idioma y una opción para agregar Interfaz de usuario multilingüe paquetes en escenarios específicos. No había disponible compatibilidad para desarrolladores con aplicaciones multilingües.

[Con Windows Vista,](evolution-of-mui-support-across-windows-versions.md)Microsoft ha realizado una inversión significativa en LAN Y Windows Vista se ha creado desde cero en una plataforma DESA. Aunque esto representa un avance importante en la estrategia de localización de Windows, ya que es un habilitador clave para que Microsoft proporcione Windows en más idiomas que nunca, es en primer lugar y, ante todo, un gran avance para los usuarios, desarrolladores y clientes de Windows. Proporciona varias ventajas importantes, como:

-   Un sistema operativo neutral del lenguaje con compatibilidad integrada con LAN.
-   Empaquetado, implementación e instalación configurables para admitir escenarios multilingües.
-   Implementación de una sola imagen con varios idiomas.
-   Un modelo de mantenimiento mejorado en el que el código ejecutable se puede actualizar independientemente de los recursos.
-   Compatibilidad para desarrolladores con la creación de aplicaciones multilingües.

En la tabla siguiente se proporciona información general detallada sobre la compatibilidad de Windows plataforma de desarrollo para EL SITIO WEB:

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Soporte técnico</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Versiones Windows compatibles (solo compatibilidad con el sistema operativo)</td>
<td><ul>
<li>Windows 2000 Professional</li>
<li>Windows 2000 Server</li>
<li>Windows XP Professional</li>
<li>Windows XP Tablet PC Edition</li>
<li>Windows Familia Server 2003</li>
<li>Windows XP Embedded</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Versiones Windows compatibles (compatibilidad con aplicaciones & sistema operativo)</td>
<td><ul>
<li>Windows Vista</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Versiones no admitidas de Windows</td>
<td><ul>
<li>Windows 9x</li>
<li>Windows Me</li>
<li>Windows XP Home Edition</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a>Ventajas de la tecnología DESA

LA CONVERSIÓN afecta positivamente a varios aspectos del Windows ecosistema:

-   [Ventajas](benefits-of-mui-explained.md)para los desarrolladores: la disponibilidad de la compatibilidad con API de LA API de JAVA ofrece numerosas ventajas para crear aplicaciones multilingües modeladas en los mismos principios que la compatibilidad multilingüe en el sistema operativo Windows principal. Entre las ventajas se incluye lo siguiente:
    -   La capacidad de proporcionar una experiencia de lenguaje de presentación coherente con lo que ofrece el propio sistema operativo.
    -   La capacidad de ampliar fácilmente la compatibilidad de lenguaje para una aplicación.
    -   La capacidad de mantener y dar servicio fácilmente a la aplicación.
    -   La capacidad de habilitar la implementación de una sola imagen de aplicaciones por oem.
-   [Ventajas para las empresas:](benefits-of-mui-explained.md)la principal ventaja que ofrece LAN para las empresas es la capacidad de implantar, dar soporte técnico y mantener la misma imagen multilingüe en todo el mundo con una sola instalación. Otra ventaja importante es la capacidad de admitir escritorios multilingües que ofrecen una interacción sin problemas a los usuarios con distintas preferencias de idioma.
-   [Ventajas para los](benefits-of-mui-explained.md)OEM: la principal ventaja para los OEM es la instalación de una sola imagen que HABILITANIA, con compatibilidad con varios lenguajes, lo que permite una administración más eficaz del inventario. Los OEM también se benefician de la compatibilidad con LAME para el desarrollo de aplicaciones, ya que les permite proporcionar aplicaciones de valor añadido en sus imágenes y, al mismo tiempo, beneficiarse de la instalación de una sola imagen, siempre que estas aplicaciones estén habilitadas para JPEG.

 

 




