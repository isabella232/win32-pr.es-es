---
title: atributo handle
description: El atributo \ handle\ especifica un atributo definido por el usuario o \ 0034;customized \ 0034; tipo de identificador.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- handle attribute MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159568"
---
# <a name="handle-attribute"></a>atributo handle

El \[ **atributo** \] handle especifica un tipo de identificador definido por el usuario o "personalizado".

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Typename* 
</dt> <dd>

Especifica el nombre del tipo de identificador de enlace definido por el usuario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los identificadores definidos por el usuario permiten a los desarrolladores diseñar identificadores significativos para la aplicación. Un identificador definido por el usuario solo se puede definir en una declaración de tipo, no en un declarador de función.

Un parámetro de un tipo definido por el atributo handle se usa para determinar el enlace de la llamada y se \[  \] transmite al procedimiento llamado.

El usuario debe proporcionar rutinas de enlace y desenlace para convertir entre tipos de identificador primitivos y definidos por el usuario. Dado un identificador definido por el usuario de tipo *typename*, el usuario debe proporcionar las rutinas *typename* bind y \_  *typename* \_ **unbind**. Por ejemplo, si el tipo de identificador definido por el usuario se denomina MYHANDLE, las rutinas se denominan enlace MYHANDLE y \_  MYHANDLE \_ **desenlazado.**

Si se realiza correctamente, *la rutina de enlace typename* debe devolver un identificador de enlace primitivo \_  válido. Si no se realiza correctamente, la rutina debe devolver un **valor NULL.** Si la rutina devuelve **NULL**, no se llamará a la rutina unbind *typename.* \_  Si la rutina de enlace devuelve un identificador de enlace no válido diferente de **NULL,** el comportamiento del código auxiliar no está definido.

Cuando el procedimiento remoto tiene un identificador definido por el usuario como parámetro o como identificador implícito, los códigos auxiliares de cliente llaman a la rutina de enlace antes de llamar al procedimiento remoto. Los códigos auxiliares de cliente llaman a la rutina de desenlace después de la llamada remota.

En DCE IDL, un parámetro con el atributo handle debe aparecer como primer \[  \] parámetro en la lista de argumentos del procedimiento remoto. Los parámetros posteriores, incluidos \[ **otros atributos de** \] identificador, se tratan como parámetros normales. Microsoft admite una extensión para DCE IDL que permite que el parámetro de identificador definido por el usuario aparezca en posiciones que \[  \] no son el primer parámetro.

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

[Enlace y identificadores](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**identificador \_ implícito**](implicit-handle.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 