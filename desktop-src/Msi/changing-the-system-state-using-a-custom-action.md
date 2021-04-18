---
description: Las acciones personalizadas diseñadas para cambiar el estado del sistema deben ser acciones personalizadas de ejecución aplazada.
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Cambiar el estado del sistema mediante una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace5dc323bcf809c76eeb55cfa859a8621312df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667003"
---
# <a name="changing-the-system-state-using-a-custom-action"></a>Cambiar el estado del sistema mediante una acción personalizada

Las acciones personalizadas diseñadas para cambiar el estado del sistema deben ser acciones personalizadas de ejecución aplazada. Las acciones personalizadas que establecen las propiedades, los Estados de las características, los Estados de los componentes o los directorios de destino, o la programación de las operaciones del sistema mediante la inserción de filas en tablas de secuencia pueden usar la ejecución inmediata de forma segura. Sin embargo, las acciones personalizadas que cambian el sistema directamente o llaman a otro servicio de sistema deben aplazarse hasta el momento en que se ejecuta el script de instalación. Para obtener más información, vea [acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md).

No debe intentar usar una acción personalizada de ejecución inmediata para cambiar el estado del sistema, porque todas las acciones personalizadas que cambian el estado deben tener una acción personalizada rollback correspondiente para deshacer el cambio de estado del sistema en una reversión de la instalación. Todas las acciones personalizadas de reversión también se difieren en acciones personalizadas y deben preceder a la acción que deshacer. Para obtener más información, consulte [reversión de acciones personalizadas](rollback-custom-actions.md).

 

 



