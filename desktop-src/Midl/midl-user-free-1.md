---
title: midl_user_free atributo)
description: La función gratuita de usuario de MIDL la \_ \_ proporcionan las aplicaciones de cliente y servidor para desasignar la memoria asignada dinámicamente.
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free el atributo MIDL
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358896"
---
# <a name="midl_user_free-attribute"></a><span data-ttu-id="c55e2-104">\_atributo Free de usuario de MIDL \_</span><span class="sxs-lookup"><span data-stu-id="c55e2-104">midl\_user\_free attribute</span></span>

<span data-ttu-id="c55e2-105">La **función \_ \_ gratuita de usuario de MIDL** la proporcionan las aplicaciones de cliente y servidor para desasignar la memoria asignada dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="c55e2-105">The **midl\_user\_free** function is provided by client and server applications to deallocate dynamically allocated memory.</span></span>

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a><span data-ttu-id="c55e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c55e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c55e2-107">*m*</span><span class="sxs-lookup"><span data-stu-id="c55e2-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="c55e2-108">Puntero al bloque de memoria que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="c55e2-108">A pointer to the memory block to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c55e2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c55e2-109">Remarks</span></span>

<span data-ttu-id="c55e2-110">Tanto la aplicación cliente como la aplicación de servidor deben implementar la función **\_ \_ gratuita de usuario de MIDL** , a menos que esté compilando en modo de compatibilidad de OSF ([**/OSF**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="c55e2-110">Both client application and server application must implement the **midl\_user\_free** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="c55e2-111">La **función \_ \_ gratuita de usuario de MIDL** debe ser capaz de liberar todo el almacenamiento asignado por el usuario de la [**\_ \_ asignación de MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span><span class="sxs-lookup"><span data-stu-id="c55e2-111">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span>

<span data-ttu-id="c55e2-112">Las aplicaciones y los códigos auxiliares llaman al **usuario de MIDL \_ \_ gratis** al tratar con objetos a los que hacen referencia los punteros:</span><span class="sxs-lookup"><span data-stu-id="c55e2-112">Applications and stubs call **midl\_user\_free** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="c55e2-113">La aplicación de servidor debe llamar al **usuario de MIDL \_ \_ Free** para liberar memoria asignada por aplicación € ", por ejemplo, al eliminar un nodo especificado.</span><span class="sxs-lookup"><span data-stu-id="c55e2-113">The server application should call **midl\_user\_free** to free memory allocated by the applicationâ€”for example, when deleting a specified node.</span></span>
-   <span data-ttu-id="c55e2-114">El código auxiliar del servidor llama **\_ \_ gratuitamente al usuario de MIDL** para liberar memoria en el servidor después de calcular las referencias de todos los **\[** [](out-idl.md) **\]** argumentos de salida, **\[** [**en**](in.md), los argumentos de **salida \]** y el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c55e2-114">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all **\[**[**out**](out-idl.md)**\]** arguments, **\[**[**in**](in.md), **out\]** arguments, and the return value.</span></span>

## <a name="examples"></a><span data-ttu-id="c55e2-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c55e2-115">Examples</span></span>


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a><span data-ttu-id="c55e2-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="c55e2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c55e2-117">**matrices**</span><span class="sxs-lookup"><span data-stu-id="c55e2-117">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="c55e2-118">Matrices y punteros</span><span class="sxs-lookup"><span data-stu-id="c55e2-118">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="c55e2-119">Atributos array y Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="c55e2-119">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="c55e2-120">**de**</span><span class="sxs-lookup"><span data-stu-id="c55e2-120">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="c55e2-121">**\_asignación de usuarios de MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="c55e2-121">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="c55e2-122">**/osf**</span><span class="sxs-lookup"><span data-stu-id="c55e2-122">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="c55e2-123">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="c55e2-123">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="c55e2-124">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="c55e2-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 