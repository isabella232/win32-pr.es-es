---
description: A continuación se proporciona información sobre las opciones que se deben tener en cuenta al personalizar iconos de aplicaciones de escritorio para Windows 8 incluido cómo diseñar iconos de aplicación de escritorio para el nuevo pantalla Inicio y cómo elegir qué puntos de entrada se muestran en el pantalla Inicio.
ms.assetid: EF5182A2-09B2-46F2-B55E-4BD212CC1F7F
title: Iconos de aplicación de escritorio en la pantalla de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ed35bd5c8405301e872ef54774914d625e1fc06c6a9fc3c26965e130301eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861227"
---
# <a name="desktop-app-tiles-on-the-start-screen"></a>Iconos de aplicación de escritorio en la pantalla de inicio

A continuación se proporciona información sobre las opciones que se deben tener en cuenta al personalizar iconos de aplicaciones de escritorio para Windows 8 incluido cómo diseñar iconos de aplicación de escritorio para el nuevo pantalla Inicio y cómo elegir qué puntos de entrada se muestran en el pantalla Inicio.

## <a name="design-your-tile-for-the-start-screen"></a>Diseñe el icono para la pantalla Inicio

Puede personalizar dos aspectos de los iconos de la aplicación de escritorio: el nombre de la aplicación y el icono. El color de fondo se deriva del color de fondo elegido por el usuario y no se puede personalizar mediante programación.

![Guía de diseño de mosaicos de la aplicación.](images/tiles-desktop-1.png)

DO: evite el truncamiento del nombre de la aplicación. Los iconos de escritorio anclados al pantalla Inicio pueden dar cabida a hasta dos líneas de texto cada línea, o aproximadamente diez caracteres (aunque esto depende del idioma de la interfaz de usuario), así que intente mantener el nombre de la aplicación lo suficientemente corto como para evitar el truncamiento.

DO: proporcione iconos para los cuatro valores de escala pantalla Inicio para asegurarse de que los iconos tienen un aspecto nítido en todos los factores de forma.



| Escala | Tamaño del icono (en píxeles) | Tamaño de icono usado (en píxeles) |
|-------|-----------------------|----------------------------|
| 80 %   | 120 x 120             | 48 x 48                    |
| 100 %  | 150 x 150             | 64 x 64                    |
| 140%  | 210 x 210             | 96 x 96                    |
| 180%  | 270 x 270             | 128 x 128                  |



 

DO: Adopte los principios de diseño de Microsoft. La nueva apariencia de los iconos es plana, por lo que si desea imitar los iconos de aplicación de Windows Store para la aplicación de escritorio, considere la posibilidad de quitar sombras paralelas, entre otras cosas.

NO: No evite el uso de color. Aunque Windows los iconos de aplicación de store a veces son monocromáticos, se recomienda usar iconos de color para aplicaciones de escritorio. Esto ayuda a diferenciar las aplicaciones de escritorio en la barra de tareas y de otros iconos de aplicación de escritorio en el pantalla Inicio porque el color de fondo de los iconos de escritorio no se puede personalizar. Considere la posibilidad de usar colores más saturados.

## <a name="decide-the-right-entry-points-to-include-in-the-start-screen"></a>Decida los puntos de entrada correctos que se incluirán en el pantalla Inicio

DO: Agregue un acceso directo por aplicación en el pantalla Inicio cuando la aplicación esté instalada. Esto garantiza que los usuarios puedan iniciar la aplicación directamente desde el pantalla Inicio o a través de la búsqueda. Si no incluye un acceso directo en el pantalla Inicio, la aplicación se vuelve difícil de iniciar. En concreto, no agregue un acceso directo solo en el escritorio. Los usuarios ven el pantalla Inicio la primera vez que inician sesión, por lo que colocar un acceso directo solo en el escritorio no es tan eficaz como incluirlo en el pantalla Inicio.

![Diagrama que muestra una cuadrícula con un icono de aplicación, dimensiones y "Segoe U I Semilight" para indicar la fuente usada.](images/tiles-desktop-2.png)

NO: no proporcione varios accesos directos a la misma aplicación. Por ejemplo, no tiene dos accesos directos que inicien una aplicación en dos modos diferentes, como uno para Windows Internet Explorer y otro para Internet Explorer sin complementos.

DO: minimice el número de iconos que se agregan como parte de la instalación. Considere la posibilidad de exponer otros puntos de entrada a las aplicaciones extraneous. Por ejemplo, en lugar de incluir una aplicación de Configuración independiente con una aplicación de consola, acceda a la configuración a través de una característica de la aplicación de consola.

NO LO HAGA: No coloque accesos directos a los siguientes elementos en el pantalla Inicio:

-   Desinstaladores. Los usuarios pueden acceder a los desinstaladores a través del elemento Programas de la Panel de control.
-   Archivos de ayuda. Incluya temas de ayuda directamente en la aplicación.
-   Opciones y configuración de la aplicación. Incluya la interfaz de usuario para configurar las opciones de una aplicación dentro de la aplicación o cree un elemento Panel de control aplicación.
-   Sitios web. Proporcione los vínculos adecuados a información como los sitios de ayuda y soporte técnico directamente en la aplicación.
-   Asistentes. Los asistentes y otras tareas de configuración únicas deben iniciarse desde dentro de la aplicación.

NO CREAR: no cree accesos directos a características o funcionalidades que se puedan iniciar desde la propia aplicación. Por ejemplo, Language Configuración se puede configurar desde cualquier aplicación de Microsoft Office, por lo que tampoco es necesario tener un punto de entrada de Language Configuración independiente en el pantalla Inicio.

NO CREAR: No cree accesos directos a elementos que no sean archivos ejecutables. Los accesos directos que no se asignan a archivos ejecutables, como los accesos directos que inician sitios web o archivos de ayuda, se filtran del pantalla Inicio.

DO: Si instala un conjunto de aplicaciones en lugar de una sola aplicación, agregue un acceso directo para cada aplicación del conjunto. Como se mencionó anteriormente, evite crear accesos directos a la funcionalidad secundaria, como la información de ayuda, las utilidades y la configuración. Esa funcionalidad debe incluirse en las aplicaciones pertinentes del conjunto de aplicaciones.

DO: cree una carpeta de producto de un solo nivel para los conjuntos que contengan tres o más iconos. En la vista Aplicaciones de la pantalla Inicio, accesible desde el acceso de búsqueda, las aplicaciones se agrupan por su carpeta de nivel superior. Elija un nombre de carpeta descriptivo pero conciso; Se recomiendan tres palabras o menos. Tenga en cuenta que, aunque la vista Aplicaciones agrupa los iconos y muestra el nombre de la carpeta, este nombre no es visible cuando un icono está anclado al pantalla Inicio, por lo que debe hacer que los nombres de los iconos sean lo suficientemente descriptivos.

NO LO HAGA: no cree una carpeta de productos si el conjunto de aplicaciones contiene solo un acceso directo. Coloque el acceso directo en la carpeta Inicio de nivel superior.

DO: Al instalar un conjunto de más de tres aplicaciones, tenga en cuenta si alguna de esas aplicaciones es para uso secundario y más irregular y no debe anclarse al pantalla Inicio. Si es así, quizás esos iconos se puedan quitar por completo, según las instrucciones anteriores, y se pueden iniciar desde una aplicación principal. Si no puede quitar los iconos, considere la posibilidad de quitarlos del pantalla Inicio. De este modo, los accesos directos seguirán apareciendo en la vista Todas las aplicaciones, pero no abarrote los pantalla Inicio. 

Para crear un acceso directo de aplicación sin anclarlo al pantalla Inicio, establezca la siguiente propiedad en el acceso directo: System.AppUserModel.StartPinOption = 1. El nombre simbólico de 1 es APPUSERMODEL \_ STARTPINOPTION \_ NOPINONINSTALL.

Esto evita que el acceso directo se muestra en el pantalla Inicio, pero todavía se puede ver en la **vista Todas** las aplicaciones y en los resultados de búsqueda. Solo el usuario puede desanclar los accesos directos existentes, por lo que debe establecer esta propiedad durante la instalación o inmediatamente después de colocar la aplicación en el disco.

NO CREAR: No cree un icono para un host o entorno de ejecución para aplicaciones, como Silverlight o Java. Proporcione un punto de entrada para desinstalar el marco en Agregar o quitar programas y proporcione cualquier punto de entrada de configuración en Panel de control.

 

 



