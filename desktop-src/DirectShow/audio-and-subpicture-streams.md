---
description: Secuencias de audio y subimagen
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Secuencias de audio y subimagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495653"
---
# <a name="audio-and-subpicture-streams"></a>Secuencias de audio y subimagen

Un disco DVD-Video puede tener hasta ocho flujos de audio, numerados de cero a siete, cada uno con hasta seis canales discretos. (Tenga en cuenta que los flujos de audio y de subimagen se numeran desde cero, mientras que los títulos, los ángulos y los niveles parentales se numeran a partir de uno). Solo se puede seleccionar una de estas secuencias en un momento dado. En el caso de las subimágenes, hay hasta 32 secuencias disponibles, aunque solo se puede activar un flujo en un momento dado. Normalmente, los discos se crean con secuencias de audio y subimágenes predeterminadas, pero una aplicación puede permitir a los usuarios ver una lista de todas las secuencias disponibles y seleccionar la del lenguaje que prefieran. Los pasos básicos de este proceso son los mismos para las secuencias de audio y de subimagen.

1.  Determine el número de secuencias disponibles para un título.
2.  Recorra en iteración los flujos y recupere los atributos de secuencia para cada uno.
3.  Recupera el código de idioma del identificador de configuración regional (LCID) devuelto y crea una cadena legible para el usuario.
4.  Rellene un cuadro de lista u otro control de la interfaz de usuario para permitir que el usuario seleccione una secuencia preferida.

En la aplicación de ejemplo de DVD, el método CAudioLangDlg:: MakeAudioStreamList de DIALOGS. cpp muestra los pasos básicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



