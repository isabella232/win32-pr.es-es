---
description: Establecimiento y recuperación de la posición
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Establecimiento y recuperación de la posición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805209"
---
# <a name="setting-and-retrieving-the-position"></a>Establecimiento y recuperación de la posición

El gráfico de filtro mantiene dos valores de posición: posición actual y posición de detención. Se definen de la siguiente manera:

-   Cuando se está ejecutando el gráfico, la posición actual es la posición de reproducción actual, con respecto al principio del origen. Cuando el gráfico está detenido o en pausa, la posición actual es el punto en el que se iniciará la transmisión por secuencias en el siguiente comando de ejecución.
-   La posición de detención es el punto en el que finalizará la secuencia. Cuando el gráfico llega a la posición de detención, no se transmiten más datos y el administrador de gráficos de filtros envía un evento de [**\_ finalización de EC**](ec-complete.md) . No obstante, el gráfico no cambia automáticamente a un estado detenido. Para obtener más información, consulte [responder a eventos](responding-to-events.md)).

Para recuperar estos valores, llame al método [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) . Los valores devueltos siempre son relativos al origen multimedia original. De forma predeterminada, los valores están en unidades de tiempo de referencia. En algunos casos, puede cambiar las unidades de tiempo; para obtener más información, vea [formatos de hora para comandos de búsqueda](time-formats-for-seek-commands.md).

Para buscar una nueva posición o establecer una nueva posición de detención, llame al método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , como se muestra en el ejemplo siguiente:


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> Un segundo es 10 millones unidades de tiempo de referencia. Para mayor comodidad, en el ejemplo se define este valor en un \_ segundo. Si usa la biblioteca de clases base de DirectShow, las unidades constantes tienen el mismo valor.

 

El parámetro *rtNow* especifica la nueva posición actual. El segundo parámetro es una marca que define cómo interpretar *rtNow*. En este ejemplo, la \_ marca AM Seek \_ AbsolutePositioning indica que *rtNow* especifica una posición absoluta en el origen. Por lo tanto, el gráfico de filtros buscará una posición de dos segundos desde el inicio de la secuencia. El parámetro *rtStop* proporciona la hora de detención. El último parámetro especifica que *rtStop* también es una posición absoluta.

Para especificar una posición relativa al valor de posición anterior, use la \_ marca AM \_ RelativePositioning Seek. Para dejar uno de los valores de posición sin modificar, use la \_ marca AM buscar \_ nopositioning. En ese caso, el parámetro de hora correspondiente puede ser **null** . El siguiente ejemplo busca hacia delante 10 segundos pero deja la posición de detención sin cambios:


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



Si el gráfico de filtros se detiene, el representador de vídeo no actualiza la imagen después de una operación de búsqueda. Para el usuario, aparecerá como si no se produjera la búsqueda. Para actualizar la imagen, Pause el gráfico después de la operación de búsqueda. Pausar las guías de gráficos un nuevo fotograma de vídeo para el representador de vídeo. Puede usar el método [**IMediaControl:: StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) , que pone en pausa el gráfico y, a continuación, lo detiene.

 

 



