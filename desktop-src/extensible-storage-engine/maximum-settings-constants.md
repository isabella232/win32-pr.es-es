---
description: 'Más información sobre: Número máximo de Configuración constantes'
title: Número máximo Configuración constantes
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa6ff7044dcd43e4b51c801784d29955f3d34a15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269631"
---
# <a name="maximum-settings-constants"></a>Número máximo Configuración constantes


_**Se aplica a:** Windows | Windows Servidor_

## <a name="maximum-settings-constants"></a>Número máximo Configuración constantes

Estas constantes proporcionan la configuración máxima permitida en los elementos de una base de datos ese.


| <p>Constante o valor</p> | <p>Descripción</p> | 
|-----------------------|--------------------|
| <p>JET_BASE_NAME_LENGTH<br />3</p> | <p>Establece la longitud del prefijo utilizado para dar nombre a los archivos utilizados por el motor de base de datos. Esta longitud es aplicable al nombre establecido para el <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> del sistema.</p> | 
| <p>JET_MAX_COMPUTERNAME_LENGTH<br />15</p> | <p>Establece la longitud máxima de <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</p> | 
| <p>JET_cbBookmarkMost<br />256</p> | <p>Tamaño máximo predeterminado de un marcador. Esto es válido cuando el tamaño de la clave se deja en su valor predeterminado.</p> | 
| <p>JET_cbBookmarkMostMost<br />2000</p> | <p>Tamaño máximo de un marcador cuando esent está configurado para tener las claves más grandes posibles.</p><p><strong>Windows 7:</strong> JET_cbBookmarkMostMost se introdujo en Windows 7.</p> | 
| <p>JET_cbNameMost<br />64</p> | <p>Longitud máxima de un objeto, columna, índice o nombre de propiedad.</p><p><strong>Nota</strong>  Si es Unicode, el valor es 128.</p> | 
| <p>JET_cbFullNameMost<br />255</p> | <p>La longitud máxima de un "name.name.name..." Construir.</p><p><strong>Nota</strong>  Si es Unicode, el valor es 510.</p> | 
| <p>JET_cbColumnLVPageOverhead<br />82</p> | <p>Este número se puede usar para calcular la cantidad máxima de un BLOB que el motor de base de datos puede almacenar en una sola página de base de datos. La fórmula es max size = JET_paramDatabasePageSize–JET_cbColumnLVPageOverhead.</p><p>Este valor ahora está obsoleto. El tamaño del fragmento de valor largo se debe recuperar con el JET_paramLVChunkSizeMost parámetro .</p> | 
| <p>JET_cbColumnMost<br />255</p> | <p>Tamaño máximo de los datos de columna de valor no largo.</p> | 
| <p>JET_cbLVDefaultValueMost<br />255</p> | <p>Tamaño máximo de un valor predeterminado de columna de valor largo (LongBinary o LongText).</p> | 
| <p>JET_cbKeyMost<br />255</p> | <p>Tamaño máximo predeterminado de una clave de ordenación o índice.</p> | 
| <p>JET_cbKeyMostMost<br />2000</p> | <p>Tamaño máximo configurable de una clave de ordenación o índice para cualquier tamaño de página. (Vea JET_INDEXCREATE2.cbKeyMost)</p><p><strong>Windows 7:</strong> JET_cbKeyMostMost se introduce en el sistema operativo Windows 7.</p> | 
| <p>JET_cbKeyMost2KBytePage<br />500</p> | <p>El tamaño máximo configurable máximo permitido para una clave de índice en una base de datos mediante páginas de 2048 bytes. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</p><p><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage se introduce en el sistema operativo Windows Vista.</p> | 
| <p>JET_cbKeyMost4KBytePage<br />1000</p> | <p>El tamaño máximo configurable máximo permitido para una clave de índice en una base de datos mediante páginas de 4096 bytes. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</p><p><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage se introdujo en Windows Vista.</p> | 
| <p>JET_cbKeyMost8KBytePage<br />2000</p> | <p>El tamaño máximo configurable máximo permitido para una clave de índice en una base de datos mediante páginas de 8192 bytes. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</p><p><strong>Windows Vista:</strong> JET_cbKeyMost8KBytePage se introdujo en Windows Vista</p> | 
| <p>JET_cbKeyMostMin<br />255</p> | <p>Tamaño máximo mínimo permitido para una clave de índice. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</p><p><strong>Windows Vista:</strong> JET_cbKeyMostMin se introdujo en Windows Vista.</p> | 
| <p>JET_cbLimitKeyMost<br />256</p> | <p>Tamaño máximo de clave cuando la clave se forma mediante un <em>grbit</em>de límite, como JET_bitStrLimit, que se usa en la <a href="gg269329(v=exchg.10).md">función JetMakeKey.</a></p> | 
| <p>JET_cbPrimaryKeyMost<br />255</p> | <p>Tamaño máximo del índice principal. Ahora está obsoleto.</p> | 
| <p>JET_cbSecondaryKeyMost<br />255</p> | <p>Tamaño máximo del índice secundario. Ahora está obsoleto.</p> | 
| <p>JET_ccolKeyMost<br />12</p> | <p>Número máximo de componentes de una clave de ordenación o índice.</p><p><strong>Windows Vista:</strong> En Windows Vista y versiones posteriores de Windows el valor es 16.</p> | 
| <p>JET_ccolMost<br />0x0000fee0</p> | <p>Número máximo de columnas permitidas en una tabla.</p><p><strong>Windows XP:</strong> El valor 0x0000fee0 se usa en Windows XP y versiones posteriores y posteriores de Windows</p><p><strong>Windows 2000:</strong> El valor 0x00007ffe se usa en Windows 2000.</p> | 
| <p>JET_ccolFixedMost<br />0x0000007f</p> | <p>Número máximo de columnas fijas permitidas en una tabla, actualmente 127.</p> | 
| <p>JET_ccolVarMost<br />0x00000080</p> | <p>Número máximo de columnas de longitud variable que se pueden incluir en una tabla, actualmente 128.</p> | 
| <p>JET_ccolTaggedMost<br />( JET_ccolMost - 0x000000ff )</p> | <p>Número máximo de columnas etiquetadas que se pueden contener en una tabla, actualmente 64993.</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 


