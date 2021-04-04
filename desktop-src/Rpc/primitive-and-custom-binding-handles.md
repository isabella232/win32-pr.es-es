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
# <a name="primitive-and-custom-binding-handles"></a><span data-ttu-id="dc09c-103">Identificadores de enlace primitivos y personalizados</span><span class="sxs-lookup"><span data-stu-id="dc09c-103">Primitive and Custom Binding Handles</span></span>

<span data-ttu-id="dc09c-104">Todos los identificadores declarados con los tipos de [**\_ \_ identificador de enlace**](rpc-binding-handle.md) de [identificador \_ t](/windows/desktop/Midl/handle-t) o RPC son identificadores de enlace primitivos.</span><span class="sxs-lookup"><span data-stu-id="dc09c-104">All handles declared with the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types are primitive binding handles.</span></span> <span data-ttu-id="dc09c-105">Puede extender los tipos de identificador de [**\_ enlace \_**](rpc-binding-handle.md) de [identificador \_ t](/windows/desktop/Midl/handle-t) o RPC para incluir información más o diferente de la que contiene el tipo de controlador primitivo.</span><span class="sxs-lookup"><span data-stu-id="dc09c-105">You can extend the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types to include more or different information than the primitive handle type contains.</span></span> <span data-ttu-id="dc09c-106">Al hacerlo, se crea un identificador de enlace personalizado.</span><span class="sxs-lookup"><span data-stu-id="dc09c-106">When you do, you create a custom binding handle.</span></span>

<span data-ttu-id="dc09c-107">Para hacer un identificador de enlace personalizado para la aplicación distribuida, deberá crear su propio tipo de datos y especificar el \[ atributo [Handle](/windows/desktop/Midl/handle) \] en una definición de tipo en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="dc09c-107">To make a custom binding handle for your distributed application, you will need to create your own data type and specify the \[ [handle](/windows/desktop/Midl/handle)\] attribute on a type definition in your IDL file.</span></span> <span data-ttu-id="dc09c-108">En última instancia, los archivos de código auxiliar asignan los identificadores de enlace personalizados a los identificadores primitivos.</span><span class="sxs-lookup"><span data-stu-id="dc09c-108">Ultimately, the stub files map custom binding handles to primitive handles.</span></span>

<span data-ttu-id="dc09c-109">Si crea su propio tipo de identificador de enlace, también debe proporcionar rutinas de enlace y desenlace que el código auxiliar de cliente use para asignar un identificador personalizado a un identificador primitivo.</span><span class="sxs-lookup"><span data-stu-id="dc09c-109">If you do create your own binding handle type, you must also supply bind and unbind routines that the client stub uses to map a custom handle to a primitive handle.</span></span> <span data-ttu-id="dc09c-110">El código auxiliar llama a las rutinas de enlace y desenlace al principio y al final de cada llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="dc09c-110">The stub calls your bind and unbind routines at the beginning and end of each remote procedure call.</span></span> <span data-ttu-id="dc09c-111">Las rutinas de enlace y desenlace deben ajustarse a los siguientes prototipos de función.</span><span class="sxs-lookup"><span data-stu-id="dc09c-111">The bind and unbind routines must conform to the following function prototypes.</span></span>



| <span data-ttu-id="dc09c-112">Prototipo de función</span><span class="sxs-lookup"><span data-stu-id="dc09c-112">Function prototype</span></span>                     | <span data-ttu-id="dc09c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc09c-113">Description</span></span>       |
|----------------------------------------|-------------------|
| <span data-ttu-id="dc09c-114">Handle \_ t Type \_ BIND (*tipo*)</span><span class="sxs-lookup"><span data-stu-id="dc09c-114">handle\_t type\_bind(*type*)</span></span>           | <span data-ttu-id="dc09c-115">Rutina de enlace</span><span class="sxs-lookup"><span data-stu-id="dc09c-115">Binding routine</span></span>   |
| <span data-ttu-id="dc09c-116">void Type \_ unbind (*Type*, *Handle \_ t*)</span><span class="sxs-lookup"><span data-stu-id="dc09c-116">void type\_unbind(*type*, *handle\_t*)</span></span> | <span data-ttu-id="dc09c-117">Desenlazar rutina</span><span class="sxs-lookup"><span data-stu-id="dc09c-117">Unbinding routine</span></span> |



 

<span data-ttu-id="dc09c-118">En el ejemplo siguiente se muestra cómo se puede definir un identificador de enlace personalizado en el archivo IDL:</span><span class="sxs-lookup"><span data-stu-id="dc09c-118">The following example shows how a custom binding handle can be defined in the IDL file:</span></span>

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

<span data-ttu-id="dc09c-119">Si la rutina de enlace detecta un error, debería producir una excepción mediante la función [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) .</span><span class="sxs-lookup"><span data-stu-id="dc09c-119">If the bind routine encounters an error, it should raise an exception using the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) function.</span></span> <span data-ttu-id="dc09c-120">El código auxiliar del cliente se limpiará y dejará que la excepción filtre por el bloque de excepciones que rodea la llamada a procedimiento remoto en el lado cliente.</span><span class="sxs-lookup"><span data-stu-id="dc09c-120">The client stub will then clean up, and let the exception filter through to the exception block surrounding the remote procedure call on the client side.</span></span> <span data-ttu-id="dc09c-121">Si la rutina BIND simplemente devuelve **null**, el código de cliente obtiene un error de \_ \_ enlace no válido de RPC S \_ .</span><span class="sxs-lookup"><span data-stu-id="dc09c-121">If the bind routine simply returns **NULL**, the client code gets error RPC\_S\_INVALID\_BINDING.</span></span> <span data-ttu-id="dc09c-122">Aunque esto puede ser aceptable en ciertas situaciones, otras situaciones (como la falta de memoria) no responden bien.</span><span class="sxs-lookup"><span data-stu-id="dc09c-122">While this might be acceptable in certain situations, other situations (such as being out of memory) do not respond well.</span></span> <span data-ttu-id="dc09c-123">La rutina unbind debe diseñarse de modo que no genere ningún error.</span><span class="sxs-lookup"><span data-stu-id="dc09c-123">The unbind routine should be designed so that it does not fail.</span></span> <span data-ttu-id="dc09c-124">La rutina unbind no debe generar excepciones.</span><span class="sxs-lookup"><span data-stu-id="dc09c-124">The unbind routine should not raise exceptions.</span></span>

<span data-ttu-id="dc09c-125">Las rutinas de enlace y desenlace definidas por el programador aparecen en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="dc09c-125">The programmer-defined bind and unbind routines appear in the client application.</span></span> <span data-ttu-id="dc09c-126">En el ejemplo siguiente, la rutina de enlace llama a [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para convertir la información de enlace de cadenas en un identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="dc09c-126">In the following example, the bind routine calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to convert the string-binding information to a binding handle.</span></span> <span data-ttu-id="dc09c-127">La rutina unbind llama a [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) para liberar el identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="dc09c-127">The unbind routine calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to free the binding handle.</span></span>

<span data-ttu-id="dc09c-128">El nombre del identificador de enlace definido por el programador, \_ tipo de identificador \_ de datos, aparece como parte del nombre de las funciones.</span><span class="sxs-lookup"><span data-stu-id="dc09c-128">The name of the programmer-defined binding handle, DATA\_HANDLE\_TYPE, appears as part of the name of the functions.</span></span> <span data-ttu-id="dc09c-129">También se utiliza como el tipo de parámetro en los parámetros de la función.</span><span class="sxs-lookup"><span data-stu-id="dc09c-129">It is also used as the parameter type in the function parameters.</span></span>

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

<span data-ttu-id="dc09c-130">Los identificadores de enlace implícitos y explícitos pueden ser identificadores primitivos o personalizados.</span><span class="sxs-lookup"><span data-stu-id="dc09c-130">Both implicit and explicit binding handles can either be primitive or custom handles.</span></span> <span data-ttu-id="dc09c-131">Es decir, un identificador puede ser:</span><span class="sxs-lookup"><span data-stu-id="dc09c-131">That is, a handle may be:</span></span>

-   <span data-ttu-id="dc09c-132">Primitivo e implícito</span><span class="sxs-lookup"><span data-stu-id="dc09c-132">Primitive and implicit</span></span>
-   <span data-ttu-id="dc09c-133">Personalizado e implícito</span><span class="sxs-lookup"><span data-stu-id="dc09c-133">Custom and implicit</span></span>
-   <span data-ttu-id="dc09c-134">Primitivas y explícitas</span><span class="sxs-lookup"><span data-stu-id="dc09c-134">Primitive and explicit</span></span>
-   <span data-ttu-id="dc09c-135">Personalizado y explícito</span><span class="sxs-lookup"><span data-stu-id="dc09c-135">Custom and explicit</span></span>

 

 