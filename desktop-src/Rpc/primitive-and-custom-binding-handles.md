---
title: Identificadores de enlace primitivos y personalizados
description: Todos los identificadores declarados con los tipos de identificador de enlace de identificador \_ t o RPC \_ \_ son identificadores de enlace primitivos.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d496a9a54ba0ee7b9552326f7c4dc15792a72bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078253"
---
# <a name="primitive-and-custom-binding-handles"></a>Identificadores de enlace primitivos y personalizados

Todos los identificadores declarados con los tipos de [**\_ \_ identificador de enlace**](rpc-binding-handle.md) de [identificador \_ t](/windows/desktop/Midl/handle-t) o RPC son identificadores de enlace primitivos. Puede extender los tipos de identificador de [**\_ enlace \_**](rpc-binding-handle.md) de [identificador \_ t](/windows/desktop/Midl/handle-t) o RPC para incluir información más o diferente de la que contiene el tipo de controlador primitivo. Al hacerlo, se crea un identificador de enlace personalizado.

Para hacer un identificador de enlace personalizado para la aplicación distribuida, deberá crear su propio tipo de datos y especificar el \[ atributo [Handle](/windows/desktop/Midl/handle) \] en una definición de tipo en el archivo IDL. En última instancia, los archivos de código auxiliar asignan los identificadores de enlace personalizados a los identificadores primitivos.

Si crea su propio tipo de identificador de enlace, también debe proporcionar rutinas de enlace y desenlace que el código auxiliar de cliente use para asignar un identificador personalizado a un identificador primitivo. El código auxiliar llama a las rutinas de enlace y desenlace al principio y al final de cada llamada a procedimiento remoto. Las rutinas de enlace y desenlace deben ajustarse a los siguientes prototipos de función.



| Prototipo de función                     | Descripción       |
|----------------------------------------|-------------------|
| Handle \_ t Type \_ BIND (*tipo*)           | Rutina de enlace   |
| void Type \_ unbind (*Type*, *Handle \_ t*) | Desenlazar rutina |



 

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

Si la rutina de enlace detecta un error, debería producir una excepción mediante la función [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) . El código auxiliar del cliente se limpiará y dejará que la excepción filtre por el bloque de excepciones que rodea la llamada a procedimiento remoto en el lado cliente. Si la rutina BIND simplemente devuelve **null**, el código de cliente obtiene un error de \_ \_ enlace no válido de RPC S \_ . Aunque esto puede ser aceptable en ciertas situaciones, otras situaciones (como la falta de memoria) no responden bien. La rutina unbind debe diseñarse de modo que no genere ningún error. La rutina unbind no debe generar excepciones.

Las rutinas de enlace y desenlace definidas por el programador aparecen en la aplicación cliente. En el ejemplo siguiente, la rutina de enlace llama a [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para convertir la información de enlace de cadenas en un identificador de enlace. La rutina unbind llama a [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) para liberar el identificador de enlace.

El nombre del identificador de enlace definido por el programador, \_ tipo de identificador \_ de datos, aparece como parte del nombre de las funciones. También se utiliza como el tipo de parámetro en los parámetros de la función.

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

Los identificadores de enlace implícitos y explícitos pueden ser identificadores primitivos o personalizados. Es decir, un identificador puede ser:

-   Primitivo e implícito
-   Personalizado e implícito
-   Primitivas y explícitas
-   Personalizado y explícito

 

 