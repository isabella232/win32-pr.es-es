---
description: La API de métricas de Hyper-V define los siguientes elementos de programación.
ms.assetid: 00235614-9FCB-4161-B03D-9D557050153B
title: Referencia de la API de métricas de Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b833d96d26a3c48183c341ab0f1ff2bc9f5b178ca4439e1c035d82551ec3e094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532255"
---
# <a name="hyper-v-metrics-api-reference"></a>Referencia de la API de métricas de Hyper-V

La API de métricas de Hyper-V define los siguientes elementos de programación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md)<br/> | Representa los aspectos de definición de una métrica que se deriva de otro valor de métrica.<br/>                                                                                                                                                                                                                             |
| [**Msvm \_ AggregationMetricValue**](msvm-aggregationmetricvalue.md)<br/>           | Representa el valor de instancia de una métrica definida por una instancia de la clase [**\_ AggregationMetricDefinition de Msvm.**](msvm-aggregationmetricdefinition.md)<br/>                                                                                                                                                         |
| [**BaseMetricDefinition de Msvm \_**](msvm-basemetricdefinition.md)<br/>               | Representa los aspectos de definición de una métrica.<br/>                                                                                                                                                                                                                                                                       |
| [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md)<br/>                         | Representa un valor de métrica definido por una instancia de la clase [**\_ BaseMetricDefinition de Msvm.**](msvm-basemetricdefinition.md)<br/>                                                                                                                                                                                       |
| [**Msvm \_ MetricCollectionDependency**](msvm-metriccollectiondependency.md)<br/>   | Representa la asociación entre dos definiciones de métricas o dos valores de métrica.<br/>                                                                                                                                                                                                                                      |
| [**Msvm \_ MetricDefForME**](msvm-metricdefforme.md)<br/>                           | Define la asociación entre [**un elemento \_ BaseMetricDefinition de Msvm**](msvm-basemetricdefinition.md) y un elemento [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) para definir las métricas de este último. ManagedElement proporciona contexto a la definición de métricas, por lo que la definición depende del elemento .<br/> |
| [**Msvm \_ MetricForME**](msvm-metricforme.md)<br/>                                 | Esta asociación vincula un elemento administrado a los valores de métrica que se mantienen para él.<br/>                                                                                                                                                                                                                               |
| [**Msvm \_ MetricInstance**](msvm-metricinstance.md)<br/>                           | Representa una asociación de objetos de valor de métrica con sus definiciones de métricas.<br/>                                                                                                                                                                                                                                    |
| [**Msvm \_ MetricService**](msvm-metricservice.md)<br/>                             | Proporciona la capacidad de administrar métricas.<br/>                                                                                                                                                                                                                                                                              |
| [**MetricServiceCapabilities de Msvm \_**](msvm-metricservicecapabilities.md)<br/>     | Describe las funcionalidades de la instancia de [**\_ Msvm MetricService**](msvm-metricservice.md) asociada.<br/>                                                                                                                                                                                                             |
| [**Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md)<br/>       | Representa la configuración del servicio de métricas. Las propiedades de esta clase no se pueden modificar directamente. El cliente debe llamar al [**método ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) para modificar cualquiera de estas propiedades.<br/>                                                              |



 

 

