---
description: 'Más información sobre: Parámetros de recursos'
title: Parámetros de recursos
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: ac1a6aba2eda729c3e705cf5acdda837c2670564
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472451"
---
# <a name="resource-parameters"></a>Parámetros de recursos


_**Se aplica a:** Windows | Windows Servidor_

## <a name="resource-parameters"></a>Parámetros de recursos

Este tema contiene parámetros que se usan para los recursos.

*JET_paramCachedClosedTables*  
125  

Este parámetro controla el número de recursos de árbol B+ almacenados en caché por la instancia después de que la aplicación haya cerrado las tablas que representan.

Los valores grandes para este parámetro harán que el motor de base de datos use más memoria, pero aumentará la velocidad con la que la aplicación puede abrir aleatoriamente un gran número de tablas. Esto es útil para las aplicaciones que tienen un esquema con un número muy grande de tablas.


| | | <p>Valor predeterminado:</p> | <p>64</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>1 – 2147483647</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Windows Vista y versiones posteriores</p> | 



*JET_paramDisablePerfmon*  
107  

Este parámetro se puede usar para evitar que el motor de base de datos publique datos sobre su rendimiento en Windows. Esto puede hacerse para reducir la actividad de subprocesos de servicio del motor de base de datos.


| | | <p>Valor predeterminado:</p> | <p>Falso</p> | | <p>Escriba:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Ámbito:</p> | <p>Global</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Windows Vista y versiones posteriores</p> | 



*JET_paramGlobalMinVerPages*  
81  

Este parámetro permite a las aplicaciones que operan en modo de instancias múltiples asignar previamente memoria para las páginas de versión de un grupo global para emular el comportamiento anterior. Esto es útil en caso de que la aplicación desee garantizar que las transacciones de un tamaño determinado puedan realizarse correctamente más adelante, incluso si la memoria se vuelve insuficiente.

**Windows 2000:**  La memoria suficiente para hacer una copia de seguridad de todas las páginas de versión siempre se reserva [a la hora de JetInit.](./jetinit-function.md)

**Windows XP:**  A Windows XP, esto sigue siendo así cuando se encuentra en modo de instancia única. Sin embargo, la memoria de la página de versión se asigna dinámicamente en modo de varias instancias.


| | | <p>Valor predeterminado:</p> | <p>64</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>1 – 2147483647</p> | | <p>Ámbito:</p> | <p>Global</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramMaxCursors*  
8  

Este parámetro reserva el número solicitado de recursos de cursor para que lo use una instancia de . Un recurso de cursor corresponde directamente a un [tipo JET_TABLEID](./jet-tableid.md) datos. Esta configuración afectará al número de cursores que se pueden usar al mismo tiempo. Diferentes sesiones no pueden compartir un recurso de cursor, por lo que este parámetro debe establecerse en un valor lo suficientemente grande para que cada sesión pueda usar tantos cursores como sean necesarios.

**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes para este parámetro consumirán espacio de direcciones y pueden aumentar el uso de memoria.


| | | <p>Valor predeterminado:</p> | <p>1024</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramMaxInstances*  
104  

Este parámetro controla el número máximo de instancias que se pueden crear en un único proceso.


| | | <p>Valor predeterminado:</p> | <p>16</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>1-1024</p> | | <p>Ámbito:</p> | <p>Global</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramMaxOpenTables*  
6  

Este parámetro reserva el número solicitado de recursos de árbol B+ para que lo use una instancia de . Esta configuración afectará al número de tablas que se pueden usar al mismo tiempo. Este parámetro debe establecerse en relación con el esquema físico de las bases de datos en uso por el motor de base de datos, por lo que esta configuración no es tan sencilla como podría ser.

En general, necesitará dos recursos más un recurso por índice secundario por tabla en uso simultáneo por la aplicación.

**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes para este parámetro consumirán espacio de direcciones y pueden aumentar el uso de memoria.


| | | <p>Valor predeterminado:</p> | <p>300</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramMaxSessions*  
5  

Este parámetro reserva el número solicitado de recursos de sesión para que los use una instancia de . Un recurso de sesión corresponde directamente a un [tipo JET_SESID](./jet-sesid.md) de datos. Esta configuración afectará al número de sesiones que se pueden usar al mismo tiempo.

**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes para este parámetro consumirán espacio de direcciones y pueden aumentar el uso de memoria.


| | | <p>Valor predeterminado:</p> | <p>16</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>0 – 30000</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramMaxTemporaryTables*  
10  

Este parámetro reserva el número solicitado de recursos de tabla temporal para que los use una instancia de . Esta configuración afectará al número de tablas temporales que se pueden usar al mismo tiempo.

**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes para este parámetro consumirán espacio de direcciones y pueden aumentar el uso de memoria.

**Windows XP y versiones posteriores:**  Si este parámetro del sistema se establece en cero, no se creará ninguna base de datos temporal y se producirá un error en cualquier actividad que requiera el uso de la base de datos temporal. Esta configuración puede ser útil para evitar la E/S necesaria para crear la base de datos temporal si se sabe que no se usará.

**Nota**  El uso de una tabla temporal también requiere un recurso de cursor.


| | | <p>Valor predeterminado:</p> | <p>20</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramMaxVerPages*  
9  

Este parámetro reserva el número solicitado de páginas del almacén de versiones para que las use una instancia de . El almacén de versiones contiene un registro activo de todas las distintas versiones de cada entrada de registro o índice de la base de datos que pueden ver todas las transacciones activas. Estas versiones se usan para admitir el control de simultaneidad con varias versiones en uso por parte del motor de base de datos para admitir transacciones mediante el aislamiento de instantáneas. Esta configuración afectará al número de actualizaciones que se pueden tener en memoria a la vez. Esto, a su vez, afectará al número máximo de actualizaciones que puede realizar una única transacción, a la duración máxima que una transacción puede estar abierta, a la carga simultánea máxima de transacciones de actualización en el sistema o a una combinación de estas.

Cada página del almacén de versiones configurada por este parámetro tiene un tamaño de 16 KB en máquinas de 32 bits y de 32 KB en máquinas de 64 bits.

**Windows Vista y versiones posteriores:**  El tamaño de página del almacén de versiones se puede leer y cambiar mediante JET_paramVerPageSize.

**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes para este parámetro consumirán espacio de direcciones y pueden aumentar el uso de memoria.

**Nota**  Este es, con diferencia, el recurso más común que agota el motor de base de datos. Se debe prestar mucha atención a la configuración del parámetro del sistema y a la carga transaccional de la aplicación para evitar agotar este recurso con un funcionamiento normal. Cuando se agote este recurso, las actualizaciones de la base de datos se rechazarán con JET_errVersionStoreOutOfMemory. Para liberar algunos de estos recursos, se debe anular la transacción pendiente más antigua.


| | | <p>Valor predeterminado:</p> | <p>64</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>1 – 2147483647</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramPageHintCacheSize*  
101  

Este parámetro controla el tamaño de una caché especial que se usa para acelerar la búsqueda de punteros a páginas secundarias del árbol B+ en la caché de páginas de la base de datos. El tamaño de la memoria caché está en bytes.


| | | <p>Valor predeterminado:</p> | <p>262 144</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Ámbito:</p> | <p>Global</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramPreferredMaxOpenTables*  
7  

Este parámetro intenta mantener el número de recursos de árbol B+ en uso por debajo del umbral especificado.

Si este parámetro se establece en cero, el valor predeterminado será el 100 % **JET_paramMaxOpenTables**.

**Windows Vista y versiones posteriores:**  Este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos. Las aplicaciones deben usar JET_paramMaxCachedClosedTables en su lugar.


| | | <p>Valor predeterminado:</p> | <p>0 (100 % de <strong>JET_paramMaxOpenTables</strong>)</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramPreferredVerPages*  
63  

Este parámetro representa un umbral relativo a JET_paramMaxVerPages **que** controla el uso discrecional de páginas de versión por parte del motor de base de datos. Si el tamaño del almacén de versiones supera este umbral, cualquier información que solo se utilice para tareas en segundo plano opcionales, como reclamar el espacio eliminado en la base de datos, se sacrificará en su lugar para conservar espacio para la información transaccional.

**Windows 2000, Windows XP y Windows Server 2003:**  Establecer este parámetro en cero establecería el umbral en el 90 % **de JET_paramMaxVerPages**.

**Windows Vista y versiones posteriores:**  Ya no se admite y se ha cambiado el valor predeterminado de este parámetro para aclarar su comportamiento.

Cada página del almacén de versiones configurada por este parámetro tiene un tamaño de 16 KB en máquinas de 32 bits y de 32 KB en máquinas de 64 bits.

**Windows Vista y versiones posteriores:**  El tamaño de página del almacén de versiones se puede leer y cambiar a través JET_paramVerPageSize.

**Nota**  Si el motor de base de datos funciona por encima de este umbral con demasiada frecuencia, es posible que la base de datos se degrade en rendimiento. Esto sucede porque los procesos en segundo plano que limpian la base de datos no pueden funcionar sin la información opcional que se descarta en este escenario. La desfragmentación en línea o sin conexión contrarresta este efecto.


| | | <p>Valor predeterminado:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 0 (90 % de JET_paramMaxVerPages)</p><p><strong>Windows Vista:</strong> 58</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>1 – 2147483647</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramVerPageSize*  
128  

Este parámetro controla el tamaño de las páginas del almacén de versiones utilizadas por el motor de base de datos para contener información transaccional. El valor de este parámetro es el tamaño de unidad para todos los demás parámetros del sistema que se encuentran en términos de páginas de versión (por ejemplo, JET_paramMaxVerPages).

El motor de base de datos puede optar por usar un tamaño de página de almacén de versiones mayor que el solicitado.


| | | <p>Valor predeterminado:</p> | <p>16384</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>1024, 2048, 4096, 8192, 16384, 32768, 65536</p> | | <p>Ámbito:</p> | <p>Global</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Windows Vista y versiones posteriores</p> | 



*JET_paramVersionStoreTaskQueueMax*  
105  

Este parámetro controla el número de elementos de trabajo de limpieza en segundo plano que se pueden poner en cola en el grupo de subprocesos del motor de base de datos en cualquier momento.


| | | <p>Valor predeterminado:</p> | <p>32</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p><strong>Windows XP y Windows Server 2003:</strong> 1 – 63</p><p><strong>Windows Vista:</strong> 1 – 127</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p><strong>Windows XP y Windows Server 2003:</strong>  No</p><p><strong>Windows Vista:</strong>  Sí</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
