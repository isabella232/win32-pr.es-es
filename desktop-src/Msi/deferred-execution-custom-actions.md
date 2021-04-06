---
description: El propósito de una acción personalizada de ejecución aplazada es retrasar la ejecución de un cambio del sistema en el momento en que se ejecuta el script de instalación.
ms.assetid: 79bf4d0b-624d-4652-8c4f-0ecd928a88e3
title: Acciones personalizadas de ejecución aplazada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09b91793f5d5bbc7be7099c92f8d8f212012d12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002277"
---
# <a name="deferred-execution-custom-actions"></a>Acciones personalizadas de ejecución aplazada

El propósito de una acción personalizada de ejecución aplazada es retrasar la ejecución de un cambio del sistema en el momento en que se ejecuta el script de instalación. Esto difiere de una acción personalizada normal o de una acción estándar, en la que el instalador ejecuta la acción inmediatamente después de encontrarla en una tabla de secuencia o en una llamada a [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). Una acción personalizada de ejecución aplazada permite que el autor del paquete especifique las operaciones del sistema en un punto determinado dentro de la ejecución del script de instalación.

El instalador no ejecuta una acción personalizada de ejecución aplazada en el momento en que se procesa la secuencia de instalación. En su lugar, el instalador escribe la acción personalizada en el script de instalación. El único parámetro de modo que establece el instalador en este caso es MSIRUNMODE \_ programado. Consulte [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) para obtener una descripción de los parámetros de modo de ejecución.

Una acción personalizada de ejecución aplazada debe programarse en la tabla ejecutar secuencia dentro de la sección que realiza la generación de scripts. Las acciones personalizadas de ejecución aplazada deben aparecer después de [InstallInitialize](installinitialize-action.md) y antes de [InstallFinalize](installfinalize-action.md) en la secuencia de acción.

Las acciones personalizadas que establecen propiedades, Estados de características, Estados de componentes o directorios de destino, o que programan las operaciones del sistema mediante la inserción de filas en tablas de secuencia, pueden en muchos casos usar la ejecución inmediata de forma segura. Sin embargo, las acciones personalizadas que cambian el sistema directamente o llaman a otro servicio del sistema deben aplazarse hasta el momento en que se ejecuta el script de instalación. Vea [acciones personalizadas sincrónicas y asincrónicas](synchronous-and-asynchronous-custom-actions.md) para obtener más información sobre posibles conflictos entre sus acciones personalizadas y el subproceso de instalación principal.

Dado que el script de instalación se puede ejecutar fuera de la sesión de instalación en la que se escribió, puede que la sesión ya no exista durante la ejecución del script de instalación. Esto significa que el identificador de sesión original y el conjunto de datos de propiedades durante la secuencia de instalación no están disponibles para una acción personalizada de ejecución aplazada. Las acciones personalizadas diferidas que llaman a las bibliotecas de vínculos dinámicos (dll) pasan un identificador que solo se puede usar para obtener una cantidad de información muy limitada, como se describe en [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md).

Tenga en cuenta que las acciones personalizadas diferidas, incluida la [reversión](rollback-custom-actions.md) de acciones personalizadas y la [confirmación de acciones personalizadas](commit-custom-actions.md), son los únicos tipos de acciones que se pueden ejecutar fuera del contexto de seguridad de los usuarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Opciones de ejecución de la acción personalizada In-Script](custom-action-in-script-execution-options.md)
</dt> <dt>

[Referencia de acción personalizada](custom-action-reference.md)
</dt> </dl>

 

 



