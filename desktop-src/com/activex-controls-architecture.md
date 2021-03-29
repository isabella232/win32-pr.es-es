---
title: Arquitectura de controles ActiveX
description: La tecnología de controles ActiveX se basa en una base de muchos objetos de nivel inferior e interfaces en OLE. Las interfaces exactas disponibles en un control varían con sus capacidades. En esta sección se examina de cerca las capacidades que puede proporcionar un control.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775090"
---
# <a name="activex-controls-architecture"></a>Arquitectura de controles ActiveX

La tecnología de controles ActiveX se basa en una base de muchos objetos de nivel inferior e interfaces en OLE. Las interfaces exactas disponibles en un control varían con sus capacidades. En esta sección se examina de cerca las capacidades que puede proporcionar un control.

Los controles ActiveX se utilizan para proporcionar los bloques de creación para crear interfaces de usuario en las aplicaciones. Por ejemplo, un botón que inicia alguna acción en la aplicación contenedora cuando se hace clic en él es un control simple. Los siguientes aspectos están implicados en la prestación de estos bloques de creación de la interfaz de usuario:

-   Un control se puede incrustar dentro de su cliente de contenedor para admitir algunas actividades de interfaz de usuario en el cliente. Por lo tanto, un control debe proporcionar una representación visual de sí mismo cuando está incrustada en el contenedor y debe proporcionar una manera de guardar su estado, por ejemplo, sus valores de propiedad y su posición dentro de su contenedor. El cliente debe admitir ser un contenedor con objetos incrustados en él.
-   Al activar el control con un teclado o un mouse, el usuario final inicia alguna acción en la aplicación cliente. Por lo tanto, un control debe responder a la actividad del teclado y debe poder comunicarse con su cliente para que pueda notificar a su contenedor sus actividades y desencadenar eventos en el cliente.
-   El cliente también proporciona normalmente un lenguaje de programación a través del cual el usuario final puede iniciar acciones proporcionadas por las propiedades y los métodos del control. Por lo tanto, un control debe admitir también la automatización y un conjunto de características en tiempo de diseño frente al tiempo de ejecución.

Como consecuencia de su rol en la prestación de bloques de creación de la interfaz de usuario, un control suele admitir características en las siguientes áreas mediante tecnologías OLE, como se indica a continuación:

<dl> <dt>

<span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Propiedades y métodos
</dt> <dd>

Al igual que cualquier objeto OLE, un control puede proporcionar gran parte de su funcionalidad a través de un conjunto de interfaces entrantes con propiedades y métodos. El contenedor puede proporcionar propiedades ambiente adicionales y puede admitir la extensión de las propiedades del control a través de la agregación. Estas características se sitúan en la automatización OLE, las páginas de propiedades, los objetos conectables y las tecnologías de control ActiveX.

</dd> <dt>

<span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Ceso
</dt> <dd>

Además de proporcionar propiedades y métodos, un control ActiveX también puede proporcionar interfaces de salida para notificar a su cliente los eventos. El cliente debe admitir el control de estos eventos. Estas características utilizan la automatización OLE y los objetos conectables.

</dd> <dt>

<span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Representación visual
</dt> <dd>

Un control puede admitir la posición y la presentación en su contenedor. El contenedor coloca el control y determina su tamaño. Estas características utilizan tecnología de documentos compuestos, incluida la tecnología OLE de arrastrar y colocar.

</dd> <dt>

<span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Control de teclado
</dt> <dd>

Un control puede responder a los aceleradores de teclado para que el usuario final pueda iniciar acciones realizadas por el control. El contenedor administra la actividad del teclado de todos sus controles incrustados. Estas características utilizan tecnologías de control y de documentos compuestos.

</dd> <dt>

<span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistence
</dt> <dd>

Un control puede guardar su estado. El cliente administra la persistencia de sus controles incrustados. Estas características utilizan tecnologías de almacenamiento estructurado y persistencia de objetos.

</dd> <dt>

<span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registro y licencias
</dt> <dd>

Un control suele admitir el registro automático y crea un conjunto de entradas del registro cuando se crea una instancia. También se puede conceder una licencia a un control para ayudar a evitar el uso no autorizado.

</dd> </dl>

La mayoría de estas características implican el control y su contenedor de cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 




