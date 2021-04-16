---
description: El proveedor WMIPerfClass y el proveedor WMIPerfInst proporcionan dinámicamente datos de contador de rendimiento para las clases de contador de rendimiento de WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Bibliotecas de rendimiento y WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705881"
---
# <a name="performance-libraries-and-wmi"></a>Bibliotecas de rendimiento y WMI

El [proveedor WMIPerfClass](wmiperfclass-provider.md) y el [proveedor WMIPerfInst](wmiperfinst-provider.md) proporcionan dinámicamente datos de contador de rendimiento para las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)de WMI.

## <a name="wmiperfclass-and-wmiperfinst-providers"></a>Proveedores de WMIPerfClass y WMIPerfInst

El [proveedor WMIPerfClass](wmiperfclass-provider.md) crea [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI en la inicialización del sistema. El [proveedor WMIPerfInst](wmiperfinst-provider.md) proporciona dinámicamente datos de contadores de rendimiento para estas clases. El proveedor del proveedor WMIPerfClass proporciona clases para los [contadores de rendimiento](/windows/desktop/PerfCtrs/performance-counters-portal)de la versión 1 y la versión 2.

Los contadores de la versión 1 se encuentran en el registro en **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**. Los servicios que proporcionan los datos de rendimiento tienen una subclave de **rendimiento** . Las clases de rendimiento de WMI creadas a partir de contadores de la versión 1 no tienen "contadores" como parte de su nombre.

El **GUID** que identifica un proveedor de contador de rendimiento de la versión 2 se encuentra en el registro en **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.

WMIPerfClass se registra como un proveedor de clases WMI normal. WMIPerfInst es un proveedor de instancias de WMI que proporciona datos del ayudante de datos de rendimiento (PDH) para los contadores de la versión 1 y la versión 2. Para obtener más información, vea [usar las funciones de PDH para consumir datos de contador](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> </dl>

 

 
