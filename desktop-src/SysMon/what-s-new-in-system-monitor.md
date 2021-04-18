---
title: Novedades del monitor de sistema
description: En la tabla siguiente se identifican las novedades de cada versión del monitor de sistema (SYSMON).
ms.assetid: 9cb0e0db-0933-4993-a995-74a36a24eccb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3662e83954630232e3fe30c26a3f6d94aa9cc7
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/26/2020
ms.locfileid: "104420378"
---
# <a name="whats-new-in-system-monitor"></a>Novedades del monitor de sistema

En la tabla siguiente se identifican las novedades de cada versión del monitor de sistema (SYSMON).



| Versión     | Descripción de las características                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión 3.7 | Esta versión agrega nuevos tipos de gráficos, la capacidad de seleccionar varios contadores, recuperar valores de contadores de un punto del gráfico, guardar valores de contadores en un archivo de registro y la opción de hacer que un gráfico de líneas se desplace continuamente en la ventana del gráfico en lugar de ajustarse a sí mismo. Incluido en Windows Server 2008 y Windows Vista.<br/> |



 

## <a name="version-37"></a>Versión 3.7

Nuevas propiedades y métodos que se agregaron a un [**objeto de contraelemento**](counteritem.md).

-   [**GetDataAt**](counteritem-getdataat.md)
-   [**Seleccionado**](counteritem-selected.md)
-   [**Visible**](counteritem-visible.md)
-   Rango de valores válidos modificados para el valor de [ **peritem. width**](counteritem-width.md)

Nuevas propiedades y métodos que se agregaron a [**SystemMonitor**](systemmonitor.md).

-   [**BatchingLock**](systemmonitor-batchinglock.md)
-   [**ChartScroll**](systemmonitor-chartscroll.md)
-   [**ClearData**](systemmonitor-cleardata.md)
-   [**DataPointCount**](systemmonitor-datapointcount.md)
-   [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)
-   [**EnableToolTips**](systemmonitor-enabletooltips.md)
-   [**GetLogViewRange**](systemmonitor-getlogviewrange.md)
-   [**LoadSettings**](systemmonitor-loadsettings.md)
-   [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)
-   [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
-   [**Registrar**](systemmonitor-relog.md)
-   [**SaveAs**](systemmonitor-saveas.md)
-   [**ScaleToFit**](systemmonitor-scaletofit.md)
-   [**SetLogViewRange**](systemmonitor-setlogviewrange.md)
-   [**ShowTimeAxisLables**](systemmonitor-showtimeaxislabels.md)

Nuevas enumeraciones que se agregaron.

-   [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)
-   [**SysmonFileType**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)
-   Se agregaron nuevos valores de tipo de presentación a [ **DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)

 

 





