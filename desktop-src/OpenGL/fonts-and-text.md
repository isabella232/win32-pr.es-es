---
title: Fuentes y texto (OpenGL)
description: La implementación de OpenGL de Microsoft en Windows admite gráficos GDI en una ventana openGL de un solo búfer.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL en Windows,fuentes
- OpenGL en Windows,text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966298b6a8d8e5584e761570205a5d3e7be58be3a8dfeb488db2a6f523fc9a25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082435"
---
# <a name="fonts-and-text-opengl"></a>Fuentes y texto (OpenGL)

La implementación de OpenGL de Microsoft en Windows admite gráficos GDI en una ventana openGL de un solo búfer. No admite gráficos GDI en una ventana OpenGL de doble búfer. Por lo tanto, solo puede llamar a las funciones estándar de fuente y texto GDI para dibujar texto en una ventana openGL de un solo búfer; No se puede llamar a esas funciones para dibujar texto en una ventana openGL de doble búfer.

Hay una solución alternativa para esta restricción en el texto en ventanas de doble búfer: cree listas de visualización openGL para imágenes de mapa de bits de caracteres y, a continuación, ejecute esas listas de visualización para dibujar caracteres. Hay tres pasos principales en este proceso:

1.  Seleccione una fuente para un contexto de dispositivo, estableciendo las propiedades de la fuente como desee.
2.  Cree un conjunto de listas de visualización de mapa de bits basadas en los glifos de la fuente del contexto del dispositivo, una lista de visualización para cada glifo que dibujará la aplicación.
3.  Dibuje cada glifo en una cadena con esas listas de visualización de mapa de bits.

Para crear las listas para mostrar, llame a [**las funciones wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) [**y wglUseFontOutlines.**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) Para dibujar caracteres en una cadena mediante esas listas para mostrar, llame [**a glCallLists**](glcalllists.md).

Para crear aplicaciones fáciles de localización y que usan recursos con moderación, la creación y el almacenamiento de estas listas de visualización de imágenes de glifo se deben administrar cuidadosamente. Muchos idiomas, a diferencia del inglés, tienen alfabetos cuyos códigos de caracteres oscilan en un conjunto de valores relativamente grande.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de fuente y texto](font-and-text-functions.md)
</dt> </dl>

 

 




