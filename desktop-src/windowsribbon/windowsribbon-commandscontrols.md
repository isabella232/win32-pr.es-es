---
title: Descripción de los comandos y los controles
description: La separación de la lógica de la presentación es la filosofía de diseño que inspira el sistema de presentación de comandos del marco de la cinta de Windows \ 8212; un sistema basado en un modelo de diseño donde la funcionalidad y el comportamiento se implementan independientemente de los controles que exponen esta funcionalidad.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Cinta de Windows, información general sobre comandos
- Cinta, información general sobre comandos
- Cinta de Windows, información general sobre controles
- Cinta, información general sobre controles
- sistema de comandos para la cinta de Windows
- controles de la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104551019"
---
# <a name="understanding-commands-and-controls"></a>Descripción de los comandos y los controles

La separación de la lógica de la presentación es la filosofía de diseño que inspira el sistema de presentación de comandos del marco de la cinta de Windows, un sistema basado en un modelo de diseño donde la funcionalidad y el comportamiento se implementan independientemente de los controles que exponen esta funcionalidad.

-   [Introducción](#introduction)
-   [Sistema de comandos de la cinta de Windows](#the-windows-ribbon-command-system)
    -   [Controles](#understanding-commands-and-controls)
    -   [Comandos](#understanding-commands-and-controls)
    -   [La experiencia del comando en acción](#the-command-experience-in-action)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

En este artículo se describe el diseño del sistema de comandos del marco de cinta. Describe los conceptos de comandos y controles, y explora cómo funcionan conjuntamente para proporcionar una experiencia de comando enriquecida con un host de nuevas capacidades de la interfaz de usuario.

## <a name="the-windows-ribbon-command-system"></a>Sistema de comandos de la cinta de Windows

En el marco de la cinta de opciones, los comandos y los controles son entidades independientes. Un comando es una estructura abstracta, sin restricciones de presentación, que representa una tarea o clase de funcionalidad específica. Por otro lado, un control es un objeto concreto que expone la funcionalidad del comando a través de la interfaz de usuario de la cinta de opciones.

Esta distinción proporciona la capacidad de definir comandos que están libres de los detalles de la interfaz de usuario y que pueden ejecutarse en el intento de una acción sin necesidad de administrar cómo se invocó la acción.

### <a name="controls"></a>Controles

Los controles son los objetos de interfaz de usuario necesarios para la presentación de comandos. Se representan y administran en tiempo de ejecución mediante el marco de trabajo en función de la interacción del usuario y un conjunto de propiedades y comportamientos inherentes.

Conocido como diseño adaptable, la flexibilidad administrada por el marco de la interfaz de usuario es una de las grandes ventajas de la cinta de opciones. Los controles de la cinta de opciones se pueden volver a configurar automáticamente a través de plantillas de diseño dependientes del marco de trabajo o definidas por el desarrollador que pueden responder a diversos requisitos de tiempo de ejecución, todo ello sin escribir una sola línea de código de presentación. Para obtener más información, vea [personalizar una cinta de opciones a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md).

Además de las ventajas del diseño adaptable, una serie de controles de cinta complejos proporcionan soluciones independientes para espacios de la interfaz de usuario específicos. Al ofrecer un modelo de interacción sofisticado, los controles de la cinta de opciones, como FontControl o ColorPicker, proporcionan la capacidad de manipular datos en términos más abstractos a través de bolsas de propiedades de atributos de fuente o de color reales en lugar de varios subcontrols, enumeraciones y valores de índice de los controles estándar de Windows.

### <a name="commands"></a>Comandos:

Con un acoplamiento flexible a los controles de la cinta de opciones que exponen su funcionalidad, las implementaciones de comandos son el dominio de la aplicación host y tienen la forma de agentes de escucha de eventos, controladores de comandos y diversas propiedades de comando.

Los comandos se declaran en el marcado de la cinta de opciones con un identificador único o se les asigna un identificador generado por el compilador de marcado en la compilación. Los comandos se asocian a los controles a través de un nombre de comando, pero, a diferencia de los controles, su funcionalidad real se define en el código donde se enlazan a controladores de comandos concretos mediante el identificador de comando.

> [!Note]  
> En la compilación, este identificador se almacena en un archivo de encabezado de definición de identificador que expone comandos a sus controladores de comandos correspondientes en la aplicación host de la cinta de opciones.

 

Cada comando tiene un tipo de comando subyacente con elementos en la enumeración [**\_ COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) de la interfaz de usuario.

### <a name="the-command-experience-in-action"></a>La experiencia del comando en acción

Las capacidades de este modelo de comandos se muestran en la barra de herramientas de acceso rápido de la cinta de opciones (QAT). QAT proporciona a los usuarios finales una manera fácil de definir sus propios métodos abreviados para prácticamente cualquier control en la interfaz de usuario de la cinta de opciones. Un acceso directo se agrega dinámicamente al QAT en tiempo de ejecución cuando el usuario hace clic con el botón secundario en un control de la cinta de opciones y selecciona **Agregar a barra de herramientas de acceso rápido** en el menú contextual.

En la imagen siguiente se muestran los comandos **pegar** y **pegar desde** , representados por un control [**splitButton**](windowsribbon-element-splitbutton.md) , en la cinta de opciones de Windows 7 Paint.

![imagen de pegar splitButton en la cinta de opciones de Microsoft Paint.](images/overviews/paint-paste-splitbutton-ribbon.png)

En la imagen siguiente se muestran los mismos comandos **pegar** y **pegar desde** , que todavía se representan mediante un control [**splitButton**](windowsribbon-element-splitbutton.md) , en la cinta de opciones Qat de Windows 7 Paint.

![imagen de pegar splitButton en Microsoft Paint Qat.](images/overviews/paint-paste-splitbutton-qat.png)

Cuando un control está hospedado por el QAT, la nueva instancia del control mantiene toda la funcionalidad del control original sin necesidad de que los agentes de escucha de eventos y controladores de comandos adicionales lo admitan. Ambos controles se enlazan al mismo controlador de comandos de la cinta de opciones a través de un identificador de comando compartido. De esta manera, el marco de trabajo trata ambos controles como uno, independientemente de lo que se invoca.

> [!Note]  
> Se tienen en cuenta los mismos beneficios cuando los comandos se incorporan en un [**ContextPopup**](windowsribbon-element-contextpopup.md) en tiempo de diseño. En este caso, se pueden usar los controladores de comandos de pegado si el control [**splitButton**](windowsribbon-element-splitbutton.md) aparece en la cinta de opciones, Qat o **ContextPopup**.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción al marco de cinta de Windows](windowsribbon-introduction.md)
</dt> <dt>

[Crear una aplicación de cinta](windowsribbon-stepbystep.md)
</dt> <dt>

[Declarar comandos y controles con el marcado de la cinta de opciones](windowsribbon-schema.md)
</dt> </dl>

 

 