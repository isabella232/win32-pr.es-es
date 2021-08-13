---
description: Proporciona los valores calculados \# (&0034;cooked&\# 0034;) datos del contador de rendimiento. Proporciona datos dinámicos a las clases WMI derivadas de Win32 \_ PerfFormattedData. También se conoce como proveedor de contadores preparado.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Proveedor de datos de rendimiento con formato
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ab8e931c3d03c619af5b1e37cadd8dacdccd21534513ed3a1aa1d7b9076acfb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556618"
---
# <a name="formatted-performance-data-provider"></a>Proveedor de datos de rendimiento con formato

\[El proveedor de datos de rendimiento con formato, también conocido como "proveedor de contadores preparado", ya no está disponible para su uso. En su lugar, use [el proveedor WMIPerfInst.](wmiperfinst-provider.md)\]

El proveedor de datos de rendimiento con formato de alto rendimiento proporciona datos de contador de rendimiento calculados ("preparado"), como el porcentaje de tiempo que un disco dedica a escribir datos. Este proveedor proporciona datos dinámicos a las clases WMI derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). La diferencia entre este [](performance-counter-provider.md) proveedor y el proveedor de contadores de rendimiento es que el proveedor contador de rendimiento proporciona datos sin procesar y el proveedor de contadores preparado proporciona datos de rendimiento que aparecen exactamente igual que en el [*Monitor de sistema*](gloss-s.md). El [**\_ \_ nombre de instancia de Win32Provider**](--win32provider.md) es "HiPerfCooker \_ v1".

El nombre de clase con formato WMI para un objeto de contador tiene el formato "Nombre de objeto de nombre de servicio Win32 \_ PerfFormattedData". \_ *\_* \_ *\_* Por ejemplo, el nombre de clase WMI que contiene los contadores de disco lógico es **Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**. Estas clases se encuentran en el espacio de nombres \\ "ROOT CIMv2".

Dado que las clases de datos de rendimiento se agregan y modifican dinámicamente en un sistema determinado, no es posible documentar formalmente las propiedades de todos los objetos de rendimiento conocidos. Para determinar qué clases están disponibles e identificar qué miembros tienen esas clases, vea Recuperación de documentación para objetos de datos de rendimiento sin formato y [sin formato.](retrieving-raw-and-formatted-performance-data.md)

Las [**clases \_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) usan el calificador **DentoqueType** en Tipos de contadores de rendimiento [WMI](wmi-performance-counter-types.md) para especificar la fórmula para calcular los datos de rendimiento. Este calificador es el mismo que el **calificador CounterType** en las clases [**\_ PerfRawData de Win32.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)

Como proveedor de alto rendimiento, el proveedor cooked Counter implementa la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como el método [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) y los métodos [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) siguientes:

-   [**CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [**CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [**CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [**GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [**QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [**StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> </dl>

 

 
