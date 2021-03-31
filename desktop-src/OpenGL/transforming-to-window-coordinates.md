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
# <a name="transforming-to-window-coordinates"></a><span data-ttu-id="5dd7d-105">Transformar a coordenadas de ventana</span><span class="sxs-lookup"><span data-stu-id="5dd7d-105">Transforming to Window Coordinates</span></span>

<span data-ttu-id="5dd7d-106">Antes de que las coordenadas del clip se conviertan en coordenadas de la ventana, se dividen por el valor de *w* para obtener coordenadas de dispositivo normalizadas.</span><span class="sxs-lookup"><span data-stu-id="5dd7d-106">Before clip coordinates are converted to window coordinates, they are divided by the value of *w* to yield normalized device coordinates.</span></span> <span data-ttu-id="5dd7d-107">La transformación ventanilla aplicada a estas coordenadas normalizadas genera coordenadas de ventana.</span><span class="sxs-lookup"><span data-stu-id="5dd7d-107">The viewport transformation applied to these normalized coordinates produces window coordinates.</span></span> <span data-ttu-id="5dd7d-108">Puede controlar la ventanilla, que determina el área de la ventana en pantalla que muestra una imagen, con [**glDepthRange**](gldepthrange.md) y [**glViewport**](glviewport.md).</span><span class="sxs-lookup"><span data-stu-id="5dd7d-108">You control the viewport, which determines the area of the on-screen window that displays an image, with [**glDepthRange**](gldepthrange.md) and [**glViewport**](glviewport.md).</span></span>

 

 




