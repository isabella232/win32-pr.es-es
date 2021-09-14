---
description: Reproducir audio de audio Secuencias
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Reproducir audio de audio Secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907bfa3e359915cf537de75cdc739630fe607d97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060986"
---
# <a name="playing-karaoke-audio-streams"></a>Reproducir audio de audio Secuencias

El navegador de DVD puede reproducir DVD-Video discos con secuencias de audio de audio de audio, pero la reproducción de audio también requiere un descodificador que admita la mezcla multicanal de audio. En concreto, el descodificador debe admitir el conjunto de propiedades [**DVD Dvd Dvd (AM**](dvd-karaoke-property-set.md) \_ PROPERTY \_ DVDKARAOKE).

Los discos de Final son un tipo DVD-Video disco y tienen la misma estructura de navegación. Por lo general, las canciones tienen el formato de títulos y los títulos se pueden agrupar en conjuntos de títulos en función del rendimiento, el estilo música u otros criterios. La principal diferencia entre ambos tipos de DVD-Videos es la secuencia de audio. Todos los discos de Disco duro contienen audio multicanal, normalmente Dolby AC-3. Los canales 0 y 1 siempre contienen la música instrumental de fondo, mientras que los canales del 2 al 5 pueden contener cualquier combinación de voces de guía, músicas de guía y efectos de sonido. Una aplicación de punto de conexión puede controlar el volumen y el altavoz de destino para cada canal auxiliar.

Cuando el navegador de DVD detecta contenido de canal en un disco y entra en modo de vídeo, informa al descodificador, que, a continuación, debe silenciar los tres canales superiores (los canales auxiliares) hasta que una aplicación haya activado explícitamente alguno de ellos o todos ellos. Las tareas básicas de una aplicación son:

1.  Determine el número de canales auxiliares y su contenido mediante [**métodos IDvdInfo2.**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)
2.  Proporcione una interfaz de usuario que muestre el contenido del canal y permita a los usuarios activar o desactivar cualquier canal auxiliar en cualquier momento, mediante [**IDvdControl2::SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).

Estos pasos se ilustran en la aplicación DVD Sample de DVDCore.cpp en el **método GetAudioAttributes.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



