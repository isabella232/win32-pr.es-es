---
title: La función type_UserUnmarshal
description: La \_ función type UserUnmarshal es una función auxiliar para los atributos \ WIRE \_ Marshal \ y \ User \_ Marshal \.
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332edbc2391aadf297789cc0ae862454786bdd8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078327"
---
# <a name="the-type_userunmarshal-function"></a><span data-ttu-id="64410-104">La \_ función type UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="64410-104">The type\_UserUnmarshal Function</span></span>

<span data-ttu-id="64410-105">La función **<type> \_ UserUnmarshal** es una función auxiliar para los atributos de serialización de \[ [ \_ conexión](/windows/desktop/Midl/wire-marshal) \] y de cálculo de \[ [ \_ referencias de usuario](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="64410-105">The **<type>\_UserUnmarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="64410-106">El código auxiliar llama a esta función para anular la serialización de datos en el cliente o en el servidor.</span><span class="sxs-lookup"><span data-stu-id="64410-106">The stubs call this function to unmarshal data on the client or server side.</span></span> <span data-ttu-id="64410-107">La función se define como:</span><span class="sxs-lookup"><span data-stu-id="64410-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="64410-108"><type>En el nombre de la función se entiende el tipo de userm especificado en la definición de la **\[ \_ serialización \] de conexión** o el tipo de cálculo de **\[ \_ referencias \] del usuario** .</span><span class="sxs-lookup"><span data-stu-id="64410-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="64410-109">Este tipo puede ser no transmitible o incluso cuando se usa con el atributo de **\[ \_ cálculo de referencias \] del usuario** , desconocido para el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="64410-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—unknown to the MIDL compiler.</span></span> <span data-ttu-id="64410-110">El nombre del tipo de conexión (el nombre del tipo transmisible) no se utiliza en el prototipo de función.</span><span class="sxs-lookup"><span data-stu-id="64410-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="64410-111">Sin embargo, tenga en cuenta que el tipo de conexión define el diseño de conexión de los datos tal y como se especifica en OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="64410-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="64410-112">El parámetro *pFlags* es un puntero a un campo de marca **larga sin signo** .</span><span class="sxs-lookup"><span data-stu-id="64410-112">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="64410-113">La palabra superior de la marca contiene marcas de representación de datos NDR tal y como se define en OSF DCE para el punto flotante, el orden de bytes y las representaciones de caracteres.</span><span class="sxs-lookup"><span data-stu-id="64410-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="64410-114">La palabra inferior contiene una marca de contexto de cálculo de referencias tal como la define el canal COM.</span><span class="sxs-lookup"><span data-stu-id="64410-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="64410-115">El diseño exacto de las marcas dentro del campo se describe en [la función de tipo de \_ usuario](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="64410-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="64410-116">El parámetro *pBuffer* es el puntero de búfer actual.</span><span class="sxs-lookup"><span data-stu-id="64410-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="64410-117">Este puntero puede o no estar alineado en la entrada.</span><span class="sxs-lookup"><span data-stu-id="64410-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="64410-118">La función **<type> \_ UserUnmarshal** debe alinear el puntero de búfer correctamente, anular la serialización de los datos y devolver la nueva posición del búfer, que es la dirección del primer byte después del objeto cuyas referencias no se han calculado.</span><span class="sxs-lookup"><span data-stu-id="64410-118">Your **<type>\_UserUnmarshal** function should align the buffer pointer appropriately, unmarshal the data, and return the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="64410-119">El parámetro *pMyObj* es un puntero a un objeto de tipo definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="64410-119">The *pMyObj* parameter is a pointer to a user-defined type object.</span></span>

<span data-ttu-id="64410-120">En un entorno heterogéneo, el motor NDR realiza cualquier conversión de datos necesaria antes de llamar a la función **<type> \_ UserUnmarshal** .</span><span class="sxs-lookup"><span data-stu-id="64410-120">In a heterogeneous environment, the NDR engine performs any data conversion necessary before calling the **<type>\_UserUnmarshal** function.</span></span> <span data-ttu-id="64410-121">Tenga en cuenta que el motor NDR realiza esta conversión de datos según la definición de tipo de conexión proporcionada para este tipo de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="64410-121">Note that the NDR engine carries out this data conversion according to the wire-type definition supplied for this user data type.</span></span> <span data-ttu-id="64410-122">La marca indica la representación de datos del remitente.</span><span class="sxs-lookup"><span data-stu-id="64410-122">The flag indicates the data representation of the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64410-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64410-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64410-124">Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión</span><span class="sxs-lookup"><span data-stu-id="64410-124">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="64410-125">\_serialización de cable</span><span class="sxs-lookup"><span data-stu-id="64410-125">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="64410-126">\_serialización de usuario</span><span class="sxs-lookup"><span data-stu-id="64410-126">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 