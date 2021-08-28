---
description: 'Más información sobre: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
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
ms.openlocfilehash: dfe7a12284c6144d9eca0b3e320f43e68ea66b4d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985278"
---
# <a name="jet_coltyp"></a>JET_COLTYP


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_coltyp"></a>JET_COLTYP

El **JET_COLTYP** de constantes describe todos los tipos de columna posibles que se pueden encontrar en una tabla.


| <p>Constante o valor</p> | <p>Descripción</p> | 
|-----------------------|--------------------|
| <p>JET_coltypNil<br />0</p> | <p>Tipo de columna no válido.</p> | 
| <p>JET_coltypBit<br />1</p> | <p>Tipo de columna que permite tres valores: <strong>True,</strong> <strong>False</strong>o <strong>NULL.</strong> Este tipo de columna tiene una longitud de un byte y tiene un tamaño fijo. <strong>False</strong> ordena antes que <strong>True.</strong> Tenga en cuenta que el tamaño de este tipo no coincide con el tamaño del tipo booleano variante.</p> | 
| <p>JET_coltypUnsignedByte<br />2</p> | <p>Entero de 1 byte sin signo que puede tomar valores entre 0 (cero) y 255.</p> | 
| <p>JET_coltypShort<br />3</p> | <p>Entero de 2 bytes con signo que puede tomar valores entre -32768 y 32767. Los valores negativos se ordenan antes que los positivos.</p> | 
| <p>JET_coltypLong<br />4</p> | <p>Entero de 4 bytes con signo que puede tomar valores entre - 2147483648 y 2147483647. Los valores negativos se ordenan antes que los positivos.</p> | 
| <p>JET_coltypCurrency<br />5</p> | <p>Entero de 8 bytes con signo que puede tomar valores entre - 9223372036854775808 y 9223372036854775807. Los valores negativos se ordenan antes que los positivos. Este tipo de columna es idéntico al tipo de moneda variante. Este tipo de columna también se puede usar como un entero con signo nativo de 8 bytes.</p> | 
| <p>JET_coltypIEEESingle<br />6</p> | <p>Número de punto flotante de precisión sencilla (4 bytes).</p> | 
| <p>JET_coltypIEEEDouble<br />7</p> | <p>Número de punto flotante de precisión doble (8 bytes).</p> | 
| <p>JET_coltypDateTime<br />8</p> | <p>Número de punto flotante de precisión doble (8 bytes) que representa una fecha en fracciones de días desde el año 1900. Este tipo de columna es idéntico al tipo de fecha variante.</p> | 
| <p>JET_coltypBinary<br />9</p> | <p>Columna binaria sin formato de longitud fija o variable que puede tener una longitud de hasta 255 bytes.</p><p>Este tipo de columna se puede usar para implementar un GUID si se configura como una columna binaria de 16 bytes de longitud fija. La única advertencia es que el orden relativo de los valores de un índice sobre una columna de este tipo no coincidirá con el orden relativo de la representación estándar de cadenas del Registro de un GUID (es decir, "{ 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}").</p> | 
| <p>JET_coltypText<br />10</p> | <p>Columna de texto de longitud fija o variable que puede tener hasta 255 caracteres ASCII de longitud o 127 caracteres Unicode.</p><p>Todas las cadenas se almacenan como un número de caracteres con recuento. No es necesario que las cadenas terminen en NULL. Además, no es necesario que el recuento incluya un terminador nulo. Por último, se pueden almacenar caracteres NULL incrustados.</p><p>Las cadenas ASCII siempre se tratan como que no tienen en cuenta mayúsculas de minúsculas con fines de ordenación y búsqueda. Además, solo se tienen en cuenta los caracteres que preceden al primer carácter nulo (si los hay) para la ordenación y la búsqueda.</p><p>Las cadenas Unicode usan <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> de la API de Win32 para crear claves de ordenación que posteriormente se usan para ordenar y buscar los datos. De forma predeterminada, las cadenas Unicode se consideran en la configuración regional del inglés de Estados Unidos y se ordenan y buscan mediante las siguientes marcas de normalización: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH. En Windows 2000, es posible personalizar estas marcas por índice para incluir también NORM_IGNORENONSPACE. En Windows XP y versiones posteriores, es posible solicitar cualquier combinación de las siguientes marcas de normalización por índice: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH y SORT_STRINGSORT.</p><p>En todas las versiones, es posible personalizar la configuración regional por índice. Se puede usar cualquier configuración regional siempre que se haya instalado el paquete de idioma adecuado en la máquina. Por último, los caracteres NULL encontrados en una cadena Unicode se omiten completamente.</p> | 
| <p>JET_coltypLongBinary<br />11</p> | <p>Columna binaria sin formato de longitud fija o variable que puede tener hasta 2147483647 bytes de longitud. Este tipo se considera un valor largo. Un valor largo es especial porque puede ser grande y porque se puede acceder a él como una secuencia. Este tipo es idéntico a JET_coltypBinary.</p> | 
| <p>JET_coltypLongText<br />12</p> | <p>Columna de texto de longitud fija o variable que puede tener hasta 2147483647 caracteres ASCII de longitud o 1073741823 caracteres Unicode. Este tipo se considera un valor largo. Un valor largo es especial porque puede ser grande y porque se puede acceder a él como una secuencia. Este tipo es idéntico a JET_coltypText.</p> | 
| <p>JET_coltypSLV<br />13</p> | <p>Este tipo de columna está obsoleto.</p> | 
| <p>JET_coltypUnsignedLong<br />14</p> | <p>Entero de 4 bytes sin signo que puede tomar valores entre 0 (cero) y 4294967295.</p><p><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna se admite en Windows Vista, Windows Server 2008 y versiones posteriores.</p> | 
| <p>JET_coltypLongLong<br />15</p> | <p>Entero de 8 bytes con signo que puede tomar valores entre - 9223372036854775808 y 9223372036854775807. Los valores negativos se ordenan antes que los positivos.</p><p><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna se admite en Windows Vista, Windows Server 2008 y versiones posteriores.</p> | 
| <p>JET_coltypGUID<br />16</p> | <p>Columna binaria de 16 bytes de longitud fija que representa de forma nativa el tipo de datos GUID. Los valores de columna GUID se ordenan de la misma manera que esos valores se ordenan como cadenas cuando están en formato estándar (es decir, {4999b5c0-7657-42d9-bdc1-4b779784e013}).</p><p><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna se admite en Windows Vista, Windows Server 2008 y versiones posteriores.</p> | 
| <p>JET_coltypUnsignedShort<br />17</p> | <p>Entero de 2 bytes sin signo que puede tomar valores comprendidos entre 0 y 65535.</p><p><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna se admite en Windows Vista, Windows Server 2008 y versiones posteriores.</p> | 
| <p>JET_coltypMax<br />18</p> | <p>Constante que describe el tipo de columna máximo (es decir, uno más allá del mayor válido) admitido por el motor.</p><p>Este valor debe usarse con cuidado porque cambiará a medida que se admiten nuevos tipos de columna. Por ejemplo, tiene un valor literal diferente en Windows 2000 que en Windows XP y versiones posteriores.</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)
