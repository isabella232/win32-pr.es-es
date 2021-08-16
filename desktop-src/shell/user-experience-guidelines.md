---
description: La responsabilidad principal de cualquier elemento Panel de control es mostrar una ventana que permita al usuario ver y manipular la configuración.
title: Directrices de la experiencia de usuario
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 15ef54d44a466f3c766075eae771ccac9d74e20c0622d6092530f1015a538425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857084"
---
# <a name="user-experience-guidelines"></a>Directrices de la experiencia de usuario

La responsabilidad principal de cualquier elemento Panel de control es mostrar una ventana que permita al usuario ver y manipular la configuración. Consulte las directrices de la experiencia del usuario [(UX)](../uxguide/winenv-ctrl-panels.md) de los paneles de control para ver el comportamiento y el diseño de Panel de control elementos. Las directrices que se deban tratar en ese tema muestran un método de flujo de tareas para organizar Panel de control elemento. Esto coloca la configuración más importante en una página principal. Las configuraciones usadas con menos frecuencia se colocan en páginas de radio o se accede a ellos desde vínculos en un panel lateral.

El Panel de control incluye muchos elementos que siguen estas directrices, como Centro de accesibilidad y Centro de redes y recursos compartidos. Otros Panel de control usan el formato de hoja de propiedades de cuadro de diálogo con pestañas como en versiones anteriores de Windows. Algunos ejemplos son el elemento mouse y las opciones de Internet. Se debe interrumpir el uso del formato de hoja de propiedades. Si crea nuevos elementos Panel de control, debe seguir las instrucciones del flujo de tareas.

En el pasado, los Panel de control se empaquetaban como .cpl archivos. Ya no es necesario. Los Panel de control nuevos deben implementarse como un archivo .exe independiente o como una opción de marca de línea de comandos para el archivo ejecutable principal de la aplicación.

> [!Note]  
> En sistemas de 64 bits, los elementos Panel de control de 32 bits se muestran en el Panel de control cuando se selecciona la opción de carpeta Ver elementos de Panel de control de **32** bits. Los elementos de 32 bits deben encontrarse en la carpeta %SystemRoot% \\ SysWOW64 que se va a mostrar. No requieren ningún registro adicional.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Panel de control elementos](control-panel-applications.md)
</dt> <dt>

[Registro de Panel de control elementos](registering-control-panel-items.md)
</dt> <dt>

[Uso de CPLApplet](using-cplapplet.md)
</dt> <dt>

[Panel de control de mensajes](message-processing.md)
</dt> <dt>

[Ejecutar elementos Panel de control datos](executing-control-panel-items.md)
</dt> <dt>

[Extender elementos de Panel de control sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Asignación de Panel de control categorías](assigning-control-panel-categories.md)
</dt> <dt>

[Crear vínculos de tareas buscables para un elemento Panel de control búsqueda](creating-searchable-task-links.md)
</dt> <dt>

[Acceso al Panel de control en modo Caja fuerte usuario](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



