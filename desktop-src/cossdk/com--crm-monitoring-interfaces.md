---
description: La infraestructura de CRM proporciona un conjunto de interfaces que se pueden usar para supervisar CRMs en una aplicación de servidor determinada.
ms.assetid: b8f40c91-001b-4003-b377-57a918988100
title: Interfaces de supervisión de CRM de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c893040c46810c980c647cbacdc808200e8d5f5e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274899"
---
# <a name="com-crm-monitoring-interfaces"></a>Interfaces de supervisión de CRM de COM+

La infraestructura de CRM proporciona un conjunto de interfaces que se pueden usar para supervisar CRMs en una aplicación de servidor determinada. Para tener acceso a las interfaces de supervisión, un componente que se ejecuta dentro de la aplicación de servidor debe crear primero un funcionario de CRM especializado denominado encargado de recuperación de CRM.

En el uso normal de CRMs, se espera que las transacciones sean de corta duración y, por lo tanto, los trabajos de CRM y los compensadores de CRM existen durante un breve período de tiempo, normalmente solo unos pocos segundos como máximo. Por tanto, las interfaces de supervisión están diseñadas para proporcionar una instantánea del estado de la CRMs que se ejecuta en un momento determinado. Si alguno de los CRMs tiene problemas, se pueden usar las interfaces de supervisión para cero en el CRM problemático, para inspeccionar sus entradas de registro y anular su transacción si es necesario.

A continuación se muestran las tres interfaces de supervisión de CRM y las descripciones de cómo funcionan.



| Interfaz                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)<br/>                     | Mediante [**ICrmMonitor:: GetClerks**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-getclerks), se puede obtener una instantánea del conjunto actual de empleados de CRM activos dentro de la aplicación de servidor. A partir de este, se puede localizar y consultar un objeto de colección de objetos de interés determinado de CRM, incluido el estado actual de su transacción y las entradas de registro escritas por el CRM.<br/> Cuando la herramienta de supervisión ha determinado qué funcionario es de interés, llama a [**ICrmMonitor:: HoldClerk**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-holdclerk) para obtener una interfaz [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) en ese funcionario determinado. En este punto, la herramienta de supervisión mantiene una referencia a ese funcionario y, si la transacción se completa, el funcionario se mantiene en la memoria y no se libera hasta que se realiza la herramienta de supervisión.<br/>                                                                                                                                                                                                    |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)<br/>         | Mediante esta interfaz, se puede examinar el objeto de colección Clerk para obtener información sobre el estado de la colección Clerk en el momento en que se obtuvo. Esta información incluye el número de empleados, el ProgID del compensador de CRM usado por el funcionario, la descripción proporcionada en el momento en que se registró el compensador de CRM (mediante [**ICrmLogControl:: RegisterCompensator**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator)), el identificador de unidad de trabajo de la transacción y el ID. de actividad. Los empleados individuales también se identifican de forma única mediante un "CLSID de instancia de funcionario", que no es un CLSID COM en el sentido habitual del término, sino simplemente un GUID único que identifica este funcionario concreto para su duración.<br/>                                                                                                                                                                                                                                                                                                |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)<br/> | Esta interfaz se puede usar para consultar el estado actual de la transacción, para averiguar el número de entradas de registro que ha escrito este funcionario de CRM y para obtener los datos de entrada de registro reales. Las entradas de registro se proporcionan desde la interfaz [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) en el mismo formato en que se escribieron originalmente (mediante [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)). Además, **ICrmMonitorLogRecords** se puede implementar opcionalmente para convertir las entradas de registro en un formato visible, de forma que se puedan presentar con una herramienta de supervisión genérica.<br/> Dado que [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) se implementa directamente en el funcionario de CRM, puede ejecutar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) (también implementado en el distribuidor de CRM). A continuación, se puede usar para anular directamente la transacción si es necesario ([**ICrmLogControl:: ForceTransactionToAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcetransactiontoabort)).<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de Administrador de recursos de compensación de COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

