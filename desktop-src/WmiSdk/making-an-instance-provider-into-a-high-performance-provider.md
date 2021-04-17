---
description: No se recomienda escribir un proveedor de alto rendimiento de WMI para crear contadores de rendimiento.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Crear un proveedor de instancias en un proveedor de High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706390"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a>Crear un proveedor de instancias en un proveedor de High-Performance

No se recomienda escribir un proveedor de alto rendimiento de WMI para crear contadores de rendimiento. A partir de Windows Vista, las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI ya no se migran a las bibliotecas de rendimiento de Windows mediante el adaptador inverso de detección automática/autopurga (ADAP). Para crear un proveedor de contadores de rendimiento, utilice los [contadores de rendimiento versión 2,0](/windows/desktop/PerfCtrs/performance-counters-portal). Después de crear los objetos de biblioteca de rendimiento, el [proveedor de WMIPerfClass](wmiperfclass-provider.md) analiza los objetos y crea o actualiza una clase WMI derivada [**de \_ Perf de Win32**](/windows/desktop/CIMWin32Prov/win32-perf) para cada objeto de rendimiento. A continuación, el [proveedor WMIPerfInst](wmiperfinst-provider.md) proporciona dinámicamente datos de contador de rendimiento sin formato y con formato a las clases de rendimiento de WMI.

El siguiente procedimiento de alto nivel proporciona los pasos necesarios para crear un proveedor de alto rendimiento.

**Para crear un proveedor de alto rendimiento**

1.  Registre el proveedor con WMI. Para obtener más información, vea [registrar un proveedor de High-Performance](registering-a-high-performance-provider.md).
2.  Implemente el proveedor. Para obtener más información, consulte [escribir un proveedor de instancias](writing-an-instance-provider.md).
3.  Implemente la interfaz de alto rendimiento. Para obtener más información, consulte [implementación de la interfaz High-Performance](implementing-the-high-performance-interface.md).
4.  Derive y escriba el esquema de Managed Object Format (MOF) para obtener datos de rendimiento sin procesar. Para obtener más información, consulte [compatibilidad con la \_ clase PerfRawData de Win32](supporting-the-win32-perfrawdata-class.md).
5.  Derive y escriba el esquema MOF para obtener datos precalculados. Al admitir esta clase, no es necesario que el proveedor realice los cálculos. Estos datos serán los mismos que aparecen en el monitor de sistema de Perfmon. Para obtener más información, consulte [compatibilidad con la \_ clase PerfFormattedData de Win32](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
