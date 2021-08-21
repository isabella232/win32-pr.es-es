---
description: Puede usar com+ Compensating Resource Manager (CRM) para integrar fácilmente y rápidamente los recursos de la aplicación con Microsoft DTC (Coordinador de transacciones distribuidas) transacciones de Microsoft DTC (Coordinador de transacciones distribuidas) (DTC).
ms.assetid: 8d1d034f-8a09-40ae-842a-5251135bd3c8
title: Conceptos de compensación Resource Manager COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b546f10e9a99f827c512e6dd7662ead05476774f7ff8dc32c40fa123b0ffe272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047633"
---
# <a name="com-compensating-resource-manager-concepts"></a>Conceptos de compensación Resource Manager COM+

Puede usar com+ Compensating Resource Manager (CRM) para integrar fácilmente y rápidamente los recursos de la aplicación con Microsoft DTC (Coordinador de transacciones distribuidas) transacciones de Microsoft DTC (Coordinador de transacciones distribuidas) (DTC). Los recursos de la aplicación pueden votar el resultado de una transacción y pueden recibir la notificación final de su resultado. Se genera un registro duradero para que los recursos de la aplicación puedan escribir registros que sobreviven a errores, y CRM recupera este archivo de registro cuando se reinicia la aplicación.

Un CRM consta de los dos componentes siguientes:

-   CRM Worker. Este componente realiza el trabajo principal del CRM específico e implementa una interfaz específica de la tarea que debe realizar. La infraestructura de CRM proporciona una interfaz al trabajador de CRM a través de la cual el trabajador de CRM puede escribir registros en un archivo de registro duradero en disco. El trabajo de CRM debe escribir registros en el registro y hacerlos duraderos antes de realizar su trabajo para que, si se produce un bloqueo, la recuperación se pueda realizar correctamente. El trabajo de CRM siempre requiere una transacción.
-   CRM Compensator. La infraestructura de CRM crea este componente al finalizar la transacción. Implementa una interfaz definida por la que la infraestructura de CRM puede pasar notificaciones de finalización de transacciones y las entradas de registro escritas previamente por el trabajador de CRM.

Un CRM de COM+ proporciona atomicidad con notificaciones transaccionales y durabilidad con el registro de CRM, pero no proporciona aislamiento de recursos. En un entorno multiproceso, es responsabilidad del desarrollador de CRM asegurarse de que el acceso a los recursos, ya sea mediante varios trabajadores de CRM o aplicaciones externas, se serializa mientras se encuentra en una transacción.

Una vez que la transacción ha superado la fase de preparación, crm compensator y crm workers se pueden ejecutar simultáneamente. Es posible que el componente de trabajo de CRM de una nueva transacción se active mientras el compensador crm de una transacción anterior sigue procesando la transacción anterior.

Durante los errores anteriores a la recuperación de la aplicación de servidor CRM, una transacción interrumpida debe considerarse activa y no completa. No debería ser posible que los procesos externos accedan a los recursos que cambiaba esta transacción determinada antes de la recuperación del proceso del servidor CRM.

CRM define tres tipos de interfaz para las funciones básicas de CRM:

-   [**ICrmLogControl se**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) implementa en el empleado de CRM y lo usa el trabajador de CRM para escribir registros en el registro. También lo puede usar el compensador de CRM.
-   [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) e [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) se implementan en CRM Compensator. Estas interfaces se usan para entregar notificaciones de resultados de transacciones y sus registros asociados al compensador crm. Normalmente, crm Compensator implementaría solo una de estas interfaces, dependiendo de si requería registros estructurados o no estructurados. *Los registros estructurados* son aquellos que se han creado como una colección de variantes y que suelen ser usados por Microsoft Visual Basic. *Las entradas de registro no estructuradas* son solo un búfer de bytes y normalmente son para su uso por Microsoft Visual C++. Un compensador crm puede implementar ambas interfaces de compensador; sin embargo, solo se usa de uno en uno para entregar las entradas de registro.
-   Las interfaces de supervisión de COM+ CRM se usan para supervisar las CRM dentro de una aplicación de servidor determinada. Para obtener información detallada sobre las interfaces de supervisión, vea Interfaces de supervisión de [CRM de COM+](com--crm-monitoring-interfaces.md).

Los temas siguientes de esta sección proporcionan más detalles sobre el servicio CRM de COM+:

-   [Consideraciones de seguridad de CRM de COM+](com--crm-security-considerations.md)
-   [Proceso operativo de COM+ CRM](com--crm-operating-process.md)
-   [Inicio y recuperación de COM+ CRM](com--crm-startup-and-recovery.md)
-   [Uso de COM+ CRM en un entorno de clúster](using-the-com--crm-in-a-cluster-environment.md)
-   [Control de errores en COM+ CRM](error-handling-in-the-com--crm.md)
-   [Registro de COM+ CRM Configuración](com--crm-registry-settings.md)
-   [Solución de problemas de COM+ CRM](troubleshooting-the-com--crm.md)
-   [Sugerencias de diseño para desarrollar un CRM de COM+](design-suggestions-for-developing-a-com--crm.md)
-   [Interfaces de supervisión de CRM de COM+](com--crm-monitoring-interfaces.md)
-   [COM+ CRM Interfaces](com--crm-interfaces.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[COM+ Compensating Resource Manager Tasks](com--compensating-resource-manager-tasks.md)
</dt> </dl>

 

 



