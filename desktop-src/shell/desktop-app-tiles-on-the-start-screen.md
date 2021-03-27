---
description: A continuación se proporciona información sobre las opciones que se deben tener en cuenta al personalizar iconos de aplicaciones de escritorio para Windows 8, incluido cómo diseñar iconos de aplicaciones de escritorio para la nueva pantalla Inicio y cómo elegir qué puntos de entrada se van a mostrar en la pantalla Inicio.
ms.assetid: EF5182A2-09B2-46F2-B55E-4BD212CC1F7F
title: Iconos de la aplicación de escritorio en la pantalla Inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fcc5475732926300e2125ae9e97ea2d188bc468
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104361795"
---
# <a name="desktop-app-tiles-on-the-start-screen"></a>Iconos de la aplicación de escritorio en la pantalla Inicio

A continuación se proporciona información sobre las opciones que se deben tener en cuenta al personalizar iconos de aplicaciones de escritorio para Windows 8, incluido cómo diseñar iconos de aplicaciones de escritorio para la nueva pantalla Inicio y cómo elegir qué puntos de entrada se van a mostrar en la pantalla Inicio.

## <a name="design-your-tile-for-the-start-screen"></a>Diseñar el icono de la pantalla Inicio

Puede personalizar dos aspectos de los iconos de la aplicación de escritorio: el nombre de la aplicación y el icono. El color de fondo se deriva del color de fondo elegido por el usuario y no se puede personalizar mediante programación.

![Guía de diseño de iconos de aplicación.](images/tiles-desktop-1.png)

DO: Evite el truncamiento del nombre de la aplicación. Los iconos de escritorio anclados a la pantalla Inicio pueden dar cabida a dos líneas de texto en cada línea o aproximadamente diez caracteres (aunque esto depende del idioma de la interfaz de usuario), por lo que debe intentar mantener el nombre de la aplicación lo suficientemente corto como para evitar el truncamiento.

HACER: proporcione iconos para los cuatro valores de escala de la pantalla de inicio admitidos para asegurarse de que los iconos se ven nítidos en todos los factores de forma.



| Escala | Tamaño de mosaico (en píxeles) | Tamaño de icono usado (en píxeles) |
|-------|-----------------------|----------------------------|
| 80 %   | 120 x 120             | 48 x 48                    |
| 100%  | 150 x 150             | 64 x 64                    |
| 140%  | 210 x 210             | 96 x 96                    |
| 180%  | 270 x 270             | 128 x 128                  |



 

DO: adopte los principios de diseño de Microsoft. La nueva apariencia de los iconos es plana, por lo que si desea imitar los iconos de la aplicación de la tienda Windows para la aplicación de escritorio, considere la posibilidad de sacar sombras paralelas, etc.

NO: no Evite el uso de color. Aunque los iconos de la aplicación de la tienda Windows a veces son monocromáticas, se recomienda usar iconos de color para las aplicaciones de escritorio. Esto ayuda a diferenciar las aplicaciones de escritorio en la barra de tareas y desde otros iconos de la aplicación de escritorio en la pantalla Inicio, ya que no se puede personalizar el color de fondo de los iconos del escritorio. Considere la posibilidad de usar colores más saturados.

## <a name="decide-the-right-entry-points-to-include-in-the-start-screen"></a>Decidir los puntos de entrada correctos que se van a incluir en la pantalla Inicio

HACER: Agregue un acceso directo por aplicación en la pantalla Inicio cuando se instale la aplicación. Esto garantiza que los usuarios puedan iniciar la aplicación directamente desde la pantalla Inicio o mediante la búsqueda. Si no incluye un acceso directo en la pantalla Inicio, la aplicación se vuelve difícil de iniciar. En concreto, no agregue un acceso directo solo en el escritorio. Los usuarios ven la pantalla Inicio cuando inician sesión por primera vez, por lo que colocar un acceso directo solo en el escritorio no es tan eficaz como incluirlo en la pantalla Inicio.

![Diagrama que muestra una cuadrícula con un icono de aplicación, dimensiones y "semiluz semiligera" para indicar la fuente utilizada.](images/tiles-desktop-2.png)

NO: no se proporcionan varios accesos directos a la misma aplicación. Por ejemplo, no tenga dos accesos directos que inicien una aplicación en dos modos diferentes, como uno para Windows Internet Explorer y otro para Internet Explorer sin complementos.

HACER: minimice el número de iconos que se agregan como parte de la instalación de. Considere la posibilidad de exponer otros puntos de entrada a las aplicaciones extrañas. Por ejemplo, en lugar de incluir una aplicación de configuración independiente con una aplicación de consola, acceda a la configuración a través de una característica de la aplicación de consola.

NO: no coloque accesos directos a los elementos siguientes en la pantalla Inicio:

-   Desinstaladores. Los usuarios pueden tener acceso a los Desinstaladores a través del elemento programas del panel de control.
-   Archivos de ayuda. Incluir temas de ayuda directamente en la aplicación.
-   Opciones y configuración de la aplicación. Incluye la interfaz de usuario para configurar las opciones de una aplicación dentro de la aplicación o crear un elemento del panel de control.
-   Sitios Web. Proporcione los vínculos adecuados a información como la ayuda y los sitios de soporte técnico directamente en su aplicación.
-   Asistentes. Los asistentes y otras tareas de configuración de una vez deben iniciarse desde la aplicación.

NO: no cree accesos directos a características o funciones que se pueden iniciar desde la propia aplicación. Por ejemplo, la configuración de idioma se puede configurar desde cualquier Microsoft Office aplicación, por lo que también es necesario tener un punto de entrada de configuración de idioma independiente en la pantalla Inicio.

NO: no cree accesos directos a elementos que no sean archivos ejecutables. Los métodos abreviados que no se asignan a los ejecutables, como los métodos abreviados que inician sitios web o archivos de ayuda, se filtran de la pantalla Inicio.

DO: Si instala un conjunto de aplicaciones en lugar de una sola aplicación, agregue un acceso directo para cada aplicación del conjunto. Como se mencionó anteriormente, Evite crear accesos directos a la funcionalidad secundaria, como la información de ayuda, las utilidades y la configuración. Esa funcionalidad debe incluirse en las aplicaciones relevantes del conjunto.

HACER: cree una carpeta de producto de un solo nivel para conjuntos que contengan tres o más mosaicos. En la vista aplicaciones de la pantalla Inicio, accesible desde el acceso de búsqueda, las aplicaciones se agrupan por su carpeta de nivel superior. Elija un nombre de carpeta descriptivo pero conciso; se recomiendan tres palabras o menos. Tenga en cuenta que mientras que la vista aplicaciones agrupa iconos y muestra el nombre de la carpeta, este nombre no está visible cuando se ancla un icono a la pantalla Inicio, por lo que los nombres de los iconos deben ser suficientemente descriptivos.

NO: no cree una carpeta de producto si el conjunto contiene un solo método abreviado. Coloque el acceso directo en la carpeta de inicio de nivel superior.

HACER: al instalar un conjunto de más de tres aplicaciones, tenga en cuenta si alguna de esas aplicaciones es para uso secundario, más irregular y no debe anclarse a la pantalla Inicio. Si es así, es posible que los mosaicos se quiten por completo, según las instrucciones anteriores, y que se inicien desde una aplicación principal. Si no puede quitar los mosaicos, considere la posibilidad de desanclarlos de la pantalla Inicio. De este modo, los accesos directos seguirán apareciendo en la vista **todas las aplicaciones** , pero no abarrotarán la pantalla Inicio del usuario.

Para crear un acceso directo de la aplicación sin anclarlo a la pantalla Inicio, establezca la siguiente propiedad en el método abreviado: System. AppUserModel. StartPinOption = 1. El nombre simbólico para 1 es APPUSERMODEL \_ STARTPINOPTION \_ NOPINONINSTALL.

Esto evita que se muestre el acceso directo en la pantalla Inicio, pero todavía se puede ver en la vista **todas las aplicaciones** y en los resultados de la búsqueda. Solo el usuario puede desanclar los accesos directos existentes, por lo que debe establecer esta propiedad durante la instalación o inmediatamente después de colocar la aplicación en el disco.

NO: no cree un icono para un host o en tiempo de ejecución para aplicaciones, como Silverlight o Java. Proporcione un punto de entrada para desinstalar el marco en Agregar o quitar programas y especifique el punto de entrada de configuración en el panel de control.

 

 



