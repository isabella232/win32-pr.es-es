---
description: Las interfaces de CRM son necesarias para proporcionar compatibilidad con los trabajos de CRM y los compensadores de CRM desarrollados mediante Visual Basic y Visual C++.
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: Interfaces de CRM para COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807904"
---
# <a name="com-crm-interfaces"></a>Interfaces de CRM para COM+

Las interfaces de CRM son necesarias para proporcionar compatibilidad con los trabajos de CRM y los compensadores de CRM desarrollados mediante Visual Basic y Visual C++.

Puede usar el Administrador de recursos de compensación de COM+ (CRM) para integrar rápida y fácilmente los recursos de la aplicación con las transacciones de Microsoft Coordinador de transacciones distribuidas (DTC).

Es más fácil para los componentes escritos con Visual Basic crear una entrada de registro como una colección de variantes. Además, los componentes de Visual Basic son subprocesos de apartamento, lo que implica que debe ser posible calcular las referencias de las interfaces del apartamento multiproceso a un contenedor uniproceso. Los componentes de CRM desarrollados con Visual C++ también podrían usar el modelo de subprocesos de apartamento, aunque se recomienda usar el modelo de subprocesos de ambos en su lugar.

Las interfaces descritas en la tabla siguiente proporcionan información de referencia detallada para los programadores de CRMs de COM+.



| Interfaces CRM                                             | Descripción                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | Esta interfaz proporciona entradas de registro no estructuradas en Visual C++.                                                           |
| [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | Esta interfaz proporciona entradas de registro estructuradas al compensador de CRM cuando se usa Visual Basic.                            |
| [**ICrmFormatLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | Esta interfaz convierte las entradas de registro en un formato visible para que se puedan presentar mediante una herramienta de supervisión genérica. |
| [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | Esta interfaz la usa el compensador de CRM y el trabajo de CRM para escribir registros en el registro y hacerlos duraderos.           |
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | Esta interfaz captura una instantánea del estado actual de un CRM y contiene un funcionario de CRM específico.                          |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | Esta interfaz obtiene información sobre el estado de los empleados.                                                             |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | Esta interfaz supervisa las entradas de registro individuales mantenidas por un funcionario de CRM específico para una transacción determinada.            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de Administrador de recursos de compensación de COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



