---
title: La función type_UserFree
description: La \_ función type UserFree es una función auxiliar para los atributos \ WIRE \_ Marshal \ y \ User \_ Marshal \.
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791733"
---
# <a name="the-type_userfree-function"></a><span data-ttu-id="e58c9-104">La \_ función type UserFree</span><span class="sxs-lookup"><span data-stu-id="e58c9-104">The type\_UserFree Function</span></span>

<span data-ttu-id="e58c9-105">La función **<type> \_ UserFree** es una función auxiliar para los atributos de serialización de \[ [ \_ conexión](/windows/desktop/Midl/wire-marshal) \] y de cálculo de \[ [ \_ referencias de usuario](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="e58c9-105">The **<type>\_UserFree** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="e58c9-106">El código auxiliar llama a esta función para liberar los datos en el lado del servidor.</span><span class="sxs-lookup"><span data-stu-id="e58c9-106">The stubs call this function to free the data on the server side.</span></span> <span data-ttu-id="e58c9-107">La función se define como:</span><span class="sxs-lookup"><span data-stu-id="e58c9-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

<span data-ttu-id="e58c9-108"><type>En el nombre de la función se entiende el tipo de userm especificado en la definición de la **\[ \_ serialización \] de conexión** o el tipo de cálculo de **\[ \_ referencias \] del usuario** .</span><span class="sxs-lookup"><span data-stu-id="e58c9-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span>

<span data-ttu-id="e58c9-109">El parámetro *pFlags* es un puntero a un campo de marca **larga sin signo** .</span><span class="sxs-lookup"><span data-stu-id="e58c9-109">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="e58c9-110">La palabra superior de la marca contiene marcas de representación de datos NDR tal y como se define en OSF DCE para el punto flotante, el orden de bytes y las representaciones de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e58c9-110">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="e58c9-111">La palabra inferior contiene una marca de contexto de cálculo de referencias tal como la define el canal COM.</span><span class="sxs-lookup"><span data-stu-id="e58c9-111">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="e58c9-112">El diseño exacto de las marcas dentro del campo se describe en [la función de tipo de \_ usuario](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="e58c9-112">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="e58c9-113">El parámetro *pMyObj* es un puntero a un objeto de tipo de usuario.</span><span class="sxs-lookup"><span data-stu-id="e58c9-113">The *pMyObj* parameter is a pointer to a user type object.</span></span> <span data-ttu-id="e58c9-114">El motor NDR libera el objeto de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="e58c9-114">The NDR engine frees the top-level object.</span></span> <span data-ttu-id="e58c9-115">Usted es responsable de liberar los objetos a los que puede apuntar el objeto de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="e58c9-115">You are responsible for freeing any objects to which the top-level object may point.</span></span>

<span data-ttu-id="e58c9-116">Las excepciones deben detectarse y administrarse localmente, las excepciones no se deben permitir que propigated la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="e58c9-116">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e58c9-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e58c9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e58c9-118">Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión</span><span class="sxs-lookup"><span data-stu-id="e58c9-118">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="e58c9-119">\_serialización de cable</span><span class="sxs-lookup"><span data-stu-id="e58c9-119">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="e58c9-120">\_serialización de usuario</span><span class="sxs-lookup"><span data-stu-id="e58c9-120">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 