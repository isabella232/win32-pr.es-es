---
title: Crear un paquete de descarga de Windows Media (en desuso)
description: Crear un paquete de descarga de Windows Media (en desuso)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Metaarchivos de Windows Media, paquetes de descarga de Windows Media
- Windows Media Player, paquetes de descarga de Windows Media
- metaarchivos, paquetes de descarga de Windows Media
- Windows Media, paquetes de descarga de Windows Media
- Paquetes de descarga de Windows Media, crear
- crear paquetes de descarga de Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075928"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a>Crear un paquete de descarga de Windows Media (en desuso)

En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.

Siga estos pasos para crear un paquete de descarga de Windows Media.

1.  **Cree un borde.** Utilice las mismas técnicas que utilizaría para crear una máscara para Windows Media Player. Diseñe el borde para que el cambio de tamaño de Windows Media Player no dañe la composición de los elementos de borde. Por ejemplo, use un color sólido o una visualización como fondo, ya que se escalarán correctamente a medida que se cambie el tamaño de Windows Media Player.
2.  **Comprimir el contenido del borde.** Cree una carpeta comprimida (con una extensión de nombre de archivo. zip) que contenga los archivos de borde: imágenes, archivos JScript y el archivo de definición de máscara con la extensión de nombre de archivo. WMS. Cambie el nombre del archivo comprimido para que tenga una extensión de nombre de archivo. WMZ.
3.  **Escriba un metarchivo de Windows Media.** Windows Media Player no cargará el borde a menos que cree un metarchivo de Windows Media con una extensión de nombre de archivo. ASX que implementa el elemento **Skin** . El metarchivo también se puede utilizar para crear una lista de reproducción que describa el contenido incluido en el paquete.
4.  **Ensamble el contenido.** Coloque todos los archivos que desee usar en una carpeta. Esto incluye archivos de audio, archivos de vídeo, metaarchivos y archivos de definición de borde.
5.  **Cree el paquete.** Cree una carpeta comprimida (con una extensión de nombre de archivo. zip) que contenga el archivo de borde, los archivos de contenido y el metarchivo. Cambie la extensión de nombre de archivo de este archivo. zip a la extensión de nombre de archivo. WMD.
6.  **Publicar el paquete en un sitio Web.** El paquete completado está listo para publicarse en un sitio web y los usuarios lo descargan.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Paquetes de descarga de Windows Media (en desuso)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




