---
title: Identificadores de enlace primitivos y personalizados
description: Todos los identificadores declarados con los tipos handle t o \_ RPC BINDING HANDLE son \_ \_ identificadores de enlace primitivos.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d496a9a54ba0ee7b9552326f7c4dc15792a72bce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265548"
---
# <a name="primitive-and-custom-binding-handles"></a>Identificadores de enlace primitivos y personalizados

Todos los identificadores declarados con los [tipos \_ handle t](/windows/desktop/Midl/handle-t) o RPC BINDING [**\_ \_ HANDLE**](rpc-binding-handle.md) son identificadores de enlace primitivos. Puede extender los tipos [handle \_ t](/windows/desktop/Midl/handle-t) o [**RPC BINDING \_ \_ HANDLE**](rpc-binding-handle.md) para incluir más información o diferente de la que contiene el tipo de identificador primitivo. Al hacerlo, se crea un identificador de enlace personalizado.

Para crear un identificador de enlace personalizado para la aplicación distribuida, deberá crear su propio tipo de datos y especificar el atributo handle en una definición de tipo en el \[ [](/windows/desktop/Midl/handle) \] archivo IDL. En última instancia, los archivos de código auxiliar asignan identificadores de enlace personalizados a identificadores primitivos.

Si crea su propio tipo de identificador de enlace, también debe proporcionar rutinas de enlace y desenlazadas que el código auxiliar del cliente usa para asignar un identificador personalizado a un identificador primitivo. El código auxiliar llama a las rutinas de enlace y desenlazadas al principio y al final de cada llamada a procedimiento remoto. Las rutinas de enlace y desenlazadas deben cumplir los siguientes prototipos de función.



| Prototipo de función                     | Descripción       |
|----------------------------------------|-------------------|
| handle \_ t type \_ bind(*type*)           | Rutina de enlace   |
| void type \_ unbind(*type*, *handle \_ t*) | Desenlace de rutina |



 

En el ejemplo siguiente se muestra cómo se puede definir un identificador de enlace personalizado en el archivo IDL:

``` syntax
/* usrdef.idl */
[
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0),
  pointer_default(unique)
]
interface usrdef
{
  typedef struct _DATA_TYPE 
  {
      unsigned char * pszUuid;
      unsigned char * pszProtocolSequence;
      unsigned char * pszNetworkAddress;
      unsigned char * pszEndpoint;
      unsigned char * pszOptions;
  } DATA_TYPE;
 
  typedef [handle] DATA_TYPE * DATA_HANDLE_TYPE;
  void UsrdefProc([in] DATA_HANDLE_TYPE  hBinding,
                  [in, string] unsigned char *   pszString);
 
  void Shutdown([in] DATA_HANDLE_TYPE hBinding);
}
```

Si la rutina de enlace encuentra un error, debe generar una excepción mediante la [**función RpcRaiseException.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) A continuación, el código auxiliar del cliente se limpiará y permitirá que la excepción se filtre hasta el bloque de excepciones que rodea la llamada a procedimiento remoto en el lado cliente. Si la rutina de enlace simplemente devuelve **NULL,** el código de cliente obtiene el error RPC \_ S INVALID \_ \_ BINDING. Aunque esto puede ser aceptable en determinadas situaciones, otras situaciones (como la falta de memoria) no responden bien. La rutina de desenlazado debe diseñarse para que no se pueda producir un error. La rutina desenlazada no debe generar excepciones.

Las rutinas de enlace y desenlace definidas por el programador aparecen en la aplicación cliente. En el ejemplo siguiente, la rutina de enlace llama a [**RpcBindingFromStringBinding para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) convertir la información de enlace de cadena en un identificador de enlace. La rutina de desenlace [**llama a RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) para liberar el identificador de enlace.

El nombre del identificador de enlace definido por el programador, DATA HANDLE TYPE, aparece como \_ parte del nombre de las \_ funciones. También se usa como tipo de parámetro en los parámetros de función.

``` syntax
/* The client stub calls this _bind routine at the */
/* beginning of each remote procedure call                */
 
RPC_BINDING_HANDLE __RPC_USER DATA_HANDLE_TYPE_bind(
    DATA_HANDLE_TYPE dh1)
{
    RPC_BINDING_HANDLE hBinding;
    RPC_STATUS status;
 
    unsigned char *pszStringBinding;
 
    status = RpcStringBindingCompose(
          dh1.pszUuid,
          dh1.pszProtocolSequence,
          dh1.pszNetworkAddress,
          dh1.pszEndpoint,
          dh1.pszOptions,
          &pszStringBinding);
          ...
 
    status = RpcBindingFromStringBinding(
          pszStringBinding,
          &hBinding);
          ...
 
    status = RpcStringFree(&pszStringBinding); 
    ...
 
    return(hBinding);
}
 
/* The client stub calls this _unbind routine */
/* after each remote procedure call.                            */
void __RPC_USER DATA_HANDLE_TYPE_unbind(
    DATA_HANDLE_TYPE dh1, 
    RPC_BINDING_HANDLE h1)
{
    RPC_STATUS status;
    status = RpcBindingFree(&h1); 
    ...
}
```

Tanto los identificadores de enlace implícitos como los explícitos pueden ser identificadores primitivos o personalizados. Es decir, un identificador puede ser:

-   Primitivo e implícito
-   Personalizado e implícito
-   Primitivo y explícito
-   Personalizado y explícito

 

 