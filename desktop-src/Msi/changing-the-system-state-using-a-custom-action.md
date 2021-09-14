---
description: Las acciones personalizadas diseñadas para cambiar el estado del sistema deben ser acciones personalizadas de ejecución aplazada.
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Cambiar el estado del sistema mediante una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace5dc323bcf809c76eeb55cfa859a8621312df7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158930"
---
# <a name="changing-the-system-state-using-a-custom-action"></a>Cambiar el estado del sistema mediante una acción personalizada

Las acciones personalizadas diseñadas para cambiar el estado del sistema deben ser acciones personalizadas de ejecución aplazada. Las acciones personalizadas que establecen propiedades, estados de características, estados de componentes o directorios de destino, u programan operaciones del sistema mediante la inserción de filas en tablas de secuencia pueden usar la ejecución inmediata de forma segura. Sin embargo, las acciones personalizadas que cambian el sistema directamente o llaman a otro servicio del sistema deben aplazarse hasta el momento en que se ejecuta el script de instalación. Para obtener más información, vea [Acciones personalizadas de ejecución aplazada.](deferred-execution-custom-actions.md)

No debe intentar usar una acción personalizada de ejecución inmediata para cambiar el estado del sistema, ya que todas las acciones personalizadas que cambien el estado deben tener una acción personalizada de reversión correspondiente para deshacer el cambio de estado del sistema en una reversión de la instalación. Todas las acciones personalizadas de reversión también se aplazan y deben preceder a la acción que deshace. Para obtener más información, vea [Reversión de acciones personalizadas.](rollback-custom-actions.md)

 

 



