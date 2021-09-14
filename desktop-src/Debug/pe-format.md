---
description: Esta especificación describe la estructura de archivos ejecutables (imagen) y archivos objeto en la Windows de sistemas operativos. Estos archivos se conocen como archivos Portable Executable (PE) y Common Object File Format (COFF), respectivamente.
ms.assetid: 3dbfbf7f-6662-45a4-99f1-e0e24c370dee
title: Formato PE
ms.topic: article
ms.date: 03/31/2021
ms.custom: contperf-fy21q1
ms.openlocfilehash: f20431f7f56c64d5d430c9992da72ea4331cbf21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164637"
---
# <a name="pe-format"></a>Formato PE

Esta especificación describe la estructura de archivos ejecutables (imagen) y archivos objeto en la Windows de sistemas operativos. Estos archivos se conocen como archivos Portable Executable (PE) y Common Object File Format (COFF), respectivamente.

> [!Note]  
> Este documento se proporciona para ayudar en el desarrollo de herramientas y aplicaciones para Windows pero no se garantiza que sea una especificación completa en todos los aspectos. Microsoft se reserva el derecho de modificar este documento sin previo aviso.

Esta revisión de la Especificación de formato de archivo de objeto común y ejecutable portable de Microsoft reemplaza todas las revisiones anteriores de esta especificación.

## <a name="general-concepts"></a>Conceptos generales

En este documento se especifica la estructura de los archivos ejecutables (imagen) y los archivos objeto de la familia de sistemas operativos Windows Microsoft. Estos archivos se conocen como archivos Portable Executable (PE) y Common Object File Format (COFF), respectivamente. El nombre "Portable Executable" hace referencia al hecho de que el formato no es específico de la arquitectura.

En la tabla siguiente se describen algunos conceptos que aparecen a lo largo de esta especificación:

| Nombre                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| certificado de atributo <br/> | Certificado que se usa para asociar instrucciones verificables a una imagen. Se pueden asociar varias instrucciones verificables diferentes a un archivo; una de las más útiles es una instrucción de un fabricante de software que indica cuál es la síntesis del mensaje de la imagen. Una síntesis de mensaje es similar a una suma de comprobación, salvo que es muy difícil de forjar. Por lo tanto, es muy difícil modificar un archivo para que tenga la misma síntesis de mensaje que el archivo original. La instrucción se puede comprobar como realizada por el fabricante mediante esquemas de criptografía de clave pública o privada. En este documento se describen detalles sobre certificados de atributo distintos de para permitir su inserción en archivos de imagen. <br/> |
| marca de fecha y hora <br/>       | Una marca que se usa para distintos propósitos en varios lugares de un archivo PE o COFF. En la mayoría de los casos, el formato de cada marca es el mismo que el que usan las funciones de tiempo de la biblioteca en tiempo de ejecución de C. Para ver las excepciones, vea el descripton de IMAGE \_ DEBUG \_ TYPE \_ REPRO en Tipo de [depuración](#debug-type). Si el valor de la marca es 0 o 0xFFFFFFFF, no representa una marca de fecha y hora real o significativa. <br/>                                                                                                                                                                                                                                                                                                                                            |
| puntero de archivo <br/>          | Ubicación de un elemento dentro del propio archivo, antes de que lo procese el vinculador (en el caso de los archivos objeto) o el cargador (en el caso de los archivos de imagen). En otras palabras, se trata de una posición dentro del archivo tal como se almacena en el disco. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| vinculador <br/>                | Referencia al vinculador que se proporciona con Microsoft Visual Studio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| objeto de archivo <br/>           | Archivo que se da como entrada al vinculador. El vinculador genera un archivo de imagen que, a su vez, el cargador usa como entrada. El término "archivo de objeto" no implica necesariamente ninguna conexión a la programación orientada a objetos. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| reservado, debe ser 0 <br/>   | Descripción de un campo que indica que el valor del campo debe ser cero para los generadores y los consumidores deben omitir el campo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Dirección virtual relativa (RVA) <br/>                   | En un archivo de imagen, esta es la dirección de un elemento después de cargarlo en la memoria, con la dirección base del archivo de imagen restada de él. La RVA de un elemento casi siempre difiere de su posición dentro del archivo en el disco (puntero de archivo). <br/> En un archivo de objeto, una RVA es menos significativa porque no se asignan ubicaciones de memoria. En este caso, una RVA sería una dirección dentro de una sección (descrita más adelante en esta tabla), a la que posteriormente se aplica una reubicación durante la vinculación. Para simplificar, un compilador solo debe establecer la primera RVA de cada sección en cero. <br/>                                                                                                                                         |
| section <br/>               | Unidad básica de código o datos dentro de un archivo PE o COFF. Por ejemplo, todo el código de un archivo objeto se puede combinar dentro de una sola sección o (según el comportamiento del compilador) cada función puede ocupar su propia sección. Con más secciones, hay más sobrecarga de archivos, pero el vinculador puede vincular en el código de forma más selectiva. Una sección es similar a un segmento de la arquitectura Intel 8086. Todos los datos sin procesar de una sección deben cargarse de forma contigua. Además, un archivo de imagen puede contener varias secciones, como .tls o .reloc , que tienen propósitos especiales. <br/>                                                                                                                                                                      |
| Dirección virtual (VA) <br/>                    | Igual que RVA, salvo que no se resta la dirección base del archivo de imagen. La dirección se denomina VA porque Windows un espacio va distinto para cada proceso, independientemente de la memoria física. Para casi todos los propósitos, una VA debe considerarse simplemente una dirección. Una VA no es tan predecible como una RVA porque es posible que el cargador no cargue la imagen en su ubicación preferida. <br/>                                                                                                                                                                                                                                                                                                                                        |

## <a name="overview"></a>Información general

En la lista siguiente se describe el formato ejecutable de Microsoft PE, con la base del encabezado de imagen en la parte superior. La sección del encabezado EXE compatible con MS-DOS 2.0 hasta la sección sin usar justo antes del encabezado PE es la sección MS-DOS 2.0 y solo se usa para la compatibilidad con MS-DOS.

-   Encabezado EXE compatible con MS-DOS 2.0
-   unused
-   Identificador de OEM

    Información de OEM

    Desplazamiento al encabezado PE

-   Programa de código auxiliar de MS-DOS 2.0 y tabla de reubicación

-   unused

-   Encabezado PE (alineado en un límite de 8 bytes)

-   Encabezados de sección
-   Páginas de imágenes:

    importar información

    exportar información

    reubicaciones base

    información de recursos

En la lista siguiente se describe el formato de módulo de objetos COFF de Microsoft:

-   Encabezado COFF de Microsoft
-   Encabezados de sección
-   Datos sin procesar:

    código

    datos

    información de depuración

    Reubicaciones

## <a name="file-headers"></a>Encabezados de archivo

- [Código auxiliar de MS-DOS (solo imagen)](#ms-dos-stub-image-only)
- [Firma (solo imagen)](#signature-image-only)
- [Encabezado de archivo COFF (objeto e imagen)](#coff-file-header-object-and-image)
  - [Tipos de máquina](#machine-types)
  - [Características](#characteristics)
- [Encabezado opcional (solo imagen)](#optional-header-image-only)
  - [Campos estándar de encabezado opcionales (solo imagen)](#optional-header-standard-fields-image-only)
  - [Campos de Windows-Specific encabezado opcionales (solo imagen)](#optional-header-windows-specific-fields-image-only)
  - [Directorios de datos de encabezado opcionales (solo imagen)](#optional-header-data-directories-image-only)

El encabezado de archivo PE consta de un código auxiliar MS-DOS de Microsoft, la firma PE, el encabezado de archivo COFF y un encabezado opcional. Un encabezado de archivo de objeto COFF consta de un encabezado de archivo COFF y un encabezado opcional. En ambos casos, los encabezados de archivo van seguidos inmediatamente de encabezados de sección.

### <a name="ms-dos-stub-image-only"></a>Código auxiliar de MS-DOS (solo imagen)

El código auxiliar de MS-DOS es una aplicación válida que se ejecuta en MS-DOS. Se coloca en la parte delantera de la imagen EXE. El vinculador coloca aquí un código auxiliar predeterminado, que imprime el mensaje "Este programa no se puede ejecutar en modo DOS" cuando la imagen se ejecuta en MS-DOS. El usuario puede especificar un código auxiliar diferente mediante la opción del vinculador /STUB.

En la 0x3c, el código auxiliar tiene el desplazamiento del archivo con respecto a la firma pe. Esta información permite Windows ejecutar correctamente el archivo de imagen, aunque tenga un código auxiliar MS-DOS. Este desplazamiento de archivo se coloca en la ubicación 0x3c durante la vinculación.

### <a name="signature-image-only"></a>Firma (solo imagen)

Después del código auxiliar de MS-DOS, en el desplazamiento de archivo especificado en offset 0x3c, es una firma de 4 bytes que identifica el archivo como un archivo de imagen de formato PE. Esta firma es "PE \\ 0 \\ 0" (las letras "P" y "E" seguidas de dos bytes nulos).

### <a name="coff-file-header-object-and-image"></a>Encabezado de archivo COFF (objeto e imagen)

Al principio de un archivo de objeto, o inmediatamente después de la firma de un archivo de imagen, es un encabezado de archivo COFF estándar con el formato siguiente. Tenga en cuenta que Windows cargador limita el número de secciones a 96.

| Offset         | Size          | Campo                            | Descripción                                                                                                                                                                                                                                                          |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Máquina <br/>              | Número que identifica el tipo de máquina de destino. Para obtener más información, vea [Tipos de máquina.](#machine-types) <br/>                                                                                                                                        |
| 2 <br/>  | 2 <br/> | NumberOfSections <br/>     | Número de secciones. Esto indica el tamaño de la tabla de la secciones, que sigue inmediatamente a los encabezados. <br/>                                                                                                                                             |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>        | Los 32 bits inferiores del número de segundos desde las 00:00 del 1 de enero de 1970 (un valor t en tiempo de ejecución de C), que indica cuándo se creó el \_ archivo. <br/>                                                                                                             |
| 8 <br/>  | 4 <br/> | PointerToSymbolTable <br/> | Desplazamiento de archivo de la tabla de símbolos COFF o cero si no hay ninguna tabla de símbolos COFF. Este valor debe ser cero para una imagen porque la información de depuración de COFF está en desuso. <br/>                                                                           |
| 12 <br/> | 4 <br/> | NumberOfSymbols <br/>      | Número de entradas de la tabla de símbolos. Estos datos se pueden usar para buscar la tabla de cadenas, que sigue inmediatamente a la tabla de símbolos. Este valor debe ser cero para una imagen porque la información de depuración de COFF está en desuso. <br/>                        |
| 16 <br/> | 2 <br/> | SizeOfOptionalHeader <br/> | Tamaño del encabezado opcional, que es necesario para los archivos ejecutables, pero no para los archivos de objeto. Este valor debe ser cero para un archivo objeto. Para obtener una descripción del formato de encabezado, vea [Encabezado opcional (solo imagen).](#optional-header-image-only) <br/> |
| 18 <br/> | 2 <br/> | Características <br/>      | Marcas que indican los atributos del archivo. Para obtener valores de marca específicos, vea [Características](#characteristics). <br/>                                                                                                                               |

#### <a name="machine-types"></a>Tipos de máquina

El campo Máquina tiene uno de los siguientes valores, que especifican el tipo de CPU. Un archivo de imagen solo se puede ejecutar en la máquina especificada o en un sistema que emula la máquina especificada.

| Constante                                    | Value              | Descripción                                                                             |
|---------------------------------------------|--------------------|-----------------------------------------------------------------------------------------|
| MÁQUINA DE \_ ARCHIVOS \_ DE IMAGEN \_ DESCONOCIDA <br/>   | 0x0 <br/>    | Se supone que el contenido de este campo es aplicable a cualquier tipo de máquina. <br/> |
| IMAGE \_ FILE \_ MACHINE \_ AM33 <br/>      | 0x1d3 <br/>  | Glushita AM33 <br/>                                                             |
| MÁQUINA \_ DE ARCHIVOS DE IMAGEN \_ \_ AMD64 <br/>     | 0x8664 <br/> | x64 <br/>                                                                         |
| IMAGE \_ FILE \_ MACHINE \_ ARM <br/>       | 0x1c0 <br/>  | Arm little endian <br/>                                                           |
| IMAGE \_ FILE \_ MACHINE \_ ARM64 <br/>     | 0xaa64 <br/> | Arm64 little endian <br/>                                                         |
| IMAGE \_ FILE \_ MACHINE \_ ARMNT <br/>     | 0x1c4 <br/>  | Arm Thumb-2 little endian <br/>                                                   |
| EBC \_ DE LA MÁQUINA DE ARCHIVOS DE \_ \_ IMAGEN <br/>       | 0xebc <br/>  | Código de bytes EFI <br/>                                                               |
| IMAGE \_ FILE \_ MACHINE \_ I386 <br/>      | 0x14c <br/>  | Procesadores Intel 386 o posteriores y procesadores compatibles <br/>                     |
| IMAGE \_ FILE \_ MACHINE \_ IA64 <br/>      | 0x200 <br/>  | Familia de procesadores Intel Itanium <br/>                                              |
| IMAGE \_ FILE \_ MACHINE \_ M32R <br/>      | 0x9041 <br/> | M32R little endian <br/>                                               |
| MÁQUINA \_ DE ARCHIVOS DE IMAGEN \_ \_ MIPS16 <br/>    | 0x266 <br/>  | MIPS16 <br/>                                                                      |
| MÁQUINA \_ DE ARCHIVOS DE IMAGEN \_ \_ MIPSFPU <br/>   | 0x366 <br/>  | MIPS con FPU <br/>                                                               |
| MÁQUINA \_ DE ARCHIVOS DE IMAGEN \_ \_ MIPSFPU16 <br/> | 0x466 <br/>  | MIPS16 con FPU <br/>                                                             |
| IMAGE \_ FILE \_ MACHINE \_ POWERPC <br/>   | 0x1f0 <br/>  | Power PC little endian <br/>                                                      |
| IMAGE \_ FILE \_ MACHINE \_ POWERPCFP <br/> | 0x1f1 <br/>  | Power PC con compatibilidad con punto flotante <br/>                                        |
| IMAGE \_ FILE \_ MACHINE \_ R4000 <br/>     | 0x166 <br/>  | MiPS little endian <br/>                                                          |
| IMAGE \_ FILE \_ MACHINE \_ RISCV32 <br/>   | 0x5032 <br/> | Espacio de direcciones RISC-V de 32 bits <br/>                                                 |
| IMAGE \_ FILE \_ MACHINE \_ RISCV64 <br/>   | 0x5064 <br/> | Espacio de direcciones RISC-V de 64 bits <br/>                                                 |
| IMAGE \_ FILE \_ MACHINE \_ RISCV128 <br/>  | 0x5128 <br/> | Espacio de direcciones RISC-V de 128 bits <br/>                                                |
| IMAGE \_ FILE \_ MACHINE \_ SH3 <br/>       | 0x1a2 <br/>  | Sh3 de Sh3 <br/>                                                                 |
| MÁQUINA \_ DE ARCHIVOS DE IMAGEN \_ \_ SH3DSP <br/>    | 0x1a3 <br/>  | Dsp Sh3 de Sh3 <br/>                                                             |
| IMAGE \_ FILE \_ MACHINE \_ SH4 <br/>       | 0x1a6 <br/>  | Sh4 de Sh4 <br/>                                                                 |
| IMAGE \_ FILE \_ MACHINE \_ SH5 <br/>       | 0x1a8 <br/>  | Sh5 de Sh5 <br/>                                                                 |
| POSICIÓN DE \_ LA MÁQUINA DEL ARCHIVO DE \_ \_ IMAGEN <br/>     | 0x1c2 <br/>  | Thumb <br/>                                                                       |
| MÁQUINA \_ DE ARCHIVOS DE IMAGEN \_ \_ WCEMIPSV2 <br/> | 0x169 <br/>  | MIPS little-endian WCE v2 <br/>                                                   |

#### <a name="characteristics"></a>Características

El campo Características contiene marcas que indican los atributos del objeto o archivo de imagen. Las marcas siguientes están definidas actualmente:

| Marca                                                 | Value              | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REUBICACIONES \_ DE ARCHIVOS DE IMAGEN \_ \_ QUITADAS <br/>            | 0x0001 <br/> | Solo imagen, Windows CE y Microsoft Windows NT y versiones posteriores. Esto indica que el archivo no contiene reubicaciones base y, por tanto, debe cargarse en su dirección base preferida. Si la dirección base no está disponible, el cargador notifica un error. El comportamiento predeterminado del vinculador es quitar reubicaciones base de archivos ejecutables (EXE). <br/> |
| IMAGEN EJECUTABLE \_ DE \_ ARCHIVO DE \_ IMAGEN <br/>           | 0x0002 <br/> | Solo imagen. Esto indica que el archivo de imagen es válido y se puede ejecutar. Si no se establece esta marca, indica un error del vinculador. <br/>                                                                                                                                                                                                                          |
| NÚMERO \_ DE LÍNEA DE ARCHIVO DE IMAGEN \_ \_ \_ QUITADO <br/>        | 0x0004 <br/> | Se han quitado los números de línea de COFF. Esta marca está en desuso y debe ser cero. <br/>                                                                                                                                                                                                                                                                       |
| IMAGEN \_ FILE \_ LOCAL \_ SYMS STRIPPED (SYMS LOCALES \_ DEL ARCHIVO DE IMAGEN QUITADOS) <br/>       | 0x0008 <br/> | Se han quitado las entradas de la tabla de símbolos COFF para los símbolos locales. Esta marca está en desuso y debe ser cero. <br/>                                                                                                                                                                                                                                             |
| IMAGEN \_ FILE \_ AGGRESSIVE \_ WS \_ TRIM <br/>        | 0x0010 <br/> | Obsoleto. Recorte agresivo del conjunto de trabajo. Esta marca está en desuso Windows 2000 y versiones posteriores y debe ser cero. <br/>                                                                                                                                                                                                                                          |
| IMAGE \_ FILE \_ LARGE \_ ADDRESS \_ AWARE <br/>      | 0x0020 <br/> | La aplicación puede controlar > direcciones de 2 GB. <br/>                                                                                                                                                                                                                                                                                                            |
|                                                      | 0x0040 <br/> | Esta marca está reservada para su uso futuro. <br/>                                                                                                                                                                                                                                                                                                                  |
| LO \_ INVERTIDO DE BYTES DE ARCHIVO DE \_ \_ \_ IMAGEN <br/>         | 0x0080 <br/> | Little endian: el bit menos significativo (LSB) precede al bit más significativo (MSB) en memoria. Esta marca está en desuso y debe ser cero. <br/>                                                                                                                                                                                                          |
| MÁQUINA \_ DE \_ 32 BITS DE ARCHIVO DE \_ IMAGEN <br/>              | 0x0100 <br/> | La máquina se basa en una arquitectura de 32 bits. <br/>                                                                                                                                                                                                                                                                                                        |
| DEPURACIÓN \_ DE ARCHIVO DE IMAGEN \_ \_ QUITADA <br/>             | 0x0200 <br/> | La información de depuración se quita del archivo de imagen. <br/>                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ FILE \_ REMOVABLE \_ RUN \_ FROM \_ SWAP <br/> | 0x0400 <br/> | Si la imagen está en medios extraíbles, cárquela completamente y cópiela en el archivo de intercambio. <br/>                                                                                                                                                                                                                                                                        |
| IMAGE \_ FILE \_ NET \_ RUN \_ FROM \_ SWAP <br/>        | 0x0800 <br/> | Si la imagen está en medios de red, cárquela completamente y cópiela en el archivo de intercambio. <br/>                                                                                                                                                                                                                                                                          |
| SISTEMA \_ DE ARCHIVOS DE \_ IMAGEN <br/>                      | 0x1000 <br/> | El archivo de imagen es un archivo del sistema, no un programa de usuario. <br/>                                                                                                                                                                                                                                                                                                   |
| ARCHIVO \_ DE IMAGEN \_ DLL <br/>                         | 0x2000 <br/> | El archivo de imagen es una biblioteca de vínculos dinámicos (DLL). Estos archivos se consideran archivos ejecutables para casi todos los propósitos, aunque no se pueden ejecutar directamente. <br/>                                                                                                                                                                                              |
| SOLO \_ EL SISTEMA DE ARCHIVOS DE \_ \_ \_ IMAGEN <br/>            | 0x4000 <br/> | El archivo solo debe ejecutarse en un equipo de un solo procesador. <br/>                                                                                                                                                                                                                                                                                                 |
| BYTES \_ DE ARCHIVO DE IMAGEN HI \_ \_ \_ INVERTIDOS <br/>         | 0x8000 <br/> | Big endian: el MSB precede al LSB en memoria. Esta marca está en desuso y debe ser cero. <br/>                                                                                                                                                                                                                                                            |

### <a name="optional-header-image-only"></a>Encabezado opcional (solo imagen)

Cada archivo de imagen tiene un encabezado opcional que proporciona información al cargador. Este encabezado es opcional en el sentido de que algunos archivos (en concreto, los archivos de objeto) no lo tienen. Para los archivos de imagen, este encabezado es obligatorio. Un archivo de objeto puede tener un encabezado opcional, pero, por lo general, este encabezado no tiene ninguna función en un archivo de objeto, excepto para aumentar su tamaño.

Tenga en cuenta que el tamaño del encabezado opcional no es fijo. El **campo SizeOfOptionalHeader** del encabezado COFF debe usarse para validar que un sondeo en el archivo de un directorio de datos determinado no va más allá **de SizeOfOptionalHeader.** Para obtener más información, vea [Encabezado de archivo COFF (objeto e imagen).](#coff-file-header-object-and-image)

El **campo NumberOfRvaAndSizes** del encabezado opcional también debe usarse para asegurarse de que ningún sondeo para una entrada de directorio de datos determinada va más allá del encabezado opcional. Además, es importante validar el número mágico de encabezado opcional para la compatibilidad de formato.

El número mágico de encabezado opcional determina si una imagen es un ejecutable PE32 o PE32+.

| Número mágico      | Formato PE         |
|-------------------|-------------------|
| 0x10b <br/> | PE32 <br/>  |
| 0x20b <br/> | PE32+ <br/> |

Las imágenes PE32+ permiten un espacio de direcciones de 64 bits mientras se limita el tamaño de la imagen a 2 gigabytes. Otras modificaciones de PE32+ se abordan en sus respectivas secciones.

El propio encabezado opcional tiene tres partes principales.

| Desplazamiento (PE32/PE32+) | Tamaño (PE32/PE32+)    | Elemento de encabezado                         | Descripción                                                                                                                                                                   |
|---------------------|----------------------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 28/24 <br/>    | Campos estándar <br/>         | Campos definidos para todas las implementaciones de COFF, incluidos UNIX. <br/>                                                                                          |
| 28/24 <br/>   | 68/88 <br/>    | Windows campos específicos de la aplicación <br/> | Campos adicionales para admitir características específicas de Windows (por ejemplo, subsistemas). <br/>                                                                              |
| 96/112 <br/>  | Variable <br/> | Directorios de datos <br/>        | Pares de dirección y tamaño para tablas especiales que se encuentran en el archivo de imagen y que el sistema operativo usa (por ejemplo, la tabla de importación y la tabla de exportación). <br/> |

#### <a name="optional-header-standard-fields-image-only"></a>Campos estándar de encabezado opcionales (solo imagen)

Los ocho primeros campos del encabezado opcional son campos estándar que se definen para cada implementación de COFF. Estos campos contienen información general que resulta útil para cargar y ejecutar un archivo ejecutable. No se modifican para el formato PE32+.

| Offset         | Size          | Campo                               | Descripción                                                                                                                                                                                                                                                                                                                                   |
|----------------|---------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Instrucción mágica <br/>                   | Entero sin signo que identifica el estado del archivo de imagen. El número más común es 0x10B, que lo identifica como un archivo ejecutable normal. 0x107 lo identifica como una imagen de ROM y 0x20B la identifica como un ejecutable PE32+. <br/>                                                                                            |
| 2 <br/>  | 1 <br/> | MajorLinkerVersion <br/>      | El número de versión principal del enlazador. <br/>                                                                                                                                                                                                                                                                                                  |
| 3 <br/>  | 1 <br/> | MinorLinkerVersion <br/>      | El número de versión secundaria del enlazador. <br/>                                                                                                                                                                                                                                                                                                  |
| 4 <br/>  | 4 <br/> | SizeOfCode <br/>              | El tamaño de la sección de código (texto) o la suma de todas las secciones de código si hay varias secciones. <br/>                                                                                                                                                                                                                              |
| 8 <br/>  | 4 <br/> | SizeOfInitializedData <br/>   | El tamaño de la sección de datos inicializados o la suma de todas estas secciones si hay varias secciones de datos. <br/>                                                                                                                                                                                                                    |
| 12 <br/> | 4 <br/> | SizeOfUninitializedData <br/> | El tamaño de la sección de datos no inicializados (BSS) o la suma de todas estas secciones si hay varias secciones de BSS. <br/>                                                                                                                                                                                                             |
| 16 <br/> | 4 <br/> | AddressOfEntryPoint <br/>     | Dirección del punto de entrada con respecto a la base de imagen cuando el archivo ejecutable se carga en la memoria. En el caso de las imágenes de programa, esta es la dirección inicial. Para los controladores de dispositivo, esta es la dirección de la función de inicialización. Un punto de entrada es opcional para los archivos DLL. Cuando no hay ningún punto de entrada, este campo debe ser cero. <br/> |
| 20 <br/> | 4 <br/> | BaseOfCode <br/>              | Dirección relativa a la base de la imagen de la sección de principio de código cuando se carga en la memoria. <br/>                                                                                                                                                                                                                    |

PE32 contiene este campo adicional, que no está presente en PE32+, después de BaseOfCode.

| Offset         | Size          | Campo                  | Descripción                                                                                                                |
|----------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------|
| 24 <br/> | 4 <br/> | BaseOfData <br/> | Dirección relativa a la base de imagen de la sección de inicio de datos cuando se carga en la memoria. <br/> |

#### <a name="optional-header-windows-specific-fields-image-only"></a>Campos de Windows-Specific encabezado opcionales (solo imagen)

Los 21 campos siguientes son una extensión del formato de encabezado opcional COFF. Contienen información adicional requerida por el vinculador y el cargador en Windows.

| Desplazamiento (PE32/PE32+) | Tamaño (PE32/PE32+) | Campo                                   | Descripción                                                                                                                                                                                                                                                                                                            |
|----------------------|--------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 28/24 <br/>    | 4/8 <br/>    | ImageBase <br/>                   | La dirección preferida del primer byte de la imagen cuando se carga en la memoria; debe ser un múltiplo de 64 K. El valor predeterminado de los archivos DLL es 0x10000000. El valor predeterminado para Windows CE es 0x00010000. El valor predeterminado para Windows NT, Windows 2000, Windows XP, Windows 95, Windows 98 y Windows Me es 0x00400000. <br/>       |
| 32/32 <br/>    | 4 <br/>      | SectionAlignment <br/>            | La alineación (en bytes) de las secciones cuando se cargan en la memoria. Debe ser mayor o igual que FileAlignment. El valor predeterminado es el tamaño de página de la arquitectura. <br/>                                                                                                                               |
| 36/36 <br/>    | 4 <br/>      | FileAlignment <br/>               | El factor de alineación (en bytes) que se usa para alinear los datos sin procesar de las secciones del archivo de imagen. El valor debe ser una potencia de 2 entre 512 y 64 K, ambos incluidos. El valor predeterminado es 512. Si SectionAlignment es menor que el tamaño de página de la arquitectura, FileAlignment debe coincidir con SectionAlignment. <br/> |
| 40/40 <br/>    | 2 <br/>      | MajorOperatingSystemVersion <br/> | El número de versión principal del sistema operativo obligatorio. <br/>                                                                                                                                                                                                                                                 |
| 42/42 <br/>    | 2 <br/>      | MinorOperatingSystemVersion <br/> | El número de versión secundaria del sistema operativo obligatorio. <br/>                                                                                                                                                                                                                                                 |
| 44/44 <br/>    | 2 <br/>      | MajorImageVersion <br/>           | El número de versión principal de la imagen. <br/>                                                                                                                                                                                                                                                                     |
| 46/46 <br/>    | 2 <br/>      | MinorImageVersion <br/>           | El número de versión secundaria de la imagen. <br/>                                                                                                                                                                                                                                                                     |
| 48/48 <br/>    | 2 <br/>      | MajorSubsystemVersion <br/>       | El número de versión principal del subsistema. <br/>                                                                                                                                                                                                                                                                 |
| 50/50 <br/>    | 2 <br/>      | MinorSubsystemVersion <br/>       | El número de versión secundaria del subsistema. <br/>                                                                                                                                                                                                                                                                 |
| 52/52 <br/>    | 4 <br/>      | Win32VersionValue <br/>           | Reservado, debe ser cero. <br/>                                                                                                                                                                                                                                                                                    |
| 56/56 <br/>    | 4 <br/>      | SizeOfImage <br/>                 | Tamaño (en bytes) de la imagen, incluidos todos los encabezados, a medida que la imagen se carga en memoria. Debe ser un múltiplo de SectionAlignment. <br/>                                                                                                                                                                      |
| 60/60 <br/>    | 4 <br/>      | SizeOfHeaders <br/>               | Tamaño combinado de un código auxiliar MS-DOS, encabezado PE y encabezados de sección redondeados a un múltiplo de FileAlignment. <br/>                                                                                                                                                                                             |
| 64/64 <br/>    | 4 <br/>      | Checksum <br/>                    | Suma de comprobación del archivo de imagen. El algoritmo para calcular la suma de comprobación se incorpora a IMAGHELP.DLL. A continuación se comprueba la validación en tiempo de carga: todos los controladores, cualquier archivo DLL cargado en tiempo de arranque y cualquier archivo DLL que se cargue en un proceso Windows crítico. <br/>                                          |
| 68/68 <br/>    | 2 <br/>      | Subsystem <br/>                   | El subsistema necesario para ejecutar esta imagen. Para obtener más información, [vea Windows Subsystem](#windows-subsystem). <br/>                                                                                                                                                                                       |
| 70/70 <br/>    | 2 <br/>      | DllCharacteristics <br/>          | Para obtener más información, vea [Características de DLL más](#dll-characteristics) adelante en esta especificación. <br/>                                                                                                                                                                                                         |
| 72/72 <br/>    | 4/8 <br/>    | SizeOfStackReserve <br/>          | El tamaño de la pila que se va a reservar. Solo se confirma SizeOfStackCommit; el resto está disponible una página a la vez hasta que se alcanza el tamaño de reserva. <br/>                                                                                                                                                    |
| 76/80 <br/>    | 4/8 <br/>    | SizeOfStackCommit <br/>           | El tamaño de la pila que se va a confirmar. <br/>                                                                                                                                                                                                                                                                           |
| 80/88 <br/>    | 4/8 <br/>    | SizeOfHeapReserve <br/>           | El tamaño del espacio de montón local que se va a reservar. Solo se confirma SizeOfHeapCommit; el resto está disponible una página a la vez hasta que se alcanza el tamaño de reserva. <br/>                                                                                                                                          |
| 84/96 <br/>    | 4/8 <br/>    | SizeOfHeapCommit <br/>            | El tamaño del espacio de montón local que se va a confirmar. <br/>                                                                                                                                                                                                                                                                |
| 88/104 <br/>   | 4 <br/>      | LoaderFlags <br/>                 | Reservado, debe ser cero. <br/>                                                                                                                                                                                                                                                                                    |
| 92/108 <br/>   | 4 <br/>      | NumberOfRvaAndSizes <br/>         | Número de entradas de directorio de datos en el resto del encabezado opcional. Cada una describe una ubicación y un tamaño. <br/>                                                                                                                                                                                          |

##### <a name="windows-subsystem"></a>Windows Subsistema

Los siguientes valores definidos para el campo Subsistema del encabezado opcional determinan Windows subsistema (si existe) es necesario para ejecutar la imagen.

| Constante                                                  | Value          | Descripción                                                      |
|-----------------------------------------------------------|----------------|------------------------------------------------------------------|
| SUBSISTEMA DE \_ IMAGEN \_ DESCONOCIDO <br/>                     | 0 <br/>  | Un subsistema desconocido <br/>                                 |
| SUBSISTEMA \_ DE \_ IMÁGENES NATIVO <br/>                      | 1 <br/>  | Controladores de dispositivos y procesos Windows nativos <br/>          |
| INTERFAZ GRÁFICA DE \_ USUARIO DE WINDOWS DEL SUBSISTEMA DE \_ \_ IMÁGENES <br/>                | 2 <br/>  | Subsistema Windows interfaz gráfica de usuario (GUI) <br/> |
| IMAGE \_ SUBSYSTEM \_ WINDOWS \_ CUI <br/>                | 3 <br/>  | Subsistema de Windows de caracteres <br/>                      |
| IMAGE \_ SUBSYSTEM \_ OS2 \_ CUI <br/>                    | 5 <br/>  | Subsistema de caracteres OS/2 <br/>                         |
| IMAGE \_ SUBSYSTEM \_ POSIX \_ CUI <br/>                  | 7 <br/>  | Subsistema de caracteres Posix <br/>                        |
| VENTANAS \_ NATIVAS \_ DEL SUBSISTEMA DE \_ IMÁGENES <br/>             | 8 <br/>  | Controlador Win9x nativo <br/>                                  |
| INTERFAZ GRÁFICA DE \_ USUARIO DE WINDOWS CE DEL SUBSISTEMA DE \_ \_ \_ IMÁGENES <br/>            | 9 <br/>  | Windows CE <br/>                                           |
| APLICACIÓN \_ \_ EFI DEL SUBSISTEMA \_ DE IMÁGENES <br/>            | 10 <br/> | Una aplicación Extensible Firmware Interface (EFI) <br/>   |
| CONTROLADOR DEL \_ SERVICIO \_ DE ARRANQUE EFI DEL SUBSISTEMA \_ \_ DE \_ IMÁGENES <br/> | 11 <br/> | Un controlador EFI con servicios de arranque <br/>                     |
| CONTROLADOR EN \_ TIEMPO DE \_ EJECUCIÓN EFI DEL SUBSISTEMA DE \_ \_ IMÁGENES <br/>       | 12 <br/> | Un controlador EFI con servicios en tiempo de ejecución <br/>                 |
| IMAGE \_ SUBSYSTEM \_ EFI \_ ROM <br/>                    | 13 <br/> | Una imagen de EFI ROM <br/>                                     |
| XBOX \_ DEL SUBSISTEMA DE \_ IMÁGENES <br/>                        | 14 <br/> | XBOX <br/>                                                 |
| APLICACIÓN DE \_ ARRANQUE DE WINDOWS DEL SUBSISTEMA DE \_ \_ \_ IMÁGENES <br/>  | 16 <br/> | Windows aplicación de arranque. <br/>                            |

##### <a name="dll-characteristics"></a>Características de DLL

Los valores siguientes se definen para el campo DllCharacteristics del encabezado opcional.

| Constante                                                             | Value              | Descripción                                                                                             |
|----------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------|
|                                                                      | 0x0001 <br/> | Reservado, debe ser cero. <br/>                                                                     |
|                                                                      | 0x0002 <br/> | Reservado, debe ser cero. <br/>                                                                     |
|                                                                      | 0x0004 <br/> | Reservado, debe ser cero. <br/>                                                                     |
|                                                                      | 0x0008 <br/> | Reservado, debe ser cero. <br/>                                                                     |
| IMAGE \_ DLLCHARACTERISTICS \_ HIGH \_ ENTROPY \_ VA <br/>             | 0x0020 <br/> | La imagen puede controlar un espacio de direcciones virtuales de 64 bits de entropía alta. <br/>                               |
| IMAGE \_ DLLCHARACTERISTICS\_ <br/> BASE \_ DINÁMICA <br/>    | 0x0040 <br/> | El archivo DLL se puede reubicar en tiempo de carga. <br/>                                                          |
| IMAGE \_ DLLCHARACTERISTICS\_ <br/> FORZAR \_ INTEGRIDAD <br/> | 0x0080 <br/> | Se aplican comprobaciones de integridad del código. <br/>                                                         |
| IMAGE \_ DLLCHARACTERISTICS\_ <br/> NX \_ COMPAT <br/>       | 0x0100 <br/> | La imagen es compatible con NX. <br/>                                                                     |
| IMAGE \_ DLLCHARACTERISTICS \_ NO \_ ISOLATION <br/>                | 0x0200 <br/> | Es consciente del aislamiento, pero no aísla la imagen. <br/>                                              |
| IMAGE \_ DLLCHARACTERISTICS \_ NO \_ SEH <br/>                      | 0x0400 <br/> | No usa el control de excepciones estructuradas (SE). No SE se puede llamar al controlador en esta imagen. <br/> |
| IMAGE \_ DLLCHARACTERISTICS \_ SIN \_ ENLACE <br/>                     | 0x0800 <br/> | No enlace la imagen. <br/>                                                                      |
| IMAGE \_ DLLCHARACTERISTICS \_ APPCONTAINER <br/>                  | 0x1000 <br/> | La imagen debe ejecutarse en un AppContainer. <br/>                                                      |
| CONTROLADOR \_ \_ WDM IMAGE DLLCHARACTERISTICS \_ <br/>                  | 0x2000 <br/> | Un controlador WDM. <br/>                                                                               |
| IMAGE \_ DLLCHARACTERISTICS \_ GUARD \_ CF <br/>                     | 0x4000 <br/> | Image admite Control Flow Guard. <br/>                                                          |
| IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL \_ SERVER \_ AWARE <br/>      | 0x8000 <br/> | Es consciente de Terminal Server. <br/>                                                                      |

#### <a name="optional-header-data-directories-image-only"></a>Directorios de datos de encabezado opcionales (solo imagen)

Cada directorio de datos proporciona la dirección y el tamaño de una tabla o cadena que Windows utiliza. Todas estas entradas del directorio de datos se cargan en la memoria para que el sistema pueda usarlas en tiempo de ejecución. Un directorio de datos es un campo de 8 bytes que tiene la siguiente declaración:

```cpp
typedef struct _IMAGE_DATA_DIRECTORY {
    DWORD   VirtualAddress;
    DWORD   Size;
} IMAGE_DATA_DIRECTORY, *PIMAGE_DATA_DIRECTORY;
```

El primer campo, VirtualAddress, es realmente el RVA de la tabla. El RVA es la dirección de la tabla en relación con la dirección base de la imagen cuando se carga la tabla. El segundo campo proporciona el tamaño en bytes. Los directorios de datos, que forman la última parte del encabezado opcional, se enumeran en la tabla siguiente.

Tenga en cuenta que el número de directorios no es fijo. Antes de buscar un directorio específico, compruebe el campo NumberOfRvaAndSizes en el encabezado opcional.

Además, no suponga que los ADA de esta tabla apuntan al principio de una sección o que las secciones que contienen tablas específicas tienen nombres específicos.

| Desplazamiento (PE/PE32+)   | Size          | Campo                               | Descripción                                                                                                                                                                          |
|---------------------|---------------|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 96/112 <br/>  | 8 <br/> | Exportar tabla <br/>            | Dirección y tamaño de la tabla de exportación. Para obtener más información, [vea .edata Section (Image Only) (Sección .edata [solo imagen]).](#the-edata-section-image-only) <br/>                                                |
| 104/120 <br/> | 8 <br/> | Importar tabla <br/>            | La dirección y el tamaño de la tabla de importación. Para obtener más información, [vea la sección .idata](#the-idata-section).<br/>                                                                    |
| 112/128 <br/> | 8 <br/> | Tabla de recursos <br/>          | La dirección y el tamaño de la tabla de recursos. Para obtener más información, [vea la sección .rsrc](#the-rsrc-section).<br/>                                                                    |
| 120/136 <br/> | 8 <br/> | Tabla de excepciones <br/>         | Dirección y tamaño de la tabla de excepciones. Para obtener más información, [vea la sección .pdata](#the-pdata-section). <br/>                                                                |
| 128/144 <br/> | 8 <br/> | Tabla de certificados <br/>       | La dirección y el tamaño de la tabla de certificados de atributo. Para obtener más información, [vea La tabla de certificados de atributos (solo imagen).](#the-attribute-certificate-table-image-only) <br/> |
| 136/152 <br/> | 8 <br/> | Tabla de reubicación base <br/>   | La dirección y el tamaño de la tabla de reubicación base. Para obtener más información, [vea La sección .reloc (solo imagen).](#the-reloc-section-image-only)<br/>                                   |
| 144/160 <br/> | 8 <br/> | Depuración <br/>                   | La dirección inicial y el tamaño de los datos de depuración. Para obtener más información, [vea la sección .debug](#the-debug-section).<br/>                                                             |
| 152/168 <br/> | 8 <br/> | Architecture <br/>            | Reservado, debe ser 0 <br/>                                                                                                                                                      |
| 160/176 <br/> | 8 <br/> | Global Ptr <br/>              | RVA del valor que se va a almacenar en el registro de puntero global. El miembro de tamaño de esta estructura debe establecerse en cero. <br/>                                                 |
| 168/184 <br/> | 8 <br/> | Tabla TLS <br/>               | La dirección y el tamaño de la tabla de almacenamiento local de subprocesos (TLS). Para obtener más información, [vea la sección .tls](#the-tls-section).<br/>                                                        |
| 176/192 <br/> | 8 <br/> | Cargar tabla de configuración <br/>       | La dirección y el tamaño de la tabla de configuración de carga. Para obtener más información, [vea La estructura de configuración de carga (solo imagen).](#the-load-configuration-structure-image-only)<br/>       |
| 184/200 <br/> | 8 <br/> | Importación enlazada <br/>            | La dirección y el tamaño de la tabla de importación enlazada. <br/>                                                                                                                                 |
| 192/208 <br/> | 8 <br/> | IAT <br/>                     | La dirección y el tamaño de la tabla de direcciones de importación. Para obtener más información, vea [Importar tabla de direcciones](#import-address-table).<br/>                                                 |
| 200/216 <br/> | 8 <br/> | Descriptor de importación de retraso <br/> | La dirección y el tamaño del descriptor de importación de retraso. Para obtener más información, vea [Tablas de importación de carga retrasada (solo imagen).](#delay-load-import-tables-image-only)<br/>                    |
| 208/224 <br/> | 8 <br/> | Encabezado en tiempo de ejecución clr <br/>      | La dirección y el tamaño del encabezado en tiempo de ejecución de CLR. Para obtener más información, [vea la sección .cormeta (solo objeto).](#the-cormeta-section-object-only)<br/>                                |
| 216/232 <br/> | 8 <br/> | Reservado, debe ser cero <br/>  |                                                                                                                                                                                      |

La entrada Tabla de certificados apunta a una tabla de certificados de atributo. Estos certificados no se cargan en la memoria como parte de la imagen. Por lo tanto, el primer campo de esta entrada, que normalmente es un RVA, es un puntero de archivo en su lugar.

## <a name="section-table-section-headers"></a>Tabla de secciones (encabezados de sección)

- [Marcas de sección](#section-flags)
- [Secciones agrupadas (solo objeto)](#grouped-sections-object-only)

Cada fila de la tabla de secciones es, en efecto, un encabezado de sección. Esta tabla sigue inmediatamente al encabezado opcional, si lo hay. Este posicionamiento es necesario porque el encabezado de archivo no contiene un puntero directo a la tabla de secciones. En su lugar, la ubicación de la tabla de secciones se determina calculando la ubicación del primer byte después de los encabezados. Asegúrese de usar el tamaño del encabezado opcional tal como se especifica en el encabezado de archivo.

El número de entradas de la tabla de secciones lo proporciona el campo NumberOfSections del encabezado de archivo. Las entradas de la tabla de secciones se numeran a partir de una (1). Las entradas de la sección de memoria de datos y código están en el orden elegido por el vinculador.

En un archivo de imagen, el vinculador debe asignar las VA de las secciones para que estén en orden ascendente y adyacentes, y deben ser un múltiplo del valor SectionAlignment en el encabezado opcional.

Cada encabezado de sección (entrada de tabla de sección) tiene el formato siguiente, para un total de 40 bytes por entrada.



| Offset         | Size          | Campo                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Nombre <br/>                 | Cadena codificada UTF-8 de 8 bytes y con un valor NULL. Si la cadena tiene exactamente 8 caracteres, no hay ningún valor NULL de terminación. Para los nombres más largos, este campo contiene una barra diagonal (/) seguida de una representación ASCII de un número decimal que es un desplazamiento en la tabla de cadenas. Las imágenes ejecutables no usan una tabla de cadenas y no admiten nombres de sección de más de 8 caracteres. Los nombres largos de los archivos de objeto se truncan si se emiten en un archivo ejecutable. <br/>                                         |
| 8 <br/>  | 4 <br/> | VirtualSize <br/>          | Tamaño total de la sección cuando se carga en memoria. Si este valor es mayor que SizeOfRawData, la sección se agrega de cero. Este campo solo es válido para las imágenes ejecutables y debe establecerse en cero para los archivos de objeto. <br/>                                                                                                                                                                                                                                                                                           |
| 12 <br/> | 4 <br/> | VirtualAddress <br/>       | En el caso de las imágenes ejecutables, la dirección del primer byte de la sección con respecto a la base de la imagen cuando la sección se carga en la memoria. Para los archivos de objeto, este campo es la dirección del primer byte antes de aplicar la reubicación; Por motivos de simplicidad, los compiladores deben establecer esto en cero. De lo contrario, es un valor arbitrario que se resta de los desplazamientos durante la reubicación. <br/>                                                                                                                                         |
| 16 <br/> | 4 <br/> | SizeOfRawData <br/>        | El tamaño de la sección (para los archivos de objeto) o el tamaño de los datos inicializados en el disco (para los archivos de imagen). Para las imágenes ejecutables, debe ser un múltiplo de FileAlignment del encabezado opcional. Si es menor que VirtualSize, el resto de la sección se rellena con cero. Dado que el campo SizeOfRawData está redondeado pero el campo VirtualSize no, también es posible que SizeOfRawData sea mayor que VirtualSize. Cuando una sección contiene solo datos sin inicializar, este campo debe ser cero. <br/> |
| 20 <br/> | 4 <br/> | PointerToRawData <br/>     | Puntero de archivo a la primera página de la sección dentro del archivo COFF. Para las imágenes ejecutables, debe ser un múltiplo de FileAlignment del encabezado opcional. Para los archivos de objeto, el valor debe alinearse en un límite de 4 bytes para obtener el mejor rendimiento. Cuando una sección contiene solo datos sin inicializar, este campo debe ser cero. <br/>                                                                                                                                                                               |
| 24 <br/> | 4 <br/> | PointerToRelocations <br/> | Puntero de archivo al principio de las entradas de reubicación de la sección. Se establece en cero para las imágenes ejecutables o si no hay reubicaciones. <br/>                                                                                                                                                                                                                                                                                                                                                                   |
| 28 <br/> | 4 <br/> | PointerToLinenumbers <br/> | Puntero de archivo al principio de las entradas de número de línea de la sección. Se establece en cero si no hay números de línea COFF. Este valor debe ser cero para una imagen porque la información de depuración de COFF está en desuso. <br/>                                                                                                                                                                                                                                                                                            |
| 32 <br/> | 2 <br/> | NumberOfRelocations <br/>  | Número de entradas de reubicación de la sección. Se establece en cero para las imágenes ejecutables. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 34 <br/> | 2 <br/> | NumberOfLinenumbers <br/>  | Número de entradas de número de línea de la sección. Este valor debe ser cero para una imagen porque la información de depuración de COFF está en desuso. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| 36 <br/> | 4 <br/> | Características <br/>      | Marcas que describen las características de la sección. Para obtener más información, vea [Marcas de sección](#section-flags).<br/>                                                                                                                                                                                                                                                                                                                                                                                                |



 

### <a name="section-flags"></a>Marcas de sección

Las marcas de sección del campo Características del encabezado de sección indican las características de la sección.



| Marca                                              | Value                  | Descripción                                                                                                                                                                 |
|---------------------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                   | 0x00000000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
|                                                   | 0x00000001 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
|                                                   | 0x00000002 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
|                                                   | 0x00000004 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ TYPE \_ NO \_ PAD <br/>             | 0x00000008 <br/> | La sección no debe agregarse al límite siguiente. Esta marca está obsoleta y se reemplaza por IMAGE \_ SCN \_ ALIGN \_ 1BYTES. Esto solo es válido para los archivos de objeto. <br/> |
|                                                   | 0x00000010 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ CNT \_ CODE <br/>                 | 0x00000020 <br/> | La sección contiene código ejecutable. <br/>                                                                                                                           |
| DATOS \_ INICIALIZADOS \_ DE CNT DE SCN \_ DE \_ IMAGEN <br/>    | 0x00000040 <br/> | La sección contiene datos inicializados. <br/>                                                                                                                          |
| DATOS \_ SIN INICIALIZAR DE CNT DE SCN \_ \_ DE \_ IMAGEN <br/> | 0x00000080 <br/> | La sección contiene datos sin inicializar. <br/>                                                                                                                        |
| IMAGE \_ SCN \_ LNK \_ OTHER <br/>                | 0x00000100 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| INFORMACIÓN \_ DE LNK de \_ SCN DE \_ IMAGEN <br/>                 | 0x00000200 <br/> | La sección contiene comentarios u otra información. La sección .drectve tiene este tipo. Esto solo es válido para archivos de objeto. <br/>                                    |
|                                                   | 0x00000400 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ LNK \_ REMOVE <br/>               | 0x00000800 <br/> | La sección no pasará a formar parte de la imagen. Esto solo es válido para los archivos de objeto. <br/>                                                                             |
| IMAGE \_ SCN \_ LNK \_ COMDAT <br/>               | 0x00001000 <br/> | La sección contiene datos COMDAT. Para obtener más información, [vea SECCIONES COMDAT (solo objetos).](#comdat-sections-object-only) Esto solo es válido para los archivos de objeto. <br/> |
| IMAGE \_ SCN \_ GPREL <br/>                     | 0x00008000 <br/> | La sección contiene datos a los que se hace referencia a través del puntero global (GP). <br/>                                                                                           |
| IMAGE \_ SCN \_ MEM \_ PURGEABLE <br/>            | 0x00020000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ 16BIT <br/>                | 0x00020000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ LOCKED <br/>               | 0x00040000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ PRELOAD <br/>              | 0x00080000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ ALIGN \_ 1BYTES <br/>             | 0x00100000 <br/> | Alinear los datos en un límite de 1 byte. Solo es válido para los archivos de objeto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ ALIGN \_ 2BYTES <br/>             | 0x00200000 <br/> | Alinear los datos en un límite de 2 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ ALIGN \_ 4BYTES <br/>             | 0x00300000 <br/> | Alinear los datos en un límite de 4 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ ALIGN \_ 8BYTES <br/>             | 0x00400000 <br/> | Alinear los datos en un límite de 8 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ ALIGN \_ 16BYTES <br/>            | 0x00500000 <br/> | Alinear los datos en un límite de 16 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ ALIGN \_ 32BYTES <br/>            | 0x00600000 <br/> | Alinear los datos en un límite de 32 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ ALIGN \_ 64BYTES <br/>            | 0x00700000 <br/> | Alinear los datos en un límite de 64 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ ALIGN \_ 128BYTES <br/>           | 0x00800000 <br/> | Alinear los datos en un límite de 128 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ ALIGN \_ 256BYTES <br/>           | 0x00900000 <br/> | Alinear los datos en un límite de 256 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ ALIGN \_ 512BYTES <br/>           | 0x00A00000 <br/> | Alinear los datos en un límite de 512 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ ALIGN \_ 1024BYTES <br/>          | 0x00B00000 <br/> | Alinear los datos en un límite de 1024 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                |
| IMAGE \_ SCN \_ ALIGN \_ 2048BYTES <br/>          | 0x00C00000 <br/> | Alinear los datos en un límite de 2048 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                |
| IMAGE \_ SCN \_ ALIGN \_ 4096BYTES <br/>          | 0x00D00000 <br/> | Alinear los datos en un límite de 4096 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                                |
| IMAGE \_ SCN \_ ALIGN \_ 8192BYTES <br/>          | 0x00E00000 <br/> | Alinee los datos en un límite de 8192 bytes. Solo es válido para los archivos de objeto. <br/>                                                                                               |
| IMAGE \_ SCN \_ LNK \_ NRELOC \_ OVFL <br/>         | 0x01000000 <br/> | La sección contiene reubicaciones extendidas. <br/>                                                                                                                      |
| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>          | 0x02000000 <br/> | La sección se puede descartar según sea necesario. <br/>                                                                                                                         |
| MEM \_ DE SCN \_ DE IMAGEN NO ALMACENADO EN \_ \_ CACHÉ <br/>          | 0x04000000 <br/> | La sección no se puede almacenar en caché. <br/>                                                                                                                                   |
| IMAGE \_ SCN \_ MEM \_ NOT \_ PAGED <br/>           | 0x08000000 <br/> | La sección no se puede paginar. <br/>                                                                                                                                    |
| IMAGE \_ SCN \_ MEM \_ SHARED <br/>               | 0x10000000 <br/> | La sección se puede compartir en memoria. <br/>                                                                                                                            |
| IMAGE \_ SCN \_ MEM \_ EXECUTE <br/>              | 0x20000000 <br/> | La sección se puede ejecutar como código. <br/>                                                                                                                            |
| IMAGE \_ SCN \_ MEM \_ READ <br/>                 | 0x40000000 <br/> | La sección se puede leer. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                | 0x80000000 <br/> | Se puede escribir en la sección . <br/>                                                                                                                                  |



 

IMAGE \_ SCN \_ LNK NRELOC OVFL indica que el recuento de reubicaciones de la sección supera los \_ 16 bits reservados para ella en el encabezado \_ de sección. Si se establece el bit y el campo NumberOfRelocations del encabezado de sección es 0xffff, el recuento de reubicaciones real se almacena en el campo VirtualAddress de 32 bits de la primera reubicación. Es un error si image \_ SCN \_ \_ LNK NRELOC OVFL está establecido y hay menos de \_ 0xffff reubicaciones en la sección.

### <a name="grouped-sections-object-only"></a>Secciones agrupadas (solo objeto)

¿El "$"? character (signo de dólar) tiene una interpretación especial en los nombres de sección de los archivos de objeto.

Al determinar la sección de imagen que contendrá el contenido de una sección de objeto, el vinculador descarta "$"? y todos los caracteres que lo siguen. Por lo tanto, una sección de objeto denominada . **text$X** contribuye realmente a la **sección .text** de la imagen.

Sin embargo, ¿los caracteres que sigue a "$"? determinar el orden de las contribuciones a la sección de imagen. Todas las contribuciones con el mismo nombre de sección de objeto se asignan de forma contigua en la imagen y los bloques de contribuciones se ordenan en orden léxico por nombre de sección de objeto. Por lo tanto, todo el contenido de los archivos de objeto con el nombre de sección **.text$X** termina junto, después de las contribuciones **.text$W** y antes de **las contribuciones .text$Y.**

¿El nombre de sección de un archivo de imagen nunca contiene "$"? .

## <a name="other-contents-of-the-file"></a>Otro contenido del archivo

- [Datos de sección](#section-data)
- [Reubicaciones de COFF (solo objeto)](#coff-relocations-object-only)
  - [Indicadores de tipo](#type-indicators)
- [Números de línea COFF (en desuso)](#coff-line-numbers-deprecated)
- [Tabla de símbolos COFF](#coff-symbol-table)
  - [Representación del nombre de símbolo](#symbol-name-representation)
  - [Valores de número de sección](#section-number-values)
  - [Representación de tipo](#type-representation)
  - [Storage Clase](#storage-class)
- [Registros de símbolos auxiliares](#auxiliary-symbol-records)
  - [Formato auxiliar 1: definiciones de función](#auxiliary-format-1-function-definitions)
  - [Formato auxiliar 2: símbolos .bf y .ef](#auxiliary-format-2-bf-and-ef-symbols)
  - [Formato auxiliar 3: externos débiles](#auxiliary-format-3-weak-externals)
  - [Formato auxiliar 4: Archivos](#auxiliary-format-4-files)
  - [Formato auxiliar 5: definiciones de sección](#auxiliary-format-5-section-definitions)
  - [Secciones COMDAT (solo objetos)](#comdat-sections-object-only)
  - [Definición de token CLR (solo objeto)](#clr-token-definition-object-only)
- [Tabla de cadenas COFF](#coff-string-table)
- [Tabla de certificados de atributo (solo imagen)](#the-attribute-certificate-table-image-only)
  - [Datos de certificado](#certificate-data)
- [Tablas de importación de carga retrasada (solo imagen)](#delay-load-import-tables-image-only)
  - [La tabla Delay-Load directory](#the-delay-load-directory-table)
  - [Atributos](#attributes)
  - [Nombre](#name)
  - [Identificador de módulo](#module-handle)
  - [Tabla de direcciones de importación retrasada](#delay-import-address-table)
  - [Tabla de nombres de importación retrasada](#delay-import-name-table)
  - [Tabla de direcciones de importación enlazadas con retraso y marca de tiempo](#delay-bound-import-address-table-and-time-stamp)
  - [Tabla de direcciones de importación de descarga retrasada](#delay-unload-import-address-table)

Las estructuras de datos descritas hasta ahora, hasta el encabezado opcional, se encuentran en un desplazamiento fijo desde el principio del archivo (o desde el encabezado PE si el archivo es una imagen que contiene un código auxiliar de MS-DOS).

El resto de un archivo de imagen o objeto COFF contiene bloques de datos que no están necesariamente en ningún desplazamiento de archivo específico. En su lugar, las ubicaciones se definen mediante punteros en el encabezado opcional o en un encabezado de sección.

Una excepción es para las imágenes con un valor SectionAlignment menor que el tamaño de página de la arquitectura (4 K para Intel x86 y para MIPS, y 8 K para Itanium). Para obtener una descripción de SectionAlignment, vea [Encabezado opcional (solo imagen).](#optional-header-image-only) En este caso, hay restricciones en el desplazamiento de archivo de los datos de sección, como se describe en la sección 5.1, "Datos de sección". Otra excepción es que el certificado de atributo y la información de depuración deben colocarse al final de un archivo de imagen, con la tabla de certificados de atributo inmediatamente anterior a la sección de depuración, porque el cargador no los asigna a la memoria. Sin embargo, la regla sobre el certificado de atributo y la información de depuración no se aplica a los archivos objeto.

### <a name="section-data"></a>Datos de sección

Los datos inicializados para una sección constan de bloques simples de bytes. Sin embargo, para las secciones que contienen todos los ceros, no es necesario incluir los datos de sección.

Los datos de cada sección se encuentran en el desplazamiento de archivo especificado por el campo PointerToRawData en el encabezado de sección. El tamaño de estos datos en el archivo se indica mediante el campo SizeOfRawData. Si SizeOfRawData es menor que VirtualSize, el resto se agrega con ceros.

En un archivo de imagen, los datos de la sección deben alinearse en un límite, tal y como especifica el campo FileAlignment en el encabezado opcional. Los datos de sección deben aparecer en orden de los valores de RVA para las secciones correspondientes (al igual que los encabezados de sección individuales de la tabla de secciones).

Hay restricciones adicionales en los archivos de imagen si el valor SectionAlignment del encabezado opcional es menor que el tamaño de página de la arquitectura. Para estos archivos, la ubicación de los datos de sección en el archivo debe coincidir con su ubicación en memoria cuando se carga la imagen, de modo que el desplazamiento físico de los datos de sección sea el mismo que el de la RVA.

### <a name="coff-relocations-object-only"></a>Reubicaciones de COFF (solo objeto)

Los archivos de objeto contienen reubicaciones de COFF, que especifican cómo se deben modificar los datos de sección cuando se colocan en el archivo de imagen y, posteriormente, se cargan en la memoria.

Los archivos de imagen no contienen reubicaciones de COFF, ya que a todos los símbolos a los que se hace referencia se les han asignado direcciones en un espacio de direcciones planas. Una imagen contiene información de reubicación en forma de reubicaciones base en la sección .reloc (a menos que la imagen tenga el atributo IMAGE \_ FILE \_ RELOCS \_ STRIPPED). Para obtener más información, [vea La sección .reloc (solo imagen).](#the-reloc-section-image-only)

Para cada sección de un archivo de objeto, una matriz de registros de longitud fija contiene las reubicaciones de COFF de la sección. La posición y la longitud de la matriz se especifican en el encabezado de sección. Cada elemento de la matriz tiene el formato siguiente.



| Offset        | Size          | Campo                        | Descripción                                                                                                                                                                                                                                                                                                                                                     |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Dirección del elemento al que se aplica la reubicación. Este es el desplazamiento desde el principio de la sección, más el valor del campo RVA/Offset de la sección. Vea [Tabla de secciones (encabezados de sección).](#section-table-section-headers) Por ejemplo, si el primer byte de la sección tiene una dirección de 0x10, el tercer byte tiene una dirección de 0x12. <br/> |
| 4 <br/> | 4 <br/> | SymbolTableIndex <br/> | Índice de base cero en la tabla de símbolos. Este símbolo proporciona la dirección que se va a usar para la reubicación. Si el símbolo especificado tiene una clase de almacenamiento de sección, la dirección del símbolo es la dirección con la primera sección del mismo nombre. <br/>                                                                                                 |
| 8 <br/> | 2 <br/> | Tipo <br/>             | Valor que indica el tipo de reubicación que se debe realizar. Los tipos de reubicación válidos dependen del tipo de máquina. Vea [Indicadores de tipo](#type-indicators). <br/>                                                                                                                                                                                     |



 

Si el símbolo al que hace referencia el campo SymbolTableIndex tiene la clase de almacenamiento IMAGE SYM CLASS SECTION, la dirección del símbolo es el \_ \_ principio de la \_ sección. La sección suele estar en el mismo archivo, excepto cuando el archivo objeto forma parte de un archivo (biblioteca). En ese caso, la sección se puede encontrar en cualquier otro archivo objeto del archivo que tenga el mismo nombre de miembro de archivo que el archivo objeto actual. (La relación con el nombre del miembro de archivo se usa en la vinculación de tablas de importación, es decir, la sección .idata).

#### <a name="type-indicators"></a>Indicadores de tipo

El campo Tipo del registro de reubicación indica qué tipo de reubicación se debe realizar. Se definen diferentes tipos de reubicación para cada tipo de máquina.

##### <a name="x64-processors"></a>Procesadores x64

Los siguientes indicadores de tipo de reubicación se definen para procesadores x64 y compatibles.



| Constante                                | Value              | Descripción                                                                                                                                                   |
|-----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ AMD64 \_ ABSOLUTE <br/> | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                        |
| IMAGE \_ REL \_ AMD64 \_ ADDR64 <br/>   | 0x0001 <br/> | Va de 64 bits del destino de reubicación. <br/>                                                                                                           |
| IMAGE \_ REL \_ AMD64 \_ ADDR32 <br/>   | 0x0002 <br/> | Va de 32 bits del destino de reubicación. <br/>                                                                                                           |
| IMAGE \_ REL \_ AMD64 \_ ADDR32NB <br/> | 0x0003 <br/> | Dirección de 32 bits sin base de imagen (RVA). <br/>                                                                                                   |
| IMAGE \_ REL \_ AMD64 \_ REL32 <br/>    | 0x0004 <br/> | Dirección relativa de 32 bits del byte siguiente a la reubicación. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 1 <br/> | 0x0005 <br/> | Dirección de 32 bits relativa a la distancia de bytes 1 desde la reubicación. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 2 <br/> | 0x0006 <br/> | Dirección de 32 bits relativa a la distancia de bytes 2 desde la reubicación. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 3 <br/> | 0x0007 <br/> | Dirección de 32 bits relativa a la distancia de bytes 3 desde la reubicación. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 4 <br/> | 0x0008 <br/> | Dirección de 32 bits relativa a la distancia de bytes 4 desde la reubicación. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 5 <br/> | 0x0009 <br/> | Dirección de 32 bits relativa a la distancia de bytes 5 desde la reubicación. <br/>                                                                               |
| SECCIÓN IMAGE \_ REL \_ AMD64 \_ <br/>  | 0x000A <br/> | Índice de sección de 16 bits de la sección que contiene el destino. Se usa para admitir la información de depuración. <br/>                                  |
| IMAGE \_ REL \_ AMD64 \_ SECREL <br/>   | 0x000B <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/> |
| IMAGE \_ REL \_ AMD64 \_ SECREL7 <br/>  | 0x000C <br/> | Desplazamiento de 7 bits sin signo de la base de la sección que contiene el destino. <br/>                                                                    |
| TOKEN \_ \_ AMD64 DE IMAGE REL \_ <br/>    | 0x000D <br/> | Tokens CLR. <br/>                                                                                                                                       |
| IMAGE \_ REL \_ AMD64 \_ SREL32 <br/>   | 0x000E <br/> | Valor dependiente del intervalo de 32 bits con firma emitido en el objeto . <br/>                                                                                     |
| IMAGE \_ REL \_ AMD64 \_ PAIR <br/>     | 0x000F <br/> | Un par que debe seguir inmediatamente cada valor dependiente del intervalo. <br/>                                                                                   |
| IMAGE \_ REL \_ AMD64 \_ SSPAN32 <br/>  | 0x0010 <br/> | Valor dependiente del intervalo de 32 bits con firma que se aplica en el momento del vínculo. <br/>                                                                                |



 

##### <a name="arm-processors"></a>Procesadores ARM

Los siguientes indicadores de tipo de reubicación se definen para los procesadores ARM.



| Constante                                | Value              | Descripción                                                                                                                                                                                                                                                            |
|-----------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ ARM \_ ABSOLUTE <br/>   | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ ARM \_ ADDR32 <br/>     | 0x0001 <br/> | Va de 32 bits del destino. <br/>                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ ARM \_ ADDR32NB <br/>   | 0x0002 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ ARM \_ BRANCH24 <br/>   | 0x0003 <br/> | Desplazamiento relativo de 24 bits al destino. <br/>                                                                                                                                                                                                            |
| IMAGE \_ REL \_ ARM \_ BRANCH11 <br/>   | 0x0004 <br/> | Referencia a una llamada de subrutina. La referencia consta de dos instrucciones de 16 bits con desplazamientos de 11 bits. <br/>                                                                                                                                                 |
| IMAGE \_ REL \_ ARM \_ REL32 <br/>      | 0x000A <br/> | Dirección relativa de 32 bits del byte siguiente a la reubicación. <br/>                                                                                                                                                                                        |
| SECCIÓN \_ DE ARM DE IMAGE REL \_ \_ <br/>    | 0x000E <br/> | Índice de sección de 16 bits de la sección que contiene el destino. Se usa para admitir la información de depuración. <br/>                                                                                                                                           |
| IMAGE \_ REL \_ ARM \_ SECREL <br/>     | 0x000F <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                                                                          |
| IMAGE \_ REL \_ ARM \_ MOV32 <br/>      | 0x0010 <br/> | Va de 32 bits del destino. Esta reubicación se aplica mediante una instrucción MOVW para los 16 bits inferiores seguido de un MOVT para los 16 bits altos. <br/>                                                                                                              |
| IMAGE \_ REL \_ THUMB \_ MOV32 <br/>    | 0x0011 <br/> | Va de 32 bits del destino. Esta reubicación se aplica mediante una instrucción MOVW para los 16 bits inferiores seguido de un MOVT para los 16 bits superiores. <br/>                                                                                                              |
| IMAGE \_ REL \_ THUMB \_ BRANCH20 <br/> | 0x0012 <br/> | La instrucción se ha corregido con el desplazamiento relativo de 21 bits al destino alineado de 2 bytes. El bit menos significativo del desplazamiento siempre es cero y no se almacena. Esta reubicación corresponde a una instrucción B condicional thumb-2 de 32 bits. <br/> |
| No utilizado <br/>                      | 0x0013 <br/> |                                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ THUMB \_ BRANCH24 <br/> | 0x0014 <br/> | La instrucción se ha corregido con el desplazamiento relativo de 25 bits al destino alineado de 2 bytes. El bit menos significativo del desplazamiento es cero y no se almacena. Esta reubicación corresponde a una instrucción Thumb-2 B. <br/>                            |
| IMAGE \_ REL \_ THUMB \_ BLX23 <br/>    | 0x0015 <br/> | La instrucción se ha corregido con el desplazamiento relativo de 25 bits al destino alineado de 4 bytes. Los 2 bits inferiores del desplazamiento son cero y no se almacenan. <br/> Esta reubicación corresponde a una instrucción BLX Thumb-2. <br/>                      |
| IMAGE \_ REL \_ ARM \_ PAIR <br/>       | 0x0016 <br/> | La reubicación solo es válida cuando sigue inmediatamente un REFHI arm o \_ THUMB \_ REFHI. Su SymbolTableIndex contiene un desplazamiento y no un índice en la tabla de símbolos. <br/>                                                                                |



 

##### <a name="arm64-processors"></a>Procesadores ARM64

Los siguientes indicadores de tipo de reubicación se definen para procesadores ARM64.



| Constante                                       | Value              | Descripción                                                                                                                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ ARM64 \_ ABSOLUTE <br/>        | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                        |
| IMAGE \_ REL \_ ARM64 \_ ADDR32 <br/>          | 0x0001 <br/> | Va de 32 bits del destino. <br/>                                                                                                                      |
| IMAGE \_ REL \_ ARM64 \_ ADDR32NB <br/>        | 0x0002 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                     |
| IMAGE \_ REL \_ ARM64 \_ BRANCH26 <br/>        | 0x0003 <br/> | Desplazamiento relativo de 26 bits al destino, para instrucciones B y BL. <br/>                                                                        |
| IMAGE \_ REL \_ ARM64 \_ PAGEBASE \_ REL21 <br/> | 0x0004 <br/> | Base de página del destino, para la instrucción ADRP. <br/>                                                                                                |
| IMAGE \_ REL \_ ARM64 \_ REL21 <br/>           | 0x0005 <br/> | Desplazamiento relativo de 12 bits al destino, para la instrucción ADR <br/>                                                                               |
| IMAGE \_ REL \_ ARM64 \_ PAGEOFFSET \_ 12A <br/> | 0x0006 <br/> | Desplazamiento de página de 12 bits del destino, para obtener instrucciones ADD/ADDS (inmediato) con desplazamiento cero. <br/>                                                      |
| IMAGE \_ REL \_ ARM64 \_ PAGEOFFSET \_ 12L <br/> | 0x0007 <br/> | Desplazamiento de página de 12 bits del destino, para la instrucción LDR (indexada, sin signo inmediata). <br/>                                                          |
| IMAGE \_ REL \_ ARM64 \_ SECREL <br/>          | 0x0008 <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/> |
| IMAGE \_ REL \_ ARM64 \_ SECREL \_ LOW12A <br/>  | 0x0009 <br/> | Bit 0:11 de desplazamiento de sección del destino, para obtener instrucciones add/adds (inmediato) con desplazamiento cero. <br/>                                                  |
| IMAGE \_ REL \_ ARM64 \_ SECREL \_ HIGH12A <br/> | 0x000A <br/> | Bit 12:23 del desplazamiento de sección del destino, para obtener instrucciones add/adds (inmediato) con desplazamiento cero. <br/>                                                 |
| IMAGE \_ REL \_ ARM64 \_ SECREL \_ LOW12L <br/>  | 0x000B <br/> | Bit 0:11 de desplazamiento de sección del destino, para la instrucción LDR (indexada, sin signo inmediata). <br/>                                                      |
| TOKEN \_ DE IMAGE REL \_ ARM64 \_ <br/>           | 0x000C <br/> | Token clr. <br/>                                                                                                                                        |
| SECCIÓN \_ IMAGE REL \_ ARM64 \_ <br/>         | 0x000D <br/> | Índice de sección de 16 bits de la sección que contiene el destino. Se usa para admitir la información de depuración. <br/>                                  |
| IMAGE \_ REL \_ ARM64 \_ ADDR64 <br/>          | 0x000E <br/> | Va de 64 bits del destino de reubicación. <br/>                                                                                                           |
| IMAGE \_ REL \_ ARM64 \_ BRANCH19 <br/>        | 0x000F <br/> | Desplazamiento de 19 bits al destino de reubicación, para la instrucción B condicional. <br/>                                                                        |
| IMAGE \_ REL \_ ARM64 \_ BRANCH14 <br/>        | 0x0010 <br/> | Desplazamiento de 14 bits al destino de reubicación, para obtener instrucciones TBZ y TBNZ. <br/>                                                                        |
| IMAGE \_ REL \_ ARM64 \_ REL32 <br/>           | 0x0011 <br/> | Dirección relativa de 32 bits del byte siguiente a la reubicación. <br/>                                                                               |

##### <a name="hitachi-superh-processors"></a>Procesadores SuperH de Amd

Los siguientes indicadores de tipo de reubicación se definen para los procesadores SH3 y SH4. Las reubicaciones específicas de SH5 se anotan como SHM (SH Media).



| Constante                                      | Value              | Descripción                                                                                                                                                                                                                |
|-----------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ SH3 \_ ABSOLUTE <br/>         | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                     |
| IMAGE \_ REL \_ SH3 \_ DIRECT16 <br/>         | 0x0001 <br/> | Referencia a la ubicación de 16 bits que contiene el VA del símbolo de destino. <br/>                                                                                                                                  |
| IMAGE \_ REL \_ SH3 \_ DIRECT32 <br/>         | 0x0002 <br/> | Va de 32 bits del símbolo de destino. <br/>                                                                                                                                                                            |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 <br/>          | 0x0003 <br/> | Referencia a la ubicación de 8 bits que contiene el VA del símbolo de destino. <br/>                                                                                                                                   |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 \_ WORD <br/>    | 0x0004 <br/> | Referencia a la instrucción de 8 bits que contiene la va de 16 bits efectiva del símbolo de destino. <br/>                                                                                                               |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 \_ LONG <br/>    | 0x0005 <br/> | Referencia a la instrucción de 8 bits que contiene la va de 32 bits efectiva del símbolo de destino. <br/>                                                                                                               |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 <br/>          | 0x0006 <br/> | Referencia a la ubicación de 8 bits cuyos 4 bits inferiores contienen el VA del símbolo de destino. <br/>                                                                                                                        |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 \_ WORD <br/>    | 0x0007 <br/> | Referencia a la instrucción de 8 bits cuyos 4 bits inferiores contienen el va efectivo de 16 bits del símbolo de destino. <br/>                                                                                                    |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 \_ LONG <br/>    | 0x0008 <br/> | Referencia a la instrucción de 8 bits cuyos 4 bits inferiores contienen el VA efectivo de 32 bits del símbolo de destino. <br/>                                                                                                    |
| IMAGE \_ REL \_ SH3 \_ PCREL8 \_ WORD <br/>     | 0x0009 <br/> | Referencia a la instrucción de 8 bits que contiene el desplazamiento relativo efectivo de 16 bits del símbolo de destino. <br/>                                                                                                  |
| IMAGE \_ REL \_ SH3 \_ PCREL8 \_ LONG <br/>     | 0x000A <br/> | Referencia a la instrucción de 8 bits que contiene el desplazamiento relativo efectivo de 32 bits del símbolo de destino. <br/>                                                                                                  |
| IMAGE \_ REL \_ SH3 \_ PCREL12 \_ WORD <br/>    | 0x000B <br/> | Referencia a la instrucción de 16 bits cuyos 12 bits inferiores contienen el desplazamiento relativo efectivo de 16 bits del símbolo de destino. <br/>                                                                                     |
| SECCIÓN IMAGE \_ REL \_ SH3 \_ STARTOF \_ <br/> | 0x000C <br/> | Referencia a una ubicación de 32 bits que es el VA de la sección que contiene el símbolo de destino. <br/>                                                                                                                |
| SECCIÓN IMAGE \_ REL \_ SH3 \_ SIZEOF \_ <br/>  | 0x000D <br/> | Referencia a la ubicación de 32 bits que es el tamaño de la sección que contiene el símbolo de destino. <br/>                                                                                                            |
| SECCIÓN \_ IMAGE REL \_ SH3 \_ <br/>          | 0x000E <br/> | Índice de sección de 16 bits de la sección que contiene el destino. Se usa para admitir la información de depuración. <br/>                                                                                               |
| IMAGE \_ REL \_ SH3 \_ SECREL <br/>           | 0x000F <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                              |
| IMAGE \_ REL \_ SH3 \_ DIRECT32 \_ NB <br/>     | 0x0010 <br/> | RVA de 32 bits del símbolo de destino. <br/>                                                                                                                                                                           |
| IMAGE \_ REL \_ SH3 \_ GPREL4 \_ LONG <br/>     | 0x0011 <br/> | Relativa a GP. <br/>                                                                                                                                                                                                   |
| TOKEN \_ DE IMAGE REL \_ SH3 \_ <br/>            | 0x0012 <br/> | Token clr. <br/>                                                                                                                                                                                                     |
| IMAGE \_ REL \_ SHM \_ PCRELPT <br/>          | 0x0013 <br/> | Desplazamiento de la instrucción actual en palabras largas. Si no se establece el bit NOMODE, inserte el inverso del bit bajo en el bit 32 para seleccionar PTA o PTB. <br/>                                                          |
| IMAGE \_ REL \_ SHM \_ REFLO <br/>            | 0x0014 <br/> | Los 16 bits inferiores de la dirección de 32 bits. <br/>                                                                                                                                                                         |
| IMAGE \_ REL \_ SHM \_ REFHALF <br/>          | 0x0015 <br/> | Los 16 bits altos de la dirección de 32 bits. <br/>                                                                                                                                                                        |
| IMAGE \_ REL \_ SHM \_ RELLO <br/>            | 0x0016 <br/> | Los 16 bits inferiores de la dirección relativa. <br/>                                                                                                                                                                       |
| IMAGE \_ REL \_ SHM \_ RELF <br/>          | 0x0017 <br/> | Los 16 bits altos de la dirección relativa. <br/>                                                                                                                                                                      |
| IMAGE \_ REL \_ SHM \_ PAIR <br/>             | 0x0018 <br/> | La reubicación solo es válida cuando sigue inmediatamente a una reubicación REFHALF, RELF o RELLO. El campo SymbolTableIndex de la reubicación contiene un desplazamiento y no un índice en la tabla de símbolos. <br/> |
| IMAGE \_ REL \_ SHM \_ NOMODE <br/>           | 0x8000 <br/> | La reubicación omite el modo de sección. <br/>                                                                                                                                                                           |



 

##### <a name="ibm-powerpc-processors"></a>Procesadores PowerPC IBM

Los siguientes indicadores de tipo de reubicación se definen para PowerPC procesadores.



| Constante                              | Value              | Descripción                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ PPC \_ ABSOLUTE <br/> | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ PPC \_ ADDR64 <br/>   | 0x0001 <br/> | Va de 64 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ PPC \_ ADDR32 <br/>   | 0x0002 <br/> | Va de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ PPC \_ ADDR24 <br/>   | 0x0003 <br/> | Los 24 bits inferiores del va del destino. Esto solo es válido cuando el símbolo de destino es absoluto y se puede extender el signo a su valor original. <br/>                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ PPC \_ ADDR16 <br/>   | 0x0004 <br/> | Los 16 bits inferiores del VA del destino. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ PPC \_ ADDR14 <br/>   | 0x0005 <br/> | Los 14 bits inferiores del VA del destino. Esto solo es válido cuando el símbolo de destino es absoluto y se puede extender el signo a su valor original. <br/>                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ PPC \_ REL24 <br/>    | 0x0006 <br/> | Desplazamiento relativo al equipo de 24 bits a la ubicación del símbolo. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ REL14 <br/>    | 0x0007 <br/> | Desplazamiento relativo al equipo de 14 bits a la ubicación del símbolo. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ ADDR32NB <br/> | 0x000A <br/> | RVA de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ PPC \_ SECREL <br/>   | 0x000B <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                                                                                                                                                                                       |
| SECCIÓN \_ IMAGE REL \_ \_ PPC <br/>  | 0x000C <br/> | Índice de sección de 16 bits de la sección que contiene el destino. Se usa para admitir la información de depuración. <br/>                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ PPC \_ SECREL16 <br/> | 0x000F <br/> | Desplazamiento de 16 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                                                                                                                                                                                       |
| IMAGE \_ REL \_ PPC \_ REFHI <br/>    | 0x0010 <br/> | Los 16 bits altos del va de 32 bits del destino. Se usa para la primera instrucción en una secuencia de dos instrucciones que carga una dirección completa. Esta reubicación debe ir seguida inmediatamente de una reubicación PAIR cuyo SymbolTableIndex contiene un desplazamiento de 16 bits firmado que se agrega a los 16 bits superiores que se tomaron de la ubicación que se va a reubicar. <br/> |
| IMAGE \_ REL \_ PPC \_ REFLO <br/>    | 0x0011 <br/> | Los 16 bits inferiores del VA del destino. <br/>                                                                                                                                                                                                                                                                                                                                     |
| PAR PPC DE IMAGE \_ REL \_ \_ <br/>     | 0x0012 <br/> | Reubicación que solo es válida cuando sigue inmediatamente a una reubicación REFHI o SECRELHI. Su SymbolTableIndex contiene un desplazamiento y no un índice en la tabla de símbolos. <br/>                                                                                                                                                                                        |
| IMAGE \_ REL \_ PPC \_ SECRELLO <br/> | 0x0013 <br/> | Los 16 bits inferiores del desplazamiento de 32 bits del destino desde el principio de su sección. <br/>                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ GPREL <br/>    | 0x0015 <br/> | Desplazamiento firmado de 16 bits del destino en relación con el registro de GP. <br/>                                                                                                                                                                                                                                                                                               |
| TOKEN \_ de \_ PPC de IMAGE REL \_ <br/>    | 0x0016 <br/> | El token clr. <br/>                                                                                                                                                                                                                                                                                                                                                          |



 

##### <a name="intel-386-processors"></a>Procesadores Intel 386

Los siguientes indicadores de tipo de reubicación se definen para Intel 386 y procesadores compatibles.



| Constante                               | Value              | Descripción                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ I386 \_ ABSOLUTE <br/> | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                        |
| IMAGE \_ REL \_ I386 \_ DIR16 <br/>    | 0x0001 <br/> | No compatible. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ I386 \_ REL16 <br/>    | 0x0002 <br/> | No compatible. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ I386 \_ DIR32 <br/>    | 0x0006 <br/> | Va de 32 bits del destino. <br/>                                                                                                                           |
| IMAGE \_ REL \_ I386 \_ DIR32NB <br/>  | 0x0007 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                          |
| IMAGE \_ REL \_ I386 \_ SEG12 <br/>    | 0x0009 <br/> | No compatible. <br/>                                                                                                                                    |
| SECCIÓN \_ IMAGE REL \_ I386 \_ <br/>  | 0x000A <br/> | Índice de sección de 16 bits de la sección que contiene el destino. Se usa para admitir la información de depuración. <br/>                                  |
| IMAGE \_ REL \_ I386 \_ SECREL <br/>   | 0x000B <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/> |
| TOKEN \_ DE IMAGE REL \_ I386 \_ <br/>    | 0x000C <br/> | El token clr. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ I386 \_ SECREL7 <br/>  | 0x000D <br/> | Desplazamiento de 7 bits desde la base de la sección que contiene el destino. <br/>                                                                             |
| IMAGE \_ REL \_ I386 \_ REL32 <br/>    | 0x0014 <br/> | Desplazamiento relativo de 32 bits al destino. Esto admite la rama relativa x86 y las instrucciones de llamada. <br/>                                      |



 

##### <a name="intel-itanium-processor-family-ipf"></a>Familia de procesadores Intel Itanium (IPF)

Los siguientes indicadores de tipo de reubicación se definen para la familia de procesadores Intel Itanium y procesadores compatibles. Tenga en cuenta que las reubicaciones en instrucciones usan el desplazamiento y el número de ranura del conjunto para el desplazamiento de reubicación.



| Constante                                 | Value              | Descripción                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ IA64 \_ ABSOLUTE <br/>   | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ IA64 \_ IMM14 <br/>      | 0x0001 <br/> | La reubicación de instrucciones puede ir seguida de una reubicación ADDEND cuyo valor se agrega a la dirección de destino antes de insertarla en la ranura especificada en la agrupación IMM14. El destino de reubicación debe ser absoluto o la imagen debe ser fija. <br/>                                                                                 |
| IMAGE \_ REL \_ IA64 \_ IMM22 <br/>      | 0x0002 <br/> | La reubicación de instrucciones puede ir seguida de una reubicación ADDEND cuyo valor se agrega a la dirección de destino antes de insertarla en la ranura especificada en la agrupación IMM22. El destino de reubicación debe ser absoluto o la imagen debe ser fija. <br/>                                                                                 |
| IMAGE \_ REL \_ IA64 \_ IMM64 <br/>      | 0x0003 <br/> | El número de ranura de esta reubicación debe ser uno (1). La reubicación puede ir seguida de una reubicación ADDEND cuyo valor se agrega a la dirección de destino antes de almacenarse en los tres espacios de la agrupación IMM64. <br/>                                                                                                                   |
| IMAGE \_ REL \_ IA64 \_ DIR32 <br/>      | 0x0004 <br/> | Va de 32 bits del destino. Esto solo se admite para las imágenes /LARGEADDRESSAWARE:NO. <br/>                                                                                                                                                                                                                                                    |
| IMAGE \_ REL \_ IA64 \_ DIR64 <br/>      | 0x0005 <br/> | Va de 64 bits del destino. <br/>                                                                                                                                                                                                                                                                                                             |
| IMAGE \_ REL \_ IA64 \_ PCREL21B <br/>   | 0x0006 <br/> | La instrucción se ha corregido con el desplazamiento relativo de 25 bits al destino alineado de 16 bits. Los 4 bits inferiores del desplazamiento son cero y no se almacenan. <br/>                                                                                                                                                                     |
| IMAGE \_ REL \_ IA64 \_ PCREL21M <br/>   | 0x0007 <br/> | La instrucción se ha corregido con el desplazamiento relativo de 25 bits al destino alineado de 16 bits. Los 4 bits inferiores del desplazamiento, que son cero, no se almacenan. <br/>                                                                                                                                                                 |
| IMAGE \_ REL \_ IA64 \_ PCREL21F <br/>   | 0x0008 <br/> | Los LSB del desplazamiento de esta reubicación deben contener el número de ranura, mientras que el resto es la dirección de agrupación. La agrupación se ha corregido con el desplazamiento relativo de 25 bits al destino alineado de 16 bits. Los 4 bits inferiores del desplazamiento son cero y no se almacenan. <br/>                                                                |
| IMAGE \_ REL \_ IA64 \_ GPREL22 <br/>    | 0x0009 <br/> | La reubicación de instrucciones puede ir seguida de una reubicación ADDEND cuyo valor se agrega a la dirección de destino y, a continuación, un desplazamiento relativo a GP de 22 bits que se calcula y se aplica a la agrupación GPREL22. <br/>                                                                                                                            |
| IMAGE \_ REL \_ IA64 \_ LTOFF22 <br/>    | 0x000A <br/> | La instrucción se fija con el desplazamiento relativo a GP de 22 bits con respecto a la entrada de tabla literal del símbolo de destino. El vinculador crea esta entrada de tabla literal basada en esta reubicación y en la reubicación addend que podría seguir. <br/>                                                                                                        |
| SECCIÓN \_ IMAGE REL \_ IA64 \_ <br/>    | 0x000B <br/> | El índice de sección de 16 bits de la sección contiene el destino. Se usa para admitir la información de depuración. <br/>                                                                                                                                                                                                                         |
| IMAGE \_ REL \_ IA64 \_ SECREL22 <br/>   | 0x000C <br/> | La instrucción se fija con el desplazamiento de 22 bits del destino desde el principio de su sección. Esta reubicación puede ir seguida inmediatamente de una reubicación ADDEND, cuyo campo Valor contiene el desplazamiento de 32 bits sin signo del destino desde el principio de la sección. <br/>                                                     |
| IMAGE \_ REL \_ IA64 \_ SECREL64I <br/>  | 0x000D <br/> | El número de ranura para esta reubicación debe ser uno (1). La instrucción se fija con el desplazamiento de 64 bits del destino desde el principio de su sección. Esta reubicación puede ir seguida inmediatamente de una reubicación ADDEND cuyo campo Valor contiene el desplazamiento sin signo de 32 bits del destino desde el principio de la sección. <br/> |
| IMAGE \_ REL \_ IA64 \_ SECREL32 <br/>   | 0x000E <br/> | Dirección de datos que se va a solucionar con el desplazamiento de 32 bits del destino desde el principio de su sección. <br/>                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ IA64 \_ DIR32NB <br/>    | 0x0010 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ IA64 \_ SREL14 <br/>     | 0x0011 <br/> | Esto se aplica a una firma inmediata de 14 bits que contiene la diferencia entre dos destinos relocables. Se trata de un campo declarativo para el vinculador que indica que el compilador ya ha emitido este valor. <br/>                                                                                                              |
| IMAGE \_ REL \_ IA64 \_ SREL22 <br/>     | 0x0012 <br/> | Esto se aplica a un inmediato de 22 bits con firma que contiene la diferencia entre dos destinos relocables. Se trata de un campo declarativo para el vinculador que indica que el compilador ya ha emitido este valor. <br/>                                                                                                              |
| IMAGE \_ REL \_ IA64 \_ SREL32 <br/>     | 0x0013 <br/> | Esto se aplica a un inmediato de 32 bits con firma que contiene la diferencia entre dos valores relocables. Se trata de un campo declarativo para el vinculador que indica que el compilador ya ha emitido este valor. <br/>                                                                                                               |
| IMAGE \_ REL \_ IA64 \_ UREL32 <br/>     | 0x0014 <br/> | Esto se aplica a un inmediato de 32 bits sin signo que contiene la diferencia entre dos valores relocables. Se trata de un campo declarativo para el vinculador que indica que el compilador ya ha emitido este valor. <br/>                                                                                                            |
| IMAGE \_ REL \_ IA64 \_ PCREL60X <br/>   | 0x0015 <br/> | Una corrección relativa a pc de 60 bits que siempre permanece como una instrucción BRL de un paquete MLX. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ IA64 \_ PCREL60B <br/>   | 0x0016 <br/> | Una corrección relativa al equipo de 60 bits. Si el desplazamiento de destino se ajusta a un campo de 25 bits firmado, convierta toda la agrupación en una agrupación MBB con NOP. B en la ranura 1 y una instrucción BR de 25 bits (con los 4 bits más bajos todos ceros y eliminados) en la ranura 2. <br/>                                                                                          |
| IMAGE \_ REL \_ IA64 \_ PCREL60F <br/>   | 0x0017 <br/> | Una corrección relativa al equipo de 60 bits. Si el desplazamiento de destino se ajusta a un campo de 25 bits firmado, convierta la agrupación completa en una agrupación MFB con NOP. F en la ranura 1 y una instrucción BR de 25 bits (4 bits más bajos, todos ceros y eliminados) en la ranura 2. <br/>                                                                                                   |
| IMAGE \_ REL \_ IA64 \_ PCREL60I <br/>   | 0x0018 <br/> | Una corrección relativa al equipo de 60 bits. Si el desplazamiento de destino se ajusta a un campo de 25 bits firmado, convierta toda la agrupación en una agrupación MIB con NOP. I in slot 1 and a 25-bit (4 lowest bits all zero and dropped) BR instruction in slot 2. <br/>                                                                                                   |
| IMAGE \_ REL \_ IA64 \_ PCREL60M <br/>   | 0x0019 <br/> | Una corrección relativa al equipo de 60 bits. Si el desplazamiento de destino se ajusta a un campo de 25 bits firmado, convierta toda la agrupación en una agrupación de MMB con NOP. M en la ranura 1 y una instrucción BR de 25 bits (4 bits más bajos todos ceros y eliminados) en la ranura 2. <br/>                                                                                                   |
| IMAGE \_ REL \_ IA64 \_ IMMGPREL64 <br/> | 0x001a <br/> | Una corrección relativa a GP de 64 bits. <br/>                                                                                                                                                                                                                                                                                                         |
| TOKEN \_ DE IMAGE REL \_ IA64 \_ <br/>      | 0x001b <br/> | Un token CLR. <br/>                                                                                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ IA64 \_ GPREL32 <br/>    | 0x001c <br/> | Una corrección relativa a GP de 32 bits. <br/>                                                                                                                                                                                                                                                                                                         |
| IMAGE \_ REL \_ IA64 \_ ADDEND <br/>     | 0x001F <br/> | La reubicación solo es válida cuando sigue inmediatamente una de las siguientes reubicaciones: IMM14, IMM22, IMM64, GPREL22, LTOFF22, LTOFF64, SECREL22, SECREL64I o SECREL32. Su valor contiene el complemento que se va a aplicar a las instrucciones dentro de una agrupación, no a los datos. <br/>                                                                  |



 

##### <a name="mips-processors"></a>Procesadores MIPS

Los siguientes indicadores de tipo de reubicación se definen para los procesadores MIPS.



| Constante                                | Value              | Descripción                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ MIPS \_ ABSOLUTE <br/>  | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ MIPS \_ REFHALF <br/>   | 0x0001 <br/> | Los 16 bits altos de la va de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                             |
| IMAGE \_ REL \_ MIPS \_ REFWORD <br/>   | 0x0002 <br/> | Va de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ MIPS \_ JMPADDR <br/>   | 0x0003 <br/> | Los 26 bits inferiores del VA del destino. Esto es compatible con las instrucciones MIPS J y MOMENTO. <br/>                                                                                                                                                                                                                                                                                      |
| IMAGE \_ REL \_ MIPS \_ REFHI <br/>     | 0x0004 <br/> | Los 16 bits altos de la va de 32 bits del destino. Se usa para la primera instrucción en una secuencia de dos instrucciones que carga una dirección completa. Esta reubicación debe ir seguida inmediatamente de una reubicación PAIR cuyo SymbolTableIndex contiene un desplazamiento de 16 bits firmado que se agrega a los 16 bits superiores que se toman de la ubicación que se va a reubicar. <br/> |
| IMAGE \_ REL \_ MIPS \_ REFLO <br/>     | 0x0005 <br/> | Los 16 bits inferiores del VA del destino. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ MIPS \_ GPREL <br/>     | 0x0006 <br/> | Desplazamiento de 16 bits con firma del destino en relación con el registro gp. <br/>                                                                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ MIPS \_ LITERAL <br/>   | 0x0007 <br/> | Igual que IMAGE \_ REL \_ MIPS \_ GPREL. <br/>                                                                                                                                                                                                                                                                                                                                    |
| SECCIÓN \_ MIPS DE IMAGE REL \_ \_ <br/>   | 0x000A <br/> | El índice de sección de 16 bits de la sección contiene el destino. Se usa para admitir la información de depuración. <br/>                                                                                                                                                                                                                                                             |
| IMAGE \_ REL \_ MIPS \_ SECREL <br/>    | 0x000B <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                                                                                                                                                                                       |
| IMAGE \_ REL \_ MIPS \_ SECRELLO <br/>  | 0x000C <br/> | Los 16 bits inferiores del desplazamiento de 32 bits del destino desde el principio de su sección. <br/>                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ MIPS \_ SECRELHI <br/>  | 0x000D <br/> | Los 16 bits altos del desplazamiento de 32 bits del destino desde el principio de su sección. Una \_ reubicación de IMAGE REL \_ MIPS \_ PAIR debe seguir inmediatamente a esta. SymbolTableIndex de la reubicación pair contiene un desplazamiento de 16 bits firmado que se agrega a los 16 bits superiores que se toman de la ubicación que se va a reubicar. <br/>                            |
| IMAGE \_ REL \_ MIPS \_ JMPADDR16 <br/> | 0x0010 <br/> | Los 26 bits inferiores del VA del destino. Esto es compatible con la instrucción MIPS16 LA. <br/>                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ MIPS \_ REFWORDNB <br/> | 0x0022 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                                                |
| PAR \_ MIPS DE IMAGE REL \_ \_ <br/>      | 0x0025 <br/> | La reubicación solo es válida cuando sigue inmediatamente a una reubicación REFHI o SECRELHI. Su SymbolTableIndex contiene un desplazamiento y no un índice en la tabla de símbolos. <br/>                                                                                                                                                                                           |



 

##### <a name="mitsubishi-m32r"></a>Noé M32R

Los siguientes indicadores de tipo de reubicación se definen para los procesadores M32R de Noé.



| Constante                               | Value              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ M32R \_ ABSOLUTE <br/> | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ M32R \_ ADDR32 <br/>   | 0x0001 <br/> | Va de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ M32R \_ ADDR32NB <br/> | 0x0002 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ M32R \_ ADDR24 <br/>   | 0x0003 <br/> | Va de 24 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ M32R \_ GPREL16 <br/>  | 0x0004 <br/> | Desplazamiento de 16 bits del destino desde el registro gp. <br/>                                                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ REL \_ M32R \_ PCREL24 <br/>  | 0x0005 <br/> | Desplazamiento de 24 bits del destino desde el contador de programa (PC), desplazado a la izquierda por 2 bits y extendido por signo <br/>                                                                                                                                                                                                                                                                                                |
| IMAGE \_ REL \_ M32R \_ PCREL16 <br/>  | 0x0006 <br/> | Desplazamiento de 16 bits del equipo del destino, desplazado a la izquierda por 2 bits y extendido por signo <br/>                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ REL \_ M32R \_ PCREL8 <br/>   | 0x0007 <br/> | Desplazamiento de 8 bits del equipo del destino, desplazado a la izquierda por 2 bits y extendido por signo <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ M32R \_ REFHALF <br/>  | 0x0008 <br/> | Los 16 MSB del VA de destino. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ M32R \_ REFHI <br/>    | 0x0009 <br/> | Los 16 MSB del VA de destino, ajustados para la extensión de firma LSB. Se usa para la primera instrucción en una secuencia de dos instrucciones que carga una dirección de 32 bits completa. Esta reubicación debe ir seguida inmediatamente de una reubicación PAIR cuyo SymbolTableIndex contiene un desplazamiento de 16 bits firmado que se agrega a los 16 bits superiores que se toman de la ubicación que se va a reubicar. <br/> |
| IMAGE \_ REL \_ M32R \_ REFLO <br/>    | 0x000A <br/> | Los 16 LSB del VA de destino. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ M32R \_ PAIR <br/>     | 0x000B <br/> | La reubicación debe seguir la reubicación de REFHI. Su SymbolTableIndex contiene un desplazamiento y no un índice en la tabla de símbolos. <br/>                                                                                                                                                                                                                                                             |
| SECCIÓN \_ IMAGE REL \_ M32R \_ <br/>  | 0x000C <br/> | Índice de sección de 16 bits de la sección que contiene el destino. Se usa para admitir la información de depuración. <br/>                                                                                                                                                                                                                                                                                  |
| IMAGE \_ REL \_ M32R \_ SECREL <br/>   | 0x000D <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                                                                                                                                                                                                                 |
| TOKEN \_ DE IMAGE REL \_ M32R \_ <br/>    | 0x000E <br/> | El token clr. <br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="coff-line-numbers-deprecated"></a>Números de línea COFF (en desuso)

Los números de línea COFF ya no se generan y, en el futuro, no se consumirán.

Los números de línea COFF indican la relación entre el código y los números de línea en los archivos de código fuente. El formato de Microsoft para los números de línea COFF es similar al estándar COFF, pero se ha ampliado para permitir que una sola sección se relaciona con números de línea en varios archivos de origen.

Los números de línea COFF constan de una matriz de registros de longitud fija. La ubicación (desplazamiento de archivo) y el tamaño de la matriz se especifican en el encabezado de sección. Cada registro de número de línea tiene el formato siguiente.



| Offset        | Size          | Campo                  | Descripción                                                                                                                                                 |
|---------------|---------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Tipo ( \* ) <br/>  | Se trata de una unión de dos campos: SymbolTableIndex y VirtualAddress. El uso de SymbolTableIndex o RVA depende del valor de Linenumber. <br/> |
| 4 <br/> | 2 <br/> | Número de línea <br/> | Cuando es distinto de cero, este campo especifica un número de línea basado en uno. Cuando es cero, el campo Tipo se interpreta como un índice de tabla de símbolos para una función. <br/>    |



 

El campo Tipo es una unión de dos campos de 4 bytes: SymbolTableIndex y VirtualAddress.



| Offset        | Size          | Campo                        | Descripción                                                                                                                                                                             |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | SymbolTableIndex <br/> | Se usa cuando Linenumber es cero: entrada de índice a tabla de símbolos para una función. Este formato se usa para indicar la función a la que hace referencia un grupo de registros de número de línea. <br/>      |
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Se usa cuando Linenumber es distinto de cero: el RVA del código ejecutable que corresponde a la línea de origen indicada. En un archivo de objeto, contiene el va dentro de la sección . <br/> |



 

Un registro de número de línea puede establecer el campo Número de línea en cero y apuntar a una definición de función en la tabla de símbolos o puede funcionar como una entrada de número de línea estándar al dar un entero positivo (número de línea) y la dirección correspondiente en el código del objeto.

Un grupo de entradas de número de línea siempre comienza con el primer formato: el índice de un símbolo de función. Si este es el primer registro de número de línea de la sección, también es el nombre del símbolo COMDAT para la función si se establece la marca COMDAT de la sección. Vea [Secciones comdat (solo objeto).](#comdat-sections-object-only) El registro auxiliar de la función en la tabla de símbolos tiene un puntero al campo Número de línea que apunta a este mismo registro de número de línea.

Un registro que identifica una función va seguido de cualquier número de entradas de número de línea que proporciona información real de número de línea (es decir, entradas con linenumber mayor que cero). Estas entradas se basan en uno, en relación con el principio de la función, y representan todas las líneas de origen de la función, excepto la primera línea.

Por ejemplo, el primer registro de número de línea para el ejemplo siguiente especificaría la función ReverseSign (SymbolTableIndex de ReverseSign y Linenumber establecida en cero). A continuación, se seguirían los registros con valores linenumber de 1, 2 y 3, correspondientes a las líneas de origen como se muestra:


```C++
// some code precedes ReverseSign function
int ReverseSign(int i)
1: {
2:  return -1 * i;
3: }
```



### <a name="coff-symbol-table"></a>Tabla de símbolos COFF

La tabla de símbolos de esta sección se hereda del formato COFF tradicional. Es distinto de la Microsoft Visual C++ de depuración. Un archivo puede contener una tabla de símbolos COFF Visual C++ información de depuración, y los dos se mantienen independientes. Algunas herramientas de Microsoft usan la tabla de símbolos con fines limitados pero importantes, como la comunicación de información COMDAT al vinculador. Los nombres de sección y los nombres de archivo, así como los símbolos de código y datos, se enumeran en la tabla de símbolos.

La ubicación de la tabla de símbolos se indica en el encabezado COFF.

La tabla de símbolos es una matriz de registros, cada uno de 18 bytes de longitud. Cada registro es un registro de tabla de símbolos estándar o auxiliar. Un registro estándar define un símbolo o nombre y tiene el formato siguiente.



| Offset         | Size          | Campo                          | Descripción                                                                                                                                                                                                                                 |
|----------------|---------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Name ( \* ) <br/>          | Nombre del símbolo, representado por una unión de tres estructuras. Se usa una matriz de 8 bytes si el nombre no tiene más de 8 bytes. Para obtener más información, vea [Representación de nombre de símbolo](https://www.bing.com/search?q=Symbol+Name+Representation). <br/> |
| 8 <br/>  | 4 <br/> | Value <br/>              | Valor asociado al símbolo. La interpretación de este campo depende de SectionNumber y StorageClass. Un significado típico es la dirección que se puede volver a convertir. <br/>                                                         |
| 12 <br/> | 2 <br/> | SectionNumber <br/>      | Entero con signo que identifica la sección, utilizando un índice basado en uno en la tabla de secciones. Algunos valores tienen un significado especial, tal como se define en la sección 5.4.2, "Valores de número de sección". <br/>                                         |
| 14 <br/> | 2 <br/> | Tipo <br/>               | Número que representa el tipo. Las herramientas de Microsoft establecen este campo 0x20 (función) o 0x0 (no una función). Para obtener más información, vea [Representación de tipos.](#type-representation) <br/>                                                |
| 16 <br/> | 1 <br/> | StorageClass <br/>       | Valor enumerado que representa la clase de almacenamiento. Para obtener más información, [vea Storage clase](#storage-class). <br/>                                                                                                                   |
| 17 <br/> | 1 <br/> | NumberOf BlueSymbols <br/> | Número de entradas de tabla de símbolos auxiliares que siguen a este registro. <br/>                                                                                                                                                           |



 

Cero o más registros auxiliares de tabla de símbolos inmediatamente siguen cada registro de tabla de símbolos estándar. Sin embargo, normalmente no más de un registro auxiliar de tabla de símbolos sigue un registro de tabla de símbolos estándar (excepto para los registros .file con nombres de archivo largos). Cada registro auxiliar tiene el mismo tamaño que un registro de tabla de símbolos estándar (18 bytes), pero en lugar de definir un nuevo símbolo, el registro auxiliar proporciona información adicional sobre el último símbolo definido. La elección de cuál de varios formatos se va a usar depende del campo StorageClass. Los formatos definidos actualmente para los registros de tabla de símbolos auxiliares se muestran en la sección 5.5, "Registros de símbolos auxiliares".

Las herramientas que leen tablas de símbolos COFF deben omitir los registros de símbolos auxiliares cuya interpretación es desconocida. Esto permite ampliar el formato de tabla de símbolos para agregar nuevos registros auxiliares, sin que se rompa con las herramientas existentes.

#### <a name="symbol-name-representation"></a>Representación de nombre de símbolo

El campo ShortName de una tabla de símbolos consta de 8 bytes que contienen el propio nombre, si no tiene más de 8 bytes de longitud, o el campo ShortName proporciona un desplazamiento en la tabla de cadenas. Para determinar si se ha especificado el propio nombre o un desplazamiento, pruebe los primeros 4 bytes para comprobar si son iguales a cero.

Por convención, los nombres se tratan como cadenas codificadas UTF-8 terminadas en cero.



| Offset        | Size          | Campo                 | Descripción                                                                                                          |
|---------------|---------------|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 8 <br/> | nombreCorto <br/> | Matriz de 8 bytes. Esta matriz se agrega con valores NULL a la derecha si el nombre tiene menos de 8 bytes. <br/> |
| 0 <br/> | 4 <br/> | Ceros <br/>    | Campo que se establece en todos los ceros si el nombre tiene más de 8 bytes. <br/>                                     |
| 4 <br/> | 4 <br/> | Offset <br/>    | Desplazamiento en la tabla de cadenas. <br/>                                                                         |



 

#### <a name="section-number-values"></a>Valores de número de sección

Normalmente, el campo Valor de sección de una entrada de tabla de símbolos es un índice basado en uno en la tabla de secciones. Sin embargo, este campo es un entero con signo y puede tomar valores negativos. Los siguientes valores, menos de uno, tienen significados especiales.



| Constante                          | Value          | Descripción                                                                                                                                                                                                                            |
|-----------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEN \_ SYM \_ UNDEFINED <br/> | 0 <br/>  | El registro de símbolos aún no tiene asignada una sección. Un valor de cero indica que una referencia a un símbolo externo se define en otro lugar. Un valor distinto de cero es un símbolo común con un tamaño especificado por el valor . <br/> |
| IMAGE \_ SYM \_ ABSOLUTE <br/>  | -1 <br/> | El símbolo tiene un valor absoluto (no relocable) y no es una dirección. <br/>                                                                                                                                                  |
| IMAGE \_ SYM \_ DEBUG <br/>     | -2 <br/> | El símbolo proporciona información general de tipo o depuración, pero no corresponde a una sección. Las herramientas de Microsoft usan esta configuración junto con los registros .file (clase de almacenamiento FILE). <br/>                                            |



 

#### <a name="type-representation"></a>Representación de tipo

El campo Tipo de una entrada de tabla de símbolos contiene 2 bytes, donde cada byte representa información de tipo. El LSB representa el tipo de datos simple (base) y el MSB representa el tipo complejo, si lo hay:



| MSB                                                       | LSB                                                        |
|-----------------------------------------------------------|------------------------------------------------------------|
| Tipo complejo: none, pointer, function, array. <br/> | Tipo base: entero, punto flotante, y así sucesivamente. <br/> |



 

Los valores siguientes se definen para el tipo base, aunque las herramientas de Microsoft generalmente no usan este campo y establecen el LSB en 0. En su lugar, Visual C++ información de depuración se usa para indicar tipos. Sin embargo, los posibles valores COFF se enumeran aquí para mayor integridad.



| Constante                             | Value          | Descripción                                                                            |
|--------------------------------------|----------------|----------------------------------------------------------------------------------------|
| IMAGE \_ SYM \_ TYPE \_ NULL <br/>   | 0 <br/>  | Sin información de tipo ni tipo base desconocido. Las herramientas de Microsoft usan esta configuración <br/> |
| IMAGE \_ SYM \_ TYPE \_ VOID <br/>   | 1 <br/>  | No hay ningún tipo válido; se usa con punteros void y funciones <br/>                       |
| IMAGE \_ SYM \_ TYPE \_ CHAR <br/>   | 2 <br/>  | Carácter (byte con signo) <br/>                                                  |
| IMAGE \_ SYM \_ TYPE \_ SHORT <br/>  | 3 <br/>  | Entero de 2 bytes con signo <br/>                                                    |
| IMAGE \_ SYM \_ TYPE \_ INT <br/>    | 4 <br/>  | Tipo entero natural (normalmente 4 bytes en Windows) <br/>                       |
| IMAGE \_ SYM \_ TYPE \_ LONG <br/>   | 5 <br/>  | Entero de 4 bytes con signo <br/>                                                    |
| TIPO \_ DE IMAGEN SYM \_ \_ FLOAT <br/>  | 6 <br/>  | Número de punto flotante de 4 bytes <br/>                                             |
| IMAGE \_ SYM \_ TYPE \_ DOUBLE <br/> | 7 <br/>  | Número de punto flotante de 8 bytes <br/>                                            |
| IMAGE \_ SYM \_ TYPE \_ STRUCT <br/> | 8 <br/>  | Estructura <br/>                                                                |
| IMAGE \_ SYM \_ TYPE \_ UNION <br/>  | 9 <br/>  | Una unión <br/>                                                                    |
| ENUMERACIÓN \_ DE TIPO SYM DE \_ \_ IMAGEN <br/>   | 10 <br/> | Un tipo enumerado <br/>                                                         |
| MOE \_ DE TIPO SYM DE \_ \_ IMAGEN <br/>    | 11 <br/> | Un miembro de enumeración (un valor específico) <br/>                                 |
| BYTE \_ DE TIPO SYM DE \_ \_ IMAGEN <br/>   | 12 <br/> | Un byte; entero de 1 byte sin signo <br/>                                            |
| IMAGE \_ SYM \_ TYPE \_ WORD <br/>   | 13 <br/> | Una palabra; entero de 2 bytes sin signo <br/>                                            |
| IMAGE \_ SYM \_ TYPE \_ UINT <br/>   | 14 <br/> | Entero sin signo de tamaño natural (normalmente, 4 bytes) <br/>                    |
| IMAGE \_ SYM \_ TYPE \_ DWORD <br/>  | 15 <br/> | Entero de 4 bytes sin signo <br/>                                                 |



 

El byte más significativo especifica si el símbolo es un puntero a , una función que devuelve o una matriz del tipo base especificado en el LSB. Las herramientas de Microsoft usan este campo solo para indicar si el símbolo es una función, de modo que los dos únicos valores resultantes 0x0 y 0x20 para el campo Tipo. Sin embargo, otras herramientas pueden usar este campo para comunicar más información.

Es muy importante especificar el atributo de función correctamente. Esta información es necesaria para que la vinculación incremental funcione correctamente. Para algunas arquitecturas, la información puede ser necesaria para otros fines.



| Constante                                | Value         | Descripción                                                          |
|-----------------------------------------|---------------|----------------------------------------------------------------------|
| IMAGE \_ SYM \_ DTYPE \_ NULL <br/>     | 0 <br/> | Ningún tipo derivado; el símbolo es una variable escalar simple. <br/> |
| PUNTERO \_ DE DTYPE DE IMAGEN \_ \_ SYM <br/>  | 1 <br/> | El símbolo es un puntero al tipo base. <br/>                    |
| IMAGE \_ SYM \_ DTYPE \_ (FUNCIÓN) <br/> | 2 <br/> | El símbolo es una función que devuelve un tipo base. <br/>       |
| IMAGE \_ SYM \_ DTYPE \_ ARRAY <br/>    | 3 <br/> | El símbolo es una matriz de tipo base. <br/>                     |



 

#### <a name="storage-class"></a>Clase de almacenamiento

El campo StorageClass de la tabla de símbolos indica qué tipo de definición representa un símbolo. En la tabla siguiente se muestran los valores posibles. Tenga en cuenta que el campo StorageClass es un entero de 1 byte sin signo. Por lo tanto, el valor especial -1 debe considerarse como su equivalente sin signo, 0xFF.

Aunque el formato COFF tradicional usa muchos valores de clase de almacenamiento, las herramientas de Microsoft se basan en el formato de depuración de Visual C++ para la información más simbólica y, por lo general, solo usan cuatro valores de clase de almacenamiento: EXTERNAL (2), STATIC (3), FUNCTION (101) y FILE (103). Excepto en el segundo encabezado de columna siguiente, se debe tomar "Valor" como el campo Valor del registro de símbolos (cuya interpretación depende del número encontrado como clase de almacenamiento).



| Constante                                          | Value                 | Descripción o interpretación del campo Valor                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ SYM \_ CLASS \_ END \_ OF \_ FUNCTION <br/>  | -1 (0xFF) <br/> | Símbolo especial que representa el final de la función, con fines de depuración. <br/>                                                                                                                                                                                                                                                  |
| IMAGE \_ SYM \_ CLASS \_ NULL <br/>               | 0 <br/>         | No hay ninguna clase de almacenamiento asignada. <br/>                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ SYM \_ CLASS \_ AUTOMATIC <br/>          | 1 <br/>         | Variable automática (pila). El campo Valor especifica el desplazamiento del marco de pila. <br/>                                                                                                                                                                                                                                              |
| IMAGE \_ SYM \_ CLASS \_ EXTERNAL <br/>           | 2 <br/>         | Valor que las herramientas de Microsoft usan para los símbolos externos. El campo Valor indica el tamaño si el número de sección es IMAGE \_ SYM \_ UNDEFINED (0). Si el número de sección no es cero, el campo Valor especifica el desplazamiento dentro de la sección. <br/>                                                                                 |
| IMAGE \_ SYM \_ CLASS \_ STATIC <br/>             | 3 <br/>         | Desplazamiento del símbolo dentro de la sección . Si el campo Valor es cero, el símbolo representa un nombre de sección. <br/>                                                                                                                                                                                                            |
| REGISTRO \_ DE CLASE SYM DE \_ \_ IMAGEN <br/>           | 4 <br/>         | Variable de registro. El campo Valor especifica el número de registro. <br/>                                                                                                                                                                                                                                                            |
| IMAGE \_ SYM \_ CLASS \_ EXTERNAL \_ DEF <br/>      | 5 <br/>         | Símbolo que se define externamente. <br/>                                                                                                                                                                                                                                                                                           |
| IMAGE \_ SYM \_ CLASS \_ LABEL <br/>              | 6 <br/>         | Etiqueta de código que se define dentro del módulo. El campo Valor especifica el desplazamiento del símbolo dentro de la sección . <br/>                                                                                                                                                                                                         |
| IMAGE \_ SYM \_ CLASS \_ UNDEFINED \_ LABEL <br/>   | 7 <br/>         | Referencia a una etiqueta de código que no está definida. <br/>                                                                                                                                                                                                                                                                               |
| IMAGE \_ SYM \_ CLASS \_ MEMBER \_ OF \_ STRUCT <br/> | 8 <br/>         | Miembro de estructura. El campo Valor especifica el enésimo miembro. <br/>                                                                                                                                                                                                                                                               |
| IMAGE \_ SYM \_ CLASS \_ ARGUMENT <br/>           | 9 <br/>         | Argumento formal (parámetro) de una función. El campo Valor especifica el n.º argumento. <br/>                                                                                                                                                                                                                                      |
| IMAGE \_ SYM \_ CLASS \_ STRUCT \_ TAG <br/>        | 10 <br/>        | Entrada de nombre de etiqueta de estructura. <br/>                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ SYM \_ CLASS \_ MEMBER \_ OF \_ UNION <br/>  | 11 <br/>        | Miembro de unión. El campo Valor especifica el enésimo miembro. <br/>                                                                                                                                                                                                                                                                     |
| IMAGE \_ SYM \_ CLASS \_ UNION \_ TAG <br/>         | 12 <br/>        | Entrada Nombre de etiqueta Union. <br/>                                                                                                                                                                                                                                                                                                      |
| DEFINICIÓN \_ DE TIPO DE CLASE SYM DE \_ \_ \_ IMAGEN <br/>   | 13 <br/>        | Entrada Typedef. <br/>                                                                                                                                                                                                                                                                                                               |
| IMAGE \_ SYM \_ CLASS \_ UNDEFINED \_ STATIC <br/>  | 14 <br/>        | Declaración de datos estáticos. <br/>                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ SYM \_ CLASS \_ ENUM \_ TAG <br/>          | 15 <br/>        | Entrada enumerada de nombre de etiqueta de tipo. <br/>                                                                                                                                                                                                                                                                                              |
| IMAGE \_ SYM \_ CLASS \_ MEMBER \_ OF \_ ENUM <br/>   | 16 <br/>        | Miembro de una enumeración. El campo Valor especifica el nº miembro. <br/>                                                                                                                                                                                                                                                         |
| IMAGE \_ SYM \_ CLASS \_ REGISTER \_ PARAM <br/>    | 17 <br/>        | Parámetro de registro. <br/>                                                                                                                                                                                                                                                                                                          |
| CAMPO \_ DE BITS IMAGE SYM \_ CLASS \_ \_ <br/>         | 18 <br/>        | Referencia de campo de bits. El campo Valor especifica el n.º bit del campo de bits. <br/>                                                                                                                                                                                                                                                |
| BLOQUE \_ DE CLASE SYM DE \_ \_ IMAGEN <br/>              | 100 <br/>       | Un registro .bb (principio del bloque) o .eb (final del bloque). El campo Valor es la dirección relocatable de la ubicación del código. <br/>                                                                                                                                                                                                      |
| IMAGE \_ SYM \_ CLASS \_ (FUNCIÓN) <br/>           | 101 <br/>       | Valor que las herramientas de Microsoft usan para los registros de símbolos que definen la extensión de una función: begin function (.bf), end function ( .ef ) y lines in function ( .lf ). Para los registros .lf, el campo Valor proporciona el número de líneas de origen de la función. Para los registros .ef, el campo Valor proporciona el tamaño del código de función. <br/> |
| IMAGE \_ SYM \_ CLASS \_ END \_ OF \_ STRUCT <br/>    | 102 <br/>       | Entrada de fin de estructura. <br/>                                                                                                                                                                                                                                                                                                     |
| ARCHIVO \_ DE CLASE SYM DE \_ \_ IMAGEN <br/>               | 103 <br/>       | Valor que las herramientas de Microsoft, así como el formato COFF tradicional, usan para el registro de símbolos de archivo de origen. El símbolo va seguido de registros auxiliares que nombren el archivo. <br/>                                                                                                                                                       |
| SECCIÓN \_ IMAGE SYM \_ CLASS \_ <br/>            | 104 <br/>       | Definición de una sección (las herramientas de Microsoft usan la clase de almacenamiento STATIC en su lugar). <br/>                                                                                                                                                                                                                                                  |
| IMAGE \_ SYM \_ CLASS \_ WEAK \_ EXTERNAL <br/>     | 105 <br/>       | Externo débil. Para obtener más información, [vea Formato auxiliar 3: Externos débiles.](#auxiliary-format-3-weak-externals) <br/>                                                                                                                                                                                                           |
| TOKEN \_ CLR DE IMAGE SYM \_ CLASS \_ \_ <br/>         | 107 <br/>       | Símbolo de token CLR. El nombre es una cadena ASCII que consta del valor hexadecimal del token. Para obtener más información, vea [Definición de token CLR (solo objeto).](#clr-token-definition-object-only) <br/>                                                                                                                        |



 

### <a name="auxiliary-symbol-records"></a>Registros de símbolos auxiliares

Los registros de tabla de símbolos auxiliares siempre siguen y aplican a algún registro de tabla de símbolos estándar. Un registro auxiliar puede tener cualquier formato que las herramientas puedan reconocer, pero se deben asignar 18 bytes para que la tabla de símbolos se mantenga como una matriz de tamaño normal. Actualmente, las herramientas de Microsoft reconocen formatos auxiliares para los siguientes tipos de registros: definiciones de función, símbolos de inicio y fin de función (.bf y .ef), externos débiles, nombres de archivo y definiciones de sección.

El diseño COFF tradicional también incluye formatos de registro auxiliar para matrices y estructuras. Las herramientas de Microsoft no las usan, sino que coloca esa información simbólica en Visual C++ de depuración en las secciones de depuración.

#### <a name="auxiliary-format-1-function-definitions"></a>Formato auxiliar 1: definiciones de función

Un registro de tabla de símbolos marca el principio de una definición de función si tiene todo lo siguiente: una clase de almacenamiento de EXTERNAL (2), un valor type que indica que es una función (0x20) y un número de sección mayor que cero. Tenga en cuenta que un registro de tabla de símbolos que tiene un número de sección de UNDEFINED (0) no define la función y no tiene un registro auxiliar. Los registros de símbolos de definición de función van seguidos de un registro auxiliar en el formato descrito a continuación:



| Offset         | Size          | Campo                             | Descripción                                                                                                                                                                                                                   |
|----------------|---------------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | TagIndex <br/>              | Índice de tabla de símbolos del registro de símbolos .bf (función begin) correspondiente. <br/>                                                                                                                                   |
| 4 <br/>  | 4 <br/> | TotalSize <br/>             | Tamaño del código ejecutable para la propia función. Si la función está en su propia sección, sizeOfRawData en el encabezado de sección es mayor o igual que este campo, en función de las consideraciones de alineación. <br/> |
| 8 <br/>  | 4 <br/> | PointerToLinenumber <br/>   | Desplazamiento de archivo de la primera entrada de número de línea COFF para la función o cero si no existe ninguno. Para obtener más información, vea [Números de línea COFF (en desuso).](#coff-line-numbers-deprecated) <br/>                          |
| 12 <br/> | 4 <br/> | PointerToNextFunction <br/> | Índice de tabla de símbolos del registro para la función siguiente. Si la función es la última de la tabla de símbolos, este campo se establece en cero. <br/>                                                                           |
| 16 <br/> | 2 <br/> | No utilizado <br/>                |                                                                                                                                                                                                                               |



 

#### <a name="auxiliary-format-2-bf-and-ef-symbols"></a>Formato auxiliar 2: símbolos .bf y .ef

Para cada definición de función de la tabla de símbolos, tres elementos describen el principio, el final y el número de líneas. Cada uno de estos símbolos tiene la clase de almacenamiento FUNCTION (101):

Un registro de símbolos denominado .bf (función begin). El campo Valor no se usa.

Un registro de símbolos denominado .lf (líneas en la función). El campo Valor proporciona el número de líneas de la función.

Un registro de símbolos denominado .ef (final de la función). El campo Valor tiene el mismo número que el campo Tamaño total del registro de símbolos de definición de función.

Los registros de símbolos .bf y .ef (pero no los registros .lf) van seguidos de un registro auxiliar con el formato siguiente:



| Offset         | Size          | Campo                                         | Descripción                                                                                                                                                                   |
|----------------|---------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | No utilizado <br/>                            |                                                                                                                                                                               |
| 4 <br/>  | 2 <br/> | Número de línea <br/>                        | Número de línea ordinal real (1, 2, 3, y así sucesivamente) dentro del archivo de origen, correspondiente al registro .bf o .ef. <br/>                                               |
| 6 <br/>  | 6 <br/> | No utilizado <br/>                            |                                                                                                                                                                               |
| 12 <br/> | 4 <br/> | PointerToNextFunction ( solo .bf) <br/> | Índice de tabla de símbolos del siguiente registro de símbolos .bf. Si la función es la última de la tabla de símbolos, este campo se establece en cero. No se usa para los registros .ef. <br/> |
| 16 <br/> | 2 <br/> | No utilizado <br/>                            |                                                                                                                                                                               |



 

#### <a name="auxiliary-format-3-weak-externals"></a>Formato auxiliar 3: externos débiles

Los "externos débiles" son un mecanismo para los archivos de objeto que permite flexibilidad en el momento del vínculo. Un módulo puede contener un símbolo externo sin resolver (sym1), pero también puede incluir un registro auxiliar que indica que si sym1 no está presente en el momento del vínculo, se usa otro símbolo externo (sym2) para resolver las referencias en su lugar.

Si se vincula una definición de sym1, se resuelve normalmente una referencia externa al símbolo. Si una definición de sym1 no está vinculada, todas las referencias al externo débil para sym1 hacen referencia a sym2 en su lugar. El símbolo externo, sym2, siempre debe estar vinculado; normalmente, se define en el módulo que contiene la referencia débil a sym1.

Los externos débiles se representan mediante un registro de tabla de símbolos con la clase de almacenamiento EXTERNAL, el número de sección UNDEF y un valor de cero. El registro de símbolos débiles y externos va seguido de un registro auxiliar con el formato siguiente:



| Offset        | Size           | Campo                       | Descripción                                                                                                                                                                                                                                                                                                                                                |
|---------------|----------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>  | TagIndex <br/>        | Índice de la tabla de símbolos de sym2, el símbolo que se va a vincular si no se encuentra sym1. <br/>                                                                                                                                                                                                                                                                  |
| 4 <br/> | 4 <br/>  | Características <br/> | Un valor de IMAGE WEAK EXTERN SEARCH NOLIBRARY indica que no se debe realizar ninguna búsqueda de \_ \_ biblioteca para \_ \_ sym1. <br/> Un valor de IMAGE WEAK EXTERN SEARCH LIBRARY indica que se debe realizar una búsqueda de biblioteca para \_ \_ \_ \_ sym1. <br/> Un valor de IMAGE \_ WEAK \_ EXTERN \_ SEARCH ALIAS indica \_ que sym1 es un alias para sym2. <br/> |
| 8 <br/> | 10 <br/> | No utilizado <br/>          |                                                                                                                                                                                                                                                                                                                                                            |



 

Tenga en cuenta que el campo Características no está definido en WINNT. H; en su lugar, se usa el campo Tamaño total.

#### <a name="auxiliary-format-4-files"></a>Formato auxiliar 4: Archivos

Este formato sigue un registro de tabla de símbolos con la clase de almacenamiento FILE (103). El propio nombre de símbolo debe ser .file y el registro auxiliar que sigue le da el nombre de un archivo de código fuente.



| Offset        | Size           | Campo                 | Descripción                                                                                                                         |
|---------------|----------------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 18 <br/> | Nombre de archivo <br/> | Cadena ANSI que proporciona el nombre del archivo de origen. Se agrega con valores NULL si es menor que la longitud máxima. <br/> |



 

#### <a name="auxiliary-format-5-section-definitions"></a>Formato auxiliar 5: definiciones de sección

Este formato sigue un registro de tabla de símbolos que define una sección. Este registro tiene un nombre de símbolo que es el nombre de una sección (como .text o .drectve) y tiene la clase de almacenamiento STATIC (3). El registro auxiliar proporciona información sobre la sección a la que hace referencia. Por lo tanto, duplica parte de la información del encabezado de sección.



| Offset         | Size          | Campo                           | Descripción                                                                                                                                                                                                             |
|----------------|---------------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Length <br/>              | Tamaño de los datos de sección; igual que SizeOfRawData en el encabezado de sección. <br/>                                                                                                                                  |
| 4 <br/>  | 2 <br/> | NumberOfRelocations <br/> | Número de entradas de reubicación de la sección. <br/>                                                                                                                                                           |
| 6 <br/>  | 2 <br/> | NumberOfLinenumbers <br/> | Número de entradas de número de línea de la sección. <br/>                                                                                                                                                          |
| 8 <br/>  | 4 <br/> | Checksum <br/>            | Suma de comprobación para los datos de la comunidad. Es aplicable si la marca IMAGE \_ SCN \_ LNK \_ COMDAT está establecida en el encabezado de sección. Para obtener más información, [vea SECCIONES COMDAT (solo objetos).](#comdat-sections-object-only) <br/> |
| 12 <br/> | 2 <br/> | Number <br/>              | Índice basado en uno en la tabla de secciones de la sección asociada. Se usa cuando la configuración de selección de COMDAT es 5. <br/>                                                                                     |
| 14 <br/> | 1 <br/> | Número de selección <br/>           | Número de selección de COMDAT. Esto es aplicable si la sección es una sección COMDAT. <br/>                                                                                                                         |
| 15 <br/> | 3 <br/> | No utilizado <br/>              |                                                                                                                                                                                                                         |



 

#### <a name="comdat-sections-object-only"></a>Secciones COMDAT (solo objeto)

El campo Selección del formato auxiliar de definición de sección es aplicable si la sección es una sección COMDAT. Una sección COMDAT es una sección que se puede definir mediante más de un archivo de objeto. (La marca IMAGE \_ SCN \_ LNK \_ COMDAT se establece en el campo Marcas de sección del encabezado de sección). El campo Selección determina la manera en que el vinculador resuelve las varias definiciones de las secciones COMDAT.

El primer símbolo que tiene el valor de sección de la sección COMDAT debe ser el símbolo de sección. Este símbolo tiene el nombre de la sección, el campo Valor igual a cero, el número de sección de la sección COMDAT en cuestión, el campo Tipo igual a IMAGE SYM TYPE NULL, el campo Clase igual a IMAGE SYM CLASS STATIC y un registro \_ \_ \_ \_ \_ \_ auxiliar. El segundo símbolo se denomina "símbolo COMDAT" y lo usa el vinculador junto con el campo Selección.

A continuación se muestran los valores del campo Selección.



| Constante                                        | Value         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ COMDAT \_ SELECT \_ NODUPLICATES <br/> | 1 <br/> | Si este símbolo ya está definido, el vinculador emite un error de "multiplicar el símbolo definido". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ COMDAT \_ SELECT \_ ANY <br/>          | 2 <br/> | Se puede vincular cualquier sección que defina el mismo símbolo COMDAT; se quitan el resto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGE \_ COMDAT \_ SELECT \_ SAME \_ SIZE <br/>   | 3 <br/> | El vinculador elige una sección arbitraria entre las definiciones de este símbolo. Si todas las definiciones no tienen el mismo tamaño, se genera un error de "multiplicar símbolo definido". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ COMDAT \_ SELECT \_ EXACT \_ MATCH <br/> | 4 <br/> | El vinculador elige una sección arbitraria entre las definiciones de este símbolo. Si todas las definiciones no coinciden exactamente, se genera un error de "multiplicar el símbolo definido". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGE \_ COMDAT \_ SELECT \_ ASSOCIATIVE <br/>  | 5 <br/> | La sección se vincula si hay otra sección COMDAT vinculada. Esta otra sección se indica mediante el campo Número del registro de símbolos auxiliares para la definición de sección. Esta configuración es útil para las definiciones que tienen componentes en varias secciones (por ejemplo, código en una y datos en otra), pero donde todos deben vincularse o descartarse como un conjunto. La otra sección a la que está asociada esta sección debe ser una sección COMDAT, que puede ser otra sección asociativa de COMDAT. La cadena de asociación de secciones de una sección de COMDAT asociativa no puede formar un bucle. La cadena de asociación de secciones debe llegar finalmente a una sección COMDAT que no tenga establecido IMAGE \_ COMDAT \_ SELECT \_ ASSOCIATIVE. <br/> |
| IMAGE \_ COMDAT \_ SELECT \_ LARGEST <br/>      | 6 <br/> | El vinculador elige la definición más grande entre todas las definiciones de este símbolo. Si varias definiciones tienen este tamaño, la elección entre ellas es arbitraria. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

#### <a name="clr-token-definition-object-only"></a>Definición de token CLR (solo objeto)

Este símbolo auxiliar suele seguir el TOKEN CLR DE IMAGE \_ SYM \_ \_ \_ CLASS. Se usa para asociar un token al espacio de nombres de la tabla de símbolos COFF.



| Offset        | Size           | Campo                        | Descripción                                                                                |
|---------------|----------------|------------------------------|--------------------------------------------------------------------------------------------|
| 0 <br/> | 1 <br/>  | bTypeType <br/>         | Debe ser IMAGE \_ AUX SYMBOL TYPE TOKEN \_ \_ \_ \_ DEF (1). <br/>                              |
| 1 <br/> | 1 <br/>  | bReserved <br/>        | Reservado, debe ser cero. <br/>                                                        |
| 2 <br/> | 4 <br/>  | SymbolTableIndex <br/> | Índice de símbolos del símbolo COFF al que hace referencia esta definición de token CLR. <br/> |
| 6 <br/> | 12 <br/> |                              | Reservado, debe ser cero. <br/>                                                        |



 

### <a name="coff-string-table"></a>Tabla de cadenas COFF

Inmediatamente después de la tabla de símbolos COFF se encuentra la tabla de cadenas COFF. La posición de esta tabla se encuentra tomando la dirección de la tabla de símbolos en el encabezado COFF y agregando el número de símbolos multiplicado por el tamaño de un símbolo.

Al principio de la tabla de cadenas COFF hay 4 bytes que contienen el tamaño total (en bytes) del resto de la tabla de cadenas. Este tamaño incluye el propio campo de tamaño, por lo que el valor de esta ubicación sería 4 si no hubiera ninguna cadena presente.

Después del tamaño, hay cadenas terminadas en NULL a las que apuntan los símbolos de la tabla de símbolos COFF.

### <a name="the-attribute-certificate-table-image-only"></a>Tabla de certificados de atributo (solo imagen)

Los certificados de atributo se pueden asociar a una imagen agregando una tabla de certificados de atributo. La tabla de certificados de atributo se compone de un conjunto de entradas de certificado de atributos contiguos alineados con cuatro palabras. El relleno cero se inserta entre el final original del archivo y el principio de la tabla de certificados de atributo para lograr esta alineación. Cada entrada de certificado de atributo contiene los campos siguientes.



| Offset       | Size                         | Campo                       | Descripción                                                                                                |
|--------------|------------------------------|-----------------------------|------------------------------------------------------------------------------------------------------------|
| 0<br/> | 4<br/>                 | dwLength<br/>         | Especifica la longitud de la entrada del certificado de atributo. <br/>                                       |
| 4<br/> | 2<br/>                 | wRevision<br/>        | Contiene el número de versión del certificado. Para obtener más información, vea el texto siguiente.<br/>                   |
| 6<br/> | 2<br/>                 | wCertificateType<br/> | Especifica el tipo de contenido en bCertificate. Para obtener más información, vea el texto siguiente.<br/>             |
| 8<br/> | Consulte<br/> | bCertificate<br/>     | Contiene un certificado, como una firma Authenticode. Para obtener más información, vea el texto siguiente.<br/> |



 

El valor de dirección virtual de la entrada Tabla de certificados del directorio de datos de encabezado opcional es un desplazamiento de archivo con respecto a la primera entrada de certificado de atributo. Se accede a las entradas posteriores avanzando los bytes dwLength de esa entrada, redondeados hasta un múltiplo de 8 bytes, desde el inicio de la entrada del certificado de atributo actual. Esto continúa hasta que la suma de los valores dwLength redondeados es igual al valor Tamaño de la entrada Tabla de certificados del directorio de datos de encabezado opcional. Si la suma de los valores dwLength redondeados no es igual al valor Size, la tabla de certificados de atributo o el campo Size están dañados.

Por ejemplo, si la entrada de tabla de certificados del directorio de datos de encabezado opcional contiene:


```C++
virtual address = 0x5000
size = 0x1000
```



El primer certificado se inicia en el 0x5000 desde el inicio del archivo en disco. Para avanzar por todas las entradas del certificado de atributo:

1.  Agregue el primer valor dwLength del certificado de atributo al desplazamiento inicial.
2.  Redondee el valor del paso 1 al múltiplo de 8 bytes más cercano para buscar el desplazamiento de la segunda entrada de certificado de atributo.
3.  Agregue el valor de desplazamiento del paso 2 al valor dwLength de la segunda entrada de certificado de atributo y redondee al múltiplo de 8 bytes más cercano para determinar el desplazamiento de la tercera entrada de certificado de atributo.
4.  Repita el paso 3 para cada certificado sucesivo hasta que el desplazamiento calculado sea igual 0x6000 (0x5000 inicio + 0x1000 tamaño total), lo que indica que ha recorrido toda la tabla.

Como alternativa, puede enumerar las entradas del certificado llamando a la función **ImageEnumerateCertificates** de Win32 en un bucle. Para obtener un vínculo a la página de referencia de la función, vea [Referencias](#references)a .

Las entradas de la tabla de certificados de atributo pueden contener cualquier tipo de certificado, siempre y cuando la entrada tenga el valor dwLength correcto, un valor wRevision único y un valor wCertificateType único. El tipo más común de entrada de tabla de certificados es una estructura WIN CERTIFICATE, que se documenta en Wintrust.h y se describe en el resto \_ de esta sección.

Las opciones para el miembro \_ **wRevision** de WIN CERTIFICATE incluyen (pero no se limitan a) lo siguiente.



| Value             | Nombre                                 | Notas                                                                                                                                                 |
|-------------------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0100<br/> | WIN \_ CERT \_ REVISION \_ 1 \_ 0<br/> | Versión 1, versión heredada de la estructura win \_ certificate. Solo se admite con fines de comprobación de firmas authenticode heredadas<br/> |
| 0x0200<br/> | WIN \_ CERT \_ REVISION \_ 2 \_ 0<br/> | La versión 2 es la versión actual de la estructura \_ de certificados Win. <br/>                                                                       |



 

Las opciones para el miembro \_ **wCertificateType de** WIN CERTIFICATE incluyen (pero no se limitan a) los elementos de la tabla siguiente. Tenga en cuenta que algunos valores no se admiten actualmente.



| Value             | Nombre                                           | Notas                                                                                   |
|-------------------|------------------------------------------------|-----------------------------------------------------------------------------------------|
| 0x0001<br/> | TIPO \_ DE CERTIFICADO WIN \_ \_ X509 <br/>              | bCertificate contiene un certificado X.509 <br/> No compatible<br/>         |
| 0x0002<br/> | DATOS \_ FIRMADOS \_ DE \_ PKCS DEL TIPO \_ DE CERTIFICADO \_ WIN<br/> | bCertificate contiene una estructura SignedData de PKCS \# 7<br/>                         |
| 0x0003<br/> | TIPO \_ DE CERTIFICADO WIN RESERVADO \_ \_ \_ 1<br/>        | Reservada <br/>                                                                    |
| 0x0004<br/> | WIN \_ CERT \_ TYPE \_ TS \_ STACK \_ SIGNED<br/>  | Firma de certificados de pila de protocolos de Terminal Server <br/> No compatible<br/> |



 

El miembro bCertificate de la estructura WIN CERTIFICATE contiene una matriz de bytes de longitud variable con el tipo de contenido \_ especificado por **wCertificateType**.  El tipo admitido por Authenticode es WIN \_ CERT \_ TYPE \_ PKCS SIGNED \_ \_ DATA, una estructura SignedData de PKCS \# 7.  Para obtener más información sobre el formato de firma digital Authenticode, vea Windows Formato de firma ejecutable portable [de Authenticode](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx).

Si el **contenido de bCertificate** no termina en un límite de cuatro palabras, la entrada del certificado de atributo se agrega con ceros, desde el final de **bCertificate** hasta el siguiente límite de cuatro palabras.

El **valor dwLength** es la longitud de la estructura WIN \_ CERTIFICATE finalizada y se calcula como:

`dwLength = offsetof(WIN_CERTIFICATE, bCertificate) + (size of the variable-length binary array contained within bCertificate)`

Esta longitud debe incluir el tamaño de cualquier relleno que se utilice para satisfacer el requisito de que cada estructura de WIN CERTIFICATE esté \_ alineada con cuatro palabras:

` dwLength += (8 - (dwLength & 7)) & 7;`

El **tamaño de la tabla de** certificados (especificado en la entrada Tabla de certificados en los **directorios** de datos de encabezado [opcionales (solo imagen)](#optional-header-data-directories-image-only)incluye el relleno.

Para obtener más información sobre el uso de la API ImageHlp para enumerar, agregar y quitar certificados de archivos PE, vea [ImageHlp Functions](imagehlp-functions.md).

#### <a name="certificate-data"></a>Datos de certificado

Como se indicó en la sección anterior, los certificados de la tabla de certificados de atributo pueden contener cualquier tipo de certificado. Los certificados que garantizan la integridad de un archivo PE pueden incluir un hash de imagen pe.

Un hash de imagen pe (o hash de archivo) es similar a una suma de comprobación de archivo en que el algoritmo hash genera un resumen del mensaje relacionado con la integridad de un archivo. Sin embargo, un algoritmo simple genera una suma de comprobación y se usa principalmente para detectar si un bloque de memoria en el disco ha ido mal y los valores almacenados allí se han dañado. Un hash de archivo es similar a una suma de comprobación en que también detecta daños en los archivos. Sin embargo, a diferencia de la mayoría de los algoritmos de suma de comprobación, es muy difícil modificar un archivo sin cambiar el hash de archivo de su valor original sin modificar. Por lo tanto, se puede usar un hash de archivo para detectar modificaciones intencionadas e incluso sutiles en un archivo, como las introducidas por virus, hackers o programas de troyanos.

Cuando se incluye en un certificado, el resumen de la imagen debe excluir determinados campos de la imagen de PE, como la suma de comprobación y la entrada de la tabla de certificados en directorios de datos de encabezado opcionales. Esto se debe a que el acto de agregar un certificado cambia estos campos y haría que se calculara un valor hash diferente.

La función **ImageGetDigestStream** de Win32 proporciona un flujo de datos desde un archivo PE de destino con el que se aplica hash a las funciones. Este flujo de datos sigue siendo coherente cuando se agregan o quitan certificados de un archivo PE. En función de los parámetros que se pasan a **ImageGetDigestStream,** se pueden omitir otros datos de la imagen PE del cálculo hash. Para obtener un vínculo a la página de referencia de la función, vea [Referencias](#references).

### <a name="delay-load-import-tables-image-only"></a>Delay-Load importar tablas (solo imagen)

Estas tablas se agregaron a la imagen para admitir un mecanismo uniforme para que las aplicaciones retrasen la carga de un archivo DLL hasta la primera llamada a ese archivo DLL. El diseño de las tablas coincide con el de las tablas de importación tradicionales que se describen en la sección 6.4, [Sección .idata."](#the-idata-section) Aquí solo se analizan algunos detalles.

#### <a name="the-delay-load-directory-table"></a>La tabla Delay-Load directory

La tabla de directorios de carga retrasada es la equivalente a la tabla de directorios de importación. Se puede recuperar a través de la entrada Descriptor de importación retrasada en la lista de directorios de datos de encabezado opcional (desplazamiento 200). La tabla se organiza de la siguiente manera:



| Offset         | Size          | Campo                                  | Descripción                                                                                                                                                                                                                                                                                                                  |
|----------------|---------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Atributos <br/>                 | Debe ser cero. <br/>                                                                                                                                                                                                                                                                                                    |
| 4 <br/>  | 4 <br/> | Nombre <br/>                       | RVA del nombre del archivo DLL que se va a cargar. El nombre reside en la sección de datos de solo lectura de la imagen. <br/>                                                                                                                                                                                                        |
| 8 <br/>  | 4 <br/> | Identificador del módulo <br/>              | El RVA del identificador del módulo (en la sección de datos de la imagen) del archivo DLL que se va a cargar con retraso. Se usa para el almacenamiento mediante la rutina que se proporciona para administrar la carga retrasada. <br/>                                                                                                                                   |
| 12 <br/> | 4 <br/> | Retrasar la importación de la tabla de direcciones <br/> | El RVA de la tabla de direcciones de importación de carga retrasada. Para obtener más información, vea [Retrasar la importación de la tabla de direcciones (IAT).](#delay-import-address-table) <br/>                                                                                                                                                                       |
| 16 <br/> | 4 <br/> | Retrasar la tabla de nombres de importación <br/>    | El RVA de la tabla de nombres de carga retrasada, que contiene los nombres de las importaciones que podrían tener que cargarse. Esto coincide con el diseño de la tabla de nombres de importación. Para obtener más información, vea [Hint/Name Table](#hintname-table).<br/>                                                                                       |
| 20 <br/> | 4 <br/> | Tabla de importación de retraso enlazada <br/>   | RVA de la tabla de direcciones de carga retrasada enlazada, si existe. <br/>                                                                                                                                                                                                                                                     |
| 24 <br/> | 4 <br/> | Descargar tabla de importación retrasada <br/>  | El RVA de la tabla de direcciones de carga retrasada de descarga, si existe. Se trata de una copia exacta de la tabla de direcciones de importación retrasada. Si el autor de la llamada descarga el archivo DLL, esta tabla se debe volver a copiar en la tabla de direcciones de importación retrasada para que las llamadas posteriores al archivo DLL sigan usando correctamente el mecanismo thunking. <br/> |
| 28 <br/> | 4 <br/> | Marca de tiempo <br/>                 | Marca de tiempo del archivo DLL al que se ha enlazado esta imagen. <br/>                                                                                                                                                                                                                                                     |



 

Las tablas a las que se hace referencia en esta estructura de datos se organizan y ordenan igual que sus homólogos para las importaciones tradicionales. Para obtener más información, [vea la sección .idata](#the-idata-section).

#### <a name="attributes"></a>Atributos

Por el momento, no se ha definido ninguna marca de atributo. El vinculador establece este campo en cero en la imagen. Este campo se puede usar para extender el registro indicando la presencia de nuevos campos, o se puede usar para indicar comportamientos de las funciones auxiliares de retraso o descarga.

#### <a name="name"></a>Nombre

El nombre del archivo DLL que se va a cargar con retraso reside en la sección de datos de solo lectura de la imagen. Se hace referencia a él a través del campo szName.

#### <a name="module-handle"></a>Identificador de módulo

El identificador del archivo DLL que se va a cargar con retraso se encuentra en la sección de datos de la imagen. El campo phmod apunta al identificador. El asistente de carga retrasada proporcionado usa esta ubicación para almacenar el identificador en el archivo DLL cargado.

#### <a name="delay-import-address-table"></a>Tabla de direcciones de importación retrasada

El descriptor de importación retrasada hace referencia a la tabla de direcciones de importación retrasada (IAT) a través del campo pIAT. El asistente de carga retrasada actualiza estos punteros con los puntos de entrada reales para que los thunks ya no estén en el bucle de llamada. Se tiene acceso a los punteros de función mediante la expresión `pINT->u1.Function` .

#### <a name="delay-import-name-table"></a>Tabla de nombres de importación retrasada

La tabla de nombres de importación retrasada (INT) contiene los nombres de las importaciones que pueden requerir carga. Se ordenan de la misma manera que los punteros de función en el IAT. Constan de las mismas estructuras que el int estándar y se accede a ellas mediante la expresión `pINT->u1.AddressOfData->Name[0]` .

#### <a name="delay-bound-import-address-table-and-time-stamp"></a>Tabla de direcciones de importación enlazadas con retraso y marca de tiempo

La tabla de direcciones de importación enlazadas con retraso (BIAT) es una tabla opcional de elementos IMAGE THUNK DATA que se usa junto con el campo timestamp de la tabla de \_ directorios delay-load en una fase de enlace posterior \_ al proceso.

#### <a name="delay-unload-import-address-table"></a>Tabla de direcciones de importación de descarga retrasada

La tabla de direcciones de importación de descarga retrasada (UIAT) es una tabla opcional de elementos IMAGE THUNK DATA que el código de descarga usa para controlar \_ una solicitud de descarga \_ explícita. Consta de datos inicializados en la sección de solo lectura que es una copia exacta del IAT original que hizo referencia al código a los thunks de carga retrasada. En la solicitud de descarga, se puede liberar la biblioteca, borrar phmod y escribir el UIAT sobre el IAT para restaurar todo a su \* estado de precarga.

## <a name="special-sections"></a>Secciones especiales

- [Sección .debug](#the-debug-section)
  - [Directorio de depuración (solo imagen)](#debug-directory-image-only)
  - [Tipo de depuración](#debug-type)
  - [.debug$F (solo objeto)](#debugf-object-only)
  - [.debug$S (solo objeto)](#debugs-object-only)
  - [.debug$P (solo objeto)](#debugp-object-only)
  - [.debug$T (solo objeto)](#debugt-object-only)
  - [Compatibilidad del vinculador con la información de depuración de Microsoft](#linker-support-for-microsoft-debug-information)
- [La sección .drectve (solo objeto)](#the-drectve-section-object-only)
- [Sección .edata (solo imagen)](#the-edata-section-image-only)
  - [Exportar tabla de directorios](#export-directory-table)
  - [Exportar tabla de direcciones](#export-address-table)
  - [Exportar tabla de punteros de nombre](#export-name-pointer-table)
  - [Exportar tabla ordinal](#export-ordinal-table)
  - [Exportar tabla de nombres](#export-name-table)
- [Sección .idata](#the-idata-section)
  - [Importar tabla de directorios](#import-directory-table)
  - [Importar tabla de búsqueda](#import-lookup-table)
  - [Tabla de sugerencias y nombres](#hintname-table)
  - [Importar tabla de direcciones](#delay-import-address-table)
- [Sección .pdata](#the-pdata-section)
- [Sección .reloc (solo imagen)](#the-reloc-section-image-only)
  - [Bloque de reubicación base](#base-relocation-block)
  - [Tipos de reubicación base](#base-relocation-types)
- [La sección .tls](#the-tls-section)
  - [El directorio TLS](#the-tls-directory)
  - [Funciones de devolución de llamada TLS](#tls-callback-functions)
- [Estructura de configuración de carga (solo imagen)](#the-load-configuration-structure-image-only)
  - [Cargar directorio de configuración](#load-configuration-directory)
  - [Diseño de configuración de carga](#load-configuration-layout)
- [Sección .rsrc](#the-rsrc-section)
  - [Tabla de directorios de recursos](#resource-directory-table)
  - [Entradas del directorio de recursos](#resource-directory-entries)
  - [Cadena de directorio de recursos](#resource-directory-string)
  - [Entrada de datos de recursos](#resource-data-entry)
- [La sección .cormeta (solo objeto)](#the-cormeta-section-object-only)
- [Sección .sxdata](#the-sxdata-section)

Las secciones COFF típicas contienen código o datos que los vinculadores y los cargadores de Microsoft Win32 procesan sin conocimientos especiales del contenido de la sección. El contenido solo es relevante para la aplicación que se está vinculando o ejecutando.

Sin embargo, algunas secciones de COFF tienen significados especiales cuando se encuentran en archivos de objeto o archivos de imagen. Las herramientas y los cargadores reconocen estas secciones porque tienen marcas especiales establecidas en el encabezado de sección, porque las ubicaciones especiales en el encabezado opcional de la imagen apuntan a ellas, o porque el propio nombre de sección indica una función especial de la sección. (Incluso si el propio nombre de sección no indica una función especial de la sección, el nombre de la sección se dicta por convención, por lo que los autores de esta especificación pueden hacer referencia a un nombre de sección en todos los casos).

Las secciones reservadas y sus atributos se describen en la tabla siguiente, seguidas de descripciones detalladas de los tipos de sección que se conservan en archivos ejecutables y los tipos de sección que contienen metadatos para las extensiones.



| Nombre de sección          | Contenido                                                                                                                                                                  | Características                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .bss <br/>      | Datos sin inicializar (formato libre) <br/>                                                                                                                             | IMAGE \_ SCN \_ CNT \_ UNINITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                               |
| .cormeta <br/>  | Metadatos CLR que indican que el archivo de objeto contiene código administrado <br/>                                                                                       | INFORMACIÓN \_ DE LNK de SCN \_ \_ DE IMAGEN <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .data <br/>     | Datos inicializados (formato libre) <br/>                                                                                                                               | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .debug$F <br/>  | Información de depuración de FPO generada (solo objeto, solo arquitectura x86 y ahora obsoleta) <br/>                                                                       | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .debug$P <br/>  | Tipos de depuración precompilados (solo objeto) <br/>                                                                                                                        | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .debug$S <br/>  | Símbolos de depuración (solo objeto) <br/>                                                                                                                                  | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .debug$T <br/>  | Tipos de depuración (solo objeto) <br/>                                                                                                                                    | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .drective <br/> | Opciones del enlazador <br/>                                                                                                                                               | INFORMACIÓN \_ DE LNK de SCN \_ \_ DE IMAGEN <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .edata <br/>    | Exportación de tablas <br/>                                                                                                                                                | IMAGEN \_ SCN \_ CNT \_ INITIALIZED \_ DATA IMAGE \| \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| .idata <br/>    | Importación de tablas <br/>                                                                                                                                                | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .idlsym <br/>   | Incluye seh registrado (solo imagen) para admitir atributos IDL. Para obtener información, vea "Atributos de IDL" en [Referencias](#references) al final de este tema. <br/> | INFORMACIÓN \_ DE LNK de SCN \_ \_ DE IMAGEN <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .pdata <br/>    | Información de la excepción <br/>                                                                                                                                        | IMAGEN \_ SCN \_ CNT \_ INITIALIZED \_ DATA IMAGE \| \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| .rdata <br/>    | Datos inicializados de solo lectura <br/>                                                                                                                                   | IMAGEN \_ SCN \_ CNT \_ INITIALIZED \_ DATA IMAGE \| \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| .reloc <br/>    | Reubicaciones de imágenes <br/>                                                                                                                                            | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .rsrc <br/>     | Directorio de recursos <br/>                                                                                                                                           | IMAGEN \_ SCN \_ CNT \_ INITIALIZED \_ DATA IMAGE \| \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| .sbss <br/>     | Datos no inicializados relativos a GP (formato libre) <br/>                                                                                                                 | IMAGE \_ SCN \_ CNT \_ UNINITIALIZED \_ DATA IMAGE \| \_ SCN \_ MEM READ IMAGE \_ \| \_ SCN \_ MEM WRITE IMAGE \_ \| \_ SCN \_ GPREL The IMAGE \_ SCN \_ GPREL flag should be set for IA64 architectures only; this flag is not valid for other architectures. La marca IMAGE SCN GPREL es solo para archivos de objeto; cuando este tipo de sección aparece en un archivo de imagen, no se debe establecer la marca GPREL de \_ \_ IMAGE \_ \_ SCN. <br/> |
| .sdata <br/>    | Datos inicializados relativos a GP (formato libre) <br/>                                                                                                                   | IMAGE \_ SCN \_ CNT \_ \_ INITIALIZED DATA \| IMAGE \_ SCN \_ \_ MEM READ IMAGE \| \_ SCN \_ MEM WRITE IMAGE \_ \| \_ SCN \_ GPREL The IMAGE \_ SCN \_ GPREL flag should be set for IA64 architectures only; this flag is not valid for other architectures. La marca IMAGE SCN GPREL es solo para archivos de objeto; cuando este tipo de sección aparece en un archivo de imagen, no se debe establecer la marca GPREL de \_ \_ IMAGE \_ \_ SCN. <br/>   |
| .srdata <br/>   | Datos de solo lectura relativos a GP (formato libre) <br/>                                                                                                                     | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA IMAGE \| \_ SCN \_ MEM READ IMAGE \_ \| \_ SCN \_ GPREL The IMAGE \_ SCN \_ GPREL flag should be set for IA64 architectures only; this flag is not valid for other architectures. La marca IMAGE SCN GPREL es solo para archivos de objeto; cuando este tipo de sección aparece en un archivo de imagen, no se debe establecer la marca GPREL de \_ \_ IMAGE \_ \_ SCN. <br/>                             |
| .sxdata <br/>   | Datos del controlador de excepciones registrados (solo formato libre y x86/object) <br/>                                                                                          | IMAGE SCN LNK INFO Contiene el índice de símbolos de cada uno de los controladores de excepciones a los que hace referencia el \_ código de ese archivo \_ \_ objeto. El símbolo puede ser para un símbolo UNDEF o uno definido en ese módulo. <br/>                                                                                                                                                                     |
| .text <br/>     | Código ejecutable (formato libre) <br/>                                                                                                                                | IMAGEN \_ SCN \_ CNT \_ CODE IMAGE \| \_ SCN \_ MEM EXECUTE \_ \| IIMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                           |
| .tls <br/>      | Almacenamiento local de subprocesos (solo objeto) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .tls$ <br/>     | Almacenamiento local de subprocesos (solo objeto) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .vsdata <br/>   | Datos inicializados relativos a GP (formato libre y solo para arquitecturas ARM, SH4 y Thumb) <br/>                                                                    | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .xdata <br/>    | Información de excepción (formato libre) <br/>                                                                                                                          | IMAGEN \_ SCN \_ CNT \_ INITIALIZED \_ DATA IMAGE \| \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |



 

Algunas de las secciones enumeradas aquí se marcan como "solo objeto" o "solo imagen" para indicar que su semántica especial solo es relevante para los archivos de objeto o de imagen, respectivamente. Una sección marcada como "solo imagen" podría aparecer en un archivo objeto como una manera de entrar en el archivo de imagen, pero la sección no tiene ningún significado especial para el vinculador, solo para el cargador de archivos de imagen.

### <a name="the-debug-section"></a>Sección .debug

La sección .debug se usa en archivos de objeto para contener información de depuración generada por el compilador y en archivos de imagen para contener toda la información de depuración que se genera. En esta sección se describe el empaquetado de información de depuración en archivos de objeto e imagen.

En la sección siguiente se describe el formato del directorio de depuración, que puede estar en cualquier lugar de la imagen. En las secciones posteriores se describen los "grupos" en los archivos de objeto que contienen información de depuración.

El valor predeterminado del vinculador es que la información de depuración no se asigna al espacio de direcciones de la imagen. Solo existe una sección .debug cuando la información de depuración se asigna en el espacio de direcciones.

#### <a name="debug-directory-image-only"></a>Directorio de depuración (solo imagen)

Los archivos de imagen contienen un directorio de depuración opcional que indica qué forma de información de depuración está presente y dónde está. Este directorio consta de una matriz de entradas de directorio de depuración cuya ubicación y tamaño se indican en el encabezado opcional de la imagen.

El directorio de depuración puede estar en una sección .debug descartable (si existe), o puede incluirse en cualquier otra sección del archivo de imagen o no estar en ninguna sección.

Cada entrada del directorio de depuración identifica la ubicación y el tamaño de un bloque de información de depuración. La RVA especificada puede ser cero si la información de depuración no está cubierta por un encabezado de sección (es decir, reside en el archivo de imagen y no está asignada al espacio de direcciones en tiempo de ejecución). Si está asignado, la RVA es su dirección.

Una entrada de directorio de depuración tiene el formato siguiente:



| Offset         | Size          | Campo                        | Descripción                                                                                                                                            |
|----------------|---------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Características <br/>  | Reservado, debe ser cero. <br/>                                                                                                                    |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>    | Hora y fecha en que se crearon los datos de depuración. <br/>                                                                                         |
| 8 <br/>  | 2 <br/> | MajorVersion <br/>     | Número de versión principal del formato de datos de depuración. <br/>                                                                                         |
| 10 <br/> | 2 <br/> | MinorVersion <br/>     | Número de versión secundaria del formato de datos de depuración. <br/>                                                                                         |
| 12 <br/> | 4 <br/> | Tipo <br/>             | Formato de la información de depuración. Este campo habilita la compatibilidad con varios depuradores. Para obtener más información, vea [Tipo de depuración](#debug-type).<br/> |
| 16 <br/> | 4 <br/> | SizeOfData <br/>       | Tamaño de los datos de depuración (sin incluir el propio directorio de depuración). <br/>                                                                     |
| 20 <br/> | 4 <br/> | AddressOfRawData <br/> | Dirección de los datos de depuración cuando se cargan, en relación con la base de la imagen. <br/>                                                                     |
| 24 <br/> | 4 <br/> | PointerToRawData <br/> | Puntero de archivo a los datos de depuración. <br/>                                                                                                        |



 

#### <a name="debug-type"></a>Tipo de depuración

Los valores siguientes se definen para el campo Tipo de la entrada del directorio de depuración:



| Constante                                        | Value          | Descripción                                                                                                                                                                                                      |
|-------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPO DE \_ \_ DEPURACIÓN DE IMAGEN \_ DESCONOCIDO <br/>         | 0 <br/>  | Valor desconocido que todas las herramientas omiten. <br/>                                                                                                                                                       |
| IMAGE \_ DEBUG \_ TYPE \_ COFF <br/>            | 1 <br/>  | La información de depuración de COFF (números de línea, tabla de símbolos y tabla de cadenas). Los campos de los encabezados de archivo también señalan a este tipo de información de depuración. <br/>                                          |
| IMAGE \_ DEBUG \_ TYPE \_ CODEVIEW <br/>        | 2 <br/>  | El Visual C++ información de depuración. <br/>                                                                                                                                                                    |
| IMAGE \_ DEBUG \_ TYPE \_ FPO <br/>             | 3 <br/>  | Información de omisión del puntero de marco (FPO). Esta información indica al depurador cómo interpretar los marcos de pila no estándar, que usan el registro EBP para un propósito distinto de como puntero de marco. <br/> |
| TIPO \_ DE \_ DEPURACIÓN DE IMAGEN \_ MISC <br/>            | 4 <br/>  | Ubicación del archivo DBG. <br/>                                                                                                                                                                            |
| EXCEPCIÓN \_ DE TIPO \_ DE DEPURACIÓN DE \_ IMAGEN <br/>       | 5 <br/>  | Una copia de la sección .pdata. <br/>                                                                                                                                                                            |
| CORRECCIÓN \_ DEL \_ TIPO DE \_ DEPURACIÓN DE IMAGEN <br/>           | 6 <br/>  | Reservado. <br/>                                                                                                                                                                                            |
| IMAGE \_ DEBUG \_ TYPE \_ OMAP \_ TO \_ SRC <br/>   | 7 <br/>  | Asignación de una RVA en imagen a una RVA en la imagen de origen. <br/>                                                                                                                                          |
| IMAGE \_ DEBUG \_ TYPE \_ OMAP \_ FROM \_ SRC <br/> | 8 <br/>  | Asignación de una RVA en la imagen de origen a una RVA en la imagen. <br/>                                                                                                                                          |
| TIPO \_ DE \_ DEPURACIÓN DE IMAGEN \_ BORLAND <br/>         | 9 <br/>  | Reservado para Borland. <br/>                                                                                                                                                                                |
| TIPO \_ DE \_ DEPURACIÓN DE IMAGEN \_ RESERVADO10 <br/>      | 10 <br/> | Reservado. <br/>                                                                                                                                                                                            |
| \_CLSID DE TIPO DE \_ \_ DEPURACIÓN DE IMAGEN <br/>           | 11 <br/> | Reservado. <br/>                                                                                                                                                                                            |
| IMAGE \_ DEBUG \_ TYPE \_ REPRO <br/>           | 16 <br/> | Determinismo o reproducibilidad de PE. <br/>                                                                                                                                                                   |
| IMAGE \_ DEBUG \_ TYPE \_ EX \_ DLLCHARACTERISTICS | 20 | Bits de características de DLL extendidas. |



 

Si el campo Tipo se establece en IMAGE \_ DEBUG \_ TYPE FPO, los datos sin procesar de depuración son una matriz en la que cada miembro describe el marco de \_ pila de una función. No todas las funciones del archivo de imagen deben tener definida la información de FPO, aunque el tipo de depuración sea FPO. Se supone que las funciones que no tienen información de FPO tienen marcos de pila normales. El formato de la información de FPO es el siguiente:


```C++
#define FRAME_FPO   0               
#define FRAME_TRAP  1
#define FRAME_TSS   2
               
typedef struct _FPO_DATA {
    DWORD       ulOffStart;            // offset 1st byte of function code
    DWORD       cbProcSize;            // # bytes in function
    DWORD       cdwLocals;             // # bytes in locals/4
    WORD        cdwParams;             // # bytes in params/4
    WORD        cbProlog : 8;          // # bytes in prolog
    WORD        cbRegs   : 3;          // # regs saved
    WORD        fHasSEH  : 1;          // TRUE if SEH in func
    WORD        fUseBP   : 1;          // TRUE if EBP has been allocated
    WORD        reserved : 1;          // reserved for future use
    WORD        cbFrame  : 2;          // frame type
} FPO_DATA;
```



La presencia de una entrada de tipo IMAGE DEBUG TYPE REPRO indica que el archivo PE se compila de manera que se \_ \_ pueda lograr \_ determinismo o reproducibilidad. Si la entrada no cambia, se garantiza que el archivo PE de salida sea idéntico bit a bit, independientemente de cuándo o dónde se produzca el PE. Varios campos de marca de fecha y hora del archivo PE se rellenan con parte o todos los bits de un valor hash calculado que usa el contenido del archivo PE como entrada y, por tanto, ya no representan la fecha y hora reales en que se genera un archivo PE o datos específicos relacionados dentro del PE. Los datos sin procesar de esta entrada de depuración pueden estar vacíos o pueden contener un valor hash calculado precedido de un valor de cuatro bytes que representa la longitud del valor hash.

Si el campo Tipo se establece en IMAGE \_ DEBUG \_ TYPE EX \_ DLLCHARACTERISTICS, los datos sin procesar de depuración contienen bits de características dll extendidas, además de los que se podrían establecer en el encabezado opcional de la \_ imagen. Vea [Características de DLL en](#dll-characteristics) la sección Optional Header Windows-Specific Fields [(Image Only) (Campos de encabezado opcionales [solo imagen]).](#optional-header-windows-specific-fields-image-only)

##### <a name="extended-dll-characteristics"></a>Características extendidas del archivo DLL

Los siguientes valores se definen para los bits de características extendidas del archivo DLL.

| Constante | Value | Descripción |
|-|-|-|
| IMAGEN \_ DLLCHARACTERISTICS \_ EX \_ CET \_ COMPAT | 0x0001 | La imagen es compatible con CET. |

#### <a name="debugf-object-only"></a>.debug$F (solo objeto)

Los datos de esta sección se han reemplazado en Visual C++ versión 7.0 y posteriores por un conjunto más amplio de datos que se emite en una subsección **.debug$S.**

Los archivos de objeto pueden contener secciones .debug$F cuyo contenido es uno o varios registros de datos FPO (información de omisión \_ del puntero de marco). Vea "IMAGE \_ DEBUG \_ TYPE \_ FPO" en [Tipo de depuración.](#debug-type)

El vinculador reconoce estos **registros .debug$F.** Si se genera información de depuración, el vinculador ordena los registros de datos FPO por procedimiento RVA y genera una entrada de directorio de \_ depuración para ellos.

El compilador no debe generar registros FPO para los procedimientos que tienen un formato de marco estándar.

#### <a name="debugs-object-only"></a>.debug$S (solo objeto)

Esta sección contiene información Visual C++ depuración (información simbólica).

#### <a name="debugp-object-only"></a>.debug$P (solo objeto)

Esta sección contiene Visual C++ de depuración (información precompilada). Se trata de tipos compartidos entre todos los objetos compilados mediante el encabezado precompilado que se generó con este objeto.

#### <a name="debugt-object-only"></a>.debug$T (solo objeto)

Esta sección contiene información Visual C++ depuración (información de tipo).

#### <a name="linker-support-for-microsoft-debug-information"></a>Compatibilidad del vinculador con la información de depuración de Microsoft

Para admitir la información de depuración, el vinculador:

-   Recopila todos los datos de depuración pertinentes de las secciones **.debug$F**, **debug$S,** **.debug$P** y **.debug$T.**

-   Procesa los datos junto con la información de depuración generada por el vinculador en el archivo PDB y crea una entrada de directorio de depuración para hacer referencia a él.

### <a name="the-drectve-section-object-only"></a>La sección .drectve (solo objeto)

Una sección es una sección de directiva si tiene la marca IMAGE SCN LNK INFO establecida en el encabezado de sección y tiene el nombre \_ \_ de la sección \_ **.drectve.** El enlazador quita una sección **.drectve** después de procesar la información, por lo que la sección no aparece en el archivo de imagen que se está vinculando.

Una **sección .drectve** consta de una cadena de texto que se puede codificar como ANSI o UTF-8. Si el marcador de orden de bytes UTF-8 (BOM, un prefijo de tres bytes que consta de 0xEF, 0xBB y 0xBF) no está presente, la cadena de directiva se interpreta como ANSI. La cadena de directiva es una serie de opciones del vinculador separadas por espacios. Cada opción contiene un guion, el nombre de la opción y cualquier atributo adecuado. Si una opción contiene espacios, la opción debe incluirse entre comillas. La **sección .drectve** no debe tener reubicaciones ni números de línea.

### <a name="the-edata-section-image-only"></a>Sección .edata (solo imagen)

La sección exportar datos, denominada .edata, contiene información sobre los símbolos a los que otras imágenes pueden acceder a través de la vinculación dinámica. Normalmente, los símbolos exportados se encuentran en archivos DLL, pero los archivos DLL también pueden importar símbolos.

A continuación se describe una introducción a la estructura general de la sección de exportación. Las tablas descritas suelen ser contiguas en el archivo en el orden mostrado (aunque esto no es necesario). Solo se necesitan la tabla de directorios de exportación y la tabla de direcciones de exportación para exportar símbolos como ordinales. (Un ordinal es una exportación a la que tiene acceso directamente su índice de tabla de direcciones de exportación). La tabla de puntero de nombre, la tabla ordinal y la tabla de nombres de exportación existen para admitir el uso de nombres de exportación.



| Nombre de la tabla                         | Descripción                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exportar tabla de directorios <br/> | Una tabla con una sola fila (a diferencia del directorio de depuración). Esta tabla indica las ubicaciones y tamaños de las demás tablas de exportación. <br/>                                                                                                                                                                                                               |
| Exportar tabla de direcciones <br/>   | Matriz de MATRIZ de símbolos exportados. Estas son las direcciones reales de las funciones y los datos exportados dentro de las secciones de datos y código ejecutable. Otros archivos de imagen pueden importar un símbolo mediante un índice para esta tabla (un ordinal) o, opcionalmente, mediante el uso del nombre público que corresponde al ordinal si se define un nombre público. <br/> |
| Tabla de puntero de nombre <br/>     | Matriz de punteros a los nombres de exportación públicos, ordenados en orden ascendente. <br/>                                                                                                                                                                                                                                                                    |
| Tabla ordinal <br/>          | Matriz de los ordinales que corresponden a los miembros de la tabla de puntero de nombre. La correspondencia es por posición; Por lo tanto, la tabla de puntero de nombre y la tabla ordinal deben tener el mismo número de miembros. Cada ordinal es un índice en la tabla de direcciones de exportación. <br/>                                                                        |
| Exportar tabla de nombres <br/>      | Una serie de cadenas ASCII terminadas en NULL. Los miembros de la tabla de puntero de nombre apuntan a esta área. Estos nombres son los nombres públicos a través de los cuales se importan y exportan los símbolos. no son necesariamente los mismos que los nombres privados que se usan en el archivo de imagen. <br/>                                                           |



 

Cuando otro archivo de imagen importa un símbolo por nombre, el cargador de Win32 busca en la tabla de punteros de nombre una cadena correspondiente. Si se encuentra una cadena correspondiente, el ordinal asociado se identifica mediante la búsqueda del miembro correspondiente en la tabla ordinal (es decir, el miembro de la tabla ordinal con el mismo índice que el puntero de cadena encontrado en la tabla de puntero de nombre). El ordinal resultante es un índice en la tabla de direcciones de exportación, que proporciona la ubicación real del símbolo deseado. Un ordinal puede acceder a cada símbolo de exportación.

Cuando otro archivo de imagen importa un símbolo por ordinal, no es necesario buscar en la tabla de puntero de nombre una cadena correspondiente. Por lo tanto, el uso directo de un ordinal es más eficaz. Sin embargo, un nombre de exportación es más fácil de recordar y no requiere que el usuario conozca el índice de tabla del símbolo.

#### <a name="export-directory-table"></a>Exportar tabla de directorios

La información de símbolos de exportación comienza con la tabla de directorios de exportación, que describe el resto de la información de símbolos de exportación. La tabla de directorios de exportación contiene información de dirección que se usa para resolver las importaciones en los puntos de entrada de esta imagen.



| Offset         | Size          | Campo                                | Descripción                                                                                                                                                               |
|----------------|---------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Exportar marcas <br/>             | Reservado, debe ser 0. <br/>                                                                                                                                          |
| 4 <br/>  | 4 <br/> | Marca de fecha y hora <br/>          | Hora y fecha en que se crearon los datos de exportación. <br/>                                                                                                           |
| 8 <br/>  | 2 <br/> | Major Version <br/>            | Número de versión principal. El usuario puede establecer los números de versión principal y secundaria. <br/>                                                                         |
| 10 <br/> | 2 <br/> | Minor Version <br/>            | Número de versión secundaria. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Nombre RVA <br/>                 | Dirección de la cadena ASCII que contiene el nombre del archivo DLL. Esta dirección es relativa a la base de la imagen. <br/>                                                |
| 16 <br/> | 4 <br/> | Ordinal Base <br/>             | Número ordinal inicial para las exportaciones de esta imagen. Este campo especifica el número ordinal inicial para la tabla de direcciones de exportación. Normalmente se establece en 1. <br/> |
| 20 <br/> | 4 <br/> | Entradas de tabla de direcciones <br/>    | Número de entradas de la tabla de direcciones de exportación. <br/>                                                                                                            |
| 24 <br/> | 4 <br/> | Número de punteros de nombre <br/>  | Número de entradas de la tabla de puntero de nombre. También es el número de entradas de la tabla ordinal. <br/>                                                     |
| 28 <br/> | 4 <br/> | Exportar RVA de tabla de direcciones <br/> | Dirección de la tabla de direcciones de exportación, relativa a la base de la imagen. <br/>                                                                                          |
| 32 <br/> | 4 <br/> | RVA de puntero de nombre <br/>         | Dirección de la tabla de puntero de nombre de exportación, relativa a la base de la imagen. El tamaño de la tabla se da mediante el campo Number of Name Pointers (Número de punteros de nombre). <br/>                       |
| 36 <br/> | 4 <br/> | RVA de tabla ordinal <br/>        | Dirección de la tabla ordinal, relativa a la base de la imagen. <br/>                                                                                                 |



 

#### <a name="export-address-table"></a>Exportar tabla de direcciones

La tabla de direcciones de exportación contiene la dirección de los puntos de entrada exportados y los datos exportados y absolutos. Un número ordinal se usa como índice en la tabla de direcciones de exportación.

Cada entrada de la tabla de direcciones de exportación es un campo que usa uno de los dos formatos de la tabla siguiente. Si la dirección especificada no está dentro de la sección de exportación (definida por la dirección y la longitud indicadas en el encabezado opcional), el campo es una RVA de exportación, que es una dirección real en el código o los datos. De lo contrario, el campo es un RVA de reenviador, que denomina un símbolo en otro archivo DLL.



| Offset        | Size          | Campo                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------|---------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Exportación de RVA <br/>    | Dirección del símbolo exportado cuando se carga en la memoria, con respecto a la base de la imagen. Por ejemplo, la dirección de una función exportada. <br/>                                                                                                                                                                                                                                                                                                       |
| 0 <br/> | 4 <br/> | Reenviador RVA <br/> | Puntero a una cadena ASCII terminada en NULL en la sección de exportación. Esta cadena debe estar dentro del intervalo especificado por la entrada del directorio de datos de la tabla de exportación. Vea [Directorios de datos de encabezado opcionales (solo imagen).](#optional-header-data-directories-image-only) Esta cadena proporciona el nombre del archivo DLL y el nombre de la exportación (por ejemplo, "MYDLL.expfunc") o el nombre del archivo DLL y el número ordinal de la exportación (por ejemplo, "MYDLL. \# 27"). <br/> |



 

Un reenviador RVA exporta una definición de otra imagen, lo que hace que parezca como si la estuviera exportando la imagen actual. Por lo tanto, el símbolo se importa y exporta simultáneamente.

Por ejemplo, Kernel32.dll en Windows XP, la exportación denominada "HeapAlloc" se reenvía a la cadena "NTDLL. RtlAllocateHeap". Esto permite a las aplicaciones usar Windows módulo específico de XP Ntdll.dll sin contener realmente referencias de importación a él. La tabla de importación de la aplicación solo hace referencia a Kernel32.dll. Por lo tanto, la aplicación no es específica Windows XP y se puede ejecutar en cualquier sistema Win32.

#### <a name="export-name-pointer-table"></a>Exportar tabla de puntero de nombre

La tabla de puntero de nombre de exportación es una matriz de direcciones (PDA) en la tabla de nombres de exportación. Los punteros son de 32 bits cada uno y son relativos a la base de la imagen. Los punteros se ordenan léxicamente para permitir búsquedas binarias.

Solo se define un nombre de exportación si la tabla de punteros de nombre de exportación contiene un puntero a ella.

#### <a name="export-ordinal-table"></a>Exportar tabla ordinal

La tabla ordinal de exportación es una matriz de índices de 16 bits no sesados en la tabla de direcciones de exportación. Los ordinales están sesgados por el campo Base ordinal de la tabla de directorios de exportación. En otras palabras, la base ordinal debe restarse de los ordinales para obtener índices verdaderos en la tabla de direcciones de exportación.

La tabla de puntero de nombre de exportación y la tabla ordinal de exportación forman dos matrices paralelas separadas para permitir la alineación de campos naturales. Estas dos tablas, en efecto, funcionan como una tabla, en la que la columna Export Name Pointer apunta a un nombre público (exportado) y la columna Export Ordinal proporciona el ordinal correspondiente para ese nombre público. Un miembro de la tabla de puntero de nombre de exportación y un miembro de la tabla ordinal de exportación están asociados al tener la misma posición (índice) en sus matrices respectivas.

Por lo tanto, cuando se busca la tabla de puntero de nombre de exportación y se encuentra una cadena correspondiente en la posición i, el algoritmo para buscar el RVA del símbolo y el ordinal sesgado es:

```C++
i = Search_ExportNamePointerTable (name);
ordinal = ExportOrdinalTable [i];

rva = ExportAddressTable [ordinal];
biased_ordinal = ordinal + OrdinalBase;
```

Al buscar un símbolo por ordinal (sesgado), el algoritmo para buscar la RVA y el nombre del símbolo es:

```C++
ordinal = biased_ordinal - OrdinalBase;
i = Search_ExportOrdinalTable (ordinal);

rva = ExportAddressTable [ordinal];
name = ExportNameTable [i];
```

#### <a name="export-name-table"></a>Exportar tabla de nombres

La tabla de nombres de exportación contiene los datos de cadena reales a los que apunta la tabla de punteros de nombre de exportación. Las cadenas de esta tabla son nombres públicos que otras imágenes pueden usar para importar los símbolos. Estos nombres de exportación públicas no son necesariamente los mismos que los nombres de símbolos privados que los símbolos tienen en su propio archivo de imagen y código fuente, aunque pueden serlo.

Cada símbolo exportado tiene un valor ordinal, que es simplemente el índice de la tabla de direcciones de exportación. Sin embargo, el uso de nombres de exportación es opcional. Algunos, todos o ninguno de los símbolos exportados pueden tener nombres de exportación. En el caso de los símbolos exportados que tienen nombres de exportación, las entradas correspondientes de la tabla de puntero de nombre de exportación y la tabla ordinal de exportación funcionan conjuntamente para asociar cada nombre a un ordinal.

La estructura de la tabla de nombres de exportación es una serie de cadenas ASCII terminadas en NULL de longitud variable.

### <a name="the-idata-section"></a>Sección .idata

Todos los archivos de imagen que importan símbolos, incluidos prácticamente todos los archivos ejecutables (EXE), tienen una sección .idata. A continuación se proporciona un diseño de archivo típico para la información de importación:

-   Tabla de directorios

    Entrada de directorio NULL

-   Tabla de búsqueda de importación de DLL1

    Null

-   Tabla de búsqueda de importación de DLL2

    Null

-   Tabla de búsqueda de importación de DLL3

    Null

-   Hint-Name tabla

#### <a name="import-directory-table"></a>Importar tabla de directorios

La información de importación comienza con la tabla de directorios de importación, que describe el resto de la información de importación. La tabla de directorios de importación contiene información de direcciones que se usa para resolver las referencias de corrección a los puntos de entrada dentro de una imagen DLL. La tabla de directorios de importación consta de una matriz de entradas de directorio de importación, una entrada para cada archivo DLL al que hace referencia la imagen. La última entrada de directorio está vacía (rellenada con valores NULL), lo que indica el final de la tabla de directorios.

Cada entrada de directorio de importación tiene el formato siguiente:



| Offset         | Size          | Campo                                                 | Descripción                                                                                                                                                                                 |
|----------------|---------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Importar RVA de tabla de búsqueda (características) <br/> | RVA de la tabla de búsqueda de importación. Esta tabla contiene un nombre o ordinal para cada importación. (El nombre "Characteristics" se usa en Winnt.h, pero ya no describe este campo). <br/> |
| 4 <br/>  | 4 <br/> | Marca de fecha y hora <br/>                           | Marca que se establece en cero hasta que se enlaza la imagen. Una vez enlazada la imagen, este campo se establece en la marca de tiempo o datos del archivo DLL. <br/>                                          |
| 8 <br/>  | 4 <br/> | Cadena de reenviador <br/>                           | Índice de la primera referencia de reenviador. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Nombre RVA <br/>                                  | Dirección de una cadena ASCII que contiene el nombre del archivo DLL. Esta dirección es relativa a la base de la imagen. <br/>                                                                   |
| 16 <br/> | 4 <br/> | Importar RVA de tabla de direcciones (tabla Thunk) <br/>    | RVA de la tabla de direcciones de importación. El contenido de esta tabla es idéntico al contenido de la tabla de búsqueda de importación hasta que se enlaza la imagen. <br/>                              |



 

#### <a name="import-lookup-table"></a>Importar tabla de búsqueda

Una tabla de búsqueda de importación es una matriz de números de 32 bits para PE32 o una matriz de números de 64 bits para PE32+. Cada entrada usa el formato de campo de bits que se describe en la tabla siguiente. En este formato, el bit 31 es el bit más significativo para PE32 y el bit 63 es el bit más significativo para PE32+. La colección de estas entradas describe todas las importaciones de un archivo DLL determinado. La última entrada se establece en cero (NULL) para indicar el final de la tabla.



| Bit(s)            | Size           | Campo de bit                       | Descripción                                                                                                                                                               |
|-------------------|----------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31/63 <br/> | 1 <br/>  | Marca ordinal/nombre <br/>   | Si se establece este bit, importe por ordinal. De lo contrario, importe por nombre. Bit se enmascara como 0x80000000 pe32, 0x8000000000000000 para PE32+. <br/>                         |
| 15-0 <br/>  | 16 <br/> | Número ordinal <br/>      | Número ordinal de 16 bits. Este campo solo se usa si el campo de bits Ordinal/Name Flag es 1 (importar por ordinal). Los bits 30-15 o 62-15 deben ser 0. <br/>                  |
| 30-0 <br/>  | 31 <br/> | RVA de tabla de sugerencias y nombres <br/> | Una RVA de 31 bits de una entrada de tabla de sugerencias o nombres. Este campo solo se usa si el campo de bits Ordinal/Name Flag es 0 (importar por nombre). Para PE32+ los bits 62-31 deben ser cero. <br/> |



 

#### <a name="hintname-table"></a>Tabla de sugerencias y nombres

Una tabla de sugerencias y nombres es suficiente para toda la sección de importación. Cada entrada de la tabla hint/name tiene el formato siguiente:



| Offset         | Size                 | Campo            | Descripción                                                                                                                                                                                       |
|----------------|----------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>        | Pista <br/> | Índice de la tabla de puntero de nombre de exportación. Primero se intenta una coincidencia con este valor. Si se produce un error, se realiza una búsqueda binaria en la tabla de puntero de nombre de exportación del archivo DLL. <br/>            |
| 2 <br/>  | variable <br/> | Nombre <br/> | Cadena ASCII que contiene el nombre que se importará. Esta es la cadena que debe coincidir con el nombre público del archivo DLL. Esta cadena distingue mayúsculas de minúsculas y termina con un byte nulo. <br/> |
| \* <br/> | 0 o 1 <br/>   | Pad <br/>  | Byte de relleno cero final que aparece después del byte nulo final, si es necesario, para alinear la siguiente entrada en un límite par. <br/>                                                        |



 

#### <a name="import-address-table"></a>Importar tabla de direcciones

La estructura y el contenido de la tabla de direcciones de importación son idénticos a los de la tabla de búsqueda de importación, hasta que se enlaza el archivo. Durante el enlace, las entradas de la tabla de direcciones de importación se sobrescriben con las direcciones de 32 bits (para PE32) o de 64 bits (para PE32+) de los símbolos que se importan. Estas direcciones son las direcciones de memoria reales de los símbolos, aunque técnicamente se siguen denominando "direcciones virtuales". Normalmente, el cargador procesa el enlace.

### <a name="the-pdata-section"></a>Sección .pdata

La sección .pdata contiene una matriz de entradas de tabla de funciones que se usan para el control de excepciones. La entrada de la tabla de excepciones apunta a ella en el directorio de datos de la imagen. Las entradas deben ordenarse según las direcciones de función (el primer campo de cada estructura) antes de emitirse en la imagen final. La plataforma de destino determina cuál de las tres variaciones de formato de entrada de tabla de funciones descritas a continuación se usa.

En el caso de las imágenes MIPS de 32 bits, las entradas de la tabla de funciones tienen el formato siguiente:



| Offset         | Size          | Campo                          | Descripción                                                                    |
|----------------|---------------|--------------------------------|--------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Dirección de inicio <br/>      | Va de la función correspondiente. <br/>                              |
| 4 <br/>  | 4 <br/> | Dirección final <br/>        | Va del final de la función. <br/>                                 |
| 8 <br/>  | 4 <br/> | Controlador de excepciones <br/>  | Puntero al controlador de excepciones que se va a ejecutar. <br/>               |
| 12 <br/> | 4 <br/> | Datos de controlador <br/>       | Puntero a información adicional que se va a pasar al controlador. <br/> |
| 16 <br/> | 4 <br/> | Dirección final del prólogo <br/> | Va del final del prólogo de la función. <br/>                        |



 

Para las plataformas arm, PowerPC, SH3 y SH4 Windows CE, las entradas de la tabla de funciones tienen el formato siguiente:



| Offset        | Size                | Campo                       | Descripción                                                                                                               |
|---------------|---------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>       | Dirección de inicio <br/>   | Va de la función correspondiente. <br/>                                                                         |
| 4 <br/> | 8 bits <br/>  | Longitud del prólogo <br/>   | Número de instrucciones del prólogo de la función. <br/>                                                          |
| 4 <br/> | 22 bits <br/> | Longitud de la función <br/> | Número de instrucciones de la función. <br/>                                                                   |
| 4 <br/> | 1 bit <br/>   | Marca de 32 bits <br/>     | Si se establece, la función consta de instrucciones de 32 bits. Si está clara, la función consta de instrucciones de 16 bits. <br/> |
| 4 <br/> | 1 bit <br/>   | Marca de excepción <br/>  | Si se establece, existe un controlador de excepciones para la función. De lo contrario, no existe ningún controlador de excepciones. <br/>                 |



 

En el caso de las plataformas x64 e Itanium, las entradas de tabla de funciones tienen el formato siguiente:



| Offset        | Size          | Campo                          | Descripción                                        |
|---------------|---------------|--------------------------------|----------------------------------------------------|
| 0 <br/> | 4 <br/> | Dirección de inicio <br/>      | RVA de la función correspondiente. <br/> |
| 4 <br/> | 4 <br/> | Dirección final <br/>        | RVA del final de la función. <br/>    |
| 8 <br/> | 4 <br/> | Información de desenredo <br/> | RVA de la información de desenredo. <br/>     |



 

### <a name="the-reloc-section-image-only"></a>Sección .reloc (solo imagen)

La tabla de reubicación base contiene entradas para todas las reubicaciones base de la imagen. El campo Tabla de reubicación base de los directorios de datos de encabezado opcionales proporciona el número de bytes de la tabla de reubicación base. Para obtener más información, vea [Directorios de datos de encabezado opcionales (solo imagen).](#optional-header-data-directories-image-only) La tabla de reubicación base se divide en bloques. Cada bloque representa las reubicaciones base para una página 4K. Cada bloque debe comenzar en un límite de 32 bits.

No es necesario que el cargador procese reubicaciones base resueltas por el vinculador, a menos que la imagen de carga no se pueda cargar en la base de imagen especificada en el encabezado PE.

#### <a name="base-relocation-block"></a>Bloque de reubicación base

Cada bloque de reubicación base comienza con la siguiente estructura:



| Offset        | Size          | Campo                  | Descripción                                                                                                                                              |
|---------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Página RVA <br/>   | La base de la imagen más la RVA de página se agrega a cada desplazamiento para crear la va donde se debe aplicar la reubicación base. <br/>                         |
| 4 <br/> | 4 <br/> | Tamaño de bloque <br/> | Número total de bytes del bloque de reubicación base, incluidos los campos Page RVA y Block Size y los campos Type/Offset que siguen. <br/> |



 

A continuación, el campo Tamaño de bloque va seguido de cualquier número de entradas de campo Tipo o Desplazamiento. Cada entrada es word (2 bytes) y tiene la siguiente estructura:



| Offset        | Size                | Campo              | Descripción                                                                                                                                                                                                            |
|---------------|---------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 bits <br/>  | Tipo <br/>   | Se almacena en los 4 bits superiores de WORD, un valor que indica el tipo de reubicación base que se va a aplicar. Para obtener más información, vea [Tipos de reubicación base](#base-relocation-types).<br/>                         |
| 0 <br/> | 12 bits <br/> | Offset <br/> | Almacenados en los 12 bits restantes de WORD, un desplazamiento de la dirección inicial que se especificó en el campo Page RVA para el bloque. Este desplazamiento especifica dónde se va a aplicar la reubicación base. <br/> |



 

Para aplicar una reubicación base, la diferencia se calcula entre la dirección base preferida y la base donde se carga realmente la imagen. Si la imagen se carga en su base preferida, la diferencia es cero y, por tanto, no es necesario aplicar las reubicaciones base.

#### <a name="base-relocation-types"></a>Tipos de reubicación base



| Constante                                       | Value          | Descripción                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ BASED \_ ABSOLUTE <br/>        | 0 <br/>  | Se omite la reubicación base. Este tipo se puede usar para realizar un panel de un bloque. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ BASED \_ HIGH <br/>            | 1 <br/>  | La reubicación base agrega los 16 bits altos de la diferencia al campo de 16 bits en desplazamiento. El campo de 16 bits representa el valor alto de una palabra de 32 bits. <br/>                                                                                                                                                               |
| IMAGE \_ REL \_ BASED \_ LOW <br/>             | 2 <br/>  | La reubicación base agrega los 16 bits inferiores de la diferencia al campo de 16 bits en desplazamiento. El campo de 16 bits representa la mitad baja de una palabra de 32 bits. <br/>                                                                                                                                                                  |
| IMAGE \_ REL \_ BASED \_ HIGHLOW <br/>         | 3 <br/>  | La reubicación base aplica los 32 bits de la diferencia al campo de 32 bits en desplazamiento. <br/>                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ BASED \_ HIGHADJ <br/>         | 4 <br/>  | La reubicación base agrega los 16 bits altos de la diferencia al campo de 16 bits en desplazamiento. El campo de 16 bits representa el valor alto de una palabra de 32 bits. Los 16 bits inferiores del valor de 32 bits se almacenan en la palabra de 16 bits que sigue a esta reubicación base. Esto significa que esta reubicación base ocupa dos ranuras. <br/> |
| IMAGE \_ REL \_ BASED \_ MIPS \_ JMPADDR <br/>   | 5 <br/>  | La interpretación de la reubicación depende del tipo de máquina. <br/> Cuando el tipo de máquina es MIPS, la reubicación base se aplica a una instrucción de salto de MIPS. <br/>                                                                                                                                                    |
| IMAGE \_ REL \_ BASED \_ ARM \_ MOV32 <br/>      | 5 <br/>  | Esta reubicación solo es significativa cuando el tipo de máquina es ARM o Thumb. La reubicación base aplica la dirección de 32 bits de un símbolo en un par de instrucciones MOVW/MOVT consecutivo. <br/>                                                                                                                                 |
| IMAGE \_ REL \_ BASED \_ RISCV \_ HIGH20 <br/>   | 5 <br/>  | Esta reubicación solo es significativa cuando el tipo de máquina es RISC-V. La reubicación base se aplica a los 20 bits superiores de una dirección absoluta de 32 bits. <br/>                                                                                                                                                                     |
|                                                | 6 <br/>  | Reservado, debe ser cero. <br/>                                                                                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ BASED \_ THUMB \_ MOV32 <br/>    | 7 <br/>  | Esta reubicación solo es significativa cuando el tipo de máquina es Thumb. La reubicación base aplica la dirección de 32 bits de un símbolo a un par de instrucciones MOVW/MOVT consecutivo. <br/>                                                                                                                                            |
| IMAGE \_ REL \_ BASED \_ RISCV \_ LOW12I <br/>   | 7 <br/>  | Esta reubicación solo es significativa cuando el tipo de máquina es RISC-V. La reubicación base se aplica a los 12 bits inferiores de una dirección absoluta de 32 bits formada en formato de instrucción de tipo I RISC-V. <br/>                                                                                                                           |
| IMAGE \_ REL \_ BASED \_ RISCV \_ LOW12S <br/>   | 8 <br/>  | Esta reubicación solo es significativa cuando el tipo de máquina es RISC-V. La reubicación base se aplica a los 12 bits inferiores de una dirección absoluta de 32 bits formada en formato de instrucción de tipo S RISC-V. <br/>                                                                                                                           |
| IMAGE \_ REL \_ BASED \_ MIPS \_ JMPADDR16 <br/> | 9 <br/>  | La reubicación solo es significativa cuando el tipo de máquina es MIPS. La reubicación base se aplica a una instrucción de salto MIPS16. <br/>                                                                                                                                                                                            |
| IMAGE \_ REL \_ BASED \_ DIR64 <br/>           | 10 <br/> | La reubicación base aplica la diferencia al campo de 64 bits en desplazamiento. <br/>                                                                                                                                                                                                                                             |



 

### <a name="the-tls-section"></a>La sección .tls

La sección .tls proporciona compatibilidad directa con PE y COFF para el almacenamiento local de subprocesos estáticos (TLS). TLS es una clase de almacenamiento especial que Windows admite en la que un objeto de datos no es una variable automática (pila), pero es local para cada subproceso individual que ejecuta el código. Por lo tanto, cada subproceso puede mantener un valor diferente para una variable declarada mediante TLS.

Tenga en cuenta que cualquier cantidad de datos TLS puede ser compatible mediante las llamadas DE API TlsAlloc, TlsFree, TlsSetValue y TlsGetValue. La implementación de PE o COFF es un enfoque alternativo al uso de la API y tiene la ventaja de ser más sencillo desde el punto de vista del programador de lenguaje de alto nivel. Esta implementación permite definir e inicializar datos TLS de forma similar a las variables estáticas normales de un programa. Por ejemplo, en Visual C++, una variable TLS estática se puede definir de la siguiente manera, sin usar la API Windows siguiente:

`__declspec (thread) int tlsFlag = 1;`

Para admitir esta construcción de programación, la sección PE y COFF .tls especifica la siguiente información: datos de inicialización, rutinas de devolución de llamada para la inicialización y finalización por subproceso y el índice TLS, que se explican en la explicación siguiente.

> [!Note]
>
> Los objetos de datos TLS declarados estáticamente solo se pueden usar en archivos de imagen cargados estáticamente. Este hecho hace que no sea confiable usar datos TLS estáticos en un archivo DLL a menos que sepa que el archivo DLL, o cualquier cosa vinculada estáticamente con él, nunca se cargará dinámicamente con la función de API LoadLibrary.

 

El código ejecutable tiene acceso a un objeto de datos TLS estático mediante los pasos siguientes:

1.  En el momento del vínculo, el vinculador establece el campo Dirección del índice del directorio TLS. Este campo apunta a una ubicación donde el programa espera recibir el índice TLS.

    La biblioteca en tiempo de ejecución de Microsoft facilita este proceso al definir una imagen de memoria del directorio TLS y darle el nombre especial \_ \_ "tls \_ used" (plataformas Intel x86) o \_ "tls \_ used" (otras plataformas). El vinculador busca esta imagen de memoria y usa los datos allí para crear el directorio TLS. Otros compiladores que admiten TLS y funcionan con el vinculador de Microsoft deben usar esta misma técnica.

2.  Cuando se crea un subproceso, el cargador comunica la dirección de la matriz TLS del subproceso colocando la dirección del bloque de entorno de subproceso (TEB) en el registro FS. Un puntero a la matriz TLS se encuentra en el desplazamiento de 0x2C desde el principio de TEB. Este comportamiento es específico de Intel x86.

3.  El cargador asigna el valor del índice TLS al lugar indicado por el campo Dirección del índice.

4.  El código ejecutable recupera el índice TLS y también la ubicación de la matriz TLS.

5.  El código usa el índice TLS y la ubicación de la matriz TLS (multiplicando el índice por 4 y usándose como desplazamiento a la matriz) para obtener la dirección del área de datos TLS para el programa y módulo especificados. Cada subproceso tiene su propia área de datos TLS, pero esto es transparente para el programa, que no necesita saber cómo se asignan los datos para subprocesos individuales.

6.  Se tiene acceso a un objeto de datos TLS individual como un desplazamiento fijo en el área de datos tls.

La matriz TLS es una matriz de direcciones que el sistema mantiene para cada subproceso. Cada dirección de esta matriz proporciona la ubicación de los datos TLS de un módulo determinado (EXE o DLL) dentro del programa. El índice TLS indica qué miembro de la matriz se va a usar. El índice es un número (significativo solo para el sistema) que identifica el módulo.

#### <a name="the-tls-directory"></a>El directorio TLS

El directorio TLS tiene el formato siguiente:



| Desplazamiento (PE32/PE32+) | Tamaño (PE32/PE32+) | Campo                            | Descripción                                                                                                                                                                                                                                                                                                                                         |
|----------------------|--------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>        | 4/8 <br/>    | Va de inicio de datos sin procesar <br/>    | Dirección inicial de la plantilla TLS. La plantilla es un bloque de datos que se usa para inicializar datos TLS. El sistema copia todos estos datos cada vez que se crea un subproceso, por lo que no debe estar dañado. Tenga en cuenta que esta dirección no es una RVA; es una dirección para la que debe haber una reubicación base en la sección .reloc. <br/> |
| 4/8 <br/>      | 4/8 <br/>    | Va de finalización de datos sin procesar <br/>      | Dirección del último byte de TLS, excepto el relleno cero. Al igual que con el campo Va de inicio de datos sin procesar, se trata de un VA, no de una RVA. <br/>                                                                                                                                                                                                       |
| 8/16 <br/>     | 4/8 <br/>    | Dirección del índice <br/>     | Ubicación en la que se va a recibir el índice TLS que asigna el cargador. Esta ubicación se encuentra en una sección de datos normal, por lo que se le puede dar un nombre simbólico que sea accesible para el programa. <br/>                                                                                                                                                    |
| 12/24 <br/>    | 4/8 <br/>    | Dirección de devoluciones de llamada <br/> | Puntero a una matriz de funciones de devolución de llamada TLS. La matriz termina en null, por lo que si no se admite ninguna función de devolución de llamada, este campo apunta a 4 bytes establecidos en cero. Para obtener información sobre el prototipo de estas funciones, vea [Funciones de devolución de llamada TLS.](#tls-callback-functions)<br/>                                                      |
| 16/32 <br/>    | 4 <br/>      | Tamaño de relleno cero <br/>    | Tamaño en bytes de la plantilla, más allá de los datos inicializados delimitados por los campos VA de inicio de datos sin procesar y VA de finalización de datos sin procesar. El tamaño total de la plantilla debe ser el mismo que el tamaño total de los datos TLS en el archivo de imagen. El relleno cero es la cantidad de datos que viene después de los datos distintos de cero inicializados. <br/>                            |
| 20/36 <br/>    | 4 <br/>      | Características <br/>      | Los cuatro bits \[ 23:20 \] describen la información de alineación. Los valores posibles son los definidos como IMAGE SCN ALIGN , que también se usan para describir la alineación \_ de la sección en los archivos de \_ \_ \* objeto. Los otros 28 bits están reservados para su uso futuro. <br/>                                                                                                       |



 

#### <a name="tls-callback-functions"></a>Funciones de devolución de llamada TLS

El programa puede proporcionar una o varias funciones de devolución de llamada TLS para admitir la inicialización y terminación adicionales para objetos de datos TLS. Un uso típico de esta función de devolución de llamada sería llamar a constructores y destructores para objetos .

Aunque normalmente no hay más de una función de devolución de llamada, una devolución de llamada se implementa como una matriz para que sea posible agregar funciones de devolución de llamada adicionales si lo desea. Si hay más de una función de devolución de llamada, se llama a cada función en el orden en que su dirección aparece en la matriz. Un puntero nulo finaliza la matriz. Es perfectamente válido tener una lista vacía (no se admite ninguna devolución de llamada), en cuyo caso la matriz de devolución de llamada tiene exactamente un puntero de miembro a nulo.

El prototipo de una función de devolución de llamada (a la que apunta un puntero de tipo PIMAGE TLS CALLBACK) tiene los mismos parámetros que una función de \_ \_ punto de entrada dll:


```C++
typedef VOID
(NTAPI *PIMAGE_TLS_CALLBACK) (
    PVOID DllHandle,
    DWORD Reason,
    PVOID Reserved
    );
```



El parámetro Reservado debe establecerse en cero. El parámetro Reason puede tomar los siguientes valores:



| Parámetro                          | Value         | Descripción                                                                                          |
|----------------------------------|---------------|------------------------------------------------------------------------------------------------------|
| ASOCIACIÓN \_ DE PROCESOS \_ DLL <br/> | 1 <br/> | Se ha iniciado un nuevo proceso, incluido el primer subproceso. <br/>                                   |
| ASOCIACIÓN \_ DE SUBPROCESOS \_ DLL <br/>  | 2 <br/> | Se ha creado un nuevo subproceso. Esta notificación se envía para todos los subprocesos, menos el primer subproceso. <br/>      |
| \_ \_ DESASOCIÓN DE SUBPROCESOS DLL <br/>  | 3 <br/> | Un subproceso está a punto de finalizar. Esta notificación se envía para todos los subprocesos, menos el primer subproceso. <br/> |
| \_DESASOCIÓN \_ DEL PROCESO DE DLL <br/> | 0 <br/> | Un proceso está a punto de finalizar, incluido el subproceso original. <br/>                          |



 

### <a name="the-load-configuration-structure-image-only"></a>Estructura de configuración de carga (solo imagen)

La estructura de configuración de carga (IMAGE LOAD CONFIG DIRECTORY) se usó anteriormente en casos muy limitados en el propio sistema operativo Windows NT para describir varias características demasiado difíciles o demasiado grandes para describir en el encabezado de archivo u encabezado opcional de la \_ \_ \_ imagen. Las versiones actuales del vinculador de Microsoft y Windows XP y versiones posteriores de Windows usan una nueva versión de esta estructura para sistemas basados en x86 de 32 bits que incluyen tecnología SEH reservada. Esto proporciona una lista de controladores de excepciones estructurados seguros que el sistema operativo usa durante el envío de excepciones. Si la dirección del controlador reside en el intervalo de VA de una imagen y está marcada como reservada para SEH (es decir, IMAGE DLLCHARACTERISTICS NO SEH está clara en el campo \_ \_ DllCharacteristics del encabezado opcional, como se describió anteriormente), el controlador debe estar en la lista de controladores seguros conocidos para \_ esa imagen. De lo contrario, el sistema operativo finaliza la aplicación. Esto ayuda a evitar el ataque de "secuestro del controlador de excepciones x86" que se ha usado en el pasado para tomar el control del sistema operativo.

El vinculador de Microsoft proporciona automáticamente una estructura de configuración de carga predeterminada para incluir los datos SEH reservados. Si el código de usuario ya proporciona una estructura de configuración de carga, debe incluir los nuevos campos SEH reservados. De lo contrario, el vinculador no puede incluir los datos de SEH reservados y la imagen no se marca como que contiene el SEH reservado.

#### <a name="load-configuration-directory"></a>Cargar directorio de configuración

La entrada del directorio de datos para una estructura de configuración de carga de SEH reservada previamente debe especificar un tamaño determinado de la estructura de configuración de carga, ya que el cargador del sistema operativo siempre espera que sea un valor determinado. En ese sentido, el tamaño es realmente solo una comprobación de versión. Por compatibilidad con Windows XP y versiones anteriores de Windows, el tamaño debe ser 64 para las imágenes x86.

#### <a name="load-configuration-layout"></a>Diseño de configuración de carga

La estructura de configuración de carga tiene el siguiente diseño para archivos PE de 32 y 64 bits:



| Offset              | Size            | Campo                                      | Descripción                                                                                                                                                                                                                                                                                 |
|---------------------|-----------------|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 4 <br/>   | Características <br/>                | Marcas que indican los atributos del archivo, actualmente sin usar. <br/>                                                                                                                                                                                                                   |
| 4 <br/>       | 4 <br/>   | TimeDateStamp <br/>                  | Valor de marca de fecha y hora. El valor se representa en el número de segundos transcurridos desde la medianoche (00:00:00), el 1 de enero de 1970, hora universal coordinada, según el reloj del sistema. La marca de tiempo se puede imprimir mediante la función de tiempo en tiempo de ejecución de C (CRT). <br/> |
| 8 <br/>       | 2 <br/>   | MajorVersion <br/>                   | Número de versión principal. <br/>                                                                                                                                                                                                                                                           |
| 10 <br/>      | 2 <br/>   | MinorVersion <br/>                   | Número de versión secundaria. <br/>                                                                                                                                                                                                                                                           |
| 12 <br/>      | 4 <br/>   | GlobalFlagsClear <br/>               | Marcas globales del cargador que se borrarán para este proceso cuando el cargador inicie el proceso. <br/>                                                                                                                                                                                             |
| 16 <br/>      | 4 <br/>   | GlobalFlagsSet <br/>                 | Marcas globales del cargador que se establecerán para este proceso cuando el cargador inicie el proceso. <br/>                                                                                                                                                                                               |
| 20 <br/>      | 4 <br/>   | CriticalSectionDefaultTimeout <br/>  | Valor de tiempo de espera predeterminado que se va a usar para las secciones críticas de este proceso que se abandonan. <br/>                                                                                                                                                                                       |
| 24 <br/>      | 4/8 <br/> | DeCommitFreeBlockThreshold <br/>     | Memoria que se debe liberar antes de que se devuelva al sistema, en bytes. <br/>                                                                                                                                                                                                        |
| 28/32 <br/>   | 4/8 <br/> | DeCommitTotalFreeThreshold <br/>     | Cantidad total de memoria libre, en bytes. <br/>                                                                                                                                                                                                                                          |
| 32/40 <br/>   | 4/8 <br/> | LockPrefixTable <br/>                | \[x86 solo Va de una lista de direcciones donde se usa el prefijo LOCK para que se puedan reemplazar por NOP en \] máquinas con un solo procesador. <br/>                                                                                                                                    |
| 36/48 <br/>   | 4/8 <br/> | MaximumAllocationSize <br/>          | Tamaño máximo de asignación, en bytes. <br/>                                                                                                                                                                                                                                              |
| 40/56 <br/>   | 4/8 <br/> | VirtualMemoryThreshold <br/>         | Tamaño máximo de memoria virtual, en bytes. <br/>                                                                                                                                                                                                                                          |
| 44/64 <br/>   | 4/8 <br/> | ProcessAffinityMask <br/>            | Establecer este campo en un valor distinto de cero equivale a llamar a SetProcessAffinityMask con este valor durante el inicio del proceso (.exe único) <br/>                                                                                                                                       |
| 48/72 <br/>   | 4 <br/>   | ProcessHeapFlags <br/>               | Procesar marcas de montón que corresponden al primer argumento de la función HeapCreate. Estas marcas se aplican al montón de procesos que se crea durante el inicio del proceso. <br/>                                                                                                              |
| 52/76 <br/>   | 2 <br/>   | CSDVersion <br/>                     | Identificador de versión del Service Pack. <br/>                                                                                                                                                                                                                                            |
| 54/78 <br/>   | 2 <br/>   | Reservada <br/>                       | Debe ser cero. <br/>                                                                                                                                                                                                                                                                   |
| 56/80 <br/>   | 4/8 <br/> | EditList <br/>                       | Reservado para su uso por el sistema. <br/>                                                                                                                                                                                                                                                 |
| 60/88 <br/>   | 4/8 <br/> | SecurityCookie <br/>                 | Puntero a una cookie que se usa en Visual C++ implementación de GS. <br/>                                                                                                                                                                                                          |
| 64/96 <br/>   | 4/8 <br/> | SEHandlerTable <br/>                 | \[x86 solo Va de la tabla ordenada de VTA de cada controlador de SE \] válido en la imagen. <br/>                                                                                                                                                                                  |
| 68/104 <br/>  | 4/8 <br/> | SEHandlerCount <br/>                 | \[x86 solo \] El recuento de controladores únicos de la tabla. <br/>                                                                                                                                                                                                                         |
| 72/112 <br/>  | 4/8 <br/> | GuardCFCheckFunctionPointer <br/>    | Va donde se almacena el Flow de la función check-function de Control y Protección. <br/>                                                                                                                                                                                                               |
| 76/120 <br/>  | 4/8 <br/> | GuardCFDispatchFunctionPointer <br/> | Va donde se almacena el Flow dispatch-function de Control. <br/>                                                                                                                                                                                                            |
| 80/128 <br/>  | 4/8 <br/> | GuardCFFunctionTable <br/>           | Va de la tabla ordenada de VTA de cada función Control Flow Guard en la imagen. <br/>                                                                                                                                                                                            |
| 84/136 <br/>  | 4/8 <br/> | GuardCFFunctionCount <br/>           | El recuento de LASA únicas de la tabla anterior. <br/>                                                                                                                                                                                                                                    |
| 88/144 <br/>  | 4 <br/>   | GuardFlags <br/>                     | Controle Flow marcas relacionadas con Guard. <br/>                                                                                                                                                                                                                                               |
| 92/148 <br/>  | 12 <br/>  | CodeIntegrity <br/>                  | Información de integridad del código. <br/>                                                                                                                                                                                                                                                     |
| 104/160 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryTable <br/> | La va donde se almacena la Flow IAT de control de la dirección de Protección contra el tráfico. <br/>                                                                                                                                                                                                              |
| 108/168 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryCount <br/> | El recuento de LASA únicas de la tabla anterior. <br/>                                                                                                                                                                                                                                    |
| 112/176 <br/> | 4/8 <br/> | GuardLongJumpTargetTable <br/>       | La va donde se almacena Flow destino de salto largo de Control Flow Guard. <br/>                                                                                                                                                                                                               |
| 116/184 <br/> | 4/8 <br/> | GuardLongJumpTargetCount <br/>       | El recuento de LASA únicas de la tabla anterior. <br/>                                                                                                                                                                                                                                    |



 

El campo GuardFlags contiene una combinación de uno o varios de los siguientes marcadores y subcampos:

-   El módulo realiza comprobaciones de integridad del flujo de control mediante la compatibilidad proporcionada por el sistema.

    ` #define IMAGE_GUARD_CF_INSTRUMENTED  0x00000100`

-   El módulo realiza comprobaciones de integridad de escritura y flujo de control.

    ` #define IMAGE_GUARD_CFW_INSTRUMENTED  0x00000200`

-   El módulo contiene metadatos de destino de flujo de control válidos.

    `#define IMAGE_GUARD_CF_FUNCTION_TABLE_PRESENT  0x00000400`

-   El módulo no hace uso de la cookie de seguridad /GS.

    ` #define IMAGE_GUARD_SECURITY_COOKIE_UNUSED  0x00000800`

-   El módulo admite IAT de carga retrasada de solo lectura.

    `#define IMAGE_GUARD_PROTECT_DELAYLOAD_IAT  0x00001000`

-   Retrasar la carga de la tabla de importación en su propia sección .didat (sin nada más) que se puede volver a proteger libremente.

    ` #define IMAGE_GUARD_DELAYLOAD_IAT_IN_ITS_OWN_SECTION  0x00002000`

-   El módulo contiene información de exportación suprimida. Esto también deduce que la tabla IAT de la dirección tomada también está presente en la configuración de carga.

    `#define  IMAGE_GUARD_CF_EXPORT_SUPPRESSION_INFO_PRESENT  0x00004000`

-   El módulo habilita la supresión de exportaciones.

    `#define IMAGE_GUARD_CF_ENABLE_EXPORT_SUPPRESSION  0x00008000`

-   El módulo contiene información de destino longjmp.

    ` #define IMAGE_GUARD_CF_LONGJUMP_TABLE_PRESENT  0x00010000`

-   Máscara para el subcampo que contiene el paso de las entradas de la tabla de funciones de Control Flow Guard (es decir, el recuento adicional de bytes por entrada de tabla).

    ` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_MASK  0xF0000000`

Además, el encabezado winnt.h del SDK de Windows define esta macro para la cantidad de bits que se va a desplazar a la derecha el valor GuardFlags para justificar a la derecha el paso de la tabla de funciones de Control Flow Guard:

` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_SHIFT  28`

### <a name="the-rsrc-section"></a>Sección .rsrc

Los recursos se indexan mediante una estructura de árbol ordenado binario de varios niveles. El diseño general puede incorporar 2 \* \* 31 niveles. Sin embargo, por convención, Windows usa tres niveles:

<dl> Tipo  
Nombre  
Lenguaje  
</dl>

Una serie de tablas de directorios de recursos relaciona todos los niveles de la siguiente manera: cada tabla de directorio va seguida de una serie de entradas de directorio que dan el nombre o identificador (ID) de ese nivel (tipo, nombre o nivel de idioma) y una dirección de una descripción de datos u otra tabla de directorio. Si la dirección apunta a una descripción de datos, los datos son una hoja en el árbol. Si la dirección apunta a otra tabla de directorios, esa tabla muestra las entradas de directorio en el siguiente nivel hacia abajo.

Los nombres de tipo, nombre e idioma de una hoja se determinan mediante la ruta de acceso que se toma a través de las tablas de directorio para llegar a la hoja. La primera tabla determina el identificador de tipo, la segunda tabla (a la que apunta la entrada de directorio en la primera tabla) determina el identificador de nombre y la tercera tabla determina el identificador de idioma.

La estructura general de la sección .rsrc es:



| data                                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tablas de directorio de recursos (y entradas de directorio de recursos) <br/> | Una serie de tablas, una para cada grupo de nodos del árbol. Todos los nodos de nivel superior (Tipo) se muestran en la primera tabla. Las entradas de esta tabla apuntan a tablas de segundo nivel. Cada árbol de segundo nivel tiene el mismo identificador de tipo, pero identificadores de nombre diferentes. Los árboles de tercer nivel tienen los mismos nombres y tipos, pero distintos. <br/> Cada tabla individual va seguida inmediatamente de entradas de directorio, en las que cada entrada tiene un nombre o un identificador numérico y un puntero a una descripción de datos o una tabla en el siguiente nivel inferior. <br/> |
| Cadenas de directorio de recursos <br/>                                 | Cadenas Unicode alineadas con dos bytes, que sirven como datos de cadena a los que apuntan las entradas del directorio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Descripción de los datos de recursos <br/>                                  | Matriz de registros, a los que apuntan las tablas, que describen el tamaño real y la ubicación de los datos del recurso. Estos registros son las hojas del árbol de descripción de recursos. <br/>                                                                                                                                                                                                                                                                                                                                                                |
| Datos de recursos <br/>                                              | Datos sin procesar de la sección de recursos. La información de tamaño y ubicación del campo Descripciones de datos de recursos delimita las regiones individuales de los datos de recursos. <br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

#### <a name="resource-directory-table"></a>Tabla de directorios de recursos

Cada tabla de directorio de recursos tiene el formato siguiente. Esta estructura de datos debe considerarse el encabezado de una tabla porque la tabla realmente consta de entradas de directorio (descritas en la sección 6.9.2, "Entradas de directorio de recursos") y esta estructura:



| Offset         | Size          | Campo                              | Descripción                                                                                                                                                                     |
|----------------|---------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Características <br/>        | Marcas de recursos. Este campo está reservado para un uso futuro. Actualmente está establecido en cero. <br/>                                                                                 |
| 4 <br/>  | 4 <br/> | Marca de fecha y hora <br/>        | Hora a la que el compilador de recursos creó los datos del recurso. <br/>                                                                                               |
| 8 <br/>  | 2 <br/> | Major Version <br/>          | Número de versión principal, establecido por el usuario. <br/>                                                                                                                          |
| 10 <br/> | 2 <br/> | Minor Version <br/>          | Número de versión secundaria, establecido por el usuario. <br/>                                                                                                                          |
| 12 <br/> | 2 <br/> | Número de entradas de nombre <br/> | Número de entradas de directorio inmediatamente después de la tabla que usan cadenas para identificar las entradas De tipo, Nombre o Idioma (en función del nivel de la tabla). <br/> |
| 14 <br/> | 2 <br/> | Número de entradas de identificador <br/>   | Número de entradas de directorio inmediatamente después de las entradas name que usan identificadores numéricos para las entradas Type, Name o Language. <br/>                                    |



 

#### <a name="resource-directory-entries"></a>Entradas del directorio de recursos

Las entradas del directorio son las filas de una tabla. Cada entrada del directorio de recursos tiene el formato siguiente. Si la entrada es una entrada nombre o identificador se indica mediante la tabla de directorios de recursos, que indica cuántas entradas de nombre e identificador le siguen (recuerde que todas las entradas de nombre preceden a todas las entradas de identificador de la tabla). Todas las entradas de la tabla se ordenan en orden ascendente: las entradas Name por cadena que distinguen mayúsculas de minúsculas y las entradas id. por valor numérico. Los desplazamientos son relativos a la dirección del directorio IMAGE \_ DIRECTORY \_ ENTRY RESOURCE \_ DataDirectory. Consulte Emparejamiento dentro del PE: un paseo por el formato de archivo ejecutable [portable Win32](/previous-versions/ms809762(v=msdn.10)#pe-file-resources) para obtener más información.



| Offset        | Size          | Campo                           | Descripción                                                                                                          |
|---------------|---------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Desplazamiento de nombre <br/>         | Desplazamiento de una cadena que proporciona la entrada Tipo, Nombre o Id. de idioma, según el nivel de tabla. <br/>     |
| 0 <br/> | 4 <br/> | Identificador entero <br/>          | Entero de 32 bits que identifica la entrada Tipo, Nombre o Id. de idioma. <br/>                                   |
| 4 <br/> | 4 <br/> | Desplazamiento de entrada de datos <br/>   | Bit alto 0. Dirección de una entrada de datos de recursos (hoja). <br/>                                                   |
| 4 <br/> | 4 <br/> | Desplazamiento del subdirectorio <br/> | Bit alto 1. Los 31 bits inferiores son la dirección de otra tabla de directorio de recursos (el siguiente nivel hacia abajo). <br/> |



 

#### <a name="resource-directory-string"></a>Cadena de directorio de recursos

El área de cadenas del directorio de recursos consta de cadenas Unicode, que están alineadas con palabras. Estas cadenas se almacenan juntas después de la última entrada de Resource Directory y antes de la primera entrada de datos de recursos. Esto minimiza el impacto de estas cadenas de longitud variable en la alineación de las entradas de directorio de tamaño fijo. Cada cadena de directorio de recursos tiene el formato siguiente:



| Offset        | Size                 | Campo                      | Descripción                                                            |
|---------------|----------------------|----------------------------|------------------------------------------------------------------------|
| 0 <br/> | 2 <br/>        | Length <br/>         | Tamaño de la cadena, sin incluir el propio campo de longitud. <br/> |
| 2 <br/> | variable <br/> | Cadena Unicode <br/> | Datos de cadena Unicode de longitud variable, alineados con palabras. <br/>     |



 

#### <a name="resource-data-entry"></a>Entrada de datos de recursos

Cada entrada de datos de recursos describe una unidad real de datos sin procesar en el área Datos de recursos. Una entrada De datos de recursos tiene el formato siguiente:



| Offset         | Size          | Campo                            | Descripción                                                                                                                                           |
|----------------|---------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | RVA de datos <br/>             | Dirección de una unidad de datos de recursos en el área Datos de recursos. <br/>                                                                         |
| 4 <br/>  | 4 <br/> | Size <br/>                 | Tamaño, en bytes, de los datos de recursos a los que apunta el campo RVA de datos. <br/>                                                        |
| 8 <br/>  | 4 <br/> | codepage <br/>             | Página de códigos que se usa para descodificar valores de punto de código dentro de los datos del recurso. Normalmente, la página de códigos sería la página de códigos Unicode. <br/> |
| 12 <br/> | 4 <br/> | Reservado, debe ser 0. <br/> |                                                                                                                                                       |



 

### <a name="the-cormeta-section-object-only"></a>La sección .cormeta (solo objeto)

Los metadatos CLR se almacenan en esta sección. Se usa para indicar que el archivo de objeto contiene código administrado. El formato de los metadatos no está documentado, pero se puede entregar a las interfaces CLR para controlar los metadatos.

### <a name="the-sxdata-section"></a>Sección .sxdata

Los controladores de excepciones válidos de un objeto se enumeran en la **sección .sxdata** de ese objeto. La sección está marcada como IMAGE \_ SCN \_ LNK \_ INFO. Contiene el índice de símbolos COFF de cada controlador válido, con 4 bytes por índice.

Además, el compilador marca un objeto COFF como SEH registrado mediante la emisión del símbolo absoluto " " con el LSB del campo de valor establecido @feat.00 en 1. Un objeto COFF sin controladores SEH registrados tendría el símbolo " @feat.00 " , pero no la sección **.sxdata.**

## <a name="archive-library-file-format"></a>Formato de archivo de archivo (biblioteca)

- [Archivar firma de archivo](#archive-file-signature)
- [Archivar encabezados de miembro](#archive-member-headers)
- [Primer miembro del vinculador](#first-linker-member)
- [Segundo miembro del vinculador](#second-linker-member)
- [Miembro Longnames](#longnames-member)

El formato de archivo COFF proporciona un mecanismo estándar para almacenar colecciones de archivos de objeto. Estas colecciones se denominan normalmente bibliotecas en la documentación de programación.

Los primeros 8 bytes de un archivo constan de la firma de archivo. El resto del archivo consta de una serie de miembros de archivo, como se muestra a continuación:

-   El primer y el segundo miembros son "miembros del vinculador". Cada uno de estos miembros tiene su propio formato, como se describe en la sección [Tipo de nombre de importación](#import-name-type). Normalmente, un vinculador coloca información en estos miembros de archivo. Los miembros del vinculador contienen el directorio del archivo.

-   El tercer miembro es el miembro "longnames". Este miembro opcional consta de una serie de cadenas ASCII terminadas en NULL en las que cada cadena es el nombre de otro miembro de archivo.

-   El resto del archivo consta de miembros estándar (archivo de objeto). Cada uno de estos miembros contiene el contenido de un archivo objeto en su totalidad.

Un encabezado de miembro de archivo precede a cada miembro. En la lista siguiente se muestra la estructura general de un archivo:

-   Firma :"! &lt; arch &gt; \\ n"
-   Encabezado

    <dl> Primer miembro del vinculador  
    </dl>

-   Encabezado

    <dl> Segundo miembro del vinculador  
    </dl>

-   Encabezado

    <dl> Miembro Longnames  
    </dl>

-   Encabezado

    <dl> Contenido del archivo OBJ 1  
    (formato COFF)  
    </dl>

-   Encabezado

    <dl> Contenido del archivo OBJ 2  
    (formato COFF)  
    </dl>

### <a name="archive-file-signature"></a>Archivar firma de archivo

La firma del archivo de archivo identifica el tipo de archivo. Cualquier utilidad (por ejemplo, un vinculador) que toma un archivo de archivo como entrada puede comprobar el tipo de archivo leyendo esta firma. La firma consta de los siguientes caracteres ASCII, en los que cada carácter siguiente se representa literalmente, excepto el carácter de nueva línea ( \\ n):

`!<arch>\n`

### <a name="archive-member-headers"></a>Archivar encabezados de miembro

Cada miembro (vinculador, longnames o miembro de archivo de objeto) va precedido de un encabezado . Un encabezado de miembro de archivo tiene el formato siguiente, en el que cada campo es una cadena de texto ASCII que se deja justificada y se agrega con espacios al final del campo. No hay ningún carácter nulo de terminación en ninguno de estos campos.

Cada encabezado de miembro se inicia en la primera dirección par después del final del miembro de archivo anterior.



| Offset         | Size           | Campo                     | Descripción                                                                                                                                                                                                 |
|----------------|----------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 16 <br/> | Nombre <br/>          | Nombre del miembro de archivo, con una barra diagonal (/) anexada para finalizar el nombre. Si el primer carácter es una barra diagonal, el nombre tiene una interpretación especial, como se describe en la tabla siguiente. <br/> |
| 16 <br/> | 12 <br/> | Date <br/>          | Fecha y hora en que se creó el miembro de archivo: se trata de la representación decimal ASCII del número de segundos desde el UCT 1/1/1970. <br/>                                                    |
| 28 <br/> | 6 <br/>  | Id. de usuario <br/>       | Representación decimal ASCII del identificador de usuario. Este campo no contiene un valor significativo en las plataformas Windows porque las herramientas de Microsoft emiten todos los espacios en blanco. <br/>                                    |
| 34 <br/> | 6 <br/>  | Identificador de grupo <br/>      | Representación decimal ASCII del identificador de grupo. Este campo no contiene un valor significativo en las plataformas Windows porque las herramientas de Microsoft emiten todos los espacios en blanco. <br/>                                   |
| 40 <br/> | 8 <br/>  | Modo <br/>          | Representación octal ASCII del modo de archivo del miembro. Este es el valor ST MODE de la función en tiempo de \_ ejecución \_ de C wstat. <br/>                                                                       |
| 48 <br/> | 10 <br/> | Size <br/>          | Representación decimal ASCII del tamaño total del miembro de archivo, sin incluir el tamaño del encabezado. <br/>                                                                                  |
| 58 <br/> | 2 <br/>  | Final del encabezado <br/> | Los dos bytes de la cadena de C " eto \\ n" (0x60 0x0A). <br/>                                                                                                                                               |



 

El campo Nombre tiene uno de los formatos que se muestran en la tabla siguiente. Como se mencionó anteriormente, cada una de estas cadenas se deja justificada y se agrega con espacios finales dentro de un campo de 16 bytes:



| Contenido del campo Nombre | Descripción                                                                                                                                                                                                                                                                                          |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name/ <br/>      | Nombre del miembro de archivo. <br/>                                                                                                                                                                                                                                                          |
| / <br/>          | El miembro de archivo es uno de los dos miembros del vinculador. Ambos miembros del vinculador tienen este nombre. <br/>                                                                                                                                                                                          |
| // <br/>         | El miembro de archivo es el miembro longnames, que consta de una serie de cadenas ASCII terminadas en NULL. El miembro longnames es el tercer miembro de archivo y es opcional. <br/>                                                                     |
| /n <br/>         | El nombre del miembro de archivo se encuentra en el desplazamiento n dentro del miembro longnames. El número n es la representación decimal del desplazamiento. Por ejemplo: "/26" indica que el nombre del miembro de archivo se encuentra 26 bytes más allá del principio del contenido del miembro longnames. <br/> |



 

### <a name="first-linker-member"></a>Primer miembro del vinculador

El nombre del primer miembro del vinculador es "/". El primer miembro del vinculador se incluye por compatibilidad con versiones anteriores. Los vinculadores actuales no lo usan, pero su formato debe ser correcto. Este miembro del vinculador proporciona un directorio de nombres de símbolos, al igual que el segundo miembro del vinculador. Para cada símbolo, la información indica dónde encontrar el miembro de archivo que contiene el símbolo.

El primer miembro del vinculador tiene el formato siguiente. Esta información aparece después del encabezado :



| Offset         | Size               | Campo                         | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|----------------|--------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Número de símbolos <br/> | Unsigned long que contiene el número de símbolos indexados. Este número se almacena en formato big-endian. Cada miembro de archivo de objeto define normalmente uno o varios símbolos externos. <br/>                                                                                                                                                                         |
| 4 <br/>  | 4 \* n <br/> | Compensaciones <br/>           | Matriz de desplazamientos de archivo para archivar encabezados de miembro, en el que n es igual al campo Number of Symbols (Número de símbolos). Cada número de la matriz es un long sin signo almacenado en formato big-endian. Para cada símbolo que se denomina en la tabla de cadenas, el elemento correspondiente de la matriz offsets proporciona la ubicación del miembro de archivo que contiene el símbolo. <br/> |
| \* <br/> | \* <br/>     | Tabla de cadenas <br/>      | Una serie de cadenas terminadas en NULL que nombren todos los símbolos del directorio. Cada cadena comienza inmediatamente después del carácter nulo de la cadena anterior. El número de cadenas debe ser igual al valor del campo Number of Symbols (Número de símbolos). <br/>                                                                                                       |



 

Los elementos de la matriz offsets deben organizarse en orden ascendente. Este hecho implica que los símbolos de la tabla de cadenas deben organizarse según el orden de los miembros de archivo. Por ejemplo, todos los símbolos del primer miembro de archivo de objeto tendrían que aparecer antes que los símbolos del segundo archivo de objeto.

### <a name="second-linker-member"></a>Segundo miembro del vinculador

El segundo miembro del vinculador tiene el nombre "/" al igual que el primer miembro del vinculador. Aunque ambos miembros del vinculador proporcionan un directorio de símbolos y miembros de archivo que los contienen, todos los vinculadores actuales usan el segundo miembro del vinculador en lugar del primero. El segundo miembro del vinculador incluye nombres de símbolos en orden léxico, lo que permite una búsqueda más rápida por nombre.

El segundo miembro tiene el formato siguiente. Esta información aparece después del encabezado :



| Offset         | Size               | Campo                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|--------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Número de miembros <br/> | Un long sin signo que contiene el número de miembros de archivo. <br/>                                                                                                                                                                                                                                                                                                                                |
| 4 <br/>  | 4 \* m <br/> | Compensaciones <br/>           | Matriz de desplazamientos de archivo para archivar encabezados de miembro, organizados en orden ascendente. Cada desplazamiento es un largo sin signo. El número m es igual al valor del campo Number of Members (Número de miembros). <br/>                                                                                                                                                                                                        |
| \* <br/> | 4 <br/>      | Número de símbolos <br/> | Long sin signo que contiene el número de símbolos indizados. Cada miembro de archivo de objeto define normalmente uno o varios símbolos externos. <br/>                                                                                                                                                                                                                                                        |
| \* <br/> | 2 \* n <br/> | Índices <br/>           | Matriz de índices basados en 1 (corto sin signo) que asignan nombres de símbolos a desplazamientos de miembros de archivo. El número n es igual al campo Number of Symbols (Número de símbolos). Para cada símbolo que se denomina en la tabla de cadenas, el elemento correspondiente de la matriz Índices proporciona un índice en la matriz offsets. La matriz offsets, a su vez, proporciona la ubicación del miembro de archivo que contiene el símbolo. <br/> |
| \* <br/> | \* <br/>     | Tabla de cadenas <br/>      | Una serie de cadenas terminadas en NULL que nombren todos los símbolos del directorio. Cada cadena comienza inmediatamente después del byte nulo de la cadena anterior. El número de cadenas debe ser igual al valor del campo Number of Symbols (Número de símbolos). En esta tabla se enumeran todos los nombres de símbolos en orden léxico ascendente. <br/>                                                                             |



 

### <a name="longnames-member"></a>Miembro Longnames

El nombre del miembro longnames es "//". El miembro longnames es una serie de cadenas de nombres de miembro de archivo. Aquí solo aparece un nombre cuando no hay espacio suficiente en el campo Nombre (16 bytes). El miembro longnames es opcional. Puede estar vacío solo con un encabezado o puede estar completamente ausente sin un encabezado.

Las cadenas finalizan en null. Cada cadena comienza inmediatamente después del byte nulo de la cadena anterior.

## <a name="import-library-format"></a>Formato de la biblioteca de importación

- [Importar encabezado](#import-header)
- [Tipo de importación](#import-type)

Las bibliotecas de importación tradicionales, es decir, las bibliotecas que describen las exportaciones de una imagen para que las use otra, suelen seguir el diseño descrito en la sección 7, Formato de archivo de archivo [(biblioteca).](#archive-library-file-format) La principal diferencia es que los miembros de la biblioteca de importación contienen archivos pseudo object en lugar de archivos reales, en los que cada miembro incluye las contribuciones de sección necesarias para compilar las tablas de importación que se describen en la sección 6.4, La sección [.idata](#the-idata-section) El vinculador genera este archivo al compilar la aplicación de exportación.

Las contribuciones de la sección para una importación se pueden deducir a partir de un pequeño conjunto de información. El vinculador puede generar la información completa y detallada en la biblioteca de importación para cada miembro en el momento de la creación de la biblioteca o escribir solo la información canónica en la biblioteca y permitir que la aplicación que la usa más adelante genere los datos necesarios sobre la marcha.

En una biblioteca de importación con el formato long, un solo miembro contiene la siguiente información:

<dl> Encabezado de miembro de archivo  
Encabezado de archivo  
Encabezados de sección  
Datos que corresponden a cada uno de los encabezados de sección  
Tabla de símbolos COFF  
Cadenas  
  
</dl>

Por el contrario, una biblioteca de importación corta se escribe de la siguiente manera:

<dl> Encabezado de miembro de archivo  
Importar encabezado  
Cadena de nombre de importación terminada en NULL  
Cadena de nombre de DLL terminada en NULL  
</dl>

Se trata de información suficiente para reconstruir con precisión todo el contenido del miembro en el momento de su uso.

### <a name="import-header"></a>Importar encabezado

El encabezado import contiene los siguientes campos y desplazamientos:



| Offset         | Size                | Campo                       | Descripción                                                                                                                  |
|----------------|---------------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>       | Sig1 <br/>            | Debe ser IMAGE \_ FILE \_ MACHINE \_ UNKNOWN. Para obtener más información, vea [Tipos de máquina.](#machine-types) <br/>                |
| 2 <br/>  | 2 <br/>       | Sig2 <br/>            | Debe ser 0xFFFF. <br/>                                                                                                  |
| 4 <br/>  | 2 <br/>       | Versión <br/>         | Versión de la estructura. <br/>                                                                                           |
| 6 <br/>  | 2 <br/>       | Máquina <br/>         | Número que identifica el tipo de máquina de destino. Para obtener más información, vea [Tipos de máquina.](#machine-types)<br/> |
| 8 <br/>  | 4 <br/>       | Time-Date stamp <br/> | Hora y fecha en que se creó el archivo. <br/>                                                                     |
| 12 <br/> | 4 <br/>       | Tamaño de los datos <br/>    | Tamaño de las cadenas que siguen al encabezado. <br/>                                                                  |
| 16 <br/> | 2 <br/>       | Ordinal/Sugerencia <br/>    | El ordinal o la sugerencia para la importación, determinado por el valor del campo Tipo de nombre. <br/>                   |
| 18 <br/> | 2 bits <br/>  | Tipo <br/>            | Tipo de importación. Para obtener valores y descripciones específicos, vea [Tipo de importación](#import-type).<br/>                           |
|                | 3 bits <br/>  | Tipo de nombre <br/>       | Tipo de nombre de importación. Para obtener más información, vea [Tipo de nombre de importación](#import-name-type). <br/>                           |
|                | 11 bits <br/> | Reservada <br/>        | Reservado, debe ser 0. <br/>                                                                                             |



 

Esta estructura va seguida de dos cadenas terminadas en NULL que describen el nombre del símbolo importado y el archivo DLL del que salió.

### <a name="import-type"></a>Tipo de importación

Los valores siguientes se definen para el campo Tipo en el encabezado de importación:

| Constante                  | Value         | Descripción                                      |
|---------------------------|---------------|--------------------------------------------------|
| IMPORTAR \_ CÓDIGO <br/>  | 0 <br/> | Código ejecutable. <br/>                     |
| IMPORTAR \_ DATOS <br/>  | 1 <br/> | Datos <br/>                                |
| IMPORT \_ CONST <br/> | 2 <br/> | Se especifica como CONST en el archivo .def. <br/> |

Estos valores se usan para determinar qué contribuciones de sección debe generar la herramienta que usa la biblioteca si debe tener acceso a esos datos.

### <a name="import-name-type"></a>Tipo de nombre de importación

El nombre del símbolo de importación terminado en NULL sigue inmediatamente a su encabezado de importación asociado. Los valores siguientes se definen para el campo Tipo de nombre del encabezado de importación. Indican cómo se va a usar el nombre para generar los símbolos correctos que representan la importación:

| Constante | Value | Descripción |
| - | - | - |
| \_ORDINAL DE IMPORTACIÓN | 0 | La importación es por ordinal. Esto indica que el valor del campo Ordinal/Hint del encabezado de importación es el ordinal de la importación. Si no se especifica esta constante, el campo Ordinal/Hint siempre debe interpretarse como la sugerencia de la importación. |
| NOMBRE DE \_ IMPORTACIÓN | 1 | El nombre de importación es idéntico al nombre del símbolo público. |
| IMPORT \_ NAME \_ NOPREFIX | 2 | El nombre de importación es el nombre del símbolo público, pero omitiendo el signo inicial ?, @u, opcionalmente, \_ . |
| IMPORT \_ NAME \_ UNDECORATE | 3 | El nombre de importación es el nombre del símbolo público, pero omitiendo el inicial ?, @u opcionalmente , y \_ truncando en el primer @ . |

## <a name="appendix-a-calculating-authenticode-pe-image-hash"></a>Apéndice A: Cálculo del hash de imagen de Authenticode PE

- [¿Qué es un hash de imagen de Authenticode PE?](#what-is-an-authenticode-pe-image-hash)
- [¿Qué se trata en un hash de imagen de Authenticode PE?](#what-is-covered-in-an-authenticode-pe-image-hash)

Se espera que se utilicen varios certificados de atributo para comprobar la integridad de las imágenes. Sin embargo, la más común es la firma Authenticode. Se puede usar una firma Authenticode para comprobar que las secciones pertinentes de un archivo de imagen pe no se han modificado de ninguna manera desde el formulario original del archivo. Para llevar a cabo esta tarea, las firmas Authenticode contienen algo denominado hash de imagen pe.

### <a name="what-is-an-authenticode-pe-image-hash"></a>¿Qué es un hash de imagen de Authenticode PE?

El hash de imagen de Authenticode PE, o hash de archivo para abrevía, es similar a una suma de comprobación de archivo, ya que genera un valor pequeño relacionado con la integridad de un archivo. Un algoritmo simple genera una suma de comprobación y se usa principalmente para detectar errores de memoria. Es decir, se usa para detectar si un bloque de memoria en disco ha ido mal y los valores almacenados allí se han dañado. Un hash de archivo es similar a una suma de comprobación en que también detecta daños en los archivos. Sin embargo, a diferencia de la mayoría de los algoritmos de suma de comprobación, es muy difícil modificar un archivo para que tenga el mismo hash de archivo que su formato original (sin modificar). Es decir, una suma de comprobación está pensada para detectar errores de memoria simples que conducen a daños, pero se puede usar un hash de archivo para detectar modificaciones intencionadas e incluso sutiles en un archivo, como las introducidas por virus, hackers o programas de troyanos.

En una firma Authenticode, el hash de archivo se firma digitalmente mediante una clave privada que solo conoce el firmante del archivo. Un consumidor de software puede comprobar la integridad del archivo calculando el valor hash del archivo y comparándolo con el valor de hash firmado contenido en la firma digital Authenticode. Si los hashes de archivo no coinciden, se ha modificado parte del archivo cubierto por el hash de imagen pe.

### <a name="what-is-covered-in-an-authenticode-pe-image-hash"></a>¿Qué se trata en un hash de imagen de Authenticode PE?

No es posible ni deseable incluir todos los datos del archivo de imagen en el cálculo del hash de imagen pe. A veces simplemente presenta características no deseadas (por ejemplo, la información de depuración no se puede quitar de los archivos publicados públicamente); a veces es simplemente imposible. Por ejemplo, no es posible incluir toda la información dentro de un archivo de imagen en una firma Authenticode, luego insertar la firma Authenticode que contiene ese hash de imagen pe en la imagen pe y, posteriormente, poder generar un hash de imagen PE idéntico incluyendo todos los datos del archivo de imagen en el cálculo de nuevo, porque el archivo contiene ahora la firma Authenticode que no estaba originalmente allí.

#### <a name="process-for-generating-the-authenticode-pe-image-hash"></a>Proceso para generar el hash de imagen de Authenticode PE

En esta sección se describe cómo se calcula un hash de imagen pe y qué partes de la imagen pe se pueden modificar sin invalidar la firma Authenticode.

> [!NOTE]
> El hash de imagen pe de un archivo específico se puede incluir en un archivo de catálogo independiente sin incluir un certificado de atributo dentro del archivo con hash. Esto es pertinente, ya que es posible invalidar el hash de imagen pe en un archivo de catálogo firmado por Authenticode modificando una imagen pe que realmente no contiene una firma Authenticode.

Todos los datos de las secciones de la imagen de PE que se especifican en la tabla de secciones tienen hash en su totalidad, excepto los siguientes intervalos de exclusión:

- **Campo CheckSum de archivo del Windows específicos del encabezado opcional.** Esta suma de comprobación incluye todo el archivo (incluidos los certificados de atributo del archivo). Con toda probabilidad, la suma de comprobación será diferente del valor original después de insertar la firma Authenticode.

- **Información relacionada con los certificados de atributo**. Las áreas de la imagen de PE relacionadas con la firma Authenticode no se incluyen en el cálculo del hash de imagen pe porque las firmas authenticode se pueden agregar o quitar de una imagen sin afectar a la integridad general de la imagen. Esto no es un problema, ya que hay escenarios de usuario que dependen de volver a firmar imágenes pe o de agregar una marca de tiempo. Authenticode excluye la siguiente información del cálculo hash:

  - Campo Tabla de certificados de los directorios de datos de encabezado opcionales.

  - La tabla de certificados y los certificados correspondientes a los que apunta el campo Tabla de certificados enumerados inmediatamente arriba.

  Para calcular el hash de imagen pe, Authenticode ordena las secciones especificadas en la tabla de secciones por intervalo de direcciones y, a continuación, aplica un algoritmo hash a la secuencia resultante de bytes, pasando los intervalos de exclusión.

- **Información pasada del final de la última sección.** No se aplica hash al área que se encuentra más allá de la última sección (definida por el desplazamiento más alto). Esta área normalmente contiene información de depuración. Por lo general, la información de depuración se puede considerar como un aviso para los depuradores. no afecta a la integridad real del programa ejecutable. Es muy posible quitar literalmente la información de depuración de una imagen después de que se haya entregado un producto y no afectar a la funcionalidad del programa. De hecho, esto a veces se realiza como una medida de ahorro de disco. Merece la pena tener en cuenta que la información de depuración contenida en las secciones especificadas de la imagen de PE no se puede quitar sin que no se invalide la firma Authenticode.

Puede usar las herramientas makecert y signtool proporcionadas en el SDK de Windows Platform para experimentar con la creación y comprobación de firmas authenticode. Para obtener más información, vea Referencia a continuación.

## <a name="references"></a>Referencias

[Descargas y herramientas para Windows (incluye el SDK Windows)](https://developer.microsoft.com/windows/downloads)

[Creación, visualización y administración de certificados](/windows/desktop/SecCrypto/creating-viewing-and-managing-certificates)

[Tutorial de firma de código en modo kernel (.doc)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/KMCS_Walkthrough.doc)

[SignTool](/windows/desktop/SecCrypto/signtool)

[Windows Formato de firma ejecutable portable authenticode (.docx)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx)

[ImageHlp (Funciones)](/windows/desktop/Debug/imagehlp-functions)
