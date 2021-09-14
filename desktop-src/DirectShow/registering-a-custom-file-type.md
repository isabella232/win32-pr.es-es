---
description: En este artículo se describe cómo el Administrador de Graph busca un filtro de origen, dado un nombre de archivo.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Registro de un tipo de archivo personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246435"
---
# <a name="registering-a-custom-file-type"></a>Registro de un tipo de archivo personalizado

En este artículo se describe cómo el Administrador de Graph busca un filtro de origen, dado un nombre de archivo. Puede usar este mecanismo para registrar sus propios tipos de archivo personalizados. Una vez registrado el tipo de archivo, DirectShow cargará automáticamente el filtro de origen correcto cada vez que una aplicación llame a [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

-   [Información general](#overview)
-   [Protocolos](#protocols)
-   [Extensiones de archivo](#file-extensions)
-   [Comprobar bytes](#check-bytes)
-   [Carga del filtro de origen](#loading-the-source-filter)
-   [Tipos de archivo personalizados en Reproductor de Windows Media](#custom-file-types-in-windows-media-player)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Para buscar un filtro de origen a partir de un nombre de archivo determinado, el Administrador de Graph intenta hacer lo siguiente, en orden:

1.  Coincide con el protocolo, si lo hay.
2.  Coincide con la extensión de archivo.
3.  Coincidencia de patrones de bytes dentro del archivo, *denominados bytes de comprobación*.

## <a name="protocols"></a>Protocolos

Los nombres de protocolo como "ftp" o "http" se registran en el

**RAÍZ DE CLASES HKEY \_ \_**

key, con la siguiente estructura:


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



Si el nombre de archivo o la dirección URL contienen dos puntos (':'), el Administrador de filtros Graph intenta usar la parte anterior a ':' como nombre de protocolo. Por ejemplo, si el nombre es "myprot://myfile.ext", busca una clave del Registro denominada **myprot**. Si esta clave existe y contiene una subclave denominada "Extensiones", el Administrador de filtros de Graph Busca dentro de esa subclave las entradas que coinciden con la extensión de archivo. El valor de la clave debe ser un GUID en forma de cadena; por ejemplo, " {00000000-0000-0000-0000-000000000000} ". Si el Administrador de Graph no puede  coincidir con nada dentro de la subclave Extensiones, busca una subclave denominada Filtro de origen **,** que también debe ser un GUID en forma de cadena.

Si filter Graph Manager encuentra un GUID correspondiente, lo usa como CLSID del filtro de origen e intenta cargar el filtro. Si no encuentra una coincidencia, usa el filtro Origen de [archivo (URL),](file-source--url--filter.md) que trata el nombre de archivo como una dirección URL.

Hay dos excepciones a este algoritmo:

-   Para excluir las letras del controlador, las cadenas de un solo carácter no se consideran protocolos.
-   Si la cadena es "file:" o "file://", no se trata como un protocolo.

## <a name="file-extensions"></a>Extensiones de archivo

Si no hay ningún protocolo en el nombre de archivo, el Administrador de filtros Graph busca en el Registro entradas con la clave **HKEY \_ CLASSES ROOT Media \_ Type \\ \\ Extensions \\**.*ext* \\ , donde .*ext* es la extensión de archivo. Si esta clave existe, el valor **Filtro de origen** contiene el CLSID del filtro de origen, en forma de cadena. Opcionalmente, la clave puede tener valores para **Tipo de** medio y **Subtipo**, que dan los GUID de tipo principal y subtipo.

## <a name="check-bytes"></a>Comprobar bytes

Algunos tipos de archivo se pueden identificar mediante patrones específicos de bits que se producen en desplazamientos de bytes específicos en el archivo. El Administrador Graph filtros busca claves en el Registro con el formato siguiente:

**HKEY \_ CLASSES \_ ROOT \\ MediaType \\**{ tipo *principal* } \\ { *subtipo* }

donde *el tipo principal* y el *subtipo* son GUID que definen el tipo de medio para la secuencia de bytes. Cada clave contiene una o varias subclaves, normalmente denominadas 1, 2, etc., que definen los bytes de comprobación. y una subclave denominada **Filtro de origen** que proporciona el CLSID del filtro de origen, en forma de cadena. Las subclaves check-byte son cadenas que contienen uno o varios cuadrántos de números denominados:

*offset*, *cb*, *mask*, *val*

Para que coincida con el archivo, el Administrador de Graph lee cb bytes, empezando por el desplazamiento del número de bytes. A continuación, realiza una operación AND bit a bit con el valor de mask. Si el resultado es igual a val, el archivo es una coincidencia para ese cuadráng. Los valores mask y val se dan en hexadecimal. Una entrada en blanco para mask se trata como una cadena de 1s de longitud cb. Un valor negativo para offset indica un desplazamiento desde el final del archivo. Para que coincida con la clave, el archivo debe coincidir con todos los quads de cualquiera de las subclaves.

Por ejemplo, suponga que el registro contiene las siguientes claves en HKCR Media Type (Tipo **de medio \\ HKCR):**


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



La primera clave corresponde al tipo principal MediaTYPE \_ Stream. La subclave siguiente que corresponde al subtipo MEDIATYPE \_ Midi. El valor de la subclave Filtro de origen es CLSID \_ AsyncReader, el CLSID del filtro de origen de archivo [(Async).](file-source--async--filter.md)

Cada entrada puede tener varios valores. todos ellos deben coincidir. En el ejemplo siguiente, los primeros 4 bytes del archivo deben ser 0xAB, 0xCD, 0x12, 0x34; y los últimos 4 bytes del archivo deben 0xAB, 0xAB, 0x00, 0xAB:


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



Además, puede haber varias entradas enumeradas en un único tipo de medio. Una coincidencia con cualquiera de ellas es suficiente. Este esquema permite un conjunto de máscaras alternativas; por ejemplo, archivos .wav que podrían tener o no un encabezado RIFF.

> [!Note]  
> Este esquema es similar al utilizado por la [**función GetClassFile.**](/windows/win32/api/objbase/nf-objbase-getclassfile)

 

## <a name="loading-the-source-filter"></a>Carga del filtro de origen

Suponiendo que filter Graph Manager encuentra un filtro de origen correspondiente para el archivo, agrega ese filtro al gráfico, consulta el filtro para la interfaz [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) y llama a [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load). Los argumentos del **método Load** son el nombre de archivo y el tipo de medio, según se determina en el Registro.

Si el Administrador de Graph no encuentra nada en el Registro, el valor predeterminado es usar el filtro Origen de archivo asincrónico. En ese caso, establece el tipo de medio en **MediaTYPE \_ Stream**, **MEDIASUBTYPE \_ None**.

## <a name="custom-file-types-in-windows-media-player"></a>Tipos de archivo personalizados en Reproductor de Windows Media

Reproductor de Windows Media usa un conjunto adicional de entradas del Registro. Para obtener más información, vea [File Name Extension Registry Configuración](../wmp/file-name-extension-registry-settings.md) en el SDK Reproductor de Windows Media.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 
