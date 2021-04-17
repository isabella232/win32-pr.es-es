---
description: Más información acerca de los archivos del motor de almacenamiento extensible
title: Archivos del motor de almacenamiento extensible
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: c27bb0104c5923496c5dd7962ef4a9bacdc90af4
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717453"
---
# <a name="extensible-storage-engine-files"></a>Archivos del motor de almacenamiento extensible


_**Se aplica a:** Windows | Windows Server_

## <a name="extensible-storage-engine-files"></a>Archivos del motor de almacenamiento extensible

El motor de almacenamiento extensible usa los siguientes tipos de archivos:

- [Archivos de registro de transacciones](#transaction-log-files)

- [Archivos de registro de transacciones temporales](#temporary-transaction-log-files)

- [Archivos de registro de transacciones reservados](#reserved-transaction-log-files)

- [Archivos de puntos de control](#checkpoint-files)

- [Archivos de la base de datos](#database-files)

- [Bases de datos temporales](#temporary-databases)

- [Vaciar archivos de asignación](#flush-map-files)

Esta tabla contiene información general de los nombres de los archivos de datos administrados por ESE. En Windows Vista y versiones posteriores, el valor JET_paramLegacyNames afecta a los nombres de archivo que se usan.

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p>Sistema operativo</p>
    </th>
    <th>
      <p>Windows Server 2003 y versiones anteriores<br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p>Windows Vista y versiones posteriores (cliente) <br />
Windows Server 2008 y versiones posteriores (servidor)
</p>
    </th>
    <th>
      <p>Actualización de aniversario de Windows 10 y versiones posteriores (cliente) <br />
Windows Server 2016 y versiones posteriores (servidor)
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p>
        <strong>JET_paramLegacyNames configuración</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>N/A</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>Ninguna</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>JET_bitESE98FileNames</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>Igual que Windows Vista/servidor 2008</strong>
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <p>Registro actual</p>
    </td>
    <td>
      <p>&lt;INST &gt; . log</p>
    </td>
    <td>
      <p>&lt;INST &gt; . JTX</p>
    </td>
    <td>
      <p>&lt;INST &gt; . log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Registro previo a la inicialización</p>
    </td>
    <td>
      <p>&lt;INST &gt; . log tmp</p>
    </td>
    <td>
      <p>&lt;INST &gt; tmp. JTX</p>
    </td>
    <td>
      <p>&lt;INST &gt; . log tmp</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Registros girados</p>
    </td>
    <td>
      <p>&lt;INST &gt; . log</p>
    </td>
    <td>
      <p>&lt;INST &gt; . JTX después de FFFFF cambie a &lt; inst &gt; xxxxxxxx. JTX</p>
    </td>
    <td>
      <p>&lt;Inst. &gt; log después de FFFFF cambie a &lt; inst &gt; xxxxxxxx. log.</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Archivos de punto de comprobación</a>
      </p>
    </td>
    <td>
      <p>&lt;INST &gt; . chk</p>
    </td>
    <td>
      <p>&lt;INST &gt; . JCP</p>
    </td>
    <td>
      <p>&lt;INST &gt; . chk</p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Bases de datos temporales</a>
      </p>
    </td>
    <td>
      <p>&lt;Temp. edb del nombre de archivo de la base de archivos temporal &gt; : tmp. edb</p>
    </td>
    <td>
      <p>&lt;Temp. edb del nombre de archivo de la base de archivos temporal &gt; : tmp. edb</p>
    </td>
    <td>
      <p>&lt;Temp. edb del nombre de archivo de la base de archivos temporal &gt; : tmp. edb</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Archivos de registro de transacciones reservados</a>
      </p>
    </td>
    <td>
      <p>res1. log &amp; Res2. log</p>
    </td>
    <td>
      <p>&lt;INST &gt; RESXXXXX. JRS</p>
    </td>
    <td colspan="2">
      <p>&lt;INST &gt; RESXXXXX. JRS</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Archivos de base de datos</a>
      </p>
    </td>
    <td>
      <p>&lt;nombre de archivo de base de archivos&gt;</p>
    </td>
    <td>
      <p>&lt;nombre de archivo de base de archivos&gt;</p>
    </td>
    <td>
      <p>&lt;nombre de archivo de base de archivos&gt;</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Vaciar archivos de asignación</a>
      </p>
    </td>
    <td>
      <p>N/D</p>
    </td>
    <td>
      <p>N/D</p>
    </td>
    <td>
      <p>N/D</p>
    </td>
    <td>
      <p>&lt;nombre de archivo de base de archivo sin extensión &gt; . JFM</p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a>Archivos de registro de transacciones

Los archivos de registro de transacciones contienen operaciones en archivos de base de datos. Contienen información suficiente para poner una base de datos a un estado coherente lógicamente después de una terminación de proceso inesperada o un cierre del sistema.

Los nombres de los archivos de registro dependen de un nombre base de tres letras, que se puede establecer con [JET_paramBaseName](./transaction-log-parameters.md). En los ejemplos siguientes se usa un nombre base de "edb", ya que es el nombre base predeterminado. La extensión de los archivos de registro de transacciones será. log o. JTX, dependiendo de si el JET_bitESE98FileNames se establece en el parámetro JET_paramLegacyFileNames. Para obtener más información, vea [parámetros del sistema del motor de almacenamiento extensible](./extensible-storage-engine-system-parameters.md).

Los archivos de registro de transacciones se denominan \<base\> \<generation-number\> . log, comenzando por 1. El número de generación de registro está en formato hexadecimal. Por ejemplo, edb00001. log es el primer registro y edb000ff. log es el registro 255th. Los archivos de registro tienen cinco dígitos hexadecimales en el nombre del archivo de registro, hasta el archivo de registro 1048576th, momento en el que los archivos de registro empiezan a denominarse en un formato 11,3 (por ejemplo, edb00100000. log). \<base\>. log siempre es el archivo de registro que se está usando actualmente. Si el motor de base de datos no está activo, la generación de edb. log puede identificarse con el siguiente comando: **esentutl.exe-ml EDB. log**.

Aunque los archivos de registro de transacciones tienen el. Extensión de registro asociada normalmente a archivos de texto, los archivos de registro de transacciones están en formato binario y nunca deben ser editados por un usuario. Las operaciones de base de datos se escriben primero en el registro. Los datos se pueden escribir más adelante en el archivo de base de datos. posiblemente de inmediato, posiblemente más tarde. En caso de que se produzca un proceso inesperado o una terminación del sistema, las operaciones seguirán presentes en los archivos de registro y se pueden revertir las transacciones incompletas. La acción de reproducir archivos de registro de transacciones se denomina *recuperación de software* y se realiza automáticamente cuando se llama a [JetInit](./jetinit-function.md) o [JetInit2](./jetinit2-function.md) . La recuperación de software también puede realizarse manualmente con la opción "-r" del programa Esentutl.exe. La acción de reproducir archivos de registro de transacciones en una base de datos restaurada a partir de una copia de seguridad se denomina *recuperación de hardware*.

Los archivos de registro tienen un tamaño fijo, personalizable con [JET_paramLogFileSize](./transaction-log-parameters.md). Cuando se rellena el archivo de registro actual (es decir, EDB. log), se le cambia el nombre a \<base\> \<generation-number\> . log y se necesita un nuevo archivo de registro de transacciones en la secuencia del registro de transacciones.

Cada instancia de base de datos tiene asociada una única secuencia de archivos de registro. Windows XP presentó [JetCreateInstance](./jetcreateinstance-function.md), lo que permite usar varias secuencias de archivos de registro de transacciones en un único proceso. Sin embargo, no pueden existir varias secuencias de archivo de registro de transacciones en el mismo directorio.

Los archivos de registro de transacciones nunca deben manipularse, cambiarse de nombre, moverse o eliminarse de forma manual, ya que pueden producirse daños en los datos.

El motor de base de datos eliminará los archivos de registro de transacciones durante una copia de seguridad completa (vea [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)), o durante las operaciones normales, si está habilitado el registro circular.

Una vez que se llena un archivo de registro de transacciones, el motor de base de datos debe crear un nuevo archivo de registro. El registro circular es un medio por el que el motor de base de datos puede limpiar automáticamente los archivos de registro cuando ya no son necesarios para la recuperación tras bloqueo. Este proceso es una alternativa a la eliminación de archivos de registro como un producto de la realización de una copia de seguridad. El registro circular se puede controlar con el parámetro del sistema [JET_paramCircularLog](./transaction-log-parameters.md) . Los archivos de registro de transacciones no se deben eliminar con ningún otro método.

### <a name="temporary-transaction-log-files"></a>Archivos de registro de transacciones temporales

Cuando se llena EDB. log, ESE debe crear un nuevo archivo. El nuevo archivo de transacción de registro se conoce como archivo de registro de transacciones temporal antes de que lo use ESE.

Mientras se crea un nuevo archivo de registro y su tamaño se extiende, se denominará \<base\> tmp. log. La creación de un nuevo archivo puede ser una operación potencialmente costosa, por lo que ESE creará el siguiente archivo de registro de forma proactiva como una tarea en segundo plano.

Dado que el archivo de registro de transacciones temporal se crea en previsión de necesidad de un nuevo archivo de registro de transacciones, no contiene ninguna información útil.

### <a name="reserved-transaction-log-files"></a>Archivos de registro de transacciones reservados

Los archivos de registro de transacciones reservados se crean cuando el motor comienza a permitir que se registren operaciones importantes para obtener un cierre correcto.

**Windows Vista:** En Windows Vista y versiones posteriores, los archivos de registro de transacciones reservados se denominan \<base\> RESXXXXX. JRS.

**Windows Server 2003:** En Windows Server 2003 y versiones anteriores, los archivos de registro de transacciones reservados se denominan res1. log y Res2. log.

Cuando el motor de base de datos se queda sin espacio en disco, no puede crear un nuevo archivo de registro. Lo más seguro es cerrar sin problemas, pero es necesario registrar algunas operaciones (como las operaciones de reversión). La mayoría de las operaciones de base de datos producirán errores durante esta fase.

Dado que los archivos de registro de transacciones reservados se crean en previsión de necesidad de archivos de registro de transacciones en un escenario fuera de disco, no contienen ninguna información útil.

### <a name="checkpoint-files"></a>punto de comprobación, archivos

El archivo de punto de comprobación almacena el punto de control para una secuencia de archivo de registro de transacciones determinada. El archivo de punto de comprobación se denomina \<base\> . chk o \<base\> . JCP, dependiendo de si el JET_bitESE98FileNames se establece en el parámetro JET_paramLegacyFileNames y [JET_paramSystemPath](./transaction-log-parameters.md)proporciona su ubicación.

Las operaciones de base de datos se escriben primero en los archivos de registro y, a continuación, se almacenan en la memoria caché. En algún momento posterior, las operaciones se escriben en el archivo de base de datos, pero por razones de rendimiento, el orden en el que se escriben las operaciones en el archivo de base de datos podría no coincidir con el orden en el que se registraron originalmente. Las operaciones escritas en el archivo de registro de transacciones estarán en uno de estos dos Estados:

  - Se escriben en el archivo de registro de transacciones y en el archivo de base de datos.

  - Se escribe en el archivo de registro de transacciones y aún no se ha escrito en el archivo de base de datos.

Muchas operaciones de base de datos se pueden almacenar en un único archivo de registro de transacciones. Un archivo de registro determinado puede estar formado por los siguientes elementos:

  - Todas las operaciones escritas en el archivo de base de datos.

  - No se han escrito operaciones en el archivo de base de datos

  - Combinación de operaciones escritas en el archivo de base de datos y operaciones que todavía no se han escrito en el archivo de base de datos.

El punto de control hace referencia al punto en el tiempo en la secuencia del registro de transacciones, donde todas las operaciones anteriores al punto de control se han escrito en el archivo de base de datos. No hay ninguna garantía sobre las operaciones que se producen después del punto de control; algunos pueden estar en memoria y otros pueden escribirse en la base de datos.

Dado que todas las operaciones en los archivos de registro antes del punto de control se representan en el archivo de base de datos, solo se necesitan los archivos de registro de transacciones después del punto de control para que la recuperación de software Ponga una base de datos determinada en un estado limpio.

### <a name="database-files"></a>Archivos de la base de datos

El archivo de base de datos contiene el esquema de todas las tablas de la base de datos, los registros de todas las tablas de la base de datos y los índices de las tablas. Su ubicación se proporciona con [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md)o [JetAttachDatabase2](./jetattachdatabase2-function.md).

Una base de datos se cierra correctamente solo después de una llamada correcta a [JetTerm](./jetterm-function.md) o [JetTerm2](./jetterm2-function.md).

El programa Esentutl.exe puede detectar si una base de datos se cierra correctamente con la opción "-MH". Por ejemplo, "esentutl.exe-AG sample. edb" leerá el encabezado de la base de datos de una base de datos denominada sample. edb e imprimirá el estado de sample. edb. Puede imprimir "estado: cierre correcto" o "estado: cierre con errores".

Una base de datos que no se ha cerrado correctamente se encuentra en un estado de cierre con errores. Antes de Windows XP, este estado se llamaba *incoherente*. Una base de datos desfasada (incoherente) se puede trasladar a un estado limpio con recuperación de software. Una base de datos dañada no es lo mismo que una base de datos desfasada ("incoherente").

Una base de datos dañada hace referencia a un daño físico o lógico, y no se puede corregir con la recuperación de software. Los daños físicos pueden ser volteo de bits, que se capturan con frecuencia en las sumas de comprobación de las páginas de base de datos. Una suma de comprobación con errores en un archivo de base de datos se manifiesta como un error de JET_errReadVerifyFailure.

Solo las bases de datos que se cierran correctamente pueden moverse o cambiarse de nombre con seguridad. Si una base de datos no se ha cerrado correctamente, no se puede cambiar o cambiar de nombre automáticamente.

Varias bases de datos se pueden asociar a una sola secuencia de archivos de registro de transacciones.

### <a name="temporary-databases"></a>Bases de datos temporales

La base de datos temporal se usa como una memoria auxiliar para temptables y también se usa al crear índices.

El nombre y la ubicación se configuran con [JET_paramTempPath](./temporary-database-parameters.md).

Temptables se crean con [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md). También se crean mediante algunas llamadas API y se usan para devolver información de esquema (por ejemplo, [JetGetIndexInfo](./jetgetindexinfo-function.md)).

## <a name="flush-map-files"></a>Vaciar archivos de asignación

A partir de la actualización de aniversario (cliente) de Windows 10 y Windows Server 2016 (servidor), ESE agregó un nivel adicional de protección contra las escrituras perdidas (o vaciados perdidos) 1, lo que permite detectar eventos initialization2 de este tipo. Esta característica requiere la persistencia de metadatos en un archivo independiente denominado archivo de "mapa de vaciado".

Se crea un archivo de mapa de vaciado para cada archivo de base de datos y se encuentra en el mismo directorio. El archivo se denomina de forma similar al archivo de base de datos, pero con una extensión diferente. Por ejemplo, si la aplicación cliente crea una base de datos con la ruta de acceso completa C: mi \\ Director \\ MyDabatase. edb, su archivo de mapa de vaciado correspondiente es C: mi \\ Director \\ MyDabatase. JFM.

Esta mejora presenta dos requisitos para el nombre de los archivos de base de datos:

  - Dos bases de datos del mismo directorio no deben tener el mismo nombre de archivo con extensiones diferentes. Por ejemplo: C: \\ \\ MyDabatase. db1 y c: mi \\ Director \\ MyDabatase. DB2.

  - 2\. Una base de datos no debe tener una extensión. JFM.

Al copiar o trasladar un archivo de base de datos manualmente, su archivo de mapa de vaciado correspondiente también debe copiarse o moverse al mismo directorio de destino, respectivamente. Si no hay un archivo de mapa de vaciado en el momento de una nueva base de datos adjunta (a través de [JetAttachDatabase](./jetattachdatabase-function.md), se creará un nuevo y se volverá a rellenar a petición a medida que las páginas se leen en la base de datos. ESE controla la combinación de archivos de mapa de bits y de base de datos no coincidentes, y obliga a que se elimine el mapa de vaciado no coincidente y se vuelva a crear desde cero.

El tamaño de un archivo de mapa de vaciado es directamente proporcional a su archivo de base de datos asociado y aproximadamente igual a (todos los tamaños en bytes, el resultado se debe redondear al siguiente múltiplo de 8.192):

`8,192 + ((<database file size> / <database page size>) / 4)`

Por ejemplo: para una base de datos de 1,5 GB con un tamaño de página de 32 KB, el tamaño aproximado del mapa de vaciado es 24.576 bytes (o 24KB).

El archivo de mapa de vaciado debe actualizarse a medida que se vacíen las páginas de la base de datos. Si el registro transaccional está habilitado (por ejemplo, [JET_paramRecovery](./transaction-log-parameters.md) establecido en "ON", el valor predeterminado), la actualización del mapa de vaciado se realiza a medida que la aplicación cliente realiza modificaciones en la base de datos. En promedio, todo el mapa de vaciado se escribe en el medio no volátil una vez por cada 20% de [JET_paramCheckpointDepthMax](./database-cache-parameters.md) (en bytes) de los registros transaccionales generados. El número de operaciones de escritura depende de cómo se distribuyan las modificaciones en la base de datos. Pero, a lo sumo, aproximadamente (todos los tamaños en bytes):

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

Si el registro transaccional está deshabilitado (por ejemplo, [JET_paramRecovery](./transaction-log-parameters.md) establecido en "OFF"), el mapa de vaciado se actualiza solo una vez cuando la base de datos se separa explícitamente (a través de [JetDetachDatabase](./jetdetachdatabase-function.md), o bien se desasocia implícitamente al terminar la instancia de ese asociada (a través de cualquiera de las funciones [JetTerm](./jetterm-function.md) , siempre y cuando no se pase [JET_bitTermDirty](./jetterm2-function.md) ).

1 una escritura perdida (o vaciado perdido) se define como una operación de escritura que se devuelve correctamente desde el sistema operativo al motor de base de datos de ESE, pero los datos reales nunca se conservan en el archivo de base de datos en los medios no volátiles. Normalmente se debe a una pila de almacenamiento mal configurada o mal configurada (software o hardware). Las aplicaciones cliente pueden recibir un error de [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) de las funciones de ese que requieren leer datos de la base de datos si los datos se encuentran en una región que ha sufrido un evento de escritura perdido.

2 la capacidad de detectar escrituras perdidas dentro de la duración de un proceso ha estado presente desde Windows 8 (cliente) y Windows Server 2012 (servidor).
