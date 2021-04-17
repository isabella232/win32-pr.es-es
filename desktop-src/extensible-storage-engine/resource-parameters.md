---
description: 'Más información acerca de: parámetros de recursos'
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
ms.openlocfilehash: 953488a273092413df78d4fe396899d284c7a01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687676"
---
# <a name="resource-parameters"></a>Parámetros de recursos


_**Se aplica a:** Windows | Windows Server_

## <a name="resource-parameters"></a>Parámetros de recursos

Este tema contiene los parámetros que se usan para los recursos.

*JET_paramCachedClosedTables*  
125  

Este parámetro controla el número de recursos de árbol B + almacenados en memoria caché por la instancia de después de que la aplicación haya cerrado las tablas que representan.

Los valores grandes de este parámetro harán que el motor de base de datos use más memoria, pero aumentará la velocidad con la que la aplicación puede abrir aleatoriamente un gran número de tablas. Esto resulta útil para las aplicaciones que tienen un esquema con un gran número de tablas.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
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


*JET_paramDisablePerfmon*  
107  

Este parámetro se puede utilizar para evitar que el motor de base de datos publique datos sobre su rendimiento en Windows. Esto se puede hacer para reducir la actividad de subprocesos de servicio del motor de base de datos.

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
<td><p>No</p></td>
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


*JET_paramGlobalMinVerPages*  
81  

Este parámetro permite que las aplicaciones que operan en modo de varias instancias realicen previamente la asignación de memoria para las páginas de versión de un grupo global con el fin de emular el comportamiento anterior. Esto resulta útil en caso de que la aplicación quiera garantizar que las transacciones de un determinado tamaño puedan tener éxito más adelante aunque la memoria se vuelva insuficiente.

**Windows 2000:**  La memoria suficiente para volver a todas las páginas de la versión siempre se reserva en el momento de [JetInit](./jetinit-function.md) .

**Windows XP:**  A partir de Windows XP, esto sigue siendo true cuando se encuentra en modo de instancia única. Sin embargo, la memoria de la página de la versión se asigna dinámicamente cuando se está en modo de varias instancias.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1 – 2147483647</p></td>
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
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows XP y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCursors*  
8  

Este parámetro reserva el número solicitado de recursos de cursor para su uso por parte de una instancia de. Un recurso cursor se corresponde directamente con un tipo de datos [JET_TABLEID](./jet-tableid.md) . Este valor afectará al número de cursores que se pueden usar al mismo tiempo. Un recurso de cursor no puede compartirse por sesiones diferentes, por lo que este parámetro debe establecerse en un valor suficientemente grande para que cada sesión pueda usar tantos cursores como sean necesarios.

**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes de este parámetro utilizarán el espacio de direcciones y pueden aumentar el uso de memoria.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>1024</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
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
<td><p>No</p></td>
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


*JET_paramMaxInstances*  
104  

Este parámetro controla el número máximo de instancias que se pueden crear en un único proceso.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1-1024</p></td>
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
<td><p>Windows XP y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxOpenTables*  
6  

Este parámetro reserva el número solicitado de recursos de árbol B + para su uso por parte de una instancia de. Este valor afectará al número de tablas que se pueden usar al mismo tiempo. Este parámetro debe establecerse en relación con el esquema físico de las bases de datos que usa el motor de base de datos, por lo que esta configuración no es tan sencilla como podría ser.

En general, necesitará dos recursos más un recurso por cada índice secundario por tabla en uso simultáneo por la aplicación.

**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes de este parámetro utilizarán el espacio de direcciones y pueden aumentar el uso de memoria.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>300</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
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
<td><p>No</p></td>
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


*JET_paramMaxSessions*  
5  

Este parámetro reserva el número solicitado de recursos de sesión para su uso por parte de una instancia de. Un recurso de sesión se corresponde directamente con un tipo de datos [JET_SESID](./jet-sesid.md) . Esta configuración afectará a la cantidad de sesiones que se pueden usar al mismo tiempo.

**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes de este parámetro utilizarán el espacio de direcciones y pueden aumentar el uso de memoria.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 30000</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
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
<td><p>No</p></td>
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


*JET_paramMaxTemporaryTables*  
10  

Este parámetro reserva el número solicitado de recursos de tabla temporal para su uso por parte de una instancia de. Esta configuración afectará al número de tablas temporales que se pueden usar al mismo tiempo.

**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes de este parámetro utilizarán el espacio de direcciones y pueden aumentar el uso de memoria.

**Windows XP y versiones posteriores:**  Si este parámetro del sistema se establece en cero, no se creará ninguna base de datos temporal y se producirá un error en cualquier actividad que requiera el uso de la base de datos temporal. Esta configuración puede ser útil para evitar la e/s necesaria para crear la base de datos temporal si se sabe que no se va a usar.

**Nota:**  El uso de una tabla temporal también requiere un recurso de cursor.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>20</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
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


*JET_paramMaxVerPages*  
9  

Este parámetro reserva el número solicitado de páginas del almacén de versiones para su uso por parte de una instancia de. El almacén de versiones contiene un registro en directo de todas las versiones de cada entrada de registro o índice de la base de datos que pueden verse en todas las transacciones activas. Estas versiones se utilizan para admitir el control de simultaneidad con varias versiones que usa el motor de base de datos para admitir transacciones que usan el aislamiento de instantánea. Este valor afectará al número de actualizaciones que se pueden conservar en la memoria a la vez. Esto, a su vez, afecta al número máximo de actualizaciones que puede realizar una única transacción, la duración máxima de una transacción abierta, la carga máxima simultánea de transacciones de actualización en el sistema o una combinación de estas.

Cada página del almacén de versiones tal como la configura este parámetro tiene 16 KB de tamaño en los equipos de 32 bits y 32 KB en los equipos de 64 bits.

**Windows Vista y versiones posteriores:**  El tamaño de la página del almacén de versiones se puede leer y cambiar mediante JET_paramVerPageSize.

**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes de este parámetro utilizarán el espacio de direcciones y pueden aumentar el uso de memoria.

**Nota:**  Este es el recurso más común que el motor de base de datos debe agotar. Se debe prestar especial atención a la configuración del parámetro del sistema y a la carga transaccional de la aplicación para evitar agotar este recurso en el funcionamiento normal. Cuando se agote este recurso, las actualizaciones de la base de datos se rechazarán con JET_errVersionStoreOutOfMemory. Para liberar algunos de estos recursos, se debe anular la transacción pendiente más antigua.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
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
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
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


*JET_paramPageHintCacheSize*  
101  

Este parámetro controla el tamaño de una memoria caché especial que se usa para acelerar la búsqueda de punteros de página secundaria de B + árbol en la caché de páginas de base de datos. El tamaño de la memoria caché está en bytes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>262 144</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 2147483647</p></td>
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
<td><p>Windows XP y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramPreferredMaxOpenTables*  
7  

Este parámetro intenta mantener el número de recursos de árbol B + en uso por debajo del umbral especificado.

Si este parámetro se establece en cero, el valor predeterminado será 100% de **JET_paramMaxOpenTables**.

**Windows Vista y versiones posteriores:**  Este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos. Las aplicaciones deben usar JET_paramMaxCachedClosedTables en su lugar.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>0 (100% de <strong>JET_paramMaxOpenTables</strong>)</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
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


*JET_paramPreferredVerPages*  
63  

Este parámetro representa un umbral relativo a **JET_paramMaxVerPages** que controla el uso discrecional de páginas de versión por parte del motor de base de datos. Si el tamaño del almacén de versiones supera este umbral, cualquier información que solo se use para tareas en segundo plano opcionales, como la recuperación del espacio eliminado en la base de datos, se sacrifica en su lugar para conservar el espacio para la información transaccional.

**Windows 2000, Windows XP y Windows Server 2003:**  Si se establece este parámetro en cero, el umbral se establecerá en el 90% de **JET_paramMaxVerPages**.

**Windows Vista y versiones posteriores:**  Ya no se admite y el valor predeterminado de este parámetro se ha cambiado para aclarar su comportamiento.

Cada página del almacén de versiones tal como la configura este parámetro tiene 16 KB de tamaño en los equipos de 32 bits y 32 KB en los equipos de 64 bits.

**Windows Vista y versiones posteriores:**  El tamaño de la página del almacén de versiones se puede leer y cambiar mediante JET_paramVerPageSize.

**Nota:**  Si el motor de base de datos funciona por encima de este umbral con demasiada frecuencia, es posible que la base de datos se reduzca el rendimiento. Esto sucede porque los procesos en segundo plano que limpian la base de datos no pueden funcionar sin la información opcional que se produce en este escenario. La desfragmentación en línea o sin conexión contrarresta este efecto.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  0 (90% de JET_paramMaxVerPages)</p>
<p><strong>Windows Vista:</strong>  58</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
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


*JET_paramVerPageSize*  
128  

Este parámetro controla el tamaño de las páginas del almacén de versiones utilizadas por el motor de base de datos para contener información transaccional. El valor de este parámetro es el tamaño de la unidad para todos los demás parámetros del sistema que se encuentran en términos de páginas de versión (por ejemplo, JET_paramMaxVerPages).

El motor de base de datos puede optar por usar un tamaño de página del almacén de versiones mayor que el solicitado.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>16384</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1024, 2048, 4096, 8192, 16384, 32768, 65536</p></td>
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
<td><p>No</p></td>
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


*JET_paramVersionStoreTaskQueueMax*  
105  

Este parámetro controla el número de elementos de trabajo de limpieza en segundo plano que se pueden poner en cola en el grupo de subprocesos del motor de base de datos al mismo tiempo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>32</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows XP y Windows Server 2003:  </strong>  1 – 63</p>
<p><strong>Windows Vista:</strong>  1 – 127</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows XP y Windows Server 2003:  </strong>  No</p>
<p><strong>Windows Vista:</strong>  ?</p></td>
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
<td><p>Windows XP y versiones posteriores</p></td>
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
