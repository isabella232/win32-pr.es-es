---
title: Frontal, posterior y otros búferes
description: OpenGL almacena y manipula datos de píxeles en un fotogramas.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL en Windows, búferes
- framebuffers OpenGL
- búferes de color OpenGL
- búferes de profundidad OpenGL
- búferes de acumulación OpenGL
- búferes de estarcido OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418835"
---
# <a name="front-back-and-other-buffers"></a>Frontal, posterior y otros búferes

OpenGL almacena y manipula datos de píxeles en un fotogramas. Fotogramas consta de un conjunto de búferes lógicos: color, Depth, acumulación y búferes de estarcido. El búfer de color se compone de un conjunto de búferes lógicos; Este conjunto puede incluir una parte delantera izquierda, una parte delantera derecha, una parte trasera izquierda, una parte derecha y un número de búferes auxiliares. Es posible que un formato de píxel determinado o una implementación de OpenGL no suministren todos estos búferes. Por ejemplo, la versión actual de la implementación de OpenGL en Windows de Microsoft no admite imágenes Stereoscopic, por lo que un formato de píxel no puede tener búferes de color a la izquierda y a la derecha. Además, la versión actual no admite búferes auxiliares. Para obtener más información sobre los búferes OpenGL y las funciones OpenGL que operan en ellos, vea el *manual de referencia de OpenGL* y la guía de programación de *OpenGL*.

La implementación de OpenGL en Windows de Microsoft admite el doble búfer de imágenes. Se trata de una técnica en la que una aplicación dibuja píxeles en un búfer fuera de pantalla y, a continuación, cuando la imagen está lista para mostrarse, copia el contenido del búfer fuera de pantalla en un búfer en pantalla. El doble búfer permite cambios de imagen suaves, que son especialmente importantes para las imágenes animadas.

Dos búferes de color están disponibles para las aplicaciones que utilizan el almacenamiento en búfer doble: un búfer frontal y un búfer de reserva. De forma predeterminada, los comandos de dibujo se dirigen al búfer de reserva (el búfer fuera de pantalla), mientras que el búfer frontal se muestra en la pantalla. Cuando el búfer fuera de pantalla está listo para su presentación, se llama a [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)y Windows copia el contenido del búfer fuera de pantalla en el búfer en pantalla.

La implementación genérica usa un mapa de bits independiente del dispositivo (DIB) como búfer de reserva y la presentación en pantalla como búfer frontal. Los dispositivos de hardware y sus controladores pueden usar enfoques diferentes.

El almacenamiento en búfer doble es una propiedad de formato de píxeles. Para solicitar un doble búfer para un formato de píxel, establezca la \_ marca PFD DOUBLEBUFFER en la estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) en una llamada a [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).

La función básica de OpenGL, [**glDrawBuffer**](gldrawbuffer.md), selecciona los búferes para escritura y borrado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de búfer](buffer-functions.md)
</dt> </dl>

 

 




