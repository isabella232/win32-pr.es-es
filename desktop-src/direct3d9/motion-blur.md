---
description: Puede mejorar la velocidad percibida de un objeto en una escena 3D si desenfoca el objeto y deja un final de imágenes de objeto desenfocado detrás del objeto. Las aplicaciones de Direct3D lo logran al representar el objeto varias veces por fotograma.
ms.assetid: 8b1a1f0d-5857-4ab4-828c-8ca7c17a4890
title: Desenfoque de movimiento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3daa0b35a0c375cc798b619f18f1e363001050de4dcc950e6c6828a7d365801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628325"
---
# <a name="motion-blur-direct3d-9"></a>Desenfoque de movimiento (Direct3D 9)

Puede mejorar la velocidad percibida de un objeto en una escena 3D si desenfoca el objeto y deja un final de imágenes de objeto desenfocado detrás del objeto. Las aplicaciones de Direct3D lo logran al representar el objeto varias veces por fotograma.

Recuerde que las aplicaciones de Direct3D suelen representar escenas en un búfer fuera de la pantalla. El contenido del búfer se muestra en la pantalla cuando la aplicación llama al método [**IDirect3DDevice9::P resent.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) La aplicación Direct3D puede representar el objeto varias veces en una escena antes de mostrar el marco en la pantalla.

Mediante programación, la aplicación realiza varias llamadas a un método DrawPrimitive, pasando repetidamente el mismo objeto 3D. Antes de cada llamada, la posición del objeto se actualiza ligeramente, lo que genera una serie de imágenes de objetos desenfocados en la superficie de representación de destino. Si el objeto tiene una o varias texturas, la aplicación puede mejorar el efecto de desenfoque de movimiento al representar la primera imagen del objeto con todas sus texturas casi transparente. Cada vez que se representa el objeto, disminuye la transparencia de la textura del objeto. Cuando la aplicación representa el objeto en su posición final, debe representar las texturas del objeto sin transparencia. La excepción es si va a agregar desenfoque de movimiento a otro efecto que requiere transparencia de textura. En cualquier caso, la imagen inicial del objeto en el marco debe ser la más transparente. La imagen final debe ser la menos transparente.

Después de que la aplicación represente la serie de imágenes de objeto en la superficie de representación de destino y represente el resto de la escena, debe llamar al método [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para mostrar el marco en la pantalla.

Si la aplicación está simulando el efecto de que el usuario se mueve por una escena a alta velocidad, puede agregar desenfoque de movimiento a toda la escena. En este caso, la aplicación representa la escena completa varias veces por fotograma. Cada vez que se representa la escena, la aplicación debe mover ligeramente el punto de vista. Si la escena es muy compleja, el usuario puede ver una degradación del rendimiento visible a medida que aumenta la aceleración debido al creciente número de representaciones de escena por fotograma.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Antialiasing](antialiasing.md)
</dt> </dl>

 

 
