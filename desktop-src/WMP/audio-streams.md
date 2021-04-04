---
title: Secuencias de audio
description: Secuencias de audio
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Windows Media Player tiendas en línea, secuencias de audio
- tiendas en línea, secuencias de audio
- tipo 1 almacenes en línea, secuencias de audio
- Windows Media Player tiendas en línea, secuencias de servidores de música
- tiendas en línea, secuencias de servidores de música
- tipo 1 tiendas en línea, secuencias de servidores de música
- Windows Media Player tiendas en línea, secuencias del servidor de música
- tiendas en línea, secuencias del servidor de música
- tipo 1 almacenes en línea, secuencias del servidor de música
- secuencias de audio
- secuencias del servidor de música
- flujos de servidores de música
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077341"
---
# <a name="audio-streams"></a>Secuencias de audio

Las tiendas en línea pueden proporcionar música como una transmisión desde un servidor de música. Esto resulta útil para proporcionar ejemplos, elementos promocionales especiales o para permitir que los usuarios de la suscripción disfruten de música sin tener que descargar el contenido. No es habitual almacenar la dirección URL de la secuencia como parte del catálogo de música, sino que debe resolver la dirección URL justo antes de la reproducción basada en el identificador de pista. Para habilitar esto, Windows Media Player llama a [IWMPContentPartner:: GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) y proporciona el tipo de transmisión por secuencias (como un valor de enumeración [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) ) y el identificador de la secuencia. El complemento devuelve la dirección URL del flujo a través del parámetro *pbstrURL* .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




