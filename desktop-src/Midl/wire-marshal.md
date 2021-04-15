---
title: wire_marshal (atributo)
description: El atributo \ cable \_ Marshal \ especifica un tipo de datos que se usará para la transmisión (el tipo de conexión) en lugar de un tipo de datos específico de la aplicación (el tipo userm).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- wire_marshal el atributo MIDL
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421540"
---
# <a name="wire_marshal-attribute"></a>\_atributo de serialización de cable

El atributo de **\[ \_ serialización \] de conexión** especifica un tipo de datos que se utilizará para la transmisión (el tipo de *conexión*) en lugar de un tipo de datos específico de la aplicación (el *tipo userm*).

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

*tipo de conexión* 
</dt> <dd>

Especifica el tipo de datos de transferencia con nombre que se transfiere realmente entre el cliente y el servidor. El *tipo de conexión* debe ser un tipo base de MIDL, un tipo predefinido o un identificador de tipo de un tipo que se pueda transmitir a través de la red.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Tipo para el que *userm* se convertirá en un alias.

</dd> <dt>

*tipo de userm* 
</dt> <dd>

Especifica el identificador del tipo de datos de usuario del que se van a calcular las referencias. Puede ser cualquier tipo, tal y como lo proporciona el *especificador Type-Specifier*, siempre que tenga un tamaño bien definido. No es necesario que el *tipo userm* sea transmitible, sino que debe ser un tipo conocido para el compilador de MIDL.

</dd> <dt>

*pFlags* 
</dt> <dd>

Especifica un puntero a un campo de marca ( [**unsigned**](unsigned.md) [**Long**](long.md)). La palabra de orden superior especifica las marcas de representación de datos NDR definidas por DCE para el punto flotante, el Big-endian y la representación de caracteres. La palabra de orden inferior especifica una marca de contexto de cálculo de referencias. El diseño exacto de las marcas se describe en [la función de tipo de \_ usuario](/windows/desktop/Rpc/the-type-usersize-function).

</dd> <dt>

*StartingSize* 
</dt> <dd>

Especifica el tamaño de búfer actual (desplazamiento) antes de ajustar el tamaño del objeto.

</dd> <dt>

*pUser \_ typeObject* 
</dt> <dd>

Especifica un puntero a un objeto de *\_ tipo userm.*

</dd> <dt>

*Buffer* 
</dt> <dd>

Especifica el puntero de búfer actual.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cada tipo de datos específico de la aplicación, *userm-Type,* tiene una correspondencia uno a uno con un *tipo de conexión* que define la representación de la conexión del tipo. Debe proporcionar rutinas para ajustar el tamaño de los datos para el cálculo de referencias, para calcular las referencias de los datos y para deserializarlos, y para liberar memoria. Tenga en cuenta que si hay tipos incrustados en los datos que también se definen con **\[ \_ serialización \] de conexión** o **\[** [**\_ serialización de usuario**](user-marshal.md), debe **\]** administrar también el servicio de esos tipos incrustados. Para obtener más información sobre estas rutinas, vea [el \_ atributo de serialización de la conexión](/windows/desktop/Rpc/the-wire-marshal-attribute).

La implementación debe seguir las reglas de serialización según la especificación de OSF-DCE. Encontrará más información sobre la sintaxis de transferencia de NDR en [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) . No se recomienda usar la **\[ \_ serialización \] de conexión** si no está familiarizado con el protocolo de conexión.

El *tipo de conexión* no puede ser un puntero de interfaz ni un puntero completo. El *tipo de conexión* debe tener un tamaño de memoria bien definido. Vea [serialización de reglas para la serialización de usuarios \_ y \_ serialización de conexión](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) para más información sobre cómo calcular las referencias de un *tipo de conexión* determinado.

El *tipo de userm* no debe ser un puntero de interfaz porque se pueden calcular las referencias directamente. Si el tipo de usuario es un puntero completo, debe administrar el alias.

No se puede usar el atributo de **\[ \_ serialización \] de conexión** con el **\[** atributo [**allocate**](allocate.md) **\]** , ya sea directa o indirectamente, porque el motor NDR no controla la asignación de memoria para el tipo transmitido.

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

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**tal**](long.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[Atributo de \_ serialización de cable](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**sin signo**](unsigned.md)
</dt> <dt>

[**\_serialización de usuario**](user-marshal.md)
</dt> </dl>

 

 