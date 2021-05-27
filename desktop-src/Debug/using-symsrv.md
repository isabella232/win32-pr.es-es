---
description: Uso de SymSrv
ms.assetid: d400f222-c50c-4c7b-8f8a-0c3ed3bba3b9
title: Uso de SymSrv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bbaf68e80555629db8bc9a2a21394b95fe6fb85
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550040"
---
# <a name="using-symsrv"></a>Uso de SymSrv

SymSrv entrega archivos de símbolos desde almacenes de símbolos centralizados. Estos almacenes pueden contener cualquier número de archivos de símbolos, correspondientes a cualquier número de programas o sistemas operativos. Los almacenes también pueden contener archivos binarios, que son especialmente útiles al depurar archivos de minivolfón.

Los almacenes pueden contener los archivos binarios y de símbolos reales o simplemente punteros a archivos de símbolos. Si el almacén contiene punteros, SymSrv recuperará los archivos reales directamente de sus orígenes.

SymSrv también puede separar un almacén de símbolos grande en un subconjunto más pequeño que sea adecuado para una tarea de depuración especializada.

Por último, SymSrv puede obtener archivos de símbolos de un origen HTTP o HTTPS mediante la información de inicio de sesión proporcionada por el sistema operativo. SymSrv admite sitios HTTPS protegidos por tarjetas inteligentes, certificados e inicios de sesión y contraseñas normales.

## <a name="setting-the-symbol-path"></a>Establecer la ruta de acceso del símbolo

Como se describe en [Rutas](symbol-paths.md)de acceso de símbolos , la ruta de acceso de símbolos (variable de entorno NT SYMBOL PATH) puede estar integrada por varios elementos path separados por \_ punto y \_ \_ coma. Si uno o varios de estos elementos de ruta de acceso comienzan con el texto "srv", el elemento es un servidor de símbolos y usará SymSrv para buscar archivos \* de símbolos.

> [!Note]  
> Si no se especifica el texto "srv", pero el elemento path real es un almacén de servidores de símbolos, el controlador de símbolos actuará como si se hubiera especificado \* \* "srv". El controlador de símbolos realiza esta determinación buscando la existencia de un archivo denominado "pingme.txt" en el directorio raíz de la ruta de acceso especificada.

 

Al igual que las rutas de acceso de símbolos se realizan con elementos de ruta de acceso de símbolos separados por punto y coma, los servidores de símbolos se realizan con elementos de almacén de símbolos separados por asteriscos. Puede haber hasta 10 almacenes de símbolos después del prefijo \* "srv". Los almacenes que aparecen a  la izquierda de la lista se denominan almacenes de nivel inferior y los almacenes de la derecha se denominan *almacenes ascendentes.*

<dl> srv \* *SymbolStore*  
srv \* *SymbolStore1* \* *SymbolStoreN*  
</dl>

Si solo se incluye un elemento de almacén de símbolos en la ruta de acceso, SymSrv intentará usar cualquier archivo solicitado directamente desde ese almacén.

Si hay dos almacenes de símbolos en la ruta de acceso, SymSrv busca el archivo de símbolos en el almacén de símbolos situado más a la izquierda. Si el archivo está ahí, se usa. Si no está ahí, SymSrv busca en el almacén de símbolos inmediatamente a la derecha. Si el archivo está ahí, se copia en el almacén izquierdo y se abre desde allí.

Si hay más de dos almacenes, este comportamiento continúa a la derecha hasta que se encuentra el archivo o no hay más almacenes en la lista.

El archivo nunca se abre desde ningún almacén, sino desde el almacén situado más a la izquierda. Si el archivo se encuentra en cualquier otro lugar de la cadena, se copia en cada almacén situado a la izquierda. Este proceso de copia se denomina "en cascada" y proporciona ciertas ventajas que se declararán más adelante en este documento.

## <a name="types-of-symbol-stores"></a>Tipos de almacenes de símbolos

En la tabla siguiente se muestran ejemplos de los tipos de almacén de símbolos admitidos.

|  Tipo de almacén de símbolos       |  Descripción |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\\\recurso \\ compartido de servidor          | Una ruta de acceso UNC completa a un recurso compartido en un servidor remoto.                                                                                                                                                                                                                                                                                                 |
| c: \\ LocalCache             | Ruta de acceso a un directorio en el equipo cliente.                                                                                                                                                                                                                                                                                                             |
| https://InternetSite        | Dirección URL de un sitio web que hospeda los símbolos. Debe ser el almacén más a la derecha de la lista y no debe ser el único almacén de la lista.                                                                                                                                                                                                                          |
| https://SecureInternetSite | Dirección URL de un sitio web seguro que hospeda los símbolos. Esto puede admitir contraseñas, credenciales de inicio de sesión de Windows, certificados y tarjetas inteligentes. Debe ser el almacén más a la derecha de la lista y no debe ser el único almacén de la lista.                                                                                                                              |
| <blank>              | Si no hay texto entre dos asteriscos, esto indica el *almacén de nivel inferior predeterminado.* La ubicación se establece mediante una llamada [**a SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory). El valor predeterminado es un directorio denominado "sym" inmediatamente debajo del directorio del programa de la aplicación que realiza la llamada. Esto se conoce a veces como caché *local predeterminada.* |



 

Dado que no se puede escribir en un almacén de símbolos basado en HTTP, debe ser el almacén situado más a la derecha de la lista. Si un almacén de símbolos basado en HTTP se encuentra en el centro o la izquierda de la lista de tiendas, no sería posible copiar en él los archivos encontrados y la cadena se dividiría. Además, dado que el controlador de símbolos no puede abrir un archivo desde un sitio web, un almacén basado en HTTP no debe ser el almacén más a la izquierda o solo el almacén de la lista. Si SymSrv se presenta alguna vez con esta ruta de acceso de símbolos, intentará recuperarse copiando el archivo en el almacén de nivel inferior predeterminado y ábralo desde allí, independientemente de si el almacén de nivel inferior predeterminado se indica en la ruta de acceso del símbolo o no.

## <a name="examples"></a>Ejemplos

Para usar SymSrv con un almacén de símbolos en \\ \\ mybuilds \\ mysymbols, establezca la siguiente ruta de acceso de símbolos:

**set \_ NT \_ SYMBOL \_ PATH= srv \* \\ \\ mybuilds \\ mysymbols**

Para establecer la ruta de acceso de símbolos para que el depurador copie los archivos de símbolos de un almacén de símbolos en \\ \\ mybuilds mysymbols en el directorio \\ local c: \\ localsymbols, use:

**set \_ NT \_ SYMBOL \_ PATH=srv \* c: \\ localsymbols \* \\ \\ mybuilds \\ mysymbols**

Para establecer la ruta de acceso de símbolos para que el depurador copie los archivos de símbolos de un almacén de símbolos en \\ mybuilds mysymbols en el almacén de nivel inferior predeterminado \\ \\ (normalmente c: \\ depuradores \\ sym), use:

**set \_ NT \_ SYMBOL \_ PATH=srv \* \* \\ \\ mybuilds \\ mysymbols**

Para usar un almacén en cascada, establezca la siguiente ruta de acceso de símbolos:

**set \_ NT SYMBOL PATH = \_ \_ srv \* c: \\ localsymbols \* \\ \\ NearbyServer \\ store\*https://DistantServer**

En este ejemplo, SymSrv busca primero el archivo en c: \\ localsymbols. Si se encuentra allí, devolverá una ruta de acceso al archivo. De lo contrario, SymSrv busca el archivo en \\ \\ el almacén \\ NearbyServer. Si se encuentra allí, SymSrv copia el archivo en c: localsymbols y devuelve una ruta de acceso al archivo; si no se encuentra, SymSrv busca el archivo en y, si se encuentra allí, SymSrv copia el archivo en el almacén \\ NearbyServer y, a continuación, en https://DistantServer \\ \\ \\ c: \\ localsymbols.

En este último ejemplo se muestra cómo se puede usar el diseño desaconsciente de una ruta de acceso de símbolos para optimizar la descarga de símbolos. Si tiene un sitio de trabajo con un grupo de depuradores y todos necesitan obtener símbolos de una ubicación lejana, puede configurar un servidor común con un almacén de símbolos cerca de todos los depuradores. A continuación, configure cada depurador con la ruta de acceso de símbolos anterior. El primer depurador que requiere una versión determinada de foo.pdb la descargará desde en el almacén NearbyServer y, a continuación, en su propia máquina https://DistantServer \\ \\ \\ en c: \\ localsymbols. El siguiente depurador que requiere el mismo archivo podrá descargarlo desde el almacén NearbyServer porque el depurador anterior ya lo descargó en \\ \\ \\ esa ubicación. Este almacenamiento en caché de varios niveles ahorra mucho tiempo y ancho de banda de red.

## <a name="microsoft-symbol-store"></a>Almacén de símbolos de Microsoft

Microsoft proporciona acceso a un servidor de símbolos de Internet que contiene archivos de símbolos para las distintas versiones del sistema operativo Windows. No se garantiza que este catálogo de símbolos esté completo, pero es amplio. También se representan otros productos de Microsoft.

El servidor de símbolos de Internet se rellena con una variedad de símbolos de Windows para sistemas operativos Microsoft Windows, incluidas correcciones de accesos temporales, Service Packs, paquetes de paquetes acumulativos de seguridad y versiones comerciales. Los símbolos también están disponibles en el servidor para las versiones beta actuales y los candidatos de lanzamiento para productos de Windows, además de una variedad de otros productos de Microsoft, como Microsoft Internet Explorer.

Si tiene acceso a Internet durante la depuración, puede configurar el depurador para descargar símbolos según sea necesario durante una sesión de depuración, en lugar de descargar archivos de símbolos por separado antes de una sesión de depuración. Los símbolos se descargan en una ubicación de directorio que especifique y, a continuación, el depurador los carga desde allí.

La dirección URL del almacén de símbolos de Microsoft es https://msdl.microsoft.com/download/symbols . En el ejemplo siguiente se muestra cómo establecer la ruta de acceso de símbolos del depurador (sustituya la ruta de acceso del almacén de nivel inferior por *c: \\ DownstreamStore*):

``` syntax
srv*c:\DownstreamStore*https://msdl.microsoft.com/download/symbols
```

## <a name="compressed-files"></a>Archivos comprimidos

SymSrv es compatible con los almacenes de símbolos que contienen archivos comprimidos, siempre que esta compresión se haya creado previamente con la herramienta compress.exe que se distribuyó con el Kit de recursos de Windows Server 2003. Los archivos comprimidos deben tener un carácter de subrayado como último carácter en sus extensiones de archivo (por ejemplo, module1.pd \_ o module2.db). \_ Para más información, consulte [Uso de SymStore.](using-symstore.md)

Cuando se encuentran en cascada, los archivos no se comprimen a menos que el almacén de destino sea el almacén situado más a la izquierda en la ruta de acceso. Si solo hay un almacén en la ruta de acceso y contiene un archivo comprimido, SymSrv copiará el archivo en el almacén de nivel inferior predeterminado y lo abrirá desde allí, aunque el almacén de nivel inferior predeterminado no se indique en la ruta de acceso de símbolos.

**DbgHelp 6.1 y versiones anteriores:** Si los archivos del almacén maestro están comprimidos, debe usar un almacén de nivel inferior. SymSrv descomprimirá todos los archivos antes de copiarlos en el almacén de nivel inferior.

## <a name="deleting-the-cache"></a>Eliminación de la caché

Si usa un almacén de bajada como caché, puede eliminar este directorio en cualquier momento para ahorrar espacio en disco.

Es posible tener un gran almacén de símbolos que incluya archivos de símbolos para muchos programas diferentes o versiones de Windows. Si actualiza la versión de Windows usada en el equipo de destino, todos los archivos de símbolos almacenados en caché coincidirán con la versión anterior. Estos archivos almacenados en caché no serán de ningún uso adicional y, por lo tanto, podría ser un buen momento para eliminar la memoria caché.

Herramientas de depuración para Windows incluye una utilidad denominada agestore.exe que quitará selectivamente los archivos de un árbol de directorios, dejando los archivos usados más recientemente. Esta herramienta está diseñada para la eliminación de archivos no usados de almacenes de servidores de símbolos. Permite controlar muchas opciones, incluidos los algoritmos de fecha límite y tamaño de directorio.

## <a name="flat-cache-directory"></a>Directorio de caché plana

Es posible declarar el almacén de bajada predeterminado como un directorio plano, en lugar de una estructura de árbol de símbolos estándar. Para ello, llame a la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con **SYMOPT \_ FLAT \_ DIRECTORY** (esto también establece la opción **SSRVOPT \_ FLAT DEFAULT \_ \_ STORE** en SymSrv). Asegúrese de llamar a [**SymSetHomeDirectory antes**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) de hacerlo; De lo contrario, los archivos de símbolos se pueden escribir en el directorio del programa.

## <a name="pointer-files"></a>Archivos de puntero

SymStore puede crear y usar archivos que apunten a un archivo de destino en lugar del propio archivo de destino. Si un almacén de símbolos contiene este tipo de archivo de puntero, el valor predeterminado es copiar el archivo desde la ubicación indicada en el archivo de puntero al almacén. Para configurar un almacén de forma que se copie el archivo de puntero en lugar del archivo al que apunta, cree un archivo denominado wantsptr.txt en la raíz del almacén de destino. El contenido de wantsptr.txt no es importante, solo la presencia del archivo.

## <a name="excluding-files-from-symbols-list"></a>Exclusión de archivos de la lista de símbolos

Para excluir archivos de una búsqueda de símbolos, puede especificar sus nombres en symsrv.ini o en el Registro. Para especificar los archivos en symsrv.ini, cree una sección denominada Exclusiones y enumó los archivos. Los nombres de archivo pueden contener caracteres comodín, como se muestra en el ejemplo siguiente:

``` syntax
[Exclusions]
dbghelp.pdb
symsrv.*
mso*
```

Symsrv.ini debe encontrarse en el mismo directorio que symsrv.dll reside. En la mayoría de las instalaciones, el archivo no existe y tendrá que crear uno nuevo.

Como alternativa, puede almacenar los archivos que se excluirán en el Registro. Cree la siguiente clave del Registro: **HKEY \_ LOCAL MACHINE Software Microsoft Symbol Server \_ \\ \\ \\ \\ Exclusions**. Almacene cada nombre de archivo como un valor de cadena (REG \_ SZ) dentro de esta clave. El nombre del valor de cadena especifica el nombre del archivo que se va a excluir. Puede usar el contenido del valor de cadena para almacenar un comentario que describa por qué se excluye el archivo.

## <a name="installation"></a>Instalación

El servidor de símbolos SymSrv (symsrv.dll) se incluye en el paquete Herramientas de depuración para Windows. Debe instalarse en el mismo directorio que la copia de dbghelp.dll que está cargando. Para obtener más información, vea [Llamar a la biblioteca DbgHelp](calling-the-dbghelp-library.md).

 

 



