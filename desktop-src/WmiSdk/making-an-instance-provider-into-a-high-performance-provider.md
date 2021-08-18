---
description: No se recomienda escribir un proveedor de alto rendimiento WMI para crear contadores de rendimiento.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Convertir un proveedor de instancias en un High-Performance personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b6326c0af270088c37bb2a1798951ba0a9de7afe65ec593f5f7ab6768b83b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996495"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a>Convertir un proveedor de instancias en un High-Performance personalizado

No se recomienda escribir un proveedor de alto rendimiento WMI para crear contadores de rendimiento. A partir de Windows Vista, las clases de contadores de rendimiento wmi ya no se migran a las bibliotecas de rendimiento de Windows mediante el adaptador inverso AutoDiscovery/AutoPurge (ADAP). [](/windows/desktop/CIMWin32Prov/performance-counter-classes) Para crear un proveedor de contadores de rendimiento, use [Contadores de rendimiento versión 2.0.](/windows/desktop/PerfCtrs/performance-counters-portal) Una vez creados los objetos de la biblioteca de rendimiento, el proveedor [WMIPerfClass](wmiperfclass-provider.md) analiza los objetos y crea o actualiza una clase WMI derivada de [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf) para cada objeto de rendimiento. A [continuación, el proveedor WMIPerfInst](wmiperfinst-provider.md) proporciona dinámicamente datos de contadores de rendimiento sin formato y sin formato a las clases de rendimiento wmi.

El siguiente procedimiento de alto nivel proporciona los pasos necesarios para crear un proveedor de alto rendimiento.

**Para crear un proveedor de alto rendimiento**

1.  Registre el proveedor con WMI. Para obtener más información, [vea Registrar un proveedor de High-Performance .](registering-a-high-performance-provider.md)
2.  Implemente el proveedor. Para obtener más información, vea [Escribir un proveedor de instancias.](writing-an-instance-provider.md)
3.  Implemente la interfaz de alto rendimiento. Para obtener más información, vea [Implementing the High-Performance Interface](implementing-the-high-performance-interface.md).
4.  Derive y escriba el esquema Managed Object Format (MOF) para obtener datos de rendimiento sin procesar. Para obtener más información, [vea Supporting the Win32 \_ PerfRawData Class](supporting-the-win32-perfrawdata-class.md).
5.  Derive y escriba el esquema MOF para obtener datos precalculados. Al admitir esta clase, no es necesario que el proveedor realice los cálculos. Estos datos serán los mismos que aparecen en el Monitor de sistema en Perfmon. Para obtener más información, [vea Compatibilidad con la clase \_ PerfFormattedData de Win32](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
