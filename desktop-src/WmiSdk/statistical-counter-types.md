---
description: El proveedor de datos de rendimiento con formato de alto rendimiento wmi calcula los tipos de contadores estadísticos en un número especificado de ejemplos de datos de contadores sin procesar.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Tipos de contadores estadísticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1289bae423305bac863afefaba8e5700268d98e594fe767d597c8470aa4f1ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314824"
---
# <a name="statistical-counter-types"></a>Tipos de contadores estadísticos

El proveedor de [](formatted-performance-data-provider.md) datos de rendimiento con formato de alto rendimiento wmi calcula los tipos de contadores estadísticos en un número especificado de ejemplos de datos de contadores sin procesar. Los algoritmos para los tipos de contador no requieren propiedades heredadas de marca de tiempo o frecuencia (como **TimeStamp \_ PerfTime** o **Frequency \_ PerfTime)** que requieren otros tipos de contadores.

En su lugar, los tipos de contador estadísticos **admiten un calificador** que identifica cuántas muestras usar. Se recopila un ejemplo cuando se llama [**al método Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) para el objeto de rendimiento. Para los scripts, use [**el método SWbemRefresher.Refresh.**](swbemrefresher-refresh.md) Los datos calculados contienen el resultado del cálculo realizado en el **número sampleWindow** de muestras de la propiedad de datos sin procesar. Los datos sin procesar para el cálculo proceden del nombre de propiedad especificado en el **calificador Counter.**

Para obtener más información, vea [Obtener datos estadísticos de rendimiento](obtaining-statistical-performance-data.md) y Obtener acceso a clases de rendimiento [preinstaladas de WMI.](accessing-wmi-preinstalled-performance-classes.md)



| CounterType (constante)                    | Descripción                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [COOKER \_ AVERAGE](cooker-average.md)   | Suma las observaciones repetidas de una propiedad en una clase [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y divide la suma por el número de observaciones.                              |
| [COOKER \_ MAX](cooker-max.md)           | Valor más grande de un conjunto de observaciones de una propiedad en una clase [**\_ PerfRawData de Win32.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)                                                                    |
| [COOKER \_ MIN](cooker-min.md)           | Valor más pequeño de un conjunto de observaciones de una propiedad en una clase [**\_ PerfRawData de Win32.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)                                                                   |
| [INTERVALO DE LA \_ COCINA](cooker-range.md)       | Diferencia entre los [valores Min](cooker-min.md) y [Max](cooker-max.md) de un conjunto de observaciones sin procesar de una propiedad en una clase [**\_ PerfRawData de Win32.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) |
| [VARIANZA DE LA \_ COCINA](cooker-variance.md) | Medida de variabilidad que se puede usar para caracterizar la dispersión de un conjunto de observaciones sin procesar de una propiedad en una clase [**\_ PerfRawData de Win32.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contadores de rendimiento wmi](wmi-performance-counter-types.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> <dt>

[Actualizar datos WMI en scripts](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Acceso a datos de rendimiento en script](accessing-performance-data-in-script.md)
</dt> <dt>

[Acceso a datos de rendimiento en C++](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
