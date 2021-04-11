---
description: En esta revisión, se rediseña la aplicación de ejemplo para eliminar las conexiones innecesarias.
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 'Revisión 2: rediseño para menos conexiones'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155873"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a>Revisión 2: rediseño para menos conexiones

En esta revisión, se rediseña la aplicación de ejemplo para eliminar las conexiones innecesarias.

> [!WARNING]
> En este ejemplo de la aplicación también se proporciona un rendimiento insuficiente intencionadamente, con el fin de mostrar las mejoras de rendimiento posibles con los cambios en el código. No use este ejemplo de código en la aplicación; solo es para fines ilustrativos.

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a>Problemas restantes

Los cambios en la revisión dos rediseñaron la aplicación para realizar solo una conexión por actualización. La aplicación todavía incluye los siguientes problemas de rendimiento:

-   La aplicación todavía se serializa y conversa.
-   La aplicación todavía tiene un diseño FAT; Hay muchos envíos que no requieren ninguna operación en este diseño.
-   Los envíos siguen siendo solo 3 bytes, que es un flujo deficiente.

## <a name="key-performance-metrics"></a>Métricas de rendimiento clave

Las siguientes métricas de rendimiento se expresan en tiempo de ida y vuelta (RTT), Goodput y sobrecarga del protocolo. Consulte el tema [terminología de red](network-terminology-2.md) para obtener una explicación de estos términos.

Esta versión refleja las siguientes métricas de rendimiento:

-   Tiempo de la celda: 1 \* RTT
-   Goodput: 4 bytes/RTT
-   Sobrecarga de protocolo: 96,8%

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

[Revisión 3: envío de bloque comprimido](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Mejoras futuras](future-improvements-2.md)
</dt> </dl>

 

 



