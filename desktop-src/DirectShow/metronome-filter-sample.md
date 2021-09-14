---
description: Ejemplo de filtro de metrónoma
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Ejemplo de filtro de metrónoma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072161"
---
# <a name="metronome-filter-sample"></a>Ejemplo de filtro de metrónoma

## <a name="description"></a>Descripción

Este filtro de ejemplo muestra cómo implementar un reloj de referencia. El filtro usa la entrada de micrófono predeterminada para escuchar picos de audio (como clics, pulsaciones de mano o pórtas), que usa para determinar la velocidad del reloj.

## <a name="usage"></a>Uso

Compile el proyecto de ejemplo y copie el archivo DLL de filtro (Metronom.ax) en el Windows del sistema. Ejecute el archivo Metronom.reg para registrar el archivo DLL.

Para usar el filtro:

1.  Cree un gráfico de filtros en GraphEdit que represente una secuencia de vídeo.
2.  Elimine las secuencias de audio que se represente.
3.  Agregue el filtro Metronome al gráfico. Aparece en la categoría DirectShow filtros.
4.  Ejecute el gráfico. El vídeo comenzará a reproducirse a velocidad normal.
5.  Póntese las manos o use un metrónoma para establecer una nueva velocidad.

## <a name="programming-notes"></a>Notas de programación

Este filtro solo funciona para vídeo. El representador de audio no es capaz de sincronizarse con velocidades de reloj radicalmente diferentes.

Si se pesquisa 92 veces por minuto (una vez cada ~652 ms), el vídeo se reproducirá a la velocidad normal. Puede cambiar este valor predeterminado cambiando el valor de la constante `BPM` en Metronom.cpp.

Si deja de entrelazar durante un período de tiempo y, a continuación, vuelve a empezar a entrelazar, debe empezar de nuevo aproximadamente a la misma velocidad o el filtro lo omitirá. Además, la velocidad de reproducción de vídeo está limitada por la velocidad de CPU. Si supera el límite durante cualquier período de tiempo, el filtro dejará de responder a los cambios de velocidad. Si esto sucede, detenga el gráfico y reinicie.

Si implementa su propio reloj, las reglas más importantes es que los relojes de referencia no deben retroceder. Es decir, nunca deben notificar un valor de hora menor que el valor de hora anterior.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente [de Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: *\[ SDK Root \]* Samples Multimedia DirectShow Filters \\ \\ \\ \\ \\ Metronome.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> <dt>

[DirectShow Muestras](directshow-samples.md)
</dt> </dl>

 

 



