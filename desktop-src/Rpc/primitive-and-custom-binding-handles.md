---
title: Identificadores de enlace primitivos y personalizados
description: Todos los identificadores declarados con los tipos \_ handle t o RPC BINDING HANDLE son \_ \_ identificadores de enlace primitivos.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0e1d6f7cc2ad4d11e268e0f5c83b0275fcd2677a32303820507272f550b834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019155"
---
# <a name="primitive-and-custom-binding-handles"></a>Identificadores de enlace primitivos y personalizados

Todos los identificadores declarados con los [tipos \_ handle t](/windows/desktop/Midl/handle-t) o RPC BINDING [**\_ \_ HANDLE**](rpc-binding-handle.md) son identificadores de enlace primitivos. Puede extender los tipos [handle \_ t](/windows/desktop/Midl/handle-t) o [**RPC BINDING \_ \_ HANDLE**](rpc-binding-handle.md) para incluir más información o diferente de la que contiene el tipo de identificador primitivo. Cuando lo haga, creará un identificador de enlace personalizado.

Para crear un identificador de enlace personalizado para la aplicación distribuida, deberá crear su propio tipo de datos y especificar el atributo handle en una definición de tipo en el \[ [](/windows/desktop/Midl/handle) \] archivo IDL. En última instancia, los archivos de código auxiliar asignan identificadores de enlace personalizados a identificadores primitivos.

Si crea su propio tipo de identificador de enlace, también debe proporcionar rutinas de enlace y desenlazadas que el código auxiliar de cliente usa para asignar un identificador personalizado a un identificador primitivo. El código auxiliar llama a las rutinas de enlace y desenlazadas al principio y al final de cada llamada a procedimiento remoto. Las rutinas de enlace y desenlazadas deben ajustarse a los siguientes prototipos de función.



| Prototipo de función                     | Descripción       |
|----------------------------------------|-------------------|
| handle \_ t type \_ bind(*type*)           | Rutina de enlace   |
| void type \_ unbind(*type*, *handle \_ t*) | Rutina de desenlace |



 

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

Si la rutina de enlace encuentra un error, debe generar una excepción mediante la [**función RpcRaiseException.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) A continuación, el código auxiliar de cliente se limpiará y permitirá que la excepción se filtre hasta el bloque de excepciones que rodea la llamada a procedimiento remoto en el lado cliente. Si la rutina de enlace simplemente devuelve **NULL,** el código de cliente obtiene el error RPC \_ S INVALID \_ \_ BINDING. Aunque esto puede ser aceptable en determinadas situaciones, otras situaciones (como la falta de memoria) no responden bien. La rutina de desenlazado debe diseñarse para que no se pueda producir un error. La rutina desenlazada no debe generar excepciones.

Las rutinas de enlace y desenlazadas definidas por el programador aparecen en la aplicación cliente. En el ejemplo siguiente, la rutina de enlace llama a [**RpcBindingFromStringBinding para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) convertir la información de enlace de cadena en un identificador de enlace. La rutina sin enlazar llama [**a RpcBindingFree para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) liberar el identificador de enlace.

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

 

 