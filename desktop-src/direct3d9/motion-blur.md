---
description: Puede mejorar la velocidad percibida de un objeto en una escena 3D desenfocando el objeto y saliendo del rastro desenfocado de las imágenes de objeto detrás del objeto. Para ello, las aplicaciones de Direct3D representan el objeto varias veces por fotograma.
ms.assetid: 8b1a1f0d-5857-4ab4-828c-8ca7c17a4890
title: Desenfoque de movimiento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fccb5c00d1208041afc31d4afe1cf0c7a5425037
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537593"
---
# <a name="motion-blur-direct3d-9"></a>Desenfoque de movimiento (Direct3D 9)

Puede mejorar la velocidad percibida de un objeto en una escena 3D desenfocando el objeto y saliendo del rastro desenfocado de las imágenes de objeto detrás del objeto. Para ello, las aplicaciones de Direct3D representan el objeto varias veces por fotograma.

Recuerde que las aplicaciones de Direct3D normalmente representan escenas en un búfer fuera de la pantalla. El contenido del búfer se muestra en la pantalla cuando la aplicación llama a [**IDirect3DDevice9::P método reenviado**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) . La aplicación Direct3D puede representar el objeto varias veces en una escena antes de mostrar el marco en la pantalla.

Mediante programación, la aplicación realiza varias llamadas a un método DrawPrimitive, pasando repetidamente el mismo objeto 3D. Antes de cada llamada, la posición del objeto se actualiza ligeramente, lo que produce una serie de imágenes de objeto borrosas en la superficie de representación de destino. Si el objeto tiene una o más texturas, la aplicación puede mejorar el efecto de desenfoque de movimiento representando la primera imagen del objeto con todas sus texturas casi transparentes. Cada vez que se representa el objeto, disminuye la transparencia de la textura del objeto. Cuando la aplicación representa el objeto en su posición final, debe representar las texturas del objeto sin transparencia. La excepción es si va a agregar el desenfoque de movimiento a otro efecto que requiera transparencia de textura. En cualquier caso, la imagen inicial del objeto en el marco debe ser la más transparente. La imagen final debe ser el menos transparente.

Una vez que la aplicación representa la serie de imágenes de objeto en la superficie de representación de destino y representa el resto de la escena, debe llamar al método [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para mostrar el marco en la pantalla.

Si la aplicación simula el efecto del usuario que se desplaza a través de una escena a alta velocidad, puede Agregar el desenfoque de movimiento a toda la escena. En este caso, la aplicación representa la escena completa varias veces por fotograma. Cada vez que se representa la escena, la aplicación debe colocar ligeramente el punto de vista. Si la escena es muy compleja, el usuario puede ver una degradación del rendimiento visible a medida que aumenta la aceleración debido al creciente número de representaciones de escenas por fotograma.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suavizado](antialiasing.md)
</dt> </dl>

 

 
