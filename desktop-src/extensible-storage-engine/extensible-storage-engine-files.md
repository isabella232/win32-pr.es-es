---
description: 'Más información sobre: Archivos extensibles Storage engine'
title: Archivos extensibles Storage engine
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: a955da455cb2a2397010fd7869f6320970ef9f85ac1e1602f4439239dc56b167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118256398"
---
# <a name="extensible-storage-engine-files"></a>Archivos extensibles Storage engine


_**Se aplica a:** Windows | Windows Servidor_

## <a name="extensible-storage-engine-files"></a>Archivos extensibles Storage engine

El motor Storage extensible usa los siguientes tipos de archivos:

- [Archivos de registro de transacciones](#transaction-log-files)

- [Archivos de registro de transacciones temporales](#temporary-transaction-log-files)

- [Archivos de registro de transacciones reservados](#reserved-transaction-log-files)

- [Archivos de puntos de control](#checkpoint-files)

- [Archivos de la base de datos](#database-files)

- [Bases de datos temporales](#temporary-databases)

- [Vaciar archivos de mapa](#flush-map-files)

Esta tabla contiene información general de los nombres de archivo de datos administrados por ESE. Por Windows Vista y versiones posteriores, el JET_paramLegacyNames de archivo afecta a los nombres de archivo que se usan.

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
      <p>Windows 10 Actualización de aniversario y versiones posteriores (cliente) <br />
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
        <strong>Igual que Windows Vista/Server 2008</strong>
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <p>Registro actual</p>
    </td>
    <td>
      <p>&lt;inst &gt; .log</p>
    </td>
    <td>
      <p>&lt;inst &gt; .jtx</p>
    </td>
    <td>
      <p>&lt;inst &gt; .log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Registro previo al inicio de sesión</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp.log</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp.jtx</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp.log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Registros girados</p>
    </td>
    <td>
      <p>&lt;inst &gt; XXXXX.log</p>
    </td>
    <td>
      <p>&lt;inst &gt; XXXXX.jtx después de que FFFFF cambie a &lt; inst &gt; XXXXXXXX.jtx</p>
    </td>
    <td>
      <p>&lt;inst &gt; XXXXX.log después de que FFFFF cambie a &lt; inst &gt; XXXXXXXX.log.</p>
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
      <p>&lt;inst &gt; .chk</p>
    </td>
    <td>
      <p>&lt;inst &gt; .jcp</p>
    </td>
    <td>
      <p>&lt;inst &gt; .chk</p>
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
      <p>&lt;nombre de archivo temp db &gt; Predeterminado: tmp.edb</p>
    </td>
    <td>
      <p>&lt;nombre de archivo temp db &gt; Predeterminado: tmp.edb</p>
    </td>
    <td>
      <p>&lt;nombre de archivo temp db &gt; Predeterminado: tmp.edb</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Archivos de registro de transacciones reservados</a>
      </p>
    </td>
    <td>
      <p>res1.log &amp; res2.log</p>
    </td>
    <td>
      <p>&lt;inst &gt; RESXXXXX.jrs</p>
    </td>
    <td colspan="2">
      <p>&lt;inst &gt; RESXXXXX.jrs</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Archivos de base de datos</a>
      </p>
    </td>
    <td>
      <p>&lt;nombre de archivo db&gt;</p>
    </td>
    <td>
      <p>&lt;nombre de archivo db&gt;</p>
    </td>
    <td>
      <p>&lt;nombre de archivo db&gt;</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Vaciar archivos de mapa</a>
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
      <p>&lt;nombre de archivo db sin la &gt; extensión .jfm</p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a>Archivos de registro de transacciones

Los archivos de registro de transacciones contienen operaciones en archivos de base de datos. Contienen información suficiente para poner una base de datos en un estado coherente lógicamente después de una finalización inesperada del proceso o cierre del sistema.

Los nombres de los archivos de registro dependen de un nombre base de tres letras, que se puede establecer con [JET_paramBaseName](./transaction-log-parameters.md). En los ejemplos siguientes se usa un nombre base de "edb", porque es el nombre base predeterminado. La extensión de los archivos de registro de transacciones será .log o .jtx en función de si el JET_bitESE98FileNames se establece en el JET_paramLegacyFileNames de transacciones. Para obtener más información, vea [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md).

Los archivos de registro de transacciones se \<base\> \<generation-number\> denominan .log, empezando por 1. El número de generación de registros está en formato hexadecimal. Por ejemplo, edb00001.log es el primer registro y edb000ff.log es el registro 255. Los archivos de registro tienen cinco dígitos hexadecimales en el nombre del archivo de registro, hasta el archivo de registro 1048576, momento en el que los archivos de registro comienzan a denominar en un formato 11.3 (por ejemplo, edb00100000.log). \<base\>.log siempre es el archivo de registro que se está utilizando actualmente. Si el motor de base de datos no está activo, la generación de edb.log se puede identificar mediante el siguiente comando: **esentutl.exe -ml edb.log**.

Aunque los archivos de registro de transacciones tienen . La extensión LOG normalmente asociada a archivos de texto, los archivos de registro de transacciones están en formato binario y nunca deben ser editados por un usuario. Las operaciones de base de datos se escriben primero en el registro. Los datos se pueden escribir en el archivo de base de datos más adelante; posiblemente inmediatamente, posiblemente mucho más tarde. Si se produce un proceso inesperado o una terminación del sistema, las operaciones siguen estando presentes en los archivos de registro y se pueden revertir transacciones incompletas. El acto de reproducir archivos de registro de transacciones se denomina *recuperación flexible* y se realiza automáticamente cuando se llama a [JetInit](./jetinit-function.md) o [JetInit2.](./jetinit2-function.md) La recuperación flexible también se puede realizar manualmente con la opción "-r" del Esentutl.exe programa. El acto de reproducir archivos de registro de transacciones en una base de datos restaurada a partir de una copia de seguridad se denomina *recuperación en disco.*

Los archivos de registro tienen un tamaño fijo, personalizable con [JET_paramLogFileSize](./transaction-log-parameters.md). Cuando se rellena el archivo de registro actual (es decir, edb.log), se cambia el nombre a .log y se necesita un nuevo archivo de registro de transacciones en la secuencia del registro \<base\> \<generation-number\> de transacciones.

Cada instancia de base de datos tiene asociada una secuencia de archivo de registro única. Windows XP introdujo [JetCreateInstance,](./jetcreateinstance-function.md)lo que permite que un único proceso utilice varias secuencias de archivos de registro de transacciones. Sin embargo, no pueden existir varias secuencias de archivo de registro de transacciones en el mismo directorio.

Los archivos de registro de transacciones casi nunca se deben manipular, cambiar de nombre, mover o eliminar manualmente porque los datos pueden resultar dañados.

El motor de base de datos eliminará los archivos de registro de transacciones durante una copia de seguridad completa (consulte [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance)](./jettruncateloginstance-function.md)o durante las operaciones normales, si el registro circular está habilitado.

Una vez que se rellena un archivo de registro de transacciones, el motor de base de datos debe crear un nuevo archivo de registro. El registro circular es un medio por el que el motor de base de datos puede limpiar automáticamente los archivos de registro cuando ya no son necesarios para la recuperación de bloqueos. Este proceso es una alternativa a la eliminación de archivos de registro como producto de realizar una copia de seguridad. El registro circular se puede controlar con el [JET_paramCircularLog](./transaction-log-parameters.md) del sistema. Los archivos de registro de transacciones no deben eliminarse mediante ningún otro método.

### <a name="temporary-transaction-log-files"></a>Archivos de registro de transacciones temporales

Cuando edb.log se llena, ESE debe crear un nuevo archivo. El nuevo archivo de transacción de registro se conoce como archivo de registro de transacciones temporal antes de su uso por ese.

Mientras se crea un nuevo archivo de registro y se amplía su tamaño, se \<base\> denominará tmp.log. La creación de un nuevo archivo puede ser una operación potencialmente costosa, por lo que ESE creará el siguiente archivo de registro de forma proactiva como una tarea en segundo plano.

Dado que el archivo de registro de transacciones temporal se crea en previsión de la necesidad de un nuevo archivo de registro de transacciones, no contiene ninguna información útil.

### <a name="reserved-transaction-log-files"></a>Archivos de registro de transacciones reservados

Los archivos de registro de transacciones reservados se crean cuando el motor comienza a permitir que se registren operaciones importantes para obtener un apagado limpio.

**Windows Vista:** En Windows Vista y versiones posteriores, los archivos de registro de transacciones reservados se \<base\> denominan RESXXXXX.jrs.

**Windows Server 2003:** En Windows Server 2003 y versiones anteriores, los archivos de registro de transacciones reservados se denominan res1.log y res2.log.

Cuando el motor de base de datos se queda sin espacio en disco, no puede crear un nuevo archivo de registro. Lo más seguro es apagar sin problemas, pero todavía se deben registrar algunas operaciones (como las operaciones de reversión). La mayoría de las operaciones de base de datos producirán un error durante esta fase.

Dado que los archivos de registro de transacciones reservados se crean en previsión de la necesidad de archivos de registro de transacciones en un escenario fuera de disco, no contienen ninguna información útil.

### <a name="checkpoint-files"></a>punto de comprobación, archivos

El archivo de punto de comprobación almacena el punto de control para una secuencia de archivo de registro de transacciones determinada. El archivo de punto de comprobación se denomina \<base\> .chk o \<base\> .jcp, dependiendo de si el JET_bitESE98FileNames está establecido en el parámetro JET_paramLegacyFileNames y su ubicación la [especifica JET_paramSystemPath](./transaction-log-parameters.md).

Las operaciones de base de datos se escriben primero en los archivos de registro y, a continuación, se almacenan en caché en memoria. En algún momento posterior, las operaciones se escriben en el archivo de base de datos, pero por motivos de rendimiento, es posible que el orden en el que se escriben las operaciones en el archivo de base de datos no coincida con el orden en que se registraron originalmente. Las operaciones escritas en el archivo de registro de transacciones estarán en uno de estos dos estados:

  - Se escribe en el archivo de registro de transacciones y en el archivo de base de datos.

  - Se ha escrito en el archivo de registro de transacciones y aún no se ha escrito en el archivo de base de datos.

Muchas operaciones de base de datos se pueden almacenar en un único archivo de registro de transacciones. Un archivo de registro determinado puede constar de los siguientes elementos:

  - Todas las operaciones escritas en el archivo de base de datos.

  - Ninguna operación escrita en el archivo de base de datos

  - Combinación de operaciones escritas en el archivo de base de datos y operaciones que aún no se han escrito en el archivo de base de datos.

El punto de control hace referencia al momento dado en el flujo del registro de transacciones donde todas las operaciones anteriores al punto de control se han escrito en el archivo de base de datos. No hay ninguna garantía sobre las operaciones que se producen después del punto de control; Algunos podrían estar en memoria y otros se podrían escribir en la base de datos.

Puesto que todas las operaciones de los archivos de registro anteriores al punto de control se representan en el archivo de base de datos, solo se necesitan los archivos de registro de transacciones después del punto de control para que la recuperación flexible lleve una base de datos determinada a un estado limpio.

### <a name="database-files"></a>Archivos de la base de datos

El archivo de base de datos contiene el esquema de todas las tablas de la base de datos, los registros de todas las tablas de la base de datos y los índices de las tablas. Su ubicación se da mediante [JetCreateDatabase,](./jetcreatedatabase-function.md) [JetCreateDatabase2,](./jetcreatedatabase2-function.md) [JetAttachDatabase](./jetattachdatabase-function.md)o [JetAttachDatabase2.](./jetattachdatabase2-function.md)

Una base de datos se cierra correctamente solo después de una llamada correcta a [JetTerm](./jetterm-function.md) o [JetTerm2.](./jetterm2-function.md)

El Esentutl.exe puede detectar si una base de datos se cierra correctamente con la opción "-mh". Por ejemplo, "esentutl.exe -mh sample.edb" leerá el encabezado de base de datos de una base de datos denominada sample.edb e imprimirá el estado de sample.edb. Puede imprimir "State: Clean Shutdown" o "State: Dirty Shutdown".

Una base de datos que no se ha cerrado correctamente se encuentra en un estado de apagado desasedado. Antes de Windows XP, este estado se denominaba *incoherente.* Una base de datos desdesociada (incoherente) se puede llevar a un estado limpio con la recuperación flexible. Una base de datos dañada no es lo mismo que una base de datos dañada ("incoherente").

Una base de datos dañada hace referencia a daños físicos o lógicos y no se puede solucionar con la recuperación flexible. Los daños físicos pueden ser volteos de bits, que con frecuencia se detectan mediante las sumas de comprobación en las páginas de la base de datos. Una suma de comprobación con error en un archivo de base de datos se manifiesta a sí misma como JET_errReadVerifyFailure error.

Solo se puede mover o cambiar el nombre de las bases de datos de forma limpia. Si una base de datos no se cerró correctamente, no se puede mover o cambiar de nombre automáticamente de forma segura.

Se pueden asociar varias bases de datos a una única secuencia de archivos de registro de transacciones.

### <a name="temporary-databases"></a>Bases de datos temporales

La base de datos temporal se usa como un almacén de respaldo para las tablas temporales y también se usa al crear índices.

El nombre y la ubicación se configuran [con JET_paramTempPath](./temporary-database-parameters.md).

Las tablas temporales se crean [con JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2,](./jetopentemptable2-function.md) [JetOpenTempTable3](./jetopentemptable3-function.md)y [JetOpenTemporaryTable.](./jetopentemporarytable-function.md) También se crean mediante algunas llamadas API y se usan para devolver información de esquema (como [JetGetIndexInfo).](./jetgetindexinfo-function.md)

## <a name="flush-map-files"></a>Vaciar archivos de asignación

A partir de la actualización de aniversario de Windows 10 (cliente) y Windows Server 2016 (servidor), ESE agregó un nivel adicional de protección contra escrituras perdidas (o vaciados perdidos) 1, lo que le permite detectar estos eventos entre procesos de re inicialización2. Esta característica requiere conservar los metadatos en un archivo independiente denominado archivo de "mapa de vaciado".

Se crea un archivo de mapa de vaciado para cada archivo de base de datos y se encuentra en el mismo directorio. El archivo se denomina de forma similar al archivo de base de datos, pero con una extensión diferente. Por ejemplo, si la aplicación cliente crea una base de datos con la ruta de acceso completa C: MyDirectory MyDabatase.edb, su archivo de mapa de vaciado correspondiente es \\ \\ C: \\ MyDirectory \\ MyDabatase.jfm.

Esta mejora presenta dos requisitos para el nombre de los archivos de base de datos:

  - Dos bases de datos del mismo directorio no deben tener el mismo nombre de archivo con extensiones diferentes. Por ejemplo: C: \\ MyDirectory \\ MyDabatase.db1 y C: \\ MyDirectory \\ MyDabatase.db2.

  - 2\. Una base de datos no debe tener una extensión .jfm.

Al copiar o mover manualmente un archivo de base de datos, su archivo de mapa de vaciado correspondiente también debe copiarse o moverse al mismo directorio de destino, respectivamente. Si un archivo de mapa de vaciado no está presente en el momento de los datos adjuntos de una nueva base de datos (a través de [JetAttachDatabase),](./jetattachdatabase-function.md)se creará uno nuevo y se volverá a rellenar a petición a medida que se lean las páginas de la base de datos. La combinación de archivos de asignación de vaciado y base de datos no coincidentes se controla mediante ESE y obliga a eliminar y volver a crear el mapa de vaciado no coincidente desde cero.

El tamaño de un archivo de mapa de vaciado es directamente proporcional a su archivo de base de datos asociado y aproximadamente igual a (todos los tamaños en bytes, el resultado debe redondear al siguiente múltiplo de 8192):

`8,192 + ((<database file size> / <database page size>) / 4)`

Por ejemplo: para una base de datos de 1,5 GB con un tamaño de página de 32 KB, el tamaño aproximado del mapa de vaciado es de 24 576 bytes (o 24 KB).

El archivo de mapa de vaciado debe actualizarse a medida que se vacían las páginas de la base de datos. Si el registro transaccional está habilitado (por ejemplo, JET_paramRecovery establecido en "activado", el valor predeterminado), la actualización del mapa de vaciado se realiza a medida que la aplicación cliente realiza modificaciones [en](./transaction-log-parameters.md) la base de datos. De media, todo el mapa de vaciado se escribe en el medio no volátil una vez por cada 20 % de JET_paramCheckpointDepthMax [(en](./database-cache-parameters.md) bytes) de registros transaccionales generados. El número de operaciones de escritura depende de cómo se distribuyen en toda la base de datos las modificaciones. Pero es como máximo, aproximadamente (todos los tamaños en bytes):

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

Si el registro transaccional está deshabilitado (por ejemplo, JET_paramRecovery establecido en "desactivado"), el mapa de vaciado se actualiza solo una vez cuando la base de datos se desasocia explícitamente de forma limpia [(a](./transaction-log-parameters.md) través de [JetDetachDatabase](./jetdetachdatabase-function.md)o se desasocia de forma implícita mediante la terminación de su instancia ese asociada (a través de cualquiera de las funciones [de JetTerm,](./jetterm-function.md) siempre y cuando no se [pase JET_bitTermDirty).](./jetterm2-function.md)

1 Una escritura perdida (o vaciado perdido) se define como una operación de escritura que devuelve correctamente desde el sistema operativo al motor de base de datos ese, pero los datos reales nunca se conservan en el archivo de base de datos en los medios no volátiles. Normalmente se debe a un funcionamiento incorrecto o a una pila de almacenamiento mal configurada (software o hardware). Las aplicaciones cliente pueden recibir un [error](./extensible-storage-engine-error-codes.md) JET_errReadLostFlushVerifyFailure de funciones ese que requieren la lectura de datos de la base de datos si los datos se encuentran en una región que sufre un evento de escritura perdido.

2 La capacidad de detectar escrituras perdidas dentro de la duración de un proceso ha estado presente desde Windows 8 (cliente) y Windows Server 2012 (servidor).
