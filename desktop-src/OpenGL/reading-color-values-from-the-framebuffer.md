---
title: Lectura de valores de color del búfer de fotogramas
description: Al usar funciones que leen los valores de color del búfer de fotogramas, tenga en cuenta las diferencias entre la lectura de valores RGBA y los valores de índice de color en dispositivos de color verdadero y en dispositivos basados en paleta.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL on Windows,reading color values from framebuffers
- lectura de valores de color de FrameBuffers OpenGL
- framebuffers,lectura de valores de color OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65beb6dae04019637fc8683220ce12e671c4a52d4f015ae9f8d45e70db67bb36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794772"
---
# <a name="reading-color-values-from-the-framebuffer"></a>Lectura de valores de color del búfer de fotogramas

Al usar funciones que leen los valores de color del búfer de fotogramas, tenga en cuenta las diferencias entre la lectura de valores RGBA y los valores de índice de color en dispositivos de color verdadero y en dispositivos basados en paleta.

En un dispositivo de color verdadero:

-   Los valores RGBA se limitan al canal del dispositivo.
-   Los valores de índice de color se almacenan como valores RGBA en el búfer de fotogramas. Al usar estos valores, debe realizar una traducción inversa de RGBA al índice de la paleta lógica. Si dos índices lógicos tienen los mismos valores RGBA, se puede devolver un índice incorrecto.

En un dispositivo basado en paleta:

-   Los valores RGBA se leen de un índice de la paleta del sistema. El índice lógico se obtiene de una tabla inversa y se extraen los componentes RGBA.
-   Los valores de índice de color se leen de un índice en la paleta del sistema y se usa una tabla inversa para obtener el índice de la paleta lógica.

 

 




