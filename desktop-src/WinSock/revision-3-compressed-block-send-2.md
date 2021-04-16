---
description: En esta versión de la aplicación, se usa un bloque comprimido que envía los datos. Este cambio produce una mejora significativa del rendimiento.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Revisión 3: envío de bloque comprimido'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657579406ed31fce08239c518a6910f525219fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706188"
---
# <a name="revision-three-compressed-block-send"></a>Revisión 3: envío de bloque comprimido

En esta versión de la aplicación, se usa un bloque comprimido que envía los datos. Este cambio produce una mejora significativa del rendimiento.


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a>Cambios en esta versión

Esta versión refleja los cambios siguientes:

-   Las actualizaciones de celda ya no se serializan.
-   Dado que se usa un bloque de envío, la aplicación ya no está conversando.
-   Se utiliza la compresión de datos, lo que da lugar a una aplicación menos FAT.

Todavía hay un problema con esta versión de la aplicación; el riesgo de interbloqueo existe porque se usa un envío grande sin recibir. El servidor envía un byte por cada 3 bytes recibidos. Esto podría producir un interbloqueo si el tamaño del búfer de recepción es inferior a 1000 bytes para esta aplicación de ejemplo.

## <a name="key-performance-metrics"></a>Métricas de rendimiento clave

Las siguientes métricas de rendimiento se expresan en tiempo de ida y vuelta (RTT), Goodput y sobrecarga del protocolo. Consulte el tema [terminología de red](network-terminology-2.md) para obtener una explicación de estos términos.

Esta versión refleja las siguientes métricas de rendimiento:

-   Hora de la celda:. 002 \* RTT
-   Goodput: 2 kilobytes/RTT
-   Sobrecarga de protocolos: 14%

En el 14% de la sobrecarga, el 6% se deriva de los encabezados Ethernet y el otro 8% proviene del inicio y el desmontaje de la conexión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejora de una aplicación lenta](improving-a-slow-application-2.md)
</dt> <dt>

[Terminología de red](network-terminology-2.md)
</dt> <dt>

[La versión de línea base: una aplicación con un rendimiento muy deficiente](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisión 1: limpieza del manifiesto](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisión 2: rediseño para menos conexiones](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Mejoras futuras](future-improvements-2.md)
</dt> </dl>

 

 



