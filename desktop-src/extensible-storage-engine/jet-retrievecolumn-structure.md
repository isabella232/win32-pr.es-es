---
description: 'Más información sobre: JET_RETRIEVECOLUMN estructura'
title: Estructura de JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
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
ms.openlocfilehash: 4f29f3c6a9ca3262b3cd09d726634afd70db9c6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471461"
---
# <a name="jet_retrievecolumn-structure"></a>Estructura de JET_RETRIEVECOLUMN


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_retrievecolumn-structure"></a>Estructura de JET_RETRIEVECOLUMN

La **JET_RETRIEVECOLUMN** contiene parámetros de entrada y salida [para JetRetrieveColumns.](./jetretrievecolumns-function.md) Los campos de la estructura describen qué valor de columna se va a recuperar, cómo recuperarlo y dónde guardar los resultados.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a>Miembros

**columnid**

Identificador de columna de la columna que se recuperará.

**pvData**

Puntero para empezar a almacenar los datos que se recuperan del valor de columna.

**cbData**

Tamaño de asignación que comienza en **pvData,** en bytes. La operación de recuperación de columna no almacenará más datos en **pvData** que **cbData.**

**cbActual**

Tamaño, en bytes, de los datos recuperados por una operación de recuperación de columna.

**grbit**

Grupo de bits que contienen las opciones para la recuperación de columnas, que incluyen cero o más de los valores siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Recupera el valor modificado en lugar del valor original. Si el valor no se ha modificado, se recupera el valor original. De este modo, se puede recuperar un valor que aún no se ha insertado o actualizado cuando se inserta o actualiza un registro.</p> | 
| <p>JET_bitRetrieveFromIndex</p> | <p>Recupera los valores de columna del índice sin tener acceso al registro, si es posible. De esta manera, se puede evitar la carga innecesaria de registros cuando los datos necesarios están disponibles en las propias entradas de índice. En los casos en los que el valor de la columna original no se puede recuperar del índice, debido a transformaciones irreversibles o truncamiento de datos, se accederá al registro y se recuperarán los datos de la forma habitual. Se trata de una opción de rendimiento y solo se debe especificar cuando es probable que el valor de columna se pueda recuperar del índice. Esta opción no debe especificarse si el índice actual es el índice clúster, ya que las entradas de índice para el índice clúster o principal son los propios registros. Este bit no se puede establecer si JET_bitRetrieveFromPrimaryBookmark también está establecido.</p> | 
| <p>JET_bitRetrieveFromPrimaryBookmark</p> | <p>Recupera los valores de columna del marcador de índice y puede diferir del valor de índice cuando una columna aparece tanto en el índice principal como en el índice actual. Esta opción no debe especificarse si el índice actual es el índice agrupado o principal. Este bit no se puede establecer si JET_bitRetrieveFromIndex también está establecido.</p> | 
| <p>JET_bitRetrieveTag</p> | <p>Recupera el número de secuencia de un valor de columna multivalor en pretinfo- &gt; itagSequence. El campo itagSequence se usa a menudo como entrada para recuperar valores de columna multivalor de un registro. Sin embargo, al recuperar valores de un índice, también es posible asociar la entrada de índice a un número de secuencia determinado y recuperar también este número de secuencia. Recuperar el número de secuencia puede ser una operación costosa y solo debe realizarse si es necesario.</p> | 
| <p>JET_ bitRetrieveNull</p> | <p>Recupera valores NULL de columna multivalor. Si no se especifica esta opción, los valores NULL de columna multivalor se omitirán automáticamente.</p> | 
| <p>JET_bitRetrieveIgnoreDefault</p> | <p>Hace que se devuelva un valor NULL cuando el número de secuencia solicitado es 1 y no hay valores establecidos para la columna en el registro. Esta opción solo afecta a las columnas con varios valores.</p> | 
| <p>JET_bitRetrieveLongId</p> | <p>Esta marca es solo para uso interno y no está pensada para usarse en la aplicación.</p> | 
| <p>JET_bitRetrieveLongValueRefCount</p> | <p>Esta marca es solo para uso interno y no está pensada para usarse en la aplicación.</p> | 



**ibLongValue**

Desplazamiento al primer byte que se va a recuperar de una columna de [tipo JET_coltypLongBinary](./jet-coltyp.md) o [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Número de secuencia de los valores contenidos en una columna con varios valores. **itagSequence** aquí en la **JET_RETRIEVECOLUMN** puede ser 0. Si **itagSequence** es 0, se devuelve el número de instancias de una columna con varios valores en lugar de cualquier dato de columna. No se puede usar un valor de **itagSequence** de 0 en las llamadas a [JetRetrieveColumn](./jetretrievecolumn-function.md).

**columnidNextTagged**

Columnid **de** la columna etiquetada, multivalor o dispersa cuando se recuperan todas las columnas etiquetadas pasando 0 como **columnid** a [JetRetrieveColumn](./jetretrievecolumn-function.md).

**Err**

Códigos de error y advertencias devueltos desde la recuperación de la columna.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETRIEVECOLUMN]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
