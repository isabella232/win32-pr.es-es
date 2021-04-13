---
description: Algunas fórmulas requieren una propiedad de contador y una propiedad base.
ms.assetid: c14be351-e712-40bd-bab7-5b9ef6cd8a00
ms.tgt_platform: multiple
title: Tipos de contador base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e481fbf093245813d0ce0de2b5f7906316c2378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278412"
---
# <a name="base-counter-types"></a>Tipos de contador base

Algunas fórmulas requieren una propiedad de contador y una propiedad base. El valor base es el denominador en la fórmula para el tipo de contador. En [las clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de datos sin procesar derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), la propiedad base debe seguir inmediatamente a la propiedad Counter. La propiedad base debe tener el mismo nombre que el contador anterior, con **\_ base** anexada.

Por ejemplo, la propiedad **AvgDiskBytesPerRead** de [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) contiene el valor sin formato, en bytes, transferido desde el disco durante las operaciones de lectura. Tiene una propiedad base, **AvgDiskBytesPerRead \_ base**, que representa el número acumulado de operaciones. Cuando WMI aplica la fórmula para el tipo de contador especificado **, \_ media de \_ base de rendimiento**, **AvgDiskBytesPerRead** se divide por **AvgDiskBytesPerRead \_ base** para generar el valor medio. Este valor aparece en el monitor de sistema y se almacena en la propiedad [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) correspondiente. Las propiedades base solo se usan en las clases de datos sin procesar.

En las clases derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), el calificador de **contador** especifica la propiedad Numerator en la clase sin formato y el calificador **base** especifica la propiedad del denominador base.

En la tabla siguiente se enumeran los valores constantes de **tipo** de valor.



| Contratipo (constante)                                                                                      | Descripción                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rendimiento \_ de PROMEDIO \_ ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal de base 1073939458<br/>        | Valor base que se usa para calcular el **\_ \_ temporizador de promedio de rendimiento** y los tipos de contador de **\_ promedio \_ de rendimiento** .                                                                                             |
| [Rendimiento \_ de Recuento decimal de \_ varias \_ bases](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1107494144<br/> | Valor base que se usa para calcular los tipos de contador de **\_ contadores de rendimiento \_ varios \_ temporizadores**, **\_ contadores de rendimiento \_ \_ \_** de varios temporizadores, **\_ 100NSEC \_ \_** y perf **\_ \_ \_ \_ 100NSEC** . |
| [Rendimiento \_ de \_ \_ Base decimal grande sin formato](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939712<br/>     | Valor base encontrado en el cálculo de **la \_ \_ fracción sin procesar de rendimiento**, 64 bits.                                                                                                                         |
| [Rendimiento \_ de Decimal \_ base sin formato](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939459<br/>            | Valor base usado para calcular el tipo de contador de **\_ \_ fracción sin formato de rendimiento** .                                                                                                                           |
| [Rendimiento \_ de EJEMPLO \_ ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal de base 1073939457<br/>         | Valor base que se usa para calcular el **\_ \_ contador de ejemplo Perf** y los tipos de contador de **fracción de \_ ejemplo \_ de rendimiento** .                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md)
</dt> <dt>

[Tipos de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))
</dt> </dl>

 

