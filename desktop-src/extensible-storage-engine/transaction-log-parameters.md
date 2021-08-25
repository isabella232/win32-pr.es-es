---
description: 'Más información sobre: Parámetros del registro de transacciones'
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
ms.openlocfilehash: 24c8665b42aad5c94db18e3a30a2b5ea09974627
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465082"
---
# <a name="transaction-log-parameters"></a>Parámetros de registro de transacciones


_**Se aplica a:** Windows | Windows Servidor_

**En este artículo**  
Parámetros de registro de transacciones  
Requisitos  
Consulte también  

## <a name="transaction-log-parameters"></a>Parámetros de registro de transacciones

Este tema contiene parámetros que se usan para los registros de transacciones.

*JET_paramBaseName*  
3  

Este parámetro establece el prefijo de tres letras utilizado para muchos de los archivos usados por el motor de base de datos. Por ejemplo, el archivo de punto de comprobación se denomina EDB. CHK de forma predeterminada porque EDB es el nombre base predeterminado. El nombre base se puede usar para distinguir fácilmente entre conjuntos de archivos que pertenecen a instancias diferentes o a aplicaciones diferentes.


| | | <p>Valor predeterminado:</p> | <p>"edb"</p> | | <p>Escriba:</p> | <p>Cadena</p> | | <p>Intervalo válido:</p> | <p>3 caracteres</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramCircularLog*  
17  

Este parámetro configura cómo administra el motor de base de datos los archivos de registro de transacciones.

Cuando el registro circular está desactivado, todos los archivos de registro de transacciones que se generan se conservan en el disco hasta que ya no son necesarios porque se ha realizado una copia de seguridad completa de la base de datos. En este modo, es posible restaurar desde una copia de seguridad anterior y reproducir todos los archivos de registro de transacciones retenido, de modo que no se pierda ningún dato como resultado del desastre que forzó la restauración. Se requieren copias de seguridad completas periódicas para evitar que el disco se llene con archivos de registro de transacciones.

Cuando el registro circular está habilitado, solo los archivos de registro de transacciones que son más pequeños que el punto de control actual se conservan en el disco. La ventaja de este modo es que las copias de seguridad no son necesarias para retirar los archivos de registro de transacciones antiguos. La solución es que ya no es posible una restauración de pérdida de datos cero.


| | | <p>Valor predeterminado:</p> | <p>Falso</p> | | <p>Escriba:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramCommitDefault*  
16  

Este parámetro controla la acción predeterminada realizada cuando se confirma la transacción más externa en una sesión. Cualquier opción válida que se pueda pasar a [JetCommitTransaction](./jetcommittransaction-function.md) también se puede convertir en la opción predeterminada para todas las sesiones de una instancia o para una sesión específica. Consulte [JetCommitTransaction para](./jetcommittransaction-function.md) obtener más detalles sobre estas opciones.

Este parámetro tiene un impacto en la confiabilidad y el rendimiento de las transacciones. Consulte [JetCommitTransaction para](./jetcommittransaction-function.md) obtener más detalles.


| | | <p>Valor predeterminado:</p> | <p>0</p> | | <p>Escriba:</p> | <p>JET_GRBIT (entero)</p> | | <p>Intervalo válido:</p> | <p>Una opción válida para JetCommitTransaction</p> | | <p>Ámbito:</p> | <p>Instancia o sesión</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramDeleteOldLogs*  
48  

Cuando este parámetro es true y los archivos de registro de transacciones a los que apunta la ruta de acceso del archivo de registro (**JET_paramLogFilePath**) son una versión obsoleta, esos archivos de registro de transacciones se eliminarán automáticamente.

**Windows 2000:**  Debe tener cuidado con el uso de este parámetro al actualizar una base de datos de Windows NT a Windows 2000. Si la base de datos no está en un estado coherente y se eliminan los archivos de registro antiguos, se perderá el contenido de la base de datos.


| | | <p>Valor predeterminado:</p> | <p><strong>Windows 2000:</strong>  Falso</p><p><strong>Windows XP:</strong>  Verdad</p> | | <p>Escriba:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramIgnoreLogVersion*  
47  

Si este parámetro es true, el motor de base de datos no validará el número de versión del archivo de registro de transacciones durante [JetInit](./jetinit-function.md).

**Windows XP:**  A Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.


| | | <p>Valor predeterminado:</p> | <p>Falso</p> | | <p>Escriba:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramLegacyFileNames*  
136  

Este parámetro proporciona compatibilidad con versiones anteriores con las convenciones de nomenclatura de archivos de versiones anteriores del motor de base de datos.

Actualmente se admiten las siguientes opciones:

JET_bitESE98FileNames

Cuando esta opción está presente, el motor de base de datos usará las siguientes convenciones de nomenclatura para sus archivos:

  - Los archivos de registro de transacciones usarán . LOG para su extensión de archivo

  - Los archivos de punto de comprobación usarán . CHK para su extensión de archivo


| | | <p>Valor predeterminado:</p> | <p>JET_bitESE98FileNames</p> | | <p>Escriba:</p> | <p>JET_GRBIT (entero)</p> | | <p>Intervalo válido:</p> | <p>0, JET_bitESE98FileNames</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Windows Vista y versiones posteriores</p> | 



*JET_paramLogBuffers*  
12  

Este parámetro configurará la cantidad de memoria usada para almacenar en caché las entradas de registro antes de que se escriban en el archivo de registro de transacciones. La unidad de este parámetro es el tamaño de sector del volumen que contiene los archivos de registro de transacciones. El tamaño del sector es casi siempre de 512 bytes, por lo que es seguro asumir ese tamaño para la unidad.

Este parámetro afecta al rendimiento. Cuando el motor de base de datos está bajo una carga de actualización intensa, este búfer puede estar lleno muy rápidamente. Un tamaño de caché mayor para el archivo de registro de transacciones es fundamental para un buen rendimiento de actualización en una condición de carga tan alta. Se sabe que el valor predeterminado es demasiado pequeño para este caso.

**Windows XP y Windows 2000:**  En Windows XP y versiones anteriores, no se recomienda establecer este parámetro en un número de búferes mayor (en bytes) que la mitad del tamaño de un archivo de registro de transacciones.


| | | <p>Valor predeterminado:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 80</p><p><strong>Windows Vista:</strong> 126</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 80 – 2147483647</p><p><strong>Windows Vista:</strong> 1 – 2147483647</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramLogCheckpointPeriod*  
14  

Este parámetro configura el motor de base de datos para que tome un punto de control cuando se haya generado el número especificado de sectores de archivo de registro.

**Windows XP:**  A Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.


| | | <p>Valor predeterminado:</p> | <p>1024</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramLogFileCreateAsynch*  
69  

Cuando este parámetro se establece en true, el motor de base de datos creará el siguiente archivo de registro de transacciones a medida que se consuma el archivo de registro de transacciones actual. La intención es minimizar el tiempo invertido en cambiar de un archivo de registro de transacciones al siguiente bajo una carga de actualización intensa.


| | | <p>Valor predeterminado:</p> | <p>Verdadero</p> | | <p>Escriba:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramLogFilePath*  
2 

Este parámetro indica la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá los registros de transacciones de la instancia. La ruta de acceso debe terminarse con un carácter de barra diagonal inversa, lo que indica que la ruta de acceso de destino es una carpeta. Los archivos de registro de transacciones contienen la información necesaria para poner los archivos de base de datos en un estado coherente después de un bloqueo. Normalmente se denominan \* EDB. REGISTRO. El contenido de los archivos de registro de transacciones es igual de importante (si no es más) que los propios archivos de base de datos. Se debe hacer todo lo posible para protegerlos.

También habrá archivos de registro de reserva adicionales denominados RES1. LOG y RES2. LOG almacenado junto con los archivos de registro normales. El contenido de estos archivos no es importante, ya que su único propósito es reservar espacio en disco para permitir que el motor se apague correctamente en un escenario de disco bajo. También será un archivo de registro temporal denominado normalmente EDBTMP. LOG en esta misma carpeta. El contenido de este archivo tampoco es importante. Este archivo es un nuevo archivo de registro que se está preparando para su uso.

Las propiedades del volumen de host de los archivos de registro de transacciones y su ubicación con respecto a los demás archivos usados por el motor de base de datos pueden afectar drásticamente al rendimiento.

**Nota**  Si se especifica una ruta de acceso relativa, será relativa al directorio de trabajo actual del proceso que hospeda la aplicación que usa el motor de base de datos.


| | | <p>Valor predeterminado:</p> | <p>".\"</p> | | <p>Escriba:</p> | <p>Ruta de acceso de carpeta (cadena)</p> | | <p>Intervalo válido:</p> | <p>De 0 a 246 caracteres</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramLogFileSize*  
11  

Este parámetro configurará el tamaño de los archivos de registro de transacciones. Cada archivo de registro de transacciones tiene un tamaño fijo. El tamaño es igual al valor de este parámetro del sistema en unidades de 1024 bytes.

Este parámetro tiene un impacto en la confiabilidad. Si la configuración es demasiado pequeña, el número máximo de archivos de registro (1048575) se alcanzará mucho más rápido. Cuando esto sucede, la instancia debe cerrarse correctamente, se deben eliminar los archivos de registro existentes y se debe reiniciar la instancia. Esta acción no solo reducirá la disponibilidad de la aplicación, sino que también invalidará las copias de seguridad anteriores de la base de datos de la aplicación.

Este parámetro tiene un impacto en el rendimiento. Si el valor es muy grande, [JetInit](./jetinit-function.md) será lento porque el motor de base de datos debe leer el archivo de registro de ingesta (como mínimo) cuando se inicializa. Si la configuración es muy grande, también se tarda más tiempo en cambiar entre los archivos de registro. Si la configuración es muy pequeña, se tendrán que crear más archivos de registro para un número determinado de actualizaciones, lo que agregará más sobrecarga.


| | | <p>Valor predeterminado:</p> | <p>5120</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 128 – 32768</p><p><strong>Windows Vista:</strong> 64 – 32768</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramLogWaitingUserMax*  
15  

Este parámetro intenta optimizar el vaciado del búfer de registro causado por una confirmación duradera al esperar a que un número especificado de sesiones espere a una confirmación duradera antes de forzar que se produzca un vaciado con la esperanza de que otra transacción comparta el vaciado.

**Windows XP:**  A Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.


| | | <p>Valor predeterminado:</p> | <p>3</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramRecovery*  
34  

Este parámetro es el conmutador maestro que controla la recuperación de bloqueos de una instancia. Si este parámetro se establece en "On", se usará la recuperación de estilo ARIES para poner todas las bases de datos de la instancia en un estado coherente en caso de bloqueo de un proceso o equipo. Si este parámetro se establece en "Desactivado", todas las bases de datos de la instancia se administrarán sin la ventaja de la recuperación de bloqueos. Es decir, si la instancia no se apaga limpiamente mediante [JetTerm](./jetterm-function.md) antes de que el proceso salga o se apague la máquina, el contenido de todas las bases de datos de esa instancia se dañará.

Deshabilitar la recuperación es útil en circunstancias especiales en las que se sabe que el contenido de una base de datos no es útil en caso de bloqueo. La recuperación debe estar habilitada para todos los demás casos.


| | | <p>Valor predeterminado:</p> | <p>"On"</p> | | <p>Escriba:</p> | <p>Cadena</p> | | <p>Intervalo válido:</p> | <p>De 0 a 259 caracteres</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramSystemPath*  
0  

Este parámetro indica la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá el archivo de punto de comprobación de la instancia. La ruta de acceso debe terminarse con un carácter de barra diagonal inversa, lo que indica que la ruta de acceso de destino es una carpeta. El archivo de punto de comprobación es un archivo simple que se mantiene por instancia y que recuerda el archivo de registro de transacciones más antiguo que se debe reproducir para que todas las bases de datos de esa instancia se mantengan en un estado coherente después de un bloqueo. El archivo de punto de comprobación se denomina normalmente EDB. CHK.

**Nota**  Si se especifica una ruta de acceso relativa, será relativa al directorio de trabajo actual del proceso que hospeda la aplicación que usa el motor de base de datos.


| | | <p>Valor predeterminado:</p> | <p>".\"</p> | | <p>Escriba:</p> | <p>Ruta de acceso de carpeta (cadena)</p> | | <p>Intervalo válido:</p> | <p>De 0 a 246 caracteres</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramWaitLogFlush*  
13 

Este parámetro intenta optimizar el vaciado del búfer de registro causado por una confirmación duradera al esperar un período de tiempo especificado antes de forzar que se produzca un vaciado con la esperanza de que otra transacción comparta el vaciado.

**Windows XP:**  A Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.


| | | <p>Valor predeterminado:</p> | <p>0</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Ámbito:</p> | <p>Instancia o sesión</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>All</p> | 



*JET_paramLegacyFileNames*  
136  

Este parámetro se usa para especificar las características de compatibilidad de nomenclatura de archivos que se deben mantener con Windows Server 2003 y el esquema de nomenclatura de archivos anterior. Para obtener más información sobre los diferentes archivos y su nomenclatura, vea [Extensible Storage Engine Files](./extensible-storage-engine-files.md).

El JET_bitESE98FileNames garantiza que la extensión de archivo usada en los archivos de registro de transacciones y el archivo de punto de comprobación son los mismos que los que se usan en Windows Server 2003. Tenga en cuenta que si se actualiza desde Windows Server 2003, todavía no es necesario especificar este bit, ya que el motor actualizará automáticamente las extensiones de archivo si JET_paramCircularLog está establecido en **true** o mantendrá la extensión de registro anterior si JET_paramCircularLog es **false**.

**Nota**  Para establecer un bit, primero se debe recuperar el valor y, a continuación, "or" en el bit de compatibilidad deseado.


| | | <p>Valor predeterminado:</p> | <p>JET_bitESE98FileNames</p> | | <p>Escriba:</p> | <p>JET_GRBIT (entero)</p> | | <p>Intervalo válido:</p> | <p>JET_bitESE98FileNames</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>A partir de Windows Server 2008 y Windows Vista</p> | 



## <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



## <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetTerm](./jetterm-function.md)
