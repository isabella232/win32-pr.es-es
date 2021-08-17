---
description: Inicio y recuperación de COM+ CRM
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Inicio y recuperación de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f65b8b1e32f2b587f7c288c6c5147ef30148360e89fc0a04ac952c8630076e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129197"
---
# <a name="com-crm-startup-and-recovery"></a>Inicio y recuperación de COM+ CRM

Si una aplicación  de servidor tiene activada la casilla Habilitar administradores  de recursos de compensación (mediante la herramienta administrativa Servicios de componentes, en la pestaña Opciones avanzadas de la página de propiedades de la aplicación COM+), la primera vez que se inicia, crea un archivo de registro crm para que lo usen todas las CRM de ese proceso de aplicación de servidor. (Para obtener instrucciones detalladas sobre cómo configurar CRM, vea [Configuración de componentes de COM+ CRM).](configuring-com--crm-components.md)

El nombre del archivo de registro de CRM creado para la aplicación de servidor se basa en appId (un GUID) de la aplicación de servidor y el archivo de registro de CRM se coloca en el mismo directorio que el archivo de registro DTC (normalmente el directorio %SystemRoot% \\ winnt \\ system32 \\ DtcLog). Los archivos de registro de CRM tienen la extensión .crmlog.

> [!Note]  
> Puede ser necesario cambiar la ubicación predeterminada de un archivo de registro de CRM debido a motivos de rendimiento (para tener el archivo de registro de DTC en un disco diferente al archivo de registro de CRM) o quizás debido al uso de CRM en un entorno de clúster. La ubicación de los archivos de registro de CRM se puede cambiar mediante el SDK de administración de COM+. El nombre de propiedad es CRMLogFile y existe en el [**objeto de colección Applications.**](applications.md)

 

Cuando se inicia una aplicación de servidor (que está habilitada para CRM) y encuentra que ya existe un archivo de registro de CRM para esa aplicación de servidor, realiza la recuperación en ese archivo de registro de CRM. *La* recuperación es el proceso de completar las transacciones interrumpidas por un error e implica que la infraestructura de CRM lea el archivo de registro de CRM para las transacciones que no se completaron por completo. Si encuentra alguna, se pone en contacto con el DTC para determinar el resultado de la transacción. A continuación, crea el compensador de CRM y pasa las notificaciones de confirmación o anulación según sea necesario, junto con las entradas de registro asociadas.

El compensador de CRM no recibe las notificaciones de preparación durante la recuperación. Crm Compensator tiene una marca para distinguir si se llama durante el funcionamiento normal o durante la recuperación.

Normalmente, la recuperación solo encontrará transacciones incompletas si la aplicación de servidor se ha apagado de forma anómala, debido a un bloqueo del proceso de aplicación de servidor o a un bloqueo del equipo. Si se permite que la aplicación de servidor se apague con normalidad, debido al tiempo de espera de inactividad o al apagado manual a través de la herramienta administrativa Servicios de componentes, el archivo de registro estará limpio.

El inicio de una aplicación de servidor CRM para la recuperación no se inicia automáticamente. Se debe realizar alguna acción externa para iniciar la aplicación de servidor CRM donde se requiere recuperación. Normalmente, esto sería crear un componente en esa aplicación de servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Proceso operativo de COM+ CRM](com--crm-operating-process.md)
</dt> </dl>

 

 



