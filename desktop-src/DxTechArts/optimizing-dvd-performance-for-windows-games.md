---
title: Optimización del rendimiento de DVD para Windows Games
description: En este artículo se describe cómo optimizar el rendimiento de DVD para Windows juegos.
ms.assetid: 01e8dc7d-4ba7-40dd-d845-a20000201ae1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe08ba6188df9b8bbc25a73595bf1509b257696955c1fcbd1ae98091b3c8aecf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042545"
---
# <a name="optimizing-dvd-performance-for-windows-games"></a>Optimización del rendimiento de DVD para Windows Games

Un alto porcentaje de equipos que ejecutan Windows una unidad de DVD y muchos juegos se envían en DVD. Como resultado, se recomienda asegurarse de que los juegos usan la unidad de DVD para sacar el máximo partido. Al comprender cómo se leen los datos de un DVD y cómo la ubicación de los datos afecta a su tiempo de lectura, puede reducir los tiempos de carga y mejorar el rendimiento general durante el juego. En este artículo se describe cómo optimizar el rendimiento de DVD para Windows juegos.

-   [Diseño básico de un DVD](#basic-layout-of-a-dvd)
-   [Lectura desde un DVD](#reading-from-a-dvd)
-   [Errores de lectura](#reading-errors)
-   [Rendimiento de los datos](#data-throughput)
-   [Ejemplos de rendimiento desperdiciado](#examples-of-wasted-throughput)
-   [Lectura sincrónica frente a asincrónica](#reading-synchronously-vs-asynchronously)
-   [Lectura óptima](#reading-optimally)
-   [Compatibilidad de DVD](#dvd-compatibility)
-   [Resumen](#summary)

## <a name="basic-layout-of-a-dvd"></a>Diseño básico de un DVD

En esta ilustración se muestra el diseño básico de un DVD.

![diseño de dvd](images/dvdsector.png)

Los datos de un DVD se almacenan como continuos, como en un CD. sin embargo, los archivos se divide en bloques y sectores. Los archivos se reparten entre bloques de código de corrección de errores (ECC) y cada bloque se divide en 16 sectores de 2 KB (es decir, 32 KB de datos en cada bloque). Los archivos se alinean a lo largo de los límites del sector y cualquier espacio no usado en un sector se deja vacío. Si un archivo solo tiene 10 bytes, se desperdicia el resto del espacio de ese sector de 2 KB; por lo que, cuando sea posible, agrupa los archivos en incrementos de 2 KB para obtener la mejor densidad de datos. Tenga en cuenta que estas especificaciones son solo para DVD, y cd y HD-DVD tienen especificaciones diferentes.

## <a name="reading-from-a-dvd"></a>Lectura desde un DVD

Esta es la secuencia que se ejecuta una unidad de DVD al recibir una solicitud de lectura de un DVD:

1.  Cambiar capas, si es necesario
2.  Seek
3.  Reenfoque la unidad de recogida óptica (OPU) para leer los datos.
4.  Comprobación de la posición real
5.  Ajustar y repetir hasta que se encuentran los datos correctos

Las operaciones de lectura de unidades se cuantifican de forma diferente, dependiendo de si son lecturas de unidades lógicas o lecturas de unidades físicas. Las lecturas de unidades lógicas solo pueden leer una cantidad entera de sectores de DVD, mientras que una solicitud de lectura de unidad física solo puede leer una cantidad entera de bloques ECC. Normalmente, la unidad física recibe una solicitud de lectura; intentará rellenar su memoria caché. El tamaño de caché de la unidad de DVD depende de las especificaciones de cada unidad.

Cuando una unidad de DVD obtiene una solicitud de lectura que supera el tamaño de caché, la solicitud se divide en solicitudes de tamaño de caché. La unidad busca el bloque ECC que contiene el primer sector de la solicitud y lee todo el bloque ECC. El firmware de la unidad descodifica el bloque ECC y, a continuación, lee el siguiente bloque ECC. El proceso se repite hasta que se rellena la caché de unidades o se cumplen todas las solicitudes. A continuación, el kernel lee los datos descodificados de la caché de unidades. A continuación, vacía la memoria caché e inicia la siguiente operación de lectura, si quedan solicitudes de lectura.

> [!Note]  
> Cada lectura sin almacenar en caché vacía la caché de unidades.

 

## <a name="reading-errors"></a>Errores de lectura

Los DVD y las unidades de DVD no son perfectos y pueden producirse errores durante la lectura. Al igual que los CD, las partes de un DVD pueden volverse ilegibles a partir de tierra o de rasguñas. Si alguna parte de un bloque es ilegible, todo el bloque se considera ilegible. Si se produce un error de lectura, la unidad intenta volver a leer el bloque ECC. Si el bloque sigue siendo ilegible, la unidad anula la operación de lectura y devuelve un valor al kernel que indica que el bloque era ilegible. A continuación, el kernel decide qué paso seguir a continuación. El kernel puede volver a emitir la solicitud, anular la lectura por completo o girar la unidad hacia abajo y volver a emitir la solicitud.

## <a name="data-throughput"></a>Rendimiento de los datos

El rendimiento de los datos de una unidad de DVD depende de varios factores: la ubicación de los datos solicitados, la limpieza o el rascado del disco, el número de secuencias que se leen desde el disco, el tamaño de los búferes asociados a esos flujos y las especificaciones de la unidad individual. El rendimiento también depende de si la unidad tiene velocidad angular constante (CONSTANT) o velocidad lineal constante (CLV). Si una unidad gira con SPIN, el disco gira a la misma velocidad, independientemente de dónde se encuentra la unidad de recogida óptica (OPU). Esto significa que la pista de datos se mueve más rápido más allá de la OPU a medida que la OPU se acerca al borde exterior del disco. Con CLV, el disco gira más lentamente a medida que la OPU se mueve hacia el exterior, por lo que la pista de datos se mueve más allá de la OPU a una velocidad constante. Las unidades de DVD de la mayoría de los equipos usan CLV.

Mientras la unidad busca y cambia capas, los datos no se pueden leer desde el disco. Es un procedimiento recomendado minimizar estas operaciones, especialmente al leer los datos de una pantalla de carga inicial.

## <a name="examples-of-wasted-throughput"></a>Ejemplos de rendimiento desperdiciado

Para entender cómo se puede desperdiciar el rendimiento de los datos, considere una unidad hipotética y un DVD. Supongamos que es necesario leer un archivo en medio del disco. El rendimiento de esa área del disco es de aproximadamente 8,25 MB/s. Si el trazo de búsqueda es medio o un tercero de completo, el tiempo medio de búsqueda es de 150 ms. En este ejemplo, se podrían haber leído 1,2 MB (150 ms × 8,25 MB/s) en el tiempo que tardó solo en obtener la OPU donde se puede leer. La adición de un cambio de capa eleva el rendimiento desperdiciado a 1,8 MB (225 ms × 8,25 MB/s).

Otro ejemplo que muestra el rendimiento desperdiciado es la carga de 20 archivos mal ubicados desde una unidad UDP sin cambios de capa. Si el tiempo de búsqueda de cada archivo, más la latencia antes de que se puedan leer los datos, es de aproximadamente 200 ms, se dedican 4 segundos (20 archivos × 200 ms) a buscar los datos. Si los archivos se encuentran en el borde exterior y se leen a una velocidad de 11×, el rendimiento promedia 15,2 MB/s (11 velocidad/12 velocidad × 16 MB/s). El rendimiento desperdiciado en este ejemplo es de aproximadamente 60,8 MB (15,2 MB/s × 4 s).

## <a name="reading-synchronously-vs-asynchronously"></a>Lectura sincrónica frente a asincrónica

La lectura asincrónica es más eficaz que la lectura sincrónica. Al leer sincrónicamente, uno o varios bloques ecc de datos se leen en la memoria del sistema antes de copiarse en la memoria de la aplicación. En cambio, la lectura asincrónica copia los bloques ECC descodificados directamente en la memoria de la aplicación, lo que evita la memoria caché L2 y crea menos sobrecarga de CPU. Para leer de forma asincrónica, use la marca FILE \_ FLAG \_ OVERLAPPED al usar la [**función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir archivos. La [**función ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) también necesita una estructura OVERLAPPED válida pasada para realizar E/S asincrónica.

Puede encontrar más información sobre la E/S asincrónica en [E/S](/windows/desktop/FileIO/synchronous-and-asynchronous-i-o)sincrónica y asincrónica.

## <a name="reading-optimally"></a>Lectura óptima

El mejor principio para leer desde un DVD es evitar buscar y leer pequeñas cantidades de datos. Cuando la cantidad de datos leídos es menor que la capacidad de un bloque ECC (menos de 32 KB), se desperdicia el resto del bloque. Dado que los tamaños de caché varían de unidad a unidad, los desarrolladores deben decidir una cantidad mínima de datos para las solicitudes de lectura y no hacer nada más pequeño que eso. El tamaño mínimo debe ser un número entero múltiplo de un bloque ECC para evitar perder tiempo en la lectura y la decodificación de datos que no se usarán. También es importante evitar la búsqueda a toda costa, ya que cualquier tiempo dedicado a buscar es el tiempo dedicado a no leer datos.

## <a name="dvd-compatibility"></a>Compatibilidad de DVD

Hay algunos problemas de compatibilidad importantes que debe tener en cuenta al publicar en DVD. En primer lugar, las unidades de DVD de los equipos basados en Windows pueden variar en cuanto al rendimiento, por lo que si el DVD tiene un requisito específico de rendimiento, es importante asegurarse de que el hardware de los usuarios cumple esos requisitos. Además, los DVD multicapa pueden causar problemas de compatibilidad en algunas unidades de DVD. Para evitar estos problemas, es aconsejable entregar un DVD de una sola capa o probar exhaustivamente un DVD de varias capas en la mayoría de las unidades antes del lanzamiento.

## <a name="summary"></a>Resumen

Para mejorar el rendimiento del DVD, se pueden aplicar algunas reglas generales. Las técnicas siguientes pueden ayudar a maximizar el rendimiento y reducir los datos desperdiciados:

-   Evitar lecturas de menos de 32 KB
-   Análisis de datos para reducir o eliminar búsquedas
-   Definición de datos en límites de bloque ecc
-   Maximice la capacidad mediante la agrupación de archivos pequeños en bloques de 2 KB y reduzca el espacio de relleno en los sectores de DVD.
-   Lectura asincrónica para reducir la carga de CPU y el uso excesivo de memoria
-   Evitar la liberación de DVD multicapa

 

 