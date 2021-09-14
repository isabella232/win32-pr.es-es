---
description: Todos los sistemas de archivos compatibles Windows el concepto de archivos y directorios para acceder a los datos almacenados en un disco o dispositivo.
ms.assetid: 121cd5b2-e6fd-4eb4-99b4-b652d27b53e8
title: Asignar nombres a archivos, rutas de acceso y espacios de nombres
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: 59f626c931a61255cef8be9ede594cb97924cfb0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069901"
---
# <a name="naming-files-paths-and-namespaces"></a>Asignar nombres a archivos, rutas de acceso y espacios de nombres

Todos los sistemas de archivos compatibles Windows el concepto de archivos y directorios para acceder a los datos almacenados en un disco o dispositivo. Windows desarrolladores que trabajan con las API de Windows para E/S de archivos y dispositivos deben comprender las distintas reglas, convenciones y limitaciones de los nombres de archivos y directorios.

Se puede acceder a los datos desde discos, dispositivos y recursos compartidos de red mediante las API de E/S de archivos. Los archivos y directorios, junto con los espacios de nombres, forman parte del concepto de una ruta de acceso, que es una representación de cadena de dónde obtener los datos, independientemente de si son de un disco, un dispositivo o una conexión de red para una operación específica.

Algunos sistemas de archivos, como NTFS, admiten archivos y directorios vinculados, que también siguen las reglas y convenciones de nomenclatura de archivos como lo haría un archivo o directorio normal. Para obtener más información, [vea Vínculos y uniones duros](hard-links-and-junctions.md) y [Puntos de análisis y operaciones de archivo.](reparse-points-and-file-operations.md)

Para obtener información adicional, vea las siguientes subsecciones:

-   [Nombres de archivos y directorios](#file-and-directory-names)
    -   [Convenciones de nomenclatura](#naming-conventions)
    -   [Nombres cortos frente a largos](#short-vs-long-names)
-   [Paths](#fully-qualified-vs-relative-paths)
    -   [Rutas de acceso completas frente a rutas de acceso relativas](#fully-qualified-vs-relative-paths)
    -   [Limitación de longitud máxima de la ruta de acceso](#maximum-path-length-limitation)
-   [Espacios de nombres](#win32-file-namespaces)
    -   [Espacios de nombres de archivo win32](#win32-file-namespaces)
    -   [Espacios de nombres de dispositivo Win32](#win32-device-namespaces)
    -   [Espacios de nombres NT](#nt-namespaces)
-   [Temas relacionados](#related-topics)


Para obtener información sobre la configuración de Windows 10 para admitir rutas de acceso de archivo largas, vea [Limitación de longitud máxima de la ruta de acceso](./maximum-file-path-limitation.md).


## <a name="file-and-directory-names"></a>Nombres de archivos y directorios

Todos los sistemas de archivos siguen las mismas convenciones de nomenclatura generales para un archivo individual: un nombre de archivo base y una extensión opcional, separados por un punto. Sin embargo, cada sistema de archivos, como NTFS, CDFS, ex LDAP, UDFS, FAT y FAT32, puede tener reglas específicas y diferentes sobre la formación de los componentes individuales en la ruta de acceso a un directorio o archivo. Tenga en *cuenta* que un directorio es simplemente un archivo con un atributo especial que lo designa como directorio, pero de lo contrario debe seguir las mismas reglas de nomenclatura que un archivo normal. Dado que  el término directorio simplemente hace referencia a un tipo especial de archivo en  lo que respecta al sistema de archivos, algún material de referencia usará el archivo de término general para abarcar los conceptos de directorios y archivos de datos como tales. Por este problema, a menos que se especifique lo contrario, las reglas de nomenclatura o uso o los ejemplos de un archivo también se deben aplicar a un directorio. El término *ruta de* acceso hace referencia a uno o varios directorios, barras diagonales inversas y, posiblemente, un nombre de volumen. Para más información, consulte la sección [Rutas de](#fully-qualified-vs-relative-paths) acceso.

Las limitaciones del recuento de caracteres también pueden ser diferentes y pueden variar en función del sistema de archivos y el formato de prefijo de nombre de ruta de acceso usado. Esto se complica aún más por la compatibilidad con mecanismos de compatibilidad con versiones anteriores. Por ejemplo, el sistema de archivos FAT de MS-DOS anterior admite un máximo de 8 caracteres para el nombre de archivo base y 3 caracteres para la extensión, para un total de 12 caracteres, incluido el separador de puntos. Esto se conoce normalmente como un nombre de archivo *8.3.* Los Windows de archivos FAT y NTFS no se limitan a los nombres de archivo 8.3, ya que admiten nombres de archivo largos, pero siguen siendo compatibles con la versión 8.3 de los nombres de archivo largos.

### <a name="naming-conventions"></a>Convenciones de nomenclatura

Las siguientes reglas fundamentales permiten a las aplicaciones crear y procesar nombres válidos para archivos y directorios, independientemente del sistema de archivos:

-   Use un punto para separar el nombre de archivo base de la extensión en el nombre de un directorio o archivo.
-   Use una barra diagonal inversa ( \\ ) para separar los *componentes* de una ruta *de acceso*. La barra diagonal inversa divide el nombre de archivo de la ruta de acceso a él y un nombre de directorio de otro nombre de directorio en una ruta de acceso. No se puede usar una barra diagonal inversa en el nombre del archivo o directorio real porque es un carácter reservado que separa los nombres en componentes.
-   Use una barra diagonal inversa según sea necesario como parte de los nombres de volumen [,](naming-a-volume.md)por ejemplo, "C: " en "C: archivo de ruta de acceso" o "recurso compartido de servidor" en " archivo de ruta de acceso del recurso compartido de servidor" para nombres de convención de \\ nomenclatura \\ universal \\ \\ \\ \\ \\ \\ \\ \\ \\ (UNC). Para obtener más información sobre los nombres UNC, consulte la [sección Limitación de longitud máxima de la ruta de](#maximum-path-length-limitation) acceso.
-   No asuma la confidencialidad de mayúsculas y minúsculas. Por ejemplo, tenga en cuenta que los nombres DESEX, Luego y Asíns son los mismos, aunque algunos sistemas de archivos (por ejemplo, un sistema de archivos compatible con POSIX) puedan considerarlos diferentes. Tenga en cuenta que NTFS admite la semántica POSIX para la distinción entre mayúsculas y minúsculas, pero este no es el comportamiento predeterminado. Para obtener más información, vea [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).
-   Los designadores de volumen (letras de unidad) no tienen en cuenta las mayúsculas y minúsculas. Por ejemplo, "D: \\ " y "d: \\ " hacen referencia al mismo volumen.
-   Use cualquier carácter de la página de códigos actual para un nombre, incluidos los caracteres Unicode y los caracteres del juego de caracteres extendido (128-255), excepto los siguientes:

    -   Los siguientes caracteres reservados:

        -   < (menor que)
        -   \> (mayor que)
        -   : (dos puntos)
        -   " (comilla doble)
        -   / (barra diagonal)
        -   \\ (barra diagonal inversa)
        -   \| (barra vertical o barra vertical)
        -   ? (signo de interrogación)
        -   \* (asterisco)

    -   Valor entero cero, al que a veces se hace referencia como carácter *NUL* ASCII.
    -   Caracteres cuyas representaciones de enteros están en el intervalo comprendido entre 1 y 31, excepto para los flujos de datos alternativos en los que se permiten estos caracteres. Para obtener más información sobre las secuencias de archivos, vea [File Secuencias](file-streams.md).
    -   Cualquier otro carácter que el sistema de archivos de destino no permita.

-   Use un punto como componente de *directorio en* una ruta de acceso para representar el directorio actual, por ejemplo ". \\temp.txt". Para obtener más información, vea [Rutas de acceso](#fully-qualified-vs-relative-paths).
-   Use dos períodos consecutivos (..) como componente de directorio en una ruta de acceso para representar el elemento primario del directorio actual, por ejemplo "..  \\temp.txt". Para obtener más información, vea [Rutas de acceso](#fully-qualified-vs-relative-paths).
-   No use los siguientes nombres reservados para el nombre de un archivo:

    CON, PRN, AUX, NUL, COM1, COM2, COM3, COM4, COM5, COM6, COM7, COM8, COM9, LPT1, LPT2, LPT3, LPT4, LPT5, LPT6, LPT7, LPT8 y LPT9. Evite también estos nombres seguidos inmediatamente de una extensión. por ejemplo, NUL.txt no se recomienda. Para más información, consulte [Espacios de nombres](#win32-file-namespaces).

-   No termine un nombre de archivo o directorio con un espacio o un punto. Aunque el sistema de archivos subyacente puede admitir estos nombres, Windows shell y la interfaz de usuario no. Sin embargo, es aceptable especificar un punto como primer carácter de un nombre. Por ejemplo, ".temp".

### <a name="short-vs-long-names"></a>Nombres cortos frente a largos

Un nombre de archivo largo se considera cualquier nombre de archivo que supere la convención de nomenclatura de estilo MS-DOS corto (también denominada *8.3).* Al crear un nombre de archivo largo, Windows también puede crear un formato corto 8.3 del nombre, denominado *alias 8.3* o nombre corto, y almacenarlo también en el disco. Este alias 8.3 se puede deshabilitar por motivos de rendimiento en todo el sistema o para un volumen especificado, dependiendo del sistema de archivos concreto.

**Windows Server 2008, Windows Vista, Windows Server 2003** y Windows XP: los alias 8.3 no se pueden deshabilitar para volúmenes especificados hasta Windows 7 y Windows Server 2008 R2.

En muchos sistemas de archivos, un nombre de archivo contendrá una tilde (~) dentro de cada componente del nombre que es demasiado largo para cumplir las reglas de nomenclatura 8.3.

> [!Note]  
> No todos los sistemas de archivos siguen la convención de sustitución de tilde y los sistemas se pueden configurar para deshabilitar la generación de alias 8.3 aunque normalmente la admitan. Por lo tanto, no suposiciones de que el alias 8.3 ya existe en el disco.

 

Para solicitar nombres de archivo 8.3, nombres de archivo largos o la ruta de acceso completa de un archivo desde el sistema, tenga en cuenta las siguientes opciones:

-   Para obtener el formato 8.3 de un nombre de archivo largo, use la [**función GetShortPathName.**](/windows/desktop/api/FileAPI/nf-fileapi-getshortpathnamew)
-   Para obtener la versión de nombre de archivo largo de un nombre corto, use la [**función GetLongPathName.**](/windows/desktop/api/FileAPI/nf-fileapi-getlongpathnamea)
-   Para obtener la ruta de acceso completa a un archivo, use la [**función GetFullPathName.**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea)

En sistemas de archivos más recientes, como NTFS, exMF, UDFS y FAT32, Windows almacena los nombres de archivo largos en disco en Unicode, lo que significa que el nombre de archivo largo original siempre se conserva. Esto es cierto incluso si un nombre de archivo largo contiene caracteres extendidos, independientemente de la página de códigos que esté activa durante una operación de lectura o escritura de disco.

Los archivos que usan nombres de archivo largos se pueden copiar entre particiones del sistema de archivos NTFS y Windows particiones del sistema de archivos FAT sin perder ninguna información de nombre de archivo. Esto puede no ser cierto para la fat de MS-DOS anterior y algunos tipos de sistemas de archivos CDFS (CD-ROM), dependiendo del nombre de archivo real. En este caso, el nombre de archivo corto se sustituye si es posible.

## <a name="paths"></a>Rutas de acceso

La  ruta de acceso a un archivo especificado consta de uno o varios componentes *,* separados por un carácter especial (una barra diagonal inversa), donde cada componente suele ser un nombre de directorio o nombre de archivo, pero con algunas excepciones importantes que se deban tratar a continuación. A menudo es fundamental para la interpretación del sistema de una ruta de acceso con el aspecto que tiene el principio o prefijo de la ruta de acceso. Este prefijo determina el *espacio* de nombres que usa la ruta de acceso y, además, qué caracteres especiales se usan en qué posición dentro de la ruta de acceso, incluido el último carácter.

Si un componente de una ruta de acceso es un nombre de archivo, debe ser el último componente.

Cada componente de una ruta de acceso también estará restringido por la longitud máxima especificada para un sistema de archivos determinado. En general, estas reglas se divide en dos categorías: *short* y *long.* Tenga en cuenta que el sistema de archivos almacena los nombres de directorio como un tipo especial de archivo, pero las reglas de nomenclatura de los archivos también se aplican a los nombres de directorio. En resumen, una ruta de acceso es simplemente la representación de cadena de la jerarquía entre todos los directorios que existen para un nombre de archivo o directorio determinado.

### <a name="fully-qualified-vs-relative-paths"></a>Rutas de acceso completas frente a rutas de acceso relativas

En Windows funciones de API que manipulan archivos, los nombres de archivo a menudo pueden ser relativos al directorio actual, mientras que algunas API requieren una ruta de acceso completa. Un nombre de archivo es relativo al directorio actual si no comienza por uno de los siguientes:

-   Un nombre UNC de cualquier formato, que siempre comienza con dos caracteres de barra diagonal inversa (" \\ \\ "). Para obtener más información, vea la siguiente sección.
-   Un designador de disco con una barra diagonal inversa, por ejemplo"C: \\ " o "d: \\ ".
-   Una única barra diagonal inversa, por ejemplo, \\ "directorio" \\ o "file.txt". Esto también se conoce como una ruta *de acceso absoluta.*

Si un nombre de archivo comienza solo con un designador de disco, pero no con la barra diagonal inversa después de los dos puntos, se interpreta como una ruta de acceso relativa al directorio actual en la unidad con la letra especificada. Tenga en cuenta que el directorio actual puede ser o no el directorio raíz en función de lo que se haya establecido en durante la operación de "cambio de directorio" más reciente en ese disco. A continuación se muestran ejemplos de este formato:

-   "C:tmp.txt" hace referencia a un archivo denominado "tmp.txt" en el directorio actual de la unidad C.
-   "C:tempdirtmp.txt" hace referencia a un archivo de un subdirectorio al \\ directorio actual de la unidad C.

También se dice que una ruta de acceso es relativa si contiene "puntos dobles"; es decir, dos períodos juntos en un componente de la ruta de acceso. Este especificador especial se usa para indicar el directorio por encima del directorio actual, también conocido como "directorio primario". A continuación se muestran ejemplos de este formato:

-   "..\\tmp.txt" especifica un archivo denominado tmp.txt ubicado en el elemento primario del directorio actual.
-   "..\\..\\tmp.txt" especifica un archivo que está dos directorios por encima del directorio actual.
-   "..\\ tempdirtmp.txt" especifica un archivo denominado tmp.txt ubicado en un directorio denominado tempdir que es un directorio del mismo nivel \\ en el directorio actual.

Las rutas de acceso relativas pueden combinar ambos tipos de ejemplo, por ejemplo "C:.. \\tmp.txt". Esto es útil porque, aunque el sistema realiza un seguimiento de la unidad actual junto con el directorio actual de esa unidad, también realiza un seguimiento de los directorios actuales en cada una de las distintas letras de unidad (si el sistema tiene más de una), independientemente de qué designador de unidad esté establecido como unidad actual.

### <a name="maximum-path-length-limitation"></a>Limitación de longitud máxima de la ruta de acceso


En las ediciones de Windows anteriores Windows 10 versión 1607, la longitud máxima de una ruta de acceso es **MAX \_ PATH**, que se define como 260 caracteres. En versiones posteriores de Windows, es necesario cambiar una clave del Registro o usar directiva de grupo herramienta para quitar el límite. Consulte [Limitación de longitud máxima de la ruta de](./maximum-file-path-limitation.md) acceso para obtener detalles completos.


## <a name="namespaces"></a>Espacios de nombres

Hay dos categorías principales de convenciones de espacio de nombres que se usan en las API de Windows, normalmente *denominadas* espacios de nombres NT y espacios de *nombres Win32.* El espacio de nombres NT se diseñó para ser el espacio de nombres de nivel más bajo en el que podrían existir otros subsistemas y espacios de nombres, incluidos el subsistema Win32 y, por extensión, los espacios de nombres Win32. POSIX es otro ejemplo de un subsistema de Windows que se basa en el espacio de nombres NT. Las primeras versiones de Windows también definieron varios nombres predefinidos o reservados para determinados dispositivos especiales, como puertos de comunicaciones (serie y paralelos) y la consola de pantalla predeterminada como parte de lo que ahora se denomina espacio de nombres de dispositivo NT, y todavía se admiten en las versiones actuales de Windows por compatibilidad con versiones anteriores.

### <a name="win32-file-namespaces"></a>Espacios de nombres de archivo win32

Las convenciones y prefijos del espacio de nombres Win32 se resumen en esta sección y en la siguiente, con descripciones de cómo se usan. Tenga en cuenta que estos ejemplos están diseñados para usarse con las funciones de api de Windows y no funcionan necesariamente con aplicaciones de shell de Windows como Windows Explorer. Por esta razón, hay una gama más amplia de posibles rutas de acceso de las que normalmente están disponibles en las aplicaciones de shell de Windows, y las aplicaciones de Windows que aprovechan esta ventaja se pueden desarrollar mediante estas convenciones de espacio de nombres.

En el caso de la E/S de archivo, el prefijo " ? " en una cadena de ruta de acceso indica a las API de Windows que deshabilite todo el análisis de cadenas y envíe la cadena que sigue directamente al sistema de \\ \\ \\ archivos. Por ejemplo, si el sistema de archivos admite rutas de acceso de gran tamaño y nombres de archivo, puede superar los límites **de MAX \_ PATH** que, de lo contrario, aplican las API Windows archivos. Para obtener más información sobre la limitación de la ruta de acceso máxima normal, vea la sección anterior [Limitación](#maximum-path-length-limitation)de longitud máxima de la ruta de acceso .

Dado que desactiva la expansión automática de la cadena de ruta de acceso, el prefijo " ? " también permite el uso de \\ \\ ".." y "." en los nombres de ruta de acceso, lo que puede ser útil si intenta realizar operaciones en un archivo con estos especificadores de ruta de acceso relativa reservados como parte de la ruta de acceso \\ completa.

Muchas API de E/S de archivos, pero no todas, admiten " ? "; debe ver el tema de referencia de \\ \\ cada API para \\ asegurarse. 

Tenga en cuenta que las API Unicode deben usarse para asegurarse de que el prefijo "? " le permite \\ \\ superar el valor de \\ MAX **\_ PATH.** 

### <a name="win32-device-namespaces"></a>Espacios de nombres de dispositivo Win32

El prefijo " . " tendrá acceso al espacio de nombres del dispositivo \\ \\ \\ Win32 en lugar del espacio de nombres del archivo Win32. Este es el modo en que el acceso a los discos físicos y los volúmenes se realiza directamente, sin pasar por el sistema de archivos, si la API admite este tipo de acceso. Puede acceder a muchos dispositivos distintos de los discos de esta manera (por ejemplo, mediante las funciones [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) y [**DefineDosDevice).**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew)

Por ejemplo, si desea abrir el puerto 1 de comunicaciones serie del sistema, puede usar "COM1" en la llamada a la [**función CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Esto funciona porque COM1-COM9 forman parte de los nombres reservados en el espacio de nombres NT, aunque el prefijo " . " también funcionará con estos \\ \\ nombres de \\ dispositivo. En comparación, si tiene una placa de expansión serie de 100 puertos instalada y desea abrir COM56, no puede abrirla con "COM56" porque no hay ningún espacio de nombres NT predefinido para COM56. Tendrá que abrirlo con " \\ \\ . \\ COM56" porque " . " va directamente al espacio de nombres del dispositivo \\ \\ sin intentar localizar un \\ alias predefinido.

Otro ejemplo de uso del espacio de nombres de dispositivo Win32 es el uso de la [**función CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con " \\ \\ . \\ Disco *físico X*" (donde *X* es un valor entero válido) o " \\ \\ . \\ CdRom *X*". Esto le permite acceder a esos dispositivos directamente, omitiendo el sistema de archivos. Esto funciona porque el sistema crea estos nombres de dispositivo a medida que se enumeran estos dispositivos y algunos controladores también crearán otros alias en el sistema. Por ejemplo, el controlador de dispositivo que implementa el nombre "C: " tiene su propio espacio de nombres que también resulta \\ ser el sistema de archivos.

Las API que pasan por la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) suelen funcionar con el prefijo " . " porque CreateFile es la función que se usa para abrir archivos y dispositivos, en función de los parámetros \\ \\ \\ que use. 

Si está trabajando con Windows API, debe usar el prefijo " . " para acceder solo a los dispositivos \\ \\ y no a los \\ archivos.

La mayoría de las API no admitirán " . "; solo las que están diseñadas para trabajar con el espacio de nombres \\ \\ del dispositivo lo \\ reconocerán. Compruebe siempre el tema de referencia de cada API para asegurarse.

### <a name="nt-namespaces"></a>Espacios de nombres NT

También hay API que permiten el uso de la convención de espacio de nombres NT, pero el Administrador de Windows hace que sea innecesario en la mayoría de los casos. Para ilustrar esto, es útil examinar los espacios de nombres Windows en el explorador de objetos del sistema mediante la Windows Sysinternals [WinObj.](/sysinternals/downloads/winobj) Al ejecutar esta herramienta, lo que ve es el espacio de nombres NT que comienza en la raíz o " \\ ". La subcarpeta denominada "¿Global?". es donde reside el espacio de nombres Win32. Los objetos de dispositivo con nombre residen en el espacio de nombres NT dentro del subdirectorio "Dispositivo". Aquí también puede encontrar Serial0 y Serial1, los objetos de dispositivo que representan los dos primeros puertos COM si están presentes en el sistema. Un objeto de dispositivo que representa un volumen sería algo parecido a "HarddiskVolume1", aunque el sufijo numérico puede variar. El nombre "DR0" en el subdirectorio "Harddisk0" es un ejemplo del objeto de dispositivo que representa un disco, y así sucesivamente.

Para que estas aplicaciones puedan acceder a estos objetos de dispositivo Windows, los controladores de dispositivos crean un vínculo simbólico (symlink) en el espacio de nombres Win32, "¿Global?", a sus respectivos objetos de dispositivo. Por ejemplo, COM0 y COM1 en "Global?". Los subdirectorios son simplemente vínculos simbólicos a Serial0 y Serial1, "C:" es un vínculo simbólico a HarddiskVolume1, "Physicaldrive0" es un vínculo simbólico a DR0, y así sucesivamente. Sin un vínculo simbólico, un dispositivo especificado "Xxx" no estará disponible para ninguna aplicación de Windows mediante convenciones de espacio de nombres Win32 como se describió anteriormente. Sin embargo, se podría abrir un identificador en ese dispositivo mediante cualquier API que admita la ruta de acceso absoluta del espacio de nombres NT con el formato \\ "Dispositivo \\ Xxx".

Con la adición de compatibilidad con varios usuarios a través de Terminal Services y máquinas virtuales, es necesario virtualizar aún más el dispositivo raíz de todo el sistema en el espacio de nombres Win32. Esto se logra mediante la adición del vínculo simbólico denominado "GLOBALROOT" al espacio de nombres Win32, que puede ver en el "Global?". subdirectorio de la herramienta del explorador WinObj que se ha analizado anteriormente y puede acceder a través de la ruta de acceso " \\ \\ ? \\ GLOBALROOT". Este prefijo garantiza que la ruta de acceso siguiente se vea en la ruta de acceso raíz verdadera del administrador de objetos del sistema y no en una ruta de acceso dependiente de la sesión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comparación de la funcionalidad del sistema de archivos](filesystem-functionality-comparison.md)
</dt> </dl>

 

 