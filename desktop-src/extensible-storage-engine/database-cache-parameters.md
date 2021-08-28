---
description: 'Más información sobre: Parámetros de caché de base de datos'
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
ms.openlocfilehash: 43d51be7e2db82d64c70f6fa810be3caf4c6fbd8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984098"
---
# <a name="database-cache-parameters"></a>Parámetros de caché de base de datos


_**Se aplica a:** Windows | Windows Servidor_

## <a name="database-cache-parameters"></a>Parámetros de caché de base de datos

Este tema contiene parámetros que se usan para la memoria caché de la base de datos.

*JET_paramBatchIOBufferMax*  
22  

Este parámetro controla el tamaño de una parte auxiliar de la memoria caché de páginas de la base de datos que se usa para simular la E/S de recopilación de dispersión cuando, de lo contrario, no está disponible. El tamaño está en páginas de base de datos.

**Windows XP y versiones posteriores:**  Este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>256</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0, 2 – 2147483647</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramCacheSize*  
41  

Este parámetro se puede usar para controlar el tamaño de la caché de páginas de la base de datos en tiempo de ejecución. Normalmente, la memoria caché ajustará automáticamente su tamaño como una función de los niveles de actividad de la base de datos y la máquina. Si la aplicación establece este parámetro en cero, la memoria caché ajustará su propio tamaño de esta manera. Sin embargo, si la aplicación establece este parámetro en un valor distinto de cero, la memoria caché se ajustará a ese tamaño de destino (en páginas de base de datos). A continuación, la memoria caché mantendrá su tamaño en ese umbral hasta que se le haya dado un nuevo tamaño o hasta que se libera para elegir su propio tamaño.

**Nota**  El tamaño de caché sigue sujeto a los límites impuestos **por JET_paramCacheSizeMin** y **JET_paramCacheSizeMax**.

Cuando se lee este parámetro, se devuelve el tamaño real de la memoria caché en las páginas de la base de datos. La aplicación puede usar este tamaño como entrada para impulsar su ajuste manual del tamaño de caché.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>Especial</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramCacheSizeMin*  
60  

Este parámetro configura el tamaño mínimo de la caché de páginas de la base de datos. El tamaño está en páginas de base de datos.

De forma predeterminada, la caché de base de datos ajustará automáticamente su tamaño entre los límites **establecidos por JET_paramCacheSizeMin** y **JET_paramCacheSizeMax**.

**Windows 2000:**  En Windows 2000, este parámetro debe establecerse en un valor aproximadamente igual a cuatro veces el número de subprocesos que estarán dentro de la API de ESE al mismo tiempo. Esto es necesario para evitar interbloqueos causados por un número insuficiente de búferes de caché de páginas de base de datos para realizar operaciones complejas como divisiones de árbol B+.

**Windows XP y versiones posteriores:**  El administrador de caché establecerá automáticamente su propio tamaño mínimo de caché para evitar interbloqueos.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p><strong>Windows 2000:</strong> 64</p><p><strong>Windows XP:</strong> 1</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p><strong>Windows 2000:</strong>  No</p><p><strong>Windows XP:</strong>  Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p><strong>Windows 2000:</strong>  No</p><p><strong>Windows XP:</strong>  Sí</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramCacheSizeMax*  
23  

Este parámetro configura el tamaño máximo de la caché de páginas de la base de datos. El tamaño está en páginas de base de datos.

De forma predeterminada, la caché de base de datos ajustará automáticamente su tamaño entre los límites establecidos **por JET_paramCacheSizeMin** y **JET_paramCacheSizeMax**.

**Nota**   Si este parámetro se deja en su valor predeterminado, el tamaño máximo de la memoria caché se establecerá en el tamaño de la memoria física cuando se llame a [JetInit.](./jetinit-function.md)

**Windows Vista:**  A Windows Vista, se cambió el valor predeterminado de este parámetro para aclarar este comportamiento.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 512</p><p><strong>Windows Vista:</strong> 2000000000</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p><strong>Windows 2000:</strong>  No</p><p><strong>Windows XP:</strong>  Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p><strong>Windows XP y Windows 2000:</strong>  No</p><p><strong>Windows Vista y Windows Server 2003:</strong>  Sí</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramCheckpointDepthMax*  
24 

Este parámetro controla la agresividad con la que las páginas de base de datos se vacían de la caché de páginas de la base de datos para minimizar la cantidad de tiempo que se va a tardar en recuperarse de un bloqueo. El parámetro es un umbral en bytes para saber cuántos archivos de registro de transacciones deben reproducirse después de un bloqueo.

Si el registro circular está habilitado mediante [JET_paramCircularLog,](./transaction-log-parameters.md) este parámetro también controlará la cantidad aproximada de archivos de registro de transacciones que se conservarán en el disco.

Es importante que este parámetro no se establezca demasiado bajo. A medida que el valor de este parámetro se aproxima a cero, la memoria caché se volverá cada vez más agresiva al vaciar las páginas de la base de datos en el disco. Esto no solo da como resultado un mayor número de escrituras en los archivos de base de datos, sino que también provoca indirectamente un mayor número de lecturas en esos archivos. Esto puede causar problemas de rendimiento muy significativos en algunos casos. Desafortunadamente, establecer el valor óptimo más pequeño para este parámetro solo se puede realizar mediante experimentación con la aplicación de destino.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>20971520</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 0 – 2147483647</p><p><strong>Windows Vista:</strong>  Todos los valores</p> | 
| <p>Ámbito:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> Este parámetro es global.</p><p><strong>Windows Vista:</strong>  Este parámetro es por instancia.</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramCheckpointIOMax*  
135  

Este parámetro controla el número máximo de escrituras simultáneas que usará el motor de base de datos para vaciar las páginas de base de datos modificadas con el fin de avanzar en el punto de control. El valor de este parámetro se puede usar para equilibrar la velocidad con la que se puede avanzar el punto de control frente al impacto negativo que tendrá este proceso en el tiempo de respuesta de otras operaciones de E/S en los discos que mantienen la base de datos.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>96</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>8 – 1024</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows Vista y versiones posteriores</p> | 



*JET_paramEnableViewCache*  
127  

Cuando este parámetro es **True,** el motor de base de datos usará datos de base de datos directamente desde la caché de archivos Windows en lugar de copiar los datos almacenados en caché en su propia memoria privada. Los datos de base de datos modificados se almacenarán en caché en memoria privada.

La intención de este modo es reducir aún más la cantidad de memoria privada que usa el motor de base de datos para almacenar en caché los datos de la base de datos.

La caché de vistas solo se puede usar si el uso de la caché de archivos Windows está habilitado estableciendo JET_paramEnableFileCache en **True.**


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>False</p> | 
| <p>Escriba:</p> | <p>Boolean</p> | 
| <p>Intervalo válido:</p> | <p>False, True</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>Windows Vista y versiones posteriores</p> | 



*JET_paramLRUKCorrInterval*  
25  

Este parámetro establece el intervalo de tiempo en microsegundos a lo largo del cual se considera que dos accesos a páginas de base de datos están correlacionados. Este intervalo de correlación controla la confidencialidad del algoritmo de reemplazo de páginas (LRU-K) de la memoria caché a los accesos a páginas sucesivos. Esto, a su vez, afectará a las páginas que decida mantener almacenadas en caché.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>128000</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 0 – 2147483647</p><p><strong>Windows Vista:</strong>  Todos los valores</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramLRUKHistoryMax*  
26  

Este parámetro establece el número máximo de páginas de base de datos no almacenadas en caché para las que se conservarán los tiempos de acceso a páginas de base de datos. Estos registros de historial permiten que el algoritmo de reemplazo de páginas (LRU-K) de la memoria caché detecte con más precisión las páginas populares que se expulsaron incorrectamente de la caché de páginas de la base de datos.

**Windows XP y Windows Server 2003:**  Este parámetro se omite en Windows XP y Windows Server 2003 y no afecta al funcionamiento del motor de base de datos.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p><strong>Windows 2000:</strong> 1024</p><p><strong>Windows Vista:</strong> 100000</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 0 – 4194303</p><p><strong>Windows Vista:</strong>  Todos los valores</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramLRUKPolicy*  
27  

Este parámetro configura el número de accesos a páginas de base de datos que se tienen en cuenta para determinar la utilidad de la página. Este parámetro es básicamente el K en LRU-K, el algoritmo de reemplazo de páginas de la caché de páginas de la base de datos.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>2</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>1-2</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramLRUKTimeout*  
28

Este parámetro indica el período de tiempo en segundos después del cual se considera que una página de la caché de páginas de la base de datos ha perdido un acceso a la página con el fin de considerar la utilidad de la página.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>100</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 1 – 2147483647</p><p><strong>Windows Vista:</strong> 1 – 4294967295</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramLRUKTrxCorrInterval*  
29  

Este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.

*JET_paramStartFlushThreshold*  
31  

Este parámetro controla cuándo comienza la caché de páginas de la base de datos a expulsar páginas de la memoria caché para dar espacio a las páginas que no están almacenadas en caché. Cuando el número de búferes de página de la memoria caché cae por debajo de este umbral, se inicia un proceso en segundo plano para reponer ese grupo de búferes disponibles. Este umbral siempre es relativo al tamaño máximo de caché establecido por **JET_paramCacheSizeMax**. Este umbral también debe ser siempre menor que el umbral de detección establecido **por JET_paramStopFlushThreshold**.

El alto de distancia del umbral de inicio determinará el tiempo de respuesta que debe tener la caché de páginas de la base de datos para generar búferes disponibles antes de que la aplicación los necesite. Un umbral de inicio alto dará al proceso en segundo plano más tiempo para reaccionar. Sin embargo, un umbral de inicio alto implica un umbral de detección más alto y eso reducirá el tamaño efectivo de la memoria caché de páginas de base de datos para las páginas modificadas (Windows 2000) o para todas las páginas (Windows XP y versiones posteriores).


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 5 (1 %)</p><p><strong>Windows Vista:</strong> 20000000 (1 %)</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p><p><strong>Windows Vista:</strong>  Todos los valores</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramStopFlushThreshold*  
32  

Este parámetro controla cuándo termina la caché de páginas de la base de datos expulsando páginas de la memoria caché para dar espacio a las páginas que no están almacenadas en caché. Cuando el número de búferes de página de la memoria caché supera este umbral, se detiene el proceso en segundo plano que se inició para reponer ese grupo de búferes disponibles. Este umbral siempre es relativo al tamaño máximo de caché establecido por **JET_paramCacheSizeMax**. Este umbral también debe ser siempre mayor que el umbral de inicio establecido **por JET_paramStartFlushThreshold**.

La distancia entre el umbral inicial y el umbral de detección afecta a la eficacia con la que el proceso en segundo plano vacía las páginas de la base de datos. Una brecha mayor hará que sea más probable que se combinen las escrituras en páginas vecinos. Sin embargo, un umbral de detección alto reducirá el tamaño efectivo de la memoria caché de páginas de la base de datos para las páginas modificadas (Windows 2000) o para todas las páginas (Windows XP y versiones posteriores).


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 10 (2 %)</p><p><strong>Windows Vista:</strong> 40000000 (2 %)</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p><p><strong>Windows Vista:</strong>  Todos los valores</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>Sí</p> | 
| <p>Afecta a los recursos:</p> | <p>Sí</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
