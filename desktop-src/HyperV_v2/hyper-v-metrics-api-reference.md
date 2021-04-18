---
description: La API de métricas de Hyper-V define los siguientes elementos de programación.
ms.assetid: 00235614-9FCB-4161-B03D-9D557050153B
title: Referencia de API de métricas de Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdd4945bd390d995378c290f846335371fead753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687330"
---
# <a name="hyper-v-metrics-api-reference"></a>Referencia de API de métricas de Hyper-V

La API de métricas de Hyper-V define los siguientes elementos de programación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md)<br/> | Representa los aspectos de la definición de una métrica que se deriva de otro valor de métrica.<br/>                                                                                                                                                                                                                             |
| [**MSVM \_ AggregationMetricValue**](msvm-aggregationmetricvalue.md)<br/>           | Representa el valor de instancia de una métrica definida por una instancia de la clase [**MSVM \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) .<br/>                                                                                                                                                         |
| [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)<br/>               | Representa los aspectos de la definición de una métrica.<br/>                                                                                                                                                                                                                                                                       |
| [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md)<br/>                         | Representa un valor de métrica definido por una instancia de la clase [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) .<br/>                                                                                                                                                                                       |
| [**MSVM \_ MetricCollectionDependency**](msvm-metriccollectiondependency.md)<br/>   | Representa la asociación entre dos definiciones de métricas o dos valores de métricas.<br/>                                                                                                                                                                                                                                      |
| [**MSVM \_ MetricDefForME**](msvm-metricdefforme.md)<br/>                           | Define la asociación entre un [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md) y un [**\_ ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) para definir las métricas de este último. La definición de métricas se proporciona en el contexto mediante ManagedElement, que es el motivo por el que la definición depende del elemento.<br/> |
| [**MSVM \_ MetricForME**](msvm-metricforme.md)<br/>                                 | Esta asociación vincula un elemento administrado con los valores de métricas que se mantienen para él.<br/>                                                                                                                                                                                                                               |
| [**MSVM \_ MetricInstance**](msvm-metricinstance.md)<br/>                           | Representa una asociación de objetos de valor de métrica con sus definiciones de métricas.<br/>                                                                                                                                                                                                                                    |
| [**MSVM \_ MetricService**](msvm-metricservice.md)<br/>                             | Proporciona la capacidad de administrar las métricas.<br/>                                                                                                                                                                                                                                                                              |
| [**MSVM \_ MetricServiceCapabilities**](msvm-metricservicecapabilities.md)<br/>     | Describe las capacidades de la instancia de [**MSVM \_ MetricService**](msvm-metricservice.md) asociada.<br/>                                                                                                                                                                                                             |
| [**MSVM \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md)<br/>       | Representa la configuración para el servicio de métricas. Las propiedades de esta clase no se pueden modificar directamente. El cliente debe llamar al método [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) para modificar cualquiera de estas propiedades.<br/>                                                              |



 

 

