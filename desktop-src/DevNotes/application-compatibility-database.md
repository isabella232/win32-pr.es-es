---
description: La infraestructura de compatibilidad utiliza una base de datos para identificar los problemas de compatibilidad de aplicaciones y sus soluciones.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Base de datos de compatibilidad de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba33ab3a8de702f2e620b7607f4d2b6904e6165
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807124"
---
# <a name="application-compatibility-database"></a>Base de datos de compatibilidad de aplicaciones

La infraestructura de compatibilidad utiliza una base de datos para identificar los problemas de compatibilidad de aplicaciones y sus soluciones. Esta base de datos es un archivo binario indexado con una extensión. sdb. La infraestructura de compatibilidad proporciona una interfaz de programación para tener acceso a la base de datos.

Los problemas de compatibilidad se pueden resolver de forma programa por aplicación en tiempo de ejecución. Cada aplicación especificada en la base de datos contiene uno o más componentes que necesitan una solución. Los componentes son archivos ejecutables que se describen normalmente con sus atributos de archivo (por ejemplo, checksum).

El proceso de búsqueda en la base de datos y la determinación de las soluciones para cada aplicación se denomina *coincidencia*. Los atributos de archivo y la presencia de archivos asociados en la carpeta o subcarpeta que contiene el archivo. exe se pueden usar para crear una coincidencia única. Los archivos asociados se denominan *archivos coincidentes*.

Una *etiqueta* es un identificador único para las entradas y atributos de la base de datos. El *tipo de etiqueta* indica el formato de los datos asociados a la [**etiqueta**](tag.md). Por ejemplo, **el \_ nombre** de etiqueta es de tipo **tag \_ Type \_ STRINGREF**; los datos de **\_ nombre de etiqueta** son una cadena de nombre. Un *TAGID* es un puntero a una entrada en una base de datos determinada. Un *TAGREF* es un puntero a una entrada que se puede usar en varias bases de datos.

*Los atributos de archivo* son metadatos asociados a un archivo en disco. Estos atributos incluyen el nombre de archivo, el tamaño del archivo, la suma de comprobación, la versión y la fecha. Estos atributos se usan para determinar si un archivo cargado por el sistema coincide con una entrada de base de datos. Por lo tanto, estos atributos de archivo también se denominan *atributos coincidentes*.

## <a name="solutions"></a>Soluciones

Las soluciones más comunes aplicadas a los componentes de una aplicación son apphelp y AppFix.

Con apphelp, se muestra una notificación de mensajes localizados personalizada, normalmente cuando se instala o se inicia la aplicación. Contiene texto breve que explica el problema de compatibilidad y proporciona la opción de seguir ejecutando la aplicación. Sin embargo, se permite que se ejecuten drásticamente algunas aplicaciones. Apphelp no ofrece al usuario la opción de seguir ejecutando estas aplicaciones.

Con AppFix, se instalan enlaces para las API a las que llaman los componentes de la aplicación. Estos enlaces apuntan a funciones de código auxiliar a las que se puede llamar en lugar de a las funciones del sistema (también conocidas como *SHIMMING*). Las funciones de código auxiliar realizan las operaciones necesarias para permitir que la aplicación se ejecute en la versión instalada de Windows. Cada función de código auxiliar puede llamar opcionalmente a la función del sistema después de completar su trabajo. Un *nivel de compatibilidad* o un *modo* contiene una o varias correcciones de compatibilidad y marcas.

## <a name="in-this-section"></a>En esta sección

-   [**datos de APPHELP \_**](apphelp-data.md)
-   [**ATTRINFO**](attrinfo.md)
-   [**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
-   [**BUSCAR \_ información**](find-info.md)
-   [**INDEXID**](indexid.md)
-   [**tipo de ruta de acceso \_**](path-type.md)
-   [**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
-   [**SdbCloseDatabase**](sdbclosedatabase.md)
-   [**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
-   [**SdbCommitIndexes**](sdbcommitindexes.md)
-   [**SdbCreateDatabase**](sdbcreatedatabase.md)
-   [**SdbDeclareIndex**](sdbdeclareindex.md)
-   [**SdbEndWriteListTag**](sdbendwritelisttag.md)
-   [**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
-   [**SdbFindFirstTag**](sdbfindfirsttag.md)
-   [**SdbFindNextTag**](sdbfindnexttag.md)
-   [**SdbFormatAttribute**](sdbformatattribute.md)
-   [**SdbFreeFileAttributes**](sdbfreefileattributes.md)
-   [**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
-   [**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
-   [**SdbGetFileAttributes**](sdbgetfileattributes.md)
-   [**SdbGetFirstChild**](sdbgetfirstchild.md)
-   [**SdbGetIndex**](sdbgetindex.md)
-   [**SdbGetMatchingExe**](sdbgetmatchingexe.md)
-   [**SdbGetNextChild**](sdbgetnextchild.md)
-   [**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
-   [**SdbGetTagFromTagID**](sdbgettagfromtagid.md)
-   [**SdbInitDatabase**](sdbinitdatabase.md)
-   [**SdbIsStandardDatabase**](sdbisstandarddatabase.md)
-   [**SdbMakeIndexKeyFromString**](sdbmakeindexkeyfromstring.md)
-   [**SdbOpenApphelpDetailsDatabase**](sdbopenapphelpdetailsdatabase.md)
-   [**SdbOpenApphelpResourceFile**](sdbopenapphelpresourcefile.md)
-   [**SdbOpenDatabase**](sdbopendatabase.md)
-   [**SdbQueryDataExTagID**](sdbquerydataextagid.md)
-   [**SDBQUERYRESULT**](sdbqueryresult.md)
-   [**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
-   [**SdbReadBinaryTag**](sdbreadbinarytag.md)
-   [**SdbReadDWORDTag**](sdbreaddwordtag.md)
-   [**SdbReadQWORDTag**](sdbreadqwordtag.md)
-   [**SdbReadStringTag**](sdbreadstringtag.md)
-   [**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
-   [**SdbReleaseDatabase**](sdbreleasedatabase.md)
-   [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
-   [**SdbStartIndexing**](sdbstartindexing.md)
-   [**SdbStopIndexing**](sdbstopindexing.md)
-   [**SdbTagRefToTagID**](sdbtagreftotagid.md)
-   [**SdbTagToString**](sdbtagtostring.md)
-   [**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
-   [**SdbWriteBinaryTag**](sdbwritebinarytag.md)
-   [**SdbWriteBinaryTagFromFile**](sdbwritebinarytagfromfile.md)
-   [**SdbWriteDWORDTag**](sdbwritedwordtag.md)
-   [**SdbWriteNULLTag**](sdbwritenulltag.md)
-   [**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
-   [**SdbWriteStringTag**](sdbwritestringtag.md)
-   [**SdbWriteWORDTag**](sdbwritewordtag.md)
-   [**Tipos de bases de datos de Shim**](shim-database-types.md)
-   [**ShimFlushCache**](shimflushcache.md)
-   [**ETIQUETA**](tag.md)
-   [**Tipos de etiquetas**](tag-types.md)
-   [**TAGID**](tagid.md)
-   [**TAGREF**](tagref.md)

 

 



