---
title: Fuentes y texto (OpenGL)
description: La implementación de Microsoft de OpenGL en Windows admite gráficos GDI en una ventana openGL de un solo búfer.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL en Windows,fuentes
- OpenGL en Windows,text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071511"
---
# <a name="fonts-and-text-opengl"></a>Fuentes y texto (OpenGL)

La implementación de Microsoft de OpenGL en Windows admite gráficos GDI en una ventana openGL de un solo búfer. No admite gráficos GDI en una ventana OpenGL de doble búfer. Por lo tanto, solo puede llamar a las funciones estándar de fuente y texto GDI para dibujar texto en una ventana openGL de un solo búfer; No se puede llamar a esas funciones para dibujar texto en una ventana openGL de doble búfer.

Hay una solución alternativa para esta restricción en el texto en ventanas de doble búfer: cree listas de visualización openGL para imágenes de mapa de bits de caracteres y, a continuación, ejecute esas listas de visualización para dibujar caracteres. Hay tres pasos principales en este proceso:

1.  Seleccione una fuente para un contexto de dispositivo y estableciendo las propiedades de la fuente como desee.
2.  Cree un conjunto de listas de visualización de mapa de bits basadas en los glifos de la fuente del contexto del dispositivo, una lista de visualización para cada glifo que dibujará la aplicación.
3.  Dibuje cada glifo en una cadena con esas listas de visualización de mapa de bits.

Para crear las listas para mostrar, llame a [**las funciones wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) [**y wglUseFontOutlines.**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) Para dibujar caracteres en una cadena mediante esas listas para mostrar, llame [**a glCallLists**](glcalllists.md).

Para crear aplicaciones fáciles de localización y que usan recursos con moderación, la creación y el almacenamiento de estas listas de visualización de imágenes de glifo se deben administrar cuidadosamente. Muchos idiomas, a diferencia del inglés, tienen alfabetos cuyos códigos de caracteres oscilan en un conjunto de valores relativamente grande.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de fuente y texto](font-and-text-functions.md)
</dt> </dl>

 

 




