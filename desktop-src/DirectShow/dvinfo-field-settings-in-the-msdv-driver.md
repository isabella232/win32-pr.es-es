---
description: Configuración del campo DVINFO en el controlador MSDV
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Configuración del campo DVINFO en el controlador MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806151"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a>Configuración del campo DVINFO en el controlador MSDV

En esta sección se describe cómo el controlador MSDV rellena la estructura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .

La `DVINFO` estructura define el bloque de formato para las conexiones de PIN entre MSDV y otros filtros. De forma predeterminada, se usa el filtro de divisor DV al capturar desde un dispositivo DV y se usa el filtro DV MUX al transmitir al dispositivo. Sin embargo, las aplicaciones pueden proporcionar sus propios filtros personalizados, por lo que resulta útil entender cómo MSDV rellena el `DVINFO` bloque de formato.

La `DVINFO` estructura contiene la siguiente información:

-   Dos paquetes de origen auxiliares de audio (AAUX), para el primer y el segundo bloque de audio.
-   Dos paquetes de control de código fuente de AAUX, para el primer y el segundo bloque de audio.
-   Un paquete de origen de vídeo auxiliar (VAUX).
-   Un módulo de control de código fuente de VAUX.

Cada fotograma de una secuencia DV contiene paquetes de AAUX y VAUX. Sin embargo, el `DVINFO` bloque de formato es estático y solo se usa para establecer la conexión del PIN. Cuando se conecta el controlador MSDV, no examina ninguno de los paquetes AAUX o VAUX de la secuencia. En su lugar, utiliza un conjunto de valores predeterminados, en función de las siguientes características del dispositivo DV:

-   Si el dispositivo admite un formato de consumidor (DVCR) o formato profesional (DVCPRO)
-   El tipo de señal
-   Si el formato es NTSC o PAL. (Si el dispositivo no informa de esta información, MSDV tiene como valor predeterminado la configuración de NTSC)

Una vez que se inicia el streaming, es responsabilidad de los filtros de modo de usuario, como el divisor de DV, examinar el contenido real de cada fotograma DV. Dado que la información puede cambiar de un marco a otro, es posible que el filtro tenga que realizar un cambio de formato dinámico. Por ejemplo, si la velocidad de audio cambia, es posible que el filtro tenga que volver a negociar el tipo de audio.

Si captura un archivo DV de tipo 1, la `DVINFO` estructura se escribe en el archivo como el fragmento de formato de secuencia (' strf '). Estos datos se toman directamente del bloque Format proporcionado por MSDV. Como se indicó, el contenido real de la secuencia puede ser diferente. Es responsabilidad de la aplicación examinar los paquetes AAUX y VAUX en cada fotograma.

En los temas siguientes, puede encontrar tablas que enumeran todos los campos usados por MSDV.

-   [Paquete de origen (AS) de AAUX](aaux-source--as--pack.md)
-   [Paquete de control de código fuente de AAUX (ASC)](aaux-source-control--asc--pack.md)
-   [Paquete de origen de VAUX (VS)](vaux-source--vs--pack.md)
-   [Paquete de control de código fuente de VAUX (VSC)](vaux-source-control--vsc--pack.md)

Al leer estas tablas, consulte las siguientes especificaciones:

-   IEC 61834
-   314M SMPTE
-   SMPTE 370

En cada tabla, la primera columna proporciona el código de campo, seguido del número de bits (entre paréntesis). Las columnas restantes proporcionan los valores de campo. Muchos de los campos AAUX y VAUX no son relevantes para la conexión de PIN, en cuyo caso MSDV establece un valor ficticio. El valor numérico de todo el paquete se muestra en la parte inferior de cada tabla.

Las notas después de cada tabla proporcionan más información acerca de los campos seleccionados. Para obtener descripciones completas, consulte las especificaciones. Además, algunos campos no tienen el mismo significado en SMPTE 314M/SMPTE 370 como en IEC 61834.

> [!Note]  
> Actualmente, DirectShow no admite formatos DVCPRO. Los valores enumerados para los formatos DVCPRO se definen para su uso futuro.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Datos de DV en el formato de archivo AVI](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[Controlador MSDV](msdv-driver.md)
</dt> </dl>

 

 



