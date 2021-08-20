---
description: Varios consumidores, como el consumidor de eventos de script activo o el consumidor de eventos de la línea de comandos, tienen propiedades de cadena con el calificador Template.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Uso de plantillas de cadena estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c60a28730b890a5e922489a47b5b382b545cd6712d61cb976e96b549039ef7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049943"
---
# <a name="using-standard-string-templates"></a>Uso de plantillas de cadena estándar

Varios consumidores, como el consumidor de eventos de script activo o el consumidor de eventos de la línea de comandos, tienen propiedades de cadena con el **calificador Template.** Estas propiedades usan plantillas de cadena estándar para construir una cadena configurada en parte por la instancia del consumidor y, en parte, por un evento. La estructura de una plantilla de cadena estándar es similar a la especificación de la variable de entorno Windows Microsoft.

En la lista siguiente se muestran algunos ejemplos del lenguaje de plantilla:

-   La cadena "Some text here" siempre genera la cadena "Some text here".
-   "%CPUUtilization%" siempre genera el valor de la propiedad **CPUUtilization** del evento que se entrega. Si la propiedad no es una cadena, se convierte en una cadena; por ejemplo, "90" o "TRUE".
-   "El uso de CPU de este procesador es %CPUUtilization% en este momento" inserta el valor de la propiedad **CPUUtilization** del evento en la cadena, generando algo parecido a "El uso de CPU de este procesador es 90 en este momento".
-   "%TargetInstance.CPUUtilization%" recupera el valor de la propiedad **CPUUtilization** en la instancia incrustada de la **propiedad TargetInstance.**
-   "%%" genera un único signo de %.
-   Si la propiedad que se recupera es una matriz, toda la matriz se genera con el formato siguiente: "(1,5,10,1024)". Si solo hay un elemento en la matriz, se omiten los paréntesis. Si no hay elementos en la matriz, se genera "()".
-   Si una propiedad es un objeto incrustado, se genera la representación MOF del objeto (similar al método [**IWbemClassObject::GetObjectText).**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext)
-   Si se solicita una propiedad de una matriz incrustada de objetos, se trata como una propiedad con un valor de matriz. Por ejemplo: %MyEvents.TargetInstance.DriverLetter% podría generar "("C:","D:")" si MyEvents es una matriz de eventos de modificación de instancias incrustadas.

## <a name="string-literals"></a>Literales de cadena

Todo lo que se encuentra dentro de un par de comillas se considera un literal de cadena y no se reemplazará.

En el ejemplo siguiente se muestra la cadena que el compilador ve para "El uso de CPU es %CPUUtilization%".

``` syntax
CPU utilization is %CPUUtilization%
```

Esta cadena genera la siguiente salida.

``` syntax
CPU utilization is 90
```

Por otro lado, el compilador ve la cadena "Cpu utilization is \\ "%CPUUtilization% "" como \\ se muestra a continuación.

``` syntax
CPU utilization is "%CPUUtilization%"
```

Esta cadena genera la siguiente salida, sin sustitución de variables.

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



