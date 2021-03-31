---
title: Unidades VML
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: f95e65ad-d92a-460f-baeb-30fd8a35f84e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e59ff91fb134edeba7e653be30141b3f72c6b65
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792328"
---
# <a name="vml-units"></a>Unidades VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

VML usa las siguientes unidades CSS.



Unidades de longitud relativa

decir

Alto de la fuente del elemento.

ex

Alto de la letra "x".

px

Pixel.

%

Proporción.

Unidades de longitud absoluta

in

Pulgadas (1 pulgada = 2,54 centímetros).

cm

Centímetros.

MM

Milímetros.

pt

Puntos (1 punto = 1/72 pulgadas).

pc

Picas (1 pica = 12 puntos).



 

Las medidas y posiciones de las propiedades de la hoja de estilos en cascada (CSS) se crean mediante unidades de longitud. Internet Explorer admite dos tipos de unidades de longitud: relativa y absoluta.

Una unidad de longitud relativa especifica una longitud con respecto a otra propiedad de longitud. Las unidades de longitud relativa escalan mejor desde un dispositivo de salida a otro, como desde un monitor a una impresora. Los porcentajes y las palabras clave funcionan de forma similar.

Una unidad de longitud absoluta especifica una medida absoluta, como pulgadas o centímetros. Las unidades de longitud absoluta son útiles cuando se conocen las propiedades físicas del dispositivo de salida.

## <a name="other-units-of-measurement"></a>Otras unidades de medida

**PERTENEZCA**

La UEM (unidad métrica inglesa) es la unidad de medida útil más pequeña y la usa VML para el almacenamiento de unidades internas. Hay 914400 UME por pulgada y 12700 UME en un punto. EMUs no puede ser fraccionario.

Dado que los EMUs están definidos por números enteros con signo de 32 bits, el mayor número de EMUs es de 2348 pulgadas (aproximadamente 59 metros o 65 metros). Dado que las medidas siempre caben en un dispositivo de salida de tamaño de página o de pantalla, siempre se incluirán dentro de este intervalo.

**Ángulos**

Las medidas de ángulo se pueden definir con los siguientes sufijos.



Sufijo

FD

Fracciones de grado.

ninguno

Degrees (Grados)

deg

Degrees (Grados)

rad

Radians



 

 

 