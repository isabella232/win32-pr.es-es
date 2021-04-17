---
title: Selección de características de perfil
description: Selección de características de perfil
ms.assetid: 5e09000d-1417-43aa-9e9c-0aff536d52b7
keywords:
- perfiles, selección de características
- perfiles, seleccionar características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769b10387bb4fb660c31678b406090cfc7e42743
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704627"
---
# <a name="selecting-profile-features"></a>Selección de características de perfil

En la tabla siguiente se enumeran las características de los perfiles y se describe cuándo se deben utilizar o no.



| Característica                            | Cuándo se usa                                                                                                                                                                                                                                                                                                                | Cuándo no se debe usar                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exclusión mutua por velocidad de bits (MBR) | El archivo se transmitirá a una audiencia con velocidades de conexión que varíen de un usuario a otro (por ejemplo, los archivos entregados a través de Internet).                                                                                                                                                                              | El archivo no se transmitirá por secuencias a través de una red. El archivo se transmitirá por secuencias a través de una red con un ancho de banda disponible coherentemente (por ejemplo, los archivos entregados a través de una red de área local corporativa).<br/>                                                              |
| Exclusión mutua por idioma       | El archivo contiene secuencias que duplican los mismos datos en distintos idiomas. (Por ejemplo, una película doblada en varios idiomas tendría la banda sonora codificada como flujo mutuamente excluyente).                                                                                                                         | El archivo solo contiene flujos en un solo idioma. Si el archivo contiene solo flujos que se deben cambiar para idiomas individuales, puede ser más sencillo crear un nuevo archivo para cada idioma (por ejemplo, para una película de entrenamiento con gran cantidad de texto en la secuencia de vídeo).<br/> |
| Exclusión mutua por presentación   | Quiere proporcionar vídeo en más de una relación de aspecto. Por ejemplo, un archivo podría contener el mismo vídeo formateado para televisión y el formato de pantalla ancha original de así.                                                                                                                                     | Solo hay una versión de cada flujo de vídeo.                                                                                                                                                                                                                                    |
| Uso compartido de ancho de banda                  | El archivo se transmitirá por secuencias y tendrá dos o más secuencias que, cuando se combinan, usan menos ancho de banda que los valores de velocidad de bits de ambos flujos agregados juntos. Dado que la velocidad de bits de una secuencia es esencialmente el ancho de banda máximo necesario para la secuencia, algunas secuencias pueden tener algunos períodos de menor transferencia de datos. | El archivo no se transmitirá por secuencias a través de una red. Todas las secuencias tienen velocidades de bits coherentes.<br/>                                                                                                                                                                                     |
| Priorización de flujos              | El archivo se transmitirá por secuencias y algunas secuencias son más importantes que otras.                                                                                                                                                                                                                                                 | El archivo no se transmitirá por secuencias a través de una red. Todas las secuencias tienen la misma importancia.<br/>                                                                                                                                                                                       |
| Extensiones de unidad de datos               | Hay información importante relacionada con los ejemplos de una secuencia que se deben mantener con los ejemplos.                                                                                                                                                                                                                      | El archivo está pensado para entregarse a través de un ancho de banda restringido. En este caso, las extensiones de unidad de datos pueden utilizar demasiada sobrecarga.                                                                                                                                                    |



 

También es importante tener en cuenta las características de códec que desea usar con el archivo al crear un perfil. Para obtener más información, consulte [características de códec](codec-features.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Diseñar perfiles**](designing-profiles.md)
</dt> </dl>

 

 





