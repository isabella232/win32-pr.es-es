---
description: Durante la representación, la canalización interpola los datos de vértices en cada triángulo.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Interpolación de triángulos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a411f53351ccd5d3407b358b03e705677e9bf5a96a57b162016afe09332bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746265"
---
# <a name="triangle-interpolation-direct3d-9"></a>Interpolación de triángulos (Direct3D 9)

Durante la representación, la canalización interpola los datos de vértices en cada triángulo. Los datos de vértices pueden ser una amplia variedad de datos y pueden incluir (pero no se limita a): color difuso, color especular, alfa difuso (opacidad del triángulo), alfa especular y un factor de oscilación (tomado de alfa especular para la canalización de vértices de función fija y del registro de vértices programable). Los datos del vértice se definen mediante la declaración [de vértices (Direct3D 9).](vertex-declaration.md)

Para algunos datos de vértice, la interpolación depende del modo de sombreado actual, como se muestra en la tabla siguiente.



| Modo de sombreado | Descripción                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Plano         | Solo el factor de fusión se interpola en modo de sombreado plano. Para todos los demás valores interpolados, el color del primer vértice del triángulo se aplica en toda la cara. |
| Gouraud      | La interpolación lineal se realiza entre los tres vértices.                                                                                                               |



 

El color difuso y el color especular se tratan de forma diferente, en función del modelo de color. En el modelo de color RGB, el sistema usa los componentes de color rojo, verde y azul en la interpolación.

El componente alfa de un color se trata como un valor interpolado independiente porque los controladores de dispositivos pueden implementar la transparencia de dos maneras diferentes: mediante la combinación de texturas o mediante el uso de la combinación de texturas.

Use el miembro ShadeCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar qué formas de interpolación admite el controlador de dispositivo actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistemas de coordenadas y geometría](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



