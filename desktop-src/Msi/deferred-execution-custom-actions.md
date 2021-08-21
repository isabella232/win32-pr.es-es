---
description: El propósito de una acción personalizada de ejecución aplazada es retrasar la ejecución de un cambio del sistema al momento en que se ejecuta el script de instalación.
ms.assetid: 79bf4d0b-624d-4652-8c4f-0ecd928a88e3
title: Acciones personalizadas de ejecución aplazada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cec06600fa2cdb447ace579ecf9d19be62e5f4824ecf2d34d77ed879a717d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379182"
---
# <a name="deferred-execution-custom-actions"></a>Acciones personalizadas de ejecución aplazada

El propósito de una acción personalizada de ejecución aplazada es retrasar la ejecución de un cambio del sistema al momento en que se ejecuta el script de instalación. Esto difiere de una acción personalizada normal, o una acción estándar, en la que el instalador ejecuta la acción inmediatamente después de encontrarla en una tabla de secuencia o en una llamada a [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). Una acción personalizada de ejecución aplazada permite a un autor del paquete especificar operaciones del sistema en un punto determinado dentro de la ejecución del script de instalación.

El instalador no ejecuta una acción personalizada de ejecución aplazada en el momento en que se procesa la secuencia de instalación. En su lugar, el instalador escribe la acción personalizada en el script de instalación. El único parámetro de modo que establece el instalador en este caso es MSIRUNMODE \_ SCHEDULED. Consulte [**MsiGetMode para**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) obtener una descripción de los parámetros del modo de ejecución.

Se debe programar una acción personalizada de ejecución diferida en la tabla de secuencia de ejecución dentro de la sección que realiza la generación de scripts. Las acciones personalizadas de ejecución aplazada deben ir después [de InstallInitialize](installinitialize-action.md) y deben ir antes [de InstallFinalize en](installfinalize-action.md) la secuencia de acciones.

Las acciones personalizadas que establecen propiedades, estados de características, estados de componentes o directorios de destino, o que programan operaciones del sistema mediante la inserción de filas en tablas de secuencias, pueden, en muchos casos, usar la ejecución inmediata de forma segura. Sin embargo, las acciones personalizadas que cambian el sistema directamente o llaman a otro servicio del sistema se deben aplazar hasta el momento en que se ejecuta el script de instalación. Vea [Acciones personalizadas sincrónicas](synchronous-and-asynchronous-custom-actions.md) y asincrónicas para obtener más información sobre posibles conflictos entre sus acciones personalizadas y el subproceso de instalación principal.

Dado que el script de instalación se puede ejecutar fuera de la sesión de instalación en la que se escribió, es posible que la sesión ya no exista durante la ejecución del script de instalación. Esto significa que el identificador de sesión original y el conjunto de datos de propiedad durante la secuencia de instalación no están disponibles para una acción personalizada de ejecución aplazada. Las acciones personalizadas diferidas que llaman a bibliotecas de vínculos dinámicos (DLL) pasan un [](obtaining-context-information-for-deferred-execution-custom-actions.md)identificador que solo se puede usar para obtener una cantidad muy limitada de información, como se describe en Obtención de información de contexto para acciones personalizadas de ejecución aplazada.

Tenga en cuenta que [](rollback-custom-actions.md) las acciones personalizadas diferidas, incluidas las acciones personalizadas de reversión y las acciones personalizadas de [confirmación,](commit-custom-actions.md)son los únicos tipos de acciones que se pueden ejecutar fuera del contexto de seguridad de los usuarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Opciones de ejecución de In-Script acción personalizada](custom-action-in-script-execution-options.md)
</dt> <dt>

[Referencia de acción personalizada](custom-action-reference.md)
</dt> </dl>

 

 



