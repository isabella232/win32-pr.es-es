---
description: Representan diferencias entre las muestras a lo largo del tiempo y, a menudo, usan un valor base para el cálculo.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmo básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706934"
---
# <a name="basic-algorithm-counter-types"></a>Tipos de contadores de algoritmo básicos

Normalmente, los tipos de contadores de algoritmos básicos representan diferencias entre muestras a lo largo del tiempo y, a menudo, usan un valor base para el cálculo. Por ejemplo, la propiedad **PercentFreeSpace** de la clase [**Win32 \_ PerfFormattedData \_ perfdisk \_ DiscoFísico**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representa la relación entre el espacio libre disponible en la unidad de disco físico y el espacio utilizable total proporcionado por la unidad de disco físico seleccionada. Esta clase también contiene el valor base **PercentFreeSpace \_ base**. El porcentaje de espacio libre en disco se obtiene dividiendo **PercentFreeSpace** por **PercentFreeSpace \_ base** y multiplicando por 100%.

Se proporcionan los algoritmos básicos de la tabla siguiente.



| Contratipo (constante)                                                                                    | Descripción                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rendimiento \_ de \_Fracción](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 537003008<br/>       | Relación entre un subconjunto y su conjunto como porcentaje. Este tipo de contador muestra únicamente el porcentaje actual, no un promedio a lo largo del tiempo.                                    |
| [Rendimiento \_ de EJEMPLO de \_ fracción](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 549585920<br/>    | Proporción media de aciertos de todas las operaciones durante los dos últimos intervalos de muestra. Este tipo de contador requiere una propiedad base con el \_ tipo de contador base de ejemplo de rendimiento \_ . |
| [Rendimiento \_ de CONTADOR decimal \_ DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4195328<br/>        | Este tipo de contador muestra la variación del atributo que se ha medido entre los dos intervalos de muestra más recientes.                                                         |
| [Rendimiento \_ de CONTADOR \_ de \_ diferencia Decimal grande](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4195584<br/> | Igual que \_ \_ la diferencia de contador de rendimiento, pero una representación de 64 bits para valores mayores.                                                                                        |
| [Rendimiento \_ de Decimal de \_ tiempo transcurrido](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))807666944<br/>       | Tiempo total entre el inicio del proceso y el momento en que se calcula este valor.                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

