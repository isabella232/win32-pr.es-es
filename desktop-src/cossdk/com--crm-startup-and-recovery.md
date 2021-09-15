---
description: Inicio y recuperación de COM+ CRM
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Inicio y recuperación de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465565"
---
# <a name="com-crm-startup-and-recovery"></a>Inicio y recuperación de COM+ CRM

Si una aplicación  de servidor tiene activada la casilla Habilitar administradores  de recursos de compensación (mediante la herramienta administrativa Servicios de componentes, en la pestaña Avanzadas de la página de propiedades de la aplicación COM+), la primera vez que se inicia, crea un archivo de registro crm que usarán todas las CRM de ese proceso de aplicación de servidor. (Para obtener instrucciones detalladas sobre cómo configurar CRM, vea [Configuración de componentes de CRM de COM+).](configuring-com--crm-components.md)

El nombre del archivo de registro de CRM creado para la aplicación de servidor se basa en el AppId (un GUID) de la aplicación de servidor y el archivo de registro de CRM se coloca en el mismo directorio que el archivo de registro DTC (normalmente el directorio %SystemRoot% \\ winnt \\ system32 \\ DtcLog). Los archivos de registro de CRM tienen la extensión .crmlog.

> [!Note]  
> Puede que sea necesario cambiar la ubicación predeterminada de un archivo de registro de CRM debido a motivos de rendimiento (para tener el archivo de registro de DTC en un disco diferente al archivo de registro de CRM) o quizás debido al uso de CRM en un entorno de clúster. La ubicación de los archivos de registro de CRM se puede cambiar mediante el SDK de administración de COM+. El nombre de la propiedad es CRMLogFile y existe en el [**objeto de colección Applications.**](applications.md)

 

Cuando se inicia una aplicación de servidor (que está habilitada para CRM) y descubre que ya existe un archivo de registro crm para esa aplicación de servidor, realiza la recuperación en ese archivo de registro de CRM. *La* recuperación es el proceso de completar las transacciones interrumpidas por un error e implica que la infraestructura de CRM lea el archivo de registro de CRM para las transacciones que no se completaron por completo. Si encuentra alguno, se pone en contacto con el DTC para determinar el resultado de la transacción. A continuación, crea el compensador crm y pasa las notificaciones de confirmación o anulación según sea necesario, junto con las entradas de registro asociadas.

El compensador de CRM no recibe las notificaciones de preparación durante la recuperación. Crm Compensator tiene una marca para distinguir si se llama durante el funcionamiento normal o durante la recuperación.

Normalmente, la recuperación encontrará transacciones no completas solo si la aplicación de servidor se ha apagado de forma anómala, debido a un bloqueo del proceso de aplicación de servidor o a un bloqueo del equipo. Si se permite que la aplicación de servidor se apague con normalidad, ya sea debido al tiempo de espera de inactividad o al apagado manual a través de la herramienta administrativa Servicios de componentes, el archivo de registro estará limpio.

El inicio de una aplicación de servidor CRM para la recuperación no se inicia automáticamente. Se debe realizar alguna acción externa para iniciar la aplicación de servidor CRM en la que se requiere recuperación. Normalmente, esto sería crear un componente en esa aplicación de servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Proceso operativo de COM+ CRM](com--crm-operating-process.md)
</dt> </dl>

 

 



