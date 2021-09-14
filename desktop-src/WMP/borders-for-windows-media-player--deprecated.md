---
title: Bordes para Reproductor de Windows Media (en desuso)
description: Bordes para Reproductor de Windows Media (en desuso)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Reproductor de Windows Media,borders
- Reproductor de Windows Media máscaras,bordes
- máscaras, bordes
- bordes, en comparación con las máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885393"
---
# <a name="borders-for-windows-media-player-deprecated"></a>Bordes para Reproductor de Windows Media (en desuso)

En esta página se documenta una característica que puede no estar disponible en versiones futuras de Reproductor de Windows Media y el SDK Reproductor de Windows Media.

Un borde es similar a una máscara, pero en lugar de reemplazar la interfaz de usuario para el modo compacto de Reproductor de Windows Media, se incrusta un borde en el panel Reproducción ahora del modo completo Reproductor de Windows Media.

Al usar un Windows de descarga multimedia, puede incluir contenido con un borde, lo que allana el camino a las aplicaciones multimedia.

En el directorio de Windows ejemplos de este SDK se incluye un paquete de descarga multimedia de ejemplo que incluye un borde y contenido insertado.

## <a name="creating-a-border"></a>Creación de un borde

Un borde se crea de la misma manera que una máscara. La única diferencia es que la máscara se incrusta dentro del **panel Reproducción** ahora. Esto significa que no se puede calcular el tamaño de la máscara y que todos los elementos de máscara deben ser relativos. Si el usuario cambia Reproductor de Windows Media tamaño, es posible que algunas partes del borde se recorten y no se vean.

## <a name="loading-a-border"></a>Carga de un borde

Se carga un borde cuando se carga Windows metarchivo multimedia que usa el **elemento SKIN.** El **atributo HREF** del elemento **SKIN** debe hacer referencia a una máscara. Un elemento **SKIN** típico tendría este aspecto:


```C++
<SKIN HREF="myborder.wmz">

```



Para obtener más información, vea [ELEMENTO SKIN (en desuso).](skin-element--deprecated.md)

## <a name="including-content-with-a-border"></a>Incluir contenido con un borde

Puede incluir contenido con un borde mediante un archivo Windows de descarga multimedia (con una extensión de nombre de archivo .wmd). Siga estos pasos:

1.  Cree el borde. Asegúrese de crearlo de tal manera que el tamaño no desalmete la composición del borde. Por ejemplo, no incluya un archivo en segundo plano; hacer que el fondo sea transparente para que una visualización pueda ejecutarse detrás de él.
2.  Comprima el contenido de la máscara (art, JScript y el archivo de definición de máscara) en un archivo con una extensión de nombre de archivo .wmz.
3.  Cree un Windows multimedia (con una extensión de nombre de archivo .asx) que haga referencia al archivo de borde comprimido (con una extensión de nombre de archivo .wmz). El metarchivo puede incluir información de lista de reproducción con metadatos de arte y direcciones URL para contenido específico.
4.  Ensamblar el contenido multimedia digital.
5.  Comprima el borde, el metarchivo y el contenido en un archivo y asígále una extensión de nombre de archivo .wmd.

## <a name="using-a-border"></a>Uso de un borde

Después de haber creado el Windows de descarga multimedia, todo lo que tiene que hacer el usuario es hacer doble clic en él. El archivo se descargará en el equipo del usuario. Los archivos dentro del paquete se desempaquetarán, la lista de reproducción  se agregará a las listas de reproducción, el borde aparecerá en el panel Reproducción ahora del modo completo Reproductor de Windows Media y el primer elemento de la nueva lista de reproducción comenzará a reproducirse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las máscaras**](about-skins.md)
</dt> <dt>

[**Ejemplos**](samples.md)
</dt> <dt>

[**Windows Paquetes de descarga de medios (en desuso)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




