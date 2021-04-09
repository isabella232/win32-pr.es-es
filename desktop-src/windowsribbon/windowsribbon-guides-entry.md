---
title: Guías para desarrolladores del marco de cinta de Windows
description: Los temas incluidos en esta sección describen aspectos específicos del marco de la cinta de opciones de Windows.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Cinta de Windows, marco
- Cinta de opciones, marco
- Cinta de opciones de Windows, guías para desarrolladores
- Cinta de opciones, guías para desarrolladores
- guías del desarrollador para la cinta de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149531"
---
# <a name="windows-ribbon-framework-developer-guides"></a>Guías para desarrolladores del marco de cinta de Windows

Los temas incluidos en esta sección describen aspectos específicos del marco de la cinta de opciones de Windows.

## <a name="basics"></a>Aspectos básicos

[Crear una aplicación de cinta](windowsribbon-stepbystep.md)

Para que el marco de la cinta de opciones de Windows consuma el archivo de marcado de la cinta de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario. Un compilador de marcado de cinta dedicado, el compilador de comandos de interfaz de usuario (UICC), se incluye en el kit de desarrollo de software (SDK) de Microsoft Windows (7,0 o posterior) para este propósito. Además de compilar la versión binaria del marcado de la cinta, UICC genera un archivo de encabezado de definición de identificador (. h) que expone todos los elementos de marcado a la aplicación host de la cinta de opciones y un archivo de recursos (. RC) que se usa para vincular los recursos de imagen y de cadena a la aplicación host en tiempo de compilación.

[Migrar al marco de cinta de Windows](ribbon-migration.md)

Una aplicación que se basa en los menús, las barras de herramientas y los cuadros de diálogo tradicionales se puede migrar a la interfaz de usuario (UI) enriquecida, dinámica y controlada por el contexto del sistema de comandos del marco de cinta. Esta es una manera fácil y eficaz de modernizar y revitalizar la aplicación, a la vez que mejora la accesibilidad, la facilidad de uso y la capacidad de detección de su funcionalidad.

[Descripción de los comandos y los controles](windowsribbon-commandscontrols.md)

La separación de la lógica de la presentación es la filosofía de diseño que inspira el sistema de presentación de comandos del marco de la cinta de opciones, un sistema basado en un modelo de diseño donde la funcionalidad y el comportamiento se implementan independientemente de los controles que exponen esta funcionalidad.

## <a name="user-interface"></a>Interfaz de usuario

[Especificar recursos de imagen de cinta](windowsribbon-imageformats.md)

Como sistema de presentación de comandos enriquecido, el marco de la cinta de opciones se ha diseñado para admitir los recursos de imagen en gran medida a través de la interfaz de usuario (UI) de la cinta. Todos los recursos de imagen se declaran en el [marcado de la cinta](windowsribbon-schema.md) o se consultan desde una aplicación host de cinta.

En Windows 8 y versiones posteriores, el marco de la cinta de opciones admite los siguientes formatos de gráficos: archivos de mapa de bits ARGB de 32 bits (BMP) y archivos PNG (Portable Network Graphics) con transparencia.

En Windows 7 y versiones anteriores, los recursos de imagen deben ajustarse al formato de gráficos BMP estándar usado en Windows.

[Personalización de una cinta a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)

Los controles hospedados en la barra de comandos de la cinta están sujetos a las reglas de diseño que aplica el marco de la cinta de opciones y en función de una combinación de comportamientos y plantillas de diseño predeterminados (definidas por el marco y personalizadas) como se declara en el marcado de la cinta. Estas reglas definen los comportamientos de diseño adaptable del marco de cinta que influyen en cómo se adaptan los controles de la barra de comandos a varios tamaños de cinta en tiempo de ejecución.

[Trabajar con galerías](ribbon-controls-galleries.md)

El marco de la cinta de opciones proporciona a los desarrolladores un modelo sólido y coherente para administrar el contenido dinámico en diversos controles basados en colecciones. Al adaptar y volver a configurar la interfaz de usuario de la cinta de opciones, estos controles dinámicos permiten que el marco de trabajo responda a la interacción del usuario en la propia cinta y la aplicación host, y proporciona la flexibilidad necesaria para controlar diversos entornos en tiempo de ejecución.

[Mostrar pestañas contextuales](ribbon-contextualtabs.md)

En una aplicación de marco de cinta, una pestaña contextual es un control de [pestaña](windowsribbon-controls-tab.md) oculto que se muestra en la fila de pestañas cuando se selecciona o resalta un objeto en el área de trabajo de la aplicación, como una imagen.

[Volver a configurar la cinta de opciones con modos de aplicación](ribbon-applicationmodes.md)

El marco de la cinta de opciones admite la reconfiguración dinámica y la exposición de los elementos básicos de la interfaz de usuario (UI) de la cinta en tiempo de ejecución, en función del estado de la aplicación (también conocido como contexto). Declarado y asociado con elementos específicos en el marcado, los distintos Estados admitidos por una aplicación se conocen como modos de aplicación.

[Personalizar los colores de la cinta de opciones](ribbon-color.md)

El marco de la cinta de opciones expone un conjunto de propiedades de color que permiten a una aplicación personalizar la apariencia de varios elementos de la interfaz de usuario (UI) de la cinta en tiempo de ejecución.

[Mostrar la cinta de opciones](ribbon-visibility.md)

El marco de la cinta de opciones expone un conjunto de propiedades que permiten a una aplicación especificar cómo se muestra la interfaz de usuario (UI) de la cinta en tiempo de ejecución.

## <a name="management"></a>Administración

[Conservar el estado de la cinta](ribbon-statepersistence.md)

Windows Ribon Framework (cinta) ofrece la posibilidad de conservar el estado de una variedad de configuraciones y preferencias de usuario en las sesiones de la aplicación.

[Escuchar eventos de la cinta de opciones](listening-for-ribbon-events.md)

El marco de la cinta de opciones usa la infraestructura [de seguimiento de eventos para Windows (ETW)](../etw/event-tracing-portal.md) para que los desarrolladores puedan saber cómo interactúan los usuarios con la cinta de la aplicación.

## <a name="markup-compiler"></a>Compilador de marcado

[Compilar marcado de cinta](windowsribbon-intentcl.md)

Para que el marco de cinta utilice el archivo de marcado de la [cinta](windowsribbon-schema.md) de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario. Un compilador de marcado dedicado, el compilador de comandos de la interfaz de usuario (UICC), se incluye con el kit de desarrollo de software (SDK) de Microsoft Windows (SDK) (7,0 o posterior) para este propósito. Además de compilar la versión binaria del marcado, UICC genera un archivo de encabezado de definición de identificador (. h) que expone todos los elementos de marcado a la aplicación host de la cinta de opciones y un archivo de recursos (. RC) que se usa para vincular los recursos de imagen y de cadena a la aplicación host en tiempo de compilación.

[Descripción de los mensajes del compilador de marcado](windowsribbon-compilationerrors.md)

El compilador de marcado de Windows Ribbon Framework (cinta), el compilador de comandos de la interfaz de usuario (UICC.exe), valida el marcado de la cinta de opciones con el esquema de la cinta de opciones y un conjunto adicional de reglas definido por el marco de cinta.

 

 