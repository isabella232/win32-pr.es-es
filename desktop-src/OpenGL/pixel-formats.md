---
title: Formatos de píxel
description: Formatos de píxel
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL en Windows,píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbcd49b17c298d00d0ab41391172c8ae4c3bce8cb295db619d1c9787a2bca36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486197"
---
# <a name="pixel-formats"></a>Formatos de píxel

Un *formato de píxel* especifica varias propiedades de una superficie de dibujo OpenGL. Algunas de las propiedades especificadas por un formato de píxel son:

-   Si el búfer de píxeles está almacenado en búfer único o doble.
-   Si los datos de píxeles están en formato RGBA o de índice de color.
-   Número de bits usados para almacenar datos de color.
-   Número de bits usados para el búfer de profundidad (eje Z).
-   Número de bits usados para el búfer de galería de símbolos.
-   Número de planos superpuestos e subyacentes.
-   Varias máscaras de visibilidad.

La implementación de Microsoft de OpenGL para Windows usa la estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) para transmitir datos de formato de píxel. Los miembros de la estructura especifican las propiedades anteriores y otras.

Un contexto de dispositivo determinado puede admitir varios formatos de píxel. Windows identifica los formatos de píxel que admite un contexto de dispositivo con valores de índice uno consecutivos (1, 2, 3, 4, y así sucesivamente). Un contexto de dispositivo puede tener solo un formato de píxel actual, elegido entre el conjunto de formatos de píxeles que admite.

Cada ventana tiene su propio formato de píxel actual en OpenGL en Windows. Esto significa, por ejemplo, que una aplicación puede mostrar simultáneamente ventanas RGBA y OpenGL de índice de colores, o ventanas OpenGL de un solo y doble búfer. Esta funcionalidad de formato de píxel por ventana se limita a las ventanas OpenGL.

Normalmente, se obtiene un contexto de dispositivo, se establece el formato de píxel del contexto de dispositivo y, a continuación, se crea un contexto de representación openGL adecuado para ese dispositivo.

> [!Note]  
> Establezca el formato de píxel antes de crear un contexto de representación porque el contexto de representación hereda el formato de píxel del contexto del dispositivo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de formato de píxel](pixel-format-functions.md)
</dt> </dl>

 

 




