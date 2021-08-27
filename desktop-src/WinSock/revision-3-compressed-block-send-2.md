---
description: En esta versión de la aplicación, se usa un envío de bloque comprimido de los datos. Este cambio da como resultado una mejora significativa del rendimiento.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Revisión tres: Envío de bloque comprimido'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bba84010a09755c5b978665cbd8aa1b29068ec42294ab7b1e499c631fc6b472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121285"
---
# <a name="revision-three-compressed-block-send"></a>Revisión tres: Envío de bloque comprimido

En esta versión de la aplicación, se usa un envío de bloque comprimido de los datos. Este cambio da como resultado una mejora significativa del rendimiento.


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

-   Las actualizaciones de celdas ya no se serializan.
-   Puesto que se usa un envío de bloques, la aplicación ya no es de chat.
-   Se usa la compresión de datos, lo que da lugar a una aplicación menos fat.

Todavía hay un problema con esta versión de la aplicación. existe el riesgo de interbloqueo, ya que se usa un envío grande sin recibir. El servidor envía un byte por cada 3 bytes recibidos. Esto podría provocar un interbloqueo si el tamaño del búfer de recepción es inferior a 1000 bytes para esta aplicación de ejemplo.

## <a name="key-performance-metrics"></a>Métricas clave de rendimiento

Las siguientes métricas de rendimiento se expresan en Tiempo de ida y vuelta (RTT), Goodput y Sobrecarga de protocolo. Consulte el [tema Terminología de red](network-terminology-2.md) para obtener una explicación de estos términos.

Esta versión refleja las siguientes métricas de rendimiento:

-   Tiempo de celda: .002 \* RTT
-   Goodput: 2 kilobytes/RTT
-   Sobrecarga de protocolo: 14 %

De la sobrecarga del 14 %, el 6 % es de los encabezados Ethernet y el otro 8 % es del inicio y desmontaje de la conexión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejora de una aplicación lenta](improving-a-slow-application-2.md)
</dt> <dt>

[Terminología de red](network-terminology-2.md)
</dt> <dt>

[La versión de línea de base: una aplicación de muy bajo rendimiento](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisión 1: Limpieza de lo obvio](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisión 2: Rediseño para menos conectos](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Mejoras futuras](future-improvements-2.md)
</dt> </dl>

 

 



