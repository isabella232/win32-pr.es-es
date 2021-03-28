---
description: De forma predeterminada, a partir de los elementos del panel de control de Windows Vista no se muestran cuando Windows se ejecuta en modo seguro.
title: Acceder al panel de control en modo seguro
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984367"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a>Acceder al panel de control en modo seguro

De forma predeterminada, a partir de los elementos del panel de control de Windows Vista no se muestran cuando Windows se ejecuta en modo seguro. Para que se pueda ver un nuevo elemento del panel de control en modo seguro, se pueden establecer los valores del registro adecuados para el tipo de elemento. Los valores se interpretan de la siguiente manera:



| Value | Significado                                                            |
|-------|--------------------------------------------------------------------|
| 1     | El elemento debe aparecer solo en el modo seguro mínimo.                  |
| 2     | El elemento debe aparecer en modo seguro solo si está habilitada la red. |
| 3     | El elemento siempre debe aparecer en cualquier forma de modo seguro.            |



 

En este ejemplo se muestran las entradas necesarias para un elemento implementado como un archivo. cpl o. dll. Especifica que el elemento debe aparecer en modo seguro con funciones de red.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

En este ejemplo se muestran las entradas necesarias para un elemento implementado como un archivo. exe. Especifica que el elemento debe aparecer en cualquier forma de modo seguro.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos del panel de control](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
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
</dt> </dl>

 

 



