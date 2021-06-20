---
description: Comprenda cómo usar el argumento CRUMB en Windows Search para controlar el ámbito de una búsqueda.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argumento CRUMB (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f56287c7182c0cf370250d53075a1c951ddf28b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403738"
---
# <a name="crumb-argument-windows-search"></a>Argumento CRUMB (Windows Search)

El argumento admite instrucciones de sintaxis de consulta avanzada (AQS) completa y es especialmente útil como medio de controlar el `crumb` ámbito de una búsqueda. Además de los argumentos de AQS, el argumento puede tomar un parámetro especial en Windows Vista y los parámetros y en XP, como se describe más `crumb` `location` adelante en este `kind` `store` tema.

Este tema se organiza de la siguiente manera:

-   [Sintaxis de crumb](#crumb-syntax)
    -   [Ejemplos generales](#general-examples)
-   [Uso de crumb con Vista (ubicación)](#using-crumb-with-vista-location)
    -   [Ejemplos de Vista](#vista-examples)
    -   [Constantes para carpetas comunes](#constants-for-common-folders)
-   [Uso de crumb con Windows XP (tipo y tienda)](#using-crumb-with-windows-xp-kind-and-store)
    -   [Ejemplos de XP](#xp-examples)
-   [Temas relacionados](#related-topics)

 

## <a name="crumb-syntax"></a>Sintaxis de crumb

La sintaxis crumb es la siguiente:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



La <column> parte es cualquier propiedad del sistema de propiedades y <value> portion es un valor válido para esa propiedad. La <label> parte es un alias opcional para la propiedad que se muestra como una sugerencia de interfaz de usuario.

### <a name="general-examples"></a>Ejemplos generales


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>Uso de crumb con Vista (ubicación)

En el parámetro crumb, Windows Vista admite AQS completo y también la propiedad , que tiene una implementación especial `location` disponible solo en Windows Vista. Puede usar una cadena de AQS o la propiedad dentro `location` de un único parámetro crumb, pero no ambos. Si el parámetro crumb incluye AQS, se omite todo lo demás en ese parámetro crumb.

La `location` propiedad permite especificar una ruta de acceso para buscar. Windows Vista puede omitir el indexador y recorrer el directorio directamente si la ubicación está fuera del ámbito de rastreo del indexador. Por lo tanto, estas búsquedas pueden ser más lentas que las búsquedas que usan el indexador.

Al especificar una `location` propiedad, se admiten dos parámetros adicionales y opcionales:



| Parámetro | Valores                  | Descripción                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inserción | include, exclude        | Especifica si la consulta debe incluir o excluir elementos de esa ruta de acceso. "Include" es el valor predeterminado. Windows Vista no admite exclusiones sin inclusiones. (Vea el ejemplo) |
| recursión | recursiva, no recursiva | Especifica si la búsqueda debe repetir todas las subcarpetas a partir del valor definido en la ubicación:<value>. "Recursive" es el valor predeterminado.                             |



 

Para el ámbito de una búsqueda mediante el protocolo search-ms:, tiene diferentes opciones en función del destino del ámbito.

Carpeta en una máquina local:

-   Usar AQS (crumb=folder:<ruta de acceso con codificación URL>)
-   Uso del argumento location (crumb=location:<ruta de acceso codificada con dirección URL>)

Carpeta en una máquina o red remota:

-   Uso del argumento location (crumb=location:<ruta de acceso codificada con dirección URL>)

Carpeta a la que se accede a través de un controlador de protocolo UNC conocido:

-   Use AQS (crumb=store: <UNC protocol handler name> )
-   Uso del argumento location (crumb=location:<ruta de acceso codificada con dirección URL>)

### <a name="vista-examples"></a>Ejemplos de Vista


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



En el primer ejemplo se ejecuta una búsqueda de "vacaciones" a partir de la ubicación shell://Personal (un acceso directo especial a la carpeta Mis documentos del usuario), incluida esa carpeta y todas las subcarpetas. Consulte la tabla siguiente.

En el segundo ejemplo se ejecuta una búsqueda en C: \\ Imágenes, pero no en C: \\ Imágenes \\ duplicadas.

En el tercer ejemplo se ejecuta una búsqueda en C: Documentos, limitado a archivos con la propiedad \\ kind establecida en imágenes.

### <a name="constants-for-common-folders"></a>Constantes para carpetas comunes

Windows Vista permite el uso de valores [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) que proporcionan una manera única independiente del sistema de identificar las carpetas especiales usadas con frecuencia por las aplicaciones, pero que pueden no tener el mismo nombre o ubicación en un sistema determinado. Por ejemplo, la carpeta del sistema puede ser "C: Windows" en \\ un sistema y "C: \\ Winnt" en otro. Antes de Windows Vista, [se usaban los CSID.](/windows/desktop/shell/csidl)

Use estas ubicaciones con esta sintaxis:


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>Uso de crumb con Windows XP (tipo y tienda)

Por Windows Search en Windows XP (WDS 3.x), los términos "kind" y "store" de AQS tienen una implementación especial. Los valores "kind" son los mismos [que se usan en WDS 2.x.](../lwef/-search-2x-wds-perceivedtype.md) Entre los valores de "store" se incluyen los siguientes:

-   Mapi
-   archivo
-   outlookexpress
-   cualquiera

### <a name="xp-examples"></a>Ejemplos de XP


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



En el primer ejemplo se devuelven correos electrónicos de Microsoft Outlook Express de John con la etiqueta personalizada "Correo electrónico de E/S". En el segundo ejemplo se ejecuta una búsqueda de cualquier comunicación de John.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Parameter-Value argumentos](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argumentos del identificador de configuración regional](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argumento SYNTAX](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argumento SUBQUERY](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
