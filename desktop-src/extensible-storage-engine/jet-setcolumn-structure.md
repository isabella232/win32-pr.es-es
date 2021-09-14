---
description: 'Más información sobre: JET_SETCOLUMN estructura'
title: JET_SETCOLUMN estructura
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: 811bd31b10ca4e304746f8ba26324b297feca602
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126962831"
---
# <a name="jet_setcolumn-structure"></a>JET_SETCOLUMN estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_setcolumn-structure"></a>JET_SETCOLUMN estructura

La **JET_SETCOLUMN** contiene parámetros de entrada y salida [para JetSetColumns](./jetsetcolumns-function.md). Los campos de la estructura describen qué valor de columna se va a establecer, cómo establecerlo y dónde obtener los datos del conjunto de columnas.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a>Members

**columnid**

Identificador de columna de una columna que se establecerá.

**pvData**

Puntero a los datos que se establecen en una columna.

**cbData**

Tamaño de asignación, en bytes, a partir de **pvData** en bytes.

**grbit**

Grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitSetAppendLV</p> | <p>Anexa datos a una columna de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. El mismo comportamiento se puede lograr determinando el tamaño del valor long existente y especificando <strong>ibLongValue</strong> en <strong>psetinfo</strong>. Sin embargo, es más sencillo usar este <em>grbit</em>, ya que no es necesario conocer el tamaño del valor de columna existente.</p> | 
| <p>JET_bitSetOverwriteLV</p> | <p>Reemplaza el valor long existente por los nuevos datos. Cuando se usa esta opción, es como si el valor long existente se hubiera establecido en 0 (cero) longitud antes de establecer los nuevos datos.</p> | 
| <p>JET_bitSetSizeLV</p> | <p>Interpreta el búfer de entrada como un número entero de bytes que se va a establecer como la longitud del valor largo descrito por el columnid especificado y, si se proporciona, el número de secuencia en psetinfo- &gt; itagSequence. Si el tamaño especificado es mayor que el valor de columna existente, la columna se ampliará con 0s. Si el tamaño es menor que el valor de columna existente, el valor se truncará.</p> | 
| <p>JET_bitSetZeroLength</p> | <p>Establece un valor en longitud cero. Normalmente, un valor de columna se establece en NULL pasando cbMax de 0. Sin embargo, para algunos tipos, <a href="gg269213(v=exchg.10).md">como JET_coltypText</a>, un valor de columna puede tener una longitud de 0 en lugar de NULL, y esta opción se usa para diferenciar entre null y 0 longitud.</p> | 
| <p>JET_bitSetSeparateLV</p> | <p>Fuerza que un valor largo, las columnas de <a href="gg269213(v=exchg.10).md">tipo JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, se almacenen por separado del resto de datos de registro. Esto sucede normalmente cuando el tamaño del valor largo impide que se almacene con los datos de registro restantes. Sin embargo, esta opción se puede usar para forzar que el valor long se almacene por separado. Tenga en cuenta que los valores largos de cuatro bytes de tamaño o más pequeños no se pueden forzar para que sean independientes. En tales casos, se omite la opción .</p> | 
| <p>JET_bitSetUniqueMultiValues</p> | <p>Aplica valores distintos en una columna con varios valores. Esta opción compara los datos de la columna de origen, sin ninguna transformación, con otros valores de columna existentes y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, JET_bitSetAppendLv, JET_bitSetOverwriteLV y JET_bitSetSizeLV también se pueden proporcionar.</p> | 
| <p>JET_bitSetUniqueNormalizedMultiValues</p> | <p>Aplica valores distintos en una columna con varios valores. Esta opción compara la transformación normalizada de clave de los datos de columna con otros valores de columna existentes transformados de forma similar y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, JET_bitSetAppendLv, JET_bitSetOverwriteLV y JET_bitSetSizeLV también se pueden proporcionar.</p> | 
| <p>JET_bitSetRevertToDefaultValue</p> | <p>Hace que la columna devuelva el valor de columna predeterminado en las operaciones de recuperación de columnas posteriores. Se quitan todos los valores de columna existentes. Esta opción solo es aplicable a las columnas etiquetadas, dispersas o con varios valores.</p> | 
| <p>JET_bitSetIntrinsicLV</p> | <p>Mantiene el valor largo, las columnas de <a href="gg269213(v=exchg.10).md">tipo JET_coltypLongText</a> o JET_coltypeLongBinary, almacenados con los datos de registro restantes si es posible. Normalmente, las columnas largas se almacenan por separado cuando su longitud supera los 1024 bytes o, de lo contrario, hace que la longitud del registro supere su limitación de tamaño de página relacionada. Sin embargo, si se establece esta opción, se producirá un error en la operación de establecimiento de columna JET_errColumnTooBig en lugar de almacenar este valor de columna independiente de los datos de registro restantes.</p> | 



**ibLongValue**

Desplazamiento al primer byte que se va a recuperar de una columna de [tipo JET_coltypLongBinary](./jet-coltyp.md)o [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Describe el número de secuencia de valor de una columna de varios valores. Una **itagSequence** de 0 indica que el conjunto de valores de columna debe agregarse como una nueva instancia de una columna de varios valores.

**Err**

Códigos de error y advertencias devueltos por la operación de establecer columna.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetSetColumns](./jetsetcolumns-function.md)
