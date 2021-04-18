---
description: Reproducir flujos de audio de karaoke
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Reproducir flujos de audio de karaoke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907bfa3e359915cf537de75cdc739630fe607d97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677146"
---
# <a name="playing-karaoke-audio-streams"></a>Reproducir flujos de audio de karaoke

El navegador de DVD puede reproducir discos DVD-Video con secuencias de audio de karaoke, pero la reproducción de karaoke también requiere un descodificador que admita la combinación de Karaoke de multicanal. En concreto, el descodificador debe admitir el [**conjunto de propiedades de Karaoke de DVD**](dvd-karaoke-property-set.md) ( \_ propiedad \_ DVDKARAOKE).

Los discos de karaoke son un tipo de disco DVD-Video y tienen la misma estructura de navegación. Las canciones suelen tener el formato de títulos y los títulos se pueden agrupar en conjuntos de títulos basados en el rendimiento, estilo musical u otros criterios. La diferencia principal entre el karaoke y otros tipos de DVD-Videos es la secuencia de audio. Los discos de karaoke contienen audio multicanal, normalmente Dolby AC-3. Los canales 0 y 1 siempre contienen la música instrumental de fondo, mientras que los canales del 2 al 5 pueden contener cualquier combinación de voces guía, Melodies de guía y efectos sonoros. Una aplicación de Karaoke puede controlar el volumen y el altavoz de destino para cada canal auxiliar.

Cuando el navegador de DVD detecta el contenido de karaoke en un disco y entra en el modo de karaoke, informa al descodificador, que debe silenciar los tres canales superiores (los canales auxiliares) hasta que una aplicación Active explícitamente cualquiera de ellos. Las tareas básicas de una aplicación de karaoke son:

1.  Determine el número de canales auxiliares y su contenido mediante métodos [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) .
2.  Proporcione una interfaz de usuario que muestre el contenido del canal y permita a los usuarios activar o desactivar cualquier canal auxiliar en cualquier momento, mediante [**IDvdControl2:: SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).

Estos pasos se ilustran en la aplicación de ejemplo de DVD en DVDCore. cpp en el método **GetAudioAttributes** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



