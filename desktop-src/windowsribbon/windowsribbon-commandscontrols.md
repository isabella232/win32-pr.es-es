---
title: Descripción de los comandos y controles
description: La separación de la lógica de la presentación es la filosofía de diseño que inspira el sistema de presentación de comandos del marco de la cinta de opciones de Windows \ 8212; un sistema basado en un patrón de diseño donde la funcionalidad y el comportamiento se implementan independientemente de los controles que exponen esta funcionalidad.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Windows Cinta de opciones, información general sobre comandos
- Cinta de opciones, información general sobre comandos
- Windows Cinta de opciones, información general sobre controles
- Cinta de opciones, información general sobre controles
- sistema de comandos para Windows cinta de opciones
- controles para Windows cinta de opciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467126"
---
# <a name="understanding-commands-and-controls"></a>Descripción de los comandos y controles

La separación de la lógica de la presentación es la filosofía de diseño que inspira el sistema de presentación de comandos del marco de la cinta de opciones de Windows, un sistema basado en un patrón de diseño donde la funcionalidad y el comportamiento se implementan independientemente de los controles que exponen esta funcionalidad.

-   [Introducción](#introduction)
-   [El Windows de comandos de la cinta de opciones](#the-windows-ribbon-command-system)
    -   [Controles](#understanding-commands-and-controls)
    -   [Comandos](#understanding-commands-and-controls)
    -   [La experiencia de comando en acción](#the-command-experience-in-action)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

En este artículo se describe el diseño del sistema de comandos del marco de cinta de opciones. Describe los conceptos de comandos y controles y explora cómo funcionan conjuntamente para proporcionar una experiencia de comandos enriquecida con una gran cantidad de nuevas funcionalidades de interfaz de usuario.

## <a name="the-windows-ribbon-command-system"></a>El sistema Windows de la cinta de opciones

En el marco de la cinta de opciones, los comandos y los controles son entidades independientes. Un comando es una estructura abstracta, sin restricciones de presentación, que representa una tarea o clase específica de funcionalidad. Por otro lado, un control es un objeto concreto que expone la funcionalidad Command a través de la interfaz de usuario de la cinta de opciones.

Esta distinción proporciona la capacidad de definir comandos que no tienen detalles de la interfaz de usuario y que pueden ejecutarse con la intención de una acción sin necesidad de administrar cómo se invocó la acción.

### <a name="controls"></a>Controles

Los controles son los objetos de interfaz de usuario necesarios para la presentación de comandos. El marco los representa y administra en tiempo de ejecución en función de la interacción del usuario y un conjunto de propiedades y comportamientos inherentes.

Conocida como diseño adaptable, la flexibilidad administrada por el marco de trabajo de la interfaz de usuario es uno de los grandes puntos fuertes de la cinta de opciones. Los controles de la cinta de opciones pueden volver a configurarse automáticamente a través de plantillas de diseño dependientes del marco o definidas por el desarrollador que pueden responder a varios requisitos de tiempo de ejecución, todo ello sin escribir una sola línea de código de presentación. Para más información, consulte [Personalización de una cinta de opciones mediante definiciones de tamaño y Directivas de escalado.](windowsribbon-templates.md)

Además de las ventajas del diseño adaptable, una serie de controles complejos de la cinta de opciones proporcionan soluciones independientes para espacios de problemas de interfaz de usuario específicos. Al ofrecer un modelo de interacción sofisticado, los controles ribbon, como FontControl o ColorPicker, proporcionan la capacidad de manipular datos en términos más abstractos a través de bolsa de propiedades de atributos de fuente o color reales en lugar de a través de varios subcontroles, enumeraciones y valores de índice de controles Windows estándar.

### <a name="commands"></a>Comandos:

Acopladas de forma flexible a los controles de la cinta de opciones que exponen su funcionalidad, las implementaciones de comandos son el dominio de la aplicación host y toman la forma de agentes de escucha de eventos, controladores de comandos y varias propiedades Command.

Los comandos se declaran en el marcado de la cinta de opciones con un identificador único o se les asigna un identificador generado por el compilador de marcado durante la compilación. Los comandos están asociados a controles a través de un nombre de comando, pero, a diferencia de los controles, su funcionalidad real se define en el código, donde están enlazados a controladores de comandos específicos a través del identificador de comando.

> [!Note]  
> En la compilación, este identificador se almacena en un archivo de encabezado de definición de identificador que expone Comandos a sus controladores de comandos correspondientes en la aplicación host de la cinta de opciones.

 

Cada comando tiene un tipo command subyacente con elementos en la [**\_ enumeración COMMANDTYPE de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) interfaz de usuario.

### <a name="the-command-experience-in-action"></a>La experiencia de comando en acción

Las funcionalidades de este modelo de comandos se muestran en la barra de herramientas de acceso rápido (QAT) de la cinta de opciones. El QAT proporciona a los usuarios finales una manera de definir fácilmente sus propios accesos directos para prácticamente cualquier control en la interfaz de usuario de la cinta de opciones. Un acceso directo se agrega dinámicamente al QAT en tiempo de ejecución cuando el usuario hace clic con el botón derecho en un control de cinta de opciones y selecciona **Agregar** a la barra de herramientas de acceso rápido en el menú contextual.

En la imagen siguiente  se muestra **el** control Pegar y pegar desde comandos, representado por un control [**SplitButton,**](windowsribbon-element-splitbutton.md) en la cinta de opciones Windows 7 Paint.

![imagen del botón de división pegar en la cinta de microsoft paint.](images/overviews/paint-paste-splitbutton-ribbon.png)

En la siguiente  imagen  se muestra la misma opción Pegar y pegar desde comandos, todavía representada por un control [**SplitButton,**](windowsribbon-element-splitbutton.md) en el QAT de la cinta de Windows 7 Paint.

![imagen del botón de división pegar en el qat de microsoft paint.](images/overviews/paint-paste-splitbutton-qat.png)

Cuando el QAT hospeda un control , la nueva instancia del control mantiene toda la funcionalidad del control original sin necesidad de que los agentes de escucha de eventos adicionales y los controladores de comandos lo admitan. Ambos controles están enlazados al mismo controlador de comandos de la cinta de opciones a través de un identificador de comando compartido. De este modo, el marco trata ambos controles como uno, independientemente de cuál se invoque.

> [!Note]  
> Las mismas ventajas se realizan cuando los comandos se incorporan a [**un ContextPopup en**](windowsribbon-element-contextpopup.md) tiempo de diseño. En este caso, se pueden usar los controladores Pegar comando si el control [**SplitButton**](windowsribbon-element-splitbutton.md) aparece en la cinta de opciones, el QAT o **ContextPopup**.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Presentación del marco de Windows ribbon](windowsribbon-introduction.md)
</dt> <dt>

[Creación de una aplicación de cinta de opciones](windowsribbon-stepbystep.md)
</dt> <dt>

[Declarar comandos y controles con marcado de cinta](windowsribbon-schema.md)
</dt> </dl>

 

 