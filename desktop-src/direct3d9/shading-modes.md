---
description: El modo de sombreado utilizado para representar un polígono tiene un efecto profundo en su apariencia. Los modos de sombreado determinan la intensidad del color y la iluminación en cualquier punto de una cara de polígono. Direct3D admite dos modos de sombreado.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Modos de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714e9610e1cae344148bf78ef39bc5e8355cb2af6395e3f92a3bc01b87860605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092241"
---
# <a name="shading-modes-direct3d-9"></a>Modos de sombreado (Direct3D 9)

El modo de sombreado utilizado para representar un polígono tiene un efecto profundo en su apariencia. Los modos de sombreado determinan la intensidad del color y la iluminación en cualquier punto de una cara de polígono. Direct3D admite dos modos de sombreado.

-   [Sombreado plano](#flat-shading)
-   [Sombreado de Gouraud](#gouraud-shading)

## <a name="flat-shading"></a>Sombreado plano

En el modo de sombreado plano, la canalización de representación de Direct3D representa un polígono, usando el color del material del polígono en su primer vértice como color para todo el polígono. Los objetos 3D que se representan con sombreado plano tienen bordes visiblemente nítidos entre polígonos si no son coplanares.

En la ilustración siguiente se muestra un depósito de té representado con sombreado plano. El contorno de cada polígono es claramente visible. El sombreado plano es la forma más rápida de sombreado.

![ilustración de un depósito de té mediante sombreado plano](images/flattea.png)

## <a name="gouraud-shading"></a>Sombreado de Gouraud

Cuando Direct3D representa un polígono mediante sombreado de Gouraud, calcula un color para cada vértice mediante los parámetros normales y de iluminación del vértice. A continuación, interpola el color a través de la cara de los polígonos La interpolación se realiza linealmente. Por ejemplo, si el componente rojo del color del vértice 1 es 0,8 y el componente rojo del vértice 2 es 0,4, mediante el modo de sombreado Gouraud y el modelo de color RGB, el módulo de iluminación de Direct3D asigna un componente rojo de 0,6 al píxel en el punto medio de la línea entre estos vértices.

En la ilustración siguiente se muestra el sombreado de Gouraud. Esta cafetera se compone de muchos polígonos planos y triangulares. Sin embargo, el sombreado de Gouraud hace que la superficie del objeto parezca curva y suave.

![ilustración del depósito de té mediante el sombreado gouraud](images/gourtea.png)

El sombreado de Gouraud también se puede usar para mostrar objetos con bordes nítidos.

Para obtener más información, vea [Vectores normales de caras y vértices (Direct3D 9).](face-and-vertex-normal-vectors.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreado](shading.md)
</dt> </dl>

 

 



