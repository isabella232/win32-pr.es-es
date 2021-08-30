---
description: 'Más información sobre: Parámetros de índice'
title: Parámetros de índice
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: 3971f8093b9f1578a9b84d19a3927e45262acbad
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987028"
---
# <a name="index-parameters"></a>Parámetros de índice


_**Se aplica a:** Windows | Windows Servidor_

## <a name="index-parameters"></a>Parámetros de índice

Este tema contiene parámetros que se usan para el índice.

*JET_paramIndexTupleIncrement*  
132  

Este parámetro especifica el valor predeterminado para el incremento de desplazamiento utilizado para desplazarse paso a paso por el valor de la columna de origen al generar cada tupla. Para obtener más información, vea la [estructura JET_TUPLELIMITS](./jet-tuplelimits-structure.md) datos.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>1</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0 - 32767</p> | 
| <p>Ámbito:</p> | <p>Instancia</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows Vista y versiones posteriores</p> | 



*JET_paramIndexTupleStart*  
133  

Este parámetro especifica el valor predeterminado para el desplazamiento en el valor de la columna de origen en el que se iniciará la generación de tupla. Para obtener más información, vea la [estructura JET_TUPLELIMITS](./jet-tuplelimits-structure.md) datos.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>0</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>0 - 32767</p> | 
| <p>Ámbito:</p> | <p>Instancia</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows Vista y versiones posteriores</p> | 



*JET_paramIndexTuplesLengthMax*  
111  

Este parámetro especifica el valor predeterminado para la longitud máxima de tupla en un índice de tupla. Para obtener más información, vea la [estructura JET_TUPLELIMITS](./jet-tuplelimits-structure.md) datos.

**Windows Vista:**  Antes de Windows Vista, establecer este parámetro en cero lo establecería de nuevo en su valor predeterminado. Para Windows Vista, ya no se admite.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>10</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 0, 2-255</p><p><strong>Windows Vista:</strong> 2-255</p> | 
| <p>Ámbito:</p> | <p>Instancia</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramIndexTuplesLengthMin*  
110  

Este parámetro especifica el valor predeterminado para la longitud mínima de tupla en un índice de tupla. Consulte [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) para obtener más información.

**Windows Vista:**  Antes de Windows Vista, establecer este parámetro en cero lo establecería de nuevo en su valor predeterminado. Para Windows Vista, ya no se admite.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>3</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 0, 2-255</p><p><strong>Windows Vista:</strong> 2-255</p> | 
| <p>Ámbito:</p> | <p>Instancia</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramIndexTuplesToIndexMax*  
112  

Este parámetro especifica el valor predeterminado para la longitud máxima de una cadena de origen que se interrumpirá en tuplas para un índice de tupla. Consulte [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) para obtener más información.

**Windows Vista:**  Antes de Windows Vista, al establecer este parámetro en cero, se vuelve a establecer en su valor predeterminado. Para Windows Vista, ya no se admite.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>32767</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> 0 – 32767</p><p><strong>Windows Vista:</strong> 1 – 32767</p> | 
| <p>Ámbito:</p> | <p>Instancia</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramUnicodeIndexDefault*  
72  

Este parámetro controla los parámetros Unicode predeterminados utilizados por cualquier índice sobre una columna de clave Unicode. El tipo de este parámetro se [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) y se pasa realmente mediante un puntero de búfer almacenado en el parámetro entero [de JetGetSystemParameter](./jetgetsystemparameter-function.md) y [JetSetSystemParameter](./jetsetsystemparameter-function.md). El tamaño del búfer debe ser igual al tamaño de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) y debe pasarse a [JetGetSystemParameter](./jetgetsystemparameter-function.md) mediante el parámetro de tamaño de búfer de cadena. Esto es claramente incoherente, pero ese es el comportamiento de este parámetro.

El valor predeterminado de este parámetro contiene un LCID para la configuración regional del inglés de EE. UU. y las siguientes marcas [LCMapStringW:](/windows/win32/api/winnls/nf-winnls-lcmapstringa)LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.

**Windows 2000:**  El SORTID del LCID se omite. Siempre se usa un SORTID de SORT_DEFAULT se usa.

**Windows 2000:**  Las [marcas LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) deben contener las marcas siguientes: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH. Además, las [marcas LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)pueden contener las marcas siguientes: NORM_IGNORENONSPACE.

**Nota**  Si la aplicación desea almacenar datos Unicode, se recomienda encarecidamente no confiar en los parámetros Unicode predeterminados para los índices. El uso del inglés de EE. UU. equivale al uso de la configuración regional invariable y se sabe que las marcas [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)predeterminadas interfieren gravemente con algunos idiomas. Siempre debe especificar su propia configuración para los parámetros Unicode en JetCreateIndex2 [mediante JET_INDEXCREATE](./jet-indexcreate-structure.md).


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>Especial</p> | 
| <p>Escriba:</p> | <p>JET_UNICODEINDEX* (JET_UNICODEINDEX)</p> | 
| <p>Intervalo válido:</p> | <p>Especial</p> | 
| <p>Ámbito:</p> | <p>Instancia</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
