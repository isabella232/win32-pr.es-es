---
title: atributo Handle
description: El atributo \ Handle \ especifica un definido por el usuario o \ 0034; personalizado \ 0034; tipo de identificador.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- identificador del atributo MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904602"
---
# <a name="handle-attribute"></a>atributo Handle

El \[ atributo **Handle** \] especifica un tipo de identificador definido por el usuario o "personalizado".

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombreDeTipo* 
</dt> <dd>

Especifica el nombre del tipo de identificador de enlace definido por el usuario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los identificadores definidos por el usuario permiten a los desarrolladores diseñar controladores que sean significativos para la aplicación. Un identificador definido por el usuario solo se puede definir en una declaración de tipos, no en un declarador de función.

Un parámetro de un tipo definido por el \[  \] atributo Handle se utiliza para determinar el enlace de la llamada y se transmite al procedimiento llamado.

El usuario debe proporcionar rutinas de enlace y desenlace para realizar la conversión entre tipos primitivos y de identificador definidos por el usuario. Dado un identificador definido por el usuario de tipo *TypeName*, el usuario debe proporcionar las rutinas *TypeName* \_ **BIND** y *TypeName* \_ **unbind**. Por ejemplo, si el tipo de identificador definido por el usuario se denomina MyHandler, las rutinas se denominan MYHANDLER \_ **BIND** y MyHandler \_ **unbind**.

Si se realiza correctamente , la rutina de \_ **enlace** TypeName debe devolver un identificador de enlace primitivo válido. Si no se realiza correctamente, la rutina debe devolver un **valor null**. Si la rutina devuelve **null**,  \_ no se llamará a la rutina TypeName **unbind** . Si la rutina de enlace devuelve un identificador de enlace no válido distinto de **null**, el comportamiento del código auxiliar es indefinido.

Cuando el procedimiento remoto tiene un identificador definido por el usuario como un parámetro o como un identificador implícito, el código auxiliar del cliente llama a la rutina de enlace antes de llamar al procedimiento remoto. El código auxiliar del cliente llama a la rutina de desenlace después de la llamada remota.

En DCE IDL, un parámetro con el \[  \] atributo Handle debe aparecer como el primer parámetro de la lista de argumentos de procedimiento remoto. Los parámetros subsiguientes, incluidos otros \[  \] atributos de identificador, se tratan como parámetros ordinarios. Microsoft admite una extensión de DCE IDL que permite que el parámetro de identificador definido por el usuario \[  \] aparezca en posiciones distintas del primer parámetro.

## <a name="examples"></a>Ejemplos

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Enlace y controladores](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 