---
description: El proveedor WMIPerfClass y el proveedor WMIPerfInst proporcionan dinámicamente datos de contador de rendimiento para las clases de contador de rendimiento wmi.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Bibliotecas de rendimiento y WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063942"
---
# <a name="performance-libraries-and-wmi"></a>Bibliotecas de rendimiento y WMI

El [proveedor WMIPerfClass y](wmiperfclass-provider.md) el proveedor [WMIPerfInst](wmiperfinst-provider.md) proporcionan dinámicamente datos de contador de rendimiento para las clases de [contador de rendimiento de](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI .

## <a name="wmiperfclass-and-wmiperfinst-providers"></a>Proveedores WMIPerfClass y WMIPerfInst

[El proveedor WMIPerfClass crea](wmiperfclass-provider.md) clases [de contador de rendimiento WMI en](/windows/desktop/CIMWin32Prov/performance-counter-classes) la inicialización del sistema. El [proveedor WMIPerfInst proporciona](wmiperfinst-provider.md) dinámicamente datos de contadores de rendimiento para estas clases. El proveedor WMIPerfClass proporciona clases para los contadores de rendimiento de la versión 1 [y](/windows/desktop/PerfCtrs/performance-counters-portal)la versión 2.

Los contadores de la versión 1 se encuentran en el Registro en **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Services**. Los servicios que proporcionan datos de rendimiento tienen una **subclave** Rendimiento. Las clases de rendimiento wmi creadas a partir de los contadores de la versión 1 no tienen "Contadores" como parte de su nombre.

Los **GUID que** identifican un proveedor de contadores de rendimiento de la versión 2 se encuentran en el Registro en **HKEY LOCAL MACHINE SOFTWARE \_ Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.

WMIPerfClass se registra como un proveedor de clases WMI normal. WMIPerfInst es un proveedor de instancias wmi que proporciona datos del Asistente de datos de rendimiento (PDH) para los contadores de la versión 1 y la versión 2. Para obtener más información, [vea Usar las funciones PDH para consumir datos de contador.](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> </dl>

 

 
