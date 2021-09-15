---
description: La infraestructura de CRM proporciona un conjunto de interfaces que se pueden usar para supervisar las CRM dentro de una aplicación de servidor determinada.
ms.assetid: b8f40c91-001b-4003-b377-57a918988100
title: Interfaces de supervisión de CRM de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c893040c46810c980c647cbacdc808200e8d5f5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465567"
---
# <a name="com-crm-monitoring-interfaces"></a>Interfaces de supervisión de CRM de COM+

La infraestructura de CRM proporciona un conjunto de interfaces que se pueden usar para supervisar las CRM dentro de una aplicación de servidor determinada. Para acceder a las interfaces de supervisión, un componente que se ejecuta dentro de la aplicación de servidor debe crear primero un empleado de CRM especializado denominado el agente de recuperación de CRM.

En el uso normal de LAS CRM, se espera que las transacciones sean de corta duración y, por tanto, los trabajadores de CRM y los compensadores de CRM existen durante un breve período de tiempo, normalmente solo unos segundos como máximo. Por lo tanto, las interfaces de supervisión están diseñadas para proporcionar una instantánea del estado de las CRM en ejecución en un momento dado. Si alguna de las CRM tiene problemas, las interfaces de supervisión se pueden usar para establecer cero en en el CRM problemático, para inspeccionar sus registros y anular su transacción si es necesario.

A continuación se encuentran las tres interfaces de supervisión de CRM y descripciones de cómo funcionan.



| Interfaz                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)<br/>                     | Mediante [**ICrmMonitor::GetClerks,**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-getclerks)se puede obtener una instantánea del conjunto actual de empleados de CRM activos dentro de la aplicación de servidor. A partir de esto, se puede encontrar y consultar un objeto de colección de vendedores de CRM determinado de interés, incluido el estado actual de su transacción y las entradas de registro escritas por CRM.<br/> Cuando la herramienta de supervisión ha determinado qué dependiente es de interés, llama a [**ICrmMonitor::HoldClerk**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-holdclerk) para obtener una [**interfaz ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) en ese determinado vendedor. En este momento, la herramienta de supervisión mantiene una referencia a ese vendedor y, si se completa la transacción, el vendedor se mantiene en memoria y no se libera hasta que se realiza la herramienta de supervisión.<br/>                                                                                                                                                                                                    |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)<br/>         | Con esta interfaz, se puede examinar el objeto de colección de vendedores para obtener información sobre el estado de la colección de vendedores en el momento en que se obtuvo. Esta información incluye el número de empleados, el ProgID del compensador crm usado por el vendedor, la descripción proporcionada en el momento en que se registró el compensador de CRM (mediante [**ICrmLogControl::RegisterCompensator),**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator)el identificador de unidad de trabajo de transacción y el identificador de actividad. Los empleados individuales también se identifican de forma única mediante un "CLSID de instancia de vendedor", que no es un CLSID COM en el sentido habitual del término, sino simplemente un GUID único que identifica a este empleado concreto para su duración.<br/>                                                                                                                                                                                                                                                                                                |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)<br/> | Esta interfaz se puede usar para consultar el estado actual de la transacción, para averiguar cuántas entradas de registro ha escrito este registrador de CRM y para obtener los datos de registro reales. Las entradas de registro se proporcionan desde la [**interfaz ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) en el mismo formato que se escribieron originalmente (mediante [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)). Además, **ICrmMonitorLogRecords** se puede implementar opcionalmente para convertir las entradas de registro al formato visualizable para que se puedan presentar mediante una herramienta de supervisión genérica.<br/> Dado [**que ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) se implementa directamente en el vendedor de CRM, puede usar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) (también implementado en el vendedor de CRM). A continuación, se puede usar para anular directamente la transacción si es necesario ([**ICrmLogControl::ForceTransactionToAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcetransactiontoabort)).<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

