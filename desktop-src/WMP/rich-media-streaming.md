---
title: Rich Media Streaming
description: Rich Media Streaming
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Reproductor de Windows Media, presentaciones basadas en web
- Reproductor de Windows Media de objetos, presentaciones basadas en web
- modelo de objetos, presentaciones basadas en web
- Reproductor de Windows Media Presentaciones móviles basadas en web
- Reproductor de Windows Media ActiveX, presentaciones basadas en web
- Reproductor de Windows Media Control de ActiveX móviles, presentaciones basadas en web
- ActiveX control, presentaciones basadas en web
- Reproductor de Windows Media, streaming multimedia enriquecido
- Reproductor de Windows Media de objetos enriquecidos, streaming multimedia enriquecido
- modelo de objetos, streaming multimedia enriquecido
- Reproductor de Windows Media Móvil, streaming multimedia enriquecido
- Reproductor de Windows Media ActiveX, streaming multimedia enriquecido
- Reproductor de Windows Media Control de ActiveX móvil, streaming multimedia enriquecido
- ActiveX, streaming multimedia enriquecido
- Presentaciones basadas en web, streaming multimedia enriquecido
- crear presentaciones basadas en web, streaming multimedia enriquecido
- streaming multimedia enriquecido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070887"
---
# <a name="rich-media-streaming"></a>Rich Media Streaming

Las páginas web complejas contienen muchos componentes diferentes que normalmente se transfieren por separado. En una conexión lenta, estas páginas se muestran de una en una y pueden tardar varios minutos en mostrarse por completo. Esto puede impedir la sincronización eficaz de páginas web con los medios digitales. La solución a este problema es el streaming multimedia enriquecido, lo que significa agregar las páginas web a la secuencia multimedia digital para que se entreguen al mismo tiempo que los datos de audio o vídeo.

El streaming multimedia enriquecido usa un diseño de conjunto de fotogramas simple y se comporta exactamente igual que el volteo normal de la dirección URL. Al igual que en el cambio de dirección URL, los comandos de script de dirección URL insertados en secuencias multimedia digitales se usan para mostrar el contenido en el marco de destino. Sin embargo, en lugar de apuntar a páginas en la Web, Reproductor de Windows Media series 9 o versiones posteriores usan los comandos de script de dirección URL para acceder a los archivos de la caché de Internet Explorer donde se coloca el contenido HTML transmitido a medida que se recibe. Al igual que con el cambio de dirección URL normal, puede escribir controladores de eventos que respondan a estos comandos de script de dirección URL, o puede permitir que el control Reproductor de Windows Media control controle todo automáticamente.

> [!Note]  
> Cualquier contenido HTML entregado a través de streaming multimedia enriquecido se reproduce en la zona de seguridad de Internet y está sujeto a la configuración de seguridad del explorador del usuario.

 

Para más información sobre la creación de presentaciones multimedia enriquecciones, consulte el SDK de la serie Windows Media Format 9 o posterior y el SDK de la serie Windows Media Encoder 9.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de Web-Based presentación**](creating-web-based-presentations.md)
</dt> <dt>

[**Usar script para controlar el volteo de direcciones URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




