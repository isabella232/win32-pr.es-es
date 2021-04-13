---
title: Fuentes y texto (OpenGL)
description: La implementación de OpenGL en Windows de Microsoft admite gráficos GDI en una ventana de OpenGL de un solo búfer.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL en Windows, fuentes
- OpenGL en Windows, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421816"
---
# <a name="fonts-and-text-opengl"></a>Fuentes y texto (OpenGL)

La implementación de OpenGL en Windows de Microsoft admite gráficos GDI en una ventana de OpenGL de un solo búfer. No admite gráficos de GDI en una ventana de OpenGL de doble búfer. Por lo tanto, solo puede llamar a las funciones de texto y fuente de GDI estándar para dibujar texto en una ventana de OpenGL de un solo búfer. no se puede llamar a esas funciones para dibujar texto en una ventana de OpenGL de doble búfer.

Existe una solución alternativa para esta restricción en el texto de las ventanas de doble búfer: Cree listas de visualización de OpenGL para imágenes de mapa de bits de caracteres y, a continuación, ejecute esas listas de visualización para dibujar caracteres. Existen tres pasos principales en este proceso:

1.  Seleccione una fuente para un contexto de dispositivo y establezca las propiedades de la fuente según sea necesario.
2.  Cree un conjunto de listas de presentación de mapas de bits en función de los glifos de la fuente del contexto del dispositivo, una lista de visualización para cada glifo que la aplicación va a dibujar.
3.  Dibuje cada glifo en una cadena mediante las listas de visualización del mapa de bits.

Para crear las listas de visualización, llame a las funciones [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) y [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) . Para dibujar caracteres en una cadena mediante esas listas de visualización, llame a [**glCallLists**](glcalllists.md).

Para crear aplicaciones que sean fáciles de localizar y que utilicen los recursos de manera moderada, la creación y el almacenamiento de estas listas de visualización de imágenes de glifo deben administrarse con cuidado. Muchos idiomas, a diferencia del inglés, tienen alfabetos cuyos códigos de carácter van a través de un conjunto de valores relativamente grande.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de fuente y texto](font-and-text-functions.md)
</dt> </dl>

 

 




