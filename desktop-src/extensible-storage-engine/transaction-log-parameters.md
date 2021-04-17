---
description: 'Más información acerca de: parámetros de registro de transacciones'
title: Parámetros de registro de transacciones
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: 2d72cafc990d8526cadf7c5f6d149796ff846181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697438"
---
# <a name="transaction-log-parameters"></a>Parámetros de registro de transacciones


_**Se aplica a:** Windows | Windows Server_

**En este artículo**  
Parámetros de registro de transacciones  
Requisitos  
Consulte también  

## <a name="transaction-log-parameters"></a>Parámetros de registro de transacciones

Este tema contiene los parámetros que se utilizan para los registros de transacciones.

*JET_paramBaseName*  
3  

Este parámetro establece el prefijo de tres letras que se usa para muchos de los archivos utilizados por el motor de base de datos. Por ejemplo, el archivo de punto de comprobación se denomina EDB. CHK de forma predeterminada porque EDB es el nombre base predeterminado. El nombre base se puede usar para distinguir fácilmente entre los conjuntos de archivos que pertenecen a distintas instancias o a aplicaciones diferentes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>&quot;EDB&quot;</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>3 caracteres</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramCircularLog*  
17  

Este parámetro configura el modo en que el motor de base de datos administra los archivos de registro de transacciones.

Cuando el registro circular está desactivado, todos los archivos de registro de transacciones que se generan se conservan en el disco hasta que ya no son necesarios porque se ha realizado una copia de seguridad completa de la base de datos. En este modo, es posible realizar una restauración a partir de una copia de seguridad anterior y reproducir hacia delante a través de todos los archivos de registro de transacciones retenidos, de modo que no se pierdan datos como resultado del desastre que forzó la restauración. Se requieren copias de seguridad completas normales para evitar que el disco se llene con los archivos de registro de transacciones.

Cuando el registro circular está activado, solo se conservan en el disco los archivos de registro de transacciones que son más jóvenes que el punto de control actual. La ventaja de este modo es que las copias de seguridad no son necesarias para retirar los archivos de registro de transacciones antiguos. La contrapartida es que ya no es posible la restauración de una pérdida de datos.

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


*JET_paramCommitDefault*  
16  

Este parámetro controla la acción predeterminada realizada cuando se confirma la transacción más externa en una sesión. Cualquier opción válida que se pueda pasar a [JetCommitTransaction](./jetcommittransaction-function.md) también puede ser la predeterminada para todas las sesiones de una instancia de o para una sesión específica. Consulte [JetCommitTransaction](./jetcommittransaction-function.md) para obtener más información sobre estas opciones.

Este parámetro afecta a la confiabilidad y el rendimiento de las transacciones. Consulte [JetCommitTransaction](./jetcommittransaction-function.md) para obtener más información.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>JET_GRBIT (entero)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Una opción válida para JetCommitTransaction</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia o sesión</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramDeleteOldLogs*  
48  

Cuando este parámetro es true y los archivos de registro de transacciones a los que apunta la ruta de acceso del archivo de registro (**JET_paramLogFilePath**) son una versión obsoleta, esos archivos de registro de transacciones se eliminarán automáticamente.

**Windows 2000:**  Se debe tener cuidado con el uso de este parámetro al actualizar una base de datos de Windows NT a Windows 2000. Si la base de datos no tiene un estado coherente y se eliminan los archivos de registro antiguos, se perderá el contenido de la base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p><strong>Windows 2000:</strong>  Es</p>
<p><strong>Windows XP:</strong>  Reales</p></td>
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
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
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


*JET_paramIgnoreLogVersion*  
47  

Si este parámetro es true, el motor de base de datos no validará el número de versión del archivo de registro de transacciones durante [JetInit](./jetinit-function.md).

**Windows XP:**  A partir de Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.

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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramLegacyFileNames*  
136  

Este parámetro proporciona compatibilidad con versiones anteriores de las convenciones de nomenclatura de los archivos de las versiones anteriores del motor de base de datos.

Actualmente se admiten las siguientes opciones:

JET_bitESE98FileNames

Cuando esta opción está presente, el motor de base de datos usará las siguientes convenciones de nomenclatura para sus archivos:

  - Los archivos de registro de transacciones utilizarán. LOG para la extensión de archivo

  - Los archivos de punto de comprobación usarán. CHK para la extensión de archivo

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>JET_GRBIT (entero)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0, JET_bitESE98FileNames</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows Vista y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramLogBuffers*  
12  

Este parámetro configurará la cantidad de memoria que se usa para almacenar en caché las entradas de registro antes de que se escriban en el archivo de registro de transacciones. La unidad para este parámetro es el tamaño de sector del volumen que contiene los archivos de registro de transacciones. El tamaño del sector es casi siempre de 512 bytes, por lo que es seguro suponer ese tamaño para la unidad.

Este parámetro afecta al rendimiento. Cuando el motor de base de datos está sometido a una carga de actualización pesada, este búfer puede llenarse con mucha rapidez. Un tamaño de caché mayor para el archivo de registro de transacciones es fundamental para un buen rendimiento de actualización en una condición de carga elevada. Se sabe que el valor predeterminado es demasiado pequeño para este caso.

**Windows XP y windows 2000:**  En Windows XP y versiones anteriores, no se recomienda establecer este parámetro en un número de búferes mayor (en bytes) de la mitad del tamaño de un archivo de registro de transacciones.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  80</p>
<p><strong>Windows Vista:</strong>  126</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  80 – 2147483647</p>
<p><strong>Windows Vista:</strong>  1 – 2147483647</p></td>
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


*JET_paramLogCheckpointPeriod*  
14  

Este parámetro configura el motor de base de datos para tomar un punto de control cuando se ha generado el número especificado de sectores del archivo de registro.

**Windows XP:**  A partir de Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.

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
<td><p>Sí</p></td>
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


*JET_paramLogFileCreateAsynch*  
69  

Cuando este parámetro se establece en true, el motor de base de datos creará el siguiente archivo de registro de transacciones a medida que se consuma el archivo de registro de transacciones actual. La intención es minimizar el tiempo invertido en cambiar de un archivo de registro de transacciones a la siguiente bajo una carga de actualización pesada.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>True</p></td>
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


*JET_paramLogFilePath*  
2 

Este parámetro indica la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá los registros de transacciones de la instancia. La ruta de acceso debe terminar con un carácter de barra diagonal inversa, lo que indica que la ruta de acceso de destino es una carpeta. Los archivos de registro de transacciones contienen la información necesaria para poner los archivos de base de datos en un estado coherente después de un bloqueo. Normalmente se denominan EDB \* . Inicia. El contenido de los archivos de registro de transacciones es tan importante (si no más) que los propios archivos de base de datos. Se debe hacer todo lo posible para protegerlos.

También habrá archivos de registro de reserva adicionales denominados RES1. LOG y RES2. REGISTRO almacenado junto con los archivos de registro normales. El contenido de estos archivos no es importante porque su único propósito es reservar espacio en disco para permitir que el motor se cierre correctamente en un escenario de disco insuficiente. También serán un archivo de registro temporal denominado EDBTMP. Inicie sesión en esta misma carpeta. El contenido de este archivo no es importante. Este archivo es un nuevo archivo de registro que se está preparando para su uso.

Las propiedades del volumen de host de los archivos de registro de transacciones y su ubicación en relación con los otros archivos utilizados por el motor de base de datos pueden afectar drásticamente al rendimiento.

**Nota:**  Si se especifica una ruta de acceso relativa, será relativa al directorio de trabajo actual del proceso que hospeda la aplicación que usa el motor de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>&quot;.\& entrecomillados</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Ruta de acceso de la carpeta (cadena)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 246 caracteres</p></td>
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
<td><p>Sí</p></td>
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


*JET_paramLogFileSize*  
11  

Este parámetro configurará el tamaño de los archivos de registro de transacciones. Cada archivo de registro de transacciones tiene un tamaño fijo. El tamaño es igual al valor de este parámetro del sistema en unidades de 1024 bytes.

Este parámetro afecta a la confiabilidad. Si el valor es demasiado pequeño, el número máximo de archivos de registro (1048575) se alcanzará mucho más rápido. Cuando esto sucede, la instancia debe cerrarse correctamente, se deben eliminar los archivos de registro existentes y se debe reiniciar la instancia. Esta acción no solo reducirá la disponibilidad de la aplicación, sino que también invalidará las copias de seguridad anteriores de la base de datos de la aplicación.

Este parámetro afecta al rendimiento. Si el valor es muy grande, [JetInit](./jetinit-function.md) será lento, ya que el motor de base de datos debe leer el archivo de registro más reciente (como mínimo) cuando se inicializa. Si el valor es muy grande, también tardará más tiempo en cambiar entre los archivos de registro. Si el valor es muy pequeño, se deberán crear más archivos de registro para un número determinado de actualizaciones que agregarán más sobrecarga.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>5120</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  128 – 32768</p>
<p><strong>Windows Vista:</strong>  64 – 32768</p></td>
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


*JET_paramLogWaitingUserMax*  
15  

Este parámetro intenta optimizar el vaciado del búfer de registro causado por una confirmación duradera al esperar a que un número especificado de sesiones espere una confirmación duradera antes de forzar que se produzca una operación de vaciado en la espera de que otra transacción comparta el vaciado.

**Windows XP:**  A partir de Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>3</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramRecovery*  
34  

Este parámetro es el modificador principal que controla la recuperación tras bloqueo de una instancia de. Si este parámetro se establece en "ON", se usará la recuperación de estilo ARIES para que todas las bases de datos de la instancia tengan un estado coherente en caso de que se produzca un bloqueo del proceso o del equipo. Si este parámetro se establece en "OFF", todas las bases de datos de la instancia se administrarán sin la ventaja de la recuperación tras bloqueo. Es decir, que si la instancia no se cierra correctamente con [JetTerm](./jetterm-function.md) antes de que el proceso salga o cierre el equipo, el contenido de todas las bases de datos de esa instancia estará dañado.

La deshabilitación de la recuperación resulta útil en circunstancias especiales en las que se sabe que el contenido de una base de datos no es útil en caso de bloqueo. La recuperación debe estar habilitada para todos los demás casos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>&quot;Activado&quot;</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 259 caracteres</p></td>
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


*JET_paramSystemPath*  
0  

Este parámetro indica la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá el archivo de punto de comprobación de la instancia. La ruta de acceso debe terminar con un carácter de barra diagonal inversa, lo que indica que la ruta de acceso de destino es una carpeta. El archivo de punto de comprobación es un archivo simple mantenido por instancia que recuerda el archivo de registro de transacciones más antiguo que debe reproducirse para que todas las bases de datos de esa instancia tengan un estado coherente después de un bloqueo. El archivo de punto de comprobación se denomina normalmente EDB. CHK.

**Nota:**  Si se especifica una ruta de acceso relativa, será relativa al directorio de trabajo actual del proceso que hospeda la aplicación que usa el motor de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>&quot;.\& entrecomillados</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Ruta de acceso de la carpeta (cadena)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 246 caracteres</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramWaitLogFlush*  
13 

Este parámetro intenta optimizar el vaciado del búfer de registro causado por una confirmación duradera esperando un período de tiempo especificado antes de forzar que se produzca una operación de vaciado, por lo que otra transacción compartirá el vaciado.

**Windows XP:**  A partir de Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>0</p></td>
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
<td><p>Instancia o sesión</p></td>
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
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramLegacyFileNames*  
136  

Este parámetro se usa para especificar las características de compatibilidad de nombres de archivo que se deben mantener con Windows Server 2003 y el esquema de nombres de archivo anterior. Para obtener más información sobre los distintos archivos y su nombre, consulte [archivos del motor de almacenamiento extensible](./extensible-storage-engine-files.md).

El JET_bitESE98FileNames garantiza la extensión de archivo que se usa en los archivos de registro de transacciones y el archivo de punto de comprobación son los mismos que se usan en Windows Server 2003. Nota: si se actualiza desde Windows Server 2003, no es necesario especificar este bit, ya que el motor actualizará automáticamente las extensiones de archivo si JET_paramCircularLog está establecido en **true** o mantiene la extensión de registro anterior si JET_paramCircularLog es **false**.

**Nota:**  Para establecer un bit, primero se debe recuperar el valor y, después, "or" en el bit de compatibilidad deseado.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>JET_GRBIT (entero)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>A partir de Windows Server 2008 y Windows Vista</p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a>Requisitos

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


## <a name="see-also"></a>Consulte también

[Archivos del motor de almacenamiento extensible](./extensible-storage-engine-files.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetTerm](./jetterm-function.md)
