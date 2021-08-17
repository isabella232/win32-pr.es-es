---
description: Los monitores se pueden configurar mediante la interfaz Monitor de red usuario. Los usuarios finales pueden pasar criterios de configuración al monitor mediante un formulario HTML almacenado como un archivo HTM en la siguiente sub carpeta del SDK Monitor de red instalado.
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: Supervisar configuración (Monitor de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b55765774df3be2722c448a1af264162bcd9cdc51ac958cc555bf820d646b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364703"
---
# <a name="monitor-configuration-network-monitor"></a>Supervisar configuración (Monitor de red)

Los monitores se pueden configurar mediante la interfaz Monitor de red usuario. Los usuarios finales pueden pasar criterios de configuración al monitor mediante un formulario HTML almacenado como un archivo HTM en la siguiente sub carpeta del SDK Monitor de red instalado.

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

Cuando un usuario final selecciona el botón Establecer configuración del **monitor,** el explorador genera un mensaje HTML **POST,** que incluye los nombres y valores de todos los elementos del formulario HTML.

Cuando MCSVC llama al método [IMonitor::D oConfigure,](imonitor-doconfigure.md) el parámetro *pConfiguration* apunta a los datos del mensaje POST. El código de ejemplo siguiente proporciona un ejemplo de datos de mensaje POST:

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Estos datos se pasan como una cadena ASCII larga. La cadena tiene un aspecto bastante largo, tanto por su longitud como por la apariencia de secciones como %3A%5C y %0D%0A. Esta mentalidad se debe a HTML, que requiere que un método coloque todas las cadenas ANSI, DBCS y Unicode posibles en un formato ASCII. Por ejemplo, el método **DoConfigure** inserta ciertos caracteres, como la y comercial (&) delante de cada nombre de variable para identificarlo como un nombre de variable. %3A%5C es una forma codificada del carácter de dos puntos y %0D%0A indica un par de retorno de carro/de retorno de línea. El código de ejemplo siguiente proporciona el código HTML resultante tal como lo interpreta el monitor.

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



