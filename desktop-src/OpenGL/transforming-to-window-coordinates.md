---
title: Transformación en coordenadas de ventana
description: Antes de que las coordenadas de recorte se conviertan en coordenadas de ventana, se dividen por el valor de w para producir coordenadas de dispositivo normalizadas.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- Canalización de procesamiento de OpenGL, conversión a coordenadas de ventana
- convertir en coordenadas de ventana OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ec3d8922890cfa3a79c5dacd94e93a06c53a73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361998"
---
# <a name="transforming-to-window-coordinates"></a>Transformación en coordenadas de ventana

Antes de que las coordenadas de recorte se conviertan en coordenadas de ventana, se dividen por el valor *de w* para producir coordenadas de dispositivo normalizadas. La transformación de ventanilla aplicada a estas coordenadas normalizadas genera coordenadas de ventana. Puede controlar la ventanilla, que determina el área de la ventana en pantalla que muestra una imagen, [**con glDepthRange**](gldepthrange.md) y [**glViewport**](glviewport.md).

 

 




