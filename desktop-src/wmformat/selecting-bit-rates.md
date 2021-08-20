---
title: Selección de velocidades de bits
description: Selección de velocidades de bits
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- perfiles, elegir velocidades de bits
- perfiles, velocidades de bits
- códecs, elegir velocidades de bits
- códecs, velocidades de bits
- perfiles, selección de velocidades de bits
- códecs, selección de velocidades de bits
- velocidades de bits, selección
- velocidades de bits, perfiles
- velocidades de bits, códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41afa50cb765ed8ff4acaa26681ba87337b05642f7d60958e02a4fe27e359840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117654329"
---
# <a name="selecting-bit-rates"></a>Selección de velocidades de bits

En el caso de los archivos que se transmitirán a través de una red, debe considerar detenidamente qué velocidades de bits debe usar. En la mayoría de las circunstancias, puede agregar las velocidades de bits de todas las secuencias de un archivo para obtener una idea general del ancho de banda disponible necesario para transmitir el archivo. Sin embargo, también se requiere una cierta cantidad de sobrecarga para cada secuencia. Esta sobrecarga se resume en la tabla siguiente.



| Intervalo de velocidad de bits (Kbps) | Ancho de banda adicional necesario para la sobrecarga (Kbps) |
|-----------------------|---------------------------------------------------|
| 10 – 16               | 3                                                 |
| 17 – 30               | 4                                                 |
| 31 – 45               | 5                                                 |
| 46 – 70               | 6                                                 |
| 71 – 225              | 7                                                 |
| >225               | 9                                                 |



 

La sobrecarga normal necesaria para un flujo no tiene en cuenta las extensiones de unidad de datos. Cada extensión de unidad de datos agrega al tamaño de la muestra a la que está asociada. En función del tipo de extensión de unidad de datos, esto puede aumentar considerablemente la velocidad de bits de la secuencia.

También debe tener en cuenta que el ancho de banda máximo teórico disponible a través de una conexión de red no es una velocidad de bits objetivo práctica. El ancho de banda medio disponible para una conexión determinada se queda muy por debajo de la capacidad de ancho de banda de la conexión, debido al tráfico de red y a muchos otros factores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Diseño de perfiles**](designing-profiles.md)
</dt> </dl>

 

 




