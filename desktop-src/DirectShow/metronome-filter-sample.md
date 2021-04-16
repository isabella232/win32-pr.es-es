---
description: Ejemplo de filtro de metrónomo
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Ejemplo de filtro de metrónomo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686344"
---
# <a name="metronome-filter-sample"></a>Ejemplo de filtro de metrónomo

## <a name="description"></a>Descripción

Este filtro de ejemplo muestra cómo implementar un reloj de referencia. El filtro usa la entrada de micrófono predeterminada para escuchar picos de audio (como clics, clapss de mano o tos), que usa para determinar la velocidad de reloj.

## <a name="usage"></a>Uso

Compile el proyecto de ejemplo y copie el archivo DLL de filtro (Metronom.ax) en el directorio del sistema de Windows. Ejecute el archivo metrónomo. reg para registrar el archivo DLL.

Para usar el filtro:

1.  Cree un gráfico de filtro en GraphEdit que representa una secuencia de vídeo.
2.  Elimine las secuencias de audio representadas.
3.  Agregue el filtro metrónomo al gráfico. Aparece en la categoría filtros de DirectShow.
4.  Ejecute el gráfico. El vídeo empezará a reproducirse a velocidad normal.
5.  Clap sus manos o use un metrónomo para establecer una nueva velocidad.

## <a name="programming-notes"></a>Notas de programación

Este filtro solo funciona para vídeo. El representador de audio no es capaz de sincronizar con diferentes velocidades de reloj.

Si Clap 92 veces por minuto (una vez cada ~ 652 MS), el vídeo se reproducirá a la tarifa normal. Puede cambiar este valor predeterminado cambiando el valor de la constante `BPM` en metrónomo. cpp.

Si detiene aplausos durante un período de tiempo y, a continuación, vuelve a iniciar aplausos, debe comenzar de nuevo con la misma velocidad o el filtro lo omitirá. Además, la velocidad de reproducción de vídeo está limitada por la velocidad de la CPU. Si supera el límite durante un período de tiempo, el filtro dejará de responder a los cambios de velocidad. Si esto ocurre, detenga el gráfico y reinícielo.

Si implementa su propio reloj, las reglas más importantes son que los relojes de referencia no deben ir hacia atrás. Es decir, nunca deben notificar un valor de tiempo menor que el valor de hora anterior.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ \] raíz del SDK* \\ \\ \\ filtros DirectShow de multimedia \\ \\ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> <dt>

[Ejemplos de DirectShow](directshow-samples.md)
</dt> </dl>

 

 



