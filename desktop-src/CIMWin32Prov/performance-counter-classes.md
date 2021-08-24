---
description: Las clases de contador de rendimiento permiten el acceso de scripts y programas a los datos de rendimiento del sistema calculados por los proveedores de alto rendimiento existentes.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Clases de contador de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc66020fc7863153e3e663c7552ee6805b2a676772fdcbf01cd9683a9ec05486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701655"
---
# <a name="performance-counter-classes"></a>Clases de contador de rendimiento

Las clases de contador de rendimiento permiten el acceso de scripts y programas a los datos de rendimiento del sistema calculados por los proveedores de alto rendimiento existentes. Estas clases constan de clases de contador de rendimiento sin formato y clases de contador de rendimiento con formato.

Diferentes proveedores suministran datos de biblioteca de rendimiento a través de WMI. Los [proveedores WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) y [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) suministran clases para los contadores de rendimiento de la versión 1 y la versión [2.](/windows/desktop/PerfCtrs/performance-counters-portal) Estos proveedores mantienen la compatibilidad con las clases disponibles en sistemas operativos anteriores.

Las clases de esta sección son las clases base abstractas que se usan para crear clases de contador de rendimiento. Esta no es una lista completa de las clases que puede encontrar en el sistema operativo. Para obtener más información, vea [Bibliotecas de rendimiento y WMI.](/windows/desktop/WmiSdk/performance-libraries-and-wmi)

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**Win32 \_ Perf**](win32-perf.md)
</dt> <dd>

Clase base para las clases de contador de [**rendimiento Win32 \_ PerfRawData**](win32-perfrawdata.md) y [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).

</dd> <dt>

[**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md)
</dt> <dd>

una clase base abstracta para las clases de datos calculadas preinstaladas.

</dd> <dt>

[**Win32 \_ PerfRawData**](win32-perfrawdata.md)
</dt> <dd>

Clase base abstracta para todas las clases de contador de rendimiento sin procesar concretas.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases win32](win32-provider.md)
</dt> </dl>

 

 
