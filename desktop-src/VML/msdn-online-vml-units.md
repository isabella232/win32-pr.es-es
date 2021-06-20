---
title: Unidades de VML
description: En este artículo se describen las unidades de VML. VML es una característica que está en desuso a partir de Windows Internet Explorer 9.
ms.assetid: f95e65ad-d92a-460f-baeb-30fd8a35f84e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184d577052412bde4a97148b51cab12a87b3672e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406948"
---
# <a name="vml-units"></a>Unidades de VML

En este tema se describe VML, una característica que está en desuso a partir de Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

VML usa las siguientes unidades CSS.



Unidades de longitud relativa

em

Alto de la fuente del elemento.

ex

Alto de la letra "x".

px

Píxeles.

%

Porcentaje.

Unidades de longitud absoluta

in

Pulgadas (1 pulgada = 2,54 cm).

cm

Centímetros.

mm

Milímetros.

pt

Puntos (1 punto = 1/72 pulgadas ).

pc

Susa (1); 12 puntos.



 

Las medidas y posiciones de las propiedades de hoja de estilos en cascada (CSS) se realizan mediante unidades de longitud. Internet Explorer admite dos tipos de unidades de longitud: relativa y absoluta.

Una unidad de longitud relativa especifica una longitud en relación con otra propiedad de longitud. Las unidades de longitud relativa se escalan mejor de un dispositivo de salida a otro, como desde un monitor a una impresora. Los porcentajes y las palabras clave tienen un rendimiento similar.

Una unidad de longitud absoluta especifica una medida absoluta, como pulgadas o centímetros. Las unidades de longitud absoluta son útiles cuando se conocen las propiedades físicas del dispositivo de salida.

## <a name="other-units-of-measurement"></a>Otras unidades de medida

**Emú**

La EMU (unidad métrica en inglés) es la unidad de medida útil más pequeña y la usa VML para el almacenamiento interno de unidades. Hay 914400 EMU por pulgada y 12700 EMU en un punto. Las EMU no pueden ser fracciones.

Puesto que las EMUs se definen mediante números enteros con firma de 32 bits, el mayor número de EMUs es de 2348 pulgadas (unos 59 metros o 65 65 pulgadas). Dado que las medidas siempre caben en un dispositivo de salida de tamaño de página o de pantalla, siempre estarán dentro de este intervalo.

**Ángulos**

Las medidas angulares se pueden definir con los sufijos siguientes.



Sufijo

Fd

Fracciones de grados.

ninguno

Degrees (Grados)

deg

Degrees (Grados)

rad

Radians



 

 

 