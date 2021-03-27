---
description: Los elementos del panel de control deben estar registrados para que aparezcan en la ventana del panel de control.
title: Registrar elementos del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156689"
---
# <a name="registering-control-panel-items"></a>Registrar elementos del panel de control

Los elementos del panel de control deben estar registrados para que aparezcan en la ventana del panel de control. Si el elemento del panel de control se implementa como parte de un archivo. exe, se registra como un objeto de comando. El registro es distinto si el elemento se implementa como un archivo. dll que exporta la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) .

En estos temas se explican los requisitos específicos:

-   [Cómo registrar elementos del panel de control ejecutable](how-to-register-an-executable-control-panel-item-registration-.md)
-   [Cómo registrar elementos del panel de control DLL](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos del panel de control](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
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

[Acceder al panel de control en modo seguro en Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
