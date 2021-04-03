---
description: El proveedor de datos de rendimiento con formato de alto rendimiento de WMI calcula los tipos de contador estadísticos en un número especificado de muestras de datos del contador sin formato.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Tipos de contadores estadísticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082977"
---
# <a name="statistical-counter-types"></a>Tipos de contadores estadísticos

El proveedor de datos de [rendimiento con formato](formatted-performance-data-provider.md) de alto rendimiento de WMI calcula los tipos de contador estadísticos en un número especificado de muestras de datos del contador sin formato. Los algoritmos de los tipos de contador no requieren propiedades de frecuencia o marca de tiempo heredadas (como **timestamp \_ PerfTime** o **Frequency \_ PerfTime**) que otros tipos de contador requieren.

En su lugar, los tipos de contador estadísticos admiten un **calificador** que identifique el número de ejemplos que se van a utilizar. Se recopila un ejemplo cuando se llama al método [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) para el objeto de rendimiento. En el caso de los scripts, use el método [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) . Los datos calculados contienen el resultado del cálculo realizado en el número de muestras de **SampleWindow** de la propiedad de datos sin procesar. Los datos sin procesar para el cálculo incluyen FRM el nombre de propiedad especificado en el calificador de **contador** .

Para obtener más información, vea [obtener datos de rendimiento estadísticos](obtaining-statistical-performance-data.md) y [obtener acceso a las clases de rendimiento preinstaladas de WMI](accessing-wmi-preinstalled-performance-classes.md).



| Contratipo (constante)                    | Descripción                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [media de COOKER \_](cooker-average.md)   | Suma las observaciones repetidas de una propiedad en una clase [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y divide la suma por el número de observaciones.                              |
| [COOKER \_ máx.](cooker-max.md)           | Valor más grande de un conjunto de observaciones de una propiedad en una clase [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .                                                                    |
| [COOKER \_ mín.](cooker-min.md)           | Valor menor de un conjunto de observaciones de una propiedad en una clase [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .                                                                   |
| [\_intervalo Cooker](cooker-range.md)       | Diferencia entre los valores [mínimo](cooker-min.md) y [máximo](cooker-max.md) de un conjunto de observaciones sin formato de una propiedad en una clase [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . |
| [varianza de COOKER \_](cooker-variance.md) | Medida de variabilidad que se puede utilizar para caracterizar la dispersión para un conjunto de observaciones sin formato de una propiedad en una clase [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> <dt>

[Actualizar datos WMI en scripts](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Obtener acceso a los datos de rendimiento del script](accessing-performance-data-in-script.md)
</dt> <dt>

[Obtener acceso a los datos de rendimiento en C++](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
