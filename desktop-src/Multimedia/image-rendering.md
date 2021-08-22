---
title: Representación de imágenes
description: Representación de imágenes
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib, representación de imágenes
- DrawDib, dibs de dibujo
- Función DrawDibDraw
- Función DrawDibGetBuffer
- Función DrawDibUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7be73fbe37a28ab44116d2fb2e68acb6a9a3a385603af23dca0e14aa2de4d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690755"
---
# <a name="image-rendering"></a>Representación de imágenes

Después de llamar a [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) para crear un controlador de dominio DrawDib (vea [DrawDib Operations](drawdib-operations.md)), puede dibujar un DIB en la pantalla mediante la función [**DrawDibDraw.**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) **DrawDibDraw dithers** true-color bitmaps when showing them with 8-bit display adapters( DrawDibDraw dithers true-color bitmaps when showing them with 8-bit display adapters.

[**DrawDibDraw también**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) admite vídeos de forma transparente al mostrar mapas de bits comprimidos. Puede acceder al búfer que contiene la imagen descomprimida mediante la [**función DrawDibGetBuffer.**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) **DrawDibGetBuffer** devuelve **NULL al** dibujar un mapa de bits sin comprimir. Debe preparar la aplicación para controlar mapas de bits comprimidos y sin comprimir.

Puede actualizar una imagen o una parte de una imagen mostrada por la aplicación mediante la macro [**DrawDibUpdate.**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las funciones DrawDib](about-the-drawdib-functions.md)
</dt> </dl>

 

 




