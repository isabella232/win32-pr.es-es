---
title: Identificadores de enlace implícitos
description: Los identificadores de enlace implícitos permiten a la aplicación seleccionar un servidor específico para ejecutar sus llamadas a procedimiento remoto.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fda8501224d66518ad2e86f13fb769c4b2fa0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077862"
---
# <a name="implicit-binding-handles"></a>Identificadores de enlace implícitos

Los identificadores de enlace implícitos permiten a la aplicación seleccionar un servidor específico para ejecutar sus llamadas a procedimiento remoto. Para obtener más información, consulte [enlace de lado cliente](client-side-binding.md). También permiten que el programa cliente/servidor use enlaces autenticados. Es decir, el cliente puede especificar la información de autenticación en un identificador de enlace implícito. La biblioteca en tiempo de ejecución de RPC utiliza la información de autenticación para establecer una sesión RPC autenticada entre el cliente y el servidor. Para obtener más información, consulte [Seguridad](security.md).

> [!Note]  
> Los identificadores de enlace implícitos no son seguros para subprocesos. Por lo tanto, las aplicaciones multiproceso deben evitar el uso de identificadores de enlace implícitos.

 

Cuando la aplicación utiliza enlaces implícitos, el cliente debe establecer la información de enlace para que pueda crear el enlace. Una vez que el cliente crea un enlace implícito, no es necesario pasar ningún manipulador de enlace a los procedimientos remotos. La biblioteca RPC controla el resto de la mecánica de la sesión de comunicación.

El cliente almacena la información de enlace de un identificador implícito en una variable global. Cuando el compilador MIDL genera el archivo de encabezado y el código auxiliar de cliente a partir de la especificación de interfaz del archivo MIDL, también genera código para una variable de identificador de enlace global. El programa cliente inicializa el identificador y, a continuación, no hace referencia a él de nuevo hasta que destruye el enlace.

Cree un identificador implícito especificando el \[ atributo de [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) \] en el ACF para una interfaz de la manera siguiente:

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

El **tipo \_ t de identificador** , que se utiliza en el ejemplo anterior, es un tipo de datos MIDL que se usa para definir los identificadores de enlace.

Después de crear el identificador implícito, la aplicación debe usarlo como parámetro para las funciones de la biblioteca en tiempo de ejecución de RPC. No utilice el identificador implícito como parámetro para llamadas a procedimientos remotos. En el siguiente ejemplo de código se muestra el uso de identificadores de enlace implícitos.

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

En el ejemplo anterior, las funciones de la biblioteca en tiempo de ejecución de RPC [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) y [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) requirieron que el identificador de enlace implícito se pasara en las listas de parámetros. Sin embargo, el procedimiento remoto MyRemoteProcedure no lo hizo, ya que no es una función de biblioteca en tiempo de ejecución de RPC.

 

 