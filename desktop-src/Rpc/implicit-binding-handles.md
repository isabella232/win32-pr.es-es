---
title: Identificadores de enlace implícitos
description: Los identificadores de enlace implícitos permiten a la aplicación seleccionar un servidor específico para ejecutar sus llamadas a procedimiento remoto.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fda8501224d66518ad2e86f13fb769c4b2fa0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244635"
---
# <a name="implicit-binding-handles"></a>Identificadores de enlace implícitos

Los identificadores de enlace implícitos permiten a la aplicación seleccionar un servidor específico para ejecutar sus llamadas a procedimiento remoto. Para obtener más información, [vea Enlace del lado cliente.](client-side-binding.md) También permiten que el programa cliente/servidor use enlaces autenticados. Es decir, el cliente puede especificar información de autenticación en un identificador de enlace implícito. La biblioteca en tiempo de ejecución de RPC usa la información de autenticación para establecer una sesión RPC autenticada entre el cliente y el servidor. Para obtener más información, consulte [Seguridad](security.md).

> [!Note]  
> Los identificadores de enlace implícitos no son seguros para subprocesos. Por lo tanto, las aplicaciones multiproceso deben evitar el uso de identificadores de enlace implícitos.

 

Cuando la aplicación usa enlaces implícitos, el cliente debe establecer la información de enlace para que pueda crear el enlace. Una vez que el cliente crea un enlace implícito, no es necesario pasar ningún identificador de enlace a procedimientos remotos. La biblioteca RPC controla el resto de los mecanismos de la sesión de comunicación.

El cliente almacena la información de enlace para un identificador implícito en una variable global. Cuando el compilador MIDL genera el código auxiliar de cliente y el archivo de encabezado a partir de la especificación de interfaz en el archivo MIDL, también genera código para una variable de identificador de enlace global. El programa cliente inicializa el identificador y, a continuación, no hace referencia a él de nuevo hasta que destruye el enlace.

Para crear un identificador implícito, especifique el \[ [**atributo de \_ identificador**](/windows/desktop/Midl/implicit-handle) implícito en \] el ACF para una interfaz como se muestra a continuación:

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

El **tipo de identificador \_ t,** que se usa en el ejemplo anterior, es un tipo de datos MIDL que se usa para definir identificadores de enlace.

Después de crear el identificador implícito, la aplicación debe usarlo como parámetro para las funciones de la biblioteca en tiempo de ejecución de RPC. No use el identificador implícito como parámetro para las llamadas a procedimiento remoto. En el ejemplo de código siguiente se muestra el uso de identificadores de enlace implícitos.

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

En el ejemplo anterior, las funciones de biblioteca en tiempo de ejecución RPC [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) y [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) requerían que se pasara el identificador de enlace implícito en sus listas de parámetros. Sin embargo, el procedimiento remoto MyRemoteProcedure no lo hizo, ya que no es una función de biblioteca en tiempo de ejecución de RPC.

 

 