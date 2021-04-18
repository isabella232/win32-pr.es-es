---
description: Aunque se recomienda que los proveedores utilicen nombres de instancia únicos, no todos los proveedores.
ms.assetid: 3c8fcb8d-2ea4-4b24-b649-7bd375c1133d
title: Administrar nombres de instancia duplicados
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 220e5d7d0181a79c1d1415486cc946d484e11952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667325"
---
# <a name="handling-duplicate-instance-names"></a>Administrar nombres de instancia duplicados

Aunque se recomienda encarecidamente que los proveedores utilicen nombres de instancia únicos, no todos los proveedores. La Convención para mostrar los nombres de instancia duplicados es anexar un `#` carácter y un número de serie al nombre de instancia, excepto en el caso de la primera aparición del nombre. Por ejemplo, si hay tres instancias de `svchost` en un ejemplo, los tres nombres se muestran como `svchost` , `svchost#1` y `svchost#2` .

Desafortunadamente, esta Convención no resuelve completamente el problema. Los números de serie se asignan en función del orden en el que aparece un nombre de instancia determinado en un ejemplo y este orden puede ser incoherente desde el ejemplo al ejemplo. Por ejemplo, el ejemplo A podría ver `svchost` (pid 100), `svchost#1` (PID 200) y `svchost#2` (PID 300). Después, si svchost con PID 100 se cierra, el ejemplo siguiente verá `svchost` (pid 200) y `svchost#1` (PID 300). La lógica de coincidencia básica intentaría hacer coincidir las estadísticas de ejemplo A `svchost#1` (desde pid 200) con las estadísticas de la muestra b `svchost#1` (desde el PID 300), lo que da lugar a resultados no válidos para el ejemplo b. los errores se producen cuando se muestra una nueva instancia no única en un ejemplo o cuando una instancia no única se detiene en un ejemplo (a menos que la instancia

## <a name="process-counterset"></a>Procesar CounterSet

Este problema es especialmente problemático para `Process` CounterSet porque solo usa el nombre del archivo exe del proceso como el nombre de la instancia aunque el nombre del archivo exe no sea único. No se puede cambiar el comportamiento predeterminado del `Process` CounterSet en Windows debido a problemas de compatibilidad.

Puede modificar el comportamiento de los `Process` `Thread` contraconjuntos y para usar nombres de instancia únicos mediante el establecimiento de los `ProcessNameFormat` `ThreadNameFormat` valores del registro o en la `HKLM\System\CurrentControlSet\Services\Perfproc\Performance` clave del registro.

> [!CAUTION]
> La habilitación de nombres de instancia únicos para `Process` CounterSet puede hacer que algunos programas se comporten de forma incorrecta, ya que muchos programas esperan el patrón de nomenclatura no único. Por ejemplo, un programa que busque una instancia con un nombre de archivo ejecutable conocido específico ya no podrá encontrar esa instancia después de habilitar los nombres de instancia únicos.

El tipo de registro para estos valores es `REG_DWORD` . Al establecer el valor en, se `2` anexa el identificador de proceso (PID) al nombre de instancia de proceso y el identificador de subproceso (TID) al nombre de instancia de subproceso. Para deshabilitar esta característica, establezca el valor en 1 o elimine el valor.
