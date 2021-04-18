---
description: Inicio y recuperación de COM+ CRM
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Inicio y recuperación de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714889"
---
# <a name="com-crm-startup-and-recovery"></a>Inicio y recuperación de COM+ CRM

Si una aplicación de servidor tiene activada la casilla **Habilitar administradores de compensación de recursos** (mediante la herramienta administrativa Servicios de componentes, en la pestaña **Opciones avanzadas** de la página de propiedades de la aplicación com+), la primera vez que se inicia crea un archivo de registro de CRM para que lo usen todos los CRMs en el proceso de la aplicación de servidor. (Para obtener instrucciones detalladas acerca de cómo configurar el CRM, consulte [configuración de componentes com+ CRM](configuring-com--crm-components.md)).

El nombre del archivo de registro de CRM creado para la aplicación de servidor se basa en el AppId (GUID) de la aplicación de servidor y el archivo de registro de CRM se coloca en el mismo directorio que el archivo de registro de DTC (normalmente el directorio% SystemRoot% \\ WinNT \\ system32 \\ DtcLog). Los archivos de registro de CRM tienen la extensión. crmlog.

> [!Note]  
> Puede que sea necesario cambiar la ubicación predeterminada de un archivo de registro de CRM por motivos de rendimiento (para que el archivo de registro de DTC esté en un disco diferente al del archivo de registro de CRM) o quizás debido al uso de CRM en un entorno de clúster. La ubicación de los archivos de registro de CRM se puede cambiar mediante el SDK de administración de COM+. El nombre de la propiedad es CRMLogFile y existe en el objeto de colección de [**aplicaciones**](applications.md) .

 

Cuando una aplicación de servidor (habilitada para CRM) se inicia y detecta que ya existe un archivo de registro de CRM para esa aplicación de servidor, realiza la recuperación en ese archivo de registro de CRM. La *recuperación* es el proceso de completar cualquier transacción interrumpida por un error e implica que la infraestructura de CRM Lea el archivo de registro de CRM para las transacciones que no se completaron completamente. Si encuentra alguno, se pone en contacto con el DTC para determinar el resultado de la transacción. A continuación, crea el compensador de CRM y pasa las notificaciones commit o Abort según sea necesario, junto con las entradas de registro asociadas.

El compensador de CRM no recibe las notificaciones de preparación durante la recuperación. El compensador de CRM tiene una marca para distinguir si se llama durante el funcionamiento normal o durante la recuperación.

Normalmente, la recuperación solo encontrará transacciones incompletas si la aplicación de servidor se ha cerrado de forma anómala, debido a un bloqueo del proceso de la aplicación de servidor o a un bloqueo del equipo. Si se permite que la aplicación de servidor se apague normalmente, debido al tiempo de espera de inactividad o al cierre manual a través de la herramienta administrativa Servicios de componentes, el archivo de registro estará limpio.

El inicio de una aplicación de servidor CRM para la recuperación no se inicia automáticamente. Se debe realizar alguna acción externa para iniciar la aplicación de servidor CRM donde se requiere recuperación. Normalmente, esto sería crear un componente en esa aplicación de servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de Administrador de recursos de compensación de COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Proceso operativo COM+ CRM](com--crm-operating-process.md)
</dt> </dl>

 

 



