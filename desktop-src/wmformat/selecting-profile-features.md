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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466211"
---
# <a name="selecting-profile-features"></a>Selección de características de perfil

En la tabla siguiente se enumeran las características del perfil y se describe cuándo desea o no desea usarlas.



| Característica                            | Cuándo se usa                                                                                                                                                                                                                                                                                                                | Cuándo no debe usarse                                                                                                                                                                                                                                                                     |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exclusión mutua por velocidad de bits (MBR) | El archivo se transmitirá a una audiencia con velocidades de conexión que varían de usuario a usuario (por ejemplo, archivos entregados a través de Internet).                                                                                                                                                                              | El archivo no se transmitirá a través de una red. El archivo se transmitirá a través de una red con un ancho de banda disponible coherentemente confiable (por ejemplo, los archivos entregados a través de una red de área local corporativa).<br/>                                                              |
| Exclusión mutua por idioma       | El archivo contiene secuencias que duplican los mismos datos en distintos idiomas. (Por ejemplo, una película con forma de estrella en varios idiomas tendría la descodificación codificada como secuencias mutuamente excluyentes).                                                                                                                         | El archivo solo contiene secuencias en un solo idioma. Si el archivo contiene solo secuencias que se deben cambiar para idiomas individuales, puede ser más sencillo crear un archivo para cada idioma (por ejemplo, para una película de entrenamiento con una gran cantidad de texto en la secuencia de vídeo).<br/> |
| Exclusión mutua por presentación   | Quiere proporcionar vídeo en más de una relación de aspecto. Por ejemplo, un archivo puede contener el mismo vídeo con formato de televisión y para el formato de pantalla ancha original.                                                                                                                                     | Solo hay una versión de cada secuencia de vídeo.                                                                                                                                                                                                                                    |
| Uso compartido de ancho de banda                  | El archivo se transmitirá y tiene dos o más secuencias que, cuando se combinan, usan menos ancho de banda disponible que los valores de velocidad de bits de ambos flujos agregados juntos. Dado que la velocidad de bits de una secuencia es básicamente el ancho de banda máximo necesario para la secuencia, algunas secuencias pueden tener algunos períodos de transferencia de datos inferiores. | El archivo no se transmitirá a través de una red. Todas las secuencias tienen velocidades de bits coherentes.<br/>                                                                                                                                                                                     |
| Priorización de secuencias              | El archivo se transmitirá y algunas secuencias son más importantes que otras.                                                                                                                                                                                                                                                 | El archivo no se transmitirá a través de una red. Todas las secuencias tienen la misma importancia.<br/>                                                                                                                                                                                       |
| Extensiones de unidad de datos               | Hay información importante relacionada con los ejemplos de una secuencia que se debe conservar con los ejemplos.                                                                                                                                                                                                                      | El archivo está pensado para la entrega a través de un ancho de banda restringido. En este caso, las extensiones de unidad de datos pueden usar demasiada sobrecarga.                                                                                                                                                    |



 

También es importante tener en cuenta las características de códec que desea usar con el archivo al crear un perfil. Para obtener más información, vea [Características de códec.](codec-features.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Diseño de perfiles**](designing-profiles.md)
</dt> </dl>

 

 





