---
title: wire_marshal (atributo)
description: El atributo \ wire marshal\ especifica un tipo de datos que se usará para la transmisión (el tipo de conexión) en lugar de un tipo de datos específico de la aplicación \_ (userm-type).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- wire_marshal atributo MIDL
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159316"
---
# <a name="wire_marshal-attribute"></a>atributo \_ wire marshal

El **\[ atributo wire \_ \] marshal** especifica un tipo de datos que se usará para la transmisión (el tipo de conexión *)* en lugar de un tipo de datos específico de la aplicación *(userm-type*).

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wire-type* 
</dt> <dd>

Especifica el tipo de datos de transferencia con nombre que se transfiere realmente entre el cliente y el servidor. El *tipo de conexión debe* ser un tipo base MIDL, un tipo predefinido o un identificador de tipo de un tipo que se pueda transmitir a través de la red.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Tipo para el que *userm-type* se convertirá en un alias.

</dd> <dt>

*userm-type* 
</dt> <dd>

Especifica el identificador del tipo de datos de usuario que se va a serializar. Puede ser cualquier tipo, tal como lo indica *el especificador* de tipo , siempre y cuando tenga un tamaño bien definido. El *tipo userm no* necesita ser transmitible, pero debe ser un tipo conocido por el compilador MIDL.

</dd> <dt>

*pFlags* 
</dt> <dd>

Especifica un puntero a un campo de marca ( [**unsigned**](unsigned.md) [**long**](long.md)). La palabra de orden superior especifica las marcas de representación de datos de BAND tal y como se define en DCE para la representación de punto flotante, big o little-endian y caracteres. La palabra de orden bajo especifica una marca de contexto de serialización. El diseño exacto de las marcas se describe en [El tipo \_ Función UserSize](/windows/desktop/Rpc/the-type-usersize-function).

</dd> <dt>

*StartingSize* 
</dt> <dd>

Especifica el tamaño de búfer actual (desplazamiento) antes de dimensionar el objeto.

</dd> <dt>

*pUser \_ typeObject* 
</dt> <dd>

Especifica un puntero a un objeto de *tipo \_ userm.*

</dd> <dt>

*Buffer* 
</dt> <dd>

Especifica el puntero de búfer actual.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cada tipo de datos específico de la aplicación, *userm-type,* tiene una correspondencia uno *a* uno con un tipo de conexión que define la representación de conexión del tipo. Debe proporcionar rutinas para cambiar el tamaño de los datos para la serialización, serializar y desmarmar los datos y liberar memoria. Tenga en cuenta **\[ \_ \]** que si hay tipos incrustados en los datos que también se definen con referencias de conexión o referencias de usuario, también debe administrar el mantenimiento de esos tipos **\[** [**\_**](user-marshal.md) **\]** incrustados. Para obtener más información sobre estas rutinas, vea [The wire \_ marshal Attribute](/windows/desktop/Rpc/the-wire-marshal-attribute).

La implementación debe seguir las reglas de marshalling según la especificación de OSF-DCE. Puede encontrar detalles sobre la sintaxis de transferencia de QL en [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) . No se recomienda usar la **\[ serialización \_ de conexión \]** si no está familiarizado con el protocolo de conexión.

El *tipo de conexión no* puede ser un puntero de interfaz ni un puntero completo. El *tipo de conexión* debe tener un tamaño de memoria bien definido. Consulte [Reglas de serialización para serialización de usuario \_ \_](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) y serialización de conexión para obtener más información sobre cómo serializar un tipo *de conexión determinado.*

*Userm-type no* debe ser un puntero de interfaz porque se pueden serializar directamente. Si el tipo de usuario es un puntero completo, debe administrar el alias usted mismo.

No se puede usar el atributo **\[ \_ wire marshal \]** con el atributo allocate, directa o **\[** [](allocate.md) **\]** indirectamente, porque el motor MOTOR no controla la asignación de memoria para el tipo transmitido.

## <a name="examples"></a>Ejemplos

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[Representación de datos](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**Largo**](long.md)
</dt> <dt>

[**GetGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[Atributo de \_ serialización de conexión](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**serialización \_ de usuario**](user-marshal.md)
</dt> </dl>

 

 