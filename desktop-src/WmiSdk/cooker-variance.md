---
description: La \_ fórmula de tipo de contador varianza de cooker proporciona variabilidad que se usa para caracterizar la dispersión para un conjunto de observaciones sin formato de una propiedad en una instancia de PerfRawData de Win32 \_ .
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f9de6c5241ccd486e4da76864139e3e54f5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082450"
---
# <a name="cooker_variance"></a>varianza de COOKER \_

La \_ fórmula de tipo de contador varianza de cooker proporciona variabilidad que se usa para caracterizar la dispersión para un conjunto de observaciones sin formato de una propiedad en una instancia de [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . La varianza se calcula dividiendo la suma del cuadrado de la desviación de la media de cada contador entre el número de contadores. En otras palabras, la varianza es el promedio de las desviaciones cuadradas de la media de cada contador. Este tipo de contador solo se define en WMI y no está disponible para las tecnologías de supervisión de rendimiento, como los [contadores de rendimiento versión 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

Para obtener más información sobre la fórmula de tipo de contador, vea [tipos de contadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).

Para obtener más información sobre los proveedores y scripts de alto rendimiento, consulte [tipos de contadores de rendimiento de WMI](wmi-performance-counter-types.md).

## <a name="example-code"></a>Código de ejemplo

Para obtener ejemplos de código, vea [obtener datos de rendimiento estadísticos](obtaining-statistical-performance-data.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contadores estadísticos](statistical-counter-types.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> </dl>

 

 
