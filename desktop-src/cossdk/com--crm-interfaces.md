---
description: Las interfaces de CRM son necesarias para proporcionar compatibilidad con los trabajadores de CRM y los compensadores de CRM desarrollados con Visual Basic y Visual C++.
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: COM+ CRM Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973544"
---
# <a name="com-crm-interfaces"></a>COM+ CRM Interfaces

Las interfaces de CRM son necesarias para proporcionar compatibilidad con los trabajadores de CRM y los compensadores de CRM desarrollados con Visual Basic y Visual C++.

Puede usar com+ Compensating Resource Manager (CRM) para integrar de forma rápida y sencilla los recursos de la aplicación con Microsoft DTC (Coordinador de transacciones distribuidas) transacciones de Microsoft DTC (Coordinador de transacciones distribuidas) (DTC).

Es más fácil para los componentes escritos Visual Basic crear una entrada de registro como una colección de variantes. Además, Visual Basic componentes son subprocesos de apartamento, lo que implica que debe ser posible serializar las interfaces del apartamento multiproceso a un solo subproceso. Los componentes de CRM desarrollados con Visual C++ también podrían usar el modelo de subprocesamiento Apartment, aunque se recomienda que utilicen en su lugar el modelo de subprocesamiento ambos.

Las interfaces descritas en la tabla siguiente proporcionan información de referencia detallada para los desarrolladores de CRM de COM+.



| Interfaces crm                                             | Descripción                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | Esta interfaz proporciona registros no estructurados en Visual C++.                                                           |
| [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | Esta interfaz entrega registros estructurados al compensador crm cuando se usa Visual Basic.                            |
| [**ICrmFormatLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | Esta interfaz convierte las entradas de registro al formato visualizable para que se puedan presentar mediante una herramienta de supervisión genérica. |
| [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | Crm Worker y CRM Compensator usan esta interfaz para escribir registros en el registro y hacerlos duraderos.           |
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | Esta interfaz captura una instantánea del estado actual de un CRM y contiene un empleado de CRM específico.                          |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | Esta interfaz obtiene información sobre el estado de los empleados.                                                             |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | Esta interfaz supervisa las entradas de registro individuales que mantiene un empleado de CRM específico para una transacción determinada.            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



