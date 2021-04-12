---
title: user_marshal atributo)
description: El \_ atributo ACF de serialización de usuario asocia un tipo local con nombre en el idioma de destino (userm-Type) con un tipo de transferencia (tipo de conexión) que se transfiere entre el cliente y el servidor.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal el atributo MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358861"
---
# <a name="user_marshal-attribute"></a><span data-ttu-id="ea3fa-104">\_atributo User Marshal</span><span class="sxs-lookup"><span data-stu-id="ea3fa-104">user\_marshal attribute</span></span>

<span data-ttu-id="ea3fa-105">El atributo ACF de **\_ serialización de usuario** asocia un tipo local con nombre en el idioma de destino (*userm-Type*) con un tipo de transferencia (*tipo de conexión*) que se transfiere entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-105">The **user\_marshal** ACF attribute associates a named local type in the target language (*userm-type*) with a transfer type (*wire-type*) that is transferred between client and server.</span></span>

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="ea3fa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea3fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea3fa-107">*tipo de userm*</span><span class="sxs-lookup"><span data-stu-id="ea3fa-107">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="ea3fa-108">Especifica el identificador del tipo de datos de usuario del que se van a calcular las referencias.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-108">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="ea3fa-109">No es necesario transmitir el *tipo userm* y no es necesario que sea un tipo conocido para el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-109">The *userm-type* need not be transmittable and need not be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="ea3fa-110">*tipo de conexión*</span><span class="sxs-lookup"><span data-stu-id="ea3fa-110">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="ea3fa-111">Especifica el tipo de datos de transferencia con nombre que se transfiere realmente entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-111">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="ea3fa-112">El tipo de conexión debe ser un tipo base de MIDL, un tipo predefinido o un identificador de tipo de un tipo que se pueda transmitir a través de la red.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-112">The wire type must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="ea3fa-113">*pFlags*</span><span class="sxs-lookup"><span data-stu-id="ea3fa-113">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="ea3fa-114">Especifica un puntero a un campo de marca ( [**unsigned**](unsigned.md) [**Long**](long.md)).</span><span class="sxs-lookup"><span data-stu-id="ea3fa-114">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="ea3fa-115">La palabra de orden superior especifica las marcas de representación de datos NDR definidas por DCE para el punto flotante, el Big-endian y la representación de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-115">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="ea3fa-116">La palabra de orden inferior especifica una marca de contexto de cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-116">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="ea3fa-117">El diseño exacto de las marcas se describe en [la función de tipo de \_ usuario](/windows/desktop/Rpc/the-type-usersize-function).</span><span class="sxs-lookup"><span data-stu-id="ea3fa-117">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="ea3fa-118">*StartingSize*</span><span class="sxs-lookup"><span data-stu-id="ea3fa-118">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="ea3fa-119">Especifica el tamaño de búfer actual (desplazamiento) antes de ajustar el tamaño del objeto.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-119">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="ea3fa-120">*pUser \_ typeObject*</span><span class="sxs-lookup"><span data-stu-id="ea3fa-120">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="ea3fa-121">Especifica un puntero a un objeto de *\_ tipo userm*.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-121">Specifies a pointer to an object of *userm\_type*.</span></span>

</dd> <dt>

<span data-ttu-id="ea3fa-122">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="ea3fa-122">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="ea3fa-123">Especifica el puntero de búfer actual.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-123">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea3fa-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea3fa-124">Remarks</span></span>

<span data-ttu-id="ea3fa-125">Cada tipo local con nombre, *userm-Type*, tiene una correspondencia uno a uno con un *tipo de conexión* que define la representación de la conexión del tipo.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-125">Each named local type, *userm-type*, has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="ea3fa-126">Debe proporcionar rutinas para ajustar el tamaño de los datos para el cálculo de referencias, para calcular las referencias de los datos y para deserializarlos, y para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-126">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="ea3fa-127">Para obtener más información sobre estas rutinas, vea [el \_ atributo User Marshal](/windows/desktop/Rpc/the-user-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="ea3fa-127">For more information on these routines, see [The user\_marshal Attribute](/windows/desktop/Rpc/the-user-marshal-attribute).</span></span> <span data-ttu-id="ea3fa-128">Tenga en cuenta que si hay tipos incrustados en los datos que también se definen con serialización de **usuario \_** o \[ [**\[ \_ serialización \] de conexión**](wire-marshal.md), también debe administrar el servicio de esos tipos incrustados.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-128">Note that if there are embedded types in your data that are also defined with **user\_marshal** or \[ [**\[wire\_marshal\]**](wire-marshal.md), you need to manage the servicing of those embedded types also.</span></span>

<span data-ttu-id="ea3fa-129">El *tipo de conexión* no puede ser un puntero de interfaz ni un puntero completo.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-129">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="ea3fa-130">El *tipo de conexión* debe tener un tamaño de memoria bien definido.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-130">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="ea3fa-131">Vea [serialización de reglas para la serialización de usuarios \_ y \_ serialización de conexión](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) para más información sobre cómo calcular las referencias de un *tipo de conexión* determinado.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-131">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="ea3fa-132">El *tipo de userm* no debe ser un puntero de interfaz, ya que estas referencias se pueden calcular directamente.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-132">The *userm-type* should not be an interface pointer as these can be marshaled directly.</span></span> <span data-ttu-id="ea3fa-133">Si el tipo de usuario es un puntero completo, debe administrar el alias.</span><span class="sxs-lookup"><span data-stu-id="ea3fa-133">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

## <a name="examples"></a><span data-ttu-id="ea3fa-134">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ea3fa-134">Examples</span></span>

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a><span data-ttu-id="ea3fa-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea3fa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea3fa-136">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="ea3fa-136">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="ea3fa-137">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="ea3fa-137">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="ea3fa-138">**tal**</span><span class="sxs-lookup"><span data-stu-id="ea3fa-138">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="ea3fa-139">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="ea3fa-139">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="ea3fa-140">**sin signo**</span><span class="sxs-lookup"><span data-stu-id="ea3fa-140">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="ea3fa-141">Atributo User \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="ea3fa-141">The user\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="ea3fa-142">**\_serialización de cable**</span><span class="sxs-lookup"><span data-stu-id="ea3fa-142">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="ea3fa-143">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="ea3fa-143">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 