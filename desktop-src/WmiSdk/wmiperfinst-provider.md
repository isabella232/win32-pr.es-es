---
description: A partir de Windows Vista, el proveedor WmiPerfInst proporciona datos del contador de rendimiento sin formato y con formato de forma dinámica a clases de contador de rendimiento de WMI derivadas de rendimiento de Win32 \_ .
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Proveedor WmiPerfInst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696914"
---
# <a name="wmiperfinst-provider"></a>Proveedor WmiPerfInst

A partir de Windows Vista, el proveedor WmiPerfInst proporciona datos del contador de rendimiento sin formato y con formato de forma dinámica a [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI derivadas de [**\_ rendimiento de Win32**](/windows/desktop/CIMWin32Prov/win32-perf). Este proveedor reemplaza el [proveedor de datos de rendimiento con formato](formatted-performance-data-provider.md), también conocido como "proveedor de contador cocido", y el [proveedor de contadores de rendimiento](performance-counter-provider.md).

El proveedor WmiPerfInst proporciona datos a las clases WMI que proporciona el proveedor [WMIPerfClass](wmiperfclass-provider.md) . Este proveedor es un puente entre las instancias del ayudante de datos de rendimiento (PDH) y las clases de rendimiento de WMI proporcionadas por el proveedor de WmiPerfClass. Cuando WmiPerfInst recibe una consulta de datos, carga la clase y usa los [calificadores](qualifiers-specific-to-wmi-performance-classes.md) de clase y propiedad para buscar las instancias de PDH. Para obtener más información, vea [usar las funciones de PDH para consumir datos de contador](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

No se recomienda desarrollar nuevos objetos de rendimiento mediante la creación de un proveedor de alto rendimiento de WMI y depender del proceso del [*adaptador de ADAP inverso*](gloss-r.md) para transferir los datos a las bibliotecas de rendimiento. La excepción es cuando se desarrolla un controlador de Modelo de controlador de Windows y se desea proporcionar datos de rendimiento. Aunque el proceso de adaptador inverso sigue funcionando por compatibilidad con versiones anteriores, el método recomendado es usar los [contadores de rendimiento versión 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

El nombre de instancia [**\_ \_ Win32Provider**](--win32provider.md) de este proveedor es "WmiPerfInst".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> <dt>

[Bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> </dl>

 

 
