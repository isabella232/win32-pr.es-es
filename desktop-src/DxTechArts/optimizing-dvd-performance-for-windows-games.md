---
title: Optimizar el rendimiento de DVD para juegos de Windows
description: En este artículo se describe cómo optimizar el rendimiento de DVD para juegos de Windows.
ms.assetid: 01e8dc7d-4ba7-40dd-d845-a20000201ae1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb15063d0441423ccb3a9f67db84caa134f801c6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665841"
---
# <a name="optimizing-dvd-performance-for-windows-games"></a>Optimizar el rendimiento de DVD para juegos de Windows

Un porcentaje alto de equipos que ejecutan Windows tienen una unidad de DVD y muchos juegos se distribuyen en DVD. Como resultado, se recomienda asegurarse de que los juegos usan la unidad de DVD para sacar el máximo partido. Al comprender cómo se leen los datos de un DVD y cómo afecta la ubicación de los datos a su tiempo de lectura, puede reducir los tiempos de carga y mejorar el rendimiento global durante la reproducción de juegos. En este artículo se describe cómo optimizar el rendimiento de DVD para juegos de Windows.

-   [Diseño básico de un DVD](#basic-layout-of-a-dvd)
-   [Lectura desde un DVD](#reading-from-a-dvd)
-   [Errores de lectura](#reading-errors)
-   [Rendimiento de los datos](#data-throughput)
-   [Ejemplos de rendimiento desperdiciado](#examples-of-wasted-throughput)
-   [Leer sincrónicamente frente a asincrónicamente](#reading-synchronously-vs-asynchronously)
-   [Lectura óptima](#reading-optimally)
-   [Compatibilidad con DVD](#dvd-compatibility)
-   [Resumen](#summary)

## <a name="basic-layout-of-a-dvd"></a>Diseño básico de un DVD

En esta ilustración se muestra el diseño básico de un DVD.

![diseño de DVD](images/dvdsector.png)

Los datos de un DVD se almacenan como espirales continuas, como en un CD; sin embargo, los archivos se dividen en bloques y sectores. Los archivos se propagan a través de bloques de código de corrección de errores (ECC) y cada bloque se divide en sectores de 16 2 KB (es decir, 32 KB de datos en cada bloque). Los archivos se alinean a lo largo de los límites del sector y cualquier espacio no utilizado en un sector se deja vacío. Si un archivo tiene solo 10 bytes, se desperdicia el resto del espacio en ese sector de 2 KB. por tanto, cuando sea posible, agrupe archivos en incrementos de 2 KB para obtener la mejor densidad de datos. Tenga en cuenta que estas especificaciones son solo para DVD y CD y HD-DVD tienen diferentes especificaciones.

## <a name="reading-from-a-dvd"></a>Lectura desde un DVD

Esta es la secuencia que se ejecuta en una unidad de DVD tras recibir una solicitud de lectura de un DVD:

1.  Cambiar capas, si es necesario
2.  Seek
3.  Reenfoque de la unidad de recogida óptica (OPU) para leer datos
4.  Comprobar la posición real
5.  Ajustar y repetir hasta que se encuentren los datos correctos

Las operaciones de lectura de unidad se cuantifican de manera diferente, dependiendo de si son lecturas de unidad lógica o lecturas de unidad física. Las lecturas de unidades lógicas solo pueden leer una cantidad Integer de sectores de DVD, mientras que una solicitud de lectura de unidad física solo puede leer una cantidad entera de bloques ECC. Normalmente, la unidad física recibe una solicitud de lectura; intentará rellenar su memoria caché. El tamaño de la memoria caché de la unidad de DVD depende de las especificaciones de la unidad individual.

Cuando una unidad de DVD obtiene una solicitud de lectura que supera el tamaño de la memoria caché, la solicitud se divide en solicitudes de tamaño de caché. La unidad busca el bloque ECC que contiene el primer sector de la solicitud y Lee todo el bloque ECC. El firmware de la unidad descodifica el bloque ECC y, a continuación, lee el siguiente bloque ECC. El proceso se repite hasta que se completa la memoria caché de la unidad o se cumplen todas las solicitudes. A continuación, el kernel Lee los datos descodificados de la memoria caché de la unidad. A continuación, vacía la memoria caché e inicia la siguiente operación de lectura, si queda alguna solicitud de lectura.

> [!Note]  
> Cada lectura no almacenada en caché vacía la memoria caché de la unidad.

 

## <a name="reading-errors"></a>Errores de lectura

Los DVDs y las unidades de DVD no son perfectos, y pueden producirse errores durante la lectura. Al igual que los CDs, las partes de un DVD se pueden volver ilegibles de polvo o arañazos. Si alguna parte de un bloque es ilegible, el bloque entero se considera ilegible. Si se produce un error de lectura, la unidad intenta volver a leer el bloque ECC. Si todavía no se puede leer el bloque, la unidad anula la operación de lectura y devuelve un valor al kernel que indica que el bloque no se puede leer. A continuación, el kernel decide qué paso debe tomar a continuación. El kernel puede volver a emitir la solicitud, anular la lectura por completo, o bien girar la unidad y volver a emitir la solicitud.

## <a name="data-throughput"></a>Rendimiento de los datos

El rendimiento de los datos de una unidad de DVD depende de varios factores: la ubicación de los datos solicitados, la limpieza o el arañazo del disco, el número de flujos que se leen desde el disco, el tamaño de los búferes asociados a esos flujos y las especificaciones de la unidad individual. El rendimiento también depende de si la unidad tiene una velocidad angular constante (CAV) o una velocidad lineal constante (CLV). Si una unidad gira con CAV, el disco gira a la misma velocidad, independientemente de dónde se encuentre la unidad de recogida óptica (OPU). Esto significa que la pista de datos se mueve más allá del OPU más rápido, ya que el OPU se acerca al borde exterior del disco. Con CLV, el disco gira más lentamente a medida que el OPU se mueve hacia afuera, por lo que la pista de datos pasa más allá de la OPU a una velocidad constante. Las unidades de DVD de la mayoría de los equipos usan CLV.

Mientras la unidad está buscando y cambiando capas, los datos no se pueden leer desde el disco. Es recomendable minimizar estas operaciones, especialmente al leer datos de una pantalla de carga inicial.

## <a name="examples-of-wasted-throughput"></a>Ejemplos de rendimiento desperdiciado

Para entender cómo se puede desperdiciar el rendimiento de los datos, considere la posibilidad de usar una unidad y un DVD hipotéticos. Supongamos que se debe leer un archivo en medio del disco. El rendimiento de esa área del disco es de aproximadamente 8,25 MB/s. Si el trazo de búsqueda es una mitad o un tercio de la totalidad, el tiempo medio de búsqueda es de 150 ms. En este ejemplo, se podría haber leído 1,2 MB (150 ms × 8,25 MB/s) en el momento en que se tomó el OPU hasta el punto en el que se puede leer. Agregar un cambio de capa eleva el rendimiento desperdiciado a 1,8 MB (225 MS × 8,25 MB/s).

Otro ejemplo que muestra el rendimiento desperdiciado es la carga de 20 archivos de ubicación incorrecta desde una unidad CAV sin cambios de capa. Si el tiempo de búsqueda de cada archivo, más la latencia antes de que se puedan leer los datos, es de aproximadamente 200 ms y, a continuación, se emplean 4 segundos (20 archivos × 200 ms) simplemente buscando los datos. Si los archivos se encuentran en el diámetro exterior y se leen a las 11 × velocidad, el rendimiento calcula el promedio de 15,2 MB/s (11 velocidad/12 velocidad × 16 MB/s). El rendimiento desperdiciado en este ejemplo es de aproximadamente 60,8 MB (15,2 MB/s × 4 segundos).

## <a name="reading-synchronously-vs-asynchronously"></a>Leer sincrónicamente frente a asincrónicamente

La lectura asincrónica es más eficaz que la lectura sincrónica. Al leer sincrónicamente, uno o varios bloques ECC de datos se leen en la memoria del sistema antes de que se copien en la memoria de la aplicación. En cambio, la lectura asincrónica copia los bloques ECC descodificados directamente en la memoria de la aplicación, lo que evita la caché L2 y crea menos sobrecarga de la CPU. Para leer de forma asincrónica, use la marca de la marca de archivo \_ \_ superpuesta al utilizar la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir los archivos. La función [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) también necesita que se pase una estructura superpuesta válida para realizar la e/s asincrónica.

Puede encontrar más información sobre la e/s asincrónica en [e/s sincrónica y asincrónica](/windows/desktop/FileIO/synchronous-and-asynchronous-i-o).

## <a name="reading-optimally"></a>Lectura óptima

El mejor principio para leer desde un DVD es evitar la búsqueda y la lectura de pequeñas cantidades de datos. Cuando la cantidad de datos leídos es menor que la capacidad de un bloque ECC (menos de 32 KB), se desperdicia el resto del bloque. Dado que los tamaños de caché varían de una unidad a otra, los desarrolladores deben decidir una cantidad mínima de datos para las solicitudes de lectura y no hacer más pequeñas que eso. El tamaño mínimo debe ser un entero múltiplo de un bloque ECC para evitar perder tiempo en leer y descodificar datos que no se usarán. También es importante evitar la búsqueda en todos los costos, ya que el tiempo dedicado a la búsqueda es el tiempo invertido en no leer los datos.

## <a name="dvd-compatibility"></a>Compatibilidad con DVD

Hay algunos problemas de compatibilidad importantes que se deben tener en cuenta al liberar en DVD. En primer lugar, las unidades de DVD de equipos basados en Windows pueden variar en cuanto a rendimiento, por lo que si el DVD tiene un requisito específico de rendimiento, es importante asegurarse de que el hardware de los usuarios cumple esos requisitos. Además, los DVDs multinivel pueden provocar problemas de compatibilidad en algunas unidades de DVD. Para evitar estos problemas, se recomienda ofrecer un DVD de una sola capa o probar exhaustivamente un DVD de varias capas en una mayoría de las unidades antes de la versión.

## <a name="summary"></a>Resumen

Para mejorar el rendimiento del DVD, se pueden aplicar algunas reglas generales. Las técnicas siguientes pueden ayudar a maximizar el rendimiento y reducir los datos desperdiciados:

-   Evite lecturas inferiores a 32 KB
-   Disposición de los datos para reducir o eliminar las búsquedas
-   Disposición de los datos en los límites de bloque ECC
-   Maximice la capacidad mediante la agrupación de archivos pequeños en bloques de 2 KB y reduzca el espacio de relleno en los sectores de DVD
-   Leer de forma asincrónica para reducir la carga de la CPU y el uso excesivo de memoria
-   Evitar la liberación de DVDs multinivel

 

 