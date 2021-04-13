---
title: La función type_UserMarshal
description: La \_ función type UserMarshal es una función auxiliar para los atributos \ WIRE \_ Marshal \ y \ User \_ Marshal \.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421374"
---
# <a name="the-type_usermarshal-function"></a><span data-ttu-id="5c7c6-104">La \_ función type UserMarshal</span><span class="sxs-lookup"><span data-stu-id="5c7c6-104">The type\_UserMarshal Function</span></span>

<span data-ttu-id="5c7c6-105">La función **<type> \_ UserMarshal** es una función auxiliar para los atributos de serialización de \[ [ \_ conexión](/windows/desktop/Midl/wire-marshal) \] y de cálculo de \[ [ \_ referencias de usuario](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="5c7c6-105">The **<type>\_UserMarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="5c7c6-106">El código auxiliar llama a esta función para calcular las referencias de los datos en el lado cliente o servidor.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-106">The stubs call this function to marshal data on the client or server side.</span></span> <span data-ttu-id="5c7c6-107">La función se define como:</span><span class="sxs-lookup"><span data-stu-id="5c7c6-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="5c7c6-108"><type>En el nombre de la función se entiende el tipo de userm especificado en la definición de la **\[ \_ serialización \] de conexión** o el tipo de cálculo de **\[ \_ referencias \] del usuario** .</span><span class="sxs-lookup"><span data-stu-id="5c7c6-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="5c7c6-109">Este tipo puede ser no transmitible o incluso cuando se usa con el atributo de **\[ \_ cálculo de referencias \] del usuario** , un tipo desconocido para el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—a type unknown to the MIDL compiler.</span></span> <span data-ttu-id="5c7c6-110">El nombre del tipo de conexión (el nombre del tipo transmisible) no se utiliza en el prototipo de función.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="5c7c6-111">Sin embargo, tenga en cuenta que el tipo de conexión define el diseño de conexión de los datos tal y como se especifica en OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="5c7c6-112">El parámetro *pFlags* es un puntero a un campo de marca larga sin signo.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-112">The *pFlags* parameter is a pointer to an unsigned long flag field.</span></span> <span data-ttu-id="5c7c6-113">La palabra superior de la marca contiene marcas de representación de datos NDR tal y como se define en OSF DCE para el punto flotante, el orden de bytes y las representaciones de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="5c7c6-114">La palabra inferior contiene una marca de contexto de cálculo de referencias tal como la define el canal COM.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="5c7c6-115">El diseño exacto de las marcas dentro del campo se describe en [la función de tipo de \_ usuario](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="5c7c6-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="5c7c6-116">El parámetro *pBuffer* es el puntero de búfer actual.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="5c7c6-117">Este puntero puede o no estar alineado en la entrada.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="5c7c6-118">La función **<type> \_ UserMarshal** debe alinear el puntero de búfer correctamente, calcular las referencias de los datos y devolver la nueva posición del búfer, que es la dirección del primer byte después del objeto serializado.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-118">Your **<type>\_UserMarshal** function should align the buffer pointer appropriately, marshal the data, and return the new buffer position, which is the address of the first byte after the marshaled object.</span></span> <span data-ttu-id="5c7c6-119">Tenga en cuenta que la especificación de tipo de conexión determina el diseño real de los datos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-119">Keep in mind that the wire type specification determines the actual layout of the data in the buffer.</span></span>

<span data-ttu-id="5c7c6-120">El parámetro *pMyObj* es un puntero a un objeto de tipo de usuario.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-120">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="5c7c6-121">El valor devuelto es la nueva posición del búfer, que es la dirección del primer byte después del objeto cuyas referencias no se han calculado.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-121">The return value is the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="5c7c6-122">El desbordamiento del búfer puede producirse cuando se calcula incorrectamente el tamaño de los datos e intenta calcular las referencias de más datos de los esperados.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-122">Buffer overflow can occur when you incorrectly calculate the size of the data and attempt to marshal more data than expected.</span></span> <span data-ttu-id="5c7c6-123">Debe tener cuidado para evitar esta situación.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-123">You should be careful to avoid this situation.</span></span> <span data-ttu-id="5c7c6-124">Puede comprobarlo con el puntero que devuelve **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="5c7c6-124">You can check against it by using the pointer that **<type>\_UserMarshal** returns.</span></span> <span data-ttu-id="5c7c6-125">De lo contrario, corre el riesgo de que el motor NDR genere una excepción de desbordamiento de búfer más adelante.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-125">Otherwise, you risk having the NDR engine raise a buffer-overflow exception later.</span></span>

<span data-ttu-id="5c7c6-126">Las excepciones deben detectarse y administrarse localmente, las excepciones no se deben permitir que propigated la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="5c7c6-126">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c7c6-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c7c6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c7c6-128">Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión</span><span class="sxs-lookup"><span data-stu-id="5c7c6-128">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="5c7c6-129">\_serialización de cable</span><span class="sxs-lookup"><span data-stu-id="5c7c6-129">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="5c7c6-130">\_serialización de usuario</span><span class="sxs-lookup"><span data-stu-id="5c7c6-130">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 