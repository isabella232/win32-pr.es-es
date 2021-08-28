---
description: Comprenda cómo usar el argumento CRUMB en Windows Search como medio de controlar el ámbito de una búsqueda.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argumento CRUMB (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a1ae426881473a631a11b40ec8e567f600daa4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886830"
---
# <a name="crumb-argument-windows-search"></a>Argumento CRUMB (Windows Search)

El argumento admite instrucciones de sintaxis de consulta avanzada (AQS) completa y es especialmente útil como medio para controlar el `crumb` ámbito de una búsqueda. Además de los valores de AQS, el argumento puede tomar un parámetro especial en Windows Vista y los parámetros y en XP, como se describe más adelante en `crumb` `location` este `kind` `store` tema.

Este tema se organiza de la siguiente manera:

-   [Sintaxis de miga](#crumb-syntax)
    -   [Ejemplos generales](#general-examples)
-   [Uso de miga con Vista (ubicación)](#using-crumb-with-vista-location)
    -   [Ejemplos de Vista](#vista-examples)
    -   [Constantes para carpetas comunes](#constants-for-common-folders)
-   [Uso de miga con Windows XP (tipo y almacén)](#using-crumb-with-windows-xp-kind-and-store)
    -   [Ejemplos de XP](#xp-examples)
-   [Temas relacionados](#related-topics)

 

## <a name="crumb-syntax"></a>Sintaxis de miga

La sintaxis de la miga es la siguiente:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



La parte de columna es cualquier propiedad del sistema de propiedades y la parte &lt; de valor es un valor válido para esa &gt; &lt; &gt; propiedad. La <label> parte es un alias opcional para la propiedad que se muestra como una sugerencia de interfaz de usuario.

### <a name="general-examples"></a>Ejemplos generales


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>Uso de miga con Vista (ubicación)

En el parámetro crumb, Windows Vista admite AQS completo y también la propiedad , que tiene una implementación especial disponible solo `location` en Windows Vista. Puede usar una cadena de AQS o la propiedad `location` dentro de un único parámetro crumb, pero no ambos. Si el parámetro crumb incluye AQS, se omite todo lo demás de ese parámetro de miga.

La `location` propiedad permite especificar una ruta de acceso para buscar. Windows Vista puede omitir el indexador y atravesar el directorio directamente si la ubicación está fuera del ámbito de rastreo del indexador. Por lo tanto, estas búsquedas pueden ser más lentas que las búsquedas que usan el indexador.

Cuando se especifica una `location` propiedad, se admiten dos parámetros adicionales y opcionales:



| Parámetro | Valores                  | Descripción                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inserción | include, exclude        | Especifica si la consulta debe incluir o excluir elementos de esa ruta de acceso. "Include" es el valor predeterminado. Windows Vista no admite exclusiones sin inclusiones. (Vea el ejemplo) |
| recursión | recursiva, no recursiva | Especifica si la búsqueda debe repetir todas las subcarpetas a partir del valor definido en la ubicación: &lt; valor &gt; . "Recursive" es el valor predeterminado.                             |



 

Para el ámbito de una búsqueda mediante el protocolo search-ms:, tiene distintas opciones en función del destino del ámbito.

Carpeta en un equipo local:

-   Usar AQS (crumb=folder:<ruta de acceso con codificación URL>)
-   Use el argumento location (crumb=location:<ruta de acceso codificada en URL>)

Carpeta en una máquina o red remota:

-   Use el argumento location (crumb=location:<ruta de acceso codificada en URL>)

Carpeta a la que se accede a través de un controlador de protocolo UNC conocido:

-   Use AQS (crumb=store: <UNC protocol handler name> )
-   Use el argumento location (crumb=location:<ruta de acceso codificada en URL>)

### <a name="vista-examples"></a>Ejemplos de Vista


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



En el primer ejemplo se ejecuta una búsqueda de "vacaciones" a partir de la ubicación shell://Personal (un acceso directo especial a la carpeta Mis documentos del usuario), incluida esa carpeta y todas las subcarpetas. Consulte la tabla siguiente.

En el segundo ejemplo se ejecuta una búsqueda en C: \\ Imágenes, pero no en C: \\ Imágenes \\ duplicadas.

En el tercer ejemplo se ejecuta una búsqueda en C: Documentos, limitada a archivos con la \\ propiedad kind establecida en imágenes.

### <a name="constants-for-common-folders"></a>Constantes para carpetas comunes

Windows Vista permite el uso de valores [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) que proporcionan una manera única independiente del sistema de identificar carpetas especiales usadas con frecuencia por las aplicaciones, pero que pueden no tener el mismo nombre o ubicación en un sistema determinado. Por ejemplo, la carpeta del sistema puede ser "C: Windows" en un sistema y \\ "C: \\ Winnt" en otro. Antes de Windows Vista, [se usaban los CSIDL.](/windows/desktop/shell/csidl)

Use estas ubicaciones con esta sintaxis:


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>Uso de miga con Windows XP (tipo y almacén)

Por Windows search en Windows XP (WDS 3.x), los términos "kind" y "store" de AQS tienen una implementación especial. Los valores "kind" son los mismos [que se usan en WDS 2.x.](../lwef/-search-2x-wds-perceivedtype.md) Los valores de "store" incluyen lo siguiente:

-   Mapi
-   archivo
-   outlookexpress
-   cualquiera

### <a name="xp-examples"></a>Ejemplos de XP


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



En el primer ejemplo se devuelven Outlook express de Microsoft de John con la etiqueta personalizada "Correo electrónico de OE". En el segundo ejemplo se ejecuta una búsqueda de cualquier comunicación de John.

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

[ARGUMENTO SUBQUERY](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
