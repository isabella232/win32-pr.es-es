---
title: Bordes de Media Player de Windows (desusado)
description: Bordes de Media Player de Windows (desusado)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Media Player de Windows, bordes
- Aspectos de Windows Media Player, bordes
- máscaras, bordes
- bordes, comparación con máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357074"
---
# <a name="borders-for-windows-media-player-deprecated"></a>Bordes de Media Player de Windows (desusado)

En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.

Un borde es similar a una máscara, pero en lugar de reemplazar la interfaz de usuario para el modo compacto de Windows Media Player, se inserta un borde en el panel reproducción en curso del Media Player de Windows en modo completo.

Mediante el uso de un paquete de descarga de Windows Media, puede incluir contenido con un borde, y así llegar a las aplicaciones multimedia.

En el directorio de ejemplos de este SDK se incluye un paquete de descarga de Windows Media de ejemplo que incluye un borde y contenido incrustado.

## <a name="creating-a-border"></a>Crear un borde

Un borde se crea de la misma manera que una máscara. La única diferencia es que la máscara está incrustada dentro del panel **reproducción en curso** . Esto significa que no se puede calcular el tamaño de la máscara y que todos los elementos de máscara deben ser relativos. Si el usuario cambia el tamaño de Windows Media Player, se pueden recortar partes del borde y no verse.

## <a name="loading-a-border"></a>Cargar un borde

Se carga un borde cuando se carga un metarchivo de Windows Media que utiliza el elemento de **máscara** . El atributo **href** del elemento **Skin** debe hacer referencia a una máscara. Un elemento de **máscara** típico tendría el siguiente aspecto:


```C++
<SKIN HREF="myborder.wmz">

```



Para obtener más información, vea [elemento Skin (deprecated)](skin-element--deprecated.md).

## <a name="including-content-with-a-border"></a>Incluir contenido con un borde

Puede incluir contenido con un borde mediante un archivo de descarga de Windows Media (con la extensión de nombre de archivo. WMD). Siga estos pasos:

1.  Cree el borde. Tenga cuidado de crearlo de modo que el cambio de tamaño no dañe la composición del borde. Por ejemplo, no incluya un archivo de fondo; Haga que el fondo sea transparente para que una visualización pueda ejecutarse detrás.
2.  Comprimir el contenido de la máscara (imágenes, archivos JScript y el archivo de definición de máscara) en un archivo con la extensión de nombre de archivo. WMZ.
3.  Cree un metarchivo de Windows Media (con una extensión de nombre de archivo. ASX) que haga referencia al archivo de borde comprimido (con una extensión de nombre de archivo. WMZ). El metarchivo puede incluir información de lista de reproducción con metadatos para arte y direcciones URL de contenido específico.
4.  Ensamble el contenido multimedia digital.
5.  Comprima el borde, el metarchivo y el contenido en un archivo y asígnele una extensión de nombre de archivo. WMD.

## <a name="using-a-border"></a>Usar un borde

Una vez creado el archivo de descarga de Windows Media, lo único que debe hacer el usuario es hacer doble clic en él. El archivo se descargará en el equipo del usuario. Los archivos incluidos en el paquete se desempaquetarán, se agregará la lista de reproducción a las listas de reproducción, el borde aparecerá en el panel **reproducción en curso** del Media Player de Windows en modo completo y el primer elemento de la nueva lista de reproducción comenzará a reproducirse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las máscaras**](about-skins.md)
</dt> <dt>

[**Ejemplos**](samples.md)
</dt> <dt>

[**Paquetes de descarga de Windows Media (en desuso)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




