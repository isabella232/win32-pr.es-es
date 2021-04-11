---
description: Usar SymSrv
ms.assetid: d400f222-c50c-4c7b-8f8a-0c3ed3bba3b9
title: Usar SymSrv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae79d9fd045ab3ce946c14468e56419d3074858c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274962"
---
# <a name="using-symsrv"></a>Usar SymSrv

SymSrv entrega archivos de símbolos de almacenes de símbolos centralizados. Estos almacenes pueden contener cualquier número de archivos de símbolos, que se correspondan con cualquier número de programas o sistemas operativos. Los almacenes también pueden contener archivos binarios, que son especialmente útiles al depurar archivos de minivolcado.

Los almacenes pueden contener los archivos de símbolos y binarios reales o simplemente punteros a archivos de símbolos. Si el almacén contiene punteros, SymSrv recuperará los archivos reales directamente de sus orígenes.

SymSrv también puede separar un almacén de símbolos grande en un subconjunto más pequeño que sea adecuado para una tarea de depuración especializada.

Por último, SymSrv puede obtener archivos de símbolos de un origen HTTP o HTTPS mediante la información de inicio de sesión proporcionada por el sistema operativo. SymSrv admite sitios HTTPS protegidos por tarjetas inteligentes, certificados e inicios de sesión y contraseñas normales.

## <a name="setting-the-symbol-path"></a>Establecer la ruta de acceso de símbolos

Como se describe en rutas de acceso de [símbolos](symbol-paths.md), la ruta de acceso de símbolos (variable de \_ entorno de \_ \_ ruta de acceso de símbolos de NT) puede estar formada por varios elementos de ruta de acceso separados por punto y coma. Si alguno de estos elementos de ruta de acceso comienza con el texto "SRV \* ", el elemento es un servidor de símbolos y usará SymSrv para buscar archivos de símbolos.

> [!Note]  
> Si \* no se especifica el texto "SRV" pero el elemento de ruta de acceso real es un almacén del servidor de símbolos, el controlador de símbolos actuará como si \* se hubiera especificado "SRV". El controlador de símbolos realiza esta determinación buscando la existencia de un archivo llamado "pingme.txt" en el directorio raíz de la ruta de acceso especificada.

 

Del mismo modo que las rutas de acceso de símbolos se componen de elementos de ruta de símbolos separados por punto y coma, los servidores de símbolos se componen de elementos de almacén de símbolos separados por asteriscos. Puede haber hasta 10 almacenes de símbolos después del \* prefijo "SRV". Los almacenes que aparecen a la izquierda de la lista se denominan almacenes de *bajada* y almacenes a la derecha se denominan almacenes *ascendentes* .

<dl> SRV \* *SymbolStore*  
SRV \* *SymbolStore1* \* *SymbolStoreN*  
</dl>

Si solo hay un elemento de almacén de símbolos incluido en la ruta de acceso, SymSrv intentará usar el archivo solicitado directamente desde ese almacén.

Si hay dos almacenes de símbolos en la ruta de acceso, SymSrv busca el archivo de símbolos en el almacén de símbolos de la izquierda. Si el archivo está ahí, se usa. Si no está allí, SymSrv buscará en el almacén de símbolos inmediatamente a la derecha. Si el archivo está ahí, se copia en el almacén izquierdo y se abre desde allí.

Si hay más de dos almacenes, este comportamiento se mantiene a la derecha hasta que se encuentra el archivo o hasta que no hay más almacenes en la lista.

El archivo nunca se abre desde ningún almacén, pero el almacén que se encuentra más a la izquierda. Si el archivo se encuentra en otra parte de la cadena, se copia en todos los almacenes a su izquierda. Este proceso de copia se denomina "en cascada" y proporciona ciertas ventajas que se clarfiedrán más adelante en este documento.

## <a name="types-of-symbol-stores"></a>Tipos de almacenes de símbolos

En la tabla siguiente se muestran ejemplos de los tipos de almacén de símbolos admitidos.

|                            |                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\\\\\recurso compartido de servidor          | Una ruta de acceso UNC completa a un recurso compartido en un servidor remoto.                                                                                                                                                                                                                                                                                                 |
| c: \\ LocalCache             | Una ruta de acceso a un directorio en el equipo cliente.                                                                                                                                                                                                                                                                                                             |
| https://InternetSite        | Dirección URL de un sitio web que hospeda los símbolos. Debe ser el almacén que se encuentra más a la derecha en la lista y no debe ser el único almacén de la lista.                                                                                                                                                                                                                          |
| https://SecureInternetSite | Dirección URL de un sitio web seguro que hospeda los símbolos. Esto puede admitir contraseñas, credenciales de inicio de sesión de Windows, certificados y tarjetas inteligentes. Debe ser el almacén que se encuentra más a la derecha en la lista y no debe ser el único almacén de la lista.                                                                                                                              |
| <blank>              | Si no hay texto entre dos asteriscos, indica el *almacén predeterminado de bajada*. La ubicación se establece mediante una llamada a [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory). El valor predeterminado es un directorio denominado "SYM" inmediatamente debajo del directorio de programas de la aplicación que realiza la llamada. A veces, esto se conoce como la *caché local predeterminada*. |



 

Dado que no se puede escribir en un almacén de símbolos basado en HTTP, debe ser el almacén de la derecha de la lista. Si un almacén de símbolos basado en HTTP se encontraba en el centro o a la izquierda de la lista de almacenes, no sería posible copiar los archivos encontrados en él y la cadena se interrumpiría. Además, dado que el controlador de símbolos no puede abrir un archivo de un sitio web, un almacén basado en HTTP no debe ser el almacén de la parte más a la izquierda o el único de la lista. Si alguna vez se presenta SymSrv con esta ruta de acceso de símbolos, intentará recuperarse mediante la copia del archivo en el almacén predeterminado de bajada y abrirlo desde allí, con independencia de si el almacén de bajada predeterminado está indicado en la ruta de acceso de símbolos o no.

## <a name="examples"></a>Ejemplos

Para usar SymSrv con un almacén de símbolos en \\ \\ las generaciones de símbolos \\ , establezca la siguiente ruta de acceso de símbolos:

**establecer \_ \_ ruta de acceso de símbolos NT \_ = SRV \* \\ \\ \\**

Para establecer la ruta de acceso de símbolos de modo que el depurador copie los archivos de símbolos de un almacén de símbolos en \\ \\ \\ el directorio local c: \\ localsymbols, use:

**set \_ NT \_ Symbol \_ path = SRV \* c: \\ localsymbols \* \\ \\ crea \\ símbolos**

Para establecer la ruta de acceso de símbolos de modo que el depurador copie los archivos de símbolos de un almacén de símbolos en \\ \\ las generaciones de símbolos \\ al almacén de bajada predeterminado (normalmente c: \\ debuggers \\ SYM), use:

**establecer \_ \_ ruta de acceso de símbolos NT \_ = SRV \* \* \\ \\ \\**

Para usar un almacén en cascada, establezca la siguiente ruta de acceso de símbolos:

**establecer \_ \_ ruta de acceso de símbolos NT \_ = SRV \* c: \\ localsymbols \* \\ \\ NearbyServer \\ Store\*https://DistantServer**

En este ejemplo, SymSrv busca primero el archivo en c: \\ localsymbols. Si se encuentra allí, devolverá una ruta de acceso al archivo. De lo contrario, SymSrv busca el archivo en el \\ \\ almacén de NearbyServer \\ . Si se encuentra ahí, SymSrv copia el archivo en c: \\ localsymbols y devuelve una ruta de acceso al archivo; si no se encuentra, SymSrv busca el archivo en https://DistantServer y, si lo encuentra, SymSrv copia el archivo en \\ \\ NearbyServer \\ Store y, a continuación, a c: \\ localsymbols.

En este último ejemplo se muestra cómo se puede usar el diseño prudente de una ruta de acceso de símbolos para optimizar la descarga de símbolos. Si tiene un sitio de trabajo con un grupo de depuradores y todos necesitan obtener símbolos de una ubicación lejana, puede configurar un servidor común con un almacén de símbolos cerca de todos los depuradores. Después, configure cada depurador con la ruta de acceso de símbolos anterior. El primer depurador que requiere una determinada versión de Foo. pdb lo descargará de https://DistantServer en \\ \\ \\ el almacén de NearbyServer y, a continuación, en su propia máquina en c: \\ localsymbols. El siguiente depurador que requiera el mismo archivo podrá descargarlo de \\ \\ NearbyServer \\ Store, ya que el depurador anterior ya lo descargó en esa ubicación. Este almacenamiento en caché de varios niveles ahorra mucho tiempo y ancho de banda de red.

## <a name="microsoft-symbol-store"></a>Almacén de símbolos de Microsoft

Microsoft proporciona acceso a un servidor de símbolos de Internet que contiene archivos de símbolos para las distintas versiones del sistema operativo Windows. No se garantiza que este catálogo de símbolos esté completo, pero es amplio. También se representan otros productos de Microsoft.

El servidor de símbolos de Internet se rellena con una variedad de símbolos de Windows para los sistemas operativos Microsoft Windows, incluidas las correcciones urgentes, los Service Pack, los paquetes de acumulación de seguridad y las versiones de lanzamiento. Los símbolos también están disponibles en el servidor para las versiones beta actuales y candidatas para lanzamiento de productos de Windows, además de otros productos de Microsoft, como Microsoft Internet Explorer.

Si tiene acceso a Internet durante la depuración, puede configurar el depurador para que descargue los símbolos según sea necesario durante una sesión de depuración, en lugar de descargar los archivos de símbolos por separado antes de una sesión de depuración. Los símbolos se descargan en una ubicación de directorio especificada y, a continuación, el depurador los carga desde allí.

La dirección URL del almacén de símbolos de Microsoft es https://msdl.microsoft.com/download/symbols . En el ejemplo siguiente se muestra cómo establecer la ruta de acceso del símbolo del depurador (sustituir la ruta de acceso del almacén inferior para *c: \\ DownstreamStore*):

``` syntax
srv*c:\DownstreamStore*https://msdl.microsoft.com/download/symbols
```

## <a name="compressed-files"></a>Archivos comprimidos

SymSrv es compatible con los almacenes de símbolos que contienen archivos comprimidos, siempre que esta compresión se haya creado con la compress.exe herramienta que se distribuyó con el kit de recursos de Windows Server 2003. Los archivos comprimidos deben tener un carácter de subrayado como último carácter en sus extensiones de archivo (por ejemplo, Module1. PD \_ o Module2. dB \_ ). Para obtener más información, consulte [uso de SymStore](using-symstore.md).

En cascada, los archivos no se descomprimen a menos que el almacén de destino sea el almacén de la izquierda en la ruta de acceso. Si solo hay un almacén en la ruta de acceso y contiene un archivo comprimido, SymSrv copiará el archivo en el almacén de bajada predeterminado y lo abrirá desde allí, aunque el almacén predeterminado de bajada no se indique en su ruta de acceso de símbolos.

**DbgHelp 6,1 y versiones anteriores:** Si los archivos del almacén maestro están comprimidos, debe usar un almacén de bajada. SymSrv descomprimirá todos los archivos antes de copiarlos en el almacén de bajada.

## <a name="deleting-the-cache"></a>Eliminar la memoria caché

Si usa un almacén de bajada como caché, puede eliminar este directorio en cualquier momento para ahorrar espacio en disco.

Es posible tener un almacén de símbolos VAST que incluya archivos de símbolos para muchos programas o versiones de Windows diferentes. Si actualiza la versión de Windows que se usa en el equipo de destino, los archivos de símbolos almacenados en caché coincidirán con la versión anterior. Estos archivos en caché no tendrán ningún otro uso y, por lo tanto, podría ser un buen momento para eliminar la memoria caché.

Herramientas de depuración para Windows incluye una utilidad llamada agestore.exe que quitará selectivamente los archivos de un árbol de directorios y dejará los archivos usados más recientemente. Esta herramienta está diseñada para la eliminación de archivos no usados de almacenes de servidores de símbolos. Permite controlar muchas opciones, entre las que se incluyen los algoritmos de tamaño reducido de fecha y de tamaño de directorio.

## <a name="flat-cache-directory"></a>Directorio de caché plana

Es posible declarar el almacén de bajada predeterminado como un directorio plano, en lugar de una estructura de árbol de símbolos estándar. Para ello, llame a la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con **el \_ \_ directorio plano SYMOPT** (esto también establece la opción de **\_ \_ \_ almacenamiento predeterminado plana SSRVOPT** en SymSrv). Asegúrese de llamar a [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) antes de hacerlo; de lo contrario, los archivos de símbolos se pueden escribir en el directorio del programa.

## <a name="pointer-files"></a>Archivos de puntero

SymStore puede crear y usar archivos que apuntan a un archivo de destino en lugar del propio archivo de destino. Si un almacén de símbolos contiene un archivo de puntero de este tipo, el valor predeterminado es copiar el archivo de la ubicación indicada en el archivo de puntero en el almacén. Para configurar un almacén de modo que se copie el archivo de puntero en lugar del archivo al que apunta, cree un archivo denominado wantsptr.txt en la raíz del almacén de destino. El contenido de wantsptr.txt no es importante, solo la presencia del archivo.

## <a name="excluding-files-from-symbols-list"></a>Excluir archivos de la lista de símbolos

Para excluir archivos de una búsqueda de símbolos, puede especificar sus nombres en symsrv.ini o en el registro. Para especificar los archivos de symsrv.ini, cree una sección denominada exclusiones y enumere los archivos. Los nombres de archivo pueden contener caracteres comodín, como se muestra en el ejemplo siguiente:

``` syntax
[Exclusions]
dbghelp.pdb
symsrv.*
mso*
```

Symsrv.ini debe encontrarse en el mismo directorio en el que reside symsrv.dll. En la mayoría de las instalaciones, el archivo no existe y tendrá que crear uno nuevo.

Como alternativa, puede almacenar los archivos que se van a excluir en el registro. Cree la siguiente clave del registro: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Symbol Server \\ exclusiones**. Almacene cada nombre de archivo como un valor de cadena (REG \_ SZ) dentro de esta clave. El nombre del valor de cadena especifica el nombre del archivo que se va a excluir. Puede usar el contenido del valor de cadena para almacenar un comentario que describa por qué se excluye el archivo.

## <a name="installation"></a>Instalación

El servidor de símbolos SymSrv (symsrv.dll) se incluye en el paquete de herramientas de depuración para Windows. Debe estar instalado en el mismo directorio que la copia de dbghelp.dll que está cargando. Para obtener más información, consulte [llamar a la biblioteca DbgHelp](calling-the-dbghelp-library.md).

 

 



