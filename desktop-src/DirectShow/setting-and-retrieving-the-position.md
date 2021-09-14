---
description: Establecer y recuperar la posición
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Establecer y recuperar la posición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061605"
---
# <a name="setting-and-retrieving-the-position"></a>Establecer y recuperar la posición

El gráfico de filtro mantiene dos valores de posición: posición actual y posición de detenerse. Se definen de la siguiente manera:

-   Cuando se ejecuta el gráfico, la posición actual es la posición de reproducción actual, con respecto al principio del origen. Cuando el gráfico se detiene o se pausa, la posición actual es el punto donde se iniciará el streaming en el siguiente comando de ejecución.
-   La posición de detenerse es el punto donde finalizará la secuencia. Cuando el gráfico alcanza la posición de detenerse, no se transmiten más datos y el administrador de gráficos de filtro publica un [**evento EC \_ COMPLETE.**](ec-complete.md) (Sin embargo, el gráfico no cambia automáticamente a un estado detenido. Para obtener más información, vea [Responder a eventos](responding-to-events.md)).

Para recuperar estos valores, llame al [**método IMediaSeeking::GetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) Los valores devueltos siempre son relativos al origen multimedia original. De forma predeterminada, los valores están en unidades de tiempo de referencia. En algunos casos, puede cambiar las unidades de tiempo; Para obtener más información, vea [Time Formats For Seek Commands](time-formats-for-seek-commands.md).

Para buscar una nueva posición o establecer una nueva posición de detenerse, llame al método [**IMediaSeeking::SetPositions,**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) como se muestra en el ejemplo siguiente:


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
> Un segundo es 10 000 000 unidades de tiempo de referencia. Para mayor comodidad, en el ejemplo se define este valor como UN \_ SEGUNDO. Si usa la biblioteca de DirectShow base, la constante UNITS tiene el mismo valor.

 

El *parámetro rtNow* especifica la nueva posición actual. El segundo parámetro es una marca que define cómo interpretar *rtNow*. En este ejemplo, la marca AbsolutePositioning de AM SEEKING indica \_ \_ que *rtNow* especifica una posición absoluta en el origen. Por lo tanto, el gráfico de filtros buscará una posición a dos segundos del inicio de la secuencia. El *parámetro rtStop* proporciona la hora de detenerse. El último parámetro especifica que *rtStop* también es una posición absoluta.

Para especificar una posición con respecto al valor de posición anterior, use la marca RelativePositioning de AM \_ \_ SEEKING. Para dejar uno de los valores de posición sin cambios, use la marca AM \_ SEEKING \_ NoPositioning. En ese caso, el parámetro time correspondiente puede ser **NULL.** En el ejemplo siguiente se busca hacia delante en 10 segundos, pero deja la posición de detenerse sin cambios:


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



Si se detiene el gráfico de filtro, el representador de vídeo no actualiza la imagen después de una operación de búsqueda. Para el usuario, aparecerá como si la búsqueda no se hubiera hecho. Para actualizar la imagen, pause el gráfico después de la operación de búsqueda. Al pausar el gráfico, se muestra un nuevo fotograma de vídeo para el representador de vídeo. Puede usar el [**método IMediaControl::StopWhenReady,**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) que pausa el gráfico y lo detiene.

 

 



