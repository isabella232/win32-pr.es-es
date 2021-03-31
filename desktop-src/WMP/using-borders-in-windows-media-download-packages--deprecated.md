---
title: Usar bordes en paquetes de descarga de Windows Media (en desuso)
description: Usar bordes en paquetes de descarga de Windows Media (en desuso)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Metaarchivos de Windows Media, paquetes de descarga de Windows Media
- Windows Media Player, paquetes de descarga de Windows Media
- metaarchivos, paquetes de descarga de Windows Media
- Windows Media, paquetes de descarga de Windows Media
- bordes, acerca de
- Paquetes de descarga de Windows Media, bordes
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418791"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a>Usar bordes en paquetes de descarga de Windows Media (en desuso)

En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.

Los bordes permiten crear una interfaz gráfica de usuario personalizada para el contenido empaquetado. El borde puede incluir elementos como imágenes, controles interactivos y vínculos a sitios Web. Puede usar bordes en los casos en los que desee agregar un valor adicional al contenido empaquetado, como para la personalización de marca o el anuncio. Después de que los usuarios descarguen y abran el paquete de descarga de Windows Media, Windows Media Player muestra automáticamente el borde personalizado cuando reproduce el contenido empaquetado.

A diferencia de una máscara, que permite a los usuarios reemplazar por completo la interfaz de usuario de Windows Media Player, solo se muestra un borde en el panel **reproducción en curso** del reproductor en modo completo. Sin embargo, las mismas herramientas y tecnologías que se usan para crear máscaras también se usan para crear bordes. En la ilustración siguiente se muestra un borde.

![un borde mostrado en el reproductor de Windows Media 10](images/border-v10.png)

Es importante comprender las técnicas básicas para crear una máscara antes de intentar crear un borde. La programación de bordes se consigue con dos lenguajes de programación: lenguaje de marcado extensible (XML) y Microsoft JScript. XML se utiliza para definir elementos de interfaz como botones, controles deslizantes y cuadros de texto. No es necesario comprender todos los detalles de XML, ya que no es necesario escribir nuevos elementos de código XML. puede simplemente usar los proporcionados por Media Player de Windows. Aunque JScript no es necesario para crear bordes, se puede usar para proporcionar funcionalidad adicional.

Un archivo de borde comprimido con la extensión de nombre de archivo. WMZ incluye un archivo de definición de borde con una extensión de nombre de archivo. WMS y todos los archivos de imagen que se usan dentro del borde.

Para incluir un borde en un paquete de descarga de Windows Media, basta con crear un borde y hacer referencia a ese borde en una lista de reproducción de metarchivo de Windows Media. El archivo de borde se carga en Windows Media Player después de que el reproductor analice el metarchivo e interprete el elemento de **máscara** que hace referencia al borde. El elemento **Skin** solo se usa para los bordes y el atributo href del elemento **Skin** solo puede hacer referencia a una máscara para cada paquete.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Bordes de Media Player de Windows (desusado)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Paquetes de descarga de Windows Media (en desuso)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Máscaras de Windows Media Player**](windows-media-player-skins.md)
</dt> </dl>

 

 




