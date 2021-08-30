---
title: ActiveX Arquitectura de controles
description: ActiveX controla la tecnología se basa en una base de muchos objetos e interfaces de nivel inferior en OLE. Las interfaces exactas disponibles en un control varían con sus funcionalidades. En esta sección se observan más de cerca las funcionalidades que puede proporcionar un control.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cde527bcfc5e683d35da8f267a6cb8b22a85cb6d84e77b905ef30325deb1d850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071245"
---
# <a name="activex-controls-architecture"></a>ActiveX Arquitectura de controles

ActiveX controla la tecnología se basa en una base de muchos objetos e interfaces de nivel inferior en OLE. Las interfaces exactas disponibles en un control varían con sus funcionalidades. En esta sección se observan más de cerca las funcionalidades que puede proporcionar un control.

ActiveX se usan para proporcionar los bloques de creación para crear interfaces de usuario en aplicaciones. Por ejemplo, un botón que inicia alguna acción en la aplicación contenedora cuando se hace clic en él es un control simple. Los siguientes aspectos están implicados en el suministro de estos bloques de creación de la interfaz de usuario:

-   Un control se puede incrustar dentro de su cliente de contenedor para admitir alguna actividad de interfaz de usuario dentro del cliente. Por lo tanto, un control debe proporcionar una representación visual de sí mismo cuando se incrusta dentro del contenedor y debe proporcionar una manera de guardar su estado, por ejemplo, sus valores de propiedad y su posición dentro de su contenedor. El cliente debe admitir ser un contenedor con objetos incrustados en él.
-   Al activar el control mediante un teclado o un mouse, el usuario final inicia alguna acción en la aplicación cliente. Por lo tanto, un control debe responder a la actividad de teclado y debe ser capaz de comunicarse con su cliente para que pueda notificar a su contenedor sus actividades y desencadenar eventos en el cliente.
-   El cliente también suele proporcionar un lenguaje de programación a través del cual el usuario final puede iniciar acciones proporcionadas por las propiedades y los métodos del control. Por lo tanto, un control debe admitir automatización y algún conjunto de características en tiempo de diseño frente a características en tiempo de ejecución.

Como resultado de su rol al proporcionar bloques de creación de la interfaz de usuario, un control normalmente admite características en las áreas siguientes mediante tecnologías OLE como se indica:

<dl> <dt>

<span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Propiedades y métodos
</dt> <dd>

Al igual que cualquier objeto OLE, un control puede proporcionar gran parte de su funcionalidad a través de un conjunto de interfaces entrantes con propiedades y métodos. El contenedor puede proporcionar propiedades ambientales adicionales y puede admitir la extensión de las propiedades del control a través de la agregación. Estas características se resalten en la automatización OLE, las páginas de propiedades, los objetos conectables y ActiveX de control.

</dd> <dt>

<span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Eventos
</dt> <dd>

Además de proporcionar propiedades y métodos, un control ActiveX también puede proporcionar interfaces salientes para notificar eventos a su cliente. El cliente debe admitir el control de estos eventos. Estas características usan automatización OLE y objetos conectables.

</dd> <dt>

<span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Representación visual
</dt> <dd>

Un control puede admitir el posicionamiento y mostrarse dentro de su contenedor. El contenedor coloca el control y determina su tamaño. Estas características usan tecnología de documentos compuestos, incluida la tecnología de arrastrar y colocar ole.

</dd> <dt>

<span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Control de teclado
</dt> <dd>

Un control puede responder a los aceleradores de teclado para que el usuario final pueda iniciar acciones realizadas por el control. El contenedor administra la actividad de teclado para todos sus controles incrustados. Estas características usan tecnologías de control y documentos compuestos.

</dd> <dt>

<span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistencia
</dt> <dd>

Un control puede guardar su estado. El cliente administra la persistencia de sus controles incrustados. Estas características usan tecnologías de persistencia de objetos y almacenamiento estructurado.

</dd> <dt>

<span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registro y licencias
</dt> <dd>

Normalmente, un control admite el registro automático y crea un conjunto de entradas del Registro cuando se crea una instancia de él. También se puede obtener una licencia de un control para ayudar a evitar el uso no autorizado.

</dd> </dl>

La mayoría de estas características implican tanto el control como su contenedor de cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 




