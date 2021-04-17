---
description: Durante la representación, la canalización interpola los datos de vértices en cada triángulo.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Interpolación triangular (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705251"
---
# <a name="triangle-interpolation-direct3d-9"></a>Interpolación triangular (Direct3D 9)

Durante la representación, la canalización interpola los datos de vértices en cada triángulo. Los datos de vértice pueden ser una amplia variedad de datos y pueden incluir (pero no se limita a): color difuso, color especular, alfa difuso (opacidad del triángulo), alfa especular y un factor de niebla (tomado del alfa especular para la canalización de vértices de función fija y del registro de niebla para la canalización de vértices programable). Los datos de vértice se definen mediante la [declaración de vértice (Direct3D 9)](vertex-declaration.md).

En algunos datos de vértices, la interpolación depende del modo de sombreado actual, tal como se muestra en la tabla siguiente.



| Modo de sombreado | Descripción                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Plano         | Solo el factor de niebla se interpola en el modo de sombra plana. Para todos los demás valores interpolados, el color del primer vértice del triángulo se aplica en toda la esfera. |
| Gouraud      | La interpolación lineal se realiza entre los tres vértices.                                                                                                               |



 

El color difuso y el color especular se tratan de forma diferente, dependiendo del modelo de color. En el modelo de color RGB, el sistema usa los componentes de color rojo, verde y azul en la interpolación.

El componente alfa de un color se trata como un valor interpolado independiente, ya que los controladores de dispositivo pueden implementar la transparencia de dos maneras diferentes: mediante el uso de la combinación de texturas o el uso de punteado.

Use el miembro ShadeCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar qué formas de interpolación admite el controlador de dispositivo actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistemas de coordenadas y geometría](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



