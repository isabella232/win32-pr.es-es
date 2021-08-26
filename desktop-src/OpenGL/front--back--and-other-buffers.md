---
title: Front, Back y otros búferes
description: OpenGL almacena y manipula datos de píxeles en un búfer de fotogramas.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL en Windows,buffers
- Framebuffers OpenGL
- búferes de color OpenGL
- búferes de profundidad OpenGL
- búferes de acumulación OpenGL
- búferes de galería de símbolos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd64f980aad1df8576accd8c37d19521a5368e1fe295393d54c2836f2db8566
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082325"
---
# <a name="front-back-and-other-buffers"></a>Front, Back y otros búferes

OpenGL almacena y manipula datos de píxeles en un búfer de fotogramas. El búfer de fotogramas consta de un conjunto de búferes lógicos: búferes de color, profundidad, acumulación y galería de símbolos. El propio búfer de color consta de un conjunto de búferes lógicos; este conjunto puede incluir un front-left, un front-right, un back-left, un back-right y un número de búferes auxiliares. Es posible que un formato de píxel determinado o una implementación de OpenGL no proporcionen todos estos búferes. Por ejemplo, la versión actual de la implementación de OpenGL de Microsoft en Windows no admite imágenes estereo estéreo, por lo que un formato de píxel no puede tener búferes de color izquierdo y derecho. Además, la versión actual no admite búferes auxiliares. Para obtener más información sobre los búferes de OpenGL y las funciones de OpenGL que funcionan en ellos, vea el Manual de referencia de *OpenGL* y la Guía *de programación de OpenGL*.

La implementación de OpenGL de Microsoft en Windows admite el almacenamiento en búfer doble de imágenes. Se trata de una técnica en la que una aplicación dibuja píxeles en un búfer fuera de pantalla y, después, cuando esa imagen está lista para mostrarse, copia el contenido del búfer fuera de pantalla en un búfer en pantalla. El almacenamiento en búfer doble permite realizar cambios de imagen sin problemas, que son especialmente importantes para las imágenes animadas.

Hay dos búferes de color disponibles para las aplicaciones que usan el almacenamiento en búfer doble: un búfer frontal y un búfer de reserva. De forma predeterminada, los comandos de dibujo se dirigen al búfer de reserva (el búfer fuera de pantalla), mientras que el búfer frontal se muestra en la pantalla. Cuando el búfer fuera de pantalla esté listo para mostrarse, llame a [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)y Windows copia el contenido del búfer fuera de pantalla en el búfer en pantalla.

La implementación genérica usa un mapa de bits independiente del dispositivo (DIB) como búfer de reserva y la pantalla se muestra como búfer frontal. Los dispositivos de hardware y sus controladores pueden usar enfoques diferentes.

El almacenamiento en búfer doble es una propiedad con formato de píxel. Para solicitar el almacenamiento en búfer doble para un formato de píxel, establezca la marca PFD DOUBLEBUFFER en la estructura de datos \_ [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) en una llamada a [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).

La función principal OpenGL, [**glDrawBuffer,**](gldrawbuffer.md)selecciona búferes para escribir y borrar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de búfer](buffer-functions.md)
</dt> </dl>

 

 




