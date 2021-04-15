---
title: wire_marshal (atributo)
description: El atributo \ cable \_ Marshal \ especifica un tipo de datos que se usará para la transmisión (el tipo de conexión) en lugar de un tipo de datos específico de la aplicación (el tipo userm).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- wire_marshal el atributo MIDL
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421540"
---
# <a name="wire_marshal-attribute"></a><span data-ttu-id="fad9d-104">\_atributo de serialización de cable</span><span class="sxs-lookup"><span data-stu-id="fad9d-104">wire\_marshal attribute</span></span>

<span data-ttu-id="fad9d-105">El atributo de **\[ \_ serialización \] de conexión** especifica un tipo de datos que se utilizará para la transmisión (el tipo de *conexión*) en lugar de un tipo de datos específico de la aplicación (el *tipo userm*).</span><span class="sxs-lookup"><span data-stu-id="fad9d-105">The **\[wire\_marshal\]** attribute specifies a data type that will be used for transmission (the *wire-type*) instead of an application-specific data type (the *userm-type*).</span></span>

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="fad9d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fad9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad9d-107">*tipo de conexión*</span><span class="sxs-lookup"><span data-stu-id="fad9d-107">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="fad9d-108">Especifica el tipo de datos de transferencia con nombre que se transfiere realmente entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="fad9d-108">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="fad9d-109">El *tipo de conexión* debe ser un tipo base de MIDL, un tipo predefinido o un identificador de tipo de un tipo que se pueda transmitir a través de la red.</span><span class="sxs-lookup"><span data-stu-id="fad9d-109">The *wire-type* must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="fad9d-110">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="fad9d-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="fad9d-111">Tipo para el que *userm* se convertirá en un alias.</span><span class="sxs-lookup"><span data-stu-id="fad9d-111">The type for which *userm-type* will become an alias.</span></span>

</dd> <dt>

<span data-ttu-id="fad9d-112">*tipo de userm*</span><span class="sxs-lookup"><span data-stu-id="fad9d-112">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="fad9d-113">Especifica el identificador del tipo de datos de usuario del que se van a calcular las referencias.</span><span class="sxs-lookup"><span data-stu-id="fad9d-113">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="fad9d-114">Puede ser cualquier tipo, tal y como lo proporciona el *especificador Type-Specifier*, siempre que tenga un tamaño bien definido.</span><span class="sxs-lookup"><span data-stu-id="fad9d-114">It can be any type, as given by the *type-specifier*, as long as it has a well-defined size.</span></span> <span data-ttu-id="fad9d-115">No es necesario que el *tipo userm* sea transmitible, sino que debe ser un tipo conocido para el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="fad9d-115">The *userm-type* need not be transmittable but must be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="fad9d-116">*pFlags*</span><span class="sxs-lookup"><span data-stu-id="fad9d-116">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="fad9d-117">Especifica un puntero a un campo de marca ( [**unsigned**](unsigned.md) [**Long**](long.md)).</span><span class="sxs-lookup"><span data-stu-id="fad9d-117">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="fad9d-118">La palabra de orden superior especifica las marcas de representación de datos NDR definidas por DCE para el punto flotante, el Big-endian y la representación de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fad9d-118">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="fad9d-119">La palabra de orden inferior especifica una marca de contexto de cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="fad9d-119">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="fad9d-120">El diseño exacto de las marcas se describe en [la función de tipo de \_ usuario](/windows/desktop/Rpc/the-type-usersize-function).</span><span class="sxs-lookup"><span data-stu-id="fad9d-120">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="fad9d-121">*StartingSize*</span><span class="sxs-lookup"><span data-stu-id="fad9d-121">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="fad9d-122">Especifica el tamaño de búfer actual (desplazamiento) antes de ajustar el tamaño del objeto.</span><span class="sxs-lookup"><span data-stu-id="fad9d-122">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="fad9d-123">*pUser \_ typeObject*</span><span class="sxs-lookup"><span data-stu-id="fad9d-123">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="fad9d-124">Especifica un puntero a un objeto de *\_ tipo userm.*</span><span class="sxs-lookup"><span data-stu-id="fad9d-124">Specifies a pointer to an object of *userm\_type.*</span></span>

</dd> <dt>

<span data-ttu-id="fad9d-125">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="fad9d-125">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="fad9d-126">Especifica el puntero de búfer actual.</span><span class="sxs-lookup"><span data-stu-id="fad9d-126">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fad9d-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fad9d-127">Remarks</span></span>

<span data-ttu-id="fad9d-128">Cada tipo de datos específico de la aplicación, *userm-Type,* tiene una correspondencia uno a uno con un *tipo de conexión* que define la representación de la conexión del tipo.</span><span class="sxs-lookup"><span data-stu-id="fad9d-128">Each application-specific data type, *userm-type,* has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="fad9d-129">Debe proporcionar rutinas para ajustar el tamaño de los datos para el cálculo de referencias, para calcular las referencias de los datos y para deserializarlos, y para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="fad9d-129">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="fad9d-130">Tenga en cuenta que si hay tipos incrustados en los datos que también se definen con **\[ \_ serialización \] de conexión** o **\[** [**\_ serialización de usuario**](user-marshal.md), debe **\]** administrar también el servicio de esos tipos incrustados.</span><span class="sxs-lookup"><span data-stu-id="fad9d-130">Note that if there are embedded types in your data that are also defined with **\[wire\_marshal\]** or **\[**[**user\_marshal**](user-marshal.md)**\]**, you need to manage the servicing of those embedded types also.</span></span> <span data-ttu-id="fad9d-131">Para obtener más información sobre estas rutinas, vea [el \_ atributo de serialización de la conexión](/windows/desktop/Rpc/the-wire-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="fad9d-131">For more information on these routines, see [The wire\_marshal Attribute](/windows/desktop/Rpc/the-wire-marshal-attribute).</span></span>

<span data-ttu-id="fad9d-132">La implementación debe seguir las reglas de serialización según la especificación de OSF-DCE.</span><span class="sxs-lookup"><span data-stu-id="fad9d-132">Your implementation must follow the marshalling rules according to the OSF-DCE specification.</span></span> <span data-ttu-id="fad9d-133">Encontrará más información sobre la sintaxis de transferencia de NDR en [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) .</span><span class="sxs-lookup"><span data-stu-id="fad9d-133">Details about NDR transfer syntax can be found at [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).</span></span> <span data-ttu-id="fad9d-134">No se recomienda usar la **\[ \_ serialización \] de conexión** si no está familiarizado con el protocolo de conexión.</span><span class="sxs-lookup"><span data-stu-id="fad9d-134">It is not recommended to use **\[wire\_marshal\]** if you are not familiar with the wire protocol.</span></span>

<span data-ttu-id="fad9d-135">El *tipo de conexión* no puede ser un puntero de interfaz ni un puntero completo.</span><span class="sxs-lookup"><span data-stu-id="fad9d-135">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="fad9d-136">El *tipo de conexión* debe tener un tamaño de memoria bien definido.</span><span class="sxs-lookup"><span data-stu-id="fad9d-136">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="fad9d-137">Vea [serialización de reglas para la serialización de usuarios \_ y \_ serialización de conexión](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) para más información sobre cómo calcular las referencias de un *tipo de conexión* determinado.</span><span class="sxs-lookup"><span data-stu-id="fad9d-137">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="fad9d-138">El *tipo de userm* no debe ser un puntero de interfaz porque se pueden calcular las referencias directamente.</span><span class="sxs-lookup"><span data-stu-id="fad9d-138">The *userm-type* should not be an interface pointer because these can be marshaled directly.</span></span> <span data-ttu-id="fad9d-139">Si el tipo de usuario es un puntero completo, debe administrar el alias.</span><span class="sxs-lookup"><span data-stu-id="fad9d-139">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

<span data-ttu-id="fad9d-140">No se puede usar el atributo de **\[ \_ serialización \] de conexión** con el **\[** atributo [**allocate**](allocate.md) **\]** , ya sea directa o indirectamente, porque el motor NDR no controla la asignación de memoria para el tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="fad9d-140">You cannot use the **\[wire\_marshal\]** attribute with the **\[**[**allocate**](allocate.md)**\]** attribute, either directly or indirectly, because the NDR engine does not control memory allocation for the transmitted type.</span></span>

## <a name="examples"></a><span data-ttu-id="fad9d-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fad9d-141">Examples</span></span>

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a><span data-ttu-id="fad9d-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="fad9d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad9d-143">**allocate**</span><span class="sxs-lookup"><span data-stu-id="fad9d-143">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="fad9d-144">Representación de datos</span><span class="sxs-lookup"><span data-stu-id="fad9d-144">Data Representation</span></span>](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[<span data-ttu-id="fad9d-145">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="fad9d-145">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="fad9d-146">**tal**</span><span class="sxs-lookup"><span data-stu-id="fad9d-146">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="fad9d-147">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="fad9d-147">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[<span data-ttu-id="fad9d-148">Atributo de \_ serialización de cable</span><span class="sxs-lookup"><span data-stu-id="fad9d-148">The wire\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="fad9d-149">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="fad9d-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="fad9d-150">**sin signo**</span><span class="sxs-lookup"><span data-stu-id="fad9d-150">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="fad9d-151">**\_serialización de usuario**</span><span class="sxs-lookup"><span data-stu-id="fad9d-151">**user\_marshal**</span></span>](user-marshal.md)
</dt> </dl>

 

 