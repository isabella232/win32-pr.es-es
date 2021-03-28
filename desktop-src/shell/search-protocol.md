---
description: 'La búsqueda: el protocolo de aplicación es una Convención extensible para llamar a la aplicación de búsqueda en el escritorio en Windows Vista con Service Pack 1 (SP1) y versiones posteriores.'
title: Usar el protocolo de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997881"
---
# <a name="using-the-search-protocol"></a>Usar el protocolo de búsqueda

La **búsqueda:** el [Protocolo de aplicación](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) es una Convención extensible para llamar a la aplicación de búsqueda en el escritorio en Windows Vista con Service Pack 1 (SP1) y versiones posteriores. El protocolo se creó en Windows Vista con SP1 (para obtener información, consulte el artículo [de Knowledge Base información general sobre los cambios de Windows Vista Desktop Search en Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) para proporcionar a Windows una forma de determinar y llamar a la aplicación de búsqueda de escritorio predeterminada.

La sintaxis del protocolo proporciona una serie de parámetros útiles para realizar búsquedas de escritorio comunes, como los términos de búsqueda especificados por el usuario o la ubicación en la que se inició la búsqueda. Cuando los usuarios buscan desde uno de los dos puntos de entrada de búsqueda disponibles (el menú **Inicio** o el explorador de Windows), el sistema operativo usa el protocolo de búsqueda para iniciar la aplicación de búsqueda en el escritorio predeterminada. Para ello, se agregan los términos de búsqueda especificados por el usuario a la sintaxis del Protocolo de búsqueda estándar y se pasa esa información a la aplicación registrada como aplicación de búsqueda predeterminada.

Si no se instala ninguna otra aplicación de búsqueda en el escritorio, una búsqueda introducida en estos puntos de entrada inicia el explorador de Windows Search. Sin embargo, los desarrolladores de terceros pueden crear, instalar y registrar sus aplicaciones para administrar el protocolo de búsqueda y ser la aplicación de búsqueda predeterminada. Dichas aplicaciones deben admitir la sintaxis del Protocolo de búsqueda y registrarse con la característica [programas predeterminados](default-programs.md) para garantizar una experiencia sin problemas con Windows.

Si desarrolla una aplicación pensada para usarse o basarse en una aplicación de búsqueda de escritorio específica, no debe depender exclusivamente de la **búsqueda:** el protocolo. Dado que muchas aplicaciones podrían poseer el protocolo **Search:** , no hay ninguna garantía de que la aplicación de búsqueda de escritorio de destino la posea en un momento dado. En su lugar, debe usar un protocolo de búsqueda privado definido por esa aplicación de búsqueda de escritorio de destino. Esto significa que las aplicaciones de búsqueda en el escritorio destinadas a ser una plataforma para aplicaciones de terceros deben admitir el protocolo **Search:** y su propio protocolo de búsqueda de propiedad.

> [!Note]  
> El protocolo **Search:** no reemplaza el propietario [Search-MS:](../search/-search-3x-wds-qryidx-searchms.md) Protocol. Las aplicaciones pueden seguir usando la **búsqueda-MS:** protocolo para iniciar el explorador de búsqueda de ventanas o para consultar el indizador de Windows Search de forma silenciosa.

 

En este tema se trata lo siguiente:

-   [Sintaxis](#syntax)
-   [Windows Vista con SP1 uso de la búsqueda: Protocolo](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [Ejemplos](#examples)
-   [Registro de la aplicación que controla el protocolo](#registering-the-application-that-handles-the-protocol)
    -   [Entradas del registro](#registry-entries)
-   [Temas relacionados](#related-topics)

## <a name="syntax"></a>Sintaxis

El protocolo de búsqueda usa la siguiente sintaxis codificada como dirección URL estándar:


```C++
search:parameter=value[&parameter=value]&
```



La sintaxis comienza por identificar el protocolo en sí (**Buscar:**). Los pares de parámetro/valor son argumentos pasados al motor de búsqueda, como se describe en la tabla siguiente, que muestra todos los parámetros posibles para la sintaxis del Protocolo de búsqueda.



| Parámetro                                              | Value                                                         | Descripción                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Query                                                  | Texto con codificación URL                                              | Texto de la consulta escrito por el usuario.                                                                                                                                                                                                                                                            |
| [inputlocale](search-protocol-localeidentifiers.md)   | Cualquier identificador de código de idioma (LCID) válido                     | LCID que identifica el idioma de entrada de la consulta.                                                                                                                                                                                                                                     |
| [keywordlocale](search-protocol-localeidentifiers.md) | Cualquier LCID válido                                                | LCID que identifica el idioma de la versión internacional del indexador. El valor predeterminado es 1033 (en-US).                                                                                                                                                                                |
| [rutas](search-protocol-crumb.md)                     | AQS (instrucción)                                                 | Este argumento restringe el ámbito en el que se busca. En Windows Vista, el protocolo de búsqueda admite AQS completo, así como una implementación especial para un `location` argumento. En Windows XP, el protocolo de búsqueda también admite AQS completo, salvo una implementación especial de `kind` y `store` . |
| [sintáctica](search-protocol-syntaxargument.md)           | NQS, AQS (no distingue mayúsculas de minúsculas)                                 | Sintaxis de consulta que se va a usar para buscar en el índice: sintaxis de consulta natural o sintaxis de consulta avanzada (AQS). AQS es el valor predeterminado y siempre se asume que se analiza y se admite.                                                                                                                        |
| [stackedby](search-protocol-stackedby.md)             | Cualquier propiedad válida del sistema de propiedades                   | Propiedad que especifica la columna por la que se van a apilar los resultados.                                                                                                                                                                                                                                      |
| [subquery](search-protocol-subquery.md)               | Una ruta de acceso completa para un archivo de búsqueda guardado ( \* . Search-MS) | Los resultados de la subconsulta se utilizan como el origen de la consulta. Es decir, se busca en los términos de la consulta con los resultados de la subconsulta.                                                                                                                                               |
| displayname                                            | Cadena con codificación URL                                            | Nombre de la búsqueda actual.                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a>Windows Vista con SP1 uso de la búsqueda: Protocolo

Windows Vista con SP1 tiene varios puntos de entrada desde los que llama a **Search:** Protocol. Estos puntos de entrada se describen a continuación, así como la sintaxis común asociada a cada uno de ellos.



| Punto de entrada del Protocolo de búsqueda | Ubicación         | Consulta llamada                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| **Buscar en todas partes**       | Menú **Inicio**   | buscar: consulta = *término de búsqueda*<>                                   |
| **Buscar en todas partes**       | Explorador de Windows | buscar: consulta =<*término de búsqueda*>&en la ubicación: <*Ubicación*> |
| Tecla del logotipo de Windows+F          | En cualquier lugar         | buscan                                                              |
| CTRL+F                      | Explorador de Windows | buscar: consulta =<*término de búsqueda*>&en la ubicación: <*Ubicación*> |
| F3                          | Menú **Inicio**   | buscan                                                              |
| F3                          | Explorador de Windows | buscar: consulta =<*término de búsqueda*>&en la ubicación: <*Ubicación*> |



 

Los puntos de entrada del Protocolo de búsqueda de Windows Vista con SP1 no aprovechan todos los parámetros posibles del Protocolo de búsqueda. Las aplicaciones que solo se preocupan por la administración de llamadas del Protocolo de búsqueda desde Windows Vista con SP1 pueden utilizar la tabla siguiente como guía del mínimo necesario para implementar.



| Parámetro                                              | ¿Lo usa Windows? | Cómo Windows Vista con SP1 lo utiliza al llamar a Search:                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Query                                                  | Sí              | Texto de la consulta escrito por el usuario.                                                                                                                                                                                                                                         |
| [rutas](search-protocol-crumb.md)                     | Sí              | [migas](search-protocol-crumb.md) de uso del `location` argumento para especificar el origen de la consulta.                                                                                                                                                                       |
| [subquery](search-protocol-subquery.md)               | Sí              | Los resultados del argumento de la [subconsulta](search-protocol-subquery.md) se utilizan como el ámbito de los elementos que se van a buscar. Esto se suele usar si un usuario usaba un archivo. Search-ms para buscar y, a continuación, se llama a la aplicación de búsqueda de escritorio predeterminada desde dentro de esa búsqueda. |
| [inputlocale](search-protocol-localeidentifiers.md)   | No               | No se usa actualmente.                                                                                                                                                                                                                                                         |
| [keywordlocale](search-protocol-localeidentifiers.md) | No               | No se usa actualmente.                                                                                                                                                                                                                                                         |
| [sintáctica](search-protocol-syntaxargument.md)           | No               | No se usa actualmente.                                                                                                                                                                                                                                                         |
| [stackedby](search-protocol-stackedby.md)             | No               | No se usa actualmente.                                                                                                                                                                                                                                                         |
| displayname                                            | No               | No se usa actualmente.                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a>Ejemplos

Si un usuario escribe "Microsoft" en el menú **Inicio** y hace clic en **Buscar en todas partes**, se realiza la llamada del Protocolo de búsqueda resultante:


```C++
search:query=microsoft&
```



Si un usuario escribe "Seattle" en el explorador de Windows en C: \\ carpeta y, a continuación, hace clic en **Buscar en todas partes**, se realiza la siguiente llamada, usando caracteres de escape para ': ' y ' \\ ':


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a>Registro de la aplicación que controla el protocolo

Dado que varias aplicaciones pueden competir por el protocolo de búsqueda, debe registrar la aplicación con la característica [programas predeterminados](default-programs.md) durante la instalación para permitir que el usuario configure el valor predeterminado más fácilmente. Además de los procedimientos de instalación que se suelen realizar en Windows XP, una aplicación basada en Windows Vista debe registrarse con la característica programas predeterminados para que la aplicación y los usuarios puedan configurar los valores predeterminados sin problemas.

Después de instalar los archivos binarios necesarios en el equipo del usuario, la rutina de instalación debe completar estas tareas generales:

1.  Escriba los ProgID en **el \_ \_ equipo local HKEY**, tal como se describe a continuación. Tenga en cuenta que las aplicaciones deben crear ProgID específicos de la aplicación para el protocolo de búsqueda.
2.  Notificar Asociación del Protocolo de búsqueda en el nivel de equipo.
3.  Registre la aplicación con los [programas predeterminados](default-programs.md), como se explica en [registrar una aplicación para su uso con programas predeterminados](default-programs.md), como un complemento para el protocolo de búsqueda.

### <a name="registry-entries"></a>Entradas del Registro

A continuación se muestran ejemplos de las entradas del registro necesarias para una aplicación de búsqueda de escritorio ficticia, contoso Search.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de consulta avanzada](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[Programas predeterminados](default-programs.md)
</dt> </dl>

 

 
