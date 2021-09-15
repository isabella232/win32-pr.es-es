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
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574497"
---
# <a name="user-experience-guidelines"></a>Directrices de la experiencia de usuario

La responsabilidad principal de cualquier elemento Panel de control es mostrar una ventana que permita al usuario ver y manipular la configuración. Consulte las directrices de la experiencia del usuario [(UX)](../uxguide/winenv-ctrl-panels.md) de los paneles de control para ver el comportamiento y el diseño de Panel de control elementos. Las directrices que se deban tratar en ese tema muestran un método de flujo de tareas para organizar Panel de control elemento. Esto coloca la configuración más importante en una página principal. Las configuraciones usadas con menos frecuencia se colocan en páginas de radio o se accede a ellos desde vínculos en un panel lateral.

El Panel de control incluye muchos elementos que siguen estas directrices, como Centro de accesibilidad y Centro de redes y recursos compartidos. Otros Panel de control usan el formato de hoja de propiedades de cuadro de diálogo con pestañas como en versiones anteriores de Windows. Algunos ejemplos son el elemento mouse y las opciones de Internet. El uso del formato de hoja de propiedades debe descontinuar. Si crea nuevos elementos Panel de control, debe seguir las directrices del flujo de tareas.

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

[Ejecución de Panel de control elementos](executing-control-panel-items.md)
</dt> <dt>

[Extender elementos de Panel de control sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Asignación de Panel de control categorías](assigning-control-panel-categories.md)
</dt> <dt>

[Crear vínculos de tareas buscables para un elemento Panel de control búsqueda](creating-searchable-task-links.md)
</dt> <dt>

[Acceso al Panel de control en Caja fuerte modo](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



