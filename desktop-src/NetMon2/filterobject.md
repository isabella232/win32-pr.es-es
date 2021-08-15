---
description: Define un único objeto de un filtro de visualización.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: Estructura FILTEROBJECT (Netmon.h)
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
ms.openlocfilehash: 6a8da526eb60d8d581ca10e24f87a78b91492c4c043e6322eebe6a2ca0ebfd10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795788"
---
# <a name="filterobject-structure"></a>FilterOBJECT (estructura)

La **estructura FILTEROBJECT** define un único objeto de un filtro de presentación. La [**función FilterAddObject**](filteraddobject.md) usa **FILTEROBJECT** para crear un filtro de visualización.

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

Marca que especifica la **acción FILTEROBJECT.** Una marca puede especificar una propiedad, un valor o un operador.

En la tabla siguiente se enumeran las marcas de propiedad del miembro Action.



| Valor                                                                                                                                                                                                | Significado                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <dt>**\_FILTERACTION, PROPIEDAD**</dt> </dl>                | Contiene esta propiedad.<br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <dt>**FILTERACTION \_ PROPERTYEXIST**</dt> </dl> | Indica que ya se ha definido una propiedad de acción de filtro.<br/> |



 

En la tabla siguiente se enumeran las marcas de valor de miembro de acción.



| Valor                                                                                                                                                                                        | Significado                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <dt>**VALOR \_ FILTERACTION**</dt> </dl>                 | Contiene este valor.<br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <dt>**FILTERACTION \_ STRING**</dt> </dl>              | Contiene esta cadena.<br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <dt>**FILTERACTION \_ ARRAY**</dt> </dl>                 | Contiene esta matriz.<br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <dt>**FILTERACTION \_ CONTAINSNC**</dt> </dl>  | Indica que una propiedad contiene una subcadena que no tiene en cuenta las mayúsculas y minúsculas.<br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <dt>**FILTERACTION \_ CONTAINS**</dt> </dl>        | Indica que una propiedad contiene una subcadena que distingue mayúsculas de minúsculas.<br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <dt>**DIRECCIÓN \_ FILTERACTION**</dt> </dl>           | Contiene la dirección MAC.<br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <dt>**FILTERACTION \_ ADDRESSANY**</dt> </dl>  | Coincide con cualquier dirección MAC.<br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <dt>**FILTERACTION \_ FROM**</dt> </dl>                    | Indica la dirección **DE MAC.**<br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <dt>**FILTERACTION \_ A**</dt> </dl>                          | Indica la dirección **MAC para** .<br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <dt>**FILTERACTION \_ FROMTO**</dt> </dl>              | Indica un emparejamiento **From/To** de direcciones MAC.<br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <dt>**FILTERACTION \_ LARGEINT**</dt> </dl>        | Contiene un entero grande.<br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <dt>**FILTERACTION \_ TIME**</dt> </dl>                    | Contiene una **estructura SYSTEMTIME.**<br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <dt>**FILTERACTION \_ ADDR \_ ETHER**</dt> </dl> | Contiene una dirección MAC Ethernet.<br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <dt>**TOKEN DE \_ ADDR FILTERACTION \_**</dt> </dl> | Contiene una dirección MAC de anillo de token.<br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <dt>**FILTERACTION \_ ADDR \_ FDDI**</dt> </dl>    | Contiene una dirección MAC FDDI.<br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <dt>**FILTERACTION \_ ADDR \_ IPX**</dt> </dl>       | Contiene una dirección MAC IPX.<br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <dt>**FILTERACTION \_ ADDR \_ IP**</dt> </dl>          | Contiene una dirección MAC IP.<br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <dt>**FILTERACTION \_ OID**</dt> </dl>                       | Contiene un identificador de objeto (OID).<br/>                             |



 

En la tabla siguiente se enumeran las marcas del operador miembro Action.



| Valor                                                                                                                                                                                                        | Significado                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <dt>**FILTERACTION \_ INVALID**</dt> </dl>                           | Indica una acción de filtro no válida.<br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <dt>**FILTERACTION \_ Y**</dt> </dl>                                       | Indica una instrucción **AND** lógica.<br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <dt>**FILTERACTION \_ O**</dt> </dl>                                          | Indica una instrucción **OR** lógica.<br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <dt>**FILTERACTION \_ XOR**</dt> </dl>                                       | Indica una instrucción **OR** exclusiva lógica (XOR).<br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <dt>**FILTERACTION \_ NOT**</dt> </dl>                                       | Indica una instrucción **NOT** lógica.<br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <dt>**FILTERACTION \_ EQUALNC**</dt> </dl>                           | La acción de filtro es igual y no tiene en cuenta las mayúsculas y minúsculas.<br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <dt>**FILTERACTION \_ EQUAL**</dt> </dl>                                 | La acción de filtro es igual y distingue mayúsculas de minúsculas.<br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <dt>**FILTERACTION \_ NOTEQUALNC**</dt> </dl>                  | La **instrucción NOT** lógica es igual y no tiene en cuenta las mayúsculas y minúsculas.<br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <dt>**FILTERACTION \_ NOTEQUAL**</dt> </dl>                        | La **instrucción NOT** lógica es igual y distingue mayúsculas de minúsculas.<br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <dt>**FILTERACTION \_ GREATERNC**</dt> </dl>                     | La acción de filtro es mayor que (>) y no tiene en cuenta las mayúsculas y minúsculas.<br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <dt>**FILTERACTION \_ GREATER**</dt> </dl>                           | La acción de filtro es mayor que (>) y distingue mayúsculas de minúsculas.<br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <dt>**FILTERACTION \_ LESSNC**</dt> </dl>                              | La acción de filtro es menor que (<) y no tiene en cuenta las mayúsculas y minúsculas.<br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <dt>**FILTERACTION \_ LESS**</dt> </dl>                                    | La acción de filtro es menor que (<) y distingue mayúsculas de minúsculas.<br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <dt>**FILTERACTION \_ GREATEREQUALNC**</dt> </dl>      | La acción de filtro es mayor o igual que (>=) y no tiene en cuenta las mayúsculas y minúsculas.<br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <dt>**FILTERACTION \_ GREATEREQUAL**</dt> </dl>            | La acción de filtro es mayor o igual que (>=) y distingue mayúsculas de minúsculas.<br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <dt>**FILTERACTION \_ LESSEQUALNC**</dt> </dl>               | La acción de filtro es menor o igual que (<=) y no tiene en cuenta las mayúsculas y minúsculas.<br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <dt>**FILTERACTION \_ LESSEQUAL**</dt> </dl>                     | La acción de filtro es menor o igual que (<=) y distingue mayúsculas de minúsculas.<br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <dt>**FILTERACTION \_ PLUS**</dt> </dl>                                    | Operador Add (+).<br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <dt>**FILTERACTION \_ MENOS**</dt> </dl>                                 | Operador Subtract (-).<br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <dt>**FILTERACTION \_ AREBITSON**</dt> </dl>                     | Indica una operación bit a bit.<br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <dt>**FILTERACTION \_ AREBITSOFF**</dt> </dl>                  | Indica una operación no bit a bit.<br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <dt>**FILTERACTION \_ PROTOCOLSEXIST**</dt> </dl>      | Indica que existen los protocolos seleccionados.<br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <dt>**FILTERACTION \_ PROTOCOLEXIST**</dt> </dl>         | Indica que existe el protocolo seleccionado.<br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <dt>**FILTERACTION \_ ARRAYEQUAL**</dt> </dl>                  | Indica que el contenido de la matriz es igual. La marca debe usarse con una **estructura FILTERACTION \_ ARRAY.**<br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <dt>**FILTERACTION \_ DEREFPROPERTY**</dt> </dl>         | Describe una coincidencia de patrón en un desplazamiento (en bytes) del protocolo.<br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <dt>**FILTERACTION \_ OID \_ CONTAINS**</dt> </dl>           | Evalúa una subcadena dentro de un identificador de objeto. La acción debe usarse con la **estructura \_ OID FILTERACTION.**<br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <dt>**FILTERACTION \_ OID \_ BEGINS \_ WITH**</dt> </dl> | Evalúa una subcadena que comienza un identificador de objeto. La marca debe usarse con **el \_ OID FILTERACTION**.<br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <dt>**FILTERACTION \_ OID \_ TERMINA \_ CON**</dt> </dl>       | Evalúa una subcadena que finaliza un identificador de objeto. La marca debe usarse con **el \_ OID FILTERACTION**.<br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <dt>**ADICIÓN \_ DE FILTERACTION \_ A LA PÁGINA DE TEXTO**</dt> </dl>                 | Contiene una dirección MAC de Vides.<br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <dt>**EXPRESIÓN \_ FILTERACTION**</dt> </dl>                  | Contiene una expresión de acción.<br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <dt>**FILTERACTION \_ BOOL**</dt> </dl>                                    | Contiene un **tipo de datos BOOL.**<br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <dt>**DIRECCIÓN \_ DEL \_ FILTRO SIGUIENTE**</dt> </dl>                       | Controla la dirección secuencial (marco siguiente) dentro de un archivo de captura.<br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <dt>**FILTER \_ DIRECTION \_ PREV**</dt> </dl>                       | Controla la dirección secuencial (marco anterior) dentro de un archivo de captura.<br/>                                                |



 

</dd> <dt>

**hProperty**
</dt> <dd>

Identificador de una clave de propiedad.

</dd> <dt>

**Valor**
</dt> <dd>

Valor de un objeto .

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

Puntero a una lista de protocolos diseñada para probar la existencia del protocolo en un marco.

</dd> <dt>

**lpAddress**
</dt> <dd>

Puntero a la dirección de tipo de kernel. Por ejemplo, MAC o IP.

</dd> <dt>

**lpLargeInt**
</dt> <dd>

DWORD **doble usado** en un Windows NT o Windows aplicación 2000.

</dd> <dt>

**lpTime**
</dt> <dd>

Puntero a una **estructura SYSTEMTIME.**

</dd> <dt>

**lpOID**
</dt> <dd>

Puntero a la **estructura OBJECT \_ IDENTIFIER** (OID).

</dd> <dt>

**ByteCount**
</dt> <dd>

Número, en bytes, del marco.

</dd> <dt>

**ByteOffset**
</dt> <dd>

Valor de byte de desplazamiento de la estructura FILTEROBJECT utilizada para comparar matrices.

</dd> <dt>

**pNext**
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




