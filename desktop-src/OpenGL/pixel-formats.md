---
title: Formatos de píxeles
description: Formatos de píxeles
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL en Windows, píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665737"
---
# <a name="pixel-formats"></a>Formatos de píxeles

Un *formato de píxel* especifica varias propiedades de una superficie de dibujo de OpenGL. Algunas de las propiedades especificadas por un formato de píxel son:

-   Si el búfer de píxeles es de un solo valor o de doble búfer.
-   Indica si los datos de píxeles están en formato RGBA o de índice de color.
-   Número de bits utilizados para almacenar los datos de color.
-   Número de bits utilizados para el búfer de profundidad (eje z).
-   Número de bits utilizados para el búfer de estarcido.
-   El número de planos superpuesto y proporcionaban.
-   Varias máscaras de visibilidad.

La implementación de OpenGL para Windows de Microsoft usa la estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) para transmitir los datos con formato de píxeles. Los miembros de la estructura especifican las propiedades anteriores y otras.

Un contexto de dispositivo determinado puede admitir varios formatos de píxeles. Windows identifica los formatos de píxel que admite un contexto de dispositivo con valores de índice de base uno consecutivos (1, 2, 3, 4, etc.). Un contexto de dispositivo solo puede tener un formato de píxel actual, elegido en el conjunto de formatos de píxel que admite.

Cada ventana tiene su propio formato de píxel actual en OpenGL en Windows. Esto significa, por ejemplo, que una aplicación puede mostrar simultáneamente las ventanas de OpenGL de índice de color y RGBA, o bien las ventanas OpenGL de un solo y doble búfer. Esta capacidad de formato de píxel por ventana está limitada a las ventanas de OpenGL.

Normalmente, se obtiene un contexto de dispositivo, se establece el formato de píxel del contexto del dispositivo y, a continuación, se crea un contexto de representación de OpenGL adecuado para ese dispositivo.

> [!Note]  
> Establezca el formato de píxel antes de crear un contexto de representación porque el contexto de representación hereda el formato de píxel del contexto del dispositivo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de formato de píxeles](pixel-format-functions.md)
</dt> </dl>

 

 




