---
description: Campo DVINFO Configuración en el controlador MSDV
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Campo DVINFO Configuración en el controlador MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6823b13a055088df6e3e5ffa82c899a490a9b0d6b9b407b3b5244ca947c209b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966285"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a>Campo DVINFO Configuración en el controlador MSDV

En esta sección se describe cómo el controlador MSDV rellena la [**estructura DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo)

La `DVINFO` estructura define el bloque de formato para anclar conexiones entre MSDV y otros filtros. De forma predeterminada, el filtro divisor DV se usa al capturar desde un dispositivo DV y el filtro dv mux se usa al transmitir al dispositivo. Sin embargo, las aplicaciones pueden proporcionar sus propios filtros personalizados, por lo que resulta útil comprender cómo MSDV rellena el bloque `DVINFO` de formato.

La `DVINFO` estructura contiene la siguiente información:

-   Dos paquetes de origen auxiliares de audio (APACK), para el primer y segundo bloques de audio.
-   Dos paquetes de control de código fuente A ODBC, para el primer y segundo bloques de audio.
-   Un paquete de origen auxiliar de vídeo (CCA).
-   Un módulo de control de código fuente de SUD.

Cada fotograma de una secuencia DV contiene paquetes APACK y ️ . Sin embargo, el `DVINFO` bloque de formato es estático y solo se usa para establecer la conexión de pin. Cuando se conecta el controlador MSDV, no examina ninguno de los paquetes AJDBC o JDBC de la secuencia. En su lugar, usa un conjunto de valores predeterminados, en función de las siguientes características del dispositivo DV:

-   Si el dispositivo admite un formato de consumidor (DVCR) o un formato profesional (DVCPRO)
-   El tipo de señal
-   Si el formato es JPEG o PAL. (Si el dispositivo no informa de esta información, MSDV tiene como valor predeterminado la configuración de OMISIÓN).

Una vez que se inicia el streaming, es responsabilidad de los filtros de modo de usuario, como el divisor DV, examinar el contenido real de cada fotograma DV. Dado que la información puede cambiar de marco a marco, es posible que el filtro tenga que realizar un cambio de formato dinámico. Por ejemplo, si cambia la velocidad de audio, es posible que el filtro tenga que volver a negociar el tipo de audio.

Si captura un archivo DV de tipo 1, la estructura se escribe en el archivo como fragmento de formato de secuencia `DVINFO` ('strf'). Estos datos se toman directamente del bloque de formato proporcionado por MSDV. Como se indicó, el contenido real de la secuencia podría ser diferente. Es responsabilidad de la aplicación examinar los paquetes A EXAMIN y EXAMIN en cada fotograma.

En los temas siguientes, puede encontrar tablas que enumeran todos los campos usados por MSDV.

-   [Paquete de origen (AS) de APACK](aaux-source--as--pack.md)
-   [Paquete de control de código fuente (ASC) de AJUN](aaux-source-control--asc--pack.md)
-   [Paquete de origen (VS) de LOA](vaux-source--vs--pack.md)
-   [Paquete de control de código fuente (VSC)](vaux-source-control--vsc--pack.md)

Al leer estas tablas, consulte las especificaciones siguientes:

-   IEC 61834
-   SMPTE 314 M
-   SMPTE 370

En cada tabla, la primera columna proporciona el código de campo, seguido del número de bits (entre paréntesis). Las columnas restantes dan los valores de campo. Muchos de los campos AVB y VB no son pertinentes para la conexión de pin, en cuyo caso MSDV establece un valor ficticio. El valor numérico de todo el paquete se muestra en la parte inferior de cada tabla.

Las notas después de cada tabla dan más información sobre los campos seleccionados. Para obtener descripciones completas, consulte las especificaciones. Además, algunos campos no tienen el mismo significado en SMPTE 314M/SMPTE 370 que en IEC 61834.

> [!Note]  
> Actualmente, DirectShow no admite formatos DVCPRO. Los valores enumerados para los formatos DVCPRO se definen para su uso futuro.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Datos DV en formato de archivo AVI](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[Controlador MSDV](msdv-driver.md)
</dt> </dl>

 

 



