---
title: user_marshal atributo)
description: El \_ atributo ACF de serialización de usuario asocia un tipo local con nombre en el idioma de destino (userm-Type) con un tipo de transferencia (tipo de conexión) que se transfiere entre el cliente y el servidor.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal el atributo MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358861"
---
# <a name="user_marshal-attribute"></a>\_atributo User Marshal

El atributo ACF de **\_ serialización de usuario** asocia un tipo local con nombre en el idioma de destino (*userm-Type*) con un tipo de transferencia (*tipo de conexión*) que se transfiere entre el cliente y el servidor.

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

*tipo de userm* 
</dt> <dd>

Especifica el identificador del tipo de datos de usuario del que se van a calcular las referencias. No es necesario transmitir el *tipo userm* y no es necesario que sea un tipo conocido para el compilador de MIDL.

</dd> <dt>

*tipo de conexión* 
</dt> <dd>

Especifica el tipo de datos de transferencia con nombre que se transfiere realmente entre el cliente y el servidor. El tipo de conexión debe ser un tipo base de MIDL, un tipo predefinido o un identificador de tipo de un tipo que se pueda transmitir a través de la red.

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

Especifica un puntero a un objeto de *\_ tipo userm*.

</dd> <dt>

*Buffer* 
</dt> <dd>

Especifica el puntero de búfer actual.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cada tipo local con nombre, *userm-Type*, tiene una correspondencia uno a uno con un *tipo de conexión* que define la representación de la conexión del tipo. Debe proporcionar rutinas para ajustar el tamaño de los datos para el cálculo de referencias, para calcular las referencias de los datos y para deserializarlos, y para liberar memoria. Para obtener más información sobre estas rutinas, vea [el \_ atributo User Marshal](/windows/desktop/Rpc/the-user-marshal-attribute). Tenga en cuenta que si hay tipos incrustados en los datos que también se definen con serialización de **usuario \_** o \[ [**\[ \_ serialización \] de conexión**](wire-marshal.md), también debe administrar el servicio de esos tipos incrustados.

El *tipo de conexión* no puede ser un puntero de interfaz ni un puntero completo. El *tipo de conexión* debe tener un tamaño de memoria bien definido. Vea [serialización de reglas para la serialización de usuarios \_ y \_ serialización de conexión](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) para más información sobre cómo calcular las referencias de un *tipo de conexión* determinado.

El *tipo de userm* no debe ser un puntero de interfaz, ya que estas referencias se pueden calcular directamente. Si el tipo de usuario es un puntero completo, debe administrar el alias.

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

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**tal**](long.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**sin signo**](unsigned.md)
</dt> <dt>

[Atributo User \_ Marshal](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[**\_serialización de cable**](wire-marshal.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 