---
title: Audio Secuencias
description: Audio Secuencias
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Reproductor de Windows Media en línea, secuencias de audio
- tiendas en línea, secuencias de audio
- tiendas en línea de tipo 1, secuencias de audio
- Reproductor de Windows Media en línea, secuencias de servidores de música
- online stores,streams from music servers
- tiendas en línea de tipo 1, secuencias de servidores de música
- Reproductor de Windows Media en línea, secuencias de servidor de música
- tiendas en línea, secuencias de servidor de música
- tiendas en línea de tipo 1, secuencias de servidor de música
- secuencias de audio
- secuencias de servidor de música
- secuencias de servidores de música
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889892"
---
# <a name="audio-streams"></a>Audio Secuencias

Las tiendas en línea pueden proporcionar música como secuencia desde un servidor de música. Esto es útil para proporcionar ejemplos, elementos promocionales especiales o para permitir que los usuarios de la suscripción disfruten de música sin tener que descargar el contenido. Es habitual no almacenar la dirección URL de la secuencia como parte del catálogo de música, sino resolver la dirección URL justo antes de la reproducción en función del identificador de pista. Para habilitar esto, Reproductor de Windows Media llama a [IWMPContentPartner::GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) y proporciona el tipo de streaming (como un valor de enumeración [WMPStreamingType)](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) y el identificador de la secuencia. El complemento devuelve la dirección URL de la secuencia a través del *parámetro pbstrURL.*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




