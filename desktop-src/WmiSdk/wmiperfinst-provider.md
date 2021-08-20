---
description: A partir Windows Vista, el proveedor WmiPerfInst proporciona dinámicamente datos de contadores de rendimiento sin formato y sin formato a las clases de contadores de rendimiento de WMI derivadas de Win32 \_ Perf.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Proveedor WmiPerfInst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a781fc1dc48f0e16d1c25e03eff1b2ab3c80fcd7058d1b49f95912b392d241
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049753"
---
# <a name="wmiperfinst-provider"></a>Proveedor WmiPerfInst

A partir Windows Vista, el proveedor WmiPerfInst proporciona dinámicamente datos de contadores de rendimiento sin formato y sin formato a las clases de contadores de rendimiento wmi derivadas [de](/windows/desktop/CIMWin32Prov/performance-counter-classes) [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf). Este proveedor reemplaza el [proveedor](formatted-performance-data-provider.md)de datos de rendimiento con formato , también conocido como "Proveedor de contadores preparado" y el proveedor de [contadores de rendimiento](performance-counter-provider.md).

El proveedor WmiPerfInst proporciona datos a las clases WMI proporcionadas por el [proveedor WMIPerfClass.](wmiperfclass-provider.md) Este proveedor es un puente entre las instancias del Asistente de datos de rendimiento (PDH) y las clases de rendimiento wmi proporcionadas por el proveedor WmiPerfClass. Cuando WmiPerfInst recibe una consulta de datos, carga la clase y usa los calificadores de clase y propiedad [para](qualifiers-specific-to-wmi-performance-classes.md) buscar las instancias de PDH. Para obtener más información, [vea Usar las funciones PDH para consumir datos de contador.](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)

No se recomienda desarrollar nuevos objetos de rendimiento mediante la creación de un proveedor wmi de alto rendimiento y depender del proceso de adaptador inverso de [*ADAP*](gloss-r.md) para transferir los datos a las bibliotecas de rendimiento. La excepción es cuando está desarrollando un controlador Windows Driver Model y desea proporcionar datos de rendimiento. Aunque el proceso de adaptador inverso sigue funcionando por compatibilidad con versiones anteriores, el método recomendado es usar contadores de rendimiento [versión 6.0.](/windows/desktop/PerfCtrs/performance-counters-portal)

El [**\_ \_ nombre de instancia win32Provider**](--win32provider.md) de este proveedor es "WmiPerfInst".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> <dt>

[Bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> </dl>

 

 
