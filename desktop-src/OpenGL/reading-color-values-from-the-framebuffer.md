---
title: Leer valores de color de fotogramas
description: Al usar funciones que leen los valores de color de los fotogramas, tenga en cuenta las diferencias entre leer valores RGBA y valores de índice de color en dispositivos de color verdadero y en dispositivos basados en paletas.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL en Windows, leer valores de color de framebuffers
- leer valores de color de framebuffers OpenGL
- framebuffers, valores de color de lectura OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4df14690b68f7e93949d26ee50ac562ebd667be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774893"
---
# <a name="reading-color-values-from-the-framebuffer"></a>Leer valores de color de fotogramas

Al usar funciones que leen los valores de color de los fotogramas, tenga en cuenta las diferencias entre leer valores RGBA y valores de índice de color en dispositivos de color verdadero y en dispositivos basados en paletas.

En un dispositivo de color verdadero:

-   Los valores RGBA se limitan al canal en el dispositivo.
-   Los valores de índice de color se almacenan como valores RGBA en el fotogramas. Al utilizar estos valores, debe realizar una traducción inversa desde RGBA hasta el índice lógico de la paleta. Si dos índices lógicos tienen los mismos valores RGBA, se puede devolver el índice equivocado.

En un dispositivo basado en paleta:

-   Los valores RGBA se leen de un índice en la paleta del sistema. El índice lógico se obtiene de una tabla inversa y se extraen los componentes RGBA.
-   Los valores de índice de color se leen de un índice en la paleta del sistema y se usa una tabla inversa para obtener el índice de la paleta lógica.

 

 




