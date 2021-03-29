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
# <a name="implicit-binding-handles"></a><span data-ttu-id="c261e-103">Identificadores de enlace implícitos</span><span class="sxs-lookup"><span data-stu-id="c261e-103">Implicit Binding Handles</span></span>

<span data-ttu-id="c261e-104">Los identificadores de enlace implícitos permiten a la aplicación seleccionar un servidor específico para ejecutar sus llamadas a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="c261e-104">Implicit binding handles allow your application to select a specific server to execute its remote procedure calls.</span></span> <span data-ttu-id="c261e-105">Para obtener más información, consulte [enlace de lado cliente](client-side-binding.md).</span><span class="sxs-lookup"><span data-stu-id="c261e-105">For details, see [Client-Side Binding](client-side-binding.md).</span></span> <span data-ttu-id="c261e-106">También permiten que el programa cliente/servidor use enlaces autenticados.</span><span class="sxs-lookup"><span data-stu-id="c261e-106">They also enable your client/server program to use authenticated bindings.</span></span> <span data-ttu-id="c261e-107">Es decir, el cliente puede especificar la información de autenticación en un identificador de enlace implícito.</span><span class="sxs-lookup"><span data-stu-id="c261e-107">That is, the client can specify authentication information in an implicit binding handle.</span></span> <span data-ttu-id="c261e-108">La biblioteca en tiempo de ejecución de RPC utiliza la información de autenticación para establecer una sesión RPC autenticada entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="c261e-108">The RPC run-time library uses the authentication information to establish an authenticated RPC session between the client and the server.</span></span> <span data-ttu-id="c261e-109">Para obtener más información, consulte [Seguridad](security.md).</span><span class="sxs-lookup"><span data-stu-id="c261e-109">For more information, see [Security](security.md).</span></span>

> [!Note]  
> <span data-ttu-id="c261e-110">Los identificadores de enlace implícitos no son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c261e-110">Implicit binding handles are not thread safe.</span></span> <span data-ttu-id="c261e-111">Por lo tanto, las aplicaciones multiproceso deben evitar el uso de identificadores de enlace implícitos.</span><span class="sxs-lookup"><span data-stu-id="c261e-111">Multi-threaded applications therefore should avoid using implicit binding handles.</span></span>

 

<span data-ttu-id="c261e-112">Cuando la aplicación utiliza enlaces implícitos, el cliente debe establecer la información de enlace para que pueda crear el enlace.</span><span class="sxs-lookup"><span data-stu-id="c261e-112">When your application uses implicit bindings, the client must set the binding information so that it can create the binding.</span></span> <span data-ttu-id="c261e-113">Una vez que el cliente crea un enlace implícito, no es necesario pasar ningún manipulador de enlace a los procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="c261e-113">After the client creates an implicit binding, it does not need to pass any binding handles to remote procedures.</span></span> <span data-ttu-id="c261e-114">La biblioteca RPC controla el resto de la mecánica de la sesión de comunicación.</span><span class="sxs-lookup"><span data-stu-id="c261e-114">The RPC library handles the rest of the mechanics of the communication session.</span></span>

<span data-ttu-id="c261e-115">El cliente almacena la información de enlace de un identificador implícito en una variable global.</span><span class="sxs-lookup"><span data-stu-id="c261e-115">The client stores the binding information for an implicit handle in a global variable.</span></span> <span data-ttu-id="c261e-116">Cuando el compilador MIDL genera el archivo de encabezado y el código auxiliar de cliente a partir de la especificación de interfaz del archivo MIDL, también genera código para una variable de identificador de enlace global.</span><span class="sxs-lookup"><span data-stu-id="c261e-116">When the MIDL compiler generates the client stub and header file from the interface specification in your MIDL file, it also generates code for a global binding handle variable.</span></span> <span data-ttu-id="c261e-117">El programa cliente inicializa el identificador y, a continuación, no hace referencia a él de nuevo hasta que destruye el enlace.</span><span class="sxs-lookup"><span data-stu-id="c261e-117">Your client program initializes the handle and then does not refer to it again until it destroys the binding.</span></span>

<span data-ttu-id="c261e-118">Cree un identificador implícito especificando el \[ atributo de [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) \] en el ACF para una interfaz de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="c261e-118">You create an implicit handle by specifying the \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] attribute in the ACF for an interface as follows:</span></span>

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

<span data-ttu-id="c261e-119">El **tipo \_ t de identificador** , que se utiliza en el ejemplo anterior, es un tipo de datos MIDL que se usa para definir los identificadores de enlace.</span><span class="sxs-lookup"><span data-stu-id="c261e-119">The **handle\_t** type, which is used in the preceding example, is a MIDL data type used for defining binding handles.</span></span>

<span data-ttu-id="c261e-120">Después de crear el identificador implícito, la aplicación debe usarlo como parámetro para las funciones de la biblioteca en tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="c261e-120">After creating the implicit handle, the application needs to use it as a parameter to the RPC run-time library functions.</span></span> <span data-ttu-id="c261e-121">No utilice el identificador implícito como parámetro para llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="c261e-121">Do not use the implicit handle as a parameter to remote procedure calls.</span></span> <span data-ttu-id="c261e-122">En el siguiente ejemplo de código se muestra el uso de identificadores de enlace implícitos.</span><span class="sxs-lookup"><span data-stu-id="c261e-122">The following code sample demonstrates the use of implicit binding handles.</span></span>

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

<span data-ttu-id="c261e-123">En el ejemplo anterior, las funciones de la biblioteca en tiempo de ejecución de RPC [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) y [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) requirieron que el identificador de enlace implícito se pasara en las listas de parámetros.</span><span class="sxs-lookup"><span data-stu-id="c261e-123">In the preceding example, the RPC run-time library functions [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) and [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) both required the implicit binding handle to be passed in their parameter lists.</span></span> <span data-ttu-id="c261e-124">Sin embargo, el procedimiento remoto MyRemoteProcedure no lo hizo, ya que no es una función de biblioteca en tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="c261e-124">However, the remote procedure MyRemoteProcedure did not, since it is not an RPC run-time library function.</span></span>

 

 