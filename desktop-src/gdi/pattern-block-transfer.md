---
description: El nombre de la función PatBlt (una abreviatura para la transferencia de bloques de patrón) implica que esta función simplemente replica el pincel (o patrón) hasta que rellena un rectángulo especificado.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Transferencia de bloque de patrón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997333"
---
# <a name="pattern-block-transfer"></a>Transferencia de bloque de patrón

El nombre de la función [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (una abreviatura para la transferencia de bloques de patrón) implica que esta función simplemente replica el pincel (o patrón) hasta que rellena un rectángulo especificado. Sin embargo, la función es realmente mucho más eficaz. Antes de replicar el pincel, combina los datos de color del patrón con los datos de color de los píxeles existentes en la pantalla de vídeo mediante una operación de trama (ROP). Un ROP es una operación bit a bit que se aplica a los bits de los datos de color del pincel replicado y los bits de los datos de color del rectángulo de destino en el dispositivo de pantalla. Hay 256 ROPs; sin embargo, la función **PatBlt** reconoce solo los que requieren un patrón y un destino (no los que requieren un origen). En la tabla siguiente se identifica el ROPs más común.



| ROP       | Descripción                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| PATCOPY   | Copia el patrón en el mapa de bits de destino.                                       |
| PATINVERT | Combina el mapa de bits de destino con el patrón mediante el operador booleano XOR. |
| DSTINVERT | Invierte el mapa de bits de destino.                                                     |
| De color negro | Convierte todos los resultados en ceros binarios.                                                   |
| BLANCO | Convierte todos los resultados en binarios.                                                    |



 

Para obtener más información, vea [códigos de operación de trama](raster-operation-codes.md).

 

 



