---
description: SymStore (symstore.exe) es una herramienta para crear almacenes de símbolos. Se incluye en el paquete de herramientas de depuración para Windows.
ms.assetid: fe8a96e9-e780-4e96-98ef-c5128515ee6c
title: Usar SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a87b5c527717d78adb9202fd1eddd54d1f44c02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153100"
---
# <a name="using-symstore"></a>Usar SymStore

SymStore (symstore.exe) es una herramienta para crear almacenes de símbolos. Se incluye en el paquete de [herramientas de depuración para Windows](https://www.microsoft.com/?ref=go) .

SymStore almacena los símbolos en un formato que permite al depurador buscar los símbolos según la marca de tiempo y el tamaño de la imagen (para un archivo. dbg o ejecutable), o la firma y la edad (para un archivo. pdb). La ventaja del almacén de símbolos con respecto al formato tradicional de almacenamiento de símbolos es que todos los símbolos se pueden almacenar o hacer referencia a ellos en el mismo servidor y recuperarlos mediante el depurador sin ningún conocimiento previo de qué producto contiene el símbolo correspondiente.

Tenga en cuenta que no se pueden almacenar varias versiones de archivos de símbolos. pdb (por ejemplo, versiones públicas y privadas) en el mismo servidor, ya que cada una de ellas contiene la misma firma y edad.

## <a name="symstore-transactions"></a>Transacciones SymStore

Cada llamada a SymStore se registra como una transacción. Hay dos tipos de transacciones: agregar y eliminar.

Cuando se crea el almacén de símbolos, se crea un directorio denominado "000admin" en la raíz del servidor. El directorio 000admin contiene un archivo para cada transacción, así como los archivos de registro Server.txt y History.txt. El archivo Server.txt contiene una lista de todas las transacciones que están actualmente en el servidor. El archivo de History.txt contiene un historial cronológico de todas las transacciones.

Cada vez que SymStore almacena o quita archivos de símbolos, se crea un nuevo número de transacción. A continuación, se crea un archivo cuyo nombre es este número de transacción en 000admin. Este archivo contiene una lista de todos los archivos o punteros que se han agregado al almacén de símbolos durante esta transacción. Si se elimina una transacción, SymStore leerá el archivo de transacciones para determinar qué archivos y punteros debe eliminar.

Las opciones **Add** y **del** especifican si se va a realizar una operación de agregar o eliminar. La inclusión de la opción **/p** con una operación de agregar especifica que se va a agregar un puntero. Si se omite la opción **/p** , se especifica que se va a agregar el archivo de símbolos real.

También es posible crear el almacén de símbolos en dos fases independientes. En la primera fase, se usa SymStore con la opción **/x** para crear un archivo de índice. En la segunda fase, se usa SymStore con la opción **/y** para crear el almacén real de archivos o punteros a partir de la información del archivo de índice.

Esta técnica puede ser útil por diversos motivos. Por ejemplo, esto permite que el almacén de símbolos se vuelva a crear fácilmente si el almacén se pierde de algún modo, siempre y cuando el archivo de índice exista todavía. O quizás el equipo que contiene los archivos de símbolos tiene una conexión de red lenta con el equipo en el que se creará el almacén de símbolos. En este caso, puede crear el archivo de índice en el mismo equipo que los archivos de símbolos, transferir el archivo de índice al segundo equipo y, a continuación, crear el almacén en el segundo equipo.

Para obtener una lista completa de todos los parámetros de SymStore, consulte [Opciones de Command-Line de SymStore](symstore-command-line-options.md).

> [!Note]  
> SymStore no admite transacciones simultáneas de varios usuarios. Se recomienda que un usuario se designe como "administrador" del almacén de símbolos y sea responsable de todas las transacciones **Add** y **del** .

 

## <a name="transaction-examples"></a>Ejemplos de transacciones

A continuación se muestran dos ejemplos de SymStore agregar punteros de símbolo para la compilación 3790 de Windows Server 2003 a \\ \\ sampledir \\ symsrv:

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

En el ejemplo siguiente, SymStore agrega los archivos de símbolos reales para un proyecto de aplicación en las \\ \\ ubicaciones de largeapp de \\ AppServer \\ a \\ \\ testdir \\ symsrv:

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

Este es un ejemplo de cómo se usa un archivo de índice. En primer lugar, SymStore crea un archivo de índice basado en la colección de archivos de símbolos de \\ \\ largeapp de \\ AppServer \\ \\ . En este caso, el archivo de índice se coloca en un tercer equipo, \\ \\ \\ hubshare. La opción **/g** se usa para especificar que el prefijo de archivo " \\ \\ largeapp \\ AppServer" podría cambiar en el futuro:

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

Ahora Supongamos que mueve todos los archivos de símbolos fuera de la máquina \\ \\ largeapp \\ AppServer y los coloca en el \\ \\ AppServer de archivo \\ . A continuación, puede crear el propio almacén de símbolos desde el archivo de índice, \\ \\ \\ hubshare \\myindex.txt como se indica a continuación:

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

Por último, este es un ejemplo de SymStore que elimina un archivo agregado por una transacción anterior. Vea la siguiente sección para obtener una explicación de cómo determinar el identificador de la transacción (en este caso, 0000000096).

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a>Archivos comprimidos

SymStore se puede usar con archivos comprimidos de dos maneras diferentes.

1.  Use SymStore con la opción **/p** para almacenar punteros a los archivos de símbolos. Una vez finalizado SymStore, comprima los archivos a los que hacen referencia los punteros.
2.  Use SymStore con la opción **/x** para crear un archivo de índice. Una vez finalizado SymStore, comprima los archivos enumerados en el archivo de índice. A continuación, use SymStore con la opción **/y** (y, si lo desea, la opción **/p** ) para almacenar los archivos o punteros en los archivos del almacén de símbolos. (SymStore no necesita descomprimir los archivos para realizar esta operación).

El servidor de símbolos será responsable de descomprimir los archivos cuando sea necesario.

Si usa SymSrv como servidor de símbolos, se debe realizar cualquier compresión mediante la herramienta de compress.exe que se distribuye con el kit de desarrollo de software (SDK) de Microsoft Windows. Los archivos comprimidos deben tener un carácter de subrayado como último carácter en sus extensiones de archivo (por ejemplo, Module1. PD \_ o Module2. dB \_ ). Para obtener más información, consulte [uso de SymSrv](using-symsrv.md).

## <a name="the-servertxt-and-historytxt-files"></a>Archivos de server.txt y history.txt

Cuando se agrega una transacción, se agregan varios elementos de información a server.txt y history.txt para la capacidad de búsqueda futura. A continuación se muestra un ejemplo de una línea en server.txt y history.txt para una transacción de adición:

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

Se trata de una línea separada por comas. Los campos se definen como se indica a continuación.



| Campo      | Descripción                                                                         |
|------------|-------------------------------------------------------------------------------------|
| 0000000096 | Número de ID. de transacción, tal y como lo creó SymStore.                                      |
| add        | Tipo de transacción. Este campo puede ser **Add** o **del**.                   |
| ptr        | Indica si se agregaron archivos o punteros. Este campo puede ser **archivo** o **ptr**. |
| 10/09/99   | Fecha en que se produjo la transacción.                                                     |
| 00:08:32   | Hora de inicio de la transacción.                                                      |
| Windows XP | Producto.                                                                            |
| "fre" x86    | Versión (opcional).                                                                 |
| Agregado desde | Comentario (opcional)                                                                  |
| No utilizado     | (Reservado para su uso posterior).                                                           |



 

A continuación se muestran algunas líneas de ejemplo del archivo de transacción 0000000096. Cada línea registra el directorio y la ubicación del archivo o puntero que se agregó al directorio.

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

Si utiliza una transacción **del** para deshacer las transacciones **agregadas** originales, estas líneas se quitarán de server.txt y se agregará la siguiente línea a history.txt:

``` syntax
0000000105,del,0000000096
```

Los campos de la transacción de eliminación se definen como se indica a continuación.



| Campo      | Descripción                                                       |
|------------|-------------------------------------------------------------------|
| 0000000105 | Número de ID. de transacción, tal y como lo creó SymStore.                    |
| del        | Tipo de transacción. Este campo puede ser **Add** o **del**. |
| 0000000096 | Transacción que se eliminó.                                     |



 

## <a name="symbol-storage-format"></a>Formato de almacenamiento de símbolos

SymStore usa el sistema de archivos como una base de datos. Crea un árbol grande de directorios, con nombres de directorio basados en elementos como marcas de tiempo de archivo de símbolos, firmas, edad y otros datos.

Por ejemplo, después de que se hayan agregado al servidor varios archivos ACPI. dbg distintos, los directorios podrían tener el siguiente aspecto:

``` syntax
Directory of \\mybuilds\symsrv\acpi.dbg
10/06/1999  05:46p      <DIR>          .
10/06/1999  05:46p      <DIR>          ..
10/04/1999  01:54p      <DIR>          37cdb03962040
10/04/1999  01:49p      <DIR>          37cdb04027740
10/04/1999  12:56p      <DIR>          37e3eb1c62060
10/04/1999  12:51p      <DIR>          37e3ebcc27760
10/04/1999  12:45p      <DIR>          37ed151662060
10/04/1999  12:39p      <DIR>          37ed15dd27760
10/04/1999  11:33a      <DIR>          37f03ce962020
10/04/1999  11:21a      <DIR>          37f03cf7277c0
10/06/1999  05:38p      <DIR>          37fa7f00277e0
10/06/1999  05:46p      <DIR>          37fa7f01620a0
```

En este ejemplo, la ruta de acceso de búsqueda del archivo de símbolos ACPI. dbg podría tener un aspecto similar al siguiente: \\ \\ \\ symsrv \\ ACPI. dbg \\ 37cdb03962040.

Pueden existir tres archivos dentro del directorio de búsqueda:

1.  Si se almacenó el archivo, entonces ACPI. dbg existirá allí.
2.  Si se almacenó un puntero, se creará un archivo denominado File. PTR que contendrá la ruta de acceso al archivo de símbolos real.
3.  Un archivo denominado refs. PTR, que contiene una lista de todas las ubicaciones actuales de ACPI. dbg con esta marca de tiempo y el tamaño de la imagen que se han agregado actualmente al almacén de símbolos.

Al mostrar la lista de directorios de \\ \\ \\ symsrvs, \\ ACPI. dbg \\ 37cdb03962040 ofrece lo siguiente:

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

El archivo File. PTR contiene la cadena de texto " \\ \\ albuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ Sys \\ ACPI. dbg". Puesto que no hay ningún archivo llamado ACPI. dbg en este directorio, el depurador intentará encontrar el archivo en \\ \\ símbolos de \\ generación \\ x86 \\ 2128. chk \\ Symbols \\ Sys \\ ACPI. dbg.

El contenido de refs. PTR solo se usa en SymStore, no en el depurador. Este archivo contiene un registro de todas las transacciones que han tenido lugar en este directorio. Una línea de ejemplo de refs. PTR podría ser:

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

Esto muestra que se ha agregado un puntero a los \\ \\ símbolos de generación de \\ símbolos \\ x86 \\ 2128. chk \\ \\ Sys \\ ACPI. dbg con la transacción "0000000026".

Algunos archivos de símbolos permanecen constantes a través de varios productos o compilaciones o un producto determinado. Un ejemplo de esto es el archivo Msvcrt. pdb. Al hacer un directorio de \\ \\ \\ symsrv \\ msvcrt. pdb, se muestra que solo se han agregado dos versiones de msvcrt. pdb al servidor de símbolos:

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

Sin embargo, al hacer un directorio de \\ \\ \\ symsrv \\ msvcrt. pdb \\ 37a8f40e2, se muestra que refs. PTR tiene varios punteros.

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

El contenido de \\ \\ \\ symsrv \\ msvcrt. pdb \\ 37a8f40e2 \\ refs. PTR es el siguiente:

``` syntax
0000000001,ptr,\\mybuilds\symbols\x86\2137\symbols\dll\msvcrt.pdb
0000000002,ptr,\\mybuilds\symbols\x86\2137.chk\symbols\dll\msvcrt.pdb
0000000003,ptr,\\mybuilds\symbols\x86\2138\symbols\dll\msvcrt.pdb
0000000004,ptr,\\mybuilds\symbols\x86\2138.chk\symbols\dll\msvcrt.pdb
0000000005,ptr,\\mybuilds\symbols\x86\2139\symbols\dll\msvcrt.pdb
0000000006,ptr,\\mybuilds\symbols\x86\2139.chk\symbols\dll\msvcrt.pdb
0000000007,ptr,\\mybuilds\symbols\x86\2140\symbols\dll\msvcrt.pdb
0000000008,ptr,\\mybuilds\symbols\x86\2140.chk\symbols\dll\msvcrt.pdb
0000000009,ptr,\\mybuilds\symbols\x86\2136\symbols\dll\msvcrt.pdb
0000000010,ptr,\\mybuilds\symbols\x86\2136.chk\symbols\dll\msvcrt.pdb
0000000011,ptr,\\mybuilds\symbols\x86\2135\symbols\dll\msvcrt.pdb
0000000012,ptr,\\mybuilds\symbols\x86\2135.chk\symbols\dll\msvcrt.pdb
0000000013,ptr,\\mybuilds\symbols\x86\2134\symbols\dll\msvcrt.pdb
0000000014,ptr,\\mybuilds\symbols\x86\2134.chk\symbols\dll\msvcrt.pdb
0000000015,ptr,\\mybuilds\symbols\x86\2133\symbols\dll\msvcrt.pdb
0000000016,ptr,\\mybuilds\symbols\x86\2133.chk\symbols\dll\msvcrt.pdb
0000000017,ptr,\\mybuilds\symbols\x86\2132\symbols\dll\msvcrt.pdb
0000000018,ptr,\\mybuilds\symbols\x86\2132.chk\symbols\dll\msvcrt.pdb
0000000019,ptr,\\mybuilds\symbols\x86\2131\symbols\dll\msvcrt.pdb
0000000020,ptr,\\mybuilds\symbols\x86\2131.chk\symbols\dll\msvcrt.pdb
0000000021,ptr,\\mybuilds\symbols\x86\2130\symbols\dll\msvcrt.pdb
0000000022,ptr,\\mybuilds\symbols\x86\2130.chk\symbols\dll\msvcrt.pdb
0000000023,ptr,\\mybuilds\symbols\x86\2129\symbols\dll\msvcrt.pdb
0000000024,ptr,\\mybuilds\symbols\x86\2129.chk\symbols\dll\msvcrt.pdb
0000000025,ptr,\\mybuilds\symbols\x86\2128\symbols\dll\msvcrt.pdb
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\dll\msvcrt.pdb
0000000027,ptr,\\mybuilds\symbols\x86\2141\symbols\dll\msvcrt.pdb
0000000028,ptr,\\mybuilds\symbols\x86\2141.chk\symbols\dll\msvcrt.pdb
0000000029,ptr,\\mybuilds\symbols\x86\2142\symbols\dll\msvcrt.pdb
0000000030,ptr,\\mybuilds\symbols\x86\2142.chk\symbols\dll\msvcrt.pdb
```

Esto muestra que se ha usado el mismo archivo Msvcrt. pdb para varias compilaciones de símbolos almacenados en las \\ \\ \\ symsrv.

A continuación se muestra un ejemplo de un directorio que contiene una combinación de adiciones de archivos y punteros:

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

En este caso, refs. PTR tiene el siguiente contenido:

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

Por lo tanto, las transacciones 43, 44 y 45 agregaron el mismo archivo al servidor y las transacciones 46 y 47 punteros agregados. Si se eliminan las transacciones 43, 44 y 45, el archivo DbgHelp. dbg se eliminará del directorio. El directorio tendrá el siguiente contenido:

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

Ahora File. PTR contiene " \\ \\ sampledir2 \\ bin \\ \\ Retail \\ dll \\ DbgHelp. dbg" y refs. PTR contiene

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

Siempre que la última entrada en refs. PTR sea un puntero, el archivo File. PTR existirá y contendrá la ruta de acceso al archivo asociado. Siempre que la última entrada en refs. PTR sea un archivo, no existirá ningún archivo. PTR en este directorio. Por lo tanto, cualquier operación de eliminación que quite la entrada final en refs. PTR puede dar lugar a que se cree, elimine o cambie File. PTR.

 

 



