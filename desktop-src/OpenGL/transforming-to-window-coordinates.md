---
title: Transformar a coordenadas de ventana
description: Antes de que las coordenadas del clip se conviertan en coordenadas de la ventana, se dividen por el valor de w para obtener coordenadas de dispositivo normalizadas.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- Canalización de procesamiento de OpenGL, convertir a coordenadas de ventana
- convertir a coordenadas de ventana OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ec3d8922890cfa3a79c5dacd94e93a06c53a73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779459"
---
# <a name="transforming-to-window-coordinates"></a>Transformar a coordenadas de ventana

Antes de que las coordenadas del clip se conviertan en coordenadas de la ventana, se dividen por el valor de *w* para obtener coordenadas de dispositivo normalizadas. La transformación ventanilla aplicada a estas coordenadas normalizadas genera coordenadas de ventana. Puede controlar la ventanilla, que determina el área de la ventana en pantalla que muestra una imagen, con [**glDepthRange**](gldepthrange.md) y [**glViewport**](glviewport.md).

 

 




