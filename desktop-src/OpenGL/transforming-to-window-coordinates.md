---
title: Transformación a coordenadas de ventana
description: Antes de que las coordenadas de recorte se conviertan en coordenadas de ventana, se dividen por el valor de w para producir coordenadas normalizadas del dispositivo.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- Canalización de procesamiento openGL, conversión a coordenadas de ventana
- convertir en coordenadas de ventana OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa74b42457349b14e151099a3c4238e855ad0001e1b8f9416808a1279b82345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887995"
---
# <a name="transforming-to-window-coordinates"></a>Transformación a coordenadas de ventana

Antes de que las coordenadas de recorte se conviertan en coordenadas de ventana, se dividen por el valor *de w* para producir coordenadas normalizadas del dispositivo. La transformación de ventanilla aplicada a estas coordenadas normalizadas genera coordenadas de ventana. Puede controlar la ventanilla, que determina el área de la ventana en pantalla que muestra una imagen, con [**glDepthRange**](gldepthrange.md) y [**glViewport**](glviewport.md).

 

 




