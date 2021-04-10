---
description: El tipo de contador de rendimiento designa una fórmula necesaria para obtener los contadores de rendimiento calculados. Estos son los mismos tipos de contador usados por la supervisión de rendimiento de Windows.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Tipos de contador de rendimiento de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155993"
---
# <a name="wmi-performance-counter-types"></a>Tipos de contador de rendimiento de WMI

El [tipo de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) de rendimiento designa una fórmula necesaria para obtener los contadores de rendimiento calculados. Estos son los mismos tipos de contador usados por la [supervisión de rendimiento](/windows/desktop/PerfCtrs/performance-counters-portal)de Windows. En las clases de rendimiento de WMI, los datos sin procesar de la fórmula de tipo de contador proceden de una clase [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y el resultado calculado se encuentra en la propiedad con el mismo nombre de la clase [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondiente.

Los tipos de contador aparecen como calificador de **contratipo** para las propiedades de las clases [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y como calificador **CookingType** para las propiedades de las clases [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .

Por ejemplo, la propiedad **AvgDiskBytesPerRead** de la clase [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) es el origen de datos sin procesar de la propiedad **AvgDiskBytesPerRead** de la clase [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), que contiene los mismos datos que se muestran en el monitor de sistema.

La lista siguiente organiza las descripciones de los tipos de contador por tipo funcional:

-   [Tipos de contador base](base-counter-types.md)
-   [Tipos de contadores de algoritmo básicos](basic-algorithm-counter-types.md)
-   [Tipos de contador del algoritmo Counter](counter-algorithm-counter-types.md)
-   [Tipos de contador no computacional](noncomputational-counter-types.md)
-   [Tipos de contador del algoritmo de temporizador de precisión](precision-timer-algorithm-counter-types.md)
-   [Tipos de contador del algoritmo de longitud de cola](queue-length-algorithm-counter-types.md)
-   [Tipos de contadores estadísticos](statistical-counter-types.md)
-   [Tipos de contadores del algoritmo Timer](timer-algorithm-counter-types.md)

 

 
