---
description: Define un único objeto de un filtro de presentación.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: Estructura FILTEROBJECT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7649ab294f2ecad90946926dcc68d6937b357666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677296"
---
# <a name="filterobject-structure"></a>Estructura FILTEROBJECT

La estructura **FILTEROBJECT** define un único objeto de un filtro de presentación. La función [**FilterAddObject**](filteraddobject.md) usa **FILTEROBJECT** para crear un filtro de presentación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Acción**
</dt> <dd>

Marca que especifica la acción **FILTEROBJECT** . Una marca puede especificar una propiedad, un valor o un operador.

En la tabla siguiente se enumeran las marcas de propiedades de miembro de acción.



| Value                                                                                                                                                                                                | Significado                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <dt>**\_propiedad FILTERACTION**</dt> </dl>                | Contiene esta propiedad.<br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <dt>**FILTERACTION \_ PROPERTYEXIST**</dt> </dl> | Indica que ya se ha definido una propiedad de acción de filtrado.<br/> |



 

En la tabla siguiente se enumeran las marcas de valor de miembro de acción.



| Value                                                                                                                                                                                        | Significado                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <dt>**valor de FILTERACTION \_**</dt> </dl>                 | Contiene este valor.<br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <dt>**cadena de FILTERACTION \_**</dt> </dl>              | Contiene esta cadena.<br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <dt>**FILTERACTION ( \_ matriz)**</dt> </dl>                 | Contiene esta matriz.<br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <dt>**FILTERACTION \_ CONTAINSNC**</dt> </dl>  | Indica que una propiedad contiene una subcadena que no distingue mayúsculas de minúsculas.<br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <dt>**la FILTERACTION \_ contiene**</dt> </dl>        | Indica que una propiedad contiene una subcadena que distingue mayúsculas de minúsculas.<br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <dt>**Dirección de la FILTERACTION \_**</dt> </dl>           | Contiene la dirección MAC.<br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <dt>**FILTERACTION \_ ADDRESSANY**</dt> </dl>  | Coincide con cualquier dirección MAC.<br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <dt>**FILTERACTION \_ desde**</dt> </dl>                    | Indica la dirección **Mac de** .<br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <dt>**FILTERACTION \_ en**</dt> </dl>                          | Indica la dirección **Mac** .<br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <dt>**FILTERACTION \_ fromto**</dt> </dl>              | Indica una combinación de **/para** emparejar direcciones MAC.<br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <dt>**FILTERACTION \_ LARGEINT**</dt> </dl>        | Contiene un entero grande.<br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <dt>**tiempo de la FILTERACTION \_**</dt> </dl>                    | Contiene una estructura **SYSTEMTIME** .<br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <dt>**Dirección de la FILTERACTION \_ \_ ether**</dt> </dl> | Contiene una dirección MAC de Ethernet.<br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <dt>**\_token de dirección de la FILTERACTION \_**</dt> </dl> | Contiene una dirección MAC de token ring.<br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <dt>**Dirección de filtrado \_ \_ FDDI**</dt> </dl>    | Contiene una dirección MAC FDDI.<br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <dt>**Dirección de filtrado \_ \_ IPX**</dt> </dl>       | Contiene una dirección MAC de IPX.<br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <dt>**Dirección IP de la dirección de filtrado \_ \_**</dt> </dl>          | Contiene una dirección MAC de IP.<br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <dt>**OID de FILTERACTION \_**</dt> </dl>                       | Contiene un identificador de objeto (OID).<br/>                             |



 

En la tabla siguiente se enumeran las marcas de operador de miembro de acción.



| Value                                                                                                                                                                                                        | Significado                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <dt>**FILTERACTION \_ no válida**</dt> </dl>                           | Indica una acción de filtro no válida.<br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <dt>**FILTERACTION \_ y**</dt> </dl>                                       | Indica una instrucción **and** lógica.<br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <dt>**FILTERACTION \_ o**</dt> </dl>                                          | Indica una instrucción **or** lógica.<br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <dt>**FILTERACTION \_ XOR**</dt> </dl>                                       | Indica una instrucción or **exclusiva lógica** (XOR).<br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <dt>**FILTERACTION \_ no**</dt> </dl>                                       | Indica una instrucción **Not** lógica.<br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <dt>**FILTERACTION \_ EQUALNC**</dt> </dl>                           | La acción de filtrado es igual y no distingue mayúsculas de minúsculas.<br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <dt>**FILTERACTION \_ igual**</dt> </dl>                                 | La acción de filtrado es igual y distingue mayúsculas de minúsculas.<br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <dt>**FILTERACTION \_ NOTEQUALNC**</dt> </dl>                  | La instrucción not lógica es igual y **no** distingue mayúsculas de minúsculas.<br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <dt>**FILTRADO \_ NOTEQUAL**</dt> </dl>                        | La instrucción **Not** lógica es igual y distingue mayúsculas de minúsculas.<br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <dt>**FILTERACTION \_ GREATERNC**</dt> </dl>                     | La acción de filtrado es mayor que (>) y no distingue mayúsculas de minúsculas.<br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <dt>**la FILTERACTION es \_ mayor**</dt> </dl>                           | La acción de filtrado es mayor que (>) y distingue mayúsculas de minúsculas.<br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <dt>**FILTERACTION \_ LESSNC**</dt> </dl>                              | La acción de filtrado es menor que (<) y no distingue mayúsculas de minúsculas.<br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <dt>**FILTERACTION \_ menos**</dt> </dl>                                    | La acción de filtrado es menor que (<) y distingue mayúsculas de minúsculas.<br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <dt>**FILTERACTION \_ GREATEREQUALNC**</dt> </dl>      | La acción de filtrado es mayor o igual que (>=) y no distingue mayúsculas de minúsculas.<br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <dt>**FILTERACTION \_ mayor criticalthreshold**</dt> </dl>            | La acción de filtrado es mayor o igual que (>=) y distingue mayúsculas de minúsculas.<br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <dt>**FILTERACTION \_ LESSEQUALNC**</dt> </dl>               | La acción de filtrado es menor o igual que (<=) y no distingue mayúsculas de minúsculas.<br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <dt>**FILTERACTION \_ LESSEQUAL**</dt> </dl>                     | La acción de filtrado es menor o igual que (<=) y distingue mayúsculas de minúsculas.<br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <dt>**FILTERACTION \_ Plus**</dt> </dl>                                    | Agregar operador (+).<br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <dt>**FILTERACTION \_ menos**</dt> </dl>                                 | Operador de resta (-).<br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <dt>**FILTERACTION \_ AREBITSON**</dt> </dl>                     | Indica una operación bit a bit.<br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <dt>**FILTERACTION \_ AREBITSOFF**</dt> </dl>                  | Indica una operación no bit a bit.<br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <dt>**FILTERACTION \_ PROTOCOLSEXIST**</dt> </dl>      | Indica que existen los protocolos seleccionados.<br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <dt>**FILTERACTION \_ PROTOCOLEXIST**</dt> </dl>         | Indica que el protocolo seleccionado existe.<br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <dt>**FILTERACTION \_ ARRAYEQUAL**</dt> </dl>                  | Indica que el contenido de la matriz es igual. La marca se debe usar con una estructura de la **\_ matriz de FILTERACTION** .<br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <dt>**FILTERACTION \_ DEREFPROPERTY**</dt> </dl>         | Describe una coincidencia de patrones en un desplazamiento (en bytes) del protocolo.<br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <dt>**el OID de la FILTERACTION \_ \_ contiene**</dt> </dl>           | Evalúa una subcadena dentro de un identificador de objeto. La acción debe usarse con la estructura de la **FILTERACTION del \_ OID** .<br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <dt>**el \_ OID \_ de FILTERACTION comienza \_ con**</dt> </dl> | Evalúa una subcadena que comienza un identificador de objeto. La marca debe usarse con **el \_ OID** de la FILTERACTION.<br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <dt>**el \_ OID \_ de la FILTERACTION termina \_ con**</dt> </dl>       | Evalúa una subcadena que finaliza un identificador de objeto. La marca debe usarse con **el \_ OID** de la FILTERACTION.<br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <dt>**Dirección de filtrado- \_ \_ Vines**</dt> </dl>                 | Contiene una dirección MAC de Vines.<br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <dt>**\_expresión FILTERACTION**</dt> </dl>                  | Contiene una expresión de acción.<br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <dt>**FILTERACTION \_ bool**</dt> </dl>                                    | Contiene un tipo de datos **bool** .<br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <dt>**Dirección del filtro \_ \_ siguiente**</dt> </dl>                       | Controla la dirección secuencial (fotograma siguiente) dentro de un archivo de captura.<br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <dt>**Dirección del filtro \_ \_ anterior**</dt> </dl>                       | Controla la dirección secuencial (fotograma anterior) dentro de un archivo de captura.<br/>                                                |



 

</dd> <dt>

**hProperty**
</dt> <dd>

Identificador de una clave de propiedad.

</dd> <dt>

**Valor**
</dt> <dd>

Valor de un objeto.

</dd> <dt>

**hProtocol**
</dt> <dd>

Identificador para mostrar el protocolo de filtro.

</dd> <dt>

**lpArray**
</dt> <dd>

Puntero a una matriz.

</dd> <dt>

**lpProtocolTable**
</dt> <dd>

Puntero a una lista de protocolos diseñada para probar la existencia de un protocolo en un marco.

</dd> <dt>

**lpAddress**
</dt> <dd>

Puntero a la dirección del tipo de kernel. Por ejemplo, MAC o IP.

</dd> <dt>

**lpLargeInt**
</dt> <dd>

Doble **DWORD** usado en una aplicación Windows NT o Windows 2000.

</dd> <dt>

**lpTime**
</dt> <dd>

Puntero a una estructura **SYSTEMTIME** .

</dd> <dt>

**lpOID**
</dt> <dd>

Puntero a la estructura **de \_ identificador de objeto** (OID).

</dd> <dt>

**ByteCount**
</dt> <dd>

Número, en bytes, del marco.

</dd> <dt>

**Byteoffset (**
</dt> <dd>

El valor de byte de desplazamiento de la estructura FILTEROBJECT utilizada para comparar las matrices.

</dd> <dt>

**pNext**
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




