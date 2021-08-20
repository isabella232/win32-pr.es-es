---
description: 'La búsqueda: el protocolo de aplicación es una convención extensible para llamar a la aplicación de búsqueda de escritorio en Windows Vista con Service Pack 1 (SP1) y versiones posteriores.'
title: Uso del protocolo de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 47578ffe2ef6c26776a62a752c1034f17b5bfedaa17acdefba345d4927c94a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118048731"
---
# <a name="using-the-search-protocol"></a>Uso del protocolo de búsqueda

La **búsqueda: el** [protocolo de](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) aplicación es una convención extensible para llamar a la aplicación de búsqueda de escritorio en Windows Vista con Service Pack 1 (SP1) y versiones posteriores. El protocolo se creó en Windows Vista con SP1 Knowledge Base (para obtener información, consulte el artículo información general de la búsqueda de escritorio de Windows Vista en [Windows Vista Service Pack 1)](https://support.microsoft.com/kb/941946)para proporcionar a Windows una manera de determinar y llamar a la aplicación de búsqueda de escritorio predeterminada.

La sintaxis de protocolo proporciona una serie de parámetros útiles para realizar búsquedas de escritorio comunes, como los términos de búsqueda escritos por el usuario o la ubicación en la que se inició la búsqueda. Cuando los usuarios buscan en uno de los  dos puntos de entrada de búsqueda disponibles (el menú Inicio o Windows Explorer), el sistema operativo usa el protocolo de búsqueda para iniciar la aplicación de búsqueda de escritorio predeterminada. Para ello, agrega los términos de búsqueda especificados por el usuario a la sintaxis del protocolo de búsqueda estándar y pasa esa información a la aplicación registrada como la aplicación de búsqueda predeterminada.

Si no hay ninguna otra aplicación de búsqueda de escritorio instalada, una búsqueda especificada en estos puntos de entrada inicia el explorador Windows Search. Sin embargo, los desarrolladores de terceros pueden crear, instalar y registrar sus aplicaciones para controlar el protocolo de búsqueda y ser la aplicación de búsqueda predeterminada. Estas aplicaciones deben admitir la sintaxis del protocolo de búsqueda y registrarse con la [característica Programas](default-programs.md) predeterminados para garantizar una experiencia sin problemas con Windows.

Si desarrolla una aplicación diseñada para usar o basar en una aplicación de búsqueda de escritorio específica, no debe depender exclusivamente de la **búsqueda:** protocolo. Dado que muchas aplicaciones podrían ser propietarias de la **búsqueda:** protocolo, no hay ninguna garantía de que la aplicación de búsqueda de escritorio de destino la poseerá en un momento dado. En su lugar, debe usar un protocolo de búsqueda privada definido por esa aplicación de búsqueda de escritorio de destino. Esto significa que las aplicaciones de búsqueda de escritorio diseñadas para ser una plataforma para aplicaciones de terceros deben admitir la **búsqueda:** el protocolo y su propio protocolo de búsqueda propietario.

> [!Note]  
> El **protocolo search:** no reemplaza el [protocolo search-ms:](../search/-search-3x-wds-qryidx-searchms.md) propietario. Las aplicaciones todavía pueden usar **el protocolo search-ms:** para iniciar el Explorador de búsqueda de ventanas o para consultar de forma silenciosa el Windows search.

 

En este tema se trata lo siguiente:

-   [Sintaxis](#syntax)
-   [Windows Vista con sp1 uso de la búsqueda: protocolo](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [Ejemplos](#examples)
-   [Registro de la aplicación que controla el protocolo](#registering-the-application-that-handles-the-protocol)
    -   [Entradas del Registro](#registry-entries)
-   [Temas relacionados](#related-topics)

## <a name="syntax"></a>Syntax

El protocolo de búsqueda usa la siguiente sintaxis con codificación URL estándar:


```C++
search:parameter=value[&parameter=value]&
```



La sintaxis comienza por identificar el propio protocolo **(búsqueda:**). Los pares parámetro-valor son argumentos pasados al motor de búsqueda, como se describe en la tabla siguiente, que muestra todos los parámetros posibles para la sintaxis del protocolo de búsqueda.



| Parámetro                                              | Valor                                                         | Descripción                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Query                                                  | Texto con codificación URL                                              | Texto de consulta escrito por el usuario.                                                                                                                                                                                                                                                            |
| [inputlocale](search-protocol-localeidentifiers.md)   | Cualquier identificador de código de idioma válido (LCID)                     | LCID que identifica el idioma de entrada de la consulta.                                                                                                                                                                                                                                     |
| [keywordlocale](search-protocol-localeidentifiers.md) | Cualquier LCID válido                                                | LCID que identifica el idioma de la versión internacional del indexador. El valor predeterminado es 1033 (en-us).                                                                                                                                                                                |
| [Miga](search-protocol-crumb.md)                     | Instrucción de AQS                                                 | Este argumento restringe el ámbito que se está buscando. En Windows Vista, el protocolo de búsqueda admite AQS completo, así como una implementación especial para un `location` argumento. En Windows XP, el protocolo de búsqueda también admite AQS completo, excepto para una implementación especial de `kind` y `store` . |
| [Sintaxis](search-protocol-syntaxargument.md)           | NQS, AQS (sin distingue mayúsculas de minúsculas)                                 | Sintaxis de consulta que se usará para buscar en el índice: Sintaxis de consulta natural o Sintaxis de consulta avanzada (AQS). AQS es el valor predeterminado y siempre se supone que se analiza y se admite.                                                                                                                        |
| [stackedby](search-protocol-stackedby.md)             | Cualquier propiedad válida del sistema de propiedades                   | Propiedad que especifica la columna por la que se apilan los resultados.                                                                                                                                                                                                                                      |
| [subquery](search-protocol-subquery.md)               | Ruta de acceso completa para un archivo de búsqueda guardada \* (.search-ms) | Los resultados de la subconsulta se usan como origen de la consulta. Es decir, se buscan los términos de consulta en los resultados de la subconsulta.                                                                                                                                               |
| displayname                                            | Cadena codificada en URL                                            | Nombre de la búsqueda actual.                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a>Windows Vista con sp1 uso de la búsqueda: protocolo

Windows Vista con SP1 tiene varios puntos de entrada desde los que llama a la **búsqueda:** protocolo. Estos puntos de entrada se describen a continuación, así como la sintaxis común asociada a cada uno de ellos.



| Punto de entrada del protocolo de búsqueda | Location         | Consulta a la que se llama                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| **Buscar en todas partes**       | **Menú** Inicio   | search:query=<*término de búsqueda*>                                   |
| **Buscar en todas partes**       | Explorador de Windows | search:query=<*término de* búsqueda>&crumb=location:<*LOCATION*> |
| Tecla del logotipo de Windows+F          | En cualquier lugar         | Búsqueda:                                                              |
| CTRL+F                      | Explorador de Windows | search:query=<*término de* búsqueda>&crumb=location:<*LOCATION*> |
| F3                          | **Menú** Inicio   | Búsqueda:                                                              |
| F3                          | Explorador de Windows | search:query=<*término de* búsqueda>&crumb=location:<*LOCATION*> |



 

Los Windows vista con puntos de entrada del protocolo de búsqueda sp1 no aprovechan todos los parámetros posibles en el protocolo de búsqueda. Las aplicaciones que solo se refieren al control de llamadas de protocolo de búsqueda desde Windows Vista con SP1 pueden usar la tabla siguiente como guía para el mínimo necesario para implementar.



| Parámetro                                              | ¿La usa Windows? | Cómo Windows Vista con SP1 lo usa al llamar a search:                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Query                                                  | Sí              | Texto de consulta escrito por el usuario.                                                                                                                                                                                                                                         |
| [Miga](search-protocol-crumb.md)                     | Sí              | [crumb](search-protocol-crumb.md) usa el `location` argumento para especificar de dónde provenía la consulta.                                                                                                                                                                       |
| [subquery](search-protocol-subquery.md)               | Sí              | Los resultados del [argumento Subquery](search-protocol-subquery.md) se usan como ámbito de los elementos que se van a buscar. Normalmente, esto se usaría si un usuario usase un archivo .search-ms para buscar y, a continuación, llamara a la aplicación de búsqueda de escritorio predeterminada desde esa búsqueda. |
| [inputlocale](search-protocol-localeidentifiers.md)   | No               | No se usa actualmente.                                                                                                                                                                                                                                                         |
| [keywordlocale](search-protocol-localeidentifiers.md) | No               | No se usa actualmente.                                                                                                                                                                                                                                                         |
| [Sintaxis](search-protocol-syntaxargument.md)           | No               | No se usa actualmente.                                                                                                                                                                                                                                                         |
| [stackedby](search-protocol-stackedby.md)             | No               | No se usa actualmente.                                                                                                                                                                                                                                                         |
| displayname                                            | No               | No se usa actualmente.                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a>Ejemplos

Si un usuario escribe "Microsoft" en el menú Inicio y hace clic en **Buscar** en todas partes, se realiza la llamada al protocolo de búsqueda resultante: 


```C++
search:query=microsoft&
```



Si un usuario escribe "Seattle" en Windows Explorer en C: MyFolder y, a continuación, hace clic en Buscar en todas partes , se realiza la siguiente llamada, con caracteres de \\ escape para ":" y  \\ ":


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a>Registro de la aplicación que controla el protocolo

Dado que varias aplicaciones pueden contender por el [](default-programs.md) protocolo de búsqueda, debe registrar la aplicación con la característica Programas predeterminados durante la instalación para permitir al usuario configurar el valor predeterminado más fácilmente. Además de los procedimientos de instalación que se suelen practicar en Windows XP, una aplicación basada en Windows Vista debe registrarse con la característica Programas predeterminados para que la aplicación y los usuarios puedan configurar sin problemas los valores predeterminados.

Después de instalar los archivos binarios necesarios en el equipo del usuario, la rutina de instalación debe completar estas tareas generales:

1.  Escriba ProgID en **HKEY \_ LOCAL \_ MACHINE**, como se describe a continuación. Tenga en cuenta que las aplicaciones deben crear progIP específicos de la aplicación para el protocolo de búsqueda.
2.  Notificación de asociación del protocolo de búsqueda de nivel de máquina.
3.  Registre la aplicación con [programas predeterminados,](default-programs.md)como se explica en [Registro](default-programs.md)de una aplicación para su uso con programas predeterminados, como contendiente para el protocolo de búsqueda.

### <a name="registry-entries"></a>Entradas del Registro

A continuación se muestran ejemplos de las entradas del Registro necesarias para una aplicación ficticia de búsqueda de escritorio, Contoso Search.

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

 

 
