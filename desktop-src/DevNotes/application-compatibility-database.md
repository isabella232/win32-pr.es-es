---
description: La infraestructura de compatibilidad usa una base de datos para identificar problemas de compatibilidad de aplicaciones y sus soluciones.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Base de datos de compatibilidad de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787e8dbc9aa07bc8d466dae766c3fed406692dbd32e128123c4b37d9a7a5618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956164"
---
# <a name="application-compatibility-database"></a>Base de datos de compatibilidad de aplicaciones

La infraestructura de compatibilidad usa una base de datos para identificar problemas de compatibilidad de aplicaciones y sus soluciones. Esta base de datos es un archivo binario indexado con una extensión .sdb. La infraestructura de compatibilidad proporciona una interfaz de programación para acceder a la base de datos.

Los problemas de compatibilidad se pueden solucionar por aplicación en tiempo de ejecución. Cada aplicación especificada en la base de datos contiene uno o varios componentes que necesitan una solución. Los componentes son archivos ejecutables que generalmente se describen mediante sus atributos de archivo (por ejemplo, suma de comprobación).

El proceso de búsqueda de base de datos y determinación de las soluciones para cada aplicación se denomina *coincidencia.* Los atributos de archivo y la presencia de archivos asociados en la carpeta o subcarpeta que contiene .exe archivo se pueden usar para crear una coincidencia única. Los archivos asociados se *denominan archivos correspondientes.*

Una *ETIQUETA* es un identificador único para las entradas y atributos de la base de datos. El *tipo TAG* indica el formato de los datos asociados a la [**etiqueta**](tag.md). Por ejemplo, **TAG \_ NAME es** de tipo TAG TYPE **\_ \_ STRINGREF;** los datos de **TAG \_ NAME** son una cadena de nombre. Un *TAGID es* un puntero a una entrada de una base de datos determinada. TAGREF *es* un puntero a una entrada que se puede usar en varias bases de datos.

*Los atributos de* archivo son metadatos asociados a un archivo en disco. Estos atributos incluyen el nombre de archivo, el tamaño del archivo, la suma de comprobación, la versión y la fecha. Estos atributos se usan para determinar si un archivo cargado por el sistema coincide con una entrada de base de datos. Por lo tanto, estos atributos de archivo también se *denominan atributos que coinciden.*

## <a name="solutions"></a>Soluciones

Las soluciones más comunes que se aplican a los componentes de una aplicación son Apphelp y Appfix.

Con Apphelp, se muestra una notificación de mensaje localizada personalizada, normalmente cuando se instala o se inicia la aplicación. Contiene un breve texto que explica el problema de compatibilidad y proporciona la opción de seguir ejecutando la aplicación. Sin embargo, algunas aplicaciones producirán un error considerablemente al ejecutarse. Apphelp no dará al usuario la opción de seguir ejecutando estas aplicaciones.

Con Appfix, se instalan enlaces para las API a las que llaman los componentes de la aplicación. Estos enlaces apuntan a funciones de código auxiliar a las que se puede llamar en lugar de a las funciones del sistema (también conocidas como *correcciones de compatibilidad (shimming).* Las funciones de código auxiliar realizan las operaciones necesarias para permitir que la aplicación se ejecute en la versión instalada de Windows. Opcionalmente, cada función de código auxiliar puede llamar a la función del sistema después de completar su trabajo. Una *capa o modo* de *compatibilidad* contiene una o varias correcciones de compatibilidad (shim) y marcas.

## <a name="in-this-section"></a>En esta sección

-   [**APPHELP \_ DATA**](apphelp-data.md)
-   [**ATTRINFO**](attrinfo.md)
-   [**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
-   [**BUSCAR \_ INFORMACIÓN**](find-info.md)
-   [**INDEXID**](indexid.md)
-   [**TIPO DE \_ RUTA DE ACCESO**](path-type.md)
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
-   [**Tipos de base de datos shim**](shim-database-types.md)
-   [**ShimFlushCache**](shimflushcache.md)
-   [**etiqueta**](tag.md)
-   [**Tipos DE ETIQUETA**](tag-types.md)
-   [**TAGID**](tagid.md)
-   [**TAGREF**](tagref.md)

 

 



