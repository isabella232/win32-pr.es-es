---
description: Aunque se recomienda que los proveedores usen nombres de instancia únicos, no todos los proveedores lo hacen.
ms.assetid: 3c8fcb8d-2ea4-4b24-b649-7bd375c1133d
title: Control de nombres de instancia duplicados
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: f58f6ed11951c7b66951f5154009127c5029de3760a9419a7c9716781be8234f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144008"
---
# <a name="handling-duplicate-instance-names"></a>Control de nombres de instancia duplicados

Aunque se recomienda encarecidamente a los proveedores que usen nombres de instancia únicos, no todos los proveedores lo hacen. La convención para mostrar nombres de instancia duplicados es anexar un carácter y un número de serie al nombre de instancia, excepto la `#` primera aparición del nombre. Por ejemplo, si hay tres instancias de en un ejemplo, los tres nombres se muestran `svchost` `svchost` como , y `svchost#1` `svchost#2` .

Desafortunadamente, esta convención no resuelve completamente el problema. Los números de serie se asignan en función del orden en el que aparece un nombre de instancia determinado en una muestra, y este orden puede ser incoherente de ejemplo a ejemplo. Por ejemplo, el ejemplo A podría ver `svchost` (PID 100), `svchost#1` (PID 200) y `svchost#2` (PID 300). A continuación, si el svchost con PID 100 se apaga, el ejemplo siguiente vería `svchost` (PID 200) y `svchost#1` (PID 300). La lógica de coincidencia básica intentaría hacer coincidir las estadísticas del ejemplo A (de PID 200) con las estadísticas de la muestra `svchost#1` B (de PID 300), lo que daría lugar a resultados no válidos para el ejemplo B. Los errores se producen cuando una nueva instancia no única aparece en una muestra o cuando una instancia no única deja de aparecer en una muestra (a menos que la instancia agregada o eliminada sea la `svchost#1` última).

## <a name="process-counterset"></a>Contador de procesos

Este problema es especialmente problemático para el contraconjunto porque solo usa el nombre EXE del proceso como nombre de instancia aunque el nombre `Process` EXE no sea único. El comportamiento predeterminado del conjunto `Process` de contadores en Windows no se puede cambiar debido a problemas de compatibilidad.

Puede modificar el comportamiento de los conjuntos de contadores y para usar nombres de instancia únicos estableciendo los valores del Registro `Process` o en la clave del `Thread` `ProcessNameFormat` `ThreadNameFormat` `HKLM\System\CurrentControlSet\Services\Perfproc\Performance` Registro.

> [!CAUTION]
> Habilitar nombres de instancia únicos para el contraconjunto puede hacer que algunos programas se comporten incorrectamente, ya que muchos programas esperan el patrón de nomenclatura no `Process` único. Por ejemplo, un programa que busca una instancia con un nombre EXE conocido específico ya no podrá encontrar esa instancia después de habilitar nombres de instancia únicos.

El tipo de registro para estos valores es `REG_DWORD` . Al establecer el valor en , se anexa el identificador de proceso (PID) al nombre de la instancia de proceso y el identificador de subproceso (TID) al nombre de la `2` instancia del subproceso. Para deshabilitar esta característica, establezca el valor en 1 o elimine el valor.
