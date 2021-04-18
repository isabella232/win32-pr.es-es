---
title: El atributo transmit_as
description: El atributo \ Transmit \_ as ofrece una manera de controlar el cálculo de referencias de datos sin preocuparse por la serialización de datos en un nivel bajo \ 8212; es decir, sin preocuparse por los tamaños de datos o el intercambio de bytes en un entorno heterogéneo.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- RPC, atributos, transmit_as llamada a procedimiento remoto
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421110"
---
# <a name="the-transmit_as-attribute"></a><span data-ttu-id="72180-105">Atributo de transmisión \_ como</span><span class="sxs-lookup"><span data-stu-id="72180-105">The transmit\_as Attribute</span></span>

<span data-ttu-id="72180-106">El **\[** atributo [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) **\]** ofrece una manera de controlar el cálculo de referencias de datos sin preocuparse por la serialización de datos en un nivel bajo, es decir, sin preocuparse por los tamaños de datos o el intercambio de bytes en un entorno heterogéneo.</span><span class="sxs-lookup"><span data-stu-id="72180-106">The **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute offers a way to control data marshaling without worrying about marshaling data at a low level—that is, without worrying about data sizes or byte swapping in a heterogeneous environment.</span></span> <span data-ttu-id="72180-107">Al permitirle reducir la cantidad de datos que se transmiten a través de la red, el atributo **\[ transmitir \_ como \]** puede hacer que la aplicación sea más eficaz.</span><span class="sxs-lookup"><span data-stu-id="72180-107">By letting you reduce the amount of data transmitted over the network, the **\[transmit\_as\]** attribute can make your application more efficient.</span></span>

<span data-ttu-id="72180-108">El atributo **\[ transmitir \_ como \]** se usa para especificar un tipo de datos que el código auxiliar de RPC transmitirá a través de la red en lugar de usar el tipo de datos proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72180-108">You use the **\[transmit\_as\]** attribute to specify a data type that the RPC stubs will transmit over the network instead of using the data type provided by the application.</span></span> <span data-ttu-id="72180-109">Se proporcionan rutinas que convierten el tipo de datos a y del tipo que se utiliza para la transmisión.</span><span class="sxs-lookup"><span data-stu-id="72180-109">You supply routines that convert the data type to and from the type that is used for transmission.</span></span> <span data-ttu-id="72180-110">También debe proporcionar rutinas para liberar la memoria que se usa para el tipo de datos y el tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="72180-110">You must also supply routines to free the memory used for the data type and the transmitted type.</span></span> <span data-ttu-id="72180-111">Por ejemplo, a continuación se define el **\_ tipo de transmisión** como el tipo de datos transmitido para todos los datos de aplicación especificados como de tipo **\_ espec**:</span><span class="sxs-lookup"><span data-stu-id="72180-111">For example, the following defines **xmit\_type** as the data type transmitted for all application data specified as being of type **type\_spec**:</span></span>

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

<span data-ttu-id="72180-112">En la tabla siguiente se describen los cuatro nombres de rutinas proporcionados por el programador.</span><span class="sxs-lookup"><span data-stu-id="72180-112">The following table describes the four programmer-supplied routine names.</span></span> <span data-ttu-id="72180-113">**Type** es el tipo de datos que la aplicación conoce y **\_ tipo de transmisión** es el tipo de datos que se usa para la transmisión.</span><span class="sxs-lookup"><span data-stu-id="72180-113">**Type** is the data type known to the application, and **xmit\_type** is the data type used for transmission.</span></span>



| <span data-ttu-id="72180-114">Rutina</span><span class="sxs-lookup"><span data-stu-id="72180-114">Routine</span></span>                                                 | <span data-ttu-id="72180-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="72180-115">Description</span></span>                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72180-116">**tipo \_ que se va a \_ transmisión**</span><span class="sxs-lookup"><span data-stu-id="72180-116">**type\_to\_xmit**</span></span>](the-type-to-xmit-function.md)     | <span data-ttu-id="72180-117">Asigna un objeto del tipo transmitido y convierte de tipo de aplicación al tipo transmitido a través de la red (llamador y objeto llamado).</span><span class="sxs-lookup"><span data-stu-id="72180-117">Allocates an object of the transmitted type and converts from application type to type transmitted over the network (caller and object called).</span></span> |
| [<span data-ttu-id="72180-118">**Tipo \_ de \_ transmisión**</span><span class="sxs-lookup"><span data-stu-id="72180-118">**Type\_from\_xmit**</span></span>](the-type-from-xmit-function.md) | <span data-ttu-id="72180-119">Convierte del tipo transmitido al tipo de aplicación (llamador y objeto llamado).</span><span class="sxs-lookup"><span data-stu-id="72180-119">Converts from transmitted type to application type (caller and object called).</span></span>                                                                  |
| [<span data-ttu-id="72180-120">**Tipo \_ \_ inst gratis**</span><span class="sxs-lookup"><span data-stu-id="72180-120">**Type\_free\_inst**</span></span>](the-type-free-inst-function.md) | <span data-ttu-id="72180-121">Libera los recursos utilizados por el tipo de aplicación (solo denominado objeto).</span><span class="sxs-lookup"><span data-stu-id="72180-121">Frees resources used by the application type (object called only).</span></span>                                                                              |
| [<span data-ttu-id="72180-122">**\_Transmisión libre de tipos \_**</span><span class="sxs-lookup"><span data-stu-id="72180-122">**Type\_free\_xmit**</span></span>](the-type-free-xmit-function.md) | <span data-ttu-id="72180-123">Libera el almacenamiento devuelto por el tipo para la rutina de \*\*\*\*\*\_\*\*\* \_ transmisión\*\* (llamador y el objeto denominado).</span><span class="sxs-lookup"><span data-stu-id="72180-123">Frees storage returned by the **type ***\_*** to\_xmit** routine (caller and object called).</span></span>                                                      |



 

<span data-ttu-id="72180-124">Aparte de estas cuatro funciones proporcionadas por el programador, la aplicación no manipula el tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="72180-124">Other than by these four programmer-supplied functions, the transmitted type is not manipulated by the application.</span></span> <span data-ttu-id="72180-125">El tipo transmitido solo se define para trasladar datos a través de la red.</span><span class="sxs-lookup"><span data-stu-id="72180-125">The transmitted type is defined only to move data over the network.</span></span> <span data-ttu-id="72180-126">Una vez que los datos se han convertido al tipo utilizado por la aplicación, se libera la memoria utilizada por el tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="72180-126">After the data is converted to the type used by the application, the memory used by the transmitted type is freed.</span></span>

<span data-ttu-id="72180-127">Estas rutinas proporcionadas por el programador las proporciona el cliente o la aplicación de servidor en función de los atributos direccionales.</span><span class="sxs-lookup"><span data-stu-id="72180-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span> <span data-ttu-id="72180-128">Si el parámetro es **\[** solo [**en**](/windows/desktop/Midl/in) **\]** , el cliente se transmite al servidor.</span><span class="sxs-lookup"><span data-stu-id="72180-128">If the parameter is **\[**[**in**](/windows/desktop/Midl/in)**\]** only, the client transmits to the server.</span></span> <span data-ttu-id="72180-129">El cliente necesita el **tipo \_ para la \_ transmisión** y el tipo de las funciones de **\_ \_ transmisión libres** .</span><span class="sxs-lookup"><span data-stu-id="72180-129">The client needs the **type\_to\_xmit** and **type\_free\_xmit** functions.</span></span> <span data-ttu-id="72180-130">El servidor necesita el **tipo \_ de \_** las funciones de tipo de la transmisión y **\_ liberación de \_ inst** .</span><span class="sxs-lookup"><span data-stu-id="72180-130">The server needs the **type\_from\_xmit** and **type\_free\_inst** functions.</span></span> <span data-ttu-id="72180-131">Para un **\[** [](/windows/desktop/Midl/out-idl) **\]** parámetro de solo salida, el servidor se transmite al cliente.</span><span class="sxs-lookup"><span data-stu-id="72180-131">For an **\[**[**out**](/windows/desktop/Midl/out-idl)**\]**-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="72180-132">La aplicación de servidor debe implementar el **tipo \_ para la \_ transmisión** y el tipo de las funciones de **\_ \_ transmisión libres** , mientras que el programa cliente debe proporcionar el **tipo de la función \_ de \_ transmisión** .</span><span class="sxs-lookup"><span data-stu-id="72180-132">The server application must implement the **type\_to\_xmit** and **type\_free\_xmit** functions, while the client program must supply the **type\_from\_xmit** function.</span></span> <span data-ttu-id="72180-133">En el caso de los objetos de **\_ tipo de transmisión** temporales, el código auxiliar llamará a la \*\*\*\*\*\_\*\*\* \_ transmisión libre de tipos\*\* para liberar cualquier memoria asignada por una llamada al **tipo para la \_ \_ transmisión**.</span><span class="sxs-lookup"><span data-stu-id="72180-133">For the temporary **xmit\_type** objects, the stub will call **type ***\_*** free\_xmit** to free any memory allocated by a call to **type\_to\_xmit**.</span></span>

<span data-ttu-id="72180-134">Ciertas directrices se aplican a la instancia de tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="72180-134">Certain guidelines apply to the application type instance.</span></span> <span data-ttu-id="72180-135">Si el tipo de aplicación es un puntero o contiene un puntero, el **tipo** \_ **de la rutina de \_ transmisión** debe asignar memoria para los datos a los que apuntan los punteros (el código auxiliar manipula el objeto de tipo de aplicación de la manera habitual).</span><span class="sxs-lookup"><span data-stu-id="72180-135">If the application type is a pointer or contains a pointer, then the **type**\_**from\_xmit** routine must allocate memory for the data that the pointers point to (the application type object itself is manipulated by the stub in the usual way).</span></span>

<span data-ttu-id="72180-136">En el **caso de los parámetros out y \[ in, out o uno de sus componentes, de un tipo que contiene el atributo Transmit as, se llama automáticamente a la rutina inst Free de tipo para los objetos de datos que tienen el atributo. \]** **\[ \] \]** **\[ \_ \]**  \_ **\_**</span><span class="sxs-lookup"><span data-stu-id="72180-136">For **\[out\]** and **\[in, out\] out\]** parameters, or one of their components, of a type that contains the **\[transmit\_as\]** attribute, the **type**\_**free\_inst** routine is automatically called for the data objects that have the attribute.</span></span> <span data-ttu-id="72180-137">En el caso de los parámetros **in** ,  \_ se llama a la rutina **\_ inst inst** de tipo solo si se ha aplicado el atributo de **\[ transmisión \_ como \]** al parámetro.</span><span class="sxs-lookup"><span data-stu-id="72180-137">For **in** parameters, the **type**\_**free\_inst** routine is called only if the **\[transmit\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="72180-138">Si el atributo se ha aplicado a los componentes del parámetro,  \_ no se llama a la rutina **\_ inst Free** de tipo.</span><span class="sxs-lookup"><span data-stu-id="72180-138">If the attribute has been applied to the components of the parameter, the **type**\_**free\_inst** routine is not called.</span></span> <span data-ttu-id="72180-139">No hay ninguna llamada de liberación para los datos incrustados y, a lo sumo, una llamada (relacionada con el atributo de nivel superior) **para un solo** parámetro.</span><span class="sxs-lookup"><span data-stu-id="72180-139">There are no freeing calls for the embedded data and at-most-one call (related to the top-level attribute) for an **in** only parameter.</span></span>

<span data-ttu-id="72180-140">Con MIDL 2,0, tanto el cliente como el servidor deben proporcionar las cuatro funciones.</span><span class="sxs-lookup"><span data-stu-id="72180-140">Effective with MIDL 2.0, both client and server must supply all four functions.</span></span> <span data-ttu-id="72180-141">Por ejemplo, una lista vinculada se puede transmitir como una matriz de tamaño.</span><span class="sxs-lookup"><span data-stu-id="72180-141">For example, a linked list can be transmitted as a sized array.</span></span> <span data-ttu-id="72180-142">El **tipo \_ para \_** la rutina de transmisión recorre la lista vinculada y copia los datos ordenados en una matriz.</span><span class="sxs-lookup"><span data-stu-id="72180-142">The **type\_to\_xmit** routine walks the linked list and copies the ordered data into an array.</span></span> <span data-ttu-id="72180-143">Los elementos de la matriz se ordenan de modo que no es necesario transmitir los muchos punteros asociados a la estructura de lista.</span><span class="sxs-lookup"><span data-stu-id="72180-143">The array elements are ordered so that the many pointers associated with the list structure do not have to be transmitted.</span></span> <span data-ttu-id="72180-144">El **tipo \_ de la rutina de \_ transmisión** lee la matriz y coloca sus elementos en una estructura de lista vinculada.</span><span class="sxs-lookup"><span data-stu-id="72180-144">The **type\_from\_xmit** routine reads the array and puts its elements into a linked-list structure.</span></span>

<span data-ttu-id="72180-145">La lista vinculada doble ( \_ lista de vínculos dobles \_ ) incluye datos y punteros a los elementos de la lista anterior y siguiente:</span><span class="sxs-lookup"><span data-stu-id="72180-145">The double-linked list (DOUBLE\_LINK\_LIST) includes data and pointers to the previous and next list elements:</span></span>

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

<span data-ttu-id="72180-146">En lugar de enviar la estructura compleja, el **\[** atributo [**Transmit \_ as**](/windows/desktop/Midl/transmit-as) **\]** se puede usar para enviarlo a través de la red como una matriz.</span><span class="sxs-lookup"><span data-stu-id="72180-146">Rather than shipping the complex structure, the **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute can be used to send it over the network as an array.</span></span> <span data-ttu-id="72180-147">La secuencia de elementos de la matriz conserva el orden de los elementos de la lista a un costo más bajo:</span><span class="sxs-lookup"><span data-stu-id="72180-147">The sequence of items in the array retains the ordering of the elements in the list at a lower cost:</span></span>

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

<span data-ttu-id="72180-148">El atributo **\[ transmitir \_ como \]** aparece en el archivo IDL:</span><span class="sxs-lookup"><span data-stu-id="72180-148">The **\[transmit\_as\]** attribute appears in the IDL file:</span></span>

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

<span data-ttu-id="72180-149">En el ejemplo siguiente, **ModifyListProc** define el parámetro de tipo Double \_ Link \_ Type como **\[ in, \] out** Parameter:</span><span class="sxs-lookup"><span data-stu-id="72180-149">In the following example, **ModifyListProc** defines the parameter of type DOUBLE\_LINK\_TYPE as an **\[in, out\]** parameter:</span></span>

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

<span data-ttu-id="72180-150">Las cuatro funciones definidas por el programador usan el nombre del tipo en los nombres de función y usan los tipos presentados y transmitidos como tipos de parámetro, según sea necesario:</span><span class="sxs-lookup"><span data-stu-id="72180-150">The four programmer-defined functions use the name of the type in the function names, and use the presented and transmitted types as parameter types, as required:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 