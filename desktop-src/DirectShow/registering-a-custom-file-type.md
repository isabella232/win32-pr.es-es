---
description: En este artículo se describe cómo el administrador de gráficos de filtro localiza un filtro de origen, dado un nombre de archivo.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Registro de un tipo de archivo personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677092"
---
# <a name="registering-a-custom-file-type"></a>Registro de un tipo de archivo personalizado

En este artículo se describe cómo el administrador de gráficos de filtro localiza un filtro de origen, dado un nombre de archivo. Puede usar este mecanismo para registrar sus propios tipos de archivo personalizados. Una vez registrado el tipo de archivo, DirectShow cargará automáticamente el filtro de origen correcto cada vez que una aplicación llame a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

-   [Información general](#overview)
-   [Protocolos](#protocols)
-   [Extensiones de archivo](#file-extensions)
-   [Comprobar bytes](#check-bytes)
-   [Cargar el filtro de origen](#loading-the-source-filter)
-   [Tipos de archivo personalizados en Windows Media Player](#custom-file-types-in-windows-media-player)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Para buscar un filtro de origen a partir de un nombre de archivo determinado, el administrador de gráficos de filtros intenta hacer lo siguiente, en orden:

1.  Coincide con el protocolo, si existe.
2.  Coincide con la extensión de archivo.
3.  Coincide con patrones de bytes dentro del archivo, denominado *check bytes*.

## <a name="protocols"></a>Protocolos

Los nombres de protocolo como "FTP" o "http" se registran en el

**\_clase HKEY \_ raíz**

clave, con la siguiente estructura:


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



Si el nombre de archivo o la dirección URL contienen dos puntos (': '), el administrador de gráficos de filtros intenta usar la parte anterior a ': ' como nombre de protocolo. Por ejemplo, si el nombre es "myprot://myfile.ext", busca una clave del **registro denominada me**. Si esta clave existe y contiene una subclave denominada "Extensions", el administrador de gráficos de filtro busca en esa subclave las entradas que coinciden con la extensión de archivo. El valor de la clave debe ser un GUID en formato de cadena. por ejemplo, " {00000000-0000-0000-0000-000000000000} ". Si Filter Graph Manager no puede coincidir con nada de la subclave **extensions** , busca una subclave denominada **filtro de origen**, que también debe ser un GUID en formato de cadena.

Si el administrador de gráficos de filtro encuentra un GUID coincidente, lo usa como CLSID del filtro de origen e intenta cargar el filtro. Si no encuentra ninguna coincidencia, utiliza el filtro de [origen de archivo (URL)](file-source--url--filter.md) , que trata el nombre de archivo como una dirección URL.

Hay dos excepciones a este algoritmo:

-   Para excluir Letras de controlador, las cadenas de un solo carácter no se consideran protocolos.
-   Si la cadena es "File:" o "file://", no se trata como un protocolo.

## <a name="file-extensions"></a>Extensiones de archivo

Si no hay ningún protocolo en el nombre de archivo, el administrador de gráficos de filtro busca en el registro entradas con **las \_ \_ \\ \\ extensiones \\ de tipo de medio raíz de las clases HKEY** de clave.*EXT* \\ , donde.*EXT* es la extensión de archivo. Si esta clave existe, el **filtro de origen** del valor contiene el CLSID del filtro de origen, en forma de cadena. Opcionalmente, la clave puede tener valores para el **tipo de medio** y el **subtipo**, que proporcionan los GUID de tipo y subtipo principales.

## <a name="check-bytes"></a>Comprobar bytes

Algunos tipos de archivo se pueden identificar mediante patrones específicos de bits que se producen en determinados desplazamientos de bytes en el archivo. Filter Graph Manager busca claves con el siguiente formato en el registro:

**HKEY \_ Clases \_ \\ mediatype \\ raíz**{ *tipo principal* } \\ { *SubType* }

donde *major Type* y *SubType* son GUID que definen el tipo de medio para la secuencia de bytes. Cada clave contiene una o más subclaves, normalmente denominadas 1, 2, etc., que definen los bytes de comprobación; y una subclave denominada **filtro de origen** que proporciona el CLSID del filtro de origen, en forma de cadena. Las subclaves check-byte son cadenas que contienen uno o más cuádruples de números denominados:

*offset*, *CB*, *Mask*, *Val*

Para que coincida con el archivo, el administrador de gráficos de filtro Lee los bytes CB, empezando por el desplazamiento del número de bytes. A continuación, realiza una operación and bit a bit con el valor de Mask. Si el resultado es igual a Val, el archivo es una coincidencia para ese cuádruple. Los valores Mask y Val se proporcionan en hexadecimal. Una entrada en blanco para Mask se trata como una cadena de 1s de longitud CB. Un valor negativo para PosiciónInicial indica un desplazamiento desde el final del archivo. Para que coincida con la clave, el archivo debe coincidir con todas las cuádruples de cualquiera de las subclaves.

Por ejemplo, supongamos que el registro contiene las siguientes claves en el **\\ tipo de medio HKCR**:


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



La primera clave corresponde a la secuencia de tipo MEDIATYPE principal \_ . La subclave siguiente que corresponde al subtipo MEDIATYPE \_ MIDI. El valor de la subclave de filtro de origen es CLSID \_ AsyncReader, el CLSID del filtro de [origen de archivo (Async)](file-source--async--filter.md) .

Cada entrada puede tener varios cuadruplican; todos ellos deben coincidir. En el ejemplo siguiente, los cuatro primeros bytes del archivo deben ser 0xAB, 0xCD, 0X12, 0x34; y los últimos 4 bytes del archivo deben ser 0xAB, 0xAB, 0x00, 0xAB:


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



Además, puede haber varias entradas enumeradas bajo un solo tipo de medio. Es suficiente una coincidencia con cualquiera de ellas. Este esquema permite un conjunto de máscaras alternativas; por ejemplo, archivos. wav que pueden tener o no un encabezado RIFF.

> [!Note]  
> Este esquema es similar al utilizado por la función [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) .

 

## <a name="loading-the-source-filter"></a>Cargar el filtro de origen

Suponiendo que el administrador de gráficos de filtro encuentra un filtro de origen coincidente para el archivo, agrega ese filtro al gráfico, consulta el filtro para la interfaz [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) y llama a [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load). Los argumentos para el método **Load** son el nombre de archivo y el tipo de medio, tal y como se determina en el registro.

Si el administrador de gráficos de filtro no encuentra nada en el registro, se usa de forma predeterminada el filtro de origen de archivo asincrónico. En ese caso, establece el tipo de medio en **\_ flujo de MEDIATYPE**, **MEDIASUBTYPE \_ ninguno**.

## <a name="custom-file-types-in-windows-media-player"></a>Tipos de archivo personalizados en Windows Media Player

Windows Media Player usa un conjunto adicional de entradas del registro. Para obtener más información, consulte [configuración del registro](../wmp/file-name-extension-registry-settings.md) de la extensión de nombre de archivo en el SDK de Windows Media Player.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 
