---
description: Las clases de contador de rendimiento permiten el acceso de scripts y programas a los datos de rendimiento del sistema calculados por proveedores de alto rendimiento existentes.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Clases de contador de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907539"
---
# <a name="performance-counter-classes"></a>Clases de contador de rendimiento

Las clases de contador de rendimiento permiten el acceso de scripts y programas a los datos de rendimiento del sistema calculados por proveedores de alto rendimiento existentes. Estas clases se componen de clases de contador de rendimiento sin procesar y clases de contador de rendimiento con formato.

Los diferentes proveedores proporcionan datos de la biblioteca de rendimiento a través de WMI. Los proveedores [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) y [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) proporcionan clases para los [contadores de rendimiento](/windows/desktop/PerfCtrs/performance-counters-portal)de la versión 1 y la versión 2. Estos proveedores mantienen la compatibilidad con las clases disponibles en los sistemas operativos anteriores.

Las clases de esta sección son las clases base abstractas utilizadas para crear clases de contador de rendimiento. Esta no es una lista completa de las clases que se pueden encontrar en el sistema operativo. Para obtener más información, consulte [bibliotecas de rendimiento y WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**Rendimiento de Win32 \_**](win32-perf.md)
</dt> <dd>

La clase base para las clases de contador de rendimiento [**Win32 \_ PerfRawData**](win32-perfrawdata.md) y [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).

</dd> <dt>

[**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md)
</dt> <dd>

una clase base abstracta para las clases de datos calculadas preinstaladas.

</dd> <dt>

[**Win32 \_ PerfRawData**](win32-perfrawdata.md)
</dt> <dd>

La clase base abstracta para todas las clases de contador de rendimiento sin procesar concretas.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases Win32](win32-provider.md)
</dt> </dl>

 

 
