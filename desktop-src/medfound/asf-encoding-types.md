---
description: Tipos de codificación ASF
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Tipos de codificación ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153691"
---
# <a name="asf-encoding-types"></a>Tipos de codificación ASF

Los métodos de codificación se centran en el búfer usado por el codificador para administrar los datos de entrada sin comprimir. Este búfer se define por la velocidad de bits de la secuencia, en bits por segundo, y la ventana de búfer, en milisegundos. Al codificar en archivos ASF, los codificadores multimedia de Windows respetan las restricciones del búfer. Para obtener más información acerca de la ventana de búfer, vea [el modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md). Saber cómo y Cuándo usar cada método puede ayudarle a crear contenido comprimido de alta calidad. La tabla siguiente contiene vínculos a temas sobre cada uno de los métodos de codificación disponibles que una aplicación puede usar para codificar datos multimedia en ASF.



| Método de codificación                                                                                      | Descripción                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificación de velocidad de bits constante](constant-bit-rate-encoding.md)                                         | El codificador comprime los datos a una velocidad de bits especificada.                                                                                                                                                     |
| [Codificación de velocidad de bits variable basada en la calidad](quality-based-variable-bit-rate--vbr--encoding.md)       | El codificador comprime los datos en un valor de calidad determinado para que la calidad de los medios codificados sea coherente a lo largo de su duración, independientemente de los requisitos de búfer del flujo resultante. |
| [Codificación de velocidad de bits variable sin restricciones](unconstrained-variable-bit-rate--vbr--encoding.md)       | El codificador comprime los datos con la máxima calidad posible manteniendo una velocidad de bits especificada. Este modo también se denomina codificación de velocidad de bits variable (VBR) de dos pasos.                                    |
| [Codificación de velocidad de bits variable máxima limitada](peak-constrained-variable-bit-rate--vbr--encoding.md) | El codificador comprime los datos a una velocidad de bits especificada y mantiene los valores de búfer en la ventana de búfer máxima especificada y la velocidad de bits. Este modo también se denomina VBR máxima de dos pasos.                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Codificadores de Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



