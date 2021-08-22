---
description: El proveedor de contadores de rendimiento es un proveedor de alto rendimiento que proporciona datos de contadores de rendimiento sin procesar a las clases de contadores de rendimiento wmi derivadas de Win32 \_ PerfRawData. El \_ \_ nombre de instancia de Win32Provider &\# 0034; NT5 \_ GenericPerfProvider \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Proveedor de contador de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c846d66cd183e866623004cacfbcb630ac68480fab8dd58eca2b5a4dc6d2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050533"
---
# <a name="performance-counter-provider"></a>Proveedor de contador de rendimiento

\[El proveedor de contadores de rendimiento ya no está disponible para su uso. En su lugar, use [el proveedor WMIPerfInst.](wmiperfinst-provider.md)\]

El proveedor de contadores de rendimiento es un proveedor de alto rendimiento que proporciona datos de contadores de rendimiento sin procesar a las clases de contadores de rendimiento [wmi](/windows/desktop/CIMWin32Prov/performance-counter-classes) derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata). El [**\_ \_ nombre de instancia de Win32Provider**](--win32provider.md) es "NT5 \_ GenericPerfProvider \_ V1".

Las [**clases \_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) se encuentran en el espacio de nombres \\ "CIMv2 raíz" de WMI. Cada clase de rendimiento WMI corresponde a un objeto de rendimiento en una biblioteca de rendimiento. Las propiedades de estas clases representan los contadores del objeto . El nombre de clase WMI para un objeto de contador sin formato tiene el formato * Nombre de objeto del nombre del servicio *Win32 \_ \_ \_ PerfRawData.*.* \_ *\_* \_ Por ejemplo, el nombre de clase WMI que contiene los contadores de disco lógico es [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).

Puede usar la clase [**\_ Win32 PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondiente para obtener los datos de rendimiento calculados previamente que se muestran en [*el Monitor del sistema*](gloss-s.md). Por ejemplo, use la clase [**\_ Win32 PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) para obtener datos de disco calculados previamente.

Para obtener más información sobre cómo escribir un cliente que puede acceder a datos de rendimiento sin procesar, vea Acceso a datos [de rendimiento en C++.](accessing-performance-data-in-c--.md)

Como proveedor de alto rendimiento, el proveedor de contadores de rendimiento implementa la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como el método [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) y los métodos [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) siguientes:

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

 

 
