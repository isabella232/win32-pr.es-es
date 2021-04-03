---
description: Esta especificación describe la estructura de los archivos ejecutables (imagen) y los archivos objeto de la familia de sistemas operativos Windows. Estos archivos se denominan archivos ejecutables portables (PE) y archivos de formato de archivo de objeto común (COFF), respectivamente.
ms.assetid: 3dbfbf7f-6662-45a4-99f1-e0e24c370dee
title: Formato PE
ms.topic: article
ms.date: 08/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 257185019f329e0d4431ca61d1d88e2c0347f133
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/04/2021
ms.locfileid: "103997615"
---
# <a name="pe-format"></a>Formato PE

Esta especificación describe la estructura de los archivos ejecutables (imagen) y los archivos objeto de la familia de sistemas operativos Windows. Estos archivos se denominan archivos ejecutables portables (PE) y archivos de formato de archivo de objeto común (COFF), respectivamente.

> [!Note]  
> Este documento se proporciona para ayudar en el desarrollo de herramientas y aplicaciones para Windows, pero no se garantiza que sea una especificación completa en todos los aspectos. Microsoft se reserva el derecho de modificar este documento sin previo aviso.

Esta revisión del archivo ejecutable portable de Microsoft y la especificación de formato de archivo de objeto común reemplaza todas las revisiones anteriores de esta especificación.

## <a name="general-concepts"></a>Conceptos generales

Este documento especifica la estructura de los archivos ejecutables (imagen) y los archivos objeto de la familia de sistemas operativos Microsoft Windows. Estos archivos se denominan archivos ejecutables portables (PE) y archivos de formato de archivo de objeto común (COFF), respectivamente. El nombre "portable ejecutable" hace referencia al hecho de que el formato no es específico de la arquitectura.

En la tabla siguiente se describen algunos conceptos que aparecen a lo largo de esta especificación:

| Nombre                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| certificado de atributo <br/> | Un certificado que se utiliza para asociar instrucciones comprobables con una imagen. Se puede asociar un número de instrucciones comprobables diferentes a un archivo. uno de los más útiles es una instrucción de un fabricante de software que indica cuál es la síntesis del mensaje de la imagen. Una síntesis del mensaje es similar a una suma de comprobación, salvo que es sumamente difícil de falsificar. Por lo tanto, es muy difícil modificar un archivo para que tenga la misma síntesis del mensaje que el archivo original. La instrucción puede comprobarse como realizada por el fabricante mediante esquemas de criptografía de clave pública o privada. En este documento se describen los detalles sobre los certificados de atributo distintos de para permitir su inserción en archivos de imagen. <br/> |
| marca de fecha y hora <br/>       | Un sello que se usa para distintos propósitos en varios lugares en un archivo PE o COFF. En la mayoría de los casos, el formato de cada sello es el mismo que el utilizado por las funciones de tiempo de la biblioteca en tiempo de ejecución de C. En el caso de las excepciones, vea la reproducción del tipo de depuración descriptor de imagen \_ \_ \_ en [tipo de depuración](#debug-type). Si el valor de la marca es 0 o 0xFFFFFFFF, no representa una marca de fecha y hora real o significativa. <br/>                                                                                                                                                                                                                                                                                                                                            |
| puntero de archivo <br/>          | La ubicación de un elemento dentro del propio archivo, antes de que lo procese el enlazador (en el caso de los archivos objeto) o el cargador (en el caso de los archivos de imagen). En otras palabras, se trata de una posición dentro del archivo tal y como se almacena en el disco. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| vinculador <br/>                | Referencia al vinculador que se proporciona con Microsoft Visual Studio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| objeto de archivo <br/>           | Archivo que se proporciona como entrada para el vinculador. El enlazador genera un archivo de imagen, que a su vez se utiliza como entrada por el cargador. El término "archivo objeto" no implica necesariamente ninguna conexión con la programación orientada a objetos. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Reserved, debe ser 0 <br/>   | Una descripción de un campo que indica que el valor del campo debe ser cero para los generadores y los consumidores deben omitir el campo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Dirección virtual relativa (RVA) <br/>                   | En un archivo de imagen, se trata de la dirección de un elemento una vez cargado en la memoria, con la dirección base del archivo de imagen que se resta de él. La RVA de un elemento casi siempre difiere de su posición dentro del archivo en el disco (puntero de archivo). <br/> En un archivo objeto, una RVA es menos significativa porque no se asignan las ubicaciones de memoria. En este caso, una RVA sería una dirección dentro de una sección (descrita más adelante en esta tabla), a la que se aplica posteriormente una reubicación durante la vinculación. Para simplificar, un compilador solo debe establecer la primera RVA de cada sección en cero. <br/>                                                                                                                                         |
| section <br/>               | Unidad básica de código o datos dentro de un archivo PE o COFF. Por ejemplo, todo el código de un archivo objeto se puede combinar en una sola sección o (dependiendo del comportamiento del compilador) cada función puede ocupar su propia sección. Con más secciones, hay más sobrecarga de archivos, pero el vinculador puede vincular en el código de forma más selectiva. Una sección es similar a un segmento en la arquitectura de Intel 8086. Todos los datos sin procesar de una sección se deben cargar de forma contigua. Además, un archivo de imagen puede contener varias secciones, como. TLS o. reloc, que tienen fines especiales. <br/>                                                                                                                                                                      |
| Dirección virtual (VA) <br/>                    | Igual que RVA, salvo que no se resta la dirección base del archivo de imagen. La dirección se denomina Virginia porque Windows crea un espacio de VA distinto para cada proceso, independientemente de la memoria física. Para casi todos los propósitos, un VA se debe considerar solo una dirección. Un VA no es tan predecible como una RVA porque es posible que el cargador no cargue la imagen en su ubicación preferida. <br/>                                                                                                                                                                                                                                                                                                                                        |

## <a name="overview"></a>Información general

En la lista siguiente se describe el formato ejecutable de Microsoft PE, con la base del encabezado de la imagen en la parte superior. La sección del encabezado EXE compatible con MS-DOS 2,0 hasta la sección sin usar, justo antes del encabezado PE, es la sección de MS-DOS 2,0 y solo se utiliza para la compatibilidad con MS-DOS.

-   Encabezado EXE compatible con MS-DOS 2,0
-   unused
-   Identificador OEM

    Información de OEM

    Desplazamiento al encabezado PE

-   Tabla de reubicación y programa de código auxiliar de MS-DOS 2,0

-   unused

-   Encabezado PE (alineado en el límite de 8 bytes)

-   Encabezados de sección
-   Páginas de imagen:

    importar información

    exportar información

    reubicaciones base

    información de recursos

En la lista siguiente se describe el formato de módulo de objeto COFF de Microsoft:

-   Encabezado COFF de Microsoft
-   Encabezados de sección
-   Datos sin procesar:

    código

    datos

    información de depuración

    reubicaciones

## <a name="file-headers"></a>Encabezados de archivo

- [Código auxiliar de MS-DOS (solo imagen)](#ms-dos-stub-image-only)
- [Firma (solo imagen)](#signature-image-only)
- [Encabezado de archivo COFF (objeto e imagen)](#coff-file-header-object-and-image)
  - [Tipos de máquina](#machine-types)
  - [Características](#characteristics)
- [Encabezado opcional (solo imagen)](#optional-header-image-only)
  - [Campos opcionales de encabezado estándar (solo imagen)](#optional-header-standard-fields-image-only)
  - [Encabezado opcional Windows-Specific campos (solo imagen)](#optional-header-windows-specific-fields-image-only)
  - [Directorios de datos de encabezado opcionales (solo imagen)](#optional-header-data-directories-image-only)

El encabezado del archivo PE consta de un código auxiliar de Microsoft MS-DOS, la firma de PE, el encabezado de archivo COFF y un encabezado opcional. Un encabezado de archivo objeto COFF está formado por un encabezado de archivo COFF y un encabezado opcional. En ambos casos, los encabezados de archivo van seguidos inmediatamente de los encabezados de la sección.

### <a name="ms-dos-stub-image-only"></a>Código auxiliar de MS-DOS (solo imagen)

El código auxiliar de MS-DOS es una aplicación válida que se ejecuta en MS-DOS. Se coloca al principio de la imagen del archivo EXE. El enlazador coloca un código auxiliar predeterminado aquí, que imprime el mensaje "este programa no se puede ejecutar en modo de DOS" cuando la imagen se ejecuta en MS-DOS. El usuario puede especificar un código auxiliar diferente mediante la opción/STUB del enlazador.

En la ubicación 0x3c, el código auxiliar tiene el desplazamiento de archivo a la firma de PE. Esta información permite que Windows ejecute correctamente el archivo de imagen, aunque tenga un código auxiliar de MS-DOS. Este desplazamiento de archivo se coloca en la ubicación 0x3c durante la vinculación.

### <a name="signature-image-only"></a>Firma (solo imagen)

Después del código auxiliar de MS-DOS, en el desplazamiento de archivo especificado en offset 0x3c, es una firma de 4 bytes que identifica el archivo como un archivo de imagen con formato PE. Esta firma es "PE \\ 0 \\ 0" (las letras "P" y "e" seguidas de dos bytes null).

### <a name="coff-file-header-object-and-image"></a>Encabezado de archivo COFF (objeto e imagen)

Al principio de un archivo objeto, o inmediatamente después de la firma de un archivo de imagen, es un encabezado de archivo COFF estándar con el siguiente formato. Tenga en cuenta que el cargador de Windows limita el número de secciones a 96.

| Offset         | Tamaño          | Campo                            | Descripción                                                                                                                                                                                                                                                          |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Máquina <br/>              | Número que identifica el tipo de equipo de destino. Para obtener más información, consulte [tipos de máquina](#machine-types). <br/>                                                                                                                                        |
| 2 <br/>  | 2 <br/> | NumberOfSections <br/>     | Número de secciones. Esto indica el tamaño de la tabla de la secciones, que sigue inmediatamente a los encabezados. <br/>                                                                                                                                             |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>        | Los bits 32 bajos del número de segundos trans00:00 curridos desde el 1 de enero de 1970 (un valor t de tiempo de ejecución de C \_ ), que indica cuándo se creó el archivo. <br/>                                                                                                             |
| 8 <br/>  | 4 <br/> | PointerToSymbolTable <br/> | El desplazamiento de archivo de la tabla de símbolos COFF o cero si no hay ninguna tabla de símbolos COFF. Este valor debe ser cero para una imagen porque la información de depuración COFF está en desuso. <br/>                                                                           |
| 12 <br/> | 4 <br/> | NumberOfSymbols <br/>      | Número de entradas de la tabla de símbolos. Estos datos se pueden usar para buscar la tabla de cadenas, que sigue inmediatamente a la tabla de símbolos. Este valor debe ser cero para una imagen porque la información de depuración COFF está en desuso. <br/>                        |
| 16 <br/> | 2 <br/> | SizeOfOptionalHeader <br/> | Tamaño del encabezado opcional, que es necesario para los archivos ejecutables pero no para los archivos objeto. Este valor debe ser cero para un archivo objeto. Para obtener una descripción del formato de encabezado, consulte [encabezado opcional (solo imagen)](#optional-header-image-only). <br/> |
| 18 <br/> | 2 <br/> | Características <br/>      | Marcas que indican los atributos del archivo. Para ver valores de marca específicos, vea [características](#characteristics). <br/>                                                                                                                               |

#### <a name="machine-types"></a>Tipos de máquina

El campo equipo tiene uno de los siguientes valores, que especifican el tipo de CPU. Un archivo de imagen solo se puede ejecutar en el equipo especificado o en un sistema que Emule el equipo especificado.

| Constante                                    | Value              | Descripción                                                                             |
|---------------------------------------------|--------------------|-----------------------------------------------------------------------------------------|
| máquina de archivo de imagen \_ \_ \_ desconocida <br/>   | 0x0 <br/>    | Se supone que el contenido de este campo es aplicable a cualquier tipo de máquina <br/> |
| Máquina de archivos de imagen \_ \_ \_ AM33 <br/>      | 0x1d3 <br/>  | Matsushita AM33 <br/>                                                             |
| Máquina de archivos de imagen \_ \_ \_ AMD64 <br/>     | 0x8664 <br/> | x64 <br/>                                                                         |
| \_ARM del \_ equipo de archivos de imagen \_ <br/>       | 0x1c0 <br/>  | little endian ARM <br/>                                                           |
| Máquina de archivos de imagen \_ \_ \_ ARM64 <br/>     | 0xaa64 <br/> | little endian ARM64 <br/>                                                         |
| máquina de archivos de imagen \_ \_ \_ ARMNT <br/>     | 0x1c4 <br/>  | Control de ARM: 2 little endian <br/>                                                   |
| archivo de imagen del \_ \_ sistema \_ EBC <br/>       | 0xebc <br/>  | Código de byte EFI <br/>                                                               |
| Máquina de archivos de imagen \_ \_ \_ i386 <br/>      | 0x14c <br/>  | Procesadores Intel 386 o posterior y procesadores compatibles <br/>                     |
| Máquina de archivos de imagen \_ \_ \_ ia64 <br/>      | 0x200 <br/>  | Familia de procesadores Intel Itanium <br/>                                              |
| Máquina de archivos de imagen \_ \_ \_ M32R <br/>      | 0x9041 <br/> | little endian Mitsubishi M32R <br/>                                               |
| Máquina de archivos de imagen \_ \_ \_ MIPS16 <br/>    | 0x266 <br/>  | MIPS16 <br/>                                                                      |
| máquina de archivos de imagen \_ \_ \_ MIPSFPU <br/>   | 0x366 <br/>  | MIPS con FPU <br/>                                                               |
| Máquina de archivos de imagen \_ \_ \_ MIPSFPU16 <br/> | 0x466 <br/>  | MIPS16 con FPU <br/>                                                             |
| máquina de archivos de imagen \_ \_ \_ POWERPC <br/>   | 0x1f0 <br/>  | Power PC little endian <br/>                                                      |
| máquina de archivos de imagen \_ \_ \_ POWERPCFP <br/> | 0x1f1 <br/>  | Power PC con compatibilidad de punto flotante <br/>                                        |
| Máquina de archivos de imagen \_ \_ \_ R4000 <br/>     | 0x166 <br/>  | little endian MIPS <br/>                                                          |
| Máquina de archivos de imagen \_ \_ \_ RISCV32 <br/>   | 0x5032 <br/> | RISC-V 32 bits de espacio de direcciones <br/>                                                 |
| Máquina de archivos de imagen \_ \_ \_ RISCV64 <br/>   | 0x5064 <br/> | RISC-V 64 bits de espacio de direcciones <br/>                                                 |
| Máquina de archivos de imagen \_ \_ \_ RISCV128 <br/>  | 0x5128 <br/> | RISC-V 128 bits de espacio de direcciones <br/>                                                |
| Máquina de archivos de imagen \_ \_ \_ SH3 <br/>       | 0x1a2 <br/>  | Hitachi SH3 <br/>                                                                 |
| Máquina de archivos de imagen \_ \_ \_ SH3DSP <br/>    | 0x1a3 <br/>  | DSP de Hitachi SH3 <br/>                                                             |
| Máquina de archivos de imagen \_ \_ \_ SH4 <br/>       | 0x1a6 <br/>  | Hitachi SH4 <br/>                                                                 |
| Máquina de archivos de imagen \_ \_ \_ SH5 <br/>       | 0x1a8 <br/>  | Hitachi SH5 <br/>                                                                 |
| \_control de \_ equipo de archivo de imagen \_ <br/>     | 0x1c2 <br/>  | Thumb <br/>                                                                       |
| Máquina de archivos de imagen \_ \_ \_ WCEMIPSV2 <br/> | 0x169 <br/>  | MIPS Little-endian, WCE V2 <br/>                                                   |

#### <a name="characteristics"></a>Características

El campo características contiene marcas que indican los atributos del archivo de objeto o imagen. Actualmente están definidas las marcas siguientes:

| Marca                                                 | Value              | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| archivo de imagen \_ \_ reubicaciones \_ eliminado <br/>            | 0x0001 <br/> | Solo imagen, Windows CE y Microsoft Windows NT y versiones posteriores. Esto indica que el archivo no contiene reubicaciones base y, por tanto, se debe cargar en su dirección base preferida. Si la dirección base no está disponible, el cargador informa de un error. El comportamiento predeterminado del enlazador es quitar las reubicaciones de base de los archivos ejecutables (EXE). <br/> |
| \_ \_ imagen ejecutable del archivo de imagen \_ <br/>           | 0x0002 <br/> | Solo imagen. Esto indica que el archivo de imagen es válido y se puede ejecutar. Si no se establece esta marca, indica un error del vinculador. <br/>                                                                                                                                                                                                                          |
| línea de archivo de imagen \_ \_ \_ NUMS \_ eliminada <br/>        | 0x0004 <br/> | Se han quitado los números de línea COFF. Esta marca está en desuso y debe ser cero. <br/>                                                                                                                                                                                                                                                                       |
| \_SYMS local de archivo de imagen \_ \_ \_ eliminado <br/>       | 0x0008 <br/> | Se han quitado las entradas de la tabla de símbolos COFF para los símbolos locales. Esta marca está en desuso y debe ser cero. <br/>                                                                                                                                                                                                                                             |
| \_recorte \_ de \_ WS \_ intenso del archivo de imagen <br/>        | 0x0010 <br/> | Obsoleto. Recortar el espacio de trabajo de forma agresiva. Esta marca está en desuso para Windows 2000 y versiones posteriores, y debe ser cero. <br/>                                                                                                                                                                                                                                          |
| \_reconocimiento de \_ \_ dirección grande de archivo \_ de imagen <br/>      | 0x0020 <br/> | La aplicación puede controlar > direcciones de 2 GB. <br/>                                                                                                                                                                                                                                                                                                            |
|                                                      | 0x0040 <br/> | Esta marca se reserva para uso futuro. <br/>                                                                                                                                                                                                                                                                                                                  |
| \_bytes de archivo de imagen \_ \_ invertidas el \_ <br/>         | 0x0080 <br/> | Little Endian: el bit menos significativo (LSB) precede al bit más significativo (MSB) en la memoria. Esta marca está en desuso y debe ser cero. <br/>                                                                                                                                                                                                          |
| Archivo de imagen \_ \_ 32 bits de \_ equipo <br/>              | 0x0100 <br/> | El equipo se basa en una arquitectura de 32 bits-palabra. <br/>                                                                                                                                                                                                                                                                                                        |
| depuración de archivo de imagen \_ \_ \_ eliminada <br/>             | 0x0200 <br/> | La información de depuración se quita del archivo de imagen. <br/>                                                                                                                                                                                                                                                                                                  |
| \_ \_ \_ ejecución extraíble del archivo \_ de imagen desde el \_ intercambio <br/> | 0x0400 <br/> | Si la imagen se encuentra en un medio extraíble, cárguelo completamente y cópielo en el archivo de intercambio. <br/>                                                                                                                                                                                                                                                                        |
| \_archivo \_ de imagen NET \_ Run \_ desde \_ swap <br/>        | 0x0800 <br/> | Si la imagen se encuentra en un medio de red, cárguelo y cópielo en el archivo de intercambio. <br/>                                                                                                                                                                                                                                                                          |
| \_sistema de archivos de imagen \_ <br/>                      | 0x1000 <br/> | El archivo de imagen es un archivo del sistema, no un programa de usuario. <br/>                                                                                                                                                                                                                                                                                                   |
| \_dll del archivo de imagen \_ <br/>                         | 0x2000 <br/> | El archivo de imagen es una biblioteca de vínculos dinámicos (DLL). Estos archivos se consideran archivos ejecutables para casi todos los propósitos, aunque no se pueden ejecutar directamente. <br/>                                                                                                                                                                                              |
| \_archivo de imagen solo en el \_ \_ sistema \_ <br/>            | 0x4000 <br/> | El archivo solo debe ejecutarse en un equipo de uniprocesador. <br/>                                                                                                                                                                                                                                                                                                 |
| \_bytes de archivo de imagen \_ \_ invertidas \_ HI <br/>         | 0x8000 <br/> | Big Endian: el MSB precede al LSB en la memoria. Esta marca está en desuso y debe ser cero. <br/>                                                                                                                                                                                                                                                            |

### <a name="optional-header-image-only"></a>Encabezado opcional (solo imagen)

Cada archivo de imagen tiene un encabezado opcional que proporciona información al cargador. Este encabezado es opcional en el sentido de que algunos archivos (en concreto, archivos objeto) no lo tienen. En el caso de los archivos de imagen, este encabezado es obligatorio. Un archivo objeto puede tener un encabezado opcional, pero generalmente este encabezado no tiene ninguna función en un archivo objeto, salvo para aumentar su tamaño.

Tenga en cuenta que el tamaño del encabezado opcional no es fijo. El campo **SizeOfOptionalHeader** del encabezado COFF debe usarse para validar que un sondeo en el archivo para un directorio de datos determinado no va más allá de **SizeOfOptionalHeader**. Para obtener más información, consulte el [encabezado de archivo COFF (objeto e imagen)](#coff-file-header-object-and-image).

El campo **NumberOfRvaAndSizes** del encabezado opcional también debe usarse para asegurarse de que ningún sondeo para una entrada de directorio de datos determinada va más allá del encabezado opcional. Además, es importante validar el número mágico de encabezado opcional para la compatibilidad de formato.

El número mágico de encabezado opcional determina si una imagen es un PE32 o un ejecutable de PE32 +.

| Número mágico      | Formato PE         |
|-------------------|-------------------|
| 0x10b <br/> | PE32 <br/>  |
| 0x20b <br/> | PE32 + <br/> |

Las imágenes de PE32 + permiten un espacio de direcciones de 64 bits mientras se limita el tamaño de la imagen a 2 gigabytes. Otras modificaciones de PE32 + se tratan en las secciones respectivas.

El propio encabezado opcional tiene tres partes principales.

| Desplazamiento (PE32/PE32 +) | Tamaño (PE32/PE32 +)    | Elemento de encabezado                         | Descripción                                                                                                                                                                   |
|---------------------|----------------------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 28/24 <br/>    | Campos estándar <br/>         | Campos que se definen para todas las implementaciones de COFF, incluido UNIX. <br/>                                                                                          |
| 28/24 <br/>   | 68/88 <br/>    | Campos específicos de Windows <br/> | Campos adicionales para admitir características específicas de Windows (por ejemplo, subsistemas). <br/>                                                                              |
| 96/112 <br/>  | Variable <br/> | Directorios de datos <br/>        | Pares de dirección/tamaño para las tablas especiales que se encuentran en el archivo de imagen y que usa el sistema operativo (por ejemplo, la tabla de importación y la tabla de exportación). <br/> |

#### <a name="optional-header-standard-fields-image-only"></a>Campos opcionales de encabezado estándar (solo imagen)

Los ocho primeros campos del encabezado opcional son campos estándar que se definen para cada implementación de COFF. Estos campos contienen información general que es útil para cargar y ejecutar un archivo ejecutable. No se modifican en el formato PE32 +.

| Offset         | Tamaño          | Campo                               | Descripción                                                                                                                                                                                                                                                                                                                                   |
|----------------|---------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Instrucción mágica <br/>                   | Entero sin signo que identifica el estado del archivo de imagen. El número más común es 0x10B, que lo identifica como un archivo ejecutable normal. 0x107 lo identifica como una imagen de ROM y 0x20B lo identifica como un ejecutable de PE32 +. <br/>                                                                                            |
| 2 <br/>  | 1 <br/> | MajorLinkerVersion <br/>      | El número de versión principal del enlazador. <br/>                                                                                                                                                                                                                                                                                                  |
| 3 <br/>  | 1 <br/> | MinorLinkerVersion <br/>      | El número de versión secundaria del enlazador. <br/>                                                                                                                                                                                                                                                                                                  |
| 4 <br/>  | 4 <br/> | SizeOfCode <br/>              | Tamaño de la sección de código (texto) o la suma de todas las secciones de código si hay varias secciones. <br/>                                                                                                                                                                                                                              |
| 8 <br/>  | 4 <br/> | SizeOfInitializedData <br/>   | Tamaño de la sección de datos inicializados o la suma de todas estas secciones si hay varias secciones de datos. <br/>                                                                                                                                                                                                                    |
| 12 <br/> | 4 <br/> | SizeOfUninitializedData <br/> | El tamaño de la sección de datos no inicializados (BSS) o la suma de todas estas secciones si hay varias secciones de BSS. <br/>                                                                                                                                                                                                             |
| 16 <br/> | 4 <br/> | AddressOfEntryPoint <br/>     | La dirección del punto de entrada relativa a la base de la imagen cuando el archivo ejecutable se carga en la memoria. En el caso de las imágenes de programa, esta es la dirección de inicio. En el caso de los controladores de dispositivos, se trata de la dirección de la función de inicialización. Un punto de entrada es opcional para los archivos dll. Cuando no hay ningún punto de entrada presente, este campo debe ser cero. <br/> |
| 20 <br/> | 4 <br/> | BaseOfCode <br/>              | Dirección relativa a la base de la imagen de la sección de principio de código cuando se carga en la memoria. <br/>                                                                                                                                                                                                                    |

PE32 contiene este campo adicional, que está ausente en PE32 +, después de BaseOfCode.

| Offset         | Tamaño          | Campo                  | Descripción                                                                                                                |
|----------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------|
| 24 <br/> | 4 <br/> | BaseOfData <br/> | Dirección relativa a la base de la imagen de la sección de inicio de datos cuando se carga en la memoria. <br/> |

#### <a name="optional-header-windows-specific-fields-image-only"></a>Encabezado opcional Windows-Specific campos (solo imagen)

Los 21 campos siguientes son una extensión del formato de encabezado opcional COFF. Contienen información adicional requerida por el enlazador y el cargador en Windows.

| Desplazamiento (PE32/PE32 +) | Tamaño (PE32/PE32 +) | Campo                                   | Descripción                                                                                                                                                                                                                                                                                                            |
|----------------------|--------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 28/24 <br/>    | 4/8 <br/>    | ImageBase <br/>                   | Dirección preferida del primer byte de la imagen cuando se carga en la memoria; debe ser un múltiplo de 64 K. El valor predeterminado para los archivos dll es 0x10000000. El valor predeterminado de Windows CE exe es 0x00010000. El valor predeterminado de Windows NT, Windows 2000, Windows XP, Windows 95, Windows 98 y Windows me es 0x00400000. <br/>       |
| 32/32 <br/>    | 4 <br/>      | SectionAlignment <br/>            | La alineación (en bytes) de las secciones cuando se cargan en la memoria. Debe ser mayor o igual que FileAlignment. El valor predeterminado es el tamaño de página de la arquitectura. <br/>                                                                                                                               |
| 36/36 <br/>    | 4 <br/>      | FileAlignment <br/>               | El factor de alineación (en bytes) que se usa para alinear los datos sin procesar de las secciones del archivo de imagen. El valor debe ser una potencia de 2 entre 512 y 64 K, ambos incluidos. El valor predeterminado es 512. Si alineación es menor que el tamaño de página de la arquitectura, FileAlignment debe coincidir con alineación. <br/> |
| 40/40 <br/>    | 2 <br/>      | MajorOperatingSystemVersion <br/> | El número de versión principal del sistema operativo obligatorio. <br/>                                                                                                                                                                                                                                                 |
| 42/42 <br/>    | 2 <br/>      | MinorOperatingSystemVersion <br/> | El número de versión secundaria del sistema operativo obligatorio. <br/>                                                                                                                                                                                                                                                 |
| 44/44 <br/>    | 2 <br/>      | MajorImageVersion <br/>           | El número de versión principal de la imagen. <br/>                                                                                                                                                                                                                                                                     |
| 46/46 <br/>    | 2 <br/>      | MinorImageVersion <br/>           | El número de versión secundaria de la imagen. <br/>                                                                                                                                                                                                                                                                     |
| 48/48 <br/>    | 2 <br/>      | MajorSubsystemVersion <br/>       | El número de versión principal del subsistema. <br/>                                                                                                                                                                                                                                                                 |
| 50/50 <br/>    | 2 <br/>      | MinorSubsystemVersion <br/>       | El número de versión secundaria del subsistema. <br/>                                                                                                                                                                                                                                                                 |
| 52/52 <br/>    | 4 <br/>      | Win32VersionValue <br/>           | Reserved, debe ser cero. <br/>                                                                                                                                                                                                                                                                                    |
| 56/56 <br/>    | 4 <br/>      | SizeOfImage <br/>                 | Tamaño (en bytes) de la imagen, incluidos todos los encabezados, a medida que la imagen se carga en la memoria. Debe ser un múltiplo de alineación. <br/>                                                                                                                                                                      |
| 60/60 <br/>    | 4 <br/>      | SizeOfHeaders <br/>               | El tamaño combinado de un código auxiliar de MS-DOS, un encabezado PE y encabezados de sección se redondea a un múltiplo de FileAlignment. <br/>                                                                                                                                                                                             |
| 64/64 <br/>    | 4 <br/>      | MD5 <br/>                    | Suma de comprobación del archivo de imagen. El algoritmo para calcular la suma de comprobación se incorpora en IMAGHELP.DLL. A continuación se comprueba la validación en tiempo de carga: todos los controladores, los archivos DLL cargados durante el arranque y cualquier archivo DLL que se cargue en un proceso crítico de Windows. <br/>                                          |
| 68/68 <br/>    | 2 <br/>      | Subsystem <br/>                   | El subsistema necesario para ejecutar esta imagen. Para obtener más información, consulte el [subsistema de Windows](#windows-subsystem). <br/>                                                                                                                                                                                       |
| 70/70 <br/>    | 2 <br/>      | DllCharacteristics <br/>          | Para obtener más información, vea [características de dll](#dll-characteristics) más adelante en esta especificación. <br/>                                                                                                                                                                                                         |
| 72/72 <br/>    | 4/8 <br/>    | SizeOfStackReserve <br/>          | El tamaño de la pila que se va a reservar. Solo se confirma SizeOfStackCommit; el resto se pone a disposición de una página a la vez hasta que se alcanza el tamaño de reserva. <br/>                                                                                                                                                    |
| 76/80 <br/>    | 4/8 <br/>    | SizeOfStackCommit <br/>           | El tamaño de la pila que se va a confirmar. <br/>                                                                                                                                                                                                                                                                           |
| 80/88 <br/>    | 4/8 <br/>    | SizeOfHeapReserve <br/>           | El tamaño del espacio de montón local que se va a reservar. Solo se confirma SizeOfHeapCommit; el resto se pone a disposición de una página a la vez hasta que se alcanza el tamaño de reserva. <br/>                                                                                                                                          |
| 84/96 <br/>    | 4/8 <br/>    | SizeOfHeapCommit <br/>            | El tamaño del espacio de montón local que se va a confirmar. <br/>                                                                                                                                                                                                                                                                |
| 88/104 <br/>   | 4 <br/>      | LoaderFlags <br/>                 | Reserved, debe ser cero. <br/>                                                                                                                                                                                                                                                                                    |
| 92/108 <br/>   | 4 <br/>      | NumberOfRvaAndSizes <br/>         | El número de entradas del directorio de datos en el resto del encabezado opcional. Cada una describe una ubicación y un tamaño. <br/>                                                                                                                                                                                          |

##### <a name="windows-subsystem"></a>Subsistema de Windows

Los siguientes valores definidos para el campo Subsystem del encabezado opcional determinan qué subsistema de Windows (si existe) se requiere para ejecutar la imagen.

| Constante                                                  | Value          | Descripción                                                      |
|-----------------------------------------------------------|----------------|------------------------------------------------------------------|
| subsistema de imagen \_ \_ desconocido <br/>                     | 0 <br/>  | Un subsistema desconocido <br/>                                 |
| subsistema de imagen \_ \_ nativo <br/>                      | 1 <br/>  | Controladores de dispositivos y procesos nativos de Windows <br/>          |
| \_GUI de Windows de subsistema de imagen \_ \_ <br/>                | 2 <br/>  | El subsistema de la interfaz gráfica de usuario (GUI) de Windows <br/> |
| subsistema de imagen de \_ \_ Windows \_ Cui <br/>                | 3 <br/>  | El subsistema de caracteres de Windows <br/>                      |
| Subsistema de imagen \_ \_ OS2 \_ Cui <br/>                    | 5 <br/>  | El subsistema de caracteres SO/2 <br/>                         |
| subsistema de imagen \_ \_ POSIX \_ Cui <br/>                  | 7 <br/>  | El subsistema de caracteres POSIX <br/>                        |
| \_ \_ ventanas nativas de subsistema de imagen \_ <br/>             | 8 <br/>  | Controlador Win9x nativo <br/>                                  |
| \_ \_ GUI de Windows \_ CE \_ de subsistema de imagen <br/>            | 9 <br/>  | Windows CE <br/>                                           |
| \_aplicación EFI de subsistema de imagen \_ \_ <br/>            | 10 <br/> | Una aplicación Extensible Firmware Interface (EFI) <br/>   |
| \_ \_ controlador del servicio de arranque de EFI de subsistema de imagen \_ \_ \_ <br/> | 11 <br/> | Un controlador EFI con servicios de arranque <br/>                     |
| \_ \_ \_ controlador en tiempo de ejecución EFI de subsistema de imagen \_ <br/>       | 12 <br/> | Un controlador EFI con servicios en tiempo de ejecución <br/>                 |
| subsistema de imagen \_ \_ EFI \_ ROM <br/>                    | 13 <br/> | Una imagen de EFI ROM <br/>                                     |
| subsistema de imagen \_ \_ Xbox <br/>                        | 14 <br/> | XBOX <br/>                                                 |
| \_aplicación de arranque de Windows del subsistema de imagen \_ \_ \_ <br/>  | 16 <br/> | Aplicación de arranque de Windows. <br/>                            |

##### <a name="dll-characteristics"></a>Características de DLL

Los siguientes valores se definen para el campo DllCharacteristics del encabezado opcional.

| Constante                                                             | Value              | Descripción                                                                                             |
|----------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------|
|                                                                      | 0x0001 <br/> | Reserved, debe ser cero. <br/>                                                                     |
|                                                                      | 0x0002 <br/> | Reserved, debe ser cero. <br/>                                                                     |
|                                                                      | 0x0004 <br/> | Reserved, debe ser cero. <br/>                                                                     |
|                                                                      | 0x0008 <br/> | Reserved, debe ser cero. <br/>                                                                     |
| IMAGEN \_ DLLCHARACTERISTICS \_ alta \_ entropía \_ va <br/>             | 0x0020 <br/> | La imagen puede controlar un espacio de direcciones virtuales de alta entropía de 64 bits. <br/>                               |
| IMAGEN \_ DLLCHARACTERISTICS\_ <br/> \_base dinámica <br/>    | 0x0040 <br/> | DLL se puede reubicar en tiempo de carga. <br/>                                                          |
| IMAGEN \_ DLLCHARACTERISTICS\_ <br/> FORZAr la \_ integridad <br/> | 0x0080 <br/> | Se aplican comprobaciones de integridad de código. <br/>                                                         |
| IMAGEN \_ DLLCHARACTERISTICS\_ <br/> compatibilidad con NX \_ <br/>       | 0x0100 <br/> | La imagen es compatible con NX. <br/>                                                                     |
| IMAGE \_ DLLCHARACTERISTICS \_ no \_ Isolation <br/>                | 0x0200 <br/> | El aislamiento es compatible, pero no aísla la imagen. <br/>                                              |
| IMAGE \_ DLLCHARACTERISTICS \_ no \_ SEH <br/>                      | 0x0400 <br/> | No usa el control de excepciones estructurado (SE). No se puede llamar a ningún controlador SE en esta imagen. <br/> |
| IMAGEN \_ DLLCHARACTERISTICS \_ sin \_ enlace <br/>                     | 0x0800 <br/> | No enlazar la imagen. <br/>                                                                      |
| IMAGEN \_ DLLCHARACTERISTICS \_ APPCONTAINER <br/>                  | 0x1000 <br/> | La imagen debe ejecutarse en un AppContainer. <br/>                                                      |
| \_ \_ controlador WDM de Image DLLCHARACTERISTICS \_ <br/>                  | 0x2000 <br/> | Un controlador WDM. <br/>                                                                               |
| DLLCHARACTERISTICS de protección de imagen \_ \_ \_ CF <br/>                     | 0x4000 <br/> | La imagen es compatible con la protección de flujo de control. <br/>                                                          |
| IMAGEN \_ DLLCHARACTERISTICS \_ compatible con terminal \_ Server \_ <br/>      | 0x8000 <br/> | Terminal Server compatible. <br/>                                                                      |

#### <a name="optional-header-data-directories-image-only"></a>Directorios de datos de encabezado opcionales (solo imagen)

Cada directorio de datos proporciona la dirección y el tamaño de una tabla o cadena que usa Windows. Estas entradas de directorio de datos se cargan en la memoria para que el sistema pueda usarlas en tiempo de ejecución. Un directorio de datos es un campo de 8 bytes que tiene la siguiente declaración:

```cpp
typedef struct _IMAGE_DATA_DIRECTORY {
    DWORD   VirtualAddress;
    DWORD   Size;
} IMAGE_DATA_DIRECTORY, *PIMAGE_DATA_DIRECTORY;
```

El primer campo, VirtualAddress, es realmente la RVA de la tabla. La RVA es la dirección de la tabla relativa a la dirección base de la imagen cuando se carga la tabla. El segundo campo proporciona el tamaño en bytes. Los directorios de datos, que forman la última parte del encabezado opcional, se muestran en la tabla siguiente.

Tenga en cuenta que el número de directorios no es fijo. Antes de buscar un directorio específico, compruebe el campo NumberOfRvaAndSizes del encabezado opcional.

Además, no suponga que las RVA de esta tabla apuntan al principio de una sección o que las secciones que contienen tablas específicas tienen nombres específicos.

| Desplazamiento (PE/PE32 +)   | Tamaño          | Campo                               | Descripción                                                                                                                                                                          |
|---------------------|---------------|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 96/112 <br/>  | 8 <br/> | Exportar tabla <br/>            | La dirección y el tamaño de la tabla de exportación. Para obtener más información [, vea la sección. EDATA (solo imagen)](#the-edata-section-image-only). <br/>                                                |
| 104/120 <br/> | 8 <br/> | Importar tabla <br/>            | La dirección y el tamaño de la tabla de importación. Para obtener más información, vea [la sección. idata](#the-idata-section).<br/>                                                                    |
| 112/128 <br/> | 8 <br/> | Tabla de recursos <br/>          | La dirección y el tamaño de la tabla de recursos. Para obtener más información, vea [la sección. rsrc](#the-rsrc-section).<br/>                                                                    |
| 120/136 <br/> | 8 <br/> | Tabla de excepciones <br/>         | La dirección y el tamaño de la tabla de excepciones. Para obtener más información, vea [la sección. pdata](#the-pdata-section). <br/>                                                                |
| 128/144 <br/> | 8 <br/> | Tabla de certificados <br/>       | La dirección y el tamaño de la tabla de certificados de atributos. Para obtener más información, vea [la tabla de certificados de atributo (solo imagen)](#the-attribute-certificate-table-image-only). <br/> |
| 136/152 <br/> | 8 <br/> | Tabla de reubicación base <br/>   | La dirección y el tamaño de la tabla de reubicación de base. Para obtener más información, vea [la sección. reloc (solo imagen)](#the-reloc-section-image-only).<br/>                                   |
| 144/160 <br/> | 8 <br/> | Depuración <br/>                   | La dirección y el tamaño de inicio de los datos de depuración. Para obtener más información, vea [la sección. Debug](#the-debug-section).<br/>                                                             |
| 152/168 <br/> | 8 <br/> | Architecture <br/>            | Reserved, debe ser 0 <br/>                                                                                                                                                      |
| 160/176 <br/> | 8 <br/> | PTR global <br/>              | RVA del valor que se va a almacenar en el registro de puntero global. El miembro de tamaño de esta estructura debe establecerse en cero. <br/>                                                 |
| 168/184 <br/> | 8 <br/> | Tabla de TLS <br/>               | La dirección y el tamaño de la tabla de almacenamiento local de subprocesos (TLS). Para obtener más información, [la sección. TLS](#the-tls-section).<br/>                                                        |
| 176/192 <br/> | 8 <br/> | Cargar tabla de configuración <br/>       | La dirección y el tamaño de la tabla de configuración de carga. Para obtener más información, [la estructura de configuración de carga (solo imagen)](#the-load-configuration-structure-image-only).<br/>       |
| 184/200 <br/> | 8 <br/> | Importación enlazada <br/>            | La dirección y el tamaño de la tabla de importación enlazada. <br/>                                                                                                                                 |
| 192/208 <br/> | 8 <br/> | IAT <br/>                     | La dirección y el tamaño de la tabla de direcciones de importación. Para obtener más información, consulte [Import Address Table](#import-address-table).<br/>                                                 |
| 200/216 <br/> | 8 <br/> | Descriptor de importación de retraso <br/> | La dirección y el tamaño del descriptor de importación de retraso. Para obtener más información, vea [tablas de importación de carga retrasada (solo imagen)](#delay-load-import-tables-image-only).<br/>                    |
| 208/224 <br/> | 8 <br/> | Encabezado Runtime de CLR <br/>      | La dirección y el tamaño del encabezado de tiempo de ejecución de CLR. Para obtener más información, vea [la sección. cormeta (solo objeto)](#the-cormeta-section-object-only).<br/>                                |
| 216/232 <br/> | 8 <br/> | Reserved, debe ser cero <br/>  |                                                                                                                                                                                      |

La entrada de la tabla de certificados apunta a una tabla de certificados de atributos. Estos certificados no se cargan en la memoria como parte de la imagen. Como tal, el primer campo de esta entrada, que suele ser una RVA, es un puntero de archivo en su lugar.

## <a name="section-table-section-headers"></a>Tabla de sección (encabezados de sección)

- [Marcas de sección](#section-flags)
- [Secciones agrupadas (solo objeto)](#grouped-sections-object-only)

Cada fila de la tabla de la sección es, en efecto, un encabezado de sección. Esta tabla sigue inmediatamente al encabezado opcional, si existe. Esta posición es necesaria porque el encabezado del archivo no contiene un puntero directo a la tabla de la sección. En su lugar, la ubicación de la tabla de la sección se determina calculando la ubicación del primer byte después de los encabezados. Asegúrese de usar el tamaño del encabezado opcional tal como se especifica en el encabezado del archivo.

El campo NumberOfSections del encabezado del archivo proporciona el número de entradas de la tabla de la sección. Las entradas de la tabla de la sección se numeran a partir de una (1). Las entradas de la sección de memoria de datos y código se encuentran en el orden elegido por el enlazador.

En un archivo de imagen, el enlazador debe asignar las secciones VAs para para que estén en orden ascendente y adyacente, y deben ser un múltiplo del valor alineación en el encabezado opcional.

Cada encabezado de sección (entrada de tabla de sección) tiene el formato siguiente, para un total de 40 bytes por entrada.



| Offset         | Tamaño          | Campo                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Nombre <br/>                 | Cadena con codificación UTF-8 de 8 bytes rellenada en NULL. Si la cadena tiene una longitud exacta de 8 caracteres, no habrá terminación nula. En el caso de nombres más largos, este campo contiene una barra diagonal (/) seguida de una representación ASCII de un número decimal que es un desplazamiento en la tabla de cadenas. Las imágenes ejecutables no utilizan una tabla de cadenas y no admiten nombres de sección de más de 8 caracteres. Los nombres largos de los archivos objeto se truncan si se emiten para un archivo ejecutable. <br/>                                         |
| 8 <br/>  | 4 <br/> | VirtualSize <br/>          | Tamaño total de la sección cuando se carga en la memoria. Si este valor es mayor que SizeOfRawData, la sección se rellenará con ceros. Este campo solo es válido para las imágenes ejecutables y debe establecerse en cero para los archivos objeto. <br/>                                                                                                                                                                                                                                                                                           |
| 12 <br/> | 4 <br/> | VirtualAddress <br/>       | En el caso de las imágenes ejecutables, la dirección del primer byte de la sección relativa a la base de la imagen cuando la sección se carga en la memoria. En el caso de los archivos objeto, este campo es la dirección del primer byte antes de que se aplique la reubicación; para simplificar, los compiladores deben establecer este valor en cero. De lo contrario, es un valor arbitrario que se resta de los desplazamientos durante la reubicación. <br/>                                                                                                                                         |
| 16 <br/> | 4 <br/> | SizeOfRawData <br/>        | El tamaño de la sección (para archivos objeto) o el tamaño de los datos inicializados en disco (para archivos de imagen). En el caso de las imágenes ejecutables, debe ser un múltiplo de FileAlignment del encabezado opcional. Si es menor que VirtualSize, el resto de la sección se rellena con ceros. Dado que el campo SizeOfRawData se redondea pero el campo VirtualSize no lo es, es posible que SizeOfRawData sea mayor que VirtualSize. Cuando una sección solo contiene datos no inicializados, este campo debe ser cero. <br/> |
| 20 <br/> | 4 <br/> | PointerToRawData <br/>     | Puntero de archivo a la primera página de la sección dentro del archivo COFF. En el caso de las imágenes ejecutables, debe ser un múltiplo de FileAlignment del encabezado opcional. En el caso de los archivos de objeto, el valor se debe alinear en un límite de 4 bytes para obtener el mejor rendimiento. Cuando una sección solo contiene datos no inicializados, este campo debe ser cero. <br/>                                                                                                                                                                               |
| 24 <br/> | 4 <br/> | PointerToRelocations <br/> | Puntero de archivo al principio de las entradas de reubicación de la sección. Se establece en cero para las imágenes ejecutables o si no hay reubicaciones. <br/>                                                                                                                                                                                                                                                                                                                                                                   |
| 28 <br/> | 4 <br/> | PointerToLinenumbers <br/> | Puntero de archivo al principio de las entradas de número de línea de la sección. Se establece en cero si no hay números de línea COFF. Este valor debe ser cero para una imagen porque la información de depuración COFF está en desuso. <br/>                                                                                                                                                                                                                                                                                            |
| 32 <br/> | 2 <br/> | NumberOfRelocations <br/>  | El número de entradas de reubicación para la sección. Se establece en cero para las imágenes ejecutables. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 34 <br/> | 2 <br/> | NumberOfLinenumbers <br/>  | Número de entradas de número de línea de la sección. Este valor debe ser cero para una imagen porque la información de depuración COFF está en desuso. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| 36 <br/> | 4 <br/> | Características <br/>      | Marcas que describen las características de la sección. Para obtener más información, vea [marcas de sección](#section-flags).<br/>                                                                                                                                                                                                                                                                                                                                                                                                |



 

### <a name="section-flags"></a>Marcas de sección

Las marcas de sección del campo características del encabezado de la sección indican las características de la sección.



| Marca                                              | Value                  | Descripción                                                                                                                                                                 |
|---------------------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                   | 0x00000000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
|                                                   | 0x00000001 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
|                                                   | 0x00000002 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
|                                                   | 0x00000004 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| tipo de imagen de \_ SCN \_ \_ sin \_ Panel <br/>             | 0x00000008 <br/> | La sección no se debe rellenar hasta el siguiente límite. Esta marca está obsoleta y se ha reemplazado por IMAGE \_ SCN \_ align \_ 1BYTES. Esto solo es válido para los archivos objeto. <br/> |
|                                                   | 0x00000010 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| \_código de \_ CNT de Image \_ <br/>                 | 0x00000020 <br/> | La sección contiene código ejecutable. <br/>                                                                                                                           |
| \_ \_ \_ datos inicializados de la imagen SCN de CNT \_ <br/>    | 0x00000040 <br/> | La sección contiene datos inicializados. <br/>                                                                                                                          |
| IMAGEN \_ de \_ datos de CNT \_ sin inicializar \_ <br/> | 0x00000080 <br/> | La sección contiene datos no inicializados. <br/>                                                                                                                        |
| IMAGEN \_ SCN \_ lnk \_ otro <br/>                | 0x00000100 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ lnk \_ info <br/>                 | 0x00000200 <br/> | La sección contiene comentarios u otra información. La sección. drectve tiene este tipo. Esto solo es válido para los archivos objeto. <br/>                                    |
|                                                   | 0x00000400 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ lnk \_ Remove <br/>               | 0x00000800 <br/> | La sección no pasará a formar parte de la imagen. Esto solo es válido para los archivos objeto. <br/>                                                                             |
| IMAGE \_ SCN \_ lnk \_ COMDAT <br/>               | 0x00001000 <br/> | La sección contiene datos de COMDAT. Para obtener más información, consulte [secciones COMDAT (solo objeto)](#comdat-sections-object-only). Esto solo es válido para los archivos objeto. <br/> |
| IMAGE \_ SCN \_ GPREL <br/>                     | 0x00008000 <br/> | La sección contiene datos a los que se hace referencia a través del puntero global (GP). <br/>                                                                                           |
| IMAGEN de la \_ memoria de SCN \_ \_ depurable <br/>            | 0x00020000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| \_Memoria de \_ \_ 16 bits de la imagen SCN <br/>                | 0x00020000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGEN de la \_ \_ memoria SCN \_ bloqueada <br/>               | 0x00040000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| \_ \_ carga previa de MEM de Image SCN \_ <br/>              | 0x00080000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ align \_ 1BYTES <br/>             | 0x00100000 <br/> | Alinear los datos en un límite de 1 byte. Válido solo para archivos objeto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ align \_ 2BYTES <br/>             | 0x00200000 <br/> | Alinear los datos en un límite de 2 bytes. Válido solo para archivos objeto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ align \_ 4BYTES <br/>             | 0x00300000 <br/> | Alinear datos en un límite de 4 bytes. Válido solo para archivos objeto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ align \_ 8BYTES <br/>             | 0x00400000 <br/> | Alinear los datos en un límite de 8 bytes. Válido solo para archivos objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 16BYTES <br/>            | 0x00500000 <br/> | Alinear datos en un límite de 16 bytes. Válido solo para archivos objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 32BYTES <br/>            | 0x00600000 <br/> | Alinear datos en un límite de 32 bytes. Válido solo para archivos objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 64BYTES <br/>            | 0x00700000 <br/> | Alinear datos en un límite de 64 bytes. Válido solo para archivos objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 128BYTES <br/>           | 0x00800000 <br/> | Alinear datos en un límite de 128 bytes. Válido solo para archivos objeto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ align \_ 256BYTES <br/>           | 0x00900000 <br/> | Alinear datos en un límite de 256 bytes. Válido solo para archivos objeto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ align \_ 512BYTES <br/>           | 0x00A00000 <br/> | Alinear datos en un límite de 512 bytes. Válido solo para archivos objeto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ align \_ 1024BYTES <br/>          | 0x00B00000 <br/> | Alinear datos en un límite de 1024 bytes. Válido solo para archivos objeto. <br/>                                                                                                |
| IMAGE \_ SCN \_ align \_ 2048BYTES <br/>          | 0x00C00000 <br/> | Alinear datos en un límite de 2048 bytes. Válido solo para archivos objeto. <br/>                                                                                                |
| IMAGE \_ SCN \_ align \_ 4096BYTES <br/>          | 0x00D00000 <br/> | Alinear datos en un límite de 4096 bytes. Válido solo para archivos objeto. <br/>                                                                                                |
| IMAGE \_ SCN \_ align \_ 8192BYTES <br/>          | 0x00E00000 <br/> | Alinear datos en un límite de 8192 bytes. Válido solo para archivos objeto. <br/>                                                                                               |
| IMAGE \_ SCN \_ lnk \_ NRELOC \_ OVFL <br/>         | 0x01000000 <br/> | La sección contiene reubicaciones extendidas. <br/>                                                                                                                      |
| IMAGEN de la \_ \_ memoria SCN \_ descartable <br/>          | 0x02000000 <br/> | La sección se puede descartar según sea necesario. <br/>                                                                                                                         |
| memoria de la memoria \_ SCN \_ \_ no \_ almacenada en caché <br/>          | 0x04000000 <br/> | No se puede almacenar en caché la sección. <br/>                                                                                                                                   |
| \_ \_ memoria \_ no \_ paginada de la imagen SCN <br/>           | 0x08000000 <br/> | La sección no es paginable. <br/>                                                                                                                                    |
| IMAGEN de la \_ memoria de SCN \_ \_ compartida <br/>               | 0x10000000 <br/> | La sección puede compartirse en memoria. <br/>                                                                                                                            |
| IMAGE \_ SCN \_ MEM \_ Execute <br/>              | 0x20000000 <br/> | La sección se puede ejecutar como código. <br/>                                                                                                                            |
| IMAGEN \_ de \_ memoria de SCN \_ leída <br/>                 | 0x40000000 <br/> | Se puede leer la sección. <br/>                                                                                                                                        |
| escritura de MEM de IMAGE \_ SCN \_ \_ <br/>                | 0x80000000 <br/> | Se puede escribir en la sección. <br/>                                                                                                                                  |



 

IMAGE \_ SCN \_ lnk \_ NRELOC \_ OVFL indica que el recuento de reubicaciones de la sección supera los 16 bits que están reservados para ella en el encabezado de la sección. Si se establece el bit y el campo NumberOfRelocations del encabezado de sección es 0xFFFF, el recuento de reubicación real se almacena en el campo VirtualAddress de 32 bits de la primera reubicación. Es un error si \_ \_ se establece Image SCN lnk \_ NRELOC \_ OVFL y hay menos de 0xFFFF reubicaciones en la sección.

### <a name="grouped-sections-object-only"></a>Secciones agrupadas (solo objeto)

El "$"? el carácter (signo de dólar) tiene una interpretación especial en los nombres de sección de los archivos objeto.

Al determinar la sección de la imagen que contendrá el contenido de una sección de objeto, el vinculador descarta la "$"? y todos los caracteres que los siguen. Por lo tanto, una sección de objeto denominada. el **texto $ X** contribuye realmente a la sección **. Text** de la imagen.

Sin embargo, los caracteres que siguen a la "$" Determine el orden de las contribuciones a la sección de la imagen. Todas las contribuciones con el mismo nombre de sección de objeto se asignan de forma contigua en la imagen y los bloques de contribuciones se ordenan en orden léxico por nombre de sección de objeto. Por lo tanto, todos los archivos de objeto con nombre de sección **. Text $ X** terminan juntos, después de las contribuciones **. Text $ W** y antes de las contribuciones **. Text $ Y** .

El nombre de sección de un archivo de imagen nunca contiene un "$"? .

## <a name="other-contents-of-the-file"></a>Otro contenido del archivo

- [Datos de sección](#section-data)
- [Reubicaciones COFF (solo objeto)](#coff-relocations-object-only)
  - [Indicadores de tipo](#type-indicators)
- [Números de línea COFF (desusado)](#coff-line-numbers-deprecated)
- [Tabla de símbolos COFF](#coff-symbol-table)
  - [Representación de nombre de símbolo](#symbol-name-representation)
  - [Valores de número de sección](#section-number-values)
  - [Representación de tipos](#type-representation)
  - [Clase de almacenamiento](#storage-class)
- [Registros de símbolos auxiliares](#auxiliary-symbol-records)
  - [Formato auxiliar 1: definiciones de función](#auxiliary-format-1-function-definitions)
  - [Formato auxiliar 2: símbolos. BF y. EF](#auxiliary-format-2-bf-and-ef-symbols)
  - [Formato auxiliar 3: externos débiles](#auxiliary-format-3-weak-externals)
  - [Formato auxiliar 4: archivos](#auxiliary-format-4-files)
  - [Formato auxiliar 5: definiciones de sección](#auxiliary-format-5-section-definitions)
  - [Secciones COMDAT (solo objeto)](#comdat-sections-object-only)
  - [Definición de token de CLR (solo objeto)](#clr-token-definition-object-only)
- [Tabla de cadenas COFF](#coff-string-table)
- [La tabla de certificados de atributo (solo imagen)](#the-attribute-certificate-table-image-only)
  - [Datos de certificado](#certificate-data)
- [Tablas de importación de carga retrasada (solo imagen)](#delay-load-import-tables-image-only)
  - [Tabla del directorio Delay-Load](#the-delay-load-directory-table)
  - [Atributos](#attributes)
  - [Nombre](#name)
  - [Identificador de módulo](#module-handle)
  - [Tabla de direcciones de importación retrasada](#delay-import-address-table)
  - [Tabla retrasar nombre de importación](#delay-import-name-table)
  - [Tabla de direcciones de importación enlazada retrasada y marca de tiempo](#delay-bound-import-address-table-and-time-stamp)
  - [Tabla de direcciones de importación de descarga retrasada](#delay-unload-import-address-table)

Las estructuras de datos que se han descrito hasta el momento, hasta el encabezado opcional, inclusive, se encuentran en un desplazamiento fijo desde el principio del archivo (o desde el encabezado PE si el archivo es una imagen que contiene un código auxiliar de MS-DOS).

El resto de un objeto COFF o un archivo de imagen contiene bloques de datos que no están necesariamente en ningún desplazamiento de archivo específico. En su lugar, las ubicaciones se definen mediante punteros en el encabezado opcional o en un encabezado de sección.

Una excepción es para las imágenes con un valor de alineación menor que el tamaño de página de la arquitectura (4 K para Intel x86 y para MIPS, y 8 K para Itanium). Para obtener una descripción de alineación, consulte [encabezado opcional (solo imagen)](#optional-header-image-only). En este caso, existen restricciones en el desplazamiento de archivos de los datos de la sección, como se describe en la sección 5,1, "datos de sección". Otra excepción es que la información del certificado de atributo y de depuración debe colocarse al final de un archivo de imagen, con la tabla de certificados de atributo inmediatamente anterior a la sección de depuración, ya que el cargador no las asigna a la memoria. Sin embargo, la regla sobre el certificado de atributo y la información de depuración no se aplica a los archivos objeto.

### <a name="section-data"></a>Datos de sección

Los datos inicializados para una sección se componen de bloques simples de bytes. Sin embargo, para las secciones que contienen ceros, no es necesario incluir los datos de la sección.

Los datos de cada sección se encuentran en el desfase del archivo proporcionado por el campo PointerToRawData en el encabezado de la sección. El tamaño de estos datos en el archivo se indica mediante el campo SizeOfRawData. Si SizeOfRawData es menor que VirtualSize, el resto se rellena con ceros.

En un archivo de imagen, los datos de la sección se deben alinear en un límite tal y como se especifica en el campo FileAlignment del encabezado opcional. Los datos de la sección deben aparecer en el orden de los valores RVA de las secciones correspondientes (como los encabezados de sección individuales en la tabla de la sección).

Hay restricciones adicionales en los archivos de imagen si el valor alineación del encabezado opcional es menor que el tamaño de página de la arquitectura. Para estos archivos, la ubicación de los datos de la sección en el archivo debe coincidir con su ubicación en memoria cuando se carga la imagen, de modo que el desplazamiento físico para los datos de la sección sea el mismo que la RVA.

### <a name="coff-relocations-object-only"></a>Reubicaciones COFF (solo objeto)

Los archivos objeto contienen reubicaciones COFF, que especifican cómo se deben modificar los datos de la sección cuando se colocan en el archivo de imagen y se cargan posteriormente en la memoria.

Los archivos de imagen no contienen reubicaciones COFF, ya que todos los símbolos a los que se hace referencia ya tienen asignadas direcciones en un espacio de direcciones plano. Una imagen contiene información de reubicación en forma de reubicaciones base en la sección. reloc (a menos que la imagen tenga el \_ \_ atributo reubicaciones \_ eliminado). Para obtener más información, vea [la sección. reloc (solo imagen)](#the-reloc-section-image-only).

Para cada sección de un archivo objeto, una matriz de registros de longitud fija contiene las reubicaciones COFF de la sección. La posición y longitud de la matriz se especifican en el encabezado de la sección. Cada elemento de la matriz tiene el formato siguiente.



| Offset        | Tamaño          | Campo                        | Descripción                                                                                                                                                                                                                                                                                                                                                     |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Dirección del elemento al que se aplica la reubicación. Este es el desplazamiento desde el principio de la sección, más el valor del campo RVA/offset de la sección. Vea [tabla de sección (encabezados de sección)](#section-table-section-headers). Por ejemplo, si el primer byte de la sección tiene una dirección de 0x10, el tercer byte tiene una dirección de 0X12. <br/> |
| 4 <br/> | 4 <br/> | SymbolTableIndex <br/> | Índice de base cero de la tabla de símbolos. Este símbolo proporciona la dirección que se va a utilizar para la reubicación. Si el símbolo especificado tiene la clase de almacenamiento de sección, la dirección del símbolo es la dirección con la primera sección del mismo nombre. <br/>                                                                                                 |
| 8 <br/> | 2 <br/> | Tipo <br/>             | Valor que indica el tipo de reubicación que debe realizarse. Los tipos de reubicación válidos dependen del tipo de máquina. Vea [indicadores de tipo](#type-indicators). <br/>                                                                                                                                                                                     |



 

Si el símbolo al que hace referencia el campo SymbolTableIndex tiene la sección de \_ clase Storage Image SYM \_ Class \_ , la dirección del símbolo es el principio de la sección. La sección está normalmente en el mismo archivo, excepto cuando el archivo objeto forma parte de un archivo (biblioteca). En ese caso, la sección se puede encontrar en cualquier otro archivo objeto del archivo que tenga el mismo nombre de miembro de archivado que el archivo objeto actual. (La relación con el nombre de miembro de archivo se usa en la vinculación de las tablas de importación, es decir, la sección. idata).

#### <a name="type-indicators"></a>Indicadores de tipo

El campo tipo del registro de reubicación indica el tipo de reubicación que debe realizarse. Se definen diferentes tipos de reubicación para cada tipo de equipo.

##### <a name="x64-processors"></a>Procesadores x64

Los siguientes indicadores de tipo de reubicación se definen para procesadores x64 y compatibles.



| Constante                                | Value              | Descripción                                                                                                                                                   |
|-----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ AMD64 \_ Absolute <br/> | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                        |
| IMAGE \_ REL \_ AMD64 \_ ADDR64 <br/>   | 0x0001 <br/> | El de 64 bit VA del destino de reubicación. <br/>                                                                                                           |
| IMAGE \_ REL \_ AMD64 \_ ADDR32 <br/>   | 0x0002 <br/> | El de 32 bit VA del destino de reubicación. <br/>                                                                                                           |
| IMAGE \_ REL \_ AMD64 \_ ADDR32NB <br/> | 0x0003 <br/> | La dirección de 32 bits sin una base de imagen (RVA). <br/>                                                                                                   |
| IMAGE \_ REL \_ AMD64 \_ REL32 <br/>    | 0x0004 <br/> | Dirección relativa de 32 bits del byte después de la reubicación. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 1 <br/> | 0x0005 <br/> | Dirección de 32 bits relativa a la distancia de bytes 1 de la reubicación. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 2 <br/> | 0x0006 <br/> | Dirección de 32 bits relativa a la distancia 2 en bytes de la reubicación. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 3 <br/> | 0x0007 <br/> | Dirección de 32 bits relativa a la distancia de bytes 3 de la reubicación. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 4 <br/> | 0x0008 <br/> | Dirección de 32 bits relativa a la distancia de bytes 4 de la reubicación. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 5 <br/> | 0x0009 <br/> | Dirección de 32 bits relativa a la distancia 5 de bytes desde la reubicación. <br/>                                                                               |
| IMAGEN \_ REL en la \_ \_ sección AMD64 <br/>  | 0x000A <br/> | Índice de la sección de 16 bits de la sección que contiene el destino. Se utiliza para admitir la información de depuración. <br/>                                  |
| IMAGE \_ REL \_ AMD64 \_ SECREL <br/>   | 0x000B <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/> |
| IMAGE \_ REL \_ AMD64 \_ SECREL7 <br/>  | 0x000C <br/> | Desplazamiento de 7 bits sin signo de la base de la sección que contiene el destino. <br/>                                                                    |
| TOKEN de la imagen \_ REL \_ AMD64 \_ <br/>    | 0x000D <br/> | Tokens CLR. <br/>                                                                                                                                       |
| IMAGE \_ REL \_ AMD64 \_ SREL32 <br/>   | 0x000E <br/> | Un valor dependiente del intervalo con signo de 32 bits emitido en el objeto. <br/>                                                                                     |
| Par de imagen \_ REL \_ AMD64 \_ <br/>     | 0x000F <br/> | Par que debe seguir inmediatamente a cada valor dependiente del intervalo. <br/>                                                                                   |
| IMAGE \_ REL \_ AMD64 \_ SSPAN32 <br/>  | 0x0010 <br/> | Valor dependiente de 32 bits con signo que se aplica en el momento de la vinculación. <br/>                                                                                |



 

##### <a name="arm-processors"></a>Procesadores ARM

Los siguientes indicadores de tipo de reubicación se definen para los procesadores ARM.



| Constante                                | Value              | Descripción                                                                                                                                                                                                                                                            |
|-----------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ ARM \_ Absolute <br/>   | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ ARM \_ ADDR32 <br/>     | 0x0001 <br/> | El de 32 bit VA del destino. <br/>                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ ARM \_ ADDR32NB <br/>   | 0x0002 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ ARM \_ BRANCH24 <br/>   | 0x0003 <br/> | Desplazamiento relativo de 24 bits al destino. <br/>                                                                                                                                                                                                            |
| IMAGE \_ REL \_ ARM \_ BRANCH11 <br/>   | 0x0004 <br/> | Referencia a una llamada de subrutina. La referencia consta de instrucciones de 2 16 bits con desplazamientos de 11 bits. <br/>                                                                                                                                                 |
| IMAGE \_ REL \_ ARM \_ REL32 <br/>      | 0x000A <br/> | Dirección relativa de 32 bits del byte después de la reubicación. <br/>                                                                                                                                                                                        |
| sección de la imagen \_ REL \_ ARM \_ <br/>    | 0x000E <br/> | Índice de la sección de 16 bits de la sección que contiene el destino. Se utiliza para admitir la información de depuración. <br/>                                                                                                                                           |
| IMAGE \_ REL \_ ARM \_ SECREL <br/>     | 0x000F <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                                                                          |
| IMAGE \_ REL \_ ARM \_ MOV32 <br/>      | 0x0010 <br/> | El de 32 bit VA del destino. Esta reubicación se aplica mediante una instrucción MOVW para los 16 bits inferiores seguidos de un MOVT para los 16 bits superiores. <br/>                                                                                                              |
| IMAGE \_ REL \_ Thumb \_ MOV32 <br/>    | 0x0011 <br/> | El de 32 bit VA del destino. Esta reubicación se aplica mediante una instrucción MOVW para los 16 bits inferiores seguidos de un MOVT para los 16 bits superiores. <br/>                                                                                                              |
| IMAGE \_ REL \_ Thumb \_ BRANCH20 <br/> | 0x0012 <br/> | La instrucción se corrige con el desplazamiento relativo de 21 bits al destino alineado de 2 bytes. El bit menos significativo del desplazamiento es siempre cero y no se almacena. Esta reubicación corresponde a una instrucción B condicional B de Thumb-2 32 bits. <br/> |
| No utilizado <br/>                      | 0x0013 <br/> |                                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ Thumb \_ BRANCH24 <br/> | 0x0014 <br/> | La instrucción se corrige con el desplazamiento relativo de 25 bits al destino alineado de 2 bytes. El bit menos significativo del desplazamiento es cero y no se almacena. Esta reubicación corresponde a una instrucción Thumb-2 B. <br/>                            |
| IMAGE \_ REL \_ Thumb \_ BLX23 <br/>    | 0x0015 <br/> | La instrucción se corrige con el desplazamiento relativo de 25 bits al destino alineado de 4 bytes. Los 2 bits inferiores del desplazamiento son cero y no se almacenan. <br/> Esta reubicación corresponde a una instrucción Thumb-2 BLX. <br/>                      |
| par de ARM de imagen \_ REL \_ \_ <br/>       | 0x0016 <br/> | La reubicación solo es válida cuando sigue inmediatamente a un \_ REFHI de ARM o Thumb \_ REFHI. Su SymbolTableIndex contiene un desplazamiento y no un índice en la tabla de símbolos. <br/>                                                                                |



 

##### <a name="arm64-processors"></a>Procesadores de ARM64

Los siguientes indicadores de tipo de reubicación se definen para los procesadores de ARM64.



| Constante                                       | Value              | Descripción                                                                                                                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ ARM64 \_ Absolute <br/>        | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                        |
| IMAGE \_ REL \_ ARM64 \_ ADDR32 <br/>          | 0x0001 <br/> | El de 32 bit VA del destino. <br/>                                                                                                                      |
| IMAGE \_ REL \_ ARM64 \_ ADDR32NB <br/>        | 0x0002 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                     |
| IMAGE \_ REL \_ ARM64 \_ BRANCH26 <br/>        | 0x0003 <br/> | Desplazamiento relativo de 26 bits al destino, para las instrucciones B y BL. <br/>                                                                        |
| IMAGE \_ REL \_ ARM64 \_ PAGEBASE \_ REL21 <br/> | 0x0004 <br/> | La base de página del destino, para la instrucción ADRP. <br/>                                                                                                |
| IMAGE \_ REL \_ ARM64 \_ REL21 <br/>           | 0x0005 <br/> | Desplazamiento relativo de 12 bits al destino, para la instrucción ADR <br/>                                                                               |
| IMAGE \_ REL \_ ARM64 \_ PAGEOFFSET \_ 12A <br/> | 0x0006 <br/> | El desplazamiento de página de 12 bits del destino, para instrucciones ADD/ADDS (inmediato) con cero Shift. <br/>                                                      |
| IMAGE \_ REL \_ ARM64 \_ PAGEOFFSET \_ 12L <br/> | 0x0007 <br/> | Desplazamiento de página de 12 bits del destino, para la instrucción LDR (indexado, sin signo inmediato). <br/>                                                          |
| IMAGE \_ REL \_ ARM64 \_ SECREL <br/>          | 0x0008 <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/> |
| IMAGE \_ REL \_ ARM64 \_ SECREL \_ LOW12A <br/>  | 0x0009 <br/> | Bit 0:11 de desplazamiento de la sección del destino, para instrucciones ADD/ADDS (inmediato) con cero Shift. <br/>                                                  |
| IMAGE \_ REL \_ ARM64 \_ SECREL \_ HIGH12A <br/> | 0x000A <br/> | Bit 12:23 de desplazamiento de la sección del destino, para instrucciones ADD/ADDS (inmediato) con cero Shift. <br/>                                                 |
| IMAGE \_ REL \_ ARM64 \_ SECREL \_ LOW12L <br/>  | 0x000B <br/> | Bit 0:11 de desplazamiento de la sección del destino, para la instrucción LDR (indexado, sin signo inmediato). <br/>                                                      |
| IMAGE \_ REL \_ ARM64 \_ token <br/>           | 0x000C <br/> | Token CLR. <br/>                                                                                                                                        |
| IMAGEN de la \_ \_ sección ARM64 REL \_ <br/>         | 0x000D <br/> | Índice de la sección de 16 bits de la sección que contiene el destino. Se utiliza para admitir la información de depuración. <br/>                                  |
| IMAGE \_ REL \_ ARM64 \_ ADDR64 <br/>          | 0x000E <br/> | El de 64 bit VA del destino de reubicación. <br/>                                                                                                           |
| IMAGE \_ REL \_ ARM64 \_ BRANCH19 <br/>        | 0x000F <br/> | Desplazamiento de 19 bits al destino de reubicación, para la instrucción B condicional. <br/>                                                                        |
| IMAGE \_ REL \_ ARM64 \_ BRANCH14 <br/>        | 0x0010 <br/> | Desplazamiento de 14 bits al destino de reubicación, para las instrucciones TBZ y TBNZ. <br/>                                                                        |
| IMAGE \_ REL \_ ARM64 \_ REL32 <br/>           | 0x0011 <br/> | Dirección relativa de 32 bits del byte después de la reubicación. <br/>                                                                               |

##### <a name="hitachi-superh-processors"></a>Procesadores Hitachi SuperH

Los siguientes indicadores de tipo de reubicación se definen para los procesadores SH3 y SH4. Las reubicaciones específicas de SH5 se indican como SHM (SH media).



| Constante                                      | Value              | Descripción                                                                                                                                                                                                                |
|-----------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ SH3 \_ Absolute <br/>         | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                     |
| IMAGE \_ REL \_ SH3 \_ DIRECT16 <br/>         | 0x0001 <br/> | Referencia a la ubicación de 16 bits que contiene el VA del símbolo de destino. <br/>                                                                                                                                  |
| IMAGE \_ REL \_ SH3 \_ DIRECT32 <br/>         | 0x0002 <br/> | El de 32 bit VA del símbolo de destino. <br/>                                                                                                                                                                            |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 <br/>          | 0x0003 <br/> | Referencia a la ubicación de 8 bits que contiene el VA del símbolo de destino. <br/>                                                                                                                                   |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 \_ Word <br/>    | 0x0004 <br/> | Referencia a la instrucción de 8 bits que contiene el fin de 16 bits efectivo del símbolo de destino. <br/>                                                                                                               |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 \_ Long <br/>    | 0x0005 <br/> | Referencia a la instrucción de 8 bits que contiene el efecto de 32 bits efectivo del símbolo de destino. <br/>                                                                                                               |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 <br/>          | 0x0006 <br/> | Referencia a la ubicación de 8 bits cuyos 4 bits inferiores contienen el VA del símbolo de destino. <br/>                                                                                                                        |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 \_ Word <br/>    | 0x0007 <br/> | Referencia a la instrucción de 8 bits cuyos 4 bits inferiores contienen el fin de 16 bits efectivo del símbolo de destino. <br/>                                                                                                    |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 \_ Long <br/>    | 0x0008 <br/> | Referencia a la instrucción de 8 bits cuyos 4 bits inferiores contienen el efecto de 32 bits efectivo del símbolo de destino. <br/>                                                                                                    |
| IMAGE \_ REL \_ SH3 \_ PCREL8 \_ Word <br/>     | 0x0009 <br/> | Referencia a la instrucción de 8 bits que contiene el desplazamiento relativo de 16 bits en vigor del símbolo de destino. <br/>                                                                                                  |
| IMAGE \_ REL \_ SH3 \_ PCREL8 \_ Long <br/>     | 0x000A <br/> | Referencia a la instrucción de 8 bits que contiene el desplazamiento relativo de 32 bits en vigor del símbolo de destino. <br/>                                                                                                  |
| IMAGE \_ REL \_ SH3 \_ PCREL12 \_ Word <br/>    | 0x000B <br/> | Referencia a la instrucción de 16 bits cuyos 12 bits inferiores contienen el desplazamiento relativo de 16 bits en vigor del símbolo de destino. <br/>                                                                                     |
| IMAGEN \_ REL \_ SH3 \_ sección de inicio \_ <br/> | 0x000C <br/> | Referencia a una ubicación de 32 bits que es el VA de la sección que contiene el símbolo de destino. <br/>                                                                                                                |
| IMAGEN \_ REL \_ SH3 \_ sección sizeof \_ <br/>  | 0x000D <br/> | Referencia a la ubicación de 32 bits que es el tamaño de la sección que contiene el símbolo de destino. <br/>                                                                                                            |
| IMAGEN de la \_ \_ sección SH3 REL \_ <br/>          | 0x000E <br/> | Índice de la sección de 16 bits de la sección que contiene el destino. Se utiliza para admitir la información de depuración. <br/>                                                                                               |
| IMAGE \_ REL \_ SH3 \_ SECREL <br/>           | 0x000F <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                              |
| IMAGE \_ REL \_ SH3 \_ DIRECT32 \_ NB <br/>     | 0x0010 <br/> | RVA de 32 bits del símbolo de destino. <br/>                                                                                                                                                                           |
| IMAGE \_ REL \_ SH3 \_ GPREL4 \_ Long <br/>     | 0x0011 <br/> | Relativa a GP. <br/>                                                                                                                                                                                                   |
| IMAGE \_ REL \_ SH3 \_ token <br/>            | 0x0012 <br/> | Token CLR. <br/>                                                                                                                                                                                                     |
| IMAGE \_ REL \_ SHM \_ PCRELPT <br/>          | 0x0013 <br/> | El desplazamiento de la instrucción actual en longwords. Si no se establece el bit nomode, inserte el inverso del bit bajo en el bit 32 para seleccionar PTA o PTB. <br/>                                                          |
| IMAGE \_ REL \_ SHM \_ REFLO <br/>            | 0x0014 <br/> | Los 16 bits inferiores de la dirección de 32 bits. <br/>                                                                                                                                                                         |
| IMAGE \_ REL \_ SHM \_ REFHALF <br/>          | 0x0015 <br/> | Los 16 bits superiores de la Dirección 32 bits. <br/>                                                                                                                                                                        |
| IMAGE \_ REL \_ SHM \_ Rello <br/>            | 0x0016 <br/> | Los 16 bits inferiores de la dirección relativa. <br/>                                                                                                                                                                       |
| IMAGE \_ REL \_ SHM \_ RELHALF <br/>          | 0x0017 <br/> | Los 16 bits superiores de la dirección relativa. <br/>                                                                                                                                                                      |
| IMAGE \_ REL \_ SHM \_ pair <br/>             | 0x0018 <br/> | La reubicación solo es válida cuando sigue inmediatamente a una REFHALF, RELHALF o RELLO. El campo SymbolTableIndex de la reubicación contiene un desplazamiento y no un índice en la tabla de símbolos. <br/> |
| IMAGEN \_ REL \_ SHM \_ nomode <br/>           | 0x8000 <br/> | La reubicación omite el modo de sección. <br/>                                                                                                                                                                           |



 

##### <a name="ibm-powerpc-processors"></a>Procesadores IBM PowerPC

Los siguientes indicadores de tipo de reubicación se definen para los procesadores PowerPC.



| Constante                              | Value              | Descripción                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ PPC \_ absoluta <br/> | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ PPC \_ ADDR64 <br/>   | 0x0001 <br/> | El de 64 bit VA del destino. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ PPC \_ ADDR32 <br/>   | 0x0002 <br/> | El de 32 bit VA del destino. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ PPC \_ ADDR24 <br/>   | 0x0003 <br/> | Los 24 bits inferiores del VA del destino. Esto solo es válido cuando el símbolo de destino es absoluto y se puede extender con signo a su valor original. <br/>                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ PPC \_ ADDR16 <br/>   | 0x0004 <br/> | Los 16 bits inferiores del VA del destino. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ PPC \_ ADDR14 <br/>   | 0x0005 <br/> | Los 14 bits inferiores del VA del destino. Esto solo es válido cuando el símbolo de destino es absoluto y se puede extender con signo a su valor original. <br/>                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ PPC \_ REL24 <br/>    | 0x0006 <br/> | Desplazamiento relativo de PC de 24 bits a la ubicación del símbolo. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ REL14 <br/>    | 0x0007 <br/> | Desplazamiento relativo de un PC de 14 bits a la ubicación del símbolo. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ ADDR32NB <br/> | 0x000A <br/> | RVA de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ PPC \_ SECREL <br/>   | 0x000B <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                                                                                                                                                                                       |
| sección de la imagen \_ REL de \_ PPC \_ <br/>  | 0x000C <br/> | Índice de la sección de 16 bits de la sección que contiene el destino. Se utiliza para admitir la información de depuración. <br/>                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ PPC \_ SECREL16 <br/> | 0x000F <br/> | Desplazamiento de 16 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                                                                                                                                                                                       |
| IMAGE \_ REL \_ PPC \_ REFHI <br/>    | 0x0010 <br/> | Los 16 bits superiores del tiempo de 32 de destino VA. Se usa para la primera instrucción en una secuencia de dos instrucciones que carga una dirección completa. Esta reubicación debe ir seguida inmediatamente de una reubicación de pares cuyo SymbolTableIndex contiene un desplazamiento con signo de 16 bits que se agrega a los 16 bits superiores que se tomó de la ubicación que se va a reubicar. <br/> |
| IMAGE \_ REL \_ PPC \_ REFLO <br/>    | 0x0011 <br/> | Los 16 bits inferiores del VA del destino. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMAGEN \_ REL en el \_ \_ par PPC <br/>     | 0x0012 <br/> | Una reubicación que es válida solo cuando sigue inmediatamente a una reubicación REFHI o SECRELHI. Su SymbolTableIndex contiene un desplazamiento y no un índice en la tabla de símbolos. <br/>                                                                                                                                                                                        |
| IMAGE \_ REL \_ PPC \_ SECRELLO <br/> | 0x0013 <br/> | Los 16 bits inferiores del desplazamiento de 32 bits del destino desde el principio de su sección. <br/>                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ GPREL <br/>    | 0x0015 <br/> | Desplazamiento con signo de 16 bits del destino en relación con el registro de GP. <br/>                                                                                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ PPC \_ (token) <br/>    | 0x0016 <br/> | El token CLR. <br/>                                                                                                                                                                                                                                                                                                                                                          |



 

##### <a name="intel-386-processors"></a>Procesadores Intel 386

Los siguientes indicadores de tipo de reubicación se definen para procesadores Intel 386 y compatibles.



| Constante                               | Value              | Descripción                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ i386 \_ Absolute <br/> | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                        |
| IMAGE \_ REL \_ i386 \_ DIR16 <br/>    | 0x0001 <br/> | No se admite. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ i386 \_ REL16 <br/>    | 0x0002 <br/> | No se admite. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ i386 \_ DIR32 <br/>    | 0x0006 <br/> | El destino es de 32 bits. <br/>                                                                                                                           |
| IMAGE \_ REL \_ i386 \_ DIR32NB <br/>  | 0x0007 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                          |
| IMAGE \_ REL \_ i386 \_ SEG12 <br/>    | 0x0009 <br/> | No se admite. <br/>                                                                                                                                    |
| Sección de la imagen \_ REL \_ i386 \_ <br/>  | 0x000A <br/> | Índice de la sección de 16 bits de la sección que contiene el destino. Se utiliza para admitir la información de depuración. <br/>                                  |
| IMAGE \_ REL \_ i386 \_ SECREL <br/>   | 0x000B <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/> |
| IMAGEN \_ REL \_ token de i386 \_ <br/>    | 0x000C <br/> | El token CLR. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ i386 \_ SECREL7 <br/>  | 0x000D <br/> | Desplazamiento de 7 bits desde la base de la sección que contiene el destino. <br/>                                                                             |
| IMAGE \_ REL \_ i386 \_ REL32 <br/>    | 0x0014 <br/> | Desplazamiento relativo de 32 bits al destino. Esto admite la rama relativa x86 y las instrucciones de llamada. <br/>                                      |



 

##### <a name="intel-itanium-processor-family-ipf"></a>Familia de procesadores Intel Itanium (IPF)

Los siguientes indicadores de tipo de reubicación se definen para la familia de procesadores Intel Itanium y los procesadores compatibles. Tenga en cuenta que las reubicaciones en las instrucciones usan el desplazamiento y el número de ranura del paquete para el desplazamiento de reubicación.



| Constante                                 | Value              | Descripción                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ ia64 \_ Absolute <br/>   | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ ia64 \_ IMM14 <br/>      | 0x0001 <br/> | La reubicación de instrucciones puede ir seguida de una reubicación ADDEND cuyo valor se agrega a la dirección de destino antes de que se inserte en la ranura especificada en el paquete IMM14. El destino de la reubicación debe ser absoluto o debe corregirse la imagen. <br/>                                                                                 |
| IMAGE \_ REL \_ ia64 \_ IMM22 <br/>      | 0x0002 <br/> | La reubicación de instrucciones puede ir seguida de una reubicación ADDEND cuyo valor se agrega a la dirección de destino antes de que se inserte en la ranura especificada en el paquete IMM22. El destino de la reubicación debe ser absoluto o debe corregirse la imagen. <br/>                                                                                 |
| IMAGE \_ REL \_ ia64 \_ IMM64 <br/>      | 0x0003 <br/> | El número de ranura de esta reubicación debe ser uno (1). La reubicación puede ir seguida de una reubicación ADDEND cuyo valor se agrega a la dirección de destino antes de que se almacene en las tres ranuras del paquete IMM64. <br/>                                                                                                                   |
| IMAGE \_ REL \_ ia64 \_ DIR32 <br/>      | 0x0004 <br/> | El destino es de 32 bits. Solo se admite para/LARGEADDRESSAWARE: sin imágenes. <br/>                                                                                                                                                                                                                                                    |
| IMAGE \_ REL \_ ia64 \_ DIR64 <br/>      | 0x0005 <br/> | El destino es de 64 bits. <br/>                                                                                                                                                                                                                                                                                                             |
| IMAGE \_ REL \_ ia64 \_ PCREL21B <br/>   | 0x0006 <br/> | La instrucción se corrige con el desplazamiento relativo de 25 bits al destino alineado de 16 bits. Los 4 bits inferiores del desplazamiento son cero y no se almacenan. <br/>                                                                                                                                                                     |
| IMAGE \_ REL \_ ia64 \_ PCREL21M <br/>   | 0x0007 <br/> | La instrucción se corrige con el desplazamiento relativo de 25 bits al destino alineado de 16 bits. Los 4 bits inferiores del desplazamiento, que son cero, no se almacenan. <br/>                                                                                                                                                                 |
| IMAGE \_ REL \_ ia64 \_ PCREL21F <br/>   | 0x0008 <br/> | La LSBs del desplazamiento de esta reubicación debe contener el número de ranura, mientras que el resto es la dirección del paquete. La agrupación se fija con el desplazamiento relativo de 25 bits al destino alineado de 16 bits. Los 4 bits inferiores del desplazamiento son cero y no se almacenan. <br/>                                                                |
| IMAGE \_ REL \_ ia64 \_ GPREL22 <br/>    | 0x0009 <br/> | La reubicación de instrucciones puede ir seguida de una reubicación ADDEND cuyo valor se agrega a la dirección de destino y, a continuación, un desplazamiento relativo a GP de 22 bits que se calcula y se aplica al grupo GPREL22. <br/>                                                                                                                            |
| IMAGE \_ REL \_ ia64 \_ LTOFF22 <br/>    | 0x000A <br/> | La instrucción se corrige con el desplazamiento relativo de la Directiva de directivas de 22 bits a la entrada de la tabla literal del símbolo de destino. El vinculador crea esta entrada de tabla literal en función de esta reubicación y de la reubicación de ADDEND que puede seguir. <br/>                                                                                                        |
| IMAGEN de la \_ \_ sección REL ia64 \_ <br/>    | 0x000B <br/> | El índice de sección de 16 bits de la sección contiene el destino. Se utiliza para admitir la información de depuración. <br/>                                                                                                                                                                                                                         |
| IMAGE \_ REL \_ ia64 \_ SECREL22 <br/>   | 0x000C <br/> | La instrucción se corrige con el desplazamiento de 22 bits del destino desde el principio de su sección. Esta reubicación puede ir seguida inmediatamente de una reubicación ADDEND, cuyo campo de valor contiene el desplazamiento sin signo de 32 bits del destino desde el principio de la sección. <br/>                                                     |
| IMAGE \_ REL \_ ia64 \_ SECREL64I <br/>  | 0x000D <br/> | El número de ranura para esta reubicación debe ser uno (1). La instrucción se corrige con el desplazamiento de 64 bits del destino desde el principio de su sección. Esta reubicación puede ir seguida inmediatamente de una reubicación ADDEND cuyo campo de valor contiene el desplazamiento sin signo de 32 bits del destino desde el principio de la sección. <br/> |
| IMAGE \_ REL \_ ia64 \_ SECREL32 <br/>   | 0x000E <br/> | Dirección de los datos que se van a corregir con el desplazamiento de 32 bits del destino desde el principio de su sección. <br/>                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ ia64 \_ DIR32NB <br/>    | 0x0010 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ ia64 \_ SREL14 <br/>     | 0x0011 <br/> | Esto se aplica a una inmediata de 14 bits con signo que contiene la diferencia entre dos destinos reubicables. Este es un campo declarativo para el vinculador que indica que el compilador ya ha emitido este valor. <br/>                                                                                                              |
| IMAGE \_ REL \_ ia64 \_ SREL22 <br/>     | 0x0012 <br/> | Esto se aplica a una inmediata de 22 bits con signo que contiene la diferencia entre dos destinos reubicables. Este es un campo declarativo para el vinculador que indica que el compilador ya ha emitido este valor. <br/>                                                                                                              |
| IMAGE \_ REL \_ ia64 \_ SREL32 <br/>     | 0x0013 <br/> | Esto se aplica a una inmediata de 32 bits con signo que contiene la diferencia entre dos valores reubicables. Este es un campo declarativo para el vinculador que indica que el compilador ya ha emitido este valor. <br/>                                                                                                               |
| IMAGE \_ REL \_ ia64 \_ UREL32 <br/>     | 0x0014 <br/> | Esto se aplica a una expresión inmediata de 32 bits sin signo que contiene la diferencia entre dos valores reubicables. Este es un campo declarativo para el vinculador que indica que el compilador ya ha emitido este valor. <br/>                                                                                                            |
| IMAGE \_ REL \_ ia64 \_ PCREL60X <br/>   | 0x0015 <br/> | Una corrección relativa de PC de 60 bits que siempre permanece como una instrucción BRL de un paquete MLX. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ ia64 \_ PCREL60B <br/>   | 0x0016 <br/> | Una corrección relativa de PC de 60 bits. Si el desplazamiento de destino se encuentra en un campo de 25 bits con signo, convierta el paquete completo en un grupo de MBB con NOP. B en la ranura 1 y una instrucción BR de 25 bits (con los 4 bits más bajos todos cero y colocado) en la ranura 2. <br/>                                                                                          |
| IMAGE \_ REL \_ ia64 \_ PCREL60F <br/>   | 0x0017 <br/> | Una corrección relativa de PC de 60 bits. Si el desplazamiento de destino se encuentra en un campo de 25 bits con signo, convierta el paquete completo en un grupo de MFB con NOP. F en la ranura 1 y una instrucción BR de 25 bits (4 bits más a la baja) en la ranura 2. <br/>                                                                                                   |
| IMAGE \_ REL \_ ia64 \_ PCREL60I <br/>   | 0x0018 <br/> | Una corrección relativa de PC de 60 bits. Si el desplazamiento de destino se encuentra en un campo de 25 bits con signo, convierta el paquete completo en un paquete MIB con NOP. I en la ranura 1 y una instrucción BR de 25 bits (4 bits más a la baja) en la ranura 2. <br/>                                                                                                   |
| IMAGE \_ REL \_ ia64 \_ PCREL60M <br/>   | 0x0019 <br/> | Una corrección relativa de PC de 60 bits. Si el desplazamiento de destino se encuentra en un campo de 25 bits con signo, convierta el paquete completo en un paquete de MMB con NOP. M en la ranura 1 y una instrucción BR de 25 bits (4 bits más a la baja) en la ranura 2. <br/>                                                                                                   |
| IMAGE \_ REL \_ ia64 \_ IMMGPREL64 <br/> | 0x001a <br/> | Una corrección relativa a GP de 64 bits. <br/>                                                                                                                                                                                                                                                                                                         |
| TOKEN de imagen \_ REL \_ ia64 \_ <br/>      | 0x001b <br/> | Un token CLR. <br/>                                                                                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ ia64 \_ GPREL32 <br/>    | 0x001c <br/> | Una corrección relativa a GP de 32 bits. <br/>                                                                                                                                                                                                                                                                                                         |
| IMAGE \_ REL \_ ia64 \_ ADDEND <br/>     | 0x001F <br/> | La reubicación solo es válida cuando sigue inmediatamente a una de las siguientes reubicaciones: IMM14, IMM22, IMM64, GPREL22, LTOFF22, LTOFF64, SECREL22, SECREL64I o SECREL32. Su valor contiene el addend que se va a aplicar a las instrucciones de una agrupación, no a los datos. <br/>                                                                  |



 

##### <a name="mips-processors"></a>Procesadores MIPS

Los siguientes indicadores de tipo de reubicación se definen para los procesadores MIPS.



| Constante                                | Value              | Descripción                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ MIPS \_ Absolute <br/>  | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ MIPS \_ REFHALF <br/>   | 0x0001 <br/> | Los 16 bits superiores del tiempo de 32 de destino VA. <br/>                                                                                                                                                                                                                                                                                                                             |
| IMAGE \_ REL \_ MIPS \_ REFWORD <br/>   | 0x0002 <br/> | El destino es de 32 bits. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ MIPS \_ JMPADDR <br/>   | 0x0003 <br/> | Los 26 bits inferiores del VA del destino. Esto es compatible con las instrucciones de MIPS J y el. <br/>                                                                                                                                                                                                                                                                                      |
| IMAGE \_ REL \_ MIPS \_ REFHI <br/>     | 0x0004 <br/> | Los 16 bits superiores del tiempo de 32 de destino VA. Se usa para la primera instrucción en una secuencia de dos instrucciones que carga una dirección completa. Esta reubicación debe ir seguida inmediatamente de una reubicación de pares cuyo SymbolTableIndex contiene un desplazamiento con signo de 16 bits que se agrega a los 16 bits superiores que se toman de la ubicación que se va a reubicar. <br/> |
| IMAGE \_ REL \_ MIPS \_ REFLO <br/>     | 0x0005 <br/> | Los 16 bits inferiores del VA del destino. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ MIPS \_ GPREL <br/>     | 0x0006 <br/> | Desplazamiento con signo de 16 bits del destino en relación con el registro de GP. <br/>                                                                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ MIPS \_ literal <br/>   | 0x0007 <br/> | Igual que IMAGE \_ REL \_ MIPS \_ GPREL. <br/>                                                                                                                                                                                                                                                                                                                                    |
| sección de la imagen \_ REL \_ MIPS \_ <br/>   | 0x000A <br/> | El índice de sección de 16 bits de la sección contiene el destino. Se utiliza para admitir la información de depuración. <br/>                                                                                                                                                                                                                                                             |
| IMAGE \_ REL \_ MIPS \_ SECREL <br/>    | 0x000B <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                                                                                                                                                                                       |
| IMAGE \_ REL \_ MIPS \_ SECRELLO <br/>  | 0x000C <br/> | Los 16 bits inferiores del desplazamiento de 32 bits del destino desde el principio de su sección. <br/>                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ MIPS \_ SECRELHI <br/>  | 0x000D <br/> | Los 16 bits superiores del desplazamiento de 32 bits del destino desde el principio de su sección. Una \_ \_ reubicación de pares MIPS de la imagen REL \_ debe seguir inmediatamente a este. El SymbolTableIndex de la reubicación de pares contiene un desplazamiento con signo de 16 bits que se agrega a los 16 bits superiores que se toman de la ubicación que se va a reubicar. <br/>                            |
| IMAGE \_ REL \_ MIPS \_ JMPADDR16 <br/> | 0x0010 <br/> | Los 26 bits inferiores del VA del destino. Esto admite la instrucción MIPS16 el. <br/>                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ MIPS \_ REFWORDNB <br/> | 0x0022 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                                                |
| IMAGE \_ REL \_ MIPS \_ pair <br/>      | 0x0025 <br/> | La reubicación solo es válida cuando sigue inmediatamente a una reubicación REFHI o SECRELHI. Su SymbolTableIndex contiene un desplazamiento y no un índice en la tabla de símbolos. <br/>                                                                                                                                                                                           |



 

##### <a name="mitsubishi-m32r"></a>M32R de Mitsubishi

Los siguientes indicadores de tipo de reubicación se definen para los procesadores de M32R de Mitsubishi.



| Constante                               | Value              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ M32R \_ Absolute <br/> | 0x0000 <br/> | Se omite la reubicación. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ M32R \_ ADDR32 <br/>   | 0x0001 <br/> | El destino es de 32 bits. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ M32R \_ ADDR32NB <br/> | 0x0002 <br/> | RVA de 32 bits del destino. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ M32R \_ ADDR24 <br/>   | 0x0003 <br/> | El destino es de 24 bits. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ M32R \_ GPREL16 <br/>  | 0x0004 <br/> | Desplazamiento de 16 bits del destino del registro de GP. <br/>                                                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ REL \_ M32R \_ PCREL24 <br/>  | 0x0005 <br/> | Desplazamiento de 24 bits del destino del contador de programas (PC), desplazado a la izquierda de 2 bits y con signo extendido <br/>                                                                                                                                                                                                                                                                                                |
| IMAGE \_ REL \_ M32R \_ PCREL16 <br/>  | 0x0006 <br/> | Desplazamiento de 16 bits del destino del equipo, desplazado a la izquierda en 2 bits y con signo extendido <br/>                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ REL \_ M32R \_ PCREL8 <br/>   | 0x0007 <br/> | Desplazamiento de 8 bits del destino del equipo, desplazado a la izquierda en 2 bits y con signo extendido <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ M32R \_ REFHALF <br/>  | 0x0008 <br/> | Los 16 MSBs del VA de destino. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ M32R \_ REFHI <br/>    | 0x0009 <br/> | 16 MSBs del destino VA, ajustado para la extensión de LSB Sign. Se usa para la primera instrucción en una secuencia de dos instrucciones que carga una dirección completa de 32 bits. Esta reubicación debe ir seguida inmediatamente de una reubicación de pares cuyo SymbolTableIndex contiene un desplazamiento con signo de 16 bits que se agrega a los 16 bits superiores que se toman de la ubicación que se va a reubicar. <br/> |
| IMAGE \_ REL \_ M32R \_ REFLO <br/>    | 0x000A <br/> | Los 16 LSBs del VA de destino. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ M32R \_ pair <br/>     | 0x000B <br/> | La reubicación debe seguir la reubicación REFHI. Su SymbolTableIndex contiene un desplazamiento y no un índice en la tabla de símbolos. <br/>                                                                                                                                                                                                                                                             |
| IMAGEN de la \_ \_ sección M32R REL \_ <br/>  | 0x000C <br/> | Índice de la sección de 16 bits de la sección que contiene el destino. Se utiliza para admitir la información de depuración. <br/>                                                                                                                                                                                                                                                                                  |
| IMAGE \_ REL \_ M32R \_ SECREL <br/>   | 0x000D <br/> | Desplazamiento de 32 bits del destino desde el principio de su sección. Se usa para admitir la información de depuración y el almacenamiento local de subprocesos estáticos. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ M32R \_ token <br/>    | 0x000E <br/> | El token CLR. <br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="coff-line-numbers-deprecated"></a>Números de línea COFF (desusado)

Los números de línea COFF ya no se generan y, en el futuro, no se consumirán.

Los números de línea COFF indican la relación entre el código y los números de línea en los archivos de código fuente. El formato de Microsoft para los números de línea COFF es similar al estándar COFF, pero se ha ampliado para permitir que una sola sección se relacione con los números de línea en varios archivos de código fuente.

Los números de línea COFF se componen de una matriz de registros de longitud fija. La ubicación (desplazamiento de archivo) y el tamaño de la matriz se especifican en el encabezado de la sección. Cada registro de número de línea tiene el formato siguiente.



| Offset        | Tamaño          | Campo                  | Descripción                                                                                                                                                 |
|---------------|---------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Tipo ( \* ) <br/>  | Se trata de una Unión de dos campos: SymbolTableIndex y VirtualAddress. El uso de SymbolTableIndex o RVA depende del valor de LineNumber. <br/> |
| 4 <br/> | 2 <br/> | LineNumber <br/> | Si es distinto de cero, este campo especifica un número de línea basado en uno. Cuando el valor es cero, el campo de tipo se interpreta como un índice de tabla de símbolos para una función. <br/>    |



 

El campo de tipo es una Unión de campos de 2 4 bytes: SymbolTableIndex y VirtualAddress.



| Offset        | Tamaño          | Campo                        | Descripción                                                                                                                                                                             |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | SymbolTableIndex <br/> | Se usa cuando LineNumber es cero: índice de entrada de tabla de símbolos para una función. Este formato se usa para indicar la función a la que hace referencia un grupo de registros de números de línea. <br/>      |
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Se usa cuando LineNumber es distinto de cero: la RVA del código ejecutable que corresponde a la línea de código fuente indicada. En un archivo objeto, contiene el de la sección. <br/> |



 

Un registro de número de línea puede establecer el campo LineNumber en cero y apuntar a una definición de función en la tabla de símbolos, o bien puede funcionar como una entrada de número de línea estándar, proporcionando un entero positivo (número de línea) y la dirección correspondiente en el código de objeto.

Un grupo de entradas de número de línea siempre comienza con el primer formato: el índice de un símbolo de función. Si se trata del primer registro de número de línea de la sección, es también el nombre de símbolo de COMDAT de la función si se establece la marca COMDAT de la sección. Vea [secciones COMDAT (solo objeto)](#comdat-sections-object-only). El registro auxiliar de la función de la tabla de símbolos tiene un puntero al campo LineNumber que señala a este mismo registro de número de línea.

Un registro que identifica una función va seguido de cualquier número de entradas de número de línea que proporcionen información de número de línea real (es decir, entradas con el valor de LineNumber mayor que cero). Estas entradas están basadas en uno, con respecto al principio de la función, y representan cada línea de código fuente de la función excepto la primera línea.

Por ejemplo, el primer registro de número de línea para el ejemplo siguiente especificaría la función ReverseSign (SymbolTableIndex de ReverseSign y LineNumber establecida en cero). A continuación, se seguirán los registros con los valores de LineNumber 1, 2 y 3, correspondientes a las líneas de código fuente, como se muestra a continuación:


```C++
// some code precedes ReverseSign function
int ReverseSign(int i)
1: {
2:  return -1 * i;
3: }
```



### <a name="coff-symbol-table"></a>Tabla de símbolos COFF

La tabla de símbolos de esta sección se hereda del formato COFF tradicional. Es distinto de Microsoft Visual C++ información de depuración. Un archivo puede contener una tabla de símbolos COFF y Visual C++ información de depuración, y los dos se mantienen separados. Algunas herramientas de Microsoft usan la tabla de símbolos para fines limitados pero importantes, como comunicar información de COMDAT al vinculador. Los nombres de sección y de archivo, así como los símbolos de datos y de código, se enumeran en la tabla de símbolos.

La ubicación de la tabla de símbolos se indica en el encabezado COFF.

La tabla de símbolos es una matriz de registros, cada 18 bytes de longitud. Cada registro es un registro de tabla de símbolos estándar o auxiliar. Un registro estándar define un símbolo o un nombre y tiene el formato siguiente.



| Offset         | Tamaño          | Campo                          | Descripción                                                                                                                                                                                                                                 |
|----------------|---------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Nombre ( \* ) <br/>          | Nombre del símbolo, representado por una Unión de tres estructuras. Se utiliza una matriz de 8 bytes si el nombre no tiene más de 8 bytes de longitud. Para obtener más información, vea [representación del nombre de símbolo](https://www.bing.com/search?q=Symbol+Name+Representation). <br/> |
| 8 <br/>  | 4 <br/> | Value <br/>              | Valor asociado al símbolo. La interpretación de este campo depende de SectionNumber y StorageClass. Un significado típico es la dirección reubicable. <br/>                                                         |
| 12 <br/> | 2 <br/> | SectionNumber <br/>      | Entero con signo que identifica la sección, utilizando un índice basado en uno en la tabla de la sección. Algunos valores tienen un significado especial, tal como se define en la sección 5.4.2, "valores numéricos de sección". <br/>                                         |
| 14 <br/> | 2 <br/> | Tipo <br/>               | Número que representa el tipo. Las herramientas de Microsoft establecen este campo en 0x20 (función) o 0X0 (no en una función). Para obtener más información, consulte [representación de tipos](#type-representation). <br/>                                                |
| 16 <br/> | 1 <br/> | StorageClass <br/>       | Valor enumerado que representa la clase de almacenamiento. Para obtener más información, vea [Storage (clase](#storage-class)). <br/>                                                                                                                   |
| 17 <br/> | 1 <br/> | NumberOfAuxSymbols <br/> | El número de entradas de la tabla de símbolos auxiliares que siguen a este registro. <br/>                                                                                                                                                           |



 

Cero o más registros de tabla de símbolos auxiliares siguen inmediatamente a cada registro de tabla de símbolos estándar. Sin embargo, normalmente no hay más de un registro de símbolo de la tabla auxiliar después de un registro de tabla de símbolos estándar (excepto para los registros de archivos con nombres de archivo largos). Cada registro auxiliar tiene el mismo tamaño que un registro de tabla de símbolos estándar (18 bytes), pero en lugar de definir un símbolo nuevo, el registro auxiliar proporciona información adicional sobre el último símbolo definido. La elección de los distintos formatos que se deben usar depende del campo StorageClass. Los formatos definidos actualmente para los registros de la tabla de símbolos auxiliares se muestran en la sección 5,5, "registros de símbolos auxiliares".

Las herramientas que leen tablas de símbolos de COFF deben omitir los registros de símbolos auxiliares cuya interpretación sea desconocida. Esto permite extender el formato de tabla de símbolos para agregar nuevos registros auxiliares, sin interrumpir las herramientas existentes.

#### <a name="symbol-name-representation"></a>Representación de nombre de símbolo

El campo Nombre_corto de una tabla de símbolos consta de 8 bytes que contienen el propio nombre, si no tiene más de 8 bytes de longitud, o el campo Nombre_corto proporciona un desplazamiento en la tabla de cadenas. Para determinar si se proporciona el nombre en sí o un desplazamiento, pruebe los primeros 4 bytes para que sean iguales a cero.

Por Convención, los nombres se tratan como cadenas con codificación UTF-8 terminada en cero.



| Offset        | Tamaño          | Campo                 | Descripción                                                                                                          |
|---------------|---------------|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 8 <br/> | nombreCorto <br/> | Matriz de 8 bytes. Esta matriz se rellena con valores NULL a la derecha si el nombre tiene menos de 8 bytes de longitud. <br/> |
| 0 <br/> | 4 <br/> | Ceros <br/>    | Un campo que se establece en todos los ceros si el nombre tiene más de 8 bytes. <br/>                                     |
| 4 <br/> | 4 <br/> | Offset <br/>    | Desplazamiento en la tabla de cadenas. <br/>                                                                         |



 

#### <a name="section-number-values"></a>Valores de número de sección

Normalmente, el campo de valor de sección de una entrada de tabla de símbolos es un índice basado en uno en la tabla de la sección. Sin embargo, este campo es un entero con signo y puede tomar valores negativos. Los valores siguientes, menos de uno, tienen significados especiales.



| Constante                          | Value          | Descripción                                                                                                                                                                                                                            |
|-----------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEN \_ SYM \_ sin definir <br/> | 0 <br/>  | Todavía no se ha asignado una sección al registro de símbolos. Un valor de cero indica que se define una referencia a un símbolo externo en otra parte. Un valor distinto de cero es un símbolo común con un tamaño especificado por el valor. <br/> |
| IMAGE \_ SYM \_ Absolute <br/>  | -1 <br/> | El símbolo tiene un valor absoluto (no reubicable) y no es una dirección. <br/>                                                                                                                                                  |
| depuración de IMAGE \_ SYM \_ <br/>     | -2 <br/> | El símbolo proporciona información general sobre el tipo o la depuración, pero no se corresponde con una sección. Las herramientas de Microsoft usan este valor junto con los registros. File (archivo de clase de almacenamiento). <br/>                                            |



 

#### <a name="type-representation"></a>Representación de tipos

El campo de tipo de una entrada de tabla de símbolos contiene 2 bytes, donde cada byte representa la información de tipo. LSB representa el tipo de datos simple (base) y el MSB representa el tipo complejo, si lo hay:



| MSB                                                       | LSB                                                        |
|-----------------------------------------------------------|------------------------------------------------------------|
| Tipo complejo: ninguno, puntero, función, matriz. <br/> | Tipo base: entero, punto flotante, etc. <br/> |



 

Los siguientes valores se definen para el tipo base, aunque las herramientas de Microsoft no suelen usar este campo y establecen el valor de LSB en 0. En su lugar, Visual C++ información de depuración se utiliza para indicar tipos. Sin embargo, los valores COFF posibles se enumeran aquí para la integridad.



| Constante                             | Value          | Descripción                                                                            |
|--------------------------------------|----------------|----------------------------------------------------------------------------------------|
| IMAGE \_ SYM \_ tipo \_ null <br/>   | 0 <br/>  | No hay información de tipo o tipo base desconocido. Herramientas de Microsoft use esta opción <br/> |
| IMAGE \_ SYM \_ tipo \_ void <br/>   | 1 <br/>  | No hay ningún tipo válido; se utiliza con punteros y funciones void <br/>                       |
| IMAGE \_ SYM \_ tipo \_ Char <br/>   | 2 <br/>  | Un carácter (byte con signo) <br/>                                                  |
| \_tipo de \_ imagen \_ corto <br/>  | 3 <br/>  | Entero de 2 bytes con signo <br/>                                                    |
| IMAGE \_ SYM \_ tipo \_ int <br/>    | 4 <br/>  | Un tipo entero natural (normalmente 4 bytes en Windows) <br/>                       |
| tipo de imagen \_ SYM \_ \_ largo <br/>   | 5 <br/>  | Entero de 4 bytes con signo <br/>                                                    |
| IMAGE \_ SYM \_ tipo \_ float <br/>  | 6 <br/>  | Un número de punto flotante de 4 bytes <br/>                                             |
| tipo de imagen \_ \_ tipo \_ Double <br/> | 7 <br/>  | Un número de punto flotante de 8 bytes <br/>                                            |
| IMAGE \_ SYM \_ Type ( \_ struct) <br/> | 8 <br/>  | Estructura <br/>                                                                |
| tipo de imagen ( \_ \_ \_ Unión) <br/>  | 9 <br/>  | Una Unión <br/>                                                                    |
| \_ \_ enumeración de tipo de imagen SYM \_ <br/>   | 10 <br/> | Un tipo enumerado <br/>                                                         |
| IMAGE \_ SYM \_ Type \_ Moe <br/>    | 11 <br/> | Un miembro de la enumeración (un valor específico) <br/>                                 |
| tipo de imagen \_ SYM \_ \_ byte <br/>   | 12 <br/> | Byte; entero de 1 byte sin signo <br/>                                            |
| IMAGE \_ SYM \_ Escriba \_ Word <br/>   | 13 <br/> | Una palabra; entero de 2 bytes sin signo <br/>                                            |
| tipo de imagen de \_ \_ tipo \_ uint <br/>   | 14 <br/> | Entero sin signo de tamaño natural (normalmente, 4 bytes) <br/>                    |
| IMAGE \_ SYM \_ tipo \_ DWORD <br/>  | 15 <br/> | Entero de 4 bytes sin signo <br/>                                                 |



 

El byte más significativo especifica si el símbolo es un puntero a, función que devuelve o matriz del tipo base que se especifica en LSB. Las herramientas de Microsoft usan este campo solo para indicar si el símbolo es una función, de modo que los únicos dos valores resultantes son 0X0 y 0x20 para el campo de tipo. Sin embargo, otras herramientas pueden usar este campo para comunicar más información.

Es muy importante especificar el atributo de función correctamente. Esta información es necesaria para que la vinculación incremental funcione correctamente. En algunas arquitecturas, la información puede ser necesaria para otros fines.



| Constante                                | Value         | Descripción                                                          |
|-----------------------------------------|---------------|----------------------------------------------------------------------|
| IMAGE \_ SYM \_ DTYPE \_ null <br/>     | 0 <br/> | Sin tipo derivado; el símbolo es una variable escalar simple. <br/> |
| \_ \_ cursor DTYPE de \_ imagen <br/>  | 1 <br/> | El símbolo es un puntero al tipo base. <br/>                    |
| IMAGE \_ SYM \_ DTYPE \_ función) <br/> | 2 <br/> | El símbolo es una función que devuelve un tipo base. <br/>       |
| IMAGE \_ SYM \_ DTYPE \_ matriz <br/>    | 3 <br/> | El símbolo es una matriz de tipo base. <br/>                     |



 

#### <a name="storage-class"></a>Clase de almacenamiento

El campo StorageClass de la tabla Symbol indica qué tipo de definición representa un símbolo. En la tabla siguiente se muestran los valores posibles. Tenga en cuenta que el campo StorageClass es un entero de 1 byte sin signo. Por lo tanto, el valor especial 1 debe tomarse para indicar su equivalente sin signo, 0xFF.

Aunque el formato COFF tradicional utiliza muchos valores de clase de almacenamiento, las herramientas de Microsoft se basan en Visual C++ formato de depuración para la mayoría de la información simbólica y suelen usar solo cuatro valores de clase de almacenamiento: externo (2), estático (3), función (101) y archivo (103). Excepto en el encabezado de la segunda columna siguiente, "Value" se debe tomar para indicar el campo de valor del registro de símbolos (cuya interpretación depende del número encontrado como clase de almacenamiento).



| Constante                                          | Value                 | Descripción/interpretación del campo de valor                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ End \_ of function de la clase Image SYM \_ <br/>  | -1 (0xFF) <br/> | Símbolo especial que representa el final de la función, con fines de depuración. <br/>                                                                                                                                                                                                                                                  |
| IMAGE \_ SYM ( \_ clase) \_ null <br/>               | 0 <br/>         | No hay ninguna clase de almacenamiento asignada. <br/>                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ SYM ( \_ clase \_ automática) <br/>          | 1 <br/>         | La variable automática (stack). El campo valor especifica el desplazamiento del marco de pila. <br/>                                                                                                                                                                                                                                              |
| IMAGE \_ SYM ( \_ clase \_ externa) <br/>           | 2 <br/>         | Valor que las herramientas de Microsoft usan para los símbolos externos. El campo valor indica el tamaño si el número de sección es IMAGE \_ SYM \_ undefined (0). Si el número de sección no es cero, el campo de valor especifica el desplazamiento dentro de la sección. <br/>                                                                                 |
| IMAGE \_ SYM ( \_ clase \_ estática) <br/>             | 3 <br/>         | Desplazamiento del símbolo dentro de la sección. Si el campo de valor es cero, el símbolo representa un nombre de sección. <br/>                                                                                                                                                                                                            |
| IMAGE \_ SYM ( \_ clase) \_ <br/>           | 4 <br/>         | Una variable de registro. El campo valor especifica el número de registro. <br/>                                                                                                                                                                                                                                                            |
| IMAGE \_ SYM \_ Class \_ external \_ Def <br/>      | 5 <br/>         | Símbolo que se define externamente. <br/>                                                                                                                                                                                                                                                                                           |
| \_etiqueta de \_ clase Image SYM \_ <br/>              | 6 <br/>         | Etiqueta de código que se define en el módulo. El campo valor especifica el desplazamiento del símbolo dentro de la sección. <br/>                                                                                                                                                                                                         |
| \_ \_ \_ etiqueta sin definir de la clase Image SYM \_ <br/>   | 7 <br/>         | Referencia a una etiqueta de código que no está definida. <br/>                                                                                                                                                                                                                                                                               |
| \_ \_ miembro de clase Image SYM \_ \_ de \_ struct <br/> | 8 <br/>         | Miembro de la estructura. El campo de valor especifica el miembro n. <br/>                                                                                                                                                                                                                                                               |
| \_argumento de \_ clase Image SYM \_ <br/>           | 9 <br/>         | Un argumento formal (parámetro) de una función. El campo de valor especifica el argumento n. <br/>                                                                                                                                                                                                                                      |
| \_ \_ etiqueta struct de clase Image SYM \_ \_ <br/>        | 10 <br/>        | La entrada de nombre de etiqueta de estructura. <br/>                                                                                                                                                                                                                                                                                                  |
| \_ \_ elemento de clase Image SYM \_ \_ de \_ Union <br/>  | 11 <br/>        | Miembro de Unión. El campo de valor especifica el miembro n. <br/>                                                                                                                                                                                                                                                                     |
| \_ \_ etiqueta Union de clase Image SYM \_ \_ <br/>         | 12 <br/>        | Entrada de nombre de etiqueta de Unión. <br/>                                                                                                                                                                                                                                                                                                      |
| \_definición de \_ tipo de clase Image SYM \_ \_ <br/>   | 13 <br/>        | Una entrada typedef. <br/>                                                                                                                                                                                                                                                                                                               |
| \_clase Image \_ SYM \_ sin definir \_ static <br/>  | 14 <br/>        | Declaración de datos estáticos. <br/>                                                                                                                                                                                                                                                                                                     |
| \_ \_ etiqueta enum de clase Image SYM \_ \_ <br/>          | 15 <br/>        | Una entrada de tagName de tipo enumerado. <br/>                                                                                                                                                                                                                                                                                              |
| \_ \_ miembro de clase Image SYM \_ \_ de \_ enum <br/>   | 16 <br/>        | Miembro de una enumeración. El campo de valor especifica el miembro n. <br/>                                                                                                                                                                                                                                                         |
| la \_ clase Image SYM ( \_ \_ parámetro de registro \_ ) <br/>    | 17 <br/>        | Parámetro de registro. <br/>                                                                                                                                                                                                                                                                                                          |
| \_campo de \_ bits de clase Image SYM \_ \_ <br/>         | 18 <br/>        | Referencia de campo de bits. El campo valor especifica el bit n en el campo de bits. <br/>                                                                                                                                                                                                                                                |
| bloque de clases de IMAGE \_ SYM \_ \_ <br/>              | 100 <br/>       | Un registro. BB (inicio de bloque) o. EB (fin de bloque). El campo valor es la dirección reubicable de la ubicación del código. <br/>                                                                                                                                                                                                      |
| \_función de \_ clase Image SYM \_ <br/>           | 101 <br/>       | Valor que las herramientas de Microsoft usan para los registros de símbolos que definen el alcance de una función: Begin function (. BF), End Function (. EF) y Lines in function (. LF). En el caso de los registros. LF, el campo de valor proporciona el número de líneas de código fuente de la función. En el caso de los registros. EF, el campo valor proporciona el tamaño del código de la función. <br/> |
| IMAGE \_ SYM ( \_ clase) \_ final \_ de \_ struct <br/>    | 102 <br/>       | Una entrada de final de estructura. <br/>                                                                                                                                                                                                                                                                                                     |
| \_archivo de \_ clase Image SYM \_ <br/>               | 103 <br/>       | Un valor que las herramientas de Microsoft, así como el formato COFF tradicional, se usa para el registro de símbolos del archivo de origen. El símbolo va seguido de registros auxiliares que denominan el archivo. <br/>                                                                                                                                                       |
| sección de la \_ clase Image SYM \_ \_ <br/>            | 104 <br/>       | Definición de una sección (las herramientas de Microsoft usan la clase de almacenamiento estático en su lugar). <br/>                                                                                                                                                                                                                                                  |
| IMAGE \_ SYM \_ ( \_ clase \_ externa débil) <br/>     | 105 <br/>       | Externo débil. Para obtener más información, consulte el [formato auxiliar 3: externos débiles](#auxiliary-format-3-weak-externals). <br/>                                                                                                                                                                                                           |
| \_ \_ token CLR de clase Image SYM \_ \_ <br/>         | 107 <br/>       | Símbolo de token de CLR. El nombre es una cadena ASCII formada por el valor hexadecimal del token. Para obtener más información, vea [definición de tokens CLR (solo objeto)](#clr-token-definition-object-only). <br/>                                                                                                                        |



 

### <a name="auxiliary-symbol-records"></a>Registros de símbolos auxiliares

Los registros de la tabla de símbolos auxiliares siempre siguen y se aplican a, algunos registros de tabla de símbolos estándar. Un registro auxiliar puede tener cualquier formato que puedan reconocer las herramientas, pero se deben asignar 18 bytes para ellos, de modo que la tabla de símbolos se mantenga como una matriz de tamaño normal. Actualmente, las herramientas de Microsoft reconocen formatos auxiliares para los siguientes tipos de registros: definiciones de función, símbolos de inicio y fin de función (. BF y. EF), externos seguros, nombres de archivo y definiciones de sección.

El diseño COFF tradicional también incluye formatos auxiliares de registro para matrices y estructuras. Las herramientas de Microsoft no las utilizan, sino que colocan esa información simbólica en Visual C++ formato de depuración en las secciones de depuración.

#### <a name="auxiliary-format-1-function-definitions"></a>Formato auxiliar 1: definiciones de función

Un registro de tabla de símbolos marca el principio de la definición de una función si tiene todo lo siguiente: una clase de almacenamiento externa (2), un valor de tipo que indica que es una función (0x20) y un número de sección mayor que cero. Tenga en cuenta que un registro de tabla de símbolos que tiene un número de sección de sin definir (0) no define la función y no tiene un registro auxiliar. Los registros de símbolos de definición de función van seguidos de un registro auxiliar en el formato que se describe a continuación:



| Offset         | Tamaño          | Campo                             | Descripción                                                                                                                                                                                                                   |
|----------------|---------------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | TagIndex <br/>              | Índice de la tabla de símbolos del registro de símbolos correspondiente. BF (begin Function). <br/>                                                                                                                                   |
| 4 <br/>  | 4 <br/> | TotalSize <br/>             | Tamaño del código ejecutable de la propia función. Si la función está en su propia sección, el SizeOfRawData del encabezado de la sección es mayor o igual que este campo, en función de las consideraciones de alineación. <br/> |
| 8 <br/>  | 4 <br/> | PointerToLinenumber <br/>   | El desplazamiento de archivo de la primera entrada COFF de número de línea de la función o cero si no existe ninguna. Para obtener más información, vea [números de línea COFF (en desuso)](#coff-line-numbers-deprecated). <br/>                          |
| 12 <br/> | 4 <br/> | PointerToNextFunction <br/> | Índice de la tabla de símbolos del registro de la función siguiente. Si la función es la última de la tabla de símbolos, este campo se establece en cero. <br/>                                                                           |
| 16 <br/> | 2 <br/> | No utilizado <br/>                |                                                                                                                                                                                                                               |



 

#### <a name="auxiliary-format-2-bf-and-ef-symbols"></a>Formato auxiliar 2: símbolos. BF y. EF

Para cada definición de función de la tabla de símbolos, tres elementos describen el principio, el final y el número de líneas. Cada uno de estos símbolos tiene la función de clase de almacenamiento (101):

Un registro de símbolos denominado. BF (begin Function). El campo de valor no se utiliza.

Un registro de símbolos denominado. LF (líneas en función). El campo valor proporciona el número de líneas de la función.

Un registro de símbolos denominado. EF (fin de función). El campo valor tiene el mismo número que el campo tamaño total en el registro símbolo de la definición de función.

Los registros de símbolos. BF y. EF (pero no los registros. LF) van seguidos de un registro auxiliar con el siguiente formato:



| Offset         | Tamaño          | Campo                                         | Descripción                                                                                                                                                                   |
|----------------|---------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | No utilizado <br/>                            |                                                                                                                                                                               |
| 4 <br/>  | 2 <br/> | LineNumber <br/>                        | El número de línea ordinal real (1, 2, 3, etc.) en el archivo de código fuente, que corresponde al registro. BF o. EF. <br/>                                               |
| 6 <br/>  | 6 <br/> | No utilizado <br/>                            |                                                                                                                                                                               |
| 12 <br/> | 4 <br/> | PointerToNextFunction (solo. BF) <br/> | Índice de la tabla de símbolos del siguiente registro de símbolos. BF. Si la función es la última de la tabla de símbolos, este campo se establece en cero. No se utiliza para los registros. EF. <br/> |
| 16 <br/> | 2 <br/> | No utilizado <br/>                            |                                                                                                                                                                               |



 

#### <a name="auxiliary-format-3-weak-externals"></a>Formato auxiliar 3: externos débiles

Los "externos débiles" son un mecanismo para los archivos objeto que permite flexibilidad en el momento de la vinculación. Un módulo puede contener un símbolo externo sin resolver (sym1), pero también puede incluir un registro auxiliar que indica que si sym1 no está presente en el momento de la vinculación, se usa otro símbolo externo (sym2) para resolver las referencias en su lugar.

Si una definición de sym1 está vinculada, se resuelve normalmente una referencia externa al símbolo. Si una definición de sym1 no está vinculada, todas las referencias a la débil externa para sym1 hacen referencia a sym2 en su lugar. El símbolo externo, sym2, siempre debe estar vinculado; Normalmente, se define en el módulo que contiene la referencia débil a sym1.

Los externos débiles se representan mediante un registro de tabla de símbolos con la clase de almacenamiento externo, el número de sección UNDEF y un valor de cero. El registro de símbolos débilmente externos va seguido de un registro auxiliar con el siguiente formato:



| Offset        | Tamaño           | Campo                       | Descripción                                                                                                                                                                                                                                                                                                                                                |
|---------------|----------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>  | TagIndex <br/>        | El índice de la tabla de símbolos de sym2, el símbolo que se va a vincular si no se encuentra sym1. <br/>                                                                                                                                                                                                                                                                  |
| 4 <br/> | 4 <br/>  | Características <br/> | Un valor de IMAGE \_ Weak \_ extern \_ Search \_ nolibrary indica que no se debe realizar ninguna búsqueda de biblioteca para sym1. <br/> Un valor de la \_ biblioteca de búsqueda externa débil de la imagen \_ \_ \_ indica que debe realizarse una búsqueda de biblioteca de sym1. <br/> Un valor de \_ alias de \_ búsqueda débil extern de imagen \_ \_ indica que sym1 es un alias para sym2. <br/> |
| 8 <br/> | 10 <br/> | No utilizado <br/>          |                                                                                                                                                                                                                                                                                                                                                            |



 

Tenga en cuenta que el campo características no está definido en WINNt. C en su lugar, se usa el campo tamaño total.

#### <a name="auxiliary-format-4-files"></a>Formato auxiliar 4: archivos

Este formato sigue un registro de tabla de símbolos con el archivo de clase de almacenamiento (103). El nombre del símbolo debe ser. File y el registro auxiliar que le sigue proporciona el nombre de un archivo de código fuente.



| Offset        | Tamaño           | Campo                 | Descripción                                                                                                                         |
|---------------|----------------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 18 <br/> | Nombre de archivo <br/> | Cadena ANSI que proporciona el nombre del archivo de código fuente. Esto se rellena con valores NULL si es menor que la longitud máxima. <br/> |



 

#### <a name="auxiliary-format-5-section-definitions"></a>Formato auxiliar 5: definiciones de sección

Este formato sigue un registro de tabla de símbolos que define una sección. Dicho registro tiene un nombre de símbolo que es el nombre de una sección (como. Text o. drectve) y tiene la clase de almacenamiento STATIC (3). El registro auxiliar proporciona información acerca de la sección a la que hace referencia. Por lo tanto, duplica parte de la información en el encabezado de la sección.



| Offset         | Tamaño          | Campo                           | Descripción                                                                                                                                                                                                             |
|----------------|---------------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Length <br/>              | Tamaño de los datos de la sección; lo mismo que SizeOfRawData en el encabezado de la sección. <br/>                                                                                                                                  |
| 4 <br/>  | 2 <br/> | NumberOfRelocations <br/> | El número de entradas de reubicación para la sección. <br/>                                                                                                                                                           |
| 6 <br/>  | 2 <br/> | NumberOfLinenumbers <br/> | Número de entradas de número de línea de la sección. <br/>                                                                                                                                                          |
| 8 <br/>  | 4 <br/> | MD5 <br/>            | La suma de comprobación para los datos de Communal. Es aplicable si la marca IMAGE \_ SCN \_ lnk \_ COMDAT está establecida en el encabezado de la sección. Para obtener más información, consulte [secciones COMDAT (solo objeto)](#comdat-sections-object-only). <br/> |
| 12 <br/> | 2 <br/> | Number <br/>              | Índice basado en uno en la tabla de la sección asociada. Se utiliza cuando la opción de selección de COMDAT es 5. <br/>                                                                                     |
| 14 <br/> | 1 <br/> | Selección <br/>           | Número de selección de COMDAT. Esto es aplicable si la sección es una sección de COMDAT. <br/>                                                                                                                         |
| 15 <br/> | 3 <br/> | No utilizado <br/>              |                                                                                                                                                                                                                         |



 

#### <a name="comdat-sections-object-only"></a>Secciones COMDAT (solo objeto)

El campo de selección del formato auxiliar de definición de sección es aplicable si la sección es una sección de COMDAT. Una sección de COMDAT es una sección que puede ser definida por más de un archivo objeto. (La imagen \_ de marca SCN \_ lnk \_ COMDAT se establece en el campo marcas de sección del encabezado de la sección). El campo de selección determina el modo en que el enlazador resuelve las distintas definiciones de las secciones de COMDAT.

El primer símbolo que tenga el valor de sección de la sección COMDAT debe ser el símbolo de sección. Este símbolo tiene el nombre de la sección, el campo de valor es igual a cero, el número de sección de la sección COMDAT en cuestión, el campo de tipo igual a IMAGE \_ SYM \_ Type \_ null, el campo de clase igual a Image \_ SYM \_ Class \_ static y un registro auxiliar. El segundo símbolo se llama "el símbolo COMDAT" y lo usa el enlazador junto con el campo de selección.

A continuación se muestran los valores del campo de selección.



| Constante                                        | Value         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEN \_ COMDAT \_ seleccionar \_ noduplicaciones <br/> | 1 <br/> | Si este símbolo ya está definido, el vinculador emite un error de "multiplicación de símbolo definido". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| IMAGEN \_ COMDAT \_ Seleccione \_ cualquiera <br/>          | 2 <br/> | Se puede vincular cualquier sección que defina el mismo símbolo COMDAT; el resto se quitan. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| \_la imagen \_ COMDAT \_ Seleccione \_ el mismo tamaño <br/>   | 3 <br/> | El vinculador elige una sección arbitraria entre las definiciones de este símbolo. Si todas las definiciones no tienen el mismo tamaño, se emite un error de "multiplicación de símbolo definido". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGEN \_ COMDAT \_ seleccionar \_ \_ coincidencia exacta <br/> | 4 <br/> | El vinculador elige una sección arbitraria entre las definiciones de este símbolo. Si todas las definiciones no coinciden exactamente, se emite un error de "multiplicación de símbolo definido". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGEN \_ COMDAT \_ seleccionar \_ asociativa <br/>  | 5 <br/> | La sección se vincula si se ha vinculado una determinada sección de COMDAT. Esta otra sección se indica mediante el campo de número del registro de símbolos auxiliar de la definición de la sección. Esta configuración es útil para las definiciones que tienen componentes en varias secciones (por ejemplo, código en uno y datos de otro), pero donde todos se deben vincular o descartar como un conjunto. La otra sección asociada a esta sección debe ser una sección de COMDAT, que puede ser otra sección de COMDAT asociativa. Una cadena de Asociación de sección de COMDAT asociativa no puede formar un bucle. La sección cadena de asociación debe llegar a una sección de COMDAT que no tenga la imagen \_ COMDAT \_ seleccionar \_ conjunto asociativo. <br/> |
| IMAGEN \_ COMDAT \_ seleccionar \_ más grande <br/>      | 6 <br/> | El enlazador elige la definición más grande entre todas las definiciones de este símbolo. Si varias definiciones tienen este tamaño, la opción entre ellas es arbitraria. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

#### <a name="clr-token-definition-object-only"></a>Definición de token de CLR (solo objeto)

Este símbolo auxiliar suele seguir el \_ token CLR de la clase Image SYM \_ \_ \_ . Se utiliza para asociar un token con el espacio de nombres de la tabla de símbolos de COFF.



| Offset        | Tamaño           | Campo                        | Descripción                                                                                |
|---------------|----------------|------------------------------|--------------------------------------------------------------------------------------------|
| 0 <br/> | 1 <br/>  | bAuxType <br/>         | Debe ser \_ un símbolo auxiliar de imagen \_ \_ tipo \_ \_ DEF (1). <br/>                              |
| 1 <br/> | 1 <br/>  | bReserved <br/>        | Reserved, debe ser cero. <br/>                                                        |
| 2 <br/> | 4 <br/>  | SymbolTableIndex <br/> | Índice de símbolos del símbolo COFF al que hace referencia esta definición de token de CLR. <br/> |
| 6 <br/> | 12 <br/> |                              | Reserved, debe ser cero. <br/>                                                        |



 

### <a name="coff-string-table"></a>Tabla de cadenas COFF

Inmediatamente después de la tabla de símbolos COFF se encuentra la tabla de cadenas COFF. La posición de esta tabla se encuentra tomando la dirección de la tabla de símbolos en el encabezado COFF y agregando el número de símbolos multiplicado por el tamaño de un símbolo.

Al principio de la tabla de cadenas COFF hay 4 bytes que contienen el tamaño total (en bytes) del resto de la tabla de cadenas. Este tamaño incluye el propio campo de tamaño, por lo que el valor de esta ubicación sería 4 Si no había ninguna cadena presente.

Después del tamaño, las cadenas terminadas en null a las que apuntan los símbolos de la tabla de símbolos COFF.

### <a name="the-attribute-certificate-table-image-only"></a>La tabla de certificados de atributo (solo imagen)

Los certificados de atributo se pueden asociar a una imagen agregando una tabla de certificados de atributo. La tabla de certificados de atributo se compone de un conjunto de entradas de certificado de atributos contiguos alineados con quadword. Se inserta un relleno de ceros entre el final original del archivo y el principio de la tabla de certificados de atributo para lograr esta alineación. Cada entrada de certificado de atributo contiene los campos siguientes.



| Offset       | Tamaño                         | Campo                       | Descripción                                                                                                |
|--------------|------------------------------|-----------------------------|------------------------------------------------------------------------------------------------------------|
| 0<br/> | 4<br/>                 | dwLength<br/>         | Especifica la longitud de la entrada del certificado de atributo. <br/>                                       |
| 4<br/> | 2<br/>                 | wRevision<br/>        | Contiene el número de versión del certificado. Para obtener más información, vea el siguiente texto.<br/>                   |
| 6<br/> | 2<br/>                 | wCertificateType<br/> | Especifica el tipo de contenido de bCertificate. Para obtener más información, vea el siguiente texto.<br/>             |
| 8<br/> | Consulte<br/> | bCertificate<br/>     | Contiene un certificado, como una firma Authenticode. Para obtener más información, vea el siguiente texto.<br/> |



 

El valor de la dirección virtual de la entrada de la tabla de certificados en el directorio opcional header Data es un desplazamiento de archivo a la primera entrada de certificado de atributo. Se tiene acceso a las siguientes entradas al avanzar los bytes de dwLength de la entrada, redondeados a un múltiplo de 8 bytes, desde el inicio de la entrada de certificado del atributo actual. Esto continúa hasta que la suma de los valores de dwLength redondeados es igual al valor de tamaño de la entrada de la tabla de certificados en el directorio de datos de encabezado opcional. Si la suma de los valores de dwLength redondeados no es igual al valor de tamaño, la tabla de certificados de atributo o el campo de tamaño está dañado.

Por ejemplo, si la entrada de la tabla de certificados del directorio de datos de encabezado opcional contiene:


```C++
virtual address = 0x5000
size = 0x1000
```



El primer certificado comienza en el desplazamiento 0x5000 desde el inicio del archivo en el disco. Para avanzar por todas las entradas de certificado de atributo:

1.  Agregue el valor dwLength del primer certificado de atributo al desplazamiento inicial.
2.  Redondee el valor del paso 1 hasta el múltiplo de 8 bytes más cercano para buscar el desplazamiento de la segunda entrada de certificado del atributo.
3.  Agregue el valor de desplazamiento del paso 2 al valor dwLength de la segunda entrada de certificado de atributo y redondee al múltiplo más cercano de 8 bytes para determinar el desplazamiento de la tercera entrada de certificado de atributo.
4.  Repita el paso 3 para cada certificado sucesivo hasta que el desplazamiento calculado sea igual a 0x6000 (0x5000 Start + 0x1000 (tamaño total), que indica que ha examinado toda la tabla.

Como alternativa, puede enumerar las entradas del certificado mediante una llamada a la función **ImageEnumerateCertificates** de Win32 en un bucle. Para obtener un vínculo a la página de referencia de la función, vea [referencias](#references).

Las entradas de la tabla de certificados de atributo pueden contener cualquier tipo de certificado, siempre que la entrada tenga el valor dwLength correcto, un valor wRevision único y un valor wCertificateType único. El tipo más común de entrada de tabla de certificados es una \_ estructura de certificados de Win, que se documenta en wintrust. h y se describe en el resto de esta sección.

Las opciones del \_ miembro **wRevision** del certificado Win incluyen (pero no se limitan a) lo siguiente.



| Value             | Nombre                                 | Notas                                                                                                                                                 |
|-------------------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0100<br/> | WIN \_ CERT \_ revisión \_ 1 \_ 0<br/> | Versión 1, versión heredada de la \_ estructura de certificados Win. Solo se admite con fines de comprobación de firmas Authenticode heredadas.<br/> |
| 0x0200<br/> | WIN \_ CERT \_ revisión \_ 2 \_ 0<br/> | La versión 2 es la versión actual de la \_ estructura de certificados Win. <br/>                                                                       |



 

Las opciones del \_ miembro **wCertificateType** del certificado Win incluyen (pero no se limitan a) los elementos de la tabla siguiente. Tenga en cuenta que algunos valores no se admiten actualmente.



| Value             | Nombre                                           | Notas                                                                                   |
|-------------------|------------------------------------------------|-----------------------------------------------------------------------------------------|
| 0x0001<br/> | \_Tipo de certificado Win \_ \_ X509 <br/>              | bCertificate contiene un certificado X. 509 <br/> No compatible<br/>         |
| 0x0002<br/> | tipo de certificado WIN con \_ \_ \_ \_ datos firmados PKCS \_<br/> | bCertificate contiene una \# estructura PKCS 7 SignedData<br/>                         |
| 0x0003<br/> | \_Tipo de certificado Win \_ \_ reservado \_ 1<br/>        | Reservado <br/>                                                                    |
| 0x0004<br/> | tipo de certificado WIN de \_ \_ pila de \_ TS \_ \_ firmado<br/>  | Terminal Server la firma de certificados de pila de protocolos <br/> No compatible<br/> |



 

El \_ miembro **bCertificate** de la estructura del certificado Win contiene una matriz de bytes de longitud variable con el tipo de contenido especificado por **wCertificateType**. El tipo admitido por Authenticode es \_ el \_ tipo \_ de certificado de Windows PKCS \_ signed \_ Data, una \# estructura PKCS 7 **SignedData** . Para obtener más información sobre el formato de firma digital de Authenticode, consulte [formato de firma ejecutable portable de Windows Authenticode](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx).

Si el contenido de **bCertificate** no termina en un límite de quadword, la entrada de certificado de atributo se rellena con ceros, desde el final de **bCertificate** hasta el siguiente límite de quadword.

El valor de **dwLength** es la longitud de la estructura de certificados Win finalizada \_ y se calcula como:

`dwLength = offsetof(WIN_CERTIFICATE, bCertificate) + (size of the variable-length binary array contained within bCertificate)`

Esta longitud debe incluir el tamaño de cualquier relleno que se use para satisfacer el requisito de que \_ se quadword alinea cada estructura de certificado de Win:

` dwLength += (8 - (dwLength & 7)) & 7;`

Tamaño de la **tabla de certificados**: especificado en la entrada de la **tabla de certificados** en los directorios de [datos de encabezado opcionales (solo imagen)](#optional-header-data-directories-image-only): incluye el relleno.

Para obtener más información sobre el uso de la API ImageHlp para enumerar, agregar y quitar certificados de archivos PE, consulte [funciones imagehlp](imagehlp-functions.md).

#### <a name="certificate-data"></a>Datos de certificado

Como se indicó en la sección anterior, los certificados de la tabla de certificados de atributo pueden contener cualquier tipo de certificado. Los certificados que garantizan la integridad de un archivo PE pueden incluir un hash de imagen PE.

Un hash de imagen PE (o hash de archivo) es similar a una suma de comprobación de archivo en que el algoritmo hash genera una síntesis del mensaje que está relacionada con la integridad de un archivo. Sin embargo, una suma de comprobación se genera mediante un algoritmo simple y se usa principalmente para detectar si un bloque de memoria del disco ha desaparecido mal y los valores almacenados allí están dañados. Un hash de archivo es similar a una suma de comprobación en que también detecta daños en los archivos. Sin embargo, a diferencia de la mayoría de los algoritmos de suma de comprobación, es muy difícil modificar un archivo sin cambiar el hash de archivo de su valor original no modificado. Por tanto, se puede usar un hash de archivo para detectar modificaciones intencionadas e incluso sutiles en un archivo, como las introducidas por virus, hackers o programas troyanos.

Cuando se incluye en un certificado, el Resumen de la imagen debe excluir determinados campos de la imagen de PE, como la entrada de la tabla de certificados y la suma de comprobación en directorios opcionales de datos de encabezado. Esto se debe a que la acción de agregar un certificado cambia estos campos y haría que se calculara un valor hash diferente.

La función **ImageGetDigestStream** de Win32 proporciona un flujo de datos de un archivo PE de destino con el que aplicar el algoritmo hash a las funciones. Este flujo de datos sigue siendo coherente cuando se agregan o se quitan certificados en un archivo PE. En función de los parámetros que se pasan a **ImageGetDigestStream**, se pueden omitir otros datos de la imagen PE en el cálculo de hash. Para obtener un vínculo a la página de referencia de la función, vea [referencias](#references).

### <a name="delay-load-import-tables-image-only"></a>Delay-Load importar tablas (solo imagen)

Estas tablas se agregaron a la imagen para admitir un mecanismo uniforme para que las aplicaciones retrasen la carga de un archivo DLL hasta la primera llamada a ese archivo DLL. El diseño de las tablas coincide con el de las tablas de importación tradicionales que se describen en la sección 6,4, [sección. idata](#the-idata-section). Aquí solo se describen algunos detalles.

#### <a name="the-delay-load-directory-table"></a>Tabla del directorio Delay-Load

La tabla de directorio de carga retrasada es el homólogo de la tabla de importación de directorio. Se puede recuperar a través de la entrada Delay Import descriptor en la lista de directorios de encabezados de datos opcionales (desplazamiento 200). La tabla se organiza de la siguiente manera:



| Offset         | Tamaño          | Campo                                  | Descripción                                                                                                                                                                                                                                                                                                                  |
|----------------|---------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Atributos <br/>                 | Debe ser cero. <br/>                                                                                                                                                                                                                                                                                                    |
| 4 <br/>  | 4 <br/> | Nombre <br/>                       | RVA del nombre del archivo DLL que se va a cargar. El nombre reside en la sección de datos de solo lectura de la imagen. <br/>                                                                                                                                                                                                        |
| 8 <br/>  | 4 <br/> | Identificador de módulo <br/>              | RVA del identificador de módulo (en la sección de datos de la imagen) del archivo DLL que se va a cargar con retraso. Se usa para el almacenamiento mediante la rutina suministrada para administrar la carga retrasada. <br/>                                                                                                                                   |
| 12 <br/> | 4 <br/> | Tabla de direcciones de importación retrasada <br/> | RVA de la tabla de direcciones de importación de carga retrasada. Para obtener más información, vea [retrasar la tabla de direcciones de importación (IAT)](#delay-import-address-table). <br/>                                                                                                                                                                       |
| 16 <br/> | 4 <br/> | Tabla retrasar nombre de importación <br/>    | La RVA de la tabla de nombres de carga retrasada, que contiene los nombres de las importaciones que pueden ser necesarias para cargarse. Esto coincide con el diseño de la tabla de nombres de importación. Para obtener más información, vea [sugerencia/nombre](#hintname-table)de la tabla.<br/>                                                                                       |
| 20 <br/> | 4 <br/> | Tabla de importación de retraso enlazado <br/>   | RVA de la tabla de direcciones de carga retrasada enlazada, si existe. <br/>                                                                                                                                                                                                                                                     |
| 24 <br/> | 4 <br/> | Descargar tabla de retrasos de importación <br/>  | RVA de la tabla de direcciones de carga retrasada de descarga, si existe. Se trata de una copia exacta de la tabla de direcciones de importación retrasada. Si el autor de la llamada descarga el archivo DLL, esta tabla debe volver a copiarse en la tabla de direcciones de importación retrasada, de modo que las llamadas subsiguientes a la DLL sigan usando correctamente el mecanismo de thunk. <br/> |
| 28 <br/> | 4 <br/> | Marca de tiempo <br/>                 | Marca de tiempo de la DLL a la que se ha enlazado esta imagen. <br/>                                                                                                                                                                                                                                                     |



 

Las tablas a las que se hace referencia en esta estructura de datos se organizan y ordenan igual que sus homólogos para las importaciones tradicionales. Para obtener más información, vea [la sección. idata](#the-idata-section).

#### <a name="attributes"></a>Atributos

Como todavía, no se definen marcas de atributo. El enlazador establece este campo en cero en la imagen. Este campo se puede utilizar para extender el registro indicando la presencia de nuevos campos, o bien se puede usar para indicar comportamientos a las funciones auxiliares Delay o unload.

#### <a name="name"></a>Nombre

El nombre de la DLL en la que se va a cargar el retraso reside en la sección de datos de solo lectura de la imagen. Se hace referencia a él a través del campo szName.

#### <a name="module-handle"></a>Identificador de módulo

El identificador de la DLL que se va a cargar con retraso está en la sección de datos de la imagen. El campo phmod apunta al identificador. La aplicación auxiliar de carga retrasada proporcionada utiliza esta ubicación para almacenar el identificador en el archivo DLL cargado.

#### <a name="delay-import-address-table"></a>Tabla de direcciones de importación retrasada

Se hace referencia a la tabla de direcciones de importación retrasada (IAT) mediante el descriptor de importación de retraso a través del campo pIAT. La aplicación auxiliar de carga retrasada actualiza estos punteros con los puntos de entrada reales para que los thunks dejen de estar en el bucle de llamada. Se tiene acceso a los punteros a función mediante la expresión `pINT->u1.Function` .

#### <a name="delay-import-name-table"></a>Tabla retrasar nombre de importación

La tabla retrasar importación de nombres (INT) contiene los nombres de las importaciones que pueden requerir cargarse. Se ordenan de la misma manera que los punteros de función de la IAT. Se componen de las mismas estructuras que el INT estándar y se obtiene acceso a ellas mediante la expresión `pINT->u1.AddressOfData->Name[0]` .

#### <a name="delay-bound-import-address-table-and-time-stamp"></a>Tabla de direcciones de importación enlazada retrasada y marca de tiempo

La tabla de direcciones de importación enlazada retrasada (BIAT) es una tabla opcional de \_ elementos de datos de código THUNK de imagen \_ que se usa junto con el campo de marca de tiempo de la tabla de directorio de carga retrasada mediante una fase de enlace posterior al proceso.

#### <a name="delay-unload-import-address-table"></a>Tabla de direcciones de importación de descarga retrasada

La tabla de direcciones de importación de descarga retrasada (UIAT) es una tabla opcional de \_ elementos de datos de código THUNK de imagen \_ que el código de descarga utiliza para controlar una solicitud de descarga explícita. Consta de datos inicializados en la sección de solo lectura que es una copia exacta de la tabla IAT original que hacía referencia al código a los thunks de carga retrasada. En la solicitud de descarga, se puede liberar la biblioteca, se ha \* borrado el phmod y el UIAT se ha escrito sobre la tabla IAT para restaurar todo el estado de la precarga.

## <a name="special-sections"></a>Secciones especiales

- [Sección. Debug](#the-debug-section)
  - [Directorio de depuración (solo imagen)](#debug-directory-image-only)
  - [Tipo de depuración](#debug-type)
  - [. Debug $ F (solo objeto)](#debugf-object-only)
  - [. Debug $ S (solo objeto)](#debugs-object-only)
  - [. Debug $ P (solo objeto)](#debugp-object-only)
  - [. Debug $ T (solo objeto)](#debugt-object-only)
  - [Compatibilidad del vinculador con la información de depuración de Microsoft](#linker-support-for-microsoft-debug-information)
- [La sección. drectve (solo objeto)](#the-drectve-section-object-only)
- [La sección. EDATA (solo imagen)](#the-edata-section-image-only)
  - [Exportar tabla de directorio](#export-directory-table)
  - [Exportar tabla de direcciones](#export-address-table)
  - [Tabla de punteros de nombre de exportación](#export-name-pointer-table)
  - [Exportar tabla ordinal](#export-ordinal-table)
  - [Exportar tabla de nombres](#export-name-table)
- [La sección. idata](#the-idata-section)
  - [Importar tabla de directorio](#import-directory-table)
  - [Importar tabla de búsqueda](#import-lookup-table)
  - [Sugerencia/nombre (tabla)](#hintname-table)
  - [Importar tabla de direcciones](#delay-import-address-table)
- [La sección. pdata](#the-pdata-section)
- [La sección. reloc (solo imagen)](#the-reloc-section-image-only)
  - [Bloque de reubicación base](#base-relocation-block)
  - [Tipos de reubicación base](#base-relocation-types)
- [La sección. TLS](#the-tls-section)
  - [Directorio TLS](#the-tls-directory)
  - [Funciones de devolución de llamada TLS](#tls-callback-functions)
- [La estructura de configuración de carga (solo imagen)](#the-load-configuration-structure-image-only)
  - [Cargar directorio de configuración](#load-configuration-directory)
  - [Cargar diseño de configuración](#load-configuration-layout)
- [La sección. rsrc](#the-rsrc-section)
  - [Tabla del directorio de recursos](#resource-directory-table)
  - [Entradas de directorio de recursos](#resource-directory-entries)
  - [Cadena de directorio de recursos](#resource-directory-string)
  - [Entrada de datos de recursos](#resource-data-entry)
- [La sección. cormeta (solo objeto)](#the-cormeta-section-object-only)
- [La sección. sxdata](#the-sxdata-section)

Las secciones COFF típicas contienen código o datos que los enlazadores y los cargadores de Microsoft Win32 procesan sin un conocimiento especial del contenido de la sección. El contenido solo es relevante para la aplicación que se va a vincular o ejecutar.

Sin embargo, algunas secciones COFF tienen significados especiales cuando se encuentran en archivos objeto o archivos de imagen. Las herramientas y los cargadores reconocen estas secciones porque tienen marcas especiales establecidas en el encabezado de la sección, porque las ubicaciones especiales del encabezado de la imagen opcional apuntan a ellas, o porque el propio nombre de la sección indica una función especial de la sección. (Aunque el nombre de la sección no indique una función especial de la sección, el nombre de la sección está dictado por Convención, por lo que los autores de esta especificación pueden hacer referencia a un nombre de sección en todos los casos).

Las secciones reservadas y sus atributos se describen en la tabla siguiente, seguida de descripciones detalladas de los tipos de secciones que se almacenan en los archivos ejecutables y los tipos de sección que contienen metadatos para las extensiones.



| Nombre de sección          | Contenido                                                                                                                                                                  | Características                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| . BSS <br/>      | Datos no inicializados (formato libre) <br/>                                                                                                                             | IMAGE SCN de la imagen de \_ \_ \_ datos sin inicializar \_ \| \_ \_ \_ \| \_ \_ \_ <br/>                                                                                                                                                                                                                                                                                               |
| .cormeta <br/>  | Metadatos de CLR que indican que el archivo objeto contiene código administrado <br/>                                                                                       | IMAGE \_ SCN \_ lnk \_ info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| . Data <br/>     | Datos inicializados (formato libre) <br/>                                                                                                                               | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la \_ \| imagen \_ SCN \_ MEM memoria \_ lectura de \| imagen \_ \_ \_ <br/>                                                                                                                                                                                                                                                                                                 |
| . Debug $ F <br/>  | Información de depuración FPO generada (solo objeto, arquitectura x86 y ahora obsoleta) <br/>                                                                       | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de \_ \| \_ \_ \_ \| \_ \_ la imagen SCN \_ de la imagen de SCN <br/>                                                                                                                                                                                                                                                                                           |
| . Debug $ P <br/>  | Tipos de depuración precompilados (solo objeto) <br/>                                                                                                                        | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de \_ \| \_ \_ \_ \| \_ \_ la imagen SCN \_ de la imagen de SCN <br/>                                                                                                                                                                                                                                                                                           |
| . Debug $ S <br/>  | Símbolos de depuración (solo objeto) <br/>                                                                                                                                  | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de \_ \| \_ \_ \_ \| \_ \_ la imagen SCN \_ de la imagen de SCN <br/>                                                                                                                                                                                                                                                                                           |
| . Debug $ T <br/>  | Tipos de depuración (solo objeto) <br/>                                                                                                                                    | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de \_ \| \_ \_ \_ \| \_ \_ la imagen SCN \_ de la imagen de SCN <br/>                                                                                                                                                                                                                                                                                           |
| .drective <br/> | Opciones del enlazador <br/>                                                                                                                                               | IMAGE \_ SCN \_ lnk \_ info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .edata <br/>    | Exportar tablas <br/>                                                                                                                                                | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la \_ Image de \| \_ SCN \_ lectura de memoria \_ <br/>                                                                                                                                                                                                                                                                                                                           |
| .idata <br/>    | Importar tablas <br/>                                                                                                                                                | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la \_ \| imagen \_ SCN \_ MEM memoria \_ lectura de \| imagen \_ \_ \_ <br/>                                                                                                                                                                                                                                                                                                 |
| . idlsym insertadas <br/>   | Incluye SEH (solo imagen) registrado para admitir atributos IDL. Para obtener más información, vea "atributos IDL" en [referencias](#references) al final de este tema. <br/> | IMAGE \_ SCN \_ lnk \_ info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| . pdata <br/>    | Información de la excepción <br/>                                                                                                                                        | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la \_ Image de \| \_ SCN \_ lectura de memoria \_ <br/>                                                                                                                                                                                                                                                                                                                           |
| . rdata <br/>    | Datos inicializados de solo lectura <br/>                                                                                                                                   | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la \_ Image de \| \_ SCN \_ lectura de memoria \_ <br/>                                                                                                                                                                                                                                                                                                                           |
| . reloc <br/>    | Reubicaciones de imágenes <br/>                                                                                                                                            | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de \_ \| \_ \_ \_ \| \_ \_ la imagen SCN \_ de la imagen de SCN <br/>                                                                                                                                                                                                                                                                                           |
| . rsrc <br/>     | Directorio de recursos <br/>                                                                                                                                           | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la \_ Image de \| \_ SCN \_ lectura de memoria \_ <br/>                                                                                                                                                                                                                                                                                                                           |
| .sbss <br/>     | Datos no inicializados relativos a GP (formato libre) <br/>                                                                                                                 | IMAGE SCN de la imagen de \_ \_ datos no \_ inicializada SCN \_ de la imagen de la imagen de la \| \_ \_ memoria \_ \| \_ \_ \_ \| \_ \_ de GPREL de la impresión de la imagen SCN GPREL la \_ marca Image SCN \_ debe establecerse solo para arquitecturas ia64; esta marca no es válida para otras arquitecturas. La \_ marca Image SCN \_ GPREL es solo para archivos objeto; cuando este tipo de sección aparece en un archivo de imagen, \_ \_ no se debe establecer la marca Image SCN GPREL. <br/> |
| . sdata <br/>    | Datos inicializados relativos a GP (formato libre) <br/>                                                                                                                   | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la imagen \_ \| \_ SCN \_ MEM memoria \_ lectura \| IMAGE SCN \_ \_ MEM mem \_ \| Image \_ SCN \_ GPREL la \_ marca Image SCN \_ GPREL se debe establecer solo para arquitecturas ia64; esta marca no es válida para otras arquitecturas. La \_ marca Image SCN \_ GPREL es solo para archivos objeto; cuando este tipo de sección aparece en un archivo de imagen, \_ \_ no se debe establecer la marca Image SCN GPREL. <br/>   |
| .srdata <br/>   | Datos de solo lectura relativos a GP (formato libre) <br/>                                                                                                                     | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la imagen \_ \| \_ SCN \_ \_ \| \_ \_ de la imagen de GPREL de la imagen \_ . la marca Image SCN \_ GPREL debe establecerse solo para arquitecturas ia64; esta marca no es válida para otras arquitecturas. La \_ marca Image SCN \_ GPREL es solo para archivos objeto; cuando este tipo de sección aparece en un archivo de imagen, \_ \_ no se debe establecer la marca Image SCN GPREL. <br/>                             |
| .sxdata <br/>   | Datos registrados del controlador de excepciones (solo formato libre y x86/objeto) <br/>                                                                                          | IMAGE \_ SCN \_ lnk \_ info contiene el índice de símbolos de cada uno de los controladores de excepciones a los que hace referencia el código de ese archivo objeto. El símbolo puede ser para un símbolo UNDEF o uno que se haya definido en ese módulo. <br/>                                                                                                                                                                     |
| .text <br/>     | Código ejecutable (formato libre) <br/>                                                                                                                                | IMAGE \_ SCN \_ CNT \_ code \| Image \_ SCN \_ MEM \_ Execute \| IIMAGE \_ SCN \_ MEM \_ Read <br/>                                                                                                                                                                                                                                                                                                           |
| . TLS <br/>      | Almacenamiento local de subprocesos (solo objeto) <br/>                                                                                                                           | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la \_ \| imagen \_ SCN \_ MEM memoria \_ lectura de \| imagen \_ \_ \_ <br/>                                                                                                                                                                                                                                                                                                 |
| . TLS $ <br/>     | Almacenamiento local de subprocesos (solo objeto) <br/>                                                                                                                           | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la \_ \| imagen \_ SCN \_ MEM memoria \_ lectura de \| imagen \_ \_ \_ <br/>                                                                                                                                                                                                                                                                                                 |
| .vsdata <br/>   | Datos inicializados relativos a GP (formato libre y solo para arquitecturas ARM, SH4 y Thumb) <br/>                                                                    | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la \_ \| imagen \_ SCN \_ MEM memoria \_ lectura de \| imagen \_ \_ \_ <br/>                                                                                                                                                                                                                                                                                                 |
| . xdata <br/>    | Información de la excepción (formato libre) <br/>                                                                                                                          | IMAGE SCN de la imagen de \_ \_ \_ datos inicializados de la \_ Image de \| \_ SCN \_ lectura de memoria \_ <br/>                                                                                                                                                                                                                                                                                                                           |



 

Algunas de las secciones que se enumeran aquí están marcadas como "solo objeto" o "solo imagen" para indicar que su semántica especial solo es relevante para los archivos objeto o los archivos de imagen, respectivamente. Una sección que está marcada como "solo imagen" podría seguir apareciendo en un archivo objeto como una manera de entrar en el archivo de imagen, pero la sección no tiene un significado especial para el vinculador, solo en el cargador de archivos de imagen.

### <a name="the-debug-section"></a>Sección. Debug

La sección. Debug se usa en archivos objeto para contener información de depuración generada por el compilador y en archivos de imagen que contengan toda la información de depuración que se genera. En esta sección se describe el empaquetado de la información de depuración en archivos de objeto e imagen.

En la sección siguiente se describe el formato del directorio de depuración, que puede encontrarse en cualquier parte de la imagen. En las secciones siguientes se describen los "grupos" en archivos objeto que contienen información de depuración.

El valor predeterminado para el vinculador es que la información de depuración no está asignada en el espacio de direcciones de la imagen. Una sección. Debug solo existe cuando la información de depuración está asignada en el espacio de direcciones.

#### <a name="debug-directory-image-only"></a>Directorio de depuración (solo imagen)

Los archivos de imagen contienen un directorio de depuración opcional que indica qué forma de información de depuración está presente y dónde se encuentra. Este directorio consta de una matriz de entradas del directorio Debug cuya ubicación y tamaño se indican en el encabezado opcional Image.

El directorio de depuración puede estar en una sección descartable. debug (si existe), o puede incluirse en cualquier otra sección del archivo de imagen o no estar en una sección.

Cada entrada del directorio de depuración identifica la ubicación y el tamaño de un bloque de información de depuración. La RVA especificada puede ser cero si la información de depuración no está incluida en un encabezado de sección (es decir, reside en el archivo de imagen y no está asignada en el espacio de direcciones en tiempo de ejecución). Si se asigna, la RVA es su dirección.

Una entrada de directorio de depuración tiene el siguiente formato:



| Offset         | Tamaño          | Campo                        | Descripción                                                                                                                                            |
|----------------|---------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Características <br/>  | Reserved, debe ser cero. <br/>                                                                                                                    |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>    | Fecha y hora en que se crearon los datos de depuración. <br/>                                                                                         |
| 8 <br/>  | 2 <br/> | MajorVersion <br/>     | Número de versión principal del formato de datos de depuración. <br/>                                                                                         |
| 10 <br/> | 2 <br/> | MinorVersion <br/>     | Número de versión secundaria del formato de datos de depuración. <br/>                                                                                         |
| 12 <br/> | 4 <br/> | Tipo <br/>             | Formato de la información de depuración. Este campo habilita la compatibilidad con varios depuradores. Para obtener más información, vea [Debug Type](#debug-type).<br/> |
| 16 <br/> | 4 <br/> | SizeOfData <br/>       | Tamaño de los datos de depuración (sin incluir el propio directorio de depuración). <br/>                                                                     |
| 20 <br/> | 4 <br/> | AddressOfRawData <br/> | La dirección de los datos de depuración cuando se cargan, en relación con la base de la imagen. <br/>                                                                     |
| 24 <br/> | 4 <br/> | PointerToRawData <br/> | Puntero de archivo a los datos de depuración. <br/>                                                                                                        |



 

#### <a name="debug-type"></a>Tipo de depuración

Los siguientes valores se definen para el campo de tipo de la entrada de directorio Debug:



| Constante                                        | Value          | Descripción                                                                                                                                                                                                      |
|-------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipo de depuración de imagen \_ \_ desconocido <br/>         | 0 <br/>  | Valor desconocido que todas las herramientas omiten. <br/>                                                                                                                                                       |
| \_tipo de depuración de imagen \_ \_ COFF <br/>            | 1 <br/>  | La información de depuración de COFF (números de línea, tabla de símbolos y tabla de cadenas). Los campos de los encabezados de archivo también señalan a este tipo de información de depuración. <br/>                                          |
| \_tipo de depuración de imagen \_ \_ CODEVIEW <br/>        | 2 <br/>  | Información de depuración de Visual C++. <br/>                                                                                                                                                                    |
| \_tipo de depuración de imagen \_ \_ FPO <br/>             | 3 <br/>  | La información de omisión de puntero de marco (FPO). Esta información indica al depurador cómo interpretar marcos de pila no estándar, que usan el registro EBP para un propósito distinto de un puntero de marco. <br/> |
| \_tipo de depuración de imagen \_ \_ varios <br/>            | 4 <br/>  | Ubicación del archivo DBG. <br/>                                                                                                                                                                            |
| \_excepción de tipo de depuración de imagen \_ \_ <br/>       | 5 <br/>  | Una copia de la sección. pdata. <br/>                                                                                                                                                                            |
| \_corrección de tipo de depuración de imagen \_ \_ <br/>           | 6 <br/>  | Reservado. <br/>                                                                                                                                                                                            |
| \_tipo de depuración \_ de imagen \_ OMAP \_ a \_ src <br/>   | 7 <br/>  | Asignación de una RVA en una imagen a una RVA en la imagen de origen. <br/>                                                                                                                                          |
| \_tipo de depuración \_ de imagen \_ OMAP \_ de \_ src <br/> | 8 <br/>  | Asignación de una RVA en una imagen de origen a una RVA en la imagen. <br/>                                                                                                                                          |
| \_tipo de depuración de imagen \_ \_ Borland <br/>         | 9 <br/>  | Reservado para Borland. <br/>                                                                                                                                                                                |
| \_Tipo de depuración de imagen \_ \_ RESERVED10 <br/>      | 10 <br/> | Reservado. <br/>                                                                                                                                                                                            |
| \_tipo de depuración de imagen \_ \_ CLSID <br/>           | 11 <br/> | Reservado. <br/>                                                                                                                                                                                            |
| \_reproducción de tipo de depuración de imagen \_ \_ <br/>           | 16 <br/> | Determinismo o reproducibilidad de PE. <br/>                                                                                                                                                                   |
| \_tipo de depuración de imagen \_ \_ ex \_ DLLCHARACTERISTICS | 20 | Bits de características de DLL extendidas. |



 

Si el campo de tipo se establece en IMAGE \_ Debug \_ Type \_ FPO, los datos sin procesar de depuración son una matriz en la que cada miembro describe el marco de pila de una función. No todas las funciones del archivo de imagen deben tener definida la información de FPO, aunque el tipo de depuración sea FPO. Se supone que las funciones que no tienen información de FPO tienen marcos de pila normales. El formato de la información de FPO es el siguiente:


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



La presencia de una entrada de tipo IMAGE \_ Debug \_ Type \_ reproducción indica que el archivo PE está integrado de una manera de lograr el determinismo o la reproducibilidad. Si la entrada no cambia, se garantiza que el archivo PE de salida es idéntico en bit a bit, con independencia de Cuándo o dónde se produzca el PE. Varios campos de marca de fecha y hora del archivo PE se rellenan con parte o con todos los bits de un valor hash calculado que usa el contenido del archivo PE como entrada y, por tanto, ya no representan la fecha y hora reales en que se produce un archivo PE o datos específicos relacionados dentro del PE. Los datos sin procesar de esta entrada de depuración pueden estar vacíos o pueden contener un valor hash calculado precedido por un valor de cuatro bytes que representa la longitud del valor hash.

Si el campo de tipo se establece en IMAGE \_ Debug \_ Type \_ ex \_ DLLCHARACTERISTICS, la depuración de datos sin procesar contiene bits de características de dll extendidas, en vez de los que se podrían establecer en el encabezado opcional de la imagen. Vea [características de dll](#dll-characteristics) en la sección [encabezado opcional Windows-Specific campos (solo imagen)](#optional-header-windows-specific-fields-image-only).

##### <a name="extended-dll-characteristics"></a>Características de DLL extendidas

Los siguientes valores se definen para los bits de características de la DLL extendida.

| Constante | Value | Descripción |
|-|-|-|
| compatibilidad con la imagen \_ DLLCHARACTERISTICS \_ ex \_ CET \_ | 0x0001 | La imagen es compatible con CET. |

#### <a name="debugf-object-only"></a>. Debug $ F (solo objeto)

Los datos de esta sección se han sustituido en Visual C++ versión 7,0 y posteriores por un conjunto de datos más amplio que se emite en una subsección **. Debug $ S** .

Los archivos objeto pueden contener secciones. Debug $ F cuyo contenido es uno o más \_ registros de datos de FPO (información de omisión del puntero de marco). Vea "IMAGE \_ Debug \_ Type \_ FPO" en el [tipo de depuración](#debug-type).

El vinculador reconoce estos registros **. Debug $ F** . Si se genera información de depuración, el vinculador ordena los \_ registros de datos de FPO por el procedimiento RVA y genera una entrada de directorio de depuración para ellos.

El compilador no debe generar registros FPO para los procedimientos que tengan un formato de fotograma estándar.

#### <a name="debugs-object-only"></a>. Debug $ S (solo objeto)

Esta sección contiene Visual C++ información de depuración (información simbólica).

#### <a name="debugp-object-only"></a>. Debug $ P (solo objeto)

Esta sección contiene Visual C++ información de depuración (información precompilada). Se trata de tipos compartidos entre todos los objetos compilados mediante el encabezado precompilado que se generó con este objeto.

#### <a name="debugt-object-only"></a>. Debug $ T (solo objeto)

Esta sección contiene Visual C++ información de depuración (información de tipo).

#### <a name="linker-support-for-microsoft-debug-information"></a>Compatibilidad del vinculador con la información de depuración de Microsoft

Para admitir la información de depuración, el enlazador:

-   Recopila todos los datos de depuración pertinentes de las secciones **. Debug $ F**, **Debug $ S**, **. Debug $ P** y **. Debug $ T** .

-   Procesa los datos junto con la información de depuración generada por el enlazador en el archivo PDB y crea una entrada de directorio de depuración para hacer referencia a él.

### <a name="the-drectve-section-object-only"></a>La sección. drectve (solo objeto)

Una sección es una sección de directivas si tiene la \_ marca Image SCN \_ lnk \_ info establecida en el encabezado de la sección y tiene el nombre de sección **. drectve** . El vinculador quita una sección **. drectve** después de procesar la información, por lo que la sección no aparece en el archivo de imagen que se está vinculando.

Una sección **. drectve** consta de una cadena de texto que se puede codificar como ANSI o UTF-8. Si el marcador de orden de bytes UTF-8 (BOM, un prefijo de tres bytes que consta de 0xEF, 0xBB y 0xBF) no está presente, la cadena de Directiva se interpreta como ANSI. La cadena de directiva es una serie de opciones del vinculador separadas por espacios. Cada opción contiene un guión, el nombre de la opción y cualquier atributo adecuado. Si una opción contiene espacios, la opción debe ir entre comillas. La sección **. drectve** no debe tener reubicaciones ni números de línea.

### <a name="the-edata-section-image-only"></a>La sección. EDATA (solo imagen)

La sección Export Data, denominada. EDATA, contiene información sobre los símbolos a los que pueden acceder otras imágenes a través de la vinculación dinámica. Los símbolos exportados se suelen encontrar en archivos dll, pero los archivos dll también pueden importar símbolos.

A continuación se describe la estructura general de la sección de exportación. Las tablas descritas suelen ser contiguas en el archivo en el orden mostrado (aunque esto no es necesario). Solo se necesitan la tabla exportar directorio y la tabla dirección de exportación para exportar los símbolos como ordinales. (Un ordinal es una exportación a la que se accede directamente mediante el índice de la tabla de direcciones de exportación). Las tablas de puntero de nombre, tabla ordinal y nombre de exportación existen para admitir el uso de nombres de exportación.



| Nombre de la tabla                         | Descripción                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exportar tabla de directorio <br/> | Una tabla con una sola fila (a diferencia del directorio de depuración). En esta tabla se indican las ubicaciones y los tamaños de las demás tablas de exportación. <br/>                                                                                                                                                                                                               |
| Exportar tabla de direcciones <br/>   | Una matriz de RVA de símbolos exportados. Estas son las direcciones reales de las funciones exportadas y los datos de las secciones de datos y el código ejecutable. Otros archivos de imagen pueden importar un símbolo mediante el uso de un índice en esta tabla (un ordinal) o, opcionalmente, mediante el nombre público que corresponde al ordinal si se define un nombre público. <br/> |
| Tabla de punteros de nombre <br/>     | Matriz de punteros a los nombres de exportación públicos, ordenados en orden ascendente. <br/>                                                                                                                                                                                                                                                                    |
| Tabla ordinal <br/>          | Matriz de los ordinales que corresponden a los miembros de la tabla de puntero de nombre. La correspondencia es por posición; por lo tanto, la tabla de punteros de nombre y la tabla ordinal deben tener el mismo número de miembros. Cada ordinal es un índice de la tabla de direcciones de exportación. <br/>                                                                        |
| Exportar tabla de nombres <br/>      | Una serie de cadenas ASCII terminadas en NULL. Los miembros de la tabla de puntero de nombre apuntan a esta área. Estos nombres son los nombres públicos a través de los cuales se importan y exportan los símbolos; no son necesariamente los mismos que los nombres privados que se usan en el archivo de imagen. <br/>                                                           |



 

Cuando otro archivo de imagen importa un símbolo por su nombre, el cargador de Win32 busca en la tabla de punteros de nombre una cadena coincidente. Si se encuentra una cadena coincidente, el ordinal asociado se identifica buscando el miembro correspondiente en la tabla ordinal (es decir, el miembro de la tabla ordinal con el mismo índice que el puntero de cadena que se encuentra en la tabla de puntero de nombre). El ordinal resultante es un índice de la tabla de direcciones de exportación que proporciona la ubicación real del símbolo deseado. Se puede tener acceso a cada símbolo de exportación mediante un ordinal.

Cuando otro archivo de imagen importa un símbolo por ordinal, no es necesario buscar en la tabla de punteros de nombre una cadena coincidente. El uso directo de un ordinal es, por lo tanto, más eficaz. Sin embargo, un nombre de exportación es más fácil de recordar y no requiere que el usuario conozca el índice de la tabla para el símbolo.

#### <a name="export-directory-table"></a>Exportar tabla de directorio

La información de símbolos de exportación comienza con la tabla exportar directorio, que describe el resto de la información de símbolos de exportación. La tabla exportar directorio contiene información de la dirección que se usa para resolver las importaciones en los puntos de entrada de esta imagen.



| Offset         | Tamaño          | Campo                                | Descripción                                                                                                                                                               |
|----------------|---------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Exportar marcas <br/>             | Reserved, debe ser 0. <br/>                                                                                                                                          |
| 4 <br/>  | 4 <br/> | Marca de fecha y hora <br/>          | Fecha y hora en que se crearon los datos de exportación. <br/>                                                                                                           |
| 8 <br/>  | 2 <br/> | Major Version <br/>            | Número de versión principal. El usuario puede establecer los números de versión principal y secundaria. <br/>                                                                         |
| 10 <br/> | 2 <br/> | Minor Version <br/>            | Número de versión secundaria. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Nombre RVA <br/>                 | Dirección de la cadena ASCII que contiene el nombre del archivo DLL. Esta dirección es relativa a la base de la imagen. <br/>                                                |
| 16 <br/> | 4 <br/> | Base ordinal <br/>             | Número ordinal inicial de las exportaciones de esta imagen. Este campo especifica el número ordinal inicial de la tabla de direcciones de exportación. Normalmente, se establece en 1. <br/> |
| 20 <br/> | 4 <br/> | Entradas de la tabla de direcciones <br/>    | El número de entradas de la tabla de direcciones de exportación. <br/>                                                                                                            |
| 24 <br/> | 4 <br/> | Número de punteros de nombre <br/>  | Número de entradas de la tabla de puntero de nombre. Este también es el número de entradas de la tabla ordinal. <br/>                                                     |
| 28 <br/> | 4 <br/> | Exportar tabla de direcciones RVA <br/> | La dirección de la tabla de direcciones de exportación, relativa a la base de la imagen. <br/>                                                                                          |
| 32 <br/> | 4 <br/> | RVA del puntero de nombre <br/>         | La dirección de la tabla de puntero de nombre de exportación, relativa a la base de la imagen. El tamaño de la tabla viene determinado por el campo número de punteros de nombre. <br/>                       |
| 36 <br/> | 4 <br/> | RVA de tabla ordinal <br/>        | Dirección de la tabla ordinal, relativa a la base de la imagen. <br/>                                                                                                 |



 

#### <a name="export-address-table"></a>Exportar tabla de direcciones

La tabla de direcciones de exportación contiene la dirección de los puntos de entrada exportados y los datos exportados y los absolutos. Se usa un número ordinal como índice en la tabla de direcciones de exportación.

Cada entrada de la tabla de direcciones de exportación es un campo que usa uno de los dos formatos de la tabla siguiente. Si la dirección especificada no está en la sección de exportación (tal y como se define en la dirección y la longitud que se indican en el encabezado opcional), el campo es una RVA de exportación, que es una dirección real en código o datos. De lo contrario, el campo es una RVA de reenviador, que asigna un nombre a un símbolo en otro archivo DLL.



| Offset        | Tamaño          | Campo                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------|---------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Exportar RVA <br/>    | La dirección del símbolo exportado cuando se carga en la memoria, en relación con la base de la imagen. Por ejemplo, la dirección de una función exportada. <br/>                                                                                                                                                                                                                                                                                                       |
| 0 <br/> | 4 <br/> | RVA del reenviador <br/> | Puntero a una cadena ASCII terminada en null en la sección Export. Esta cadena debe estar dentro del intervalo especificado por la entrada exportar directorio de datos de tabla. Consulte [directorios opcionales de datos de encabezado (solo imagen)](#optional-header-data-directories-image-only). Esta cadena proporciona el nombre del archivo DLL y el nombre de la exportación (por ejemplo, "MYDLL. expfunc") o el nombre de la DLL y el número ordinal de la exportación (por ejemplo, "MYDLL. \# 27 "). <br/> |



 

Una RVA de reenviador exporta una definición de otra imagen, lo que hace que parezca que la imagen actual la estaba exportando. Por lo tanto, el símbolo se importa y exporta simultáneamente.

Por ejemplo, en Kernel32.dll en Windows XP, la exportación con el nombre "HeapAlloc" se reenvía a la cadena "NTDLL. RtlAllocateHeap." Esto permite que las aplicaciones usen el módulo específico de Windows XP Ntdll.dll sin contener realmente referencias de importación a él. La tabla de importación de la aplicación solo hace referencia a Kernel32.dll. Por lo tanto, la aplicación no es específica de Windows XP y se puede ejecutar en cualquier sistema Win32.

#### <a name="export-name-pointer-table"></a>Tabla de punteros de nombre de exportación

La tabla de punteros de nombre de exportación es una matriz de direcciones (RVA) en la tabla de nombres de exportación. Los punteros son de 32 bits cada uno y son relativos a la base de la imagen. Los punteros se ordenan léxicamente para permitir búsquedas binarias.

Un nombre de exportación solo se define si la tabla de puntero de nombre de exportación contiene un puntero a él.

#### <a name="export-ordinal-table"></a>Exportar tabla ordinal

La tabla ordinal de exportación es una matriz de índices no sesgados de 16 bits en la tabla de direcciones de exportación. Los ordinales se sesgan por el campo base ordinal de la tabla exportar directorio. En otras palabras, la base ordinal se debe restar de los ordinales para obtener índices verdaderos en la tabla de direcciones de exportación.

La tabla de punteros de nombre de exportación y la tabla ordinal de exportación forman dos matrices paralelas que se separan para permitir la alineación de campo natural. Estas dos tablas, en efecto, funcionan como una tabla, en la que la columna de puntero de nombre de exportación apunta a un nombre público (exportado) y la columna ordinal de exportación proporciona el ordinal correspondiente para ese nombre público. Un miembro de la tabla de puntero de nombre de exportación y un miembro de la tabla ordinal de exportación se asocian con la misma posición (índice) en sus matrices respectivas.

Por lo tanto, cuando se busca en la tabla de punteros de nombre de exportación y se encuentra una cadena coincidente en la posición i, el algoritmo para buscar la RVA del símbolo y el ordinal sesgado es:

```C++
i = Search_ExportNamePointerTable (name);
ordinal = ExportOrdinalTable [i];

rva = ExportAddressTable [ordinal];
biased_ordinal = ordinal + OrdinalBase;
```

Cuando se busca un ordinal de símbolo (sesgado), el algoritmo para encontrar la RVA y el nombre del símbolo es:

```C++
ordinal = biased_ordinal - OrdinalBase;
i = Search_ExportOrdinalTable (ordinal);

rva = ExportAddressTable [ordinal];
name = ExportNameTable [i];
```

#### <a name="export-name-table"></a>Exportar tabla de nombres

La tabla de nombres de exportación contiene los datos de cadena reales a los que apunta la tabla de punteros de nombre de exportación. Las cadenas de esta tabla son nombres públicos que otras imágenes pueden utilizar para importar los símbolos. Estos nombres de exportación públicos no son necesariamente los mismos que los nombres de símbolos privados que los símbolos tienen en su propio archivo de imagen y código fuente, aunque pueden ser.

Cada símbolo exportado tiene un valor ordinal, que es simplemente el índice de la tabla de direcciones de exportación. El uso de nombres de exportación, sin embargo, es opcional. Algunos, todos o ninguno de los símbolos exportados pueden tener nombres de exportación. En el caso de los símbolos exportados que tienen nombres de exportación, las entradas correspondientes de la tabla de punteros de nombre de exportación y la tabla de ordinales de exportación funcionan conjuntamente para asociar cada nombre con un ordinal.

La estructura de la tabla de nombres de exportación es una serie de cadenas ASCII terminadas en NULL de longitud variable.

### <a name="the-idata-section"></a>La sección. idata

Todos los archivos de imagen que importan símbolos, incluidos prácticamente todos los archivos ejecutables (EXE), tienen una sección. idata. A continuación se muestra un diseño de archivo típico para la información de importación:

-   Tabla de directorio

    Entrada de directorio null

-   Tabla de búsqueda de importación de DLL1

    Null

-   DLL2 importar tabla de búsqueda

    Null

-   DLL3 importar tabla de búsqueda

    Null

-   Hint-Name tabla

#### <a name="import-directory-table"></a>Importar tabla de directorio

La información de importación comienza con la tabla de importación de directorio, que describe el resto de la información de importación. La tabla importar directorio contiene información de la dirección que se usa para resolver las referencias de corrección en los puntos de entrada de una imagen DLL. La tabla de importación de directorio consta de una matriz de entradas de directorio de importación, una entrada para cada archivo DLL al que hace referencia la imagen. La última entrada de directorio está vacía (rellena con valores NULL), que indica el final de la tabla del directorio.

Cada entrada de directorio de importación tiene el siguiente formato:



| Offset         | Tamaño          | Campo                                                 | Descripción                                                                                                                                                                                 |
|----------------|---------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Importar tabla de búsqueda RVA (características) <br/> | RVA de la tabla de búsqueda de importación. Esta tabla contiene un nombre o un ordinal para cada importación. (El nombre "Characteristics" se usa en Winnt. h, pero ya no describe este campo). <br/> |
| 4 <br/>  | 4 <br/> | Marca de fecha y hora <br/>                           | Marca que se establece en cero hasta que se enlaza la imagen. Después de enlazar la imagen, este campo se establece en la marca de tiempo y datos del archivo DLL. <br/>                                          |
| 8 <br/>  | 4 <br/> | Cadena de reenviador <br/>                           | Índice de la primera referencia de reenviador. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Nombre RVA <br/>                                  | Dirección de una cadena ASCII que contiene el nombre del archivo DLL. Esta dirección es relativa a la base de la imagen. <br/>                                                                   |
| 16 <br/> | 4 <br/> | Importar la tabla de direcciones RVA (tabla thunk) <br/>    | RVA de la tabla de direcciones de importación. El contenido de esta tabla es idéntico al contenido de la tabla de búsqueda de importación hasta que la imagen esté enlazada. <br/>                              |



 

#### <a name="import-lookup-table"></a>Importar tabla de búsqueda

Una tabla de búsqueda de importación es una matriz de números de 32 bits para PE32 o una matriz de números de 64 bits para PE32 +. Cada entrada utiliza el formato de campo de bits que se describe en la tabla siguiente. En este formato, el bit 31 es el bit más significativo para PE32 y el bit 63 es el bit más significativo para PE32 +. La colección de estas entradas describe todas las importaciones de un archivo DLL determinado. La última entrada se establece en cero (NULL) para indicar el final de la tabla.



| Bits (s)            | Tamaño           | Campo de bit                       | Descripción                                                                                                                                                               |
|-------------------|----------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31/63 <br/> | 1 <br/>  | Marca de ordinal/nombre <br/>   | Si se establece este bit, importe por ordinal. De lo contrario, importe por nombre. El bit se enmascara como 0x80000000 para PE32, 0x8000000000000000 para PE32 +. <br/>                         |
| 15-0 <br/>  | 16 <br/> | Número ordinal <br/>      | Número ordinal de 16 bits. Este campo solo se usa si el campo de bits de la marca de ordinal/nombre es 1 (importación por ordinal). Los bits 30-15 o 62-15 deben ser 0. <br/>                  |
| 30-0 <br/>  | 31 <br/> | Sugerencia/nombre RVA de la tabla <br/> | RVA de 31 bits de una entrada de tabla de sugerencia/nombre. Este campo solo se usa si el campo de bits de la marca de ordinal/nombre es 0 (importar por nombre). Para PE32 + bits 62-31 debe ser cero. <br/> |



 

#### <a name="hintname-table"></a>Sugerencia/nombre (tabla)

Una tabla sugerencia/nombre es suficiente para toda la sección de importación. Cada entrada de la tabla sugerencia/nombre tiene el formato siguiente:



| Offset         | Tamaño                 | Campo            | Descripción                                                                                                                                                                                       |
|----------------|----------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>        | Diversas <br/> | Índice de la tabla de puntero de nombre de exportación. Primero se intenta una coincidencia con este valor. Si se produce un error, se realiza una búsqueda binaria en la tabla de punteros de nombre de exportación del archivo DLL. <br/>            |
| 2 <br/>  | variable <br/> | Nombre <br/> | Cadena ASCII que contiene el nombre que se va a importar. Esta es la cadena que debe coincidir con el nombre público del archivo DLL. Esta cadena distingue entre mayúsculas y minúsculas y termina con un byte nulo. <br/> |
| \* <br/> | 0 o 1 <br/>   | Pad <br/>  | Byte final de relleno de cero que aparece después del byte nulo final, si es necesario, para alinear la entrada siguiente en un límite uniforme. <br/>                                                        |



 

#### <a name="import-address-table"></a>Importar tabla de direcciones

La estructura y el contenido de la tabla de direcciones de importación son idénticos a los de la tabla de búsqueda de importación hasta que el archivo esté enlazado. Durante el enlace, las entradas de la tabla de direcciones de importación se sobrescriben con las direcciones de 32 bits (para PE32) o 64 bits (para PE32 +) de los símbolos que se van a importar. Estas direcciones son las direcciones de memoria reales de los símbolos, aunque técnicamente todavía se denominan "direcciones virtuales". El cargador normalmente procesa el enlace.

### <a name="the-pdata-section"></a>La sección. pdata

La sección. pdata contiene una matriz de entradas de la tabla de funciones que se usan para el control de excepciones. Apunta a la entrada de la tabla de excepciones en el directorio de datos de imagen. Las entradas deben estar ordenadas de acuerdo con las direcciones de la función (el primer campo de cada estructura) antes de que se emitan en la imagen final. La plataforma de destino determina cuál de las tres variantes de formato de entrada de tabla de funciones que se describen a continuación se usa.

En el caso de las imágenes de MIPS de 32 bits, las entradas de la tabla de funciones tienen el siguiente formato:



| Offset         | Tamaño          | Campo                          | Descripción                                                                    |
|----------------|---------------|--------------------------------|--------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Dirección inicial <br/>      | El VA de la función correspondiente. <br/>                              |
| 4 <br/>  | 4 <br/> | Dirección final <br/>        | El VA del final de la función. <br/>                                 |
| 8 <br/>  | 4 <br/> | Controlador de excepciones <br/>  | Puntero al controlador de excepciones que se va a ejecutar. <br/>               |
| 12 <br/> | 4 <br/> | Datos de controlador <br/>       | Puntero a la información adicional que se va a pasar al controlador. <br/> |
| 16 <br/> | 4 <br/> | Dirección final del prólogo <br/> | El VA del final del prólogo de la función. <br/>                        |



 

En el caso de las plataformas ARM, PowerPC, SH3 y SH4 Windows CE, las entradas de la tabla de funciones tienen el siguiente formato:



| Offset        | Tamaño                | Campo                       | Descripción                                                                                                               |
|---------------|---------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>       | Dirección inicial <br/>   | El VA de la función correspondiente. <br/>                                                                         |
| 4 <br/> | 8 bits <br/>  | Longitud del prólogo <br/>   | Número de instrucciones del prólogo de la función. <br/>                                                          |
| 4 <br/> | 22 bits <br/> | Longitud de la función <br/> | El número de instrucciones de la función. <br/>                                                                   |
| 4 <br/> | 1 bit <br/>   | Marca de 32 bits <br/>     | Si se establece, la función consta de instrucciones de 32 bits. Si está desactivada, la función consta de instrucciones de 16 bits. <br/> |
| 4 <br/> | 1 bit <br/>   | Marca de excepción <br/>  | Si se establece, existe un controlador de excepciones para la función. De lo contrario, no existe ningún controlador de excepciones. <br/>                 |



 

En las plataformas x64 e Itanium, las entradas de la tabla de funciones tienen el siguiente formato:



| Offset        | Tamaño          | Campo                          | Descripción                                        |
|---------------|---------------|--------------------------------|----------------------------------------------------|
| 0 <br/> | 4 <br/> | Dirección inicial <br/>      | RVA de la función correspondiente. <br/> |
| 4 <br/> | 4 <br/> | Dirección final <br/>        | RVA del final de la función. <br/>    |
| 8 <br/> | 4 <br/> | Información de desenredo <br/> | RVA de la información de desenredado. <br/>     |



 

### <a name="the-reloc-section-image-only"></a>La sección. reloc (solo imagen)

La tabla de reubicación básica contiene entradas para todas las reubicaciones base de la imagen. El campo tabla de reubicación base de los directorios de datos de encabezado opcionales proporciona el número de bytes en la tabla de reubicación base. Para obtener más información, consulte [directorios opcionales de datos de encabezado (solo imagen)](#optional-header-data-directories-image-only). La tabla de reubicación base se divide en bloques. Cada bloque representa las reubicaciones base de una página de 4K. Cada bloque debe comenzar en un límite de 32 bits.

No es necesario que el cargador Procese las reubicaciones base que resuelve el enlazador, a menos que no se pueda cargar la imagen de carga en la base de la imagen especificada en el encabezado PE.

#### <a name="base-relocation-block"></a>Bloque de reubicación base

Cada bloque de reubicación base se inicia con la siguiente estructura:



| Offset        | Tamaño          | Campo                  | Descripción                                                                                                                                              |
|---------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | RVA de página <br/>   | La base de la imagen más la RVA de la página se agrega a cada desplazamiento para crear el VA donde se debe aplicar la reubicación base. <br/>                         |
| 4 <br/> | 4 <br/> | Tamaño de bloque <br/> | El número total de bytes en el bloque de reubicación base, incluidos los campos de tamaño RVA y de tamaño de bloque, y los campos de tipo o desplazamiento siguientes. <br/> |



 

A continuación, el campo tamaño de bloque va seguido de cualquier número de entradas de campo de tipo o desplazamiento. Cada entrada es una palabra (2 bytes) y tiene la estructura siguiente:



| Offset        | Tamaño                | Campo              | Descripción                                                                                                                                                                                                            |
|---------------|---------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 bits <br/>  | Tipo <br/>   | Se almacena en los 4 bits superiores de la palabra, un valor que indica el tipo de reubicación base que se va a aplicar. Para obtener más información, vea [tipos de reubicación base](#base-relocation-types).<br/>                         |
| 0 <br/> | 12 bits <br/> | Offset <br/> | Se almacena en los 12 bits restantes de la palabra, un desplazamiento de la dirección de inicio que se especificó en el campo RVA de página para el bloque. Este desplazamiento especifica dónde se va a aplicar la reubicación base. <br/> |



 

Para aplicar una reubicación base, la diferencia se calcula entre la dirección base preferida y la base donde se carga realmente la imagen. Si la imagen se carga en su base preferida, la diferencia es cero y, por tanto, no es necesario aplicar las reubicaciones base.

#### <a name="base-relocation-types"></a>Tipos de reubicación base



| Constante                                       | Value          | Descripción                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ basado en \_ absoluto <br/>        | 0 <br/>  | Se omite la reubicación base. Este tipo se puede usar para rellenar un bloque. <br/>                                                                                                                                                                                                                                                 |
| IMAGEN \_ REL \_ basada en \_ alta <br/>            | 1 <br/>  | La reubicación base agrega los 16 bits superiores de la diferencia al campo de 16 bits en el desplazamiento. El campo de 16 bits representa el valor alto de una palabra de 32 bits. <br/>                                                                                                                                                               |
| IMAGE \_ REL \_ based \_ Low <br/>             | 2 <br/>  | La reubicación base agrega los 16 bits inferiores de la diferencia al campo de 16 bits en el desplazamiento. El campo de 16 bits representa la mitad inferior de una palabra de 32 bits. <br/>                                                                                                                                                                  |
| IMAGE \_ REL \_ based \_ HIGHLOW <br/>         | 3 <br/>  | La reubicación base aplica todos los 32 bits de la diferencia al campo de 32 bits en el desplazamiento. <br/>                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ based \_ HIGHADJ <br/>         | 4 <br/>  | La reubicación base agrega los 16 bits superiores de la diferencia al campo de 16 bits en el desplazamiento. El campo de 16 bits representa el valor alto de una palabra de 32 bits. Los 16 bits inferiores del valor de 32 bits se almacenan en la palabra de 16 bits que sigue a esta reubicación base. Esto significa que esta reubicación base ocupa dos ranuras. <br/> |
| IMAGE \_ REL \_ based \_ MIPS \_ JMPADDR <br/>   | 5 <br/>  | La interpretación de la reubicación depende del tipo de máquina. <br/> Cuando el tipo de máquina es MIPS, la reubicación base se aplica a una instrucción de salto de MIPS. <br/>                                                                                                                                                    |
| IMAGE \_ REL \_ based \_ ARM \_ MOV32 <br/>      | 5 <br/>  | Esta reubicación solo es significativa cuando el tipo de máquina es ARM o Thumb. La reubicación base aplica la dirección de 32 bits de un símbolo a través de un par de instrucciones MOVW/MOVT consecutivo. <br/>                                                                                                                                 |
| IMAGE \_ REL \_ based \_ RISCV \_ HIGH20 <br/>   | 5 <br/>  | Esta reubicación solo es significativa cuando el tipo de máquina es RISC-V. La reubicación base se aplica a los 20 bits superiores de una dirección absoluta de 32 bits. <br/>                                                                                                                                                                     |
|                                                | 6 <br/>  | Reserved, debe ser cero. <br/>                                                                                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ based \_ Thumb \_ MOV32 <br/>    | 7 <br/>  | Esta reubicación solo es significativa cuando el tipo de máquina es Thumb. La reubicación base aplica la dirección de 32 bits de un símbolo a un par de instrucciones MOVW/MOVT consecutivo. <br/>                                                                                                                                            |
| IMAGE \_ REL \_ based \_ RISCV \_ LOW12I <br/>   | 7 <br/>  | Esta reubicación solo es significativa cuando el tipo de máquina es RISC-V. La reubicación base se aplica a los 12 bits inferiores de una dirección absoluta de 32 bits formada en el formato de instrucción de tipo RISC-V I-Type. <br/>                                                                                                                           |
| IMAGE \_ REL \_ based \_ RISCV \_ LOW12S <br/>   | 8 <br/>  | Esta reubicación solo es significativa cuando el tipo de máquina es RISC-V. La reubicación base se aplica a los 12 bits inferiores de una dirección absoluta de 32 bits formada en el formato de instrucción de tipo RISC-V S-Type. <br/>                                                                                                                           |
| IMAGE \_ REL \_ based \_ MIPS \_ JMPADDR16 <br/> | 9 <br/>  | La reubicación solo es significativa cuando el tipo de máquina es MIPS. La reubicación base se aplica a una instrucción de salto de MIPS16. <br/>                                                                                                                                                                                            |
| IMAGE \_ REL \_ based \_ DIR64 <br/>           | 10 <br/> | La reubicación base aplica la diferencia al campo de 64 bits en el desplazamiento. <br/>                                                                                                                                                                                                                                             |



 

### <a name="the-tls-section"></a>La sección. TLS

La sección. TLS proporciona compatibilidad directa con PE y COFF para el almacenamiento local de subprocesos estáticos (TLS). TLS es una clase de almacenamiento especial que admite Windows en la que un objeto de datos no es una variable automática (stack), sino que es local para cada subproceso individual que ejecuta el código. Por lo tanto, cada subproceso puede mantener un valor diferente para una variable declarada mediante TLS.

Tenga en cuenta que se puede admitir cualquier cantidad de datos TLS mediante las llamadas API TlsAlloc, TlsFree, TlsSetValue y TlsGetValue. La implementación de PE o COFF es un enfoque alternativo para el uso de la API y tiene la ventaja de ser más sencilla desde el punto de vista del programador de lenguaje de alto nivel. Esta implementación permite definir e inicializar datos de TLS de forma similar a las variables estáticas ordinarias de un programa. Por ejemplo, en Visual C++, una variable TLS estática se puede definir de la siguiente manera, sin usar la API de Windows:

`__declspec (thread) int tlsFlag = 1;`

Para admitir esta construcción de programación, la sección PE y COFF. TLS especifica la siguiente información: datos de inicialización, rutinas de devolución de llamada para la inicialización y terminación por subproceso y el índice TLS, que se explican en la siguiente explicación.

> [!Note]
>
> Los objetos de datos TLS declarados de forma estática solo se pueden usar en archivos de imagen cargados estáticamente. De este hecho, no es confiable usar datos TLS estáticos en un archivo DLL a menos que sepa que el archivo DLL, o cualquier elemento vinculado estáticamente, no se cargará dinámicamente con la función de la API LoadLibrary.

 

El código ejecutable obtiene acceso a un objeto de datos TLS estático mediante los pasos siguientes:

1.  En el momento de la vinculación, el vinculador establece la dirección del campo de índice del directorio TLS. Este campo apunta a una ubicación en la que el programa espera recibir el índice de TLS.

    La biblioteca en tiempo de ejecución de Microsoft facilita este proceso definiendo una imagen de memoria del directorio TLS y asignándole el nombre especial " \_ \_ TLS \_ usado" (plataformas Intel x86) o " \_ TLS \_ usado" (otras plataformas). El enlazador busca esta imagen de memoria y usa los datos para crear el directorio TLS. Otros compiladores que admiten TLS y funcionan con el vinculador de Microsoft deben usar esta misma técnica.

2.  Cuando se crea un subproceso, el cargador comunica la dirección de la matriz TLS del subproceso colocando la dirección del bloque de entorno del subproceso (TEB) en el registro de FS. Un puntero a la matriz TLS está en el desplazamiento de 0x2C desde el principio de TEB. Este comportamiento es específico de Intel x86.

3.  El cargador asigna el valor del índice TLS en el lugar indicado por la dirección del campo de índice.

4.  El código ejecutable recupera el índice TLS y también la ubicación de la matriz TLS.

5.  El código usa el índice TLS y la ubicación de la matriz TLS (multiplicando el índice por 4 y usando como desplazamiento de la matriz) para obtener la dirección del área de datos TLS para el programa y el módulo determinados. Cada subproceso tiene su propio área de datos TLS, pero esto es transparente para el programa, lo que no necesita saber cómo se asignan los datos para los subprocesos individuales.

6.  Se tiene acceso a un objeto de datos de TLS individual como un desplazamiento fijo en el área de datos de TLS.

La matriz TLS es una matriz de direcciones que el sistema mantiene para cada subproceso. Cada dirección de esta matriz proporciona la ubicación de los datos TLS para un módulo determinado (EXE o DLL) dentro del programa. El índice de TLS indica qué miembro de la matriz se va a usar. El índice es un número (solo significativo en el sistema) que identifica el módulo.

#### <a name="the-tls-directory"></a>Directorio TLS

El directorio TLS tiene el siguiente formato:



| Desplazamiento (PE32/PE32 +) | Tamaño (PE32/PE32 +) | Campo                            | Descripción                                                                                                                                                                                                                                                                                                                                         |
|----------------------|--------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>        | 4/8 <br/>    | Inicio de datos sin procesar <br/>    | Dirección de inicio de la plantilla de TLS. La plantilla es un bloque de datos que se usa para inicializar los datos de TLS. El sistema copia todos estos datos cada vez que se crea un subproceso, por lo que no debe estar dañado. Tenga en cuenta que esta dirección no es una RVA; es una dirección para la que debe haber una reubicación base en la sección. reloc. <br/> |
| 4/8 <br/>      | 4/8 <br/>    | Fin de los datos sin procesar <br/>      | Dirección del último byte de TLS, excepto el relleno cero. Al igual que con el campo de inicio de datos sin procesar, es un VA, no una RVA. <br/>                                                                                                                                                                                                       |
| 8/16 <br/>     | 4/8 <br/>    | Dirección del índice <br/>     | Ubicación en la que se va a recibir el índice TLS, que el cargador asigna. Esta ubicación se encuentra en una sección de datos normales, por lo que se le puede dar un nombre simbólico al que pueda acceder el programa. <br/>                                                                                                                                                    |
| 12/24 <br/>    | 4/8 <br/>    | Dirección de devoluciones de llamada <br/> | Puntero a una matriz de funciones de devolución de llamada TLS. La matriz termina en null, por lo que si no se admite una función de devolución de llamada, este campo apunta a 4 bytes establecidos en cero. Para obtener información sobre el prototipo de estas funciones, vea [funciones de devolución de llamada TLS](#tls-callback-functions).<br/>                                                      |
| 16/32 <br/>    | 4 <br/>      | Tamaño de relleno cero <br/>    | El tamaño en bytes de la plantilla, más allá de los datos inicializados delimitados por los campos inicio de datos sin procesar y final de datos sin procesar. El tamaño total de la plantilla debe ser el mismo que el tamaño total de los datos TLS en el archivo de imagen. El relleno de cero es la cantidad de datos que van después de los datos no cero inicializados. <br/>                            |
| 20/36 <br/>    | 4 <br/>      | Características <br/>      | Los cuatro bits \[ 23:20 \] describen la información de alineación. Los valores posibles son los definidos como IMAGE \_ SCN \_ align \_ \* , que también se usan para describir la alineación de la sección en archivos objeto. Los otros 28 bits se reservan para uso futuro. <br/>                                                                                                       |



 

#### <a name="tls-callback-functions"></a>Funciones de devolución de llamada TLS

El programa puede proporcionar una o varias funciones de devolución de llamada de TLS para admitir la inicialización y finalización adicionales de los objetos de datos TLS. Un uso típico de este tipo de función de devolución de llamada sería llamar a constructores y destructores para los objetos.

Aunque normalmente no hay más de una función de devolución de llamada, una devolución de llamada se implementa como una matriz para que sea posible agregar funciones de devolución de llamada adicionales si se desea. Si hay más de una función de devolución de llamada, se llama a cada función en el orden en que su dirección aparece en la matriz. Un puntero nulo finaliza la matriz. Es perfectamente válido tener una lista vacía (no se admite la devolución de llamada), en cuyo caso la matriz de devolución de llamada tiene exactamente un miembro, un puntero nulo.

El prototipo de una función de devolución de llamada (al que apunta un puntero de tipo PIMAGE de \_ \_ devolución de llamada TLS) tiene los mismos parámetros que una función de punto de entrada de dll:


```C++
typedef VOID
(NTAPI *PIMAGE_TLS_CALLBACK) (
    PVOID DllHandle,
    DWORD Reason,
    PVOID Reserved
    );
```



El parámetro Reserved debe establecerse en cero. El parámetro Reason puede tomar los siguientes valores:



| Configuración                          | Value         | Descripción                                                                                          |
|----------------------------------|---------------|------------------------------------------------------------------------------------------------------|
| \_adjuntar proceso dll \_ <br/> | 1 <br/> | Se ha iniciado un nuevo proceso, incluido el primer subproceso. <br/>                                   |
| \_Asociación de subprocesos dll \_ <br/>  | 2 <br/> | Se ha creado un nuevo subproceso. Esta notificación se envía para todo excepto el primer subproceso. <br/>      |
| desasociación de \_ subprocesos dll \_ <br/>  | 3 <br/> | Un subproceso está a punto de terminar. Esta notificación se envía para todo excepto el primer subproceso. <br/> |
| desasociación de \_ procesos dll \_ <br/> | 0 <br/> | Un proceso está a punto de finalizar, incluido el subproceso original. <br/>                          |



 

### <a name="the-load-configuration-structure-image-only"></a>La estructura de configuración de carga (solo imagen)

La estructura de configuración de carga (directorio de configuración \_ \_ de carga de imagen \_ ) se usaba anteriormente en casos muy limitados en el propio sistema operativo Windows NT para describir varias características demasiado difíciles o demasiado grandes como para describir en el encabezado de archivo o el encabezado opcional de la imagen. Las versiones actuales de Microsoft linker y Windows XP y versiones posteriores de Windows usan una nueva versión de esta estructura para sistemas basados en x86 de 32 bits que incluyen tecnología SEH reservada. Esto proporciona una lista de controladores de excepciones estructurados seguros que el sistema operativo utiliza durante el envío de excepciones. Si la dirección del controlador reside en el intervalo de fin de una imagen y se marca como compatible con SEH (es decir, \_ la imagen DLLCHARACTERISTICS \_ no \_ SEH está clara en el campo DLLCHARACTERISTICS del encabezado opcional, como se describió anteriormente), el controlador debe estar en la lista de controladores seguros conocidos para esa imagen. De lo contrario, el sistema operativo finaliza la aplicación. Esto ayuda a evitar el ataque de "secuestro del controlador de excepciones x86" que se ha usado en el pasado para tomar el control del sistema operativo.

El enlazador de Microsoft proporciona automáticamente una estructura de configuración de carga predeterminada para incluir los datos de SEH reservados. Si el código de usuario ya proporciona una estructura de configuración de carga, debe incluir los nuevos campos de SEH reservados. De lo contrario, el enlazador no puede incluir los datos de SEH reservados y la imagen no está marcada como que contiene SEH reservado.

#### <a name="load-configuration-directory"></a>Cargar directorio de configuración

La entrada del directorio de datos para una estructura de configuración de carga de SEH prereservada debe especificar un tamaño determinado de la estructura de configuración de carga porque el cargador del sistema operativo siempre espera que sea un determinado valor. En ese sentido, el tamaño es en realidad solo una comprobación de la versión. Para ofrecer compatibilidad con Windows XP y versiones anteriores de Windows, el tamaño debe ser 64 para las imágenes x86.

#### <a name="load-configuration-layout"></a>Cargar diseño de configuración

La estructura de configuración de carga tiene el siguiente diseño para los archivos PE de 32 bits y de 64 bits:



| Offset              | Tamaño            | Campo                                      | Descripción                                                                                                                                                                                                                                                                                 |
|---------------------|-----------------|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 4 <br/>   | Características <br/>                | Marcas que indican los atributos del archivo, actualmente sin usar. <br/>                                                                                                                                                                                                                   |
| 4 <br/>       | 4 <br/>   | TimeDateStamp <br/>                  | Valor de marca de fecha y hora. El valor se representa en el número de segundos transcurridos desde la medianoche (00:00:00) del 1 de enero de 1970, hora universal coordinada, según el reloj del sistema. La marca de tiempo se puede imprimir mediante la función de tiempo de tiempo de ejecución de C (CRT). <br/> |
| 8 <br/>       | 2 <br/>   | MajorVersion <br/>                   | Número de versión principal. <br/>                                                                                                                                                                                                                                                           |
| 10 <br/>      | 2 <br/>   | MinorVersion <br/>                   | Número de versión secundaria. <br/>                                                                                                                                                                                                                                                           |
| 12 <br/>      | 4 <br/>   | GlobalFlagsClear <br/>               | Las marcas de cargador globales que se van a borrar para este proceso a medida que el cargador inicia el proceso. <br/>                                                                                                                                                                                             |
| 16 <br/>      | 4 <br/>   | GlobalFlagsSet <br/>                 | Las marcas de cargador globales que se van a establecer para este proceso a medida que el cargador inicia el proceso. <br/>                                                                                                                                                                                               |
| 20 <br/>      | 4 <br/>   | CriticalSectionDefaultTimeout <br/>  | Valor de tiempo de espera predeterminado que se va a usar para las secciones críticas de este proceso que se han abandonado. <br/>                                                                                                                                                                                       |
| 24 <br/>      | 4/8 <br/> | DeCommitFreeBlockThreshold <br/>     | Memoria que debe liberarse antes de que se devuelva al sistema, en bytes. <br/>                                                                                                                                                                                                        |
| 28/32 <br/>   | 4/8 <br/> | DeCommitTotalFreeThreshold <br/>     | Cantidad total de memoria libre, en bytes. <br/>                                                                                                                                                                                                                                          |
| 32/40 <br/>   | 4/8 <br/> | LockPrefixTable <br/>                | \[x86 solo \] el va de una lista de direcciones en las que se usa el prefijo de bloqueo para que se puedan reemplazar por NOP en máquinas con un solo procesador. <br/>                                                                                                                                    |
| 36/48 <br/>   | 4/8 <br/> | MaximumAllocationSize <br/>          | Tamaño máximo de asignación, en bytes. <br/>                                                                                                                                                                                                                                              |
| 40/56 <br/>   | 4/8 <br/> | VirtualMemoryThreshold <br/>         | Tamaño máximo de la memoria virtual, en bytes. <br/>                                                                                                                                                                                                                                          |
| 44/64 <br/>   | 4/8 <br/> | ProcessAffinityMask <br/>            | Establecer este campo en un valor distinto de cero es equivalente a llamar a SetProcessAffinityMask con este valor durante el inicio del proceso (solo. exe) <br/>                                                                                                                                       |
| 48/72 <br/>   | 4 <br/>   | ProcessHeapFlags <br/>               | Marcas de montón de proceso que corresponden al primer argumento de la función HeapCreate. Estas marcas se aplican al montón de procesos que se crea durante el inicio del proceso. <br/>                                                                                                              |
| 52/76 <br/>   | 2 <br/>   | CSDVersion <br/>                     | Identificador de la versión de Service Pack. <br/>                                                                                                                                                                                                                                            |
| 54/78 <br/>   | 2 <br/>   | Reservado <br/>                       | Debe ser cero. <br/>                                                                                                                                                                                                                                                                   |
| 56/80 <br/>   | 4/8 <br/> | EditList <br/>                       | Reservado para su uso por parte del sistema. <br/>                                                                                                                                                                                                                                                 |
| 60/88 <br/>   | 4/8 <br/> | SecurityCookie <br/>                 | Un puntero a una cookie que se usa en la implementación de Visual C++ o GS. <br/>                                                                                                                                                                                                          |
| 64/96 <br/>   | 4/8 <br/> | SEHandlerTable <br/>                 | \[x86 solo \] el va de la tabla ordenada de RVA de cada controlador de se válido y único en la imagen. <br/>                                                                                                                                                                                  |
| 68/104 <br/>  | 4/8 <br/> | SEHandlerCount <br/>                 | \[x86 solo \] el recuento de controladores únicos en la tabla. <br/>                                                                                                                                                                                                                         |
| 72/112 <br/>  | 4/8 <br/> | GuardCFCheckFunctionPointer <br/>    | VA donde se almacena el puntero check-function de la protección de flujo de control. <br/>                                                                                                                                                                                                               |
| 76/120 <br/>  | 4/8 <br/> | GuardCFDispatchFunctionPointer <br/> | VA donde se almacena el puntero Dispatch-function de la protección de flujo de control. <br/>                                                                                                                                                                                                            |
| 80/128 <br/>  | 4/8 <br/> | GuardCFFunctionTable <br/>           | El VA de la tabla ordenada de RVA de cada función de protección de flujo de control de la imagen. <br/>                                                                                                                                                                                            |
| 84/136 <br/>  | 4/8 <br/> | GuardCFFunctionCount <br/>           | Recuento de RVA únicas en la tabla anterior. <br/>                                                                                                                                                                                                                                    |
| 88/144 <br/>  | 4 <br/>   | GuardFlags <br/>                     | Marcas relacionadas con la protección de flujo de control. <br/>                                                                                                                                                                                                                                               |
| 92/148 <br/>  | 12 <br/>  | CodeIntegrity <br/>                  | Información de integridad de código. <br/>                                                                                                                                                                                                                                                     |
| 104/160 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryTable <br/> | El VA donde se almacena la tabla IAT de la dirección de protección de flujo de control. <br/>                                                                                                                                                                                                              |
| 108/168 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryCount <br/> | Recuento de RVA únicas en la tabla anterior. <br/>                                                                                                                                                                                                                                    |
| 112/176 <br/> | 4/8 <br/> | GuardLongJumpTargetTable <br/>       | El VA donde se almacena la tabla de destino de salto largo de la protección de flujo de control. <br/>                                                                                                                                                                                                               |
| 116/184 <br/> | 4/8 <br/> | GuardLongJumpTargetCount <br/>       | Recuento de RVA únicas en la tabla anterior. <br/>                                                                                                                                                                                                                                    |



 

El campo GuardFlags contiene una combinación de uno o varios de los siguientes marcadores y subcampos:

-   El módulo realiza comprobaciones de integridad de flujo de control mediante la compatibilidad proporcionada por el sistema.

    ` #define IMAGE_GUARD_CF_INSTRUMENTED  0x00000100`

-   El módulo realiza comprobaciones de integridad de escritura y flujo de control.

    ` #define IMAGE_GUARD_CFW_INSTRUMENTED  0x00000200`

-   El módulo contiene metadatos de destino de flujo de control válidos.

    `#define IMAGE_GUARD_CF_FUNCTION_TABLE_PRESENT  0x00000400`

-   El módulo no hace uso de la cookie de seguridad/GS.

    ` #define IMAGE_GUARD_SECURITY_COOKIE_UNUSED  0x00000800`

-   El módulo admite la carga retrasada de solo lectura.

    `#define IMAGE_GUARD_PROTECT_DELAYLOAD_IAT  0x00001000`

-   DELAYLOAD importar tabla en su propia sección. Didat (sin nada más) que se puede volver a proteger libremente.

    ` #define IMAGE_GUARD_DELAYLOAD_IAT_IN_ITS_OWN_SECTION  0x00002000`

-   El módulo contiene información de exportación suprimida. También se deduce que la tabla IAT tomada también está presente en la configuración de carga.

    `#define  IMAGE_GUARD_CF_EXPORT_SUPPRESSION_INFO_PRESENT  0x00004000`

-   El módulo permite la supresión de exportaciones.

    `#define IMAGE_GUARD_CF_ENABLE_EXPORT_SUPPRESSION  0x00008000`

-   El módulo contiene información de destino de longjmp.

    ` #define IMAGE_GUARD_CF_LONGJUMP_TABLE_PRESENT  0x00010000`

-   Máscara del subcampo que contiene el paso de las entradas de la tabla de funciones de protección de flujo de control (es decir, el recuento adicional de bytes por entrada de tabla).

    ` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_MASK  0xF0000000`

Además, el encabezado Windows SDK Winnt. h define esta macro para la cantidad de bits que se va a desplazar a la derecha el valor de GuardFlags para justificar a la derecha el intervalo de la tabla de funciones de protección de flujo de control:

` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_SHIFT  28`

### <a name="the-rsrc-section"></a>La sección. rsrc

Los recursos se indexan mediante una estructura de árbol ordenada de varios niveles binaria. El diseño general puede incorporar 2 \* \* 31 niveles. Por Convención, sin embargo, Windows usa tres niveles:

<dl> Tipo  
Nombre  
Idioma  
</dl>

Una serie de tablas del directorio de recursos relaciona todos los niveles de la siguiente manera: cada tabla de directorio va seguida de una serie de entradas de directorio que proporcionan el nombre o el identificador (ID.) para ese nivel (tipo, nombre o nivel de lenguaje) y una dirección de una descripción de datos u otra tabla de directorio. Si la dirección apunta a una descripción de datos, los datos son una hoja en el árbol. Si la dirección señala a otra tabla de directorio, la tabla muestra las entradas de directorio en el siguiente nivel inferior.

El tipo de hoja, el nombre y los identificadores de idioma se determinan mediante la ruta de acceso que se toma a través de las tablas del directorio para llegar a la hoja. La primera tabla determina el identificador de tipo, la segunda tabla (indicada por la entrada de directorio en la primera tabla) determina el identificador de nombre y la tercera tabla determina el identificador de idioma.

La estructura general de la sección. rsrc es:



| data                                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tablas de directorio de recursos (y entradas de directorio de recursos) <br/> | Una serie de tablas, una para cada grupo de nodos del árbol. Todos los nodos de nivel superior (tipo) se enumeran en la primera tabla. Las entradas de esta tabla apuntan a tablas de segundo nivel. Cada árbol de segundo nivel tiene el mismo identificador de tipo pero distintos identificadores de nombre. Los árboles de tercer nivel tienen los mismos identificadores de tipo y nombre pero distintos identificadores de idioma. <br/> Cada tabla individual va seguida inmediatamente de entradas de directorio, en las que cada entrada tiene un nombre o un identificador numérico y un puntero a una descripción de datos o una tabla en el siguiente nivel inferior. <br/> |
| Cadenas de directorio de recursos <br/>                                 | Cadenas Unicode con alineación de dos bytes, que sirven como datos de cadena a los que apuntan las entradas de directorio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Descripción de los datos de recursos <br/>                                  | Matriz de registros, a la que apuntan las tablas, que describen el tamaño y la ubicación reales de los datos de recursos. Estos registros son las hojas del árbol de descripción de recursos. <br/>                                                                                                                                                                                                                                                                                                                                                                |
| Datos de recursos <br/>                                              | Datos sin procesar de la sección de recursos. La información de tamaño y ubicación en el campo de descripciones de datos de recursos delimita las regiones individuales de los datos de recursos. <br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

#### <a name="resource-directory-table"></a>Tabla del directorio de recursos

Cada tabla del directorio de recursos tiene el formato siguiente. Esta estructura de datos debe considerarse como el encabezado de una tabla porque la tabla consta realmente de entradas de directorio (descritas en la sección 6.9.2, "entradas del directorio de recursos") y esta estructura:



| Offset         | Tamaño          | Campo                              | Descripción                                                                                                                                                                     |
|----------------|---------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Características <br/>        | Marcas de recursos. Este campo está reservado para un uso futuro. Actualmente está establecido en cero. <br/>                                                                                 |
| 4 <br/>  | 4 <br/> | Marca de fecha y hora <br/>        | La hora a la que el compilador de recursos creó los datos de recursos. <br/>                                                                                               |
| 8 <br/>  | 2 <br/> | Major Version <br/>          | Número de versión principal, establecido por el usuario. <br/>                                                                                                                          |
| 10 <br/> | 2 <br/> | Minor Version <br/>          | El número de versión secundaria, establecido por el usuario. <br/>                                                                                                                          |
| 12 <br/> | 2 <br/> | Número de entradas de nombre <br/> | Número de entradas de directorio inmediatamente después de la tabla que usan cadenas para identificar el tipo, el nombre o las entradas de idioma (dependiendo del nivel de la tabla). <br/> |
| 14 <br/> | 2 <br/> | Número de entradas de ID. <br/>   | Número de entradas de directorio inmediatamente después de las entradas de nombre que usan identificadores numéricos para las entradas de tipo, nombre o idioma. <br/>                                    |



 

#### <a name="resource-directory-entries"></a>Entradas de directorio de recursos

Las entradas de directorio componen las filas de una tabla. Cada entrada de directorio de recursos tiene el formato siguiente. Si la entrada es una entrada de nombre o identificador indicada por la tabla directorio de recursos, que indica cuántas entradas del nombre y del identificador se van a seguir (Recuerde que todas las entradas de nombre preceden a todas las entradas de ID. de la tabla). Todas las entradas de la tabla se ordenan en orden ascendente: las entradas de nombre por cadena que distingue entre mayúsculas y minúsculas y las entradas de identificador por valor numérico. Los desplazamientos son relativos a la dirección del recurso de entrada de directorio de la imagen \_ \_ \_ . Vea [emparejamiento en el archivo PE: un paseo por el formato de archivo portable ejecutable de Win32](/previous-versions/ms809762(v=msdn.10)#pe-file-resources) para obtener más información.



| Offset        | Tamaño          | Campo                           | Descripción                                                                                                          |
|---------------|---------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Desplazamiento de nombre <br/>         | Desplazamiento de una cadena que proporciona el tipo, el nombre o la entrada del identificador de idioma, dependiendo del nivel de tabla. <br/>     |
| 0 <br/> | 4 <br/> | Identificador entero <br/>          | Entero de 32 bits que identifica el tipo, el nombre o la entrada del identificador de idioma. <br/>                                   |
| 4 <br/> | 4 <br/> | Desplazamiento de entrada de datos <br/>   | Bit alto 0. Dirección de una entrada de datos de recursos (hoja). <br/>                                                   |
| 4 <br/> | 4 <br/> | Desplazamiento de subdirectorio <br/> | Bit alto 1. Los 31 bits inferiores son la dirección de otra tabla del directorio de recursos (el siguiente nivel hacia abajo). <br/> |



 

#### <a name="resource-directory-string"></a>Cadena de directorio de recursos

El área cadena de directorio de recursos consta de cadenas Unicode, que están alineadas por palabras. Estas cadenas se almacenan juntas después de la última entrada del directorio de recursos y antes de la primera entrada de datos de recursos. Esto minimiza el impacto de estas cadenas de longitud variable en la alineación de las entradas de directorio de tamaño fijo. Cada cadena de directorio de recursos tiene el siguiente formato:



| Offset        | Tamaño                 | Campo                      | Descripción                                                            |
|---------------|----------------------|----------------------------|------------------------------------------------------------------------|
| 0 <br/> | 2 <br/>        | Length <br/>         | Tamaño de la cadena, sin incluir el propio campo de longitud. <br/> |
| 2 <br/> | variable <br/> | Cadena Unicode <br/> | Datos de cadena Unicode de longitud variable, con alineación de palabras. <br/>     |



 

#### <a name="resource-data-entry"></a>Entrada de datos de recursos

Cada entrada de datos de recursos describe una unidad real de datos sin procesar en el área de datos de recursos. Una entrada de datos de recursos tiene el siguiente formato:



| Offset         | Tamaño          | Campo                            | Descripción                                                                                                                                           |
|----------------|---------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | RVA de datos <br/>             | Dirección de una unidad de datos de recursos en el área de datos de recursos. <br/>                                                                         |
| 4 <br/>  | 4 <br/> | Tamaño <br/>                 | Tamaño, en bytes, de los datos de recursos a los que apunta el campo RVA de datos. <br/>                                                        |
| 8 <br/>  | 4 <br/> | codepage <br/>             | La página de códigos que se usa para descodificar los valores de punto de código dentro de los datos de recursos. Normalmente, la página de códigos sería la página de códigos Unicode. <br/> |
| 12 <br/> | 4 <br/> | Reserved, debe ser 0. <br/> |                                                                                                                                                       |



 

### <a name="the-cormeta-section-object-only"></a>La sección. cormeta (solo objeto)

Los metadatos de CLR se almacenan en esta sección. Se utiliza para indicar que el archivo objeto contiene código administrado. El formato de los metadatos no está documentado, pero se puede pasar a las interfaces CLR para administrar los metadatos.

### <a name="the-sxdata-section"></a>La sección. sxdata

Los controladores de excepciones válidos de un objeto se enumeran en la sección **. sxdata** de ese objeto. La sección está marcada como IMAGE \_ SCN \_ lnk \_ info. Contiene el índice de símbolos de COFF de cada controlador válido, usando 4 bytes por índice.

Además, el compilador marca un objeto COFF como una SEH registrada emitiendo el símbolo absoluto " @feat.00 " con el LSB del campo de valor establecido en 1. Un objeto COFF sin controladores SEH registrados tendría el @feat.00 símbolo "", pero no **sxdata.**

## <a name="archive-library-file-format"></a>Formato de archivo de almacenamiento (biblioteca)

- [Firma de archivo de almacenamiento](#archive-file-signature)
- [Archivar encabezados de miembro](#archive-member-headers)
- [Primer miembro del vinculador](#first-linker-member)
- [Segundo miembro del vinculador](#second-linker-member)
- [Miembro Longnames](#longnames-member)

El formato de archivo COFF proporciona un mecanismo estándar para almacenar colecciones de archivos objeto. Estas colecciones se denominan comúnmente bibliotecas en la documentación de programación.

Los primeros 8 bytes de un archivo se componen de la firma del archivo. El resto del archivo se compone de una serie de miembros de archivo, como se indica a continuación:

-   Los miembros primero y segundo son "miembros del enlazador". Cada uno de estos miembros tiene su propio formato, tal y como se describe en la sección [tipo de nombre de importación](#import-name-type). Normalmente, un vinculador coloca información en estos miembros de archivo. Los miembros del enlazador contienen el directorio del archivo.

-   El tercer miembro es el miembro "longnames". Este miembro se compone de una serie de cadenas ASCII terminadas en null en las que cada cadena es el nombre de otro miembro de archivo.

-   El resto del archivo se compone de miembros estándar (archivo objeto). Cada uno de estos miembros incluye el contenido de un archivo objeto en su totalidad.

Un encabezado de miembro de archivo precede a cada miembro. En la lista siguiente se muestra la estructura general de un archivo:

-   Firma: "! &lt; Arch &gt; \\ n "
-   Encabezado

    <dl> primer miembro del vinculador  
    </dl>

-   Encabezado

    <dl> 2º miembro del vinculador  
    </dl>

-   Encabezado

    <dl> Miembro Longnames  
    </dl>

-   Encabezado

    <dl> Contenido del archivo OBJ 1  
    (Formato COFF)  
    </dl>

-   Encabezado

    <dl> Contenido del archivo OBJ 2  
    (Formato COFF)  
    </dl>

### <a name="archive-file-signature"></a>Firma de archivo de almacenamiento

La firma del archivo de almacenamiento identifica el tipo de archivo. Cualquier utilidad (por ejemplo, un vinculador) que toma como entrada un archivo de almacenamiento puede comprobar el tipo de archivo mediante la lectura de esta firma. La firma consta de los siguientes caracteres ASCII, en los que cada carácter siguiente se representa literalmente, excepto para el carácter de nueva línea ( \\ n):

`!<arch>\n`

### <a name="archive-member-headers"></a>Archivar encabezados de miembro

Cada miembro (enlazador, longnames u miembro de archivo de objeto) va precedido de un encabezado. Un encabezado de miembro de archivo tiene el formato siguiente, en el que cada campo es una cadena de texto ASCII que queda justificada y se rellena con espacios hasta el final del campo. No hay ningún carácter nulo de finalización en ninguno de estos campos.

Cada encabezado de miembro comienza en la primera dirección uniforme después del final del miembro de archivo anterior.



| Offset         | Tamaño           | Campo                     | Descripción                                                                                                                                                                                                 |
|----------------|----------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 16 <br/> | Nombre <br/>          | Nombre del miembro de archivo, con una barra diagonal (/) anexada para terminar el nombre. Si el primer carácter es una barra diagonal, el nombre tiene una interpretación especial, como se describe en la tabla siguiente. <br/> |
| 16 <br/> | 12 <br/> | Fecha <br/>          | Fecha y hora en que se creó el miembro de archivo: es la representación decimal ASCII del número de segundos transcurridos desde 1/1/1970 UCT. <br/>                                                    |
| 28 <br/> | 6 <br/>  | Id. de usuario <br/>       | Representación decimal ASCII del identificador de usuario. Este campo no contiene un valor significativo en las plataformas de Windows porque las herramientas de Microsoft emiten todos los espacios en blanco. <br/>                                    |
| 34 <br/> | 6 <br/>  | Identificador de grupo <br/>      | Representación decimal ASCII del identificador de grupo. Este campo no contiene un valor significativo en las plataformas de Windows porque las herramientas de Microsoft emiten todos los espacios en blanco. <br/>                                   |
| 40 <br/> | 8 <br/>  | Mode <br/>          | Representación octal ASCII del modo de archivo del miembro. Este es el \_ valor del modo St de la función en tiempo de ejecución de C \_ wstat. <br/>                                                                       |
| 48 <br/> | 10 <br/> | Tamaño <br/>          | Representación decimal ASCII del tamaño total del miembro de archivo, sin incluir el tamaño del encabezado. <br/>                                                                                  |
| 58 <br/> | 2 <br/>  | Fin del encabezado <br/> | Los dos bytes de la cadena de C "̃ \\ n" (0X60 0x0a). <br/>                                                                                                                                               |



 

El campo nombre tiene uno de los formatos que se muestran en la tabla siguiente. Como se mencionó anteriormente, cada una de estas cadenas se justifica y se rellena con espacios finales dentro de un campo de 16 bytes:



| Contenido del campo Nombre | Descripción                                                                                                                                                                                                                                                                                          |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name <br/>      | Nombre del miembro de archivo. <br/>                                                                                                                                                                                                                                                          |
| / <br/>          | El miembro de archivo es uno de los dos miembros del enlazador. Ambos miembros del enlazador tienen este nombre. <br/>                                                                                                                                                                                          |
| // <br/>         | El miembro Archive es el miembro longnames, que consta de una serie de cadenas ASCII terminadas en NULL. El miembro longnames es el tercer miembro de archivo y siempre debe estar presente incluso si el contenido está vacío. <br/>                                                                     |
| /n <br/>         | El nombre del miembro de archivo se encuentra en el desplazamiento n en el miembro longnames. El número n es la representación decimal del desplazamiento. Por ejemplo: "/26" indica que el nombre del miembro de archivo se encuentra 26 bytes más allá del principio del contenido del miembro longnames. <br/> |



 

### <a name="first-linker-member"></a>Primer miembro del vinculador

El nombre del primer miembro del enlazador es "/". El primer miembro del enlazador se incluye por motivos de compatibilidad con versiones anteriores. No lo usan los vinculadores actuales, pero su formato debe ser correcto. Este miembro del vinculador proporciona un directorio de nombres de símbolos, al igual que el segundo miembro del enlazador. Para cada símbolo, la información indica dónde encontrar el miembro de archivo que contiene el símbolo.

El primer miembro del vinculador tiene el formato siguiente. Esta información aparece después del encabezado:



| Offset         | Tamaño               | Campo                         | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|----------------|--------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Número de símbolos <br/> | Unsigned Long que contiene el número de símbolos indexados. Este número se almacena en formato Big-Endian. Cada miembro del archivo de objeto define normalmente uno o más símbolos externos. <br/>                                                                                                                                                                         |
| 4 <br/>  | 4 \* n <br/> | Desplazamientos <br/>           | Matriz de desplazamientos de archivo para archivar los encabezados de miembro, donde n es igual al número de campos de símbolos. Cada número de la matriz es una longitud sin signo que se almacena en formato Big-Endian. Para cada símbolo que se nombra en la tabla de cadenas, el elemento correspondiente de la matriz de desplazamientos proporciona la ubicación del miembro de archivo que contiene el símbolo. <br/> |
| \* <br/> | \* <br/>     | Tabla de cadenas <br/>      | Una serie de cadenas terminadas en null que denominan todos los símbolos del directorio. Cada cadena comienza inmediatamente después del carácter nulo de la cadena anterior. El número de cadenas debe ser igual al valor del campo número de símbolos. <br/>                                                                                                       |



 

Los elementos de la matriz de desplazamientos deben organizarse en orden ascendente. Este hecho implica que los símbolos de la tabla de cadenas se deben organizar según el orden de los miembros de archivo. Por ejemplo, todos los símbolos del primer miembro del archivo de objeto deberían aparecer antes que los símbolos del segundo archivo objeto.

### <a name="second-linker-member"></a>Segundo miembro del vinculador

El segundo miembro del vinculador tiene el nombre "/" como hace el primer miembro del enlazador. Aunque ambos miembros del enlazador proporcionan un directorio de símbolos y miembros de archivo que los contienen, el segundo miembro del enlazador se usa en preferencia al primero por todos los vinculadores actuales. El segundo miembro del vinculador incluye nombres de símbolos en orden léxico, lo que permite una búsqueda más rápida por nombre.

El segundo miembro tiene el formato siguiente. Esta información aparece después del encabezado:



| Offset         | Tamaño               | Campo                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|--------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Número de miembros <br/> | Un valor de tipo Long sin signo que contiene el número de miembros de archivo. <br/>                                                                                                                                                                                                                                                                                                                                |
| 4 <br/>  | 4 \* m <br/> | Desplazamientos <br/>           | Matriz de desplazamientos de archivo para archivar los encabezados de miembro, organizados en orden ascendente. Cada desplazamiento es una longitud sin signo. El número m es igual al valor del campo número de miembros. <br/>                                                                                                                                                                                                        |
| \* <br/> | 4 <br/>      | Número de símbolos <br/> | Un valor de tipo Long sin signo que contiene el número de símbolos indizados. Cada miembro del archivo de objeto define normalmente uno o más símbolos externos. <br/>                                                                                                                                                                                                                                                        |
| \* <br/> | 2 \* n <br/> | Índices <br/>           | Matriz de índices basados en 1 (short sin signo) que asignan nombres de símbolos a desplazamientos de miembros de archivo. El número n es igual al número de campo de símbolos. Para cada símbolo que se nombra en la tabla de cadenas, el elemento correspondiente de la matriz de índices proporciona un índice en la matriz de desplazamientos. La matriz offsets, a su vez, proporciona la ubicación del miembro de archivo que contiene el símbolo. <br/> |
| \* <br/> | \* <br/>     | Tabla de cadenas <br/>      | Una serie de cadenas terminadas en null que denominan todos los símbolos del directorio. Cada cadena comienza inmediatamente después del byte nulo de la cadena anterior. El número de cadenas debe ser igual al valor del campo número de símbolos. En esta tabla se enumeran todos los nombres de símbolos en orden léxico ascendente. <br/>                                                                             |



 

### <a name="longnames-member"></a>Miembro Longnames

El nombre del miembro longnames es "//". El miembro longnames es una serie de cadenas de nombres de miembros de archivo. Aquí solo aparece un nombre cuando no hay espacio suficiente en el campo Nombre (16 bytes). El miembro longnames es opcional. Puede estar vacío solo con un encabezado o puede estar completamente ausente sin un encabezado.

Las cadenas terminan en NULL. Cada cadena comienza inmediatamente después del byte nulo de la cadena anterior.

## <a name="import-library-format"></a>Formato de la biblioteca de importación

- [Importar encabezado](#import-header)
- [Tipo de importación](#import-type)

Las bibliotecas de importación tradicionales, es decir, las bibliotecas que describen las exportaciones de una imagen para su uso en otra, normalmente siguen el diseño descrito en la sección 7, [formato de archivo de almacenamiento (biblioteca)](#archive-library-file-format). La principal diferencia es que los miembros de la biblioteca de importación contienen archivos pseudo-Object en lugar de los reales, en los que cada miembro incluye las contribuciones de la sección necesarias para compilar las tablas de importación que se describen en la sección 6,4, [la sección. idata](#the-idata-section) , que el vinculador genera este archivo al compilar la aplicación de exportación.

La sección sobre las contribuciones de una importación se puede deducir a partir de un pequeño conjunto de información. El enlazador puede generar la información completa y detallada en la biblioteca de importación para cada miembro en el momento de la creación de la biblioteca, o escribir solo la información canónica en la biblioteca y permitir que la aplicación que la usa posteriormente genere los datos necesarios sobre la marcha.

En una biblioteca de importación con el formato largo, un solo miembro contiene la siguiente información:

<dl> Encabezado de miembro de archivo  
Encabezado de archivo  
Encabezados de sección  
Datos correspondientes a cada uno de los encabezados de sección  
Tabla de símbolos COFF  
Cadenas  
  
</dl>

En cambio, una biblioteca de importación corta se escribe de la siguiente manera:

<dl> Encabezado de miembro de archivo  
Importar encabezado  
Cadena de nombre de importación terminada en null  
Cadena de nombre de DLL terminada en null  
</dl>

Esta es la información suficiente para reconstruir con precisión todo el contenido del miembro en el momento de su uso.

### <a name="import-header"></a>Importar encabezado

El encabezado Import contiene los siguientes campos y desplazamientos:



| Offset         | Tamaño                | Campo                       | Descripción                                                                                                                  |
|----------------|---------------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>       | Sig1 <br/>            | Debe ser la \_ máquina del archivo de imagen \_ \_ desconocida. Para obtener más información, consulte [tipos de máquina](#machine-types). <br/>                |
| 2 <br/>  | 2 <br/>       | Sig2 <br/>            | Debe ser 0xFFFF. <br/>                                                                                                  |
| 4 <br/>  | 2 <br/>       | Versión <br/>         | Versión de la estructura. <br/>                                                                                           |
| 6 <br/>  | 2 <br/>       | Máquina <br/>         | Número que identifica el tipo de equipo de destino. Para obtener más información, consulte [tipos de máquina](#machine-types).<br/> |
| 8 <br/>  | 4 <br/>       | Time-Date marca <br/> | Fecha y hora en que se creó el archivo. <br/>                                                                     |
| 12 <br/> | 4 <br/>       | Tamaño de los datos <br/>    | Tamaño de las cadenas que siguen al encabezado. <br/>                                                                  |
| 16 <br/> | 2 <br/>       | Ordinal/sugerencia <br/>    | El ordinal o la sugerencia para la importación, determinado por el valor en el campo tipo de nombre. <br/>                   |
| 18 <br/> | 2 bits <br/>  | Tipo <br/>            | Tipo de importación. Para obtener información sobre los valores y las descripciones, vea [tipo de importación](#import-type).<br/>                           |
|                | 3 bits <br/>  | Tipo de nombre <br/>       | Tipo de nombre de importación. Para obtener más información, consulte [Import Name Type](#import-name-type). <br/>                           |
|                | 11 bits <br/> | Reservado <br/>        | Reserved, debe ser 0. <br/>                                                                                             |



 

Esta estructura va seguida de dos cadenas terminadas en null que describen el nombre del símbolo importado y el archivo DLL del que procede.

### <a name="import-type"></a>Tipo de importación

Los siguientes valores se definen para el campo Type en el encabezado Import:

| Constante                  | Value         | Descripción                                      |
|---------------------------|---------------|--------------------------------------------------|
| IMPORTAR \_ código <br/>  | 0 <br/> | Código ejecutable. <br/>                     |
| IMPORTAR \_ datos <br/>  | 1 <br/> | Datos <br/>                                |
| IMPORTAR \_ const <br/> | 2 <br/> | Se especifica como CONST en el archivo. def. <br/> |

Estos valores se usan para determinar qué contribuciones de la sección debe generar la herramienta que utiliza la biblioteca si debe tener acceso a esos datos.

### <a name="import-name-type"></a>Tipo de nombre de importación

El nombre del símbolo de importación terminado en NULL sigue inmediatamente a su encabezado de importación asociado. Los siguientes valores se definen para el campo tipo de nombre en el encabezado de importación. Indican cómo se va a usar el nombre para generar los símbolos correctos que representan la importación:

| Constante | Value | Descripción |
| - | - | - |
| ORDINAL de importación \_ | 0 | La importación es por ordinal. Esto indica que el valor del campo ordinal/Hint del encabezado Import es el ordinal de la importación. Si no se especifica esta constante, el campo ordinal/Hint siempre debe interpretarse como la sugerencia de la importación. |
| nombre de la importación \_ | 1 | El nombre de la importación es idéntico al nombre del símbolo público. |
| nombre de importación \_ \_ noprefix | 2 | El nombre de la importación es el nombre del símbolo público, pero se omitirá el interlineado?, @ o opcionalmente \_ . |
| desdecoración de nombre de importación \_ \_ | 3 | El nombre de la importación es el nombre del símbolo público, pero se omitirá el interlineado?, @ o opcionalmente \_ , y se truncará en el primero @ . |

## <a name="appendix-a-calculating-authenticode-pe-image-hash"></a>Apéndice A: calcular el hash de imagen de Authenticode PE

- [¿Qué es un hash de imagen de PE de Authenticode?](#what-is-an-authenticode-pe-image-hash)
- [¿Qué se trata en un hash de imagen de PE de Authenticode?](#what-is-covered-in-an-authenticode-pe-image-hash)

Se espera que se usen varios certificados de atributo para comprobar la integridad de las imágenes. Sin embargo, el más común es la firma Authenticode. Se puede usar una firma Authenticode para comprobar que las secciones pertinentes de un archivo de imagen PE no se han modificado de ninguna manera desde el formulario original del archivo. Para realizar esta tarea, las firmas de Authenticode contienen algo llamado hash de imagen PE

### <a name="what-is-an-authenticode-pe-image-hash"></a>¿Qué es un hash de imagen de PE de Authenticode?

El hash de la imagen de PE de Authenticode o el hash de archivo para abreviar es similar a una suma de comprobación de archivo en cuanto a que genera un pequeño valor relacionado con la integridad de un archivo. Una suma de comprobación se genera mediante un algoritmo simple y se utiliza principalmente para detectar errores de memoria. Es decir, se usa para detectar si un bloque de memoria del disco ha desaparecido y los valores almacenados allí están dañados. Un hash de archivo es similar a una suma de comprobación en que también detecta daños en los archivos. Sin embargo, a diferencia de la mayoría de los algoritmos de suma de comprobación, es muy difícil modificar un archivo para que tenga el mismo hash de archivo que su formulario original (sin modificar). Es decir, una suma de comprobación está pensada para detectar errores de memoria simples que conducen a daños, pero se puede usar un hash de archivo para detectar modificaciones intencionadas e incluso sutiles en un archivo, como los introducidos por virus, hackers o programas troyanos.

En una firma Authenticode, el hash de archivo se firma digitalmente con una clave privada conocida solo para el firmante del archivo. Un consumidor de software puede comprobar la integridad del archivo calculando el valor hash del archivo y comparándolo con el valor de hash firmado incluido en la firma digital de Authenticode. Si los hashes de archivo no coinciden, se ha modificado parte del archivo incluido en el hash de la imagen de PE.

### <a name="what-is-covered-in-an-authenticode-pe-image-hash"></a>¿Qué se trata en un hash de imagen de PE de Authenticode?

No es posible o deseable incluir todos los datos del archivo de imagen en el cálculo del hash de la imagen PE. A veces, simplemente presenta características no deseadas (por ejemplo, la información de depuración no se puede quitar de los archivos liberados públicamente). a veces es imposible. Por ejemplo, no es posible incluir toda la información de un archivo de imagen en una firma Authenticode y, a continuación, insertar la firma Authenticode que contiene ese hash de imagen de PE en la imagen de PE y, más tarde, poder generar un hash de imagen PE idéntico al incluir todos los datos de archivo de imagen en el cálculo de nuevo, ya que el archivo contiene ahora la firma Authenticode

#### <a name="process-for-generating-the-authenticode-pe-image-hash"></a>Proceso para generar el hash de la imagen de PE de Authenticode

En esta sección se describe cómo se calcula un hash de imagen de PE y qué partes de la imagen de PE se pueden modificar sin invalidar la firma Authenticode.

> [!NOTE]
> El hash de imagen PE para un archivo específico se puede incluir en un archivo de catálogo independiente sin incluir un certificado de atributo en el archivo hash. Esto es pertinente, ya que es posible invalidar el hash de imagen de PE en un archivo de catálogo firmado con Authenticode mediante la modificación de una imagen de PE que realmente no contiene una firma Authenticode.

Se aplica un algoritmo hash a todos los datos de las secciones de la imagen de PE que se especifican en la tabla de la sección, excepto los siguientes intervalos de exclusión:

- **El campo de suma de comprobación de archivo de los campos específicos de Windows del encabezado opcional.** Esta suma de comprobación incluye todo el archivo (incluidos los certificados de atributo del archivo). En todas las probabilidades, la suma de comprobación será diferente del valor original después de insertar la firma Authenticode.

- **Información relacionada con los certificados de atributo**. Las áreas de la imagen de PE que están relacionadas con la firma Authenticode no se incluyen en el cálculo del hash de la imagen de PE porque las firmas de Authenticode se pueden agregar o quitar de una imagen sin que ello afecte a la integridad global de la imagen. Esto no es un problema, porque hay escenarios de usuario que dependen de volver a firmar imágenes de PE o agregar una marca de tiempo. Authenticode excluye la siguiente información del cálculo de hash:

  - El campo de la tabla de certificados de los directorios de datos de encabezado opcionales.

  - La tabla de certificados y los certificados correspondientes a los que apunta el campo de la tabla de certificados que se indica a continuación.

  Para calcular el hash de la imagen de PE, Authenticode ordena las secciones que se especifican en la tabla de la sección por intervalo de direcciones y, después, aplica un algoritmo hash a la secuencia de bytes resultante, pasando por los intervalos de exclusión.

- **Información más allá del final de la última sección.** El área anterior a la última sección (definida por el desplazamiento superior) no tiene un algoritmo hash. Normalmente, esta área contiene información de depuración. Por lo general, la información de depuración se puede considerar consultiva a los depuradores; no afecta a la integridad real del programa ejecutable. Es muy literalmente posible quitar la información de depuración de una imagen una vez entregado un producto y no afectar a la funcionalidad del programa. De hecho, esto se hace a veces como una medida de ahorro de disco. Merece la pena tener en cuenta que la información de depuración contenida en las secciones especificadas de la imagen PE no se puede quitar sin la firma Authenticode.

Puede usar las herramientas Makecert y SignTool proporcionadas en el SDK de la plataforma Windows para experimentar con la creación y comprobación de firmas Authenticode. Para obtener más información, vea referencia a continuación.

## <a name="references"></a>Referencias

[Descargas y herramientas para Windows (incluye el Windows SDK)](https://developer.microsoft.com/windows/downloads)

[Creación, visualización y administración de certificados](/windows/desktop/SecCrypto/creating-viewing-and-managing-certificates)

[Tutorial de firma de código en modo kernel (. doc)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/KMCS_Walkthrough.doc)

[SignTool](/windows/desktop/SecCrypto/signtool)

[Formato de firma ejecutable portable de Windows Authenticode (. docx)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx)

[Funciones ImageHlp](/windows/desktop/Debug/imagehlp-functions)