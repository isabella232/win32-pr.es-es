---
title: Procedimientos de accesibilidad recomendados
description: La implementación de los procedimientos recomendados descritos en esta sección ayuda a garantizar que la aplicación sea accesible para las personas que usan productos de tecnología de asistencia.
ms.assetid: ef694361-49b7-424c-a583-1eadc2519db7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38d9f70828610d04255b61ad3ee533d23c514867
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070731"
---
# <a name="accessibility-best-practices"></a>Procedimientos de accesibilidad recomendados

La implementación de los procedimientos recomendados descritos en esta sección ayuda a garantizar que la aplicación sea accesible para las personas que usan productos de tecnología de asistencia. Muchos de estos procedimientos recomendados se centran en un buen diseño de la interfaz de usuario. Cada procedimiento recomendado incluye información de implementación para controles o aplicaciones. En muchos casos, gran parte del trabajo para cumplir estos procedimientos recomendados ya está incluido en los controles.

En este tema se incluyen las siguientes secciones.

-   [Acceso mediante programación](#programmatic-access)
    -   [Habilitar el acceso mediante programación a todos los elementos de la interfaz de usuario y el texto](#enable-programmatic-access-to-all-ui-elements-and-text)
    -   [Colocar nombres, títulos y descripciones en objetos de interfaz de usuario, marcos y páginas](#place-names-titles-and-descriptions-on-ui-objects-frames-and-pages)
    -   [Asegurarse de que todas las actividades de la interfaz de usuario activan eventos mediante programación](#ensure-programmatic-events-are-triggered-by-all-ui-activities)
-   [Configuración de usuario](#user-settings)
    -   [Respetar todas las configuraciones de todo el sistema y no interferir con las funciones de accesibilidad](#respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions)
-   [Diseño visual de la interfaz de usuario](#visual-ui-design)
    -   [No se Hard-Code colores](#do-not-hard-code-colors)
    -   [Compatibilidad con el contraste alto y todos los atributos de visualización del sistema](#support-high-contrast-and-all-system-display-attributes)
    -   [Asegurarse de que toda la interfaz de usuario se escale correctamente con cualquier configuración de PPP](#ensure-all-ui-correctly-scales-by-any-dpi-setting)
-   [Navegación con el teclado](#keyboard-navigation)
    -   [Proporcionar la interfaz de teclado a todos los elementos de la interfaz de usuario](#provide-keyboard-interface-for-all-ui-elements)
    -   [Mostrar el foco del teclado](#show-the-keyboard-focus)
    -   [Compatibilidad con los estándares de navegación y esquemas de navegación eficaces](#support-navigation-standards-and-powerful-navigation-schemes)
    -   [No dejar que la ubicación del mouse interfiera con la navegación mediante el teclado](#do-not-let-mouse-location-interfere-with-keyboard-navigation)
-   [Interfaz multimodal](#multi-modal-interface)
    -   [Proporcionar equivalentes seleccionables por el usuario para los elementos no textuales](#provide-user-selectable-equivalents-for-non-text-elements)
    -   [Usar color, pero proporcionar también alternativas al color](#use-color-but-also-provide-alternatives-to-color)
    -   [Usar la API de entrada estándar con llamadas independientes del dispositivo](#use-standard-input-apis-with-device-independent-calls)
-   [Temas relacionados](#related-topics)

## <a name="programmatic-access"></a>Acceso mediante programación

Los procedimientos recomendados de esta sección son que los productos de tecnología de asistencia tienen acceso mediante programación adecuado a la información y funcionalidad de la interfaz de usuario.

### <a name="enable-programmatic-access-to-all-ui-elements-and-text"></a>Habilitar el acceso mediante programación a todos los elementos de la interfaz de usuario y el texto

Los elementos de la interfaz de usuario de la aplicación deben ser accesibles mediante programación para los productos de tecnología de asistencia. Todos los elementos de la interfaz de usuario deben tener etiquetas, deben exponer todos los valores de propiedad y deben generar todos los eventos adecuados. Para los controles Windows estándar, la mayor parte de este trabajo ya se realiza a través de microsoft Automatización de la interfaz de usuario y Microsoft Active Accessibility proxy. Sin embargo, los controles personalizados requieren trabajo adicional para asegurarse de que están totalmente expuestos para que los proveedores de tecnología de asistencia puedan identificar y manipular elementos de la interfaz de usuario de la aplicación.

Seguir este procedimiento recomendado permite a los proveedores de tecnología de asistencia identificar y manipular elementos de la interfaz de usuario del producto.

### <a name="place-names-titles-and-descriptions-on-ui-objects-frames-and-pages"></a>Colocar nombres, títulos y descripciones en objetos de interfaz de usuario, marcos y páginas

Dado que los productos de tecnología de asistencia, especialmente los lectores de pantalla, usan títulos para comprender la ubicación de un marco, un objeto o una página en el esquema de navegación, los títulos deben ser muy descriptivos. Los buenos títulos descriptivos permiten a los productos de tecnología de asistencia identificar y manipular elementos de interfaz de usuario en controles y aplicaciones. Por ejemplo, un título de página web de "Página web de Microsoft" no sirve para nada si el usuario ha navegado profundamente a un área determinada. Un título descriptivo es fundamental para los usuarios que son invidentes y dependen de lectores de pantalla.

Seguir este procedimiento recomendado permite que los productos de tecnología de asistencia identifiquen y manipulen la interfaz de usuario en aplicaciones y controles de ejemplo.

### <a name="ensure-programmatic-events-are-triggered-by-all-ui-activities"></a>Asegurarse de que todas las actividades de la interfaz de usuario activan eventos mediante programación

La aplicación debe generar eventos cada vez que se produzcan cambios en el estado o la apariencia de un elemento de la interfaz de usuario.

Siguiendo este procedimiento recomendado, los productos de tecnología de asistencia pueden escuchar los cambios en la interfaz de usuario y notificar al usuario estos cambios.

## <a name="user-settings"></a>Configuración del usuario

Con el procedimiento recomendado de esta sección, puede asegurarse de que los controles o las aplicaciones no sobrescriban la configuración del usuario.

### <a name="respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions"></a>Respetar todas las configuraciones de todo el sistema y no interferir con las funciones de accesibilidad

Los usuarios pueden usar Panel de control para establecer algunas marcas de todo el sistema; otras marcas se pueden establecer mediante programación. Esta configuración no debe cambiarse con controles ni aplicaciones. Además, las aplicaciones deben admitir la configuración de accesibilidad de su sistema operativo host.

Seguir este procedimiento recomendado permite a los usuarios establecer la configuración de accesibilidad y saber que las aplicaciones no cambiarán esa configuración.

## <a name="visual-ui-design"></a>Diseño visual de la interfaz de usuario

Los procedimientos recomendados de esta sección garantizan que los controles o las aplicaciones usen el color y las imágenes de forma eficaz y que los productos de tecnología de asistencia puedan usarlos.

### <a name="do-not-hard-code-colors"></a>No se Hard-Code colores

Es posible que las personas que son daltónicas, tienen poca visión o usan una pantalla en blanco y negro no puedan utilizar las aplicaciones con colores codificados de forma rígida.

Seguir este procedimiento recomendado permite a los usuarios ajustar las combinaciones de colores en función de sus necesidades individuales.

### <a name="support-high-contrast-and-all-system-display-attributes"></a>Compatibilidad con el contraste alto y todos los atributos de visualización del sistema

Las aplicaciones no deben interrumpir ni deshabilitar la configuración de contraste seleccionada por el usuario para todo el sistema, así como las selecciones de color u otros atributos y configuraciones de visualización para todo el sistema. La configuración del sistema adoptada por un usuario mejora la accesibilidad de las aplicaciones, por lo que las aplicaciones no deben deshabilitarla ni ignorarla. El color se debe utilizar en su combinación correcta de primer plano y fondo para proporcionar el contraste apropiado. No se deben mezclar colores no relacionados y no se deben invertir los colores.

Muchos usuarios necesitan combinaciones concretas de contraste alto, como texto blanco sobre un fondo negro. Si se dibujan invertidas, por ejemplo, como texto negro sobre un fondo blanco, esto hará que el fondo se superponga al primer plano y puede dificultar la lectura de algunos usuarios.

### <a name="ensure-all-ui-correctly-scales-by-any-dpi-setting"></a>Asegurarse de que toda la interfaz de usuario se escale correctamente con cualquier configuración de PPP

Asegúrese de que todos los elementos de la interfaz de usuario se puedan escalar correctamente por cualquier configuración de puntos por pulgada (ppp). Además, asegúrese de que los elementos de la interfaz de usuario quepa en una pantalla de 1024 x 768 con 120 puntos por pulgada (ppp).

## <a name="keyboard-navigation"></a>Navegación mediante teclado

Los procedimientos recomendados de esta sección garantizan que toda la funcionalidad de la aplicación sea accesible para los usuarios que dependen del teclado.

### <a name="provide-keyboard-interface-for-all-ui-elements"></a>Proporcionar la interfaz de teclado a todos los elementos de la interfaz de usuario

Las tabulaciones, especialmente cuando se planean cuidadosamente, dan a los usuarios otra manera de navegar por la interfaz de usuario.

Las aplicaciones deben proporcionar las interfaces de teclado siguientes:

-   Tabulación para todos los controles con los que el usuario puede interactuar, como botones, vínculos o cuadros de lista.
-   Orden de tabulación lógico.

### <a name="show-the-keyboard-focus"></a>Mostrar el foco del teclado

Los usuarios necesitan saber qué objeto tiene el foco del teclado para poder prever el efecto de las pulsaciones de teclas. Para resaltar el foco del teclado, utilice colores, fuentes o gráficos como rectángulos o ampliaciones. Para resaltar de forma audible el foco del teclado, cambie el volumen, el tono o la calidad del tono.

Para evitar confusiones, las aplicaciones deben ocultar todos los indicadores de foco visuales y atenuar las selecciones que se encuentran en las ventanas, o los paneles, inactivos.

Las aplicaciones deben hacer lo siguiente con el foco del teclado:

-   Un elemento siempre debe tener el foco de teclado.
-   El foco del teclado debe ser visible y obvio.
-   Las selecciones o los elementos centrados deben resaltarse visualmente.

### <a name="support-navigation-standards-and-powerful-navigation-schemes"></a>Compatibilidad con los estándares de navegación y esquemas de navegación eficaces

Los distintos aspectos de la navegación mediante el teclado proporcionan distintas maneras para que los usuarios naveguen por la interfaz de usuario.

Las aplicaciones deben proporcionar las interfaces de teclado siguientes:

-   Teclas de método abreviado y teclas de acceso subrayadas para todos los comandos, menús y controles.
-   Métodos abreviados de teclado para vínculos importantes.
-   Todos los elementos de menú tienen una clave de acceso; todos los botones tienen teclas de aceleración, todos los comandos tienen una tecla de aceleración.

### <a name="do-not-let-mouse-location-interfere-with-keyboard-navigation"></a>No dejar que la ubicación del mouse interfiera con la navegación mediante el teclado

La ubicación del mouse no debe interferir con la navegación mediante el teclado. Por ejemplo, si el mouse está situado en un lugar y el usuario navega con el teclado, no debería producirse un clic del mouse si no lo inicia el usuario.

## <a name="multi-modal-interface"></a>Interfaz multimodal

El procedimiento recomendado de esta sección garantiza que la interfaz de usuario de la aplicación incluye alternativas para los elementos visuales.

### <a name="provide-user-selectable-equivalents-for-non-text-elements"></a>Proporcionar equivalentes seleccionables por el usuario para los elementos no textuales

Para cada elemento no textual, proporcione un equivalente seleccionable por el usuario para el texto, transcripciones o descripciones de audio, como texto alternativo, títulos o comentarios visuales.

Los elementos que no son de texto cubren una amplia gama de elementos de la interfaz de usuario, como imágenes, regiones de mapa de imágenes, animaciones, applets, fotogramas, scripts, botones gráficos, sonidos, archivos de audio independientes y vídeo. Los elementos que no son de texto son importantes cuando contienen información visual, voz o información de audio general a la que el usuario necesita acceso para comprender el contenido de la interfaz de usuario.

### <a name="use-color-but-also-provide-alternatives-to-color"></a>Usar color, pero proporcionar también alternativas al color

Use el color para mejorar, enfatizar o reiterar la información que se muestra por otros medios, pero no comunique la información con el color exclusivamente. Los usuarios daltónicos o con pantallas monocromáticas necesitan alternativas al color.

### <a name="use-standard-input-apis-with-device-independent-calls"></a>Usar la API de entrada estándar con llamadas independientes del dispositivo

Las llamadas independientes del dispositivo garantizan que todos los dispositivos de entrada se tratan por igual, a la vez que proporcionan productos de tecnología de asistencia con la información necesaria sobre la interfaz de usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Introducción a la API de Automation](windows-automation-api-overview.md)
</dt> </dl>

 

 




