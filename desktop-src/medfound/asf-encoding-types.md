---
description: Tipos de codificación asf
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Tipos de codificación asf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580013"
---
# <a name="asf-encoding-types"></a>Tipos de codificación asf

Todos los métodos de codificación se centran en el búfer utilizado por el codificador para administrar los datos de entrada sin comprimir. Este búfer se define mediante la velocidad de bits de la secuencia, en bits por segundo, y la ventana del búfer, en milisegundos. Al codificar en archivos ASF, los codificadores Windows media cumplen las restricciones del búfer. Para obtener más información sobre la ventana de búfer, vea [El modelo de búfer de cubo filtrada.](the-leaky-bucket-buffer-model.md) Saber cómo y cuándo usar cada método puede ayudarle a crear contenido comprimido de alta calidad. La tabla siguiente contiene vínculos a temas sobre cada uno de los métodos de codificación disponibles que una aplicación puede usar para codificar datos multimedia en ASF.



| Método de codificación                                                                                      | Descripción                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificación de velocidad de bits constante](constant-bit-rate-encoding.md)                                         | El codificador comprime los datos a una velocidad de bits especificada.                                                                                                                                                     |
| [Codificación de velocidad de bits variable basada en calidad](quality-based-variable-bit-rate--vbr--encoding.md)       | El codificador comprime los datos en un valor de calidad determinado para que la calidad del medio codificado sea coherente a lo largo de su duración, independientemente de los requisitos de búfer de la secuencia resultante. |
| [Codificación de velocidad de bits variable sin restricciones](unconstrained-variable-bit-rate--vbr--encoding.md)       | El codificador comprime los datos a la máxima calidad posible mientras mantiene una velocidad de bits especificada. Este modo también se denomina codificación de velocidad de bits variable (VBR) de 2 pases.                                    |
| [Codificación de velocidad de bits variable con restricciones máximas](peak-constrained-variable-bit-rate--vbr--encoding.md) | El codificador comprime los datos a una velocidad de bits especificada mientras mantiene los valores de búfer bajo la ventana de búfer máxima y la velocidad de bits especificadas. Este modo también se denomina VBR de pico de 2 paso.                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Windows Codificadores multimedia](windows-media-encoders.md)
</dt> </dl>

 

 



