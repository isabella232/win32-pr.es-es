---
description: El modo de sombreado que se usa para representar un polígono tiene un efecto profundo en su aspecto. Los modos de sombreado determinan la intensidad del color y la iluminación en cualquier punto de una esfera de polígono. Direct3D admite dos modos de sombreado.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Modos de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104554669"
---
# <a name="shading-modes-direct3d-9"></a>Modos de sombreado (Direct3D 9)

El modo de sombreado que se usa para representar un polígono tiene un efecto profundo en su aspecto. Los modos de sombreado determinan la intensidad del color y la iluminación en cualquier punto de una esfera de polígono. Direct3D admite dos modos de sombreado.

-   [Sombreado plano](#flat-shading)
-   [Sombreado Gouraud](#gouraud-shading)

## <a name="flat-shading"></a>Sombreado plano

En el modo de sombreado plano, la canalización de representación de Direct3D representa un polígono, utilizando el color del material del polígono en su primer vértice como color para todo el polígono. los objetos 3D que se representan con sombreado plano tienen bordes muy nítidos entre polígonos si no son coplanares.

En la ilustración siguiente se muestra un tetera representado con sombreado plano. El contorno de cada polígono es claramente visible. El sombreado plano es la forma más rápida de sombreado.

![Ilustración de un tetera mediante el sombreado plano](images/flattea.png)

## <a name="gouraud-shading"></a>Sombreado Gouraud

Cuando Direct3D representa un polígono mediante el sombreado Gouraud, calcula un color para cada vértice mediante los parámetros normales de vértice y de iluminación. A continuación, interpola el color a lo largo de la superficie de los polígonos, la interpolación se realiza linealmente. Por ejemplo, si el componente rojo del color del vértice 1 es 0,8 y el componente rojo del vértice 2 es 0,4, mediante el modo de sombreado Gouraud y el modelo de color RGB, el módulo de iluminación de Direct3D asigna un componente rojo de 0,6 al píxel en el punto medio de la línea entre estos vértices.

En la ilustración siguiente se muestra el sombreado Gouraud. Este tetera se compone de muchos polígonos planos y triangulares. Sin embargo, el sombreado Gouraud hace que la superficie del objeto aparezca curvada y suave.

![Ilustración de tetera mediante el sombreado Gouraud](images/gourtea.png)

El sombreado Gouraud también se puede usar para mostrar objetos con bordes nítidos.

Para obtener más información, consulte [vectores normales de cara y vértice (Direct3D 9)](face-and-vertex-normal-vectors.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreado](shading.md)
</dt> </dl>

 

 



