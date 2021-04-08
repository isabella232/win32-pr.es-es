---
description: Varios consumidores, como el consumidor de eventos de script activo o el consumidor de eventos de línea de comandos, tienen propiedades de cadena con el calificador de plantilla.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Usar plantillas de cadena estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911485"
---
# <a name="using-standard-string-templates"></a>Usar plantillas de cadena estándar

Varios consumidores, como el consumidor de eventos de script activo o el consumidor de eventos de línea de comandos, tienen propiedades de cadena con el calificador de **plantilla** . Estas propiedades usan plantillas de cadena estándar para construir una cadena que está configurada en la parte por la instancia del consumidor y en parte por un evento. La estructura de una plantilla de cadena estándar es similar a la especificación de variable de entorno de Microsoft Windows.

En la lista siguiente se muestran algunos ejemplos del lenguaje de la plantilla:

-   La cadena "Some Text here" siempre genera la cadena "Some Text here".
-   "% Gráfico%" siempre genera el valor de la propiedad **gráfico** del evento que se va a entregar. Si la propiedad no es una cadena, se convierte en una cadena; por ejemplo, "90" o "TRUE".
-   "El uso de CPU de este procesador es% gráfico% en este momento" inserta el valor de la propiedad **gráfico** del evento en la cadena, lo que genera algo parecido a "el uso de CPU de este procesador es 90 en este momento".
-   "% TargetInstance. gráfico%" recupera el valor de la propiedad **gráfico** en la instancia insertada de la propiedad **TargetInstance** .
-   "%%" genera un único signo de%.
-   Si la propiedad que se va a recuperar es una matriz, toda la matriz se produce con el siguiente formato: "(1, 5, 10, 1024)". Si solo hay un elemento en la matriz, se omiten los paréntesis. Si no hay ningún elemento en la matriz, se genera "()".
-   Si una propiedad es un objeto incrustado, se genera la representación MOF del objeto (similar al método [**IWbemClassObject:: GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) ).
-   Si se solicita una propiedad de una matriz incrustada de objetos, se trata como una propiedad con un valor de matriz. Por ejemplo:% DoEvents. TargetInstance. DriverLetter% podría producir ' ("C:", "D:") ' si DoEvents es una matriz de eventos de modificación de instancia incrustados.

## <a name="string-literals"></a>Literales de cadena

Todo lo que se encuentre dentro de un par de Comillas se considera un literal de cadena y no se reemplazará.

En el ejemplo siguiente se muestra la cadena que el compilador ve para "el uso de la CPU es% gráfico%".

``` syntax
CPU utilization is %CPUUtilization%
```

Esta cadena genera el siguiente resultado.

``` syntax
CPU utilization is 90
```

Por otro lado, el compilador verá la cadena "el uso de CPU es \\ "% gráfico% \\ "" como se indica a continuación.

``` syntax
CPU utilization is "%CPUUtilization%"
```

Esta cadena genera el siguiente resultado, sin sustitución de variables.

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



