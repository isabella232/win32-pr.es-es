---
title: Seleccionar velocidades de bits
description: Seleccionar velocidades de bits
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- perfiles, elegir velocidades de bits
- perfiles, velocidades de bits
- códecs, elegir velocidades de bits
- códecs, velocidades de bits
- perfiles, seleccionar velocidades de bits
- códecs, seleccionar velocidades de bits
- velocidades de bits, seleccionar
- tasas de bits, perfiles
- velocidades de bits, códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356663"
---
# <a name="selecting-bit-rates"></a>Seleccionar velocidades de bits

En el caso de los archivos que se transmitirán por secuencias a través de una red, debe considerar detenidamente qué tasas de bits debe usar. En la mayoría de los casos, puede Agregar las velocidades de bits de todas las secuencias de un archivo de forma conjunta para obtener una idea general del ancho de banda disponible necesario para transmitir el archivo. Sin embargo, también se requiere una determinada cantidad de sobrecarga para cada flujo. Esta sobrecarga se resume en la tabla siguiente.



| Intervalo de velocidad de bits (kbps) | Ancho de banda adicional necesario para la sobrecarga (kbps) |
|-----------------------|---------------------------------------------------|
| de 10 a 16               | 3                                                 |
| 17 – 30               | 4                                                 |
| 31 – 45               | 5                                                 |
| 46 – 70               | 6                                                 |
| 71 – 225              | 7                                                 |
| >225               | 9                                                 |



 

La sobrecarga normal necesaria para una secuencia no tiene en cuenta las extensiones de unidad de datos. Cada extensión de unidad de datos se agrega al tamaño del ejemplo al que está adjunta. Dependiendo del tipo de extensión de unidad de datos, esto puede aumentar en gran medida la velocidad de bits de la secuencia.

También debe tener en cuenta que el ancho de banda máximo teórico disponible a través de una conexión de red no es una velocidad de bits de destino práctica. El ancho de banda disponible promedio para una conexión determinada es muy breve de la capacidad de ancho de banda de la conexión, debido al tráfico de red y a muchos otros factores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Diseñar perfiles**](designing-profiles.md)
</dt> </dl>

 

 




