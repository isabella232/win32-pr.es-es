---
description: En este tema se proporciona información general conceptual de la tecnología de interfaz de usuario multilingüe (MUI), la compatibilidad con la plataforma que proporciona para habilitar experiencias de usuario multilingües y las ventajas que ofrece el ecosistema de Windows.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Información general sobre MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562469"
---
# <a name="overview-of-mui"></a>Información general sobre MUI

En este tema se proporciona información general conceptual de la tecnología de interfaz de usuario multilingüe (MUI), la compatibilidad con la plataforma que proporciona para habilitar experiencias de usuario multilingües y las ventajas que ofrece el ecosistema de Windows.

En esta página:

-   [La necesidad de la informática multilingüe](#the-need-for-multilingual-computing)
-   [El rol de MUI en la habilitación de la informática multilingüe](#the-role-of-mui-in-enabling-multilingual-computing)
-   [Conceptos básicos de MUI](#core-concepts-of-mui)
-   [Historial de MUI en Windows](#history-of-mui-in-windows)
-   [Ventajas de la tecnología MUI](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a>La necesidad de la informática multilingüe

Para beneficiarse de las oportunidades de crecimiento que presentan los mercados internacionales, las plataformas y las aplicaciones de Microsoft admiten más idiomas, culturas y mercados que nunca.

Los detalles de idioma, referencia cultural y mercado siguen siendo extremadamente relevantes para los usuarios internacionales, a pesar de aumentar las tendencias de globalización. En el gráfico circular siguiente se muestra que los hablantes que no están en inglés todavía componen el 91,5 por ciento de la población del mundo.

![gráfico circular con tres segmentos; la etiqueta "hablantes no inglesas 91,5%" es enormemente mayor que las otras dos combinadas](images/overview-of-mui-fig1.gif)

En todo el mundo, hay 193 países y más de 6.900 idiomas viviendo conocidos en uso hoy en día. En inglés, a pesar de su rol como lenguaje empresarial del mundo, solo se habla del 8,5% de la población del mundo como primer o segundo idioma. Para proporcionar información nativa al 94% de la población del mundo, esta información debe estar disponible en el 347 (aproximadamente un 5%). de los idiomas del mundo que tienen al menos un millón de oradores. Esto es especialmente cierto cuando las tendencias de globalización han aumentado las expectativas de estos usuarios con respecto a la tecnología y su disponibilidad en sus mercados.

La necesidad de localizar software en más idiomas ha aumentado a lo largo de los años y Microsoft ahora proporciona Windows Vista y otros productos en más idiomas que nunca. Esta evolución está especialmente clara en Microsoft Windows, ya que ha pasado de admitir 30 idiomas con Windows 98 a casi 100 con Windows Vista, como se muestra en el siguiente gráfico de barras.

![gráfico de barras que muestra que el número de idiomas es mucho mayor en Windows Vista que en Windows 98 o Windows XP](images/overview-of-mui-fig2.gif)

*Figura 2: número de idiomas admitidos por las versiones de Microsoft Windows*

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a>El rol de MUI en la habilitación de la informática multilingüe

Como se explicó en la sección anterior, la [globalización](glossary-for-understanding-mui.md) y la [localización](glossary-for-understanding-mui.md) de las aplicaciones se han convertido en una necesidad en un mundo más globalmente integrado. En concreto, a medida que más y más empresas van a ser globales, ya sea internamente o a través de sus redes empresariales, la necesidad de aplicaciones multilingües aumenta drásticamente. Por lo tanto, son los obstáculos en los que estas empresas se encuentran actualmente en la implementación global de estas aplicaciones.

Proporcionar compatibilidad con más idiomas para los sistemas operativos Windows, así como con aplicaciones de software compiladas para la plataforma Windows, requiere nuevas estrategias que permiten implementar todos los escenarios principales con una sobrecarga de ingeniería mínima.

La tecnología MUI está destinada a desarrolladores y proveedores de software independientes que pretenden compilar y admitir aplicaciones multilingües para la plataforma Windows. MUI también es de importancia fundamental para los OEM y las empresas, que pueden aprovecharlo para implementar el sistema operativo Windows y agregar aplicaciones a los equipos en distintos idiomas a través de la implementación de una sola imagen.

## <a name="core-concepts-of-mui"></a>Conceptos básicos de MUI

La idea fundamental que subyace a MUI es [separar el almacenamiento de recursos localizables del código fuente](mui-fundamental-concepts-explained.md)de la aplicación, de modo que pueda diseñar cualquier aplicación multilingüe como una combinación de un archivo binario principal independiente del lenguaje y un conjunto de archivos de recursos localizados específicos del idioma.

Una vez que el código fuente de la aplicación se almacena de forma independiente de los recursos localizados, es fácil [cargar dinámicamente los recursos localizados adecuados](mui-fundamental-concepts-explained.md) para un determinado contexto de la aplicación en función de una lógica que tenga en cuenta la configuración del sistema, el usuario y el nivel de aplicación para el idioma de la interfaz de usuario.

Estos atributos fundamentales de MUI ayudan a facilitar escenarios empresariales como los siguientes:

-   Un modelo de localización mejorado para la interfaz de usuario y el contenido de la ayuda, a través de la separación física del código fuente de la aplicación y los recursos localizables.
-   Tratar los recursos localizables como contenido dinámico y cargarlos según la configuración del idioma de la interfaz de usuario y las preferencias de reserva. Esto permite escenarios como los siguientes:
    -   Cambiar de un idioma de interfaz de usuario a otro en tiempo de ejecución.
    -   Crear imágenes de implementación única regional o internacional que cubran un conjunto de idiomas para OEM y empresas.

## <a name="history-of-mui-in-windows"></a>Historial de MUI en Windows

El nivel de soporte técnico disponible para una experiencia de usuario multilingüe en el nivel del sistema operativo Windows y para el desarrollo de aplicaciones multilingües en la plataforma Windows ha evolucionado a lo largo del tiempo y a través de las diferentes versiones de Windows.

La funcionalidad admitida antes de que [Windows Vista](evolution-of-mui-support-across-windows-versions.md) era bastante básica, con imágenes de Windows de un solo idioma y una opción para agregar paquetes de interfaz de usuario multilingüe en escenarios específicos. No hay compatibilidad para desarrolladores de aplicaciones multilingües.

[Con Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft ha realizado una inversión significativa en mui y Windows Vista se ha creado desde el principio en una plataforma MUI. Aunque esto representa un avance importante en la estrategia de localización de Windows, ya que es un componente clave para que Microsoft proporcione Windows en más idiomas que nunca, es primero y más importante para los usuarios, desarrolladores y clientes de Windows. Proporciona varias ventajas principales como las siguientes:

-   Un sistema operativo independiente del lenguaje con compatibilidad integrada con MUI.
-   Empaquetado, implementación e instalación configurables para admitir escenarios multilingües.
-   Implementación de una sola imagen con varios idiomas.
-   Modelo de servicio mejorado en el que el código ejecutable se puede actualizar independientemente de los recursos.
-   Compatibilidad del desarrollador con la creación de aplicaciones multilingües.

En la tabla siguiente se proporciona información general detallada sobre la compatibilidad de la plataforma Windows con MUI:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Soporte técnico</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Versiones admitidas de Windows (solo compatibilidad con sistema operativo)</td>
<td><ul>
<li>Windows 2000 Professional</li>
<li>Familia de servidores de Windows 2000</li>
<li>Windows XP Professional</li>
<li>Windows XP Tablet PC Edition</li>
<li>Familia de Windows Server 2003</li>
<li>Windows XP Embedded</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Versiones admitidas de Windows (compatibilidad con aplicaciones de SO &)</td>
<td><ul>
<li>Windows Vista</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Versiones no admitidas de Windows</td>
<td><ul>
<li>Windows 9x</li>
<li>Windows me</li>
<li>Windows XP Home Edition</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a>Ventajas de la tecnología MUI

MUI tiene un efecto positivo en varios aspectos del ecosistema de Windows:

-   [Ventajas para los desarrolladores](benefits-of-mui-explained.md): se ofrecen numerosas ventajas a los desarrolladores de aplicaciones por la disponibilidad de la compatibilidad de la API de MUI para compilar aplicaciones multilingües modeladas en los mismos principios que la compatibilidad multilingüe en el propio sistema operativo Windows. Entre las ventajas se incluye lo siguiente:
    -   La capacidad de proporcionar una experiencia de visualización de lenguaje que sea coherente con la que ofrece el propio sistema operativo.
    -   La capacidad de ampliar fácilmente la compatibilidad de idioma para una aplicación.
    -   La capacidad de mantener y atender la aplicación fácilmente.
    -   La capacidad de habilitar la implementación de una sola imagen de las aplicaciones por parte de los OEM.
-   [Ventajas para empresas](benefits-of-mui-explained.md): la principal ventaja que ofrece MUI para empresas es la capacidad de implementar, respaldar y mantener la misma imagen multilingüe en todo el mundo con una única instalación. Otro logro importante es la capacidad de admitir escritorios multilingües que ofrecen una interacción sin problemas a los usuarios con diferentes preferencias de idioma.
-   [Ventajas para los OEM](benefits-of-mui-explained.md): la principal ventaja para los OEM es la instalación de imagen única que mui habilita, con compatibilidad para varios idiomas, lo que permite una administración más eficaz del inventario. Los OEM también se benefician de la compatibilidad de MUI con el desarrollo de aplicaciones, ya que les permite proporcionar aplicaciones de valor agregado en sus imágenes mientras se benefician de la instalación de una sola imagen, siempre y cuando estas aplicaciones estén habilitadas para MUI.

 

 




