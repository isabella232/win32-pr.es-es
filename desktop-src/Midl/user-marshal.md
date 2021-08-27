---
title: user_marshal atributo
description: El atributo ACF de serialización de usuario asocia un tipo local con nombre en el idioma de destino (userm-type) a un tipo de transferencia (wire-type) que se transfiere entre el cliente \_ y el servidor.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal atributo MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f17b4ef9d4376309307403ee12e2c5aae507556beaf091f9d742998d18671a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105575"
---
# <a name="user_marshal-attribute"></a>atributo \_ de serialización de usuario

El atributo ACF de serialización de usuario asocia un tipo local con nombre en el idioma de destino *(userm-type*) a un tipo de transferencia *(tipo* de conexión) que se transfiere entre el cliente y el servidor. **\_**

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*userm-type* 
</dt> <dd>

Especifica el identificador del tipo de datos de usuario que se va a serializar. El *userm-type* no debe ser transmitible y no necesita ser un tipo conocido por el compilador MIDL.

</dd> <dt>

*wire-type* 
</dt> <dd>

Especifica el tipo de datos de transferencia con nombre que se transfiere realmente entre el cliente y el servidor. El tipo de conexión debe ser un tipo base MIDL, un tipo predefinido o un identificador de tipo de un tipo que se pueda transmitir a través de la red.

</dd> <dt>

*pFlags* 
</dt> <dd>

Especifica un puntero a un campo de marca ( [**unsigned**](unsigned.md) [**long**](long.md)). La palabra de orden superior especifica las marcas de representación de datos BAND, tal y como se define en DCE, para la representación de punto flotante, big o little-endian y caracteres. La palabra de orden bajo especifica una marca de contexto de serialización. El diseño exacto de las marcas se describe en [El tipo \_ Función UserSize](/windows/desktop/Rpc/the-type-usersize-function).

</dd> <dt>

*StartingSize* 
</dt> <dd>

Especifica el tamaño del búfer actual (desplazamiento) antes de dimensionar el objeto.

</dd> <dt>

*pUser \_ typeObject* 
</dt> <dd>

Especifica un puntero a un objeto de *tipo userm \_*.

</dd> <dt>

*Buffer* 
</dt> <dd>

Especifica el puntero de búfer actual.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cada tipo local con nombre, *userm-type*, tiene una correspondencia uno *a* uno con un tipo de conexión que define la representación de conexión del tipo. Debe proporcionar rutinas para cambiar el tamaño de los datos para la serialización, serializar y desmarmar los datos y liberar memoria. Para obtener más información sobre estas rutinas, vea [Atributo de \_ serialización de usuario](/windows/desktop/Rpc/the-user-marshal-attribute). Tenga en cuenta **\_** \[ [**\[ \_ \]**](wire-marshal.md)que si hay tipos incrustados en los datos que también se definen con referencias de usuario o referencias de conexión , también debe administrar el mantenimiento de esos tipos incrustados.

El *tipo de conexión no* puede ser un puntero de interfaz ni un puntero completo. El *tipo de conexión* debe tener un tamaño de memoria bien definido. Consulte [Reglas de serialización para la serialización de usuarios y \_ \_](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) la serialización de conexión para obtener más información sobre cómo serializar un tipo *de conexión determinado.*

*Userm-type no* debe ser un puntero de interfaz, ya que se pueden serializar directamente. Si el tipo de usuario es un puntero completo, debe administrar el alias usted mismo.

## <a name="examples"></a>Ejemplos

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[Atributo de \_ serialización de usuario](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[**wire \_ marshal**](wire-marshal.md)
</dt> <dt>

[**GetGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 