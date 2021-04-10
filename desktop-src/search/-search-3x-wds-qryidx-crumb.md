---
description: El argumento migas admite instrucciones completas de sintaxis de consulta avanzada (AQS) y es especialmente útil como medio para controlar el ámbito de una búsqueda.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argumento de MIGAs (búsqueda de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f36764174e0eecaedee4a9c360bb9d7dabca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153985"
---
# <a name="crumb-argument-windows-search"></a>Argumento de MIGAs (búsqueda de Windows)

El `crumb` argumento admite instrucciones completas de sintaxis de consulta avanzada (AQS) y es especialmente útil como medio para controlar el ámbito de una búsqueda. Además de AQS ements, el `crumb` argumento puede tomar un parámetro especial `location` en Windows Vista y `kind` `store` los parámetros de XP, tal y como se describe más adelante en este tema.

Este tema se organiza de la siguiente manera:

-   [Sintaxis de migas](#crumb-syntax)
    -   [Ejemplos generales](#general-examples)
-   [Uso de migas de vista (ubicación)](#using-crumb-with-vista-location)
    -   [Ejemplos de vista](#vista-examples)
    -   [Constantes para carpetas comunes](#constants-for-common-folders)
-   [Uso de migas de Windows XP (tipo y tienda)](#using-crumb-with-windows-xp-kind-and-store)
    -   [Ejemplos de XP](#xp-examples)
-   [Temas relacionados](#related-topics)

 

## <a name="crumb-syntax"></a>Sintaxis de migas

La sintaxis de las rutas de navegación es la siguiente:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



La <column> parte es cualquier propiedad del sistema de propiedades y el <value> la parte es un valor válido para esa propiedad. La <label> parte es un alias opcional para la propiedad que se muestra como una sugerencia de interfaz de usuario.

### <a name="general-examples"></a>Ejemplos generales


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>Uso de migas de vista (ubicación)

En el parámetro de rutas de acceso, Windows Vista admite AQS completo y también la `location` propiedad, que tiene una implementación especial disponible solo en Windows Vista. Puede usar una cadena AQS o la `location` propiedad dentro de un único parámetro de migas de línea, pero no ambos. Si el parámetro de migas incluye AQS, se omite todo lo demás en ese parámetro de migas de detalle.

La `location` propiedad permite especificar una ruta de acceso que se va a buscar. Windows Vista puede omitir el indexador y atravesar el directorio directamente si la ubicación está fuera del ámbito de rastreo del indexador. Por lo tanto, estas búsquedas pueden ser más lentas que las búsquedas que usan el indexador.

Cuando se especifica una `location` propiedad, se admiten dos parámetros adicionales y son opcionales:



| Parámetro | Valores                  | Descripción                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Introducción | incluir, excluir        | Especifica si la consulta debe incluir o excluir elementos de esa ruta de acceso. "Include" es el valor predeterminado. Windows Vista no admite exclusiones sin inclusiones. (Vea el ejemplo) |
| recursión | recursivo, no recursiva | Especifica si la búsqueda debe recurse todas las subcarpetas a partir del valor definido en la ubicación:<value>. "Recursive" es el valor predeterminado.                             |



 

Para establecer el ámbito de una búsqueda mediante el protocolo Search-MS:, tiene distintas opciones según el destino del ámbito.

En una máquina local:

-   Usar AQS (migas = carpeta: <ruta de acceso con codificación URL>)
-   Use el argumento de ubicación (migas de Ubicación: <ruta de acceso con codificación URL>)

Carpeta en un equipo o red remoto:

-   Use el argumento de ubicación (migas de Ubicación: <ruta de acceso con codificación URL>)

Carpeta a la que se tiene acceso a través de un controlador de protocolo UNC conocido:

-   Usar AQS (migas de la tienda: <UNC protocol handler name> )
-   Use el argumento de ubicación (migas de Ubicación: <ruta de acceso con codificación URL>)

### <a name="vista-examples"></a>Ejemplos de vista


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



En el primer ejemplo se ejecuta una búsqueda de "vacaciones" a partir de la ubicación shell://Personal (un acceso directo especial a la carpeta Mis documentos del usuario), incluida la carpeta y todas las subcarpetas. Consulte la tabla siguiente.

En el segundo ejemplo se ejecuta una búsqueda dentro de C: \\ Pictures, pero no en c: \\ imágenes \\ duplicadas.

En el tercer ejemplo se ejecuta una búsqueda en C: \\ Documents, limitada a los archivos con la propiedad Kind establecida en pics.

### <a name="constants-for-common-folders"></a>Constantes para carpetas comunes

Windows Vista permite el uso de valores [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) que proporcionan una manera única independiente del sistema para identificar carpetas especiales usadas con frecuencia por aplicaciones, pero que pueden no tener el mismo nombre o ubicación en ningún sistema determinado. Por ejemplo, la carpeta del sistema puede ser "C: \\ Windows" en un sistema y "c: \\ WinNT" en otro. Antes de Windows Vista, se usaban [CSIDLs](/windows/desktop/shell/csidl) .

Use estas ubicaciones con esta sintaxis:


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>Uso de migas de Windows XP (tipo y tienda)

En el caso de Windows Search en Windows XP (WDS 3. x), los términos de AQS "Kind" y "Store" tienen una implementación especial. Los valores "Kind" son los mismos que los que se [usan en WDS 2. x](../lwef/-search-2x-wds-perceivedtype.md). Los valores "Store" incluyen los siguientes:

-   interfaz
-   archivo
-   outlookexpress
-   cualquiera

### <a name="xp-examples"></a>Ejemplos de XP


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



En el primer ejemplo se devuelven mensajes de correo electrónico de Microsoft Outlook Express desde John con la etiqueta personalizada "OE Mail". En el segundo ejemplo se ejecuta una búsqueda de cualquier comunicación de John.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con argumentos de Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argumentos de identificador de configuración regional](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argumento de sintaxis](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argumento de subconsulta](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
