---
description: La responsabilidad principal de cualquier elemento del panel de control es mostrar una ventana que permita al usuario ver y manipular la configuración.
title: Directrices de la experiencia de usuario
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997917"
---
# <a name="user-experience-guidelines"></a>Directrices de la experiencia de usuario

La responsabilidad principal de cualquier elemento del panel de control es mostrar una ventana que permita al usuario ver y manipular la configuración. Vea las [directrices de experiencia del usuario (UX)](../uxguide/winenv-ctrl-panels.md) de los paneles de control para el comportamiento y el diseño de los elementos del panel de control. Las instrucciones descritas en ese tema muestran un método de flujo de tareas para organizar un elemento del panel de control. Esto coloca la configuración más importante en una página principal. Los valores de configuración usados con menos frecuencia se colocan en páginas de radio o se accede a ellos desde los vínculos de un panel lateral.

El panel de control incluye muchos elementos que siguen estas instrucciones, como el centro de accesibilidad y el centro de redes y recursos compartidos. Otros elementos del panel de control usan el formato de hoja de propiedades de cuadro de diálogo con pestañas como en versiones anteriores de Windows. Entre los ejemplos se incluyen el elemento de mouse y las opciones de Internet. El uso del formato de hoja de propiedades debe ser discontinuo. Si crea nuevos elementos del panel de control, debe seguir las instrucciones del flujo de tareas.

En el pasado, los elementos del panel de control se empaquetaban como archivos. cpl. Eso ya no es necesario. Los nuevos elementos del panel de control deben implementarse como un archivo. exe independiente o como una opción de marca de línea de comandos para el archivo ejecutable principal de la aplicación.

> [!Note]  
> En los sistemas de 64 bits, los elementos del panel de control de 32 bits se muestran en el panel de control cuando se selecciona la opción de **carpeta ver elementos del panel de control de 32 bits** . Los elementos de 32 bits deben estar ubicados en la carpeta% SystemRoot% \\ SysWOW64 que se va a mostrar. No requieren ningún registro adicional.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos del panel de control](control-panel-applications.md)
</dt> <dt>

[Registrar elementos del panel de control](registering-control-panel-items.md)
</dt> <dt>

[Usar CPLApplet](using-cplapplet.md)
</dt> <dt>

[Procesamiento de mensajes del panel de control](message-processing.md)
</dt> <dt>

[Ejecutar elementos del panel de control](executing-control-panel-items.md)
</dt> <dt>

[Extender elementos del panel de control del sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Asignar categorías del panel de control](assigning-control-panel-categories.md)
</dt> <dt>

[Crear vínculos de tarea que se pueden buscar para un elemento del panel de control](creating-searchable-task-links.md)
</dt> <dt>

[Acceder al panel de control en modo seguro](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



