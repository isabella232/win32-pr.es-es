---
description: Suministra calculada (&\# 0034; cocida&\# 0034;) datos de contadores de rendimiento. Proporciona datos dinámicos a las clases WMI derivadas de Win32 \_ PerfFormattedData. También se conoce como proveedor de contadores cocidos.
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
ms.openlocfilehash: 0db075ebdafcd31c7aa0980d191ed565873f686f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706155"
---
# <a name="formatted-performance-data-provider"></a>Proveedor de datos de rendimiento con formato

\[El proveedor de datos de rendimiento con formato, también conocido como "proveedor de contador cocido", ya no está disponible para su uso. En su lugar, use el proveedor [WMIPerfInst](wmiperfinst-provider.md) .\]

El proveedor de datos de rendimiento con formato de alto rendimiento proporciona datos de contadores de rendimiento calculados ("cocidos"), como el porcentaje de tiempo que un disco dedica a escribir datos. Este proveedor proporciona datos dinámicos a las clases WMI derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). La diferencia entre este proveedor y el [proveedor de contadores de rendimiento](performance-counter-provider.md) es que el proveedor de contadores de rendimiento proporciona datos sin procesar y el proveedor de contadores elaborados proporciona datos de rendimiento que aparecen exactamente como en el [*monitor de sistema*](gloss-s.md). El nombre de la instancia de [**\_ \_ Win32Provider**](--win32provider.md) es "HiPerfCooker \_ v1".

El nombre de clase con formato WMI para un objeto de contador tiene el formato "Win32 PerfFormattedData nombre de objeto nombre de \_ \_ *servicio \_* \_ ".*\_* Por ejemplo, el nombre de clase WMI que contiene los contadores de disco lógico es **Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**. Estas clases se encuentran en el espacio de \\ nombres "root CIMv2".

Dado que las clases de datos de rendimiento se agregan y modifican dinámicamente en un sistema determinado, no es posible documentar formalmente las propiedades de todos los objetos de rendimiento conocidos. Para determinar qué clases están disponibles, y para identificar qué miembros tienen esas clases, consulte [recuperar documentación para objetos de datos de rendimiento sin formato y con formato](retrieving-raw-and-formatted-performance-data.md).

Las [**clases \_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) usan el calificador **CookingType** en los [tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md) para especificar la fórmula para calcular los datos de rendimiento. Este calificador es el mismo que el calificador de **tipo** en las clases [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .

Como proveedor de alto rendimiento, el proveedor de contadores cocidos implementa la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como el método [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) y los siguientes métodos de [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :

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

 

 
