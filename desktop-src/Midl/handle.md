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
# <a name="handle-attribute"></a><span data-ttu-id="708c2-104">atributo Handle</span><span class="sxs-lookup"><span data-stu-id="708c2-104">handle attribute</span></span>

<span data-ttu-id="708c2-105">El \[ atributo **Handle** \] especifica un tipo de identificador definido por el usuario o "personalizado".</span><span class="sxs-lookup"><span data-stu-id="708c2-105">The \[**handle**\] attribute specifies a user-defined or "customized" handle type.</span></span>

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a><span data-ttu-id="708c2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="708c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="708c2-107">*nombreDeTipo*</span><span class="sxs-lookup"><span data-stu-id="708c2-107">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="708c2-108">Especifica el nombre del tipo de identificador de enlace definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="708c2-108">Specifies the name of the user-defined binding-handle type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="708c2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="708c2-109">Remarks</span></span>

<span data-ttu-id="708c2-110">Los identificadores definidos por el usuario permiten a los desarrolladores diseñar controladores que sean significativos para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="708c2-110">User-defined handles permit developers to design handles that are meaningful to the application.</span></span> <span data-ttu-id="708c2-111">Un identificador definido por el usuario solo se puede definir en una declaración de tipos, no en un declarador de función.</span><span class="sxs-lookup"><span data-stu-id="708c2-111">A user-defined handle can only be defined in a type declaration, not in a function declarator.</span></span>

<span data-ttu-id="708c2-112">Un parámetro de un tipo definido por el \[  \] atributo Handle se utiliza para determinar el enlace de la llamada y se transmite al procedimiento llamado.</span><span class="sxs-lookup"><span data-stu-id="708c2-112">A parameter of a type defined by the \[**handle**\] attribute is used to determine the binding for the call and is transmitted to the called procedure.</span></span>

<span data-ttu-id="708c2-113">El usuario debe proporcionar rutinas de enlace y desenlace para realizar la conversión entre tipos primitivos y de identificador definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="708c2-113">The user must provide binding and unbinding routines to convert between primitive and user-defined handle types.</span></span> <span data-ttu-id="708c2-114">Dado un identificador definido por el usuario de tipo *TypeName*, el usuario debe proporcionar las rutinas *TypeName* \_ **BIND** y *TypeName* \_ **unbind**.</span><span class="sxs-lookup"><span data-stu-id="708c2-114">Given a user-defined handle of type *typename*, the user must supply the routines *typename*\_**bind** and *typename*\_**unbind**.</span></span> <span data-ttu-id="708c2-115">Por ejemplo, si el tipo de identificador definido por el usuario se denomina MyHandler, las rutinas se denominan MYHANDLER \_ **BIND** y MyHandler \_ **unbind**.</span><span class="sxs-lookup"><span data-stu-id="708c2-115">For example, if the user-defined handle type is named MYHANDLE, the routines are named MYHANDLE\_**bind** and MYHANDLE\_**unbind**.</span></span>

<span data-ttu-id="708c2-116">Si se realiza correctamente , la rutina de \_ **enlace** TypeName debe devolver un identificador de enlace primitivo válido.</span><span class="sxs-lookup"><span data-stu-id="708c2-116">If successful, the *typename*\_**bind** routine should return a valid primitive binding handle.</span></span> <span data-ttu-id="708c2-117">Si no se realiza correctamente, la rutina debe devolver un **valor null**.</span><span class="sxs-lookup"><span data-stu-id="708c2-117">If unsuccessful, the routine should return a **NULL**.</span></span> <span data-ttu-id="708c2-118">Si la rutina devuelve **null**,  \_ no se llamará a la rutina TypeName **unbind** .</span><span class="sxs-lookup"><span data-stu-id="708c2-118">If the routine returns **NULL**, the *typename*\_**unbind** routine will not be called.</span></span> <span data-ttu-id="708c2-119">Si la rutina de enlace devuelve un identificador de enlace no válido distinto de **null**, el comportamiento del código auxiliar es indefinido.</span><span class="sxs-lookup"><span data-stu-id="708c2-119">If the binding routine returns an invalid binding handle different from **NULL**, the stub behavior is undefined.</span></span>

<span data-ttu-id="708c2-120">Cuando el procedimiento remoto tiene un identificador definido por el usuario como un parámetro o como un identificador implícito, el código auxiliar del cliente llama a la rutina de enlace antes de llamar al procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="708c2-120">When the remote procedure has a user-defined handle as a parameter or as an implicit handle, the client stubs call the binding routine before calling the remote procedure.</span></span> <span data-ttu-id="708c2-121">El código auxiliar del cliente llama a la rutina de desenlace después de la llamada remota.</span><span class="sxs-lookup"><span data-stu-id="708c2-121">The client stubs call the unbinding routine after the remote call.</span></span>

<span data-ttu-id="708c2-122">En DCE IDL, un parámetro con el \[  \] atributo Handle debe aparecer como el primer parámetro de la lista de argumentos de procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="708c2-122">In DCE IDL, a parameter with the \[**handle**\] attribute must appear as the first parameter in the remote procedure argument list.</span></span> <span data-ttu-id="708c2-123">Los parámetros subsiguientes, incluidos otros \[  \] atributos de identificador, se tratan como parámetros ordinarios.</span><span class="sxs-lookup"><span data-stu-id="708c2-123">Subsequent parameters, including other \[**handle**\] attributes, are treated as ordinary parameters.</span></span> <span data-ttu-id="708c2-124">Microsoft admite una extensión de DCE IDL que permite que el parámetro de identificador definido por el usuario \[  \] aparezca en posiciones distintas del primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="708c2-124">Microsoft supports an extension to DCE IDL that allows the user-defined \[**handle**\] parameter to appear in positions other than the first parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="708c2-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="708c2-125">Examples</span></span>

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a><span data-ttu-id="708c2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="708c2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="708c2-127">Enlace y controladores</span><span class="sxs-lookup"><span data-stu-id="708c2-127">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="708c2-128">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="708c2-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="708c2-129">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="708c2-129">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="708c2-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="708c2-130">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 