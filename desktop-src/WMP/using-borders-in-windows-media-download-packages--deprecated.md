---
title: Uso de bordes en Windows descarga de medios (en desuso)
description: Uso de bordes en Windows descarga de medios (en desuso)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Windows Metarchivos multimedia, Windows paquetes de descarga multimedia
- Reproductor de Windows Media,Windows de descarga multimedia
- metarchivos, Windows paquetes de descarga multimedia
- Windows Paquetes de descarga multimedia Windows multimedia
- borders,about
- Windows Paquetes de descarga multimedia, bordes
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070845"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a>Uso de bordes en Windows descarga de medios (en desuso)

En esta página se documenta una característica que puede no estar disponible en versiones futuras de Reproductor de Windows Media y Reproductor de Windows Media SDK.

Los bordes permiten crear una interfaz gráfica de usuario personalizada para el contenido empaquetado. El borde puede incluir elementos como imágenes, controles interactivos y vínculos a sitios web. Puede usar bordes en los casos en los que desee agregar valor adicional al contenido empaquetado, como para la marca o la publicidad. Después de que los usuarios descarguen y abran el paquete de descarga Windows multimedia, Reproductor de Windows Media automáticamente el borde personalizado cuando reproduce el contenido empaquetado.

A diferencia de una máscara, que permite a los usuarios reemplazar completamente la  interfaz de usuario Reproductor de Windows Media, solo se muestra un borde en el panel Reproducción ahora del reproductor en modo completo. Sin embargo, las mismas herramientas y tecnologías que se usan para crear máscaras también se usan para crear bordes. En la ilustración siguiente se muestra un borde.

![un borde que se muestra en el Reproductor multimedia de Windows 10](images/border-v10.png)

Es importante comprender las técnicas básicas para crear una máscara antes de intentar crear un borde. La programación de borde se realiza mediante dos lenguajes de programación: lenguaje de marcado extensible (XML) y Microsoft JScript. XML se usa para definir elementos de interfaz como botones, controles deslizantes y cuadros de texto. No es necesario comprender todos los detalles de XML, ya que no es necesario escribir nuevos elementos de código XML. puede usar simplemente las proporcionadas por Reproductor de Windows Media. Aunque JScript no es necesario para crear bordes, se puede usar para proporcionar funcionalidad adicional.

Un archivo de borde comprimido con una extensión de nombre de archivo .wmz incluye un archivo de definición de borde con una extensión de nombre de archivo .wms y todos los archivos de imagen utilizados dentro del borde.

Para incluir un borde en un paquete de descarga Windows multimedia, basta con crear un borde y hacer referencia a ese borde en una lista de reproducción Windows metarchivo multimedia. El archivo de borde se carga en Reproductor de Windows Media después de que el reproductor analice el metarchivo e interprete el elemento **SKIN** que hace referencia al borde. El **elemento SKIN** solo se usa para los bordes, y el atributo HREF del elemento **SKIN** solo puede hacer referencia a una máscara para cada paquete.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Bordes para Reproductor de Windows Media (en desuso)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Paquetes de descarga de medios (en desuso)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Reproductor de Windows Media Pieles**](windows-media-player-skins.md)
</dt> </dl>

 

 




