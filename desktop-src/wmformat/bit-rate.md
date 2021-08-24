---
title: Velocidad de bits
description: Velocidad de bits
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows SDK de formato multimedia, velocidades de bits
- Formato de sistemas avanzados (ASF), velocidades de bits
- ASF (formato de sistemas avanzados), velocidades de bits
- velocidades de bits, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a15332e18d47a72974098ad38c6a942ceaf4780e1b79dffacd49382e3416ae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809881"
---
# <a name="bit-rate"></a>Velocidad de bits

La velocidad de bits hace referencia a la cantidad de datos por segundo que se entregan desde un archivo ASF. Las medidas de velocidad de bits se encuentran en bits por segundo (bps) o kilobits por segundo (Kbps). La velocidad de bits suele confundirse con el ancho de banda, que es una medida de la capacidad de transferencia de datos de una red. El ancho de banda también se mide en bps y Kbps.

El SDK Windows Media Format se puede usar para crear aplicaciones que proporcionan streaming Windows contenido basado en multimedia desde ubicaciones de Internet o intranet. Cuando se están transmitiendo datos a través de una red o Internet, la velocidad de bits es de vital importancia para la experiencia del usuario final. Si el ancho de banda disponible para la red es menor que la velocidad de bits del archivo ASF, la reproducción del archivo se interrumpirá de alguna manera. Normalmente, el ancho de banda insuficiente dará lugar a la omisión de muestras o a una pausa en la reproducción mientras se almacena en búfer más datos.

A cada archivo ASF se le asigna un valor de velocidad de bits en el momento de la creación, en función del tipo y el número de secuencias que se incluyen en el perfil utilizado. Las secuencias individuales tienen sus propias velocidades de bits. Las velocidades de bits pueden ser constantes (los datos originales se comprimen de forma que se mantenga un flujo constante de datos aproximadamente a la misma velocidad) o variable (los datos originales se comprimen de forma que se mantenga la misma calidad en todo el proceso, aunque esto puede significar un flujo de datos desigual). Se pueden aplicar distintos tipos de velocidad de bits a diferentes secuencias dentro del mismo archivo.

Puede codificar el mismo contenido en varias secuencias diferentes, cada una con una velocidad de bits diferente. A continuación, puede configurar las secuencias para que sean mutuamente excluyentes. Esto le permite crear un único archivo que se puede transmitir a los usuarios con distintos anchos de banda. Esta característica se denomina velocidad de bits múltiple o MBR.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Codificación de velocidad de bits constante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Entradas, Secuencias salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Perfiles**](profiles.md)
</dt> <dt>

[**Codificación de velocidad de bits variable (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




