---
description: Audio y subpicture Secuencias
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Audio y subpicture Secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162229"
---
# <a name="audio-and-subpicture-streams"></a>Audio y subpicture Secuencias

Un DVD-Video disco puede tener hasta ocho secuencias de audio, numeradas de cero a siete, cada una con hasta seis canales discretos. (Tenga en cuenta que las secuencias de audio y subpicture se numeran desde cero, mientras que los títulos, los ángulos y los niveles parentales se numeran a partir de uno). Solo se puede seleccionar una de estas secuencias en un momento dado. En el caso de las subaspecciones, hay hasta 32 secuencias disponibles, aunque solo se puede activar una secuencia en un momento dado. Los discos se suelen crear con secuencias de audio y subimagen predeterminadas, pero una aplicación puede permitir a los usuarios ver una lista de todas las secuencias disponibles y seleccionar la que prefieran. Los pasos básicos de este proceso son los mismos para secuencias de audio y de subimagen.

1.  Determine el número de secuencias disponibles para un título.
2.  Itera por las secuencias y recupera los atributos de secuencia de cada uno.
3.  Recupere el código de idioma del identificador de configuración regional (LCID) devuelto y cree una cadena legible.
4.  Rellene un cuadro de lista u otro control de interfaz de usuario (UI) para permitir que el usuario seleccione una secuencia preferida.

En la aplicación de ejemplo de DVD, el método CAudioLangDlg::MakeAudioStreamList de Dialogs.cpp muestra los pasos básicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



