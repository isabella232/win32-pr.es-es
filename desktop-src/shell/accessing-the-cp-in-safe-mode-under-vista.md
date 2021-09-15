---
description: De forma predeterminada, a Windows vista Panel de control no se muestran los elementos cuando Windows se ejecuta en modo seguro.
title: Acceso al Panel de control en Caja fuerte modo de acceso
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468305"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a>Acceso al Panel de control en Caja fuerte modo de acceso

De forma predeterminada, a Windows vista Panel de control no se muestran los elementos cuando Windows se ejecuta en modo seguro. Para permitir que un nuevo Panel de control elemento se vea en modo seguro, se pueden establecer los valores del Registro adecuados para el tipo de elemento. Los valores se interpretan de la siguiente manera:



| Value | Significado                                                            |
|-------|--------------------------------------------------------------------|
| 1     | El elemento solo debe aparecer en modo seguro mínimo.                  |
| 2     | El elemento debe aparecer en modo seguro solo si las redes están habilitadas. |
| 3     | El elemento siempre debe aparecer en cualquier forma de modo seguro.            |



 

En este ejemplo se muestran las entradas necesarias para un elemento implementado como un .cpl o .dll archivo. Especifica que el elemento debe aparecer en modo seguro con redes.

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

En este ejemplo se muestran las entradas necesarias para un elemento implementado como un .exe archivo. Especifica que el elemento debe aparecer en cualquier forma de modo seguro.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Panel de control elementos](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
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
</dt> </dl>

 

 



