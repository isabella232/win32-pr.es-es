---
title: Velocidad de bits
description: Velocidad de bits
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows Media Format SDK, velocidades de bits
- Advanced Systems Format (ASF), velocidades de bits
- ASF (formato de sistemas avanzados), velocidades de bits
- velocidades de bits, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d793be8fe04746a61eea48bcf066d95d641221a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779248"
---
# <a name="bit-rate"></a>Velocidad de bits

La velocidad de bits hace referencia a la cantidad de datos por segundo que se entrega desde un archivo ASF. Las medidas de velocidad de bits están en bits por segundo (BPS) o kilobits por segundo (kbps). La velocidad de bits suele confundirse con el ancho de banda, que es una medida de la capacidad de transferencia de datos de una red. El ancho de banda también se mide en bps y kbps.

El SDK de Windows Media Format se puede usar para crear aplicaciones que entreguen contenido basado en Windows Media de streaming desde ubicaciones de Internet o intranet. Cuando se transmiten datos a través de una red o Internet, la velocidad de bits es de importancia vital para la experiencia del usuario final. Si el ancho de banda disponible para la red es menor que la velocidad de bits del archivo ASF, la reproducción del archivo se interrumpirá de alguna manera. Normalmente, el ancho de banda insuficiente hará que se omitan los ejemplos o que se produzca una pausa en la reproducción mientras se almacenan en búfer más datos.

A cada archivo ASF se le asigna un valor de velocidad de bits en el momento de la creación, en función del tipo y el número de secuencias que se incluyen en el perfil usado. Los flujos individuales tienen sus propias tasas de bits. Las velocidades de bits pueden ser constantes (los datos originales se comprimen de manera que se mantenga un flujo constante de datos aproximadamente a la misma velocidad) o la variable (los datos originales se comprimen de manera que se mantenga la misma calidad en todo, incluso aunque esto pueda significar un flujo de datos desigual). Se pueden aplicar distintos tipos de velocidad de bits a flujos diferentes dentro del mismo archivo.

Puede codificar el mismo contenido en varias secuencias diferentes, cada una con una velocidad de bits diferente. Después, puede configurar las secuencias para que sean mutuamente excluyentes. Esto le permite crear un único archivo que se puede transmitir a los usuarios con diferentes anchos de banda. Esta característica se denomina velocidad de bits múltiple o MBR.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Codificación de velocidad de bits constante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Entradas, secuencias y salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Perfiles**](profiles.md)
</dt> <dt>

[**Codificación de velocidad de bits variable (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




