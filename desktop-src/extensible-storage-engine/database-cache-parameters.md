---
description: 'Más información acerca de: parámetros de caché de base de datos'
title: Parámetros de caché de base de datos
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715413"
---
# <a name="database-cache-parameters"></a>Parámetros de caché de base de datos


_**Se aplica a:** Windows | Windows Server_

## <a name="database-cache-parameters"></a>Parámetros de caché de base de datos

Este tema contiene los parámetros que se utilizan para la caché de base de datos.

*JET_paramBatchIOBufferMax*  
22  

Este parámetro controla el tamaño de una parte auxiliar de la memoria caché de páginas de base de datos que se usa para simular la e/s de recopilación de dispersión cuando, de lo contrario, no está disponible. El tamaño está en páginas de base de datos.

**Windows XP y versiones posteriores:**  Este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>256</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0,2:2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramCacheSize*  
41  

Este parámetro se puede utilizar para controlar el tamaño de la memoria caché de páginas de base de datos en tiempo de ejecución. Normalmente, la memoria caché ajustará automáticamente su tamaño como una función de los niveles de actividad de la base de datos y del equipo. Si la aplicación establece este parámetro en cero, la memoria caché ajustará su propio tamaño de esta manera. Sin embargo, si la aplicación establece este parámetro en un valor distinto de cero, la memoria caché se ajustará a ese tamaño de destino (en páginas de base de datos). La caché conservará su tamaño en ese umbral hasta que se le proporcione un nuevo tamaño o hasta que se libere para elegir su propio tamaño.

**Nota:**  El tamaño de la caché sigue sujeto a los límites impuestos por **JET_paramCacheSizeMin** y **JET_paramCacheSizeMax**.

Cuando se lee este parámetro, se devuelve el tamaño real de la memoria caché en páginas de base de datos. La aplicación puede usar este tamaño como entrada para impulsar su ajuste manual del tamaño de la memoria caché.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>Especial</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramCacheSizeMin*  
60  

Este parámetro configura el tamaño mínimo de la caché de páginas de base de datos. El tamaño está en páginas de base de datos.

De forma predeterminada, la memoria caché de base de datos ajustará automáticamente su tamaño entre los límites establecidos por **JET_paramCacheSizeMin** y **JET_paramCacheSizeMax**.

**Windows 2000:**  En Windows 2000, este parámetro debe establecerse en un valor que sea aproximadamente igual a cuatro veces el número de subprocesos que estarán dentro de la API de ESE al mismo tiempo. Esto es necesario para evitar interbloqueos causados por un número insuficiente de búferes de caché de páginas de base de datos para realizar operaciones complejas como divisiones de árbol B +.

**Windows XP y versiones posteriores:**  El administrador de caché establecerá automáticamente su propio tamaño de caché mínimo para evitar los interbloqueos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p><strong>Windows 2000:</strong>  64</p>
<p><strong>Windows XP:</strong>  1</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p><strong>Windows 2000:</strong>  No</p>
<p><strong>Windows XP:</strong>  ?</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows 2000:</strong>  No</p>
<p><strong>Windows XP:</strong>  ?</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramCacheSizeMax*  
23  

Este parámetro configura el tamaño máximo de la caché de páginas de base de datos. El tamaño está en páginas de base de datos.

De forma predeterminada, la memoria caché de base de datos ajustará automáticamente su tamaño entre los límites establecidos por **JET_paramCacheSizeMin** y **JET_paramCacheSizeMax**.

**Nota:**   Si este parámetro se deja en su valor predeterminado, el tamaño máximo de la memoria caché se establecerá en el tamaño de la memoria física cuando se llame a [JetInit](./jetinit-function.md) .

**Windows Vista:**  A partir de Windows Vista, el valor predeterminado de este parámetro se ha cambiado para aclarar este comportamiento.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  512</p>
<p><strong>Windows Vista:</strong>  2 mil millones</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p><strong>Windows 2000:</strong>  No</p>
<p><strong>Windows XP:</strong>  ?</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows XP y windows 2000:</strong>  No</p>
<p><strong>Windows Vista y Windows Server 2003:</strong>  ?</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramCheckpointDepthMax*  
24 

Este parámetro controla el modo en que se vacían las páginas de base de datos de forma agresiva desde la memoria caché de páginas de base de datos para minimizar la cantidad de tiempo que se tarda en recuperarse de un bloqueo. El parámetro es un umbral en bytes para el número de archivos de registro de transacciones que se deben reproducir después de un bloqueo.

Si el registro circular está habilitado mediante [JET_paramCircularLog](./transaction-log-parameters.md) , este parámetro también controlará la cantidad aproximada de archivos de registro de transacciones que se conservarán en el disco.

Es importante que este parámetro no se establezca demasiado bajo. Como el valor de este parámetro se aproxima a cero, la memoria caché se vuelve más agresiva al vaciar páginas de base de datos en el disco. Esto no solo da como resultado un mayor número de operaciones de escritura en los archivos de base de datos, pero también provoca indirectamente un mayor número de lecturas en esos archivos. Esto puede producir problemas de rendimiento muy significativos en algunos casos. Desafortunadamente, el establecimiento del valor óptimo más pequeño para este parámetro solo se puede realizar mediante experimentación con la aplicación de destino.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>20971520</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  0 – 2147483647</p>
<p><strong>Windows Vista:</strong>  Todos los valores</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> Este parámetro es global.</p>
<p><strong>Windows Vista:</strong>  Este parámetro es por instancia.</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramCheckpointIOMax*  
135  

Este parámetro controla el número máximo de escrituras simultáneas que utilizará el motor de base de datos para vaciar las páginas de base de datos modificadas con el fin de avanzar el punto de control. El valor de este parámetro puede usarse para equilibrar la velocidad con la que el punto de control puede ser avanzado frente al impacto negativo que este proceso tendrá en el tiempo de respuesta para otras operaciones de e/s en los discos que contienen la base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>96</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>8:1024</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows Vista y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableViewCache*  
127  

Cuando este parámetro es **true**, el motor de base de datos usará los datos de la base de datos directamente desde la memoria caché de archivos de Windows en lugar de copiar los datos almacenados en caché en su propia memoria privada. Cualquier dato de base de datos que se modifique se almacenará en la memoria caché privada.

La intención de este modo es reducir aún más la cantidad de memoria privada que usa el motor de base de datos para almacenar en caché los datos de la base de datos.

La memoria caché de vista solo se puede usar si el uso de la memoria caché de archivos de Windows está habilitado estableciendo JET_paramEnableFileCache en **true**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows Vista y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKCorrInterval*  
25  

Este parámetro establece el intervalo de tiempo en microsegundos en el que se considera que dos accesos a las páginas de base de datos están correlacionados. Este intervalo de correlación controla la sensibilidad del algoritmo de sustitución de páginas (LRU-K) de la memoria caché en los accesos de página sucesivos. Esto, a su vez, afectará a las páginas que decida mantener almacenadas en caché.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>128000</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003: </strong>    0 – 2147483647</p>
<p><strong>Windows Vista:</strong>  Todos los valores</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKHistoryMax*  
26  

Este parámetro establece el número máximo de páginas de base de datos no almacenadas en caché para las que se conservarán los tiempos de acceso a las páginas de base de datos. Estos registros de historial permiten que el algoritmo de sustitución de páginas de la memoria caché (LRU-K) detecte con más precisión las páginas populares que se expulsaron erróneamente de la caché de páginas de base de datos.

**Windows XP y Windows Server 2003:**  Este parámetro se omite en Windows XP y Windows Server 2003 y no afecta al funcionamiento del motor de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p><strong>Windows 2000:</strong>  1024</p>
<p><strong>Windows Vista:</strong>  100000</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000:</strong>  0 – 4194303</p>
<p><strong>Windows Vista:</strong>  Todos los valores</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKPolicy*  
27  

Este parámetro configura el número de accesos a páginas de base de datos que se tienen en cuenta para determinar la utilidad de la página. Este parámetro es esencialmente el K de LRU-K, el algoritmo de reemplazo de páginas de la caché de páginas de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1-2</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKTimeout*  
28

Este parámetro indica el período de tiempo, en segundos, tras el cual se considera que una página de la memoria caché de páginas de base de datos ha perdido el acceso a la página con el fin de considerar la utilidad de la página.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  1 – 2147483647</p>
<p><strong>Windows Vista:</strong>   1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKTrxCorrInterval*  
29  

Este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.

*JET_paramStartFlushThreshold*  
31  

Este parámetro controla si la memoria caché de páginas de base de datos empieza a expulsar páginas de la memoria caché para dejar espacio a las páginas que no están almacenadas en caché. Cuando el número de búferes de página en la memoria caché cae por debajo de este umbral, se iniciará un proceso en segundo plano para reponer ese grupo de búferes disponibles. Este umbral siempre es relativo al tamaño máximo de la memoria caché establecido por **JET_paramCacheSizeMax**. Este umbral también debe ser siempre inferior al umbral de detención establecido por **JET_paramStopFlushThreshold**.

El alto de distancia del umbral de inicio determinará el tiempo de respuesta que debe tener la caché de páginas de base de datos para generar los búferes disponibles antes de que la aplicación los necesite. Un umbral de inicio alto proporcionará al proceso en segundo plano más tiempo para reaccionar. Sin embargo, un umbral de inicio alto implica un umbral de detención mayor y reduce el tamaño efectivo de la caché de páginas de base de datos para las páginas modificadas (Windows 2000) o para todas las páginas (Windows XP y versiones posteriores).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  5 (1%)</p>
<p><strong>Windows Vista:</strong>  20 millones (1%)</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p>
<p><strong>Windows Vista:</strong>  Todos los valores</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramStopFlushThreshold*  
32  

Este parámetro controla cuándo la memoria caché de páginas de base de datos termina la expulsando páginas de la memoria caché para dejar espacio a las páginas que no están almacenadas en caché. Cuando el número de búferes de página de la memoria caché supera este umbral, se detiene el proceso en segundo plano que se inició para reponer el grupo de búferes disponibles. Este umbral siempre es relativo al tamaño máximo de la memoria caché establecido por **JET_paramCacheSizeMax**. Este umbral también debe ser siempre mayor que el umbral de inicio establecido por **JET_paramStartFlushThreshold**.

La distancia entre el umbral de inicio y el umbral de detención afecta a la eficacia con la que el proceso en segundo plano vacía las páginas de la base de datos. Una brecha más grande hará que sea más probable que se combinen las escrituras en páginas vecinas. Sin embargo, un umbral de detención alta reducirá el tamaño efectivo de la caché de páginas de base de datos para las páginas modificadas (Windows 2000) o para todas las páginas (Windows XP y versiones posteriores).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  10 (2%)</p>
<p><strong>Windows Vista:</strong>  40 millones (2%)</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p>
<p><strong>Windows Vista:</strong>  Todos los valores</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
