---
description: Algunas fórmulas requieren una propiedad de contador y una propiedad base.
ms.assetid: c14be351-e712-40bd-bab7-5b9ef6cd8a00
ms.tgt_platform: multiple
title: Tipos de contador base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e481fbf093245813d0ce0de2b5f7906316c2378
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568077"
---
# <a name="base-counter-types"></a>Tipos de contador base

Algunas fórmulas requieren una propiedad de contador y una propiedad base. El valor base es el denominador de la fórmula para el tipo de contador. En las clases [de contadores de](/windows/desktop/CIMWin32Prov/performance-counter-classes) rendimiento de datos sin procesar derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), la propiedad base debe seguir inmediatamente a la propiedad counter. La propiedad base debe tener el mismo nombre que el contador anterior, con **\_ base** anexada.

Por ejemplo, la propiedad **AvgDiskBytesPerRead** de [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) contiene el valor sin procesar, en bytes, transferido desde el disco durante las operaciones de lectura. Tiene una propiedad base, **AvgDiskBytesPerRead \_ Base**, que representa el número acumulado de operaciones. Cuando WMI aplica la fórmula para el tipo de contador especificado, **PERF \_ AVERAGE \_ BASE**, **AvgDiskBytesPerRead** se divide por **AvgDiskBytesPerRead \_ Base** para generar el valor medio. Este valor aparece en el Monitor de sistema y se almacena en la propiedad [**\_ Win32 PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) correspondiente. Las propiedades base solo se usan en clases de datos sin procesar.

En las clases derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), el calificador **Counter** especifica la propiedad numerador en la clase sin formato y el calificador **Base** especifica la propiedad de denominador base.

En la tabla siguiente se enumeran los **valores constantes CounterType.**



| CounterType (constante)                                                                                      | Descripción                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ AVERAGE \_ BASE Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939458<br/>        | Valor base utilizado para calcular los tipos de contador **\_ PERF AVERAGE \_ TIMER** y **PERF \_ AVERAGE \_ BULK.**                                                                                             |
| [PERF \_ COUNTER \_ MULTI \_ BASE Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1107494144<br/> | Valor base usado para calcular los tipos de contadorES MULTI TIMER **PERF \_ COUNTER \_ \_**, **PERF \_ COUNTER MULTI TIMER \_ \_ \_ INV,** **PERF \_ 100NSEC \_ MULTI \_ TIMER** y **PERF \_ 100NSEC \_ MULTI TIMER \_ \_ INV.** |
| [PERF \_ LARGE \_ RAW \_ BASE Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939712<br/>     | Valor base encontrado en el cálculo de **PERF \_ RAW \_ FRACTION**, 64 bits.                                                                                                                         |
| [PERF \_ RAW \_ BASE Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939459<br/>            | Valor base utilizado para calcular el tipo **de contador PERF \_ RAW \_ FRACTION.**                                                                                                                           |
| [PERF \_ SAMPLE \_ BASE Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939457<br/>         | Valor base utilizado para calcular los tipos de contador **PERF \_ SAMPLE \_ COUNTER** y **PERF \_ SAMPLE \_ FRACTION.**                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contadores de rendimiento wmi](wmi-performance-counter-types.md)
</dt> <dt>

[Tipos de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))
</dt> </dl>

 

