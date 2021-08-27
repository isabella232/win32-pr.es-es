---
description: El nombre de la función PatBlt (una abreviatura para la transferencia de bloques de patrones) implica que esta función simplemente replica el pincel (o patrón) hasta que rellena un rectángulo especificado.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Transferencia de bloques de patrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecb51cbe12da80ca643e2d520e8ebe25c4c9fe03d56a8a16e0c55caf5f1ce10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092935"
---
# <a name="pattern-block-transfer"></a>Transferencia de bloques de patrones

El nombre de la [**función PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (una abreviatura para la transferencia de bloques de patrones) implica que esta función simplemente replica el pincel (o patrón) hasta que rellena un rectángulo especificado. Sin embargo, la función es realmente mucho más eficaz. Antes de replicar el pincel, combina los datos de color del patrón con los datos de color de los píxeles existentes en la presentación de vídeo mediante una operación de trama (ROP). Un ROP es una operación bit a bit que se aplica a los bits de datos de color para el pincel replicado y los bits de datos de color para el rectángulo de destino en el dispositivo de presentación. Hay 256 ROP; sin embargo, **la función PatBlt** reconoce solo aquellos que requieren un patrón y un destino (no los que requieren un origen). En la tabla siguiente se identifican las ROP más comunes.



| Rop       | Descripción                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| PATCOPY   | Copia el patrón en el mapa de bits de destino.                                       |
| PATINVERT | Combina el mapa de bits de destino con el patrón mediante el operador booleano XOR. |
| DSTINVERT | Invierte el mapa de bits de destino.                                                     |
| Oscuridad | Convierte todas las salidas en ceros binarios.                                                   |
| Blancura | Convierte todos los resultados en binarios.                                                    |



 

Para obtener más información, vea [Códigos de operación de trama.](raster-operation-codes.md)

 

 



