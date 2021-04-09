---
title: Representación de imágenes
description: Representación de imágenes
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib, representación de imágenes
- DrawDib, dibujar DIB
- DrawDibDraw función)
- DrawDibGetBuffer función)
- DrawDibUpdate función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e0d3f4d770a3acc290273b14ec14ff4b6efa30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076292"
---
# <a name="image-rendering"></a>Representación de imágenes

Después de llamar a [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) para crear un controlador de dominio de DrawDib (consulte [operaciones de DrawDib](drawdib-operations.md)), puede dibujar un DIB en la pantalla mediante la función [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) . **DrawDibDraw** crea un mapa de bits de color verdadero al mostrarlos con adaptadores de pantalla de 8 bits.

[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) también admite compresores de vídeo de forma transparente al mostrar mapas de bits comprimidos. Puede tener acceso al búfer que contiene la imagen descomprimida mediante la función [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) . **DrawDibGetBuffer** devuelve **null** cuando se dibuja un mapa de bits sin comprimir. Debe preparar la aplicación para administrar los mapas de bits comprimidos y sin comprimir.

Puede actualizar una imagen o una parte de una imagen que se muestra en la aplicación mediante la macro [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las funciones de DrawDib](about-the-drawdib-functions.md)
</dt> </dl>

 

 




