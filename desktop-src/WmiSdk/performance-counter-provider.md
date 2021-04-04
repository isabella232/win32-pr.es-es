---
description: El proveedor de contadores de rendimiento es un proveedor de alto rendimiento que proporciona datos de contador de rendimiento sin procesar a las clases de contador de rendimiento de WMI derivadas de Win32 \_ PerfRawData. El nombre de la \_ \_ instancia de Win32Provider es &\# 0034; NT5 \_ GenericPerfProvider \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Proveedor de contador de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083339"
---
# <a name="performance-counter-provider"></a>Proveedor de contador de rendimiento

\[El proveedor de contadores de rendimiento ya no está disponible para su uso. En su lugar, use el proveedor [WMIPerfInst](wmiperfinst-provider.md) .\]

El proveedor de contadores de rendimiento es un proveedor de alto rendimiento que proporciona datos de contador de rendimiento sin procesar a las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata). El nombre de la instancia de [**\_ \_ Win32Provider**](--win32provider.md) es "NT5 \_ GenericPerfProvider \_ v1".

Las [**clases \_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) se encuentran en el espacio de \\ nombres "root CIMv2" de WMI. Cada clase de rendimiento de WMI corresponde a un objeto de rendimiento en una biblioteca de rendimiento. Las propiedades de estas clases representan los contadores para el objeto. El nombre de clase WMI para un objeto de contador sin formato tiene el formato **Win32 \_ \_ \_ PerfRawData* nombre del servicio nombre del \_ *\_* objeto \_ * * *. Por ejemplo, el nombre de clase WMI que contiene los contadores de disco lógico es [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).

Puede usar la clase [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondiente para obtener los datos de rendimiento calculados previamente que se muestran en el [*monitor de sistema*](gloss-s.md). Por ejemplo, use la clase [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) para obtener datos de disco calculados previamente.

Para obtener más información sobre cómo escribir un cliente que pueda tener acceso a datos de rendimiento sin procesar, vea [obtener acceso a los datos de rendimiento en C++](accessing-performance-data-in-c--.md).

Como proveedor de alto rendimiento, el proveedor de contadores de rendimiento implementa la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como el método [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) y los siguientes métodos [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :

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

 

 
