---
title: Transmisión por secuencias multimedia enriquecida
description: Transmisión por secuencias multimedia enriquecida
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Windows Media Player, presentaciones basadas en Web
- Modelo de objetos de Windows Media Player, presentaciones basadas en Web
- modelo de objetos, presentaciones basadas en Web
- Windows Media Player presentaciones móviles y basadas en Web
- Control ActiveX de Windows Media Player, presentaciones basadas en Web
- Control ActiveX móvil de Windows Media Player, presentaciones basadas en Web
- Control ActiveX, presentaciones basadas en Web
- Windows Media Player, transmisión por secuencias multimedia enriquecida
- Modelo de objetos de Windows Media Player, transmisión por secuencias multimedia enriquecida
- modelo de objetos, streaming multimedia enriquecido
- Windows Media Player Mobile, streaming multimedia enriquecido
- Control ActiveX de Windows Media Player, transmisión por secuencias multimedia enriquecida
- Control ActiveX móvil de Windows Media Player, transmisión por secuencias multimedia enriquecida
- Control ActiveX, transmisión por secuencias multimedia enriquecida
- Presentaciones basadas en Web, transmisión por secuencias multimedia enriquecida
- crear presentaciones basadas en Web, transmisión por secuencias multimedia enriquecida
- transmisión por secuencias multimedia enriquecida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778252"
---
# <a name="rich-media-streaming"></a>Transmisión por secuencias multimedia enriquecida

Las páginas web complejas contienen muchos componentes diferentes que normalmente se transfieren por separado. En una conexión lenta, estas páginas muestran una pieza cada vez y pueden tardar varios minutos en mostrarse por completo. Esto puede impedir la sincronización efectiva de páginas web con los medios digitales. La solución a este problema es la transmisión por secuencias multimedia enriquecida, lo que significa que se agregan las páginas web al flujo multimedia digital para que se entreguen al mismo tiempo que los datos de audio o vídeo.

La transmisión por secuencias multimedia enriquecida usa un diseño de conjuntos de Marcos sencillo y se comporta exactamente igual que el volteo normal de la dirección URL. Al igual que en el volteo de direcciones URL, los comandos de script de URL insertados en secuencias de medios digitales se usan para mostrar el contenido en el marco de destino. Sin embargo, en lugar de apuntar a las páginas de la web, Windows Media Player 9 series o versiones posteriores usan los comandos de script de la dirección URL para tener acceso a los archivos de la memoria caché de Internet Explorer en los que se encuentra el contenido de HTML transmitido a medida que se recibe. Al igual que con el volteo normal de direcciones URL, puede escribir controladores de eventos que respondan a estos comandos de script de dirección URL, o bien permitir que el control de Windows Media Player controle todo automáticamente.

> [!Note]  
> Cualquier contenido HTML entregado a través de la transmisión por secuencias de multimedia enriquecida se reproduce en la zona de seguridad de Internet y está sujeto a la configuración de seguridad del explorador del usuario.

 

Para obtener más información acerca de la creación de presentaciones multimedia enriquecidas, consulte el SDK de Windows Media Format 9 series o posterior y el SDK de Windows Media Encoder 9 series.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear Web-Based presentaciones**](creating-web-based-presentations.md)
</dt> <dt>

[**Usar script para controlar el volteo de URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




