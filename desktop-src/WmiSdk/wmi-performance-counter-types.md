---
description: El tipo de contador de rendimiento designa una fórmula necesaria para obtener contadores de rendimiento calculados. Estos son los mismos tipos de contador que usa Windows supervisión del rendimiento.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Tipos de contadores de rendimiento wmi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889164"
---
# <a name="wmi-performance-counter-types"></a>Tipos de contadores de rendimiento wmi

El tipo [de contador de](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) rendimiento designa una fórmula necesaria para obtener contadores de rendimiento calculados. Estos son los mismos tipos de contador que usa Windows [supervisión de rendimiento.](/windows/desktop/PerfCtrs/performance-counters-portal) En las clases de rendimiento wmi, los datos sin procesar de la fórmula de tipo de contador proceden de una clase [**\_ PerfRawData win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y el resultado calculado se encuentra en la propiedad con el mismo nombre de una clase [**\_ PerfFormattedData correspondiente de Win32.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

Los tipos de contador aparecen como calificador **CounterType** para las propiedades de las clases [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y como calificador **Desconfiado** para las propiedades de las clases [**\_ PerfFormattedData de Win32.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

Por ejemplo, la propiedad **AvgDiskBytesPerRead** de la clase [**LogicalDisk \_ PerfRawData \_ \_ PerfDisk de Win32**](./retrieving-raw-and-formatted-performance-data.md) es el origen de datos sin procesar de la propiedad **AvgDiskBytesPerRead** de la clase [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk,**](./retrieving-raw-and-formatted-performance-data.md)que contiene los mismos datos que se muestran en el Monitor del sistema.

En la lista siguiente se organizan las descripciones de tipos de contador por tipo funcional:

-   [Tipos de contador base](base-counter-types.md)
-   [Tipos de contadores de algoritmos básicos](basic-algorithm-counter-types.md)
-   [Tipos de contadores de algoritmos de contador](counter-algorithm-counter-types.md)
-   [Tipos de contadores no superáutales](noncomputational-counter-types.md)
-   [Tipos de contadores de algoritmo de temporizador de precisión](precision-timer-algorithm-counter-types.md)
-   [Tipos de contadores de algoritmo de longitud de cola](queue-length-algorithm-counter-types.md)
-   [Tipos de contador estadísticos](statistical-counter-types.md)
-   [Tipos de contadores de algoritmos de temporizador](timer-algorithm-counter-types.md)

 

 
