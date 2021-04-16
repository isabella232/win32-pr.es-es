---
description: Todos los sistemas de archivos compatibles con Windows usan el concepto de archivos y directorios para tener acceso a los datos almacenados en un disco o un dispositivo.
ms.assetid: 121cd5b2-e6fd-4eb4-99b4-b652d27b53e8
title: Nomenclatura de archivos, rutas de acceso y espacios de nombres
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: 59f626c931a61255cef8be9ede594cb97924cfb0
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/04/2021
ms.locfileid: "105686262"
---
# <a name="naming-files-paths-and-namespaces"></a>Nomenclatura de archivos, rutas de acceso y espacios de nombres

Todos los sistemas de archivos compatibles con Windows usan el concepto de archivos y directorios para tener acceso a los datos almacenados en un disco o un dispositivo. Los desarrolladores de Windows que trabajan con las API de Windows para la e/s de archivos y dispositivos deben comprender las distintas reglas, convenciones y limitaciones de los nombres de archivos y directorios.

Se puede tener acceso a los datos desde discos, dispositivos y recursos compartidos de red mediante las API de e/s de archivos. Los archivos y directorios, junto con los espacios de nombres, forman parte del concepto de una ruta de acceso, que es una representación de cadena de dónde obtener los datos, independientemente de si se trata de un disco o un dispositivo o una conexión de red para una operación específica.

Algunos sistemas de archivos, como NTFS, admiten archivos y directorios vinculados, que también siguen las reglas y convenciones de nomenclatura de archivos, de la misma forma que los archivos o directorios normales. Para obtener más información, vea [vínculos físicos y uniones](hard-links-and-junctions.md) y [operaciones de archivo y puntos de reanálisis](reparse-points-and-file-operations.md).

Para obtener más información, vea las siguientes subsecciones:

-   [Nombres de archivos y directorios](#file-and-directory-names)
    -   [Convenciones de nomenclatura](#naming-conventions)
    -   [Nombres cortos y largos](#short-vs-long-names)
-   [Paths](#fully-qualified-vs-relative-paths)
    -   [Rutas de acceso completas y relativas](#fully-qualified-vs-relative-paths)
    -   [Límite máximo de longitud de ruta de acceso](#maximum-path-length-limitation)
-   [Espacios de nombres](#win32-file-namespaces)
    -   [Espacios de nombres de archivos Win32](#win32-file-namespaces)
    -   [Espacios de nombres de dispositivos Win32](#win32-device-namespaces)
    -   [Espacios de nombres NT](#nt-namespaces)
-   [Temas relacionados](#related-topics)


Para obtener información sobre cómo configurar Windows 10 para que admita rutas de acceso de archivo largas, vea [límite de longitud máxima de ruta de acceso](./maximum-file-path-limitation.md).


## <a name="file-and-directory-names"></a>Nombres de archivos y directorios

Todos los sistemas de archivos siguen las mismas convenciones de nomenclatura generales para un archivo individual: un nombre de archivo base y una extensión opcional, separados por un punto. Sin embargo, cada sistema de archivos, como NTFS, CDFS, exFAT, UDF, FAT y FAT32, puede tener reglas específicas y diferentes sobre la formación de componentes individuales en la ruta de acceso a un directorio o archivo. Tenga en cuenta que un *directorio* es simplemente un archivo con un atributo especial que lo designa como un directorio, pero, de lo contrario, debe seguir las mismas reglas de nomenclatura que un archivo normal. Dado que el término *directorio* simplemente hace referencia a un tipo especial de archivo en lo que se refiere al sistema de archivos, algunos materiales de referencia utilizarán el *archivo* de términos generales para incluir tanto los conceptos de los directorios como los archivos de datos como tales. Por este motivo, a menos que se especifique lo contrario, las reglas de uso o de nomenclatura o los ejemplos de un archivo también se deben aplicar a un directorio. El término *ruta de acceso* hace referencia a uno o varios directorios, barras diagonales inversas y, posiblemente, un nombre de volumen. Para obtener más información, vea la sección [rutas](#fully-qualified-vs-relative-paths) de acceso.

Las limitaciones del recuento de caracteres también pueden ser diferentes y pueden variar en función del formato del sistema de archivos y del prefijo del nombre de ruta de acceso utilizado. Esto es más complicado gracias a la compatibilidad con los mecanismos de compatibilidad con versiones anteriores. Por ejemplo, el sistema de archivos FAT de MS-DOS anterior admite un máximo de 8 caracteres para el nombre de archivo base y tres caracteres para la extensión, para un total de 12 caracteres, incluido el separador de puntos. Esto se conoce normalmente como un *nombre de archivo 8,3*. Los sistemas de archivos FAT y NTFS de Windows no se limitan a los nombres de archivo 8,3, porque tienen *compatibilidad con nombres de archivo largos*, pero siguen admitiendo la versión 8,3 de nombres de archivo largos.

### <a name="naming-conventions"></a>Convenciones de nomenclatura

Las siguientes reglas fundamentales permiten a las aplicaciones crear y procesar nombres válidos para archivos y directorios, independientemente del sistema de archivos:

-   Use un punto para separar el nombre de archivo base de la extensión en el nombre de un directorio o archivo.
-   Use una barra diagonal inversa ( \\ ) para separar los *componentes* de una *ruta de acceso*. La barra diagonal inversa divide el nombre de archivo de la ruta de acceso y un nombre de directorio de otro nombre de directorio en una ruta de acceso. No se puede usar una barra diagonal inversa en el nombre del archivo o directorio real porque es un carácter reservado que separa los nombres en componentes.
-   Use una barra diagonal inversa según sea necesario como parte de [los nombres de volumen](naming-a-volume.md), por ejemplo, "c: \\ " en "c: \\ archivo de ruta de acceso \\ " o " \\ \\ \\ recurso compartido de servidor" en "archivo de ruta de acceso del \\ \\ \\ recurso compartido del servidor \\ \\ " para los nombres de la Convención de nomenclatura universal (UNC). Para obtener más información acerca de los nombres UNC, consulte la sección [límite máximo de longitud de ruta de acceso](#maximum-path-length-limitation) .
-   No asuma la distinción de mayúsculas y minúsculas. Por ejemplo, considere los nombres OSCAR, Oscar y Oscar para que sean los mismos, aunque algunos sistemas de archivos (por ejemplo, un sistema de archivos compatible con POSIX) pueden considerarlos como diferentes. Tenga en cuenta que NTFS admite la semántica de POSIX para la distinción de mayúsculas y minúsculas, pero este no es el comportamiento predeterminado. Para obtener más información, vea [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).
-   Los designadores de volumen (Letras de unidad) no distinguen mayúsculas de minúsculas. Por ejemplo, "D: \\ " y "d: \\ " hacen referencia al mismo volumen.
-   Use cualquier carácter de la página de códigos actual para un nombre, incluidos los caracteres Unicode y los caracteres del juego de caracteres extendido (128 – 255), excepto los siguientes:

    -   Los siguientes caracteres reservados:

        -   < (menor que)
        -   \> (mayor que)
        -   : (dos puntos)
        -   " (comilla doble)
        -   / (barra diagonal)
        -   \\ barra diagonal inversa
        -   \| (barra vertical o canalización)
        -   ? (signo de interrogación)
        -   \* aparezca

    -   Valor entero cero, que a veces se conoce como carácter *NUL* ASCII.
    -   Caracteres cuyas representaciones enteras están en el intervalo comprendido entre 1 y 31, excepto los flujos de datos alternativos en los que se permiten estos caracteres. Para obtener más información sobre las secuencias de archivos, consulte [secuencias de archivo](file-streams.md).
    -   Cualquier otro carácter que no permita el sistema de archivos de destino.

-   Use un punto como *componente* de directorio en una ruta de acceso para representar el directorio actual, por ejemplo ". \\temp.txt ". Para obtener más información, vea [rutas](#fully-qualified-vs-relative-paths)de acceso.
-   Use dos puntos consecutivos (..) como *componente* de directorio en una ruta de acceso para representar el elemento primario del directorio actual, por ejemplo ".. \\temp.txt ". Para obtener más información, vea [rutas](#fully-qualified-vs-relative-paths)de acceso.
-   No use los siguientes nombres reservados para el nombre de un archivo:

    Con, PRN, AUX, NUL, COM1, COM2, COM3, COM4, COM5, COM6, COM7, COM8, COM9, LPT1, LPT2, LPT3, LPT4, LPT5, LPT6, LPT7, LPT8 y LPT9. Evite también estos nombres seguidos inmediatamente de una extensión; por ejemplo, no se recomienda NUL.txt. Para más información, consulte [Espacios de nombres](#win32-file-namespaces).

-   No termine un nombre de archivo o directorio con un espacio o un punto. Aunque el sistema de archivos subyacente puede admitir estos nombres, el shell de Windows y la interfaz de usuario no. Sin embargo, es aceptable especificar un punto como el primer carácter de un nombre. Por ejemplo, ". Temp".

### <a name="short-vs-long-names"></a>Nombres cortos y largos

Se considera que un nombre de archivo largo es cualquier nombre de archivo que supere la Convención de nomenclatura de estilo MS-DOS (también denominada *8,3*). Cuando se crea un nombre de archivo largo, Windows también puede crear una forma abreviada de 8,3 del nombre, denominado *alias 8,3* o nombre corto y almacenarlo también en el disco. Este alias de 8,3 se puede deshabilitar por motivos de rendimiento o para un volumen especificado, en función del sistema de archivos en particular.

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** no se pueden deshabilitar los alias de 8,3 para los volúmenes especificados hasta Windows 7 y windows Server 2008 R2.

En muchos sistemas de archivos, un nombre de archivo contendrá una tilde (~) dentro de cada componente del nombre que sea demasiado largo para cumplir con las reglas de nomenclatura de 8,3.

> [!Note]  
> No todos los sistemas de archivos siguen la Convención de sustitución de tildes y los sistemas se pueden configurar para deshabilitar la generación de alias 8,3 aunque normalmente lo admitan. Por lo tanto, no suponga que el alias 8,3 ya existe en el disco.

 

Para solicitar los nombres de archivo 8,3, los nombres de archivo largos o la ruta de acceso completa de un archivo del sistema, tenga en cuenta las siguientes opciones:

-   Para obtener la forma 8,3 de un nombre de archivo largo, utilice la función [**GetShortPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getshortpathnamew) .
-   Para obtener la versión de nombre de archivo largo de un nombre corto, utilice la función [**GetLongPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getlongpathnamea) .
-   Para obtener la ruta de acceso completa a un archivo, use la función [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) .

En los sistemas de archivos más recientes, como NTFS, exFAT, UDF y FAT32, Windows almacena los nombres de archivo largos en el disco en Unicode, lo que significa que siempre se conserva el nombre de archivo largo original. Esto es así incluso si un nombre de archivo largo contiene caracteres extendidos, independientemente de la página de códigos que esté activa durante una operación de lectura o escritura de disco.

Los archivos que usan nombres de archivo largos se pueden copiar entre las particiones del sistema de archivos NTFS y las particiones del sistema de archivos FAT de Windows sin perder información de nombre de archivo. Esto puede no ser cierto para los sistemas de archivos FAT anteriores de MS-DOS y algunos tipos de sistema de archivos CDFS (CD-ROM), según el nombre de archivo real. En este caso, el nombre corto de archivo se sustituye si es posible.

## <a name="paths"></a>Rutas de acceso

La *ruta de acceso* a un archivo especificado se compone de uno o más *componentes*, separados por un carácter especial (una barra diagonal inversa), donde cada componente normalmente es un nombre de directorio o de archivo, pero con algunas excepciones importantes que se describen a continuación. A menudo es fundamental que la interpretación del sistema de una ruta de acceso sea el principio o el *prefijo* de la ruta de acceso. Este prefijo determina el *espacio de nombres* que está usando la ruta de acceso y, además, los caracteres especiales que se usan en cada posición dentro de la ruta de acceso, incluido el último carácter.

Si un componente de una ruta de acceso es un nombre de archivo, debe ser el último componente.

Cada componente de una ruta de acceso también estará restringido por la longitud máxima especificada para un sistema de archivos determinado. En general, estas reglas se dividen en dos categorías: *corto* y *largo*. Tenga en cuenta que los nombres de directorio se almacenan en el sistema de archivos como un tipo especial de archivo, pero las reglas de nomenclatura de los archivos también se aplican a los nombres de directorio. En Resumen, una ruta de acceso es simplemente la representación de cadena de la jerarquía entre todos los directorios que existen para un determinado nombre de archivo o directorio.

### <a name="fully-qualified-vs-relative-paths"></a>Rutas de acceso completas y relativas

En el caso de las funciones de la API de Windows que manipulan archivos, los nombres de archivo pueden ser con frecuencia en relación con el directorio actual, mientras que algunas API requieren una ruta de acceso completa. Un nombre de archivo es relativo al directorio actual si no comienza con uno de los siguientes elementos:

-   Nombre UNC de cualquier formato, que siempre comienza con dos caracteres de barra diagonal inversa (" \\ \\ "). Para obtener más información, vea la siguiente sección.
-   Un designador de disco con una barra diagonal inversa, por ejemplo "C: \\ " o "d: \\ ".
-   Una sola barra diagonal inversa, por ejemplo, " \\ Directory" o " \\file.txt". Esto también se conoce como una *ruta de acceso absoluta*.

Si un nombre de archivo comienza con solo un designador de disco, pero no la barra diagonal inversa después de los dos puntos, se interpreta como una ruta de acceso relativa al directorio actual en la unidad con la letra especificada. Tenga en cuenta que el directorio actual puede ser o no el directorio raíz en función de su configuración durante la operación de "cambiar directorio" más reciente en ese disco. Los ejemplos de este formato son los siguientes:

-   "C:tmp.txt" hace referencia a un archivo denominado "tmp.txt" en el directorio actual de la unidad C.
-   "C:TEMPDIR \\tmp.txt" hace referencia a un archivo en un subdirectorio del directorio actual de la unidad C.

También se dice que una ruta de acceso es relativa si contiene "puntos dobles"; es decir, dos puntos juntos en un componente de la ruta de acceso. Este especificador especial se utiliza para denotar el directorio situado encima del directorio actual, conocido también como "directorio primario". Los ejemplos de este formato son los siguientes:

-   "..\\tmp.txt "especifica un archivo denominado tmp.txt ubicado en el elemento primario del directorio actual.
-   "..\\..\\tmp.txt "especifica un archivo que es dos directorios por encima del directorio actual.
-   "..\\ TEMPDIR, \\tmp.txt "especifica un archivo denominado tmp.txt ubicado en un directorio denominado TEMPDIR, que es un directorio del mismo nivel en el directorio actual.

Las rutas de acceso relativas pueden combinar ambos tipos de ejemplo, por ejemplo "C:.. \\tmp.txt ". Esto resulta útil porque, aunque el sistema realiza un seguimiento de la unidad actual junto con el directorio actual de esa unidad, también realiza un seguimiento de los directorios actuales de cada una de las letras de unidad diferentes (si el sistema tiene más de uno), independientemente de qué designador de unidad está establecido como la unidad actual.

### <a name="maximum-path-length-limitation"></a>Límite máximo de longitud de ruta de acceso


En las ediciones de Windows anteriores a la versión 1607 de Windows 10, la longitud máxima de una ruta de acceso es la **\_ ruta de acceso** máxima, que se define como 260 caracteres. En versiones posteriores de Windows, es necesario cambiar una clave del registro o usar la herramienta directiva de grupo para quitar el límite. Consulte [límite máximo de longitud de ruta de acceso](./maximum-file-path-limitation.md) para obtener detalles completos.


## <a name="namespaces"></a>Espacios de nombres

Hay dos categorías principales de convenciones de espacio de nombres que se usan en las API de Windows, que normalmente se denominan espacios de nombres *NT* y los *espacios de nombres de Win32*. El espacio de nombres NT se diseñó para ser el espacio de nombres de nivel más bajo en el que podrían existir otros subsistemas y espacios de nombres, incluido el subsistema Win32 y, por extensión, los espacios de nombres Win32. POSIX es otro ejemplo de un subsistema de Windows que se basa en el espacio de nombres NT. Las primeras versiones de Windows también definían varios nombres predefinidos o reservados para determinados dispositivos especiales, como los puertos de comunicaciones (serie y paralelos) y la consola de pantalla predeterminada como parte de lo que ahora se denomina espacio de nombres del dispositivo NT y que todavía se admiten en las versiones actuales de Windows por compatibilidad con versiones anteriores.

### <a name="win32-file-namespaces"></a>Espacios de nombres de archivos Win32

Las convenciones y el prefijo del espacio de nombres Win32 se resumen en esta sección y en la sección siguiente, con descripciones de cómo se usan. Tenga en cuenta que estos ejemplos están diseñados para usarse con las funciones de la API de Windows y no funcionan necesariamente con aplicaciones de Shell de Windows como el explorador de Windows. Por esta razón, existe una gama más amplia de rutas de acceso que normalmente está disponible en las aplicaciones de Shell de Windows y las aplicaciones de Windows que aprovechan esto se pueden desarrollar con estas convenciones de espacio de nombres.

En el caso de la e/s de archivos, el \\ \\ \\ prefijo "?" de una cadena de ruta de acceso indica a las API de Windows que deshabiliten todo el análisis de cadenas y envíen la cadena que le sigue directamente al sistema de archivos. Por ejemplo, si el sistema de archivos admite rutas de acceso de gran tamaño y nombres de archivo, puede superar los límites **máximos de la \_ ruta de acceso** que se aplican en las API de Windows. Para obtener más información sobre la limitación de la ruta de acceso máxima normal, vea la sección anterior [limitación de longitud máxima de ruta de acceso](#maximum-path-length-limitation).

Dado que desactiva la expansión automática de la cadena de ruta de acceso, el \\ \\ \\ prefijo "?" también permite el uso de ".." y "." en los nombres de ruta de acceso, lo que puede resultar útil si está intentando realizar operaciones en un archivo con estos especificadores de ruta de acceso relativos reservados de otro modo como parte de la ruta de acceso completa.

Muchas de las API de e/s de archivos, pero no todas, admiten " \\ \\ ? \\ "; debe consultar el tema de referencia de cada API para asegurarse. 

Tenga en cuenta que se deben usar las API de Unicode para asegurarse de que el \\ \\ \\ prefijo "?" permite superar la **ruta de \_ acceso máxima** 

### <a name="win32-device-namespaces"></a>Espacios de nombres de dispositivos Win32

El \\ \\ \\ prefijo "." tendrá acceso al espacio de nombres del dispositivo Win32 en lugar del espacio de nombres de archivo de Win32. Este es el modo en que el acceso a los volúmenes y discos físicos se realiza directamente, sin pasar por el sistema de archivos, si la API es compatible con este tipo de acceso. Puede tener acceso a muchos dispositivos distintos de los discos de esta manera (mediante las funciones [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) y [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) , por ejemplo).

Por ejemplo, si desea abrir el puerto de comunicaciones serie del sistema 1, puede usar "COM1" en la llamada a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Esto funciona porque COM1 – COM9 forman parte de los nombres reservados en el espacio de nombres NT, aunque el uso del \\ \\ \\ prefijo "." también funcionará con estos nombres de dispositivo. Por comparación, si tiene instalada una placa de expansión de serie de Puerto 100 y desea abrir COM56, no puede abrirla mediante "COM56" porque no hay ningún espacio de nombres NT predefinido para COM56. Tendrá que abrirlo mediante " \\ \\ . \\ COM56 "porque" \\ \\ . \\ "va directamente al espacio de nombres del dispositivo sin intentar buscar un alias predefinido.

Otro ejemplo del uso del espacio de nombres del dispositivo Win32 es usar la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con " \\ \\ . \\ DiscoFísico *x*"(donde *X* es un valor entero válido) o" \\ \\ . \\ CdRom *X*". Esto le permite tener acceso a esos dispositivos directamente y omitir el sistema de archivos. Esto funciona porque el sistema crea estos nombres de dispositivo a medida que estos dispositivos se enumeran, y algunos controladores también crearán otros alias en el sistema. Por ejemplo, el controlador de dispositivo que implementa el nombre "C: \\ " tiene su propio espacio de nombres que también es el sistema de archivos.

Las API que atraviesan la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) generalmente funcionan con el \\ \\ \\ prefijo "." porque **CreateFile** es la función que se usa para abrir archivos y dispositivos, dependiendo de los parámetros que se usen.

Si está trabajando con funciones de la API de Windows, debe usar el \\ \\ \\ prefijo "." para tener acceso solo a los dispositivos y no a los archivos.

La mayoría de las API no admiten " \\ \\ . \\ "; solo las que están diseñadas para funcionar con el espacio de nombres del dispositivo lo reconocerán. Compruebe siempre el tema de referencia de cada API para asegurarse.

### <a name="nt-namespaces"></a>Espacios de nombres NT

También hay API que permiten el uso de la Convención de espacio de nombres NT, pero el administrador de objetos de Windows hace que sea innecesario en la mayoría de los casos. Para ilustrarlo, es útil examinar los espacios de nombres de Windows en el explorador de objetos del sistema mediante la herramienta de Windows Sysinternals [WinObj](/sysinternals/downloads/winobj) . Al ejecutar esta herramienta, lo que se ve es el espacio de nombres NT que empieza en la raíz, o " \\ ". La subcarpeta denominada "global??" es donde reside el espacio de nombres de Win32. Los objetos de dispositivo con nombre residen en el espacio de nombres NT en el subdirectorio "Device". Aquí también puede encontrar Serial0 y Serial1, los objetos de dispositivo que representan los dos primeros puertos COM si están presentes en el sistema. Un objeto de dispositivo que representa un volumen sería algo como "HarddiskVolume1", aunque el sufijo numérico puede variar. El nombre "DR0" en subdirectorio "Harddisk0" es un ejemplo del objeto de dispositivo que representa un disco, etc.

Para que estas aplicaciones de Windows puedan acceder a estos objetos de dispositivo, los controladores de dispositivos crean un vínculo simbólico (symlink) en el espacio de nombres de Win32, "global??", a sus respectivos objetos de dispositivo. Por ejemplo, COM0 y COM1 en la sección "global??" los subdirectorios son simplemente vínculos simbólicos a Serial0 y Serial1, "C:" es un vínculo simbólico a HarddiskVolume1, "Physicaldrive0" es un vínculo simbólico a DR0, etc. Sin un symlink, el dispositivo especificado "xxx" no estará disponible para ninguna aplicación de Windows mediante las convenciones de espacio de nombres Win32, tal y como se ha descrito anteriormente. Sin embargo, se puede abrir un identificador a ese dispositivo mediante cualquier API que admita la ruta de acceso absoluta del espacio de nombres NT del formato " \\ dispositivo \\ xxx".

Con la adición de compatibilidad con varios usuarios a través de Terminal Services y máquinas virtuales, se han vuelto más necesarios para virtualizar el dispositivo raíz en todo el sistema en el espacio de nombres de Win32. Esto se logra agregando el symlink denominado "GLOBALROOT" al espacio de nombres de Win32, que puede ver en la sección "global??". subdirectorio de la herramienta del explorador de WinObj descrito anteriormente y que puede acceder a través de la ruta de acceso " \\ \\ ? \\ GLOBALROOT". Este prefijo garantiza que la ruta de acceso siguiente busca en la ruta de acceso raíz verdadera del administrador de objetos del sistema y no en una ruta de acceso dependiente de la sesión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comparación de la funcionalidad del sistema de archivos](filesystem-functionality-comparison.md)
</dt> </dl>

 

 