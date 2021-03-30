---
title: Serialización de reglas para user_marshal y wire_marshal
description: La especificación de OSF-DCE para calcular las referencias de los tipos de puntero incrustados requiere que se respeten las siguientes restricciones a la hora de implementar el tipo de \_ usuarios, escribir \_ UserMarshal y escribir \_ funciones de UserUnMarshal.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4d201f05787ac0b122766ba7fb662532320c43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792795"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a><span data-ttu-id="6919f-103">Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión</span><span class="sxs-lookup"><span data-stu-id="6919f-103">Marshaling Rules for user\_marshal and wire\_marshal</span></span>

<span data-ttu-id="6919f-104">La especificación de OSF-DCE para calcular las referencias de los tipos de puntero incrustados requiere que se respeten las siguientes restricciones al implementar las <type> \_ funciones de usuario, <type> \_ UserMarshal y <type> \_ UserUnMarshal.</span><span class="sxs-lookup"><span data-stu-id="6919f-104">The OSF-DCE specification for marshaling embedded pointer types requires that you observe the following restrictions when implementing the <type>\_UserSize, <type>\_UserMarshal, and <type>\_UserUnMarshal functions.</span></span> <span data-ttu-id="6919f-105">(Las reglas y los ejemplos que se proporcionan aquí son para el cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="6919f-105">(The rules and examples given here are for marshaling.</span></span> <span data-ttu-id="6919f-106">Sin embargo, las rutinas de ajuste de tamaño y de desserialización deben seguir las mismas restricciones:</span><span class="sxs-lookup"><span data-stu-id="6919f-106">However, your sizing and unmarshaling routines must follow the same restrictions):</span></span>

-   <span data-ttu-id="6919f-107">Si el tipo de conexión es un tipo plano sin punteros, la rutina de cálculo de referencias para el tipo de userm correspondiente simplemente debe calcular las referencias de los datos según el diseño del tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="6919f-107">If the wire-type is a flat type with no pointers, your marshaling routine for the corresponding userm-type should simply marshal the data according to the layout of the wire-type.</span></span> <span data-ttu-id="6919f-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6919f-108">For example:</span></span>

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    <span data-ttu-id="6919f-109">Tenga en cuenta que el tipo de conexión, **Long**, es un tipo plano.</span><span class="sxs-lookup"><span data-stu-id="6919f-109">Note that the wire type, **long**, is a flat type.</span></span> <span data-ttu-id="6919f-110">La función UserMarshal de identificador de identificador \_ \_ calcula las referencias de un **valor Long** siempre que \_ se le pasa un objeto de identificador de identificador.</span><span class="sxs-lookup"><span data-stu-id="6919f-110">Your HANDLE\_HANDLE\_UserMarshal function marshals a **long** whenever a HANDLE\_HANDLE object is passed to it.</span></span>

-   <span data-ttu-id="6919f-111">Si el tipo de conexión es un puntero a otro tipo, la rutina de cálculo de referencias para el tipo de userm correspondiente debe calcular las referencias de los datos según el diseño del tipo al que apunta el tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="6919f-111">If the wire-type is a pointer to another type, your marshaling routine for the corresponding userm-type should marshal the data according to the layout for the type that the wire-type points to.</span></span> <span data-ttu-id="6919f-112">El motor NDR se encarga del puntero.</span><span class="sxs-lookup"><span data-stu-id="6919f-112">The NDR engine takes care of the pointer.</span></span> <span data-ttu-id="6919f-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6919f-113">For example:</span></span>

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    <span data-ttu-id="6919f-114">Tenga en cuenta que el tipo de conexión, el **\_ tipo de conexión**, es un tipo de puntero.</span><span class="sxs-lookup"><span data-stu-id="6919f-114">Note that the wire type, **WIRE\_TYPE**, is a pointer type.</span></span> <span data-ttu-id="6919f-115">La función de UserMarshal de datos de identificador \_ \_ calcula las referencias de los datos relacionados con el identificador mediante el diseño HDATA, en lugar del \* diseño HDATA.</span><span class="sxs-lookup"><span data-stu-id="6919f-115">Your HANDLE\_DATA\_UserMarshal function marshals the data related to the handle, using the HDATA layout, rather than the HDATA \* layout.</span></span>

-   <span data-ttu-id="6919f-116">Un tipo de conexión debe ser un tipo de datos plano o un tipo de puntero.</span><span class="sxs-lookup"><span data-stu-id="6919f-116">A wire-type must be either a flat data type or a pointer type.</span></span> <span data-ttu-id="6919f-117">Si el tipo transmisible debe ser otro elemento (una estructura con punteros, por ejemplo), use un puntero al tipo deseado como el tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="6919f-117">If your transmissible type must be something else (a structure with pointers, for example), use a pointer to your desired type as the wire-type.</span></span>

<span data-ttu-id="6919f-118">El efecto de estas restricciones es que los tipos definidos con los atributos de serialización de \[ [**conexión \_**](/windows/desktop/Midl/wire-marshal) \] o de \[ [**cálculo de \_ referencias de usuarios**](/windows/desktop/Midl/user-marshal) \] se pueden insertar libremente en otros tipos.</span><span class="sxs-lookup"><span data-stu-id="6919f-118">The effect of these restrictions is that the types defined with the \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\] or \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\] attributes can be freely embedded in other types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6919f-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6919f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6919f-120">**\_serialización de cable**</span><span class="sxs-lookup"><span data-stu-id="6919f-120">**wire\_marshal**</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="6919f-121">**\_serialización de usuario**</span><span class="sxs-lookup"><span data-stu-id="6919f-121">**user\_marshal**</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="6919f-122">La función de tipo de \_ usuario</span><span class="sxs-lookup"><span data-stu-id="6919f-122">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
</dt> <dt>

[<span data-ttu-id="6919f-123">La \_ función type UserMarshal</span><span class="sxs-lookup"><span data-stu-id="6919f-123">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
</dt> <dt>

[<span data-ttu-id="6919f-124">El tipo \_ UserUnMarshalFunction</span><span class="sxs-lookup"><span data-stu-id="6919f-124">Thetype\_UserUnMarshalFunction</span></span>](the-type-userunmarshal-function.md)
</dt> <dt>

[<span data-ttu-id="6919f-125">El tipo \_ UserFreeFunction</span><span class="sxs-lookup"><span data-stu-id="6919f-125">Thetype\_UserFreeFunction</span></span>](the-type-userfree-function.md)
</dt> </dl>

 

 