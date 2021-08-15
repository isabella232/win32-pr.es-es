---
title: Windows Guías para desarrolladores del marco de opciones
description: Los temas contenidos en esta sección describen aspectos específicos del marco Windows ribbon.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Windows Cinta de opciones, marco
- Cinta de opciones, marco
- Windows Cinta de opciones, guías para desarrolladores
- Cinta de opciones, guías para desarrolladores
- guías para desarrolladores para Windows cinta de opciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b30c5b2564dc918c6f9accfe5a5cb36a2d77222e3822a75a76332b1d3234cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850633"
---
# <a name="windows-ribbon-framework-developer-guides"></a>Windows Guías para desarrolladores del marco de opciones

Los temas contenidos en esta sección describen aspectos específicos del marco Windows ribbon.

## <a name="basics"></a>Aspectos básicos

[Crear una aplicación de cinta de opciones](windowsribbon-stepbystep.md)

Para que Windows de la cinta de opciones consuma el archivo de marcado de la cinta de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario. Un compilador de marcado de cinta dedicado, el compilador de comandos de interfaz de usuario (UICC), se incluye con el Kit de desarrollo de software (SDK) de Microsoft Windows (7.0 o posterior) para este propósito. Además de compilar la versión binaria del marcado de la cinta de opciones, uicc genera un archivo de encabezado de definición de identificador (.h) que expone todos los elementos de marcado a la aplicación host de la cinta de opciones y un archivo de recursos (.rc) que se usa para vincular recursos de imagen y cadena a la aplicación host en tiempo de compilación.

[Migración al marco de Windows cinta de opciones](ribbon-migration.md)

Una aplicación que se basa en menús tradicionales, barras de herramientas y cuadros de diálogo se puede migrar a la interfaz de usuario (UI) enriquección, dinámica y controlada por contexto del sistema de comandos del marco de opciones. Se trata de una manera fácil y eficaz de modernizar y reactivar la aplicación a la vez que se mejora la accesibilidad, la facilidad de uso y la detectabilidad de su funcionalidad.

[Descripción de comandos y controles](windowsribbon-commandscontrols.md)

La separación de la lógica de la presentación es la filosofía de diseño que inspira el sistema de presentación de comandos del marco de la cinta de opciones, un sistema basado en un patrón de diseño donde la funcionalidad y el comportamiento se implementan independientemente de los controles que exponen esta funcionalidad.

## <a name="user-interface"></a>Interfaz de usuario

[Especificar recursos de imagen de cinta de opciones](windowsribbon-imageformats.md)

Como sistema de presentación de comandos enriquecido, el marco de la cinta de opciones está diseñado para admitir ampliamente los recursos de imagen en toda la interfaz de usuario (UI) de la cinta de opciones. Todos los recursos de imagen se declaran en el [marcado de la](windowsribbon-schema.md) cinta de opciones o se consultan desde una aplicación host de la cinta de opciones.

Para Windows 8 y versiones posteriores, el marco de la cinta de opciones admite los siguientes formatos gráficos: archivos de mapa de bits ARGB (BMP) de 32 bits y archivos de gráficos de red portátiles (PNG) con transparencia.

Para Windows 7 y versiones anteriores, los recursos de imagen deben ajustarse al formato de gráfico BMP estándar que se usa en Windows.

[Personalizar una cinta de opciones mediante definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)

Los controles hospedados en la barra de comandos de la cinta de opciones están sujetos a reglas de diseño que exige el marco de la cinta de opciones y se basan en una combinación de comportamientos predeterminados y plantillas de diseño (tanto definidas como personalizadas por el marco) tal y como se declara en el marcado de la cinta de opciones. Estas reglas definen los comportamientos de diseño adaptable del marco de la cinta de opciones que influyen en cómo los controles de la barra de comandos se adaptan a varios tamaños de cinta en tiempo de ejecución.

[Trabajar con galerías](ribbon-controls-galleries.md)

El marco de la cinta de opciones proporciona a los desarrolladores un modelo sólido y coherente para administrar contenido dinámico en una variedad de controles basados en colecciones. Al adaptar y volver a configurar la interfaz de usuario (UI) de la cinta de opciones, estos controles dinámicos permiten al marco responder a la interacción del usuario tanto en la aplicación host como en la propia cinta de opciones, y proporcionan la flexibilidad necesaria para controlar varios entornos en tiempo de ejecución.

[Mostrar pestañas contextuales](ribbon-contextualtabs.md)

En una aplicación de marco de cinta de opciones, una pestaña contextual es un control [Tab](windowsribbon-controls-tab.md) oculto que se muestra en la fila de pestaña cuando se selecciona o resalta un objeto en el área de trabajo de la aplicación, como una imagen.

[Reconfiguración de la cinta de opciones con modos de aplicación](ribbon-applicationmodes.md)

El marco de la cinta de opciones admite la reconfiguración y exposición dinámicas de los elementos principales de la interfaz de usuario (UI) de la cinta de opciones en tiempo de ejecución, en función del estado de la aplicación (también denominado contexto). Declarados y asociados a elementos específicos en el marcado, los distintos estados admitidos por una aplicación se conocen como modos de aplicación.

[Personalización de los colores de la cinta de opciones](ribbon-color.md)

El marco de la cinta de opciones expone un conjunto de propiedades de color que permiten a una aplicación personalizar la apariencia de varios elementos de la interfaz de usuario (UI) de la cinta de opciones en tiempo de ejecución.

[Mostrar la cinta de opciones](ribbon-visibility.md)

El marco de la cinta de opciones expone un conjunto de propiedades que permiten a una aplicación especificar cómo se muestra la interfaz de usuario (UI) de la cinta en tiempo de ejecución.

## <a name="management"></a>Administración

[Estado de la cinta de opciones persistente](ribbon-statepersistence.md)

El Windows marco de trabajo de Nidón (cinta de opciones) proporciona la capacidad de conservar el estado de una variedad de configuraciones de usuario y preferencias en las sesiones de la aplicación.

[Escuchar eventos de la cinta de opciones](listening-for-ribbon-events.md)

El marco de la cinta de opciones usa la infraestructura de seguimiento de eventos [para Windows (ETW)](../etw/event-tracing-portal.md) para permitir a los desarrolladores aprender cómo interactúan los usuarios con la cinta de opciones de su aplicación.

## <a name="markup-compiler"></a>Compilador de marcado

[Compilación del marcado de la cinta de opciones](windowsribbon-intentcl.md)

Para que el marco de la cinta de opciones consuma el archivo de marcado [de](windowsribbon-schema.md) la cinta de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario. Un compilador de marcado dedicado, el compilador de comandos de interfaz de usuario (UICC), se incluye con el Kit de desarrollo de software (SDK) de Microsoft Windows (7.0 o posterior) para este propósito. Además de compilar la versión binaria del marcado, uicc genera un archivo de encabezado de definición de identificador (.h) que expone todos los elementos de marcado a la aplicación host de la cinta de opciones y un archivo de recursos (.rc) que se usa para vincular recursos de imagen y cadena a la aplicación host en tiempo de compilación.

[Descripción de los mensajes del compilador de marcado](windowsribbon-compilationerrors.md)

El compilador de marcado Windows Ribbon Framework (Ribbon), ui Command Compiler (UICC.exe), valida el marcado de la cinta de opciones con el esquema de la cinta de opciones y un conjunto adicional de reglas definido por el marco de la cinta.

 

 