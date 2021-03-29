---
title: La función type_UserSize
description: La función de tipo de usuario \_ es una función auxiliar para los atributos \ WIRE \_ Marshal \ y \ User \_ Marshal \.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e5936763f9fe7b3513d66ddca7db9c35dbfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793665"
---
# <a name="the-type_usersize-function"></a><span data-ttu-id="97f67-104">La función de tipo de \_ usuario</span><span class="sxs-lookup"><span data-stu-id="97f67-104">The type\_UserSize Function</span></span>

<span data-ttu-id="97f67-105">La **<type> \_ función de usuario es** una función auxiliar para los atributos de serialización de \[ [ \_ conexión](/windows/desktop/Midl/wire-marshal) \] y de cálculo de \[ [ \_ referencias de usuarios](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="97f67-105">The **<type>\_UserSize** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="97f67-106">El código auxiliar llama a esta función para ajustar el tamaño del búfer de datos RPC para el objeto de datos del usuario antes de que se calculen las referencias de los datos en el cliente o el servidor.</span><span class="sxs-lookup"><span data-stu-id="97f67-106">The stubs call this function to size the RPC data buffer for the user data object before the data is marshaled on the client or server side.</span></span> <span data-ttu-id="97f67-107">La función se define como:</span><span class="sxs-lookup"><span data-stu-id="97f67-107">The function is defined as:</span></span>

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

<span data-ttu-id="97f67-108"><type>En el nombre de la función se entiende el tipo userm, tal y como se especifica en la definición de tipo de cálculo de referencias de **\[ \_ \] conexión** o de **\[ usuario \_ \]** .</span><span class="sxs-lookup"><span data-stu-id="97f67-108">The <type> in the function name means the userm-type, as specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="97f67-109">Este tipo puede ser no transmitible o incluso cuando se usa con el atributo de **\[ \_ cálculo de referencias \] del usuario** , desconocido para el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="97f67-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute— unknown to the MIDL compiler.</span></span> <span data-ttu-id="97f67-110">El nombre del tipo de conexión (el nombre del tipo transmitido a través de la red) no se utiliza en el prototipo de función.</span><span class="sxs-lookup"><span data-stu-id="97f67-110">The wire type name (the name of the type transmitted across the network) is not used in the function prototype.</span></span> <span data-ttu-id="97f67-111">Sin embargo, tenga en cuenta que el tipo de conexión define el diseño de los datos tal y como se especifica en OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="97f67-111">Note, however, that the wire type defines the layout for the data as specified by OSF DCE.</span></span> <span data-ttu-id="97f67-112">Todos los datos se deben convertir al formato de representación de datos de red (NDR).</span><span class="sxs-lookup"><span data-stu-id="97f67-112">All data must be converted to network data representation (NDR) format.</span></span>

<span data-ttu-id="97f67-113">El parámetro *pFlags* es un puntero a un campo de marca **larga sin signo** .</span><span class="sxs-lookup"><span data-stu-id="97f67-113">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="97f67-114">La palabra superior de la marca contiene marcas de formato NDR, tal y como se define en OSF DCE para el punto flotante, el orden de bytes y las representaciones de caracteres.</span><span class="sxs-lookup"><span data-stu-id="97f67-114">The upper word of the flag contains NDR format flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="97f67-115">La palabra inferior contiene una marca de contexto de cálculo de referencias tal como la define el canal COM.</span><span class="sxs-lookup"><span data-stu-id="97f67-115">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="97f67-116">En la tabla siguiente se muestra el diseño exacto de las marcas dentro del campo.</span><span class="sxs-lookup"><span data-stu-id="97f67-116">The exact layout of the flags within the field is shown in the following table.</span></span>



| <span data-ttu-id="97f67-117">Bits</span><span class="sxs-lookup"><span data-stu-id="97f67-117">Bits</span></span>  | <span data-ttu-id="97f67-118">Marca</span><span class="sxs-lookup"><span data-stu-id="97f67-118">Flag</span></span>                                  | <span data-ttu-id="97f67-119">Value</span><span class="sxs-lookup"><span data-stu-id="97f67-119">Value</span></span>                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="97f67-120">31-24</span><span class="sxs-lookup"><span data-stu-id="97f67-120">31-24</span></span> | <span data-ttu-id="97f67-121">Representación de punto flotante</span><span class="sxs-lookup"><span data-stu-id="97f67-121">Floating-point representation</span></span>         | <span data-ttu-id="97f67-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span><span class="sxs-lookup"><span data-stu-id="97f67-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span></span>                                                         |
| <span data-ttu-id="97f67-123">23-20</span><span class="sxs-lookup"><span data-stu-id="97f67-123">23-20</span></span> | <span data-ttu-id="97f67-124">Orden de bytes entero y de punto flotante</span><span class="sxs-lookup"><span data-stu-id="97f67-124">Integer and floating-point byte order</span></span> | <span data-ttu-id="97f67-125">0 = Big-Endian 1 = Little-endian</span><span class="sxs-lookup"><span data-stu-id="97f67-125">0 = Big-endian 1 = Little-endian</span></span>                                                          |
| <span data-ttu-id="97f67-126">19-16</span><span class="sxs-lookup"><span data-stu-id="97f67-126">19-16</span></span> | <span data-ttu-id="97f67-127">Representación de caracteres</span><span class="sxs-lookup"><span data-stu-id="97f67-127">Character representation</span></span>              | <span data-ttu-id="97f67-128">0 = ASCII 1 = EBCDIC</span><span class="sxs-lookup"><span data-stu-id="97f67-128">0 = ASCII 1 = EBCDIC</span></span>                                                                      |
| <span data-ttu-id="97f67-129">15-0</span><span class="sxs-lookup"><span data-stu-id="97f67-129">15-0</span></span>  | <span data-ttu-id="97f67-130">Marca de contexto de cálculo de referencias</span><span class="sxs-lookup"><span data-stu-id="97f67-130">Marshaling context flag</span></span>               | <span data-ttu-id="97f67-131">0 = MSHCTX \_ local 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ Inproc</span><span class="sxs-lookup"><span data-stu-id="97f67-131">0 = MSHCTX\_LOCAL 1 = MSHCTX\_NOSHAREDMEM 2 = MSHCTX\_DIFFERENTMACHINE 3 = MSHCTX\_INPROC</span></span> |



 

<span data-ttu-id="97f67-132">La marca de contexto de serialización permite modificar el comportamiento de la rutina en función del contexto de la llamada RPC.</span><span class="sxs-lookup"><span data-stu-id="97f67-132">The marshaling context flag makes it possible to alter the behavior of your routine depending on the context for the RPC call.</span></span> <span data-ttu-id="97f67-133">Por ejemplo, si tiene un identificador (**Long**) a un bloque de datos, podría enviar el identificador de una llamada en proceso, pero enviaría los datos reales para una llamada a otro equipo.</span><span class="sxs-lookup"><span data-stu-id="97f67-133">For example, if you have a handle (**long**) to a block of data, you could send the handle for an in-process call, but you would send the actual data for a call to a different machine.</span></span> <span data-ttu-id="97f67-134">La marca de contexto de cálculo de referencias y sus valores se definen en los archivos Wtypes. h y Wtypes. idl en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="97f67-134">The marshaling context flag and its values are defined in the Wtypes.h and Wtypes.idl files in the Platform Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="97f67-135">Cuando el tipo de conexión se define correctamente, no es necesario utilizar las marcas de formato NDR, ya que el motor NDR realiza las conversiones necesarias.</span><span class="sxs-lookup"><span data-stu-id="97f67-135">When the wire type is properly defined, you do not have to use the NDR format flags, as the NDR engine performs the necessary conversions.</span></span>

 

<span data-ttu-id="97f67-136">El parámetro *StartingSize* es el desplazamiento del búfer actual.</span><span class="sxs-lookup"><span data-stu-id="97f67-136">The *StartingSize* a parameter is the current buffer offset.</span></span> <span data-ttu-id="97f67-137">El tamaño inicial indica el desplazamiento del búfer para el objeto de usuario y puede o no estar alineado correctamente.</span><span class="sxs-lookup"><span data-stu-id="97f67-137">The starting size indicates the buffer offset for the user object, and it may or may not be aligned properly.</span></span> <span data-ttu-id="97f67-138">La rutina debe tener en cuenta el relleno que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="97f67-138">Your routine should account for whatever padding is necessary.</span></span>

<span data-ttu-id="97f67-139">El parámetro *pMyObj* es un puntero a un objeto de tipo de usuario.</span><span class="sxs-lookup"><span data-stu-id="97f67-139">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="97f67-140">El valor devuelto es el nuevo desplazamiento o la posición del búfer.</span><span class="sxs-lookup"><span data-stu-id="97f67-140">The return value is the new offset or buffer position.</span></span> <span data-ttu-id="97f67-141">La función debe devolver el tamaño acumulado, que es el tamaño inicial más el posible relleno más el tamaño de los datos.</span><span class="sxs-lookup"><span data-stu-id="97f67-141">The function should return the cumulative size, which is the starting size plus possible padding plus the data size.</span></span>

<span data-ttu-id="97f67-142">La función de **<type> \_ usuario** puede devolver un valor sobrestimado del tamaño necesario.</span><span class="sxs-lookup"><span data-stu-id="97f67-142">The **<type>\_UserSize** function can return an overestimate of the size needed.</span></span> <span data-ttu-id="97f67-143">El tamaño real del búfer enviado lo define el tamaño de los datos, no el tamaño de asignación del búfer.</span><span class="sxs-lookup"><span data-stu-id="97f67-143">The actual size of the sent buffer is defined by the data size, not by the buffer allocation size.</span></span>

<span data-ttu-id="97f67-144">No se llama a la función de **<type> \_ usuario** si el tamaño de la conexión se puede calcular en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="97f67-144">The **<type>\_UserSize** function is not called if the wire size can be computed at compile time.</span></span> <span data-ttu-id="97f67-145">Tenga en cuenta que para la mayoría de las uniones, incluso si no hay punteros, el tamaño real de la representación de la conexión solo se puede determinar en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="97f67-145">Note that for most unions, even if there are no pointers, the actual size of the wire representation can be determined only at run time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97f67-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97f67-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97f67-147">Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión</span><span class="sxs-lookup"><span data-stu-id="97f67-147">Marshaling rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="97f67-148">\_serialización de usuario</span><span class="sxs-lookup"><span data-stu-id="97f67-148">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="97f67-149">\_serialización de cable</span><span class="sxs-lookup"><span data-stu-id="97f67-149">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 