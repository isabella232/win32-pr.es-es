---
description: Puede usar el Administrador de recursos de compensación de COM+ (CRM) para integrar de forma fácil y rápida los recursos de la aplicación con las transacciones de Microsoft Coordinador de transacciones distribuidas (DTC).
ms.assetid: 8d1d034f-8a09-40ae-842a-5251135bd3c8
title: Conceptos de Administrador de recursos de compensación de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14206a54ffcb4f7e06ddf7362736a722393b0791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000573"
---
# <a name="com-compensating-resource-manager-concepts"></a>Conceptos de Administrador de recursos de compensación de COM+

Puede usar el Administrador de recursos de compensación de COM+ (CRM) para integrar de forma fácil y rápida los recursos de la aplicación con las transacciones de Microsoft Coordinador de transacciones distribuidas (DTC). Los recursos de la aplicación pueden votar sobre el resultado de una transacción y recibir la notificación final de su resultado. Se genera un registro duradero para que los recursos de la aplicación puedan escribir registros que sobreviven a los errores y el CRM recupera este archivo de registro cuando se reinicia la aplicación.

Un CRM consta de los dos componentes siguientes:

-   Trabajador de CRM. Este componente realiza el trabajo principal del CRM específico e implementa una interfaz específica de la tarea que necesita realizar. La infraestructura de CRM proporciona una interfaz al trabajador de CRM a través de la cual el trabajador de CRM puede escribir registros en un archivo de registro duradero en el disco. El trabajador de CRM debe escribir registros en el registro y hacerlos duraderos antes de que realice su trabajo para que, si se produce un bloqueo, la recuperación se realice correctamente. El trabajador de CRM siempre requiere una transacción.
-   Compensator de CRM. La infraestructura de CRM crea este componente al finalizar la transacción. Implementa una interfaz definida por la que la infraestructura de CRM puede pasar en las notificaciones de finalización de la transacción y las entradas de registro escritas previamente por el trabajador de CRM.

Una CRM de COM+ proporciona atomicidad con notificaciones transaccionales y durabilidad con el registro de CRM, pero no proporciona aislamiento de recursos. En un entorno multiproceso, es responsabilidad del desarrollador de CRM asegurarse de que el acceso a los recursos, ya sea por parte de varios trabajos de CRM o de aplicaciones externas, se serializa mientras se encuentra en una transacción.

Una vez que la transacción ha superado la fase de preparación, el compensador de CRM y los trabajos de CRM pueden ejecutarse simultáneamente. Es posible que el componente de trabajo de CRM de una nueva transacción se active mientras el compensador de CRM de una transacción anterior siga procesando la transacción anterior.

Durante los errores antes de la recuperación de la aplicación de servidor CRM, una transacción interrumpida debe considerarse activa y no completa. No es posible que los procesos externos tengan acceso a los recursos que esta transacción determinada estaba cambiando antes de la recuperación del proceso del servidor CRM.

CRM define tres tipos de interfaz para las funciones básicas de CRM:

-   [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) se implementa en el funcionario de CRM y el trabajador de CRM lo usa para escribir entradas de registro en el registro. También lo puede usar el compensador de CRM.
-   [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) y [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) se implementan en el compensador de CRM. Estas interfaces se utilizan para proporcionar notificaciones de resultados de transacciones y sus entradas de registro asociadas al compensador de CRM. Normalmente, el compensador de CRM implementaría solo una de estas interfaces, dependiendo de si requería entradas de registro estructuradas o no estructuradas. Las *entradas de registro estructuradas* son las que se compilan como una colección de variantes y suelen usarse en Microsoft Visual Basic. Las *entradas de registro no estructuradas* son simplemente un búfer de bytes y suelen utilizarse en Microsoft Visual C++. Un compensador de CRM puede implementar ambas interfaces Compensator; sin embargo, solo se usa una a una para proporcionar entradas de registro.
-   Las interfaces de supervisión de CRM de COM+ se utilizan para supervisar CRMs en una aplicación de servidor determinada. Para obtener información detallada acerca de las interfaces de supervisión, consulte [interfaces de supervisión de CRM de com+](com--crm-monitoring-interfaces.md).

En los siguientes temas de esta sección se proporcionan más detalles sobre el servicio COM+ CRM:

-   [Consideraciones de seguridad de COM+ CRM](com--crm-security-considerations.md)
-   [Proceso operativo COM+ CRM](com--crm-operating-process.md)
-   [Inicio y recuperación de COM+ CRM](com--crm-startup-and-recovery.md)
-   [Usar el CRM de COM+ en un entorno de clústeres](using-the-com--crm-in-a-cluster-environment.md)
-   [Control de errores en COM+ CRM](error-handling-in-the-com--crm.md)
-   [Configuración del registro de COM+ CRM](com--crm-registry-settings.md)
-   [Solución de problemas de COM+ CRM](troubleshooting-the-com--crm.md)
-   [Sugerencias de diseño para desarrollar un CRM de COM+](design-suggestions-for-developing-a-com--crm.md)
-   [Interfaces de supervisión de CRM de COM+](com--crm-monitoring-interfaces.md)
-   [Interfaces de CRM para COM+](com--crm-interfaces.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas Administrador de recursos de compensación de COM+](com--compensating-resource-manager-tasks.md)
</dt> </dl>

 

 



