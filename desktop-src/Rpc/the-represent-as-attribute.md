---
title: El atributo represent_as
description: El atributo \ representate \_ como \ permite especificar cómo se representa un tipo de datos transmitible determinado en la aplicación.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- RPC, atributos, represent_as llamada a procedimiento remoto
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149565"
---
# <a name="the-represent_as-attribute"></a><span data-ttu-id="08df8-105">El atributo de representación \_ como</span><span class="sxs-lookup"><span data-stu-id="08df8-105">The represent\_as Attribute</span></span>

<span data-ttu-id="08df8-106">El \[ atributo [representate \_ as](/windows/desktop/Midl/represent-as) \] permite especificar cómo se representa un tipo de datos transmitible determinado en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="08df8-106">The \[ [represent\_as](/windows/desktop/Midl/represent-as)\] attribute lets you specify how a particular transmittable data type is represented to the application.</span></span> <span data-ttu-id="08df8-107">Esto se hace especificando el nombre del tipo representado para un tipo transmitible conocido y proporcionando las rutinas de conversión.</span><span class="sxs-lookup"><span data-stu-id="08df8-107">This is done by specifying the name of the represented type for a known transmittable type and supplying the conversion routines.</span></span> <span data-ttu-id="08df8-108">También debe proporcionar las rutinas para liberar la memoria que usan los objetos de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="08df8-108">You must also supply the routines to free the memory used by the data type objects.</span></span>

<span data-ttu-id="08df8-109">Use el atributo **\[ representar \_ como \]** para presentar una aplicación con un tipo de datos diferente, posiblemente no transmitible, en lugar del tipo que realmente se transmite entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="08df8-109">Use the **\[represent\_as\]** attribute to present an application with a different, possibly untransmittable, data type rather than the type that is actually transmitted between the client and server.</span></span> <span data-ttu-id="08df8-110">También es posible que el tipo que manipula la aplicación se desconozca en el momento de la compilación de MIDL.</span><span class="sxs-lookup"><span data-stu-id="08df8-110">It is also possible that the type the application manipulates can be unknown at the time of MIDL compilation.</span></span> <span data-ttu-id="08df8-111">Al elegir un tipo de transmisión bien definido, no es necesario preocuparse por la representación de datos en el entorno heterogéneo.</span><span class="sxs-lookup"><span data-stu-id="08df8-111">When you choose a well-defined transmittable type, you need not be concerned about data representation in the heterogeneous environment.</span></span> <span data-ttu-id="08df8-112">El atributo **\[ representate \_ as \]** puede hacer que la aplicación sea más eficaz reduciendo la cantidad de datos transmitidos a través de la red.</span><span class="sxs-lookup"><span data-stu-id="08df8-112">The **\[represent\_as\]** attribute can make your application more efficient by reducing the amount of data transmitted over the network.</span></span>

<span data-ttu-id="08df8-113">El atributo **\[ representa \_ \] como** es similar al atributo \[ [transmitir \_ como](/windows/desktop/Midl/transmit-as) \] .</span><span class="sxs-lookup"><span data-stu-id="08df8-113">The **\[represent\_as\]** attribute is similar to the \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\] attribute.</span></span> <span data-ttu-id="08df8-114">Sin embargo, mientras se **\[ transmite \_ como \]** le permite especificar un tipo de datos que se usará para la transmisión, **\[ representa \_ como \]** le permite especificar cómo se representa un tipo de datos para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="08df8-114">However, while **\[transmit\_as\]** lets you specify a data type that will be used for transmission, **\[represent\_as\]** lets you specify how a data type is represented for the application.</span></span> <span data-ttu-id="08df8-115">No es necesario definir el tipo representado en los archivos procesados por MIDL; se puede definir en el momento en que se compilan los códigos auxiliares con el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="08df8-115">The represented type need not be defined in the MIDL processed files; it can be defined at the time the stubs are compiled with the C compiler.</span></span> <span data-ttu-id="08df8-116">Para ello, utilice la Directiva include en el archivo de configuración de la [aplicación (ACF)](the-application-configuration-file-acf-.md) para compilar el archivo de encabezado adecuado.</span><span class="sxs-lookup"><span data-stu-id="08df8-116">To do this, use the include directive in the [application configuration file (ACF)](the-application-configuration-file-acf-.md) to compile the appropriate header file.</span></span> <span data-ttu-id="08df8-117">Por ejemplo, el siguiente ACF define un tipo local para la aplicación, **repr \_ Type**, para el tipo de transmisión **denominado \_ Type:**</span><span class="sxs-lookup"><span data-stu-id="08df8-117">For example, the following ACF defines a type local to the application, **repr\_type**, for the transmittable type **named\_type:**</span></span>

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

<span data-ttu-id="08df8-118">En la tabla siguiente se describen las cuatro rutinas proporcionadas por el programador.</span><span class="sxs-lookup"><span data-stu-id="08df8-118">The following table describes the four programmer-supplied routines.</span></span>



| <span data-ttu-id="08df8-119">Rutina</span><span class="sxs-lookup"><span data-stu-id="08df8-119">Routine</span></span>                      | <span data-ttu-id="08df8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="08df8-120">Description</span></span>                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08df8-121">**tipo con nombre \_ \_ de \_ local**</span><span class="sxs-lookup"><span data-stu-id="08df8-121">**named\_type\_from\_local**</span></span> | <span data-ttu-id="08df8-122">Asigna una instancia del tipo de red y convierte el tipo local al tipo de red.</span><span class="sxs-lookup"><span data-stu-id="08df8-122">Allocates an instance of the network type and converts from the local type to the network type.</span></span>      |
| <span data-ttu-id="08df8-123">**tipo con nombre \_ \_ en \_ local**</span><span class="sxs-lookup"><span data-stu-id="08df8-123">**named\_type\_to\_local**</span></span>   | <span data-ttu-id="08df8-124">Convierte del tipo de red al tipo local.</span><span class="sxs-lookup"><span data-stu-id="08df8-124">Converts from the network type to the local type.</span></span>                                                    |
| <span data-ttu-id="08df8-125">**tipo con nombre \_ \_ Free \_ local**</span><span class="sxs-lookup"><span data-stu-id="08df8-125">**named\_type\_free\_local**</span></span> | <span data-ttu-id="08df8-126">Libera la memoria asignada por una llamada al **tipo con nombre en la rutina \_ \_ \_ local** , pero no el propio tipo.</span><span class="sxs-lookup"><span data-stu-id="08df8-126">Frees memory allocated by a call to the **named\_type\_to\_local** routine, but not the type itself.</span></span> |
| <span data-ttu-id="08df8-127">**Inst. de tipo con nombre \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="08df8-127">**named\_type\_free\_inst**</span></span>  | <span data-ttu-id="08df8-128">Libera el almacenamiento para el tipo de red (ambos lados).</span><span class="sxs-lookup"><span data-stu-id="08df8-128">Frees storage for the network type (both sides).</span></span>                                                     |



 

<span data-ttu-id="08df8-129">Aparte de estas cuatro rutinas proporcionadas por el programador, la aplicación no manipula el tipo con nombre.</span><span class="sxs-lookup"><span data-stu-id="08df8-129">Other than by these four programmer-supplied routines, the named type is not manipulated by the application.</span></span> <span data-ttu-id="08df8-130">El único tipo visible para la aplicación es el tipo representado.</span><span class="sxs-lookup"><span data-stu-id="08df8-130">The only type visible to the application is the represented type.</span></span> <span data-ttu-id="08df8-131">La aplicación utiliza el nombre de tipo representado en lugar del nombre de tipo transmitido en los prototipos y códigos auxiliares generados por el compilador.</span><span class="sxs-lookup"><span data-stu-id="08df8-131">The application uses the represented type name instead of the transmitted type name in the prototypes and stubs generated by the compiler.</span></span> <span data-ttu-id="08df8-132">Debe proporcionar el conjunto de rutinas para ambos lados.</span><span class="sxs-lookup"><span data-stu-id="08df8-132">You must supply the set of routines for both sides.</span></span>

<span data-ttu-id="08df8-133">En el caso de los objetos de **\_ tipo con nombre** temporal, el código auxiliar llamará a un **tipo con nombre \_ \_ Free \_ inst** para liberar cualquier memoria asignada por una llamada a un **tipo con nombre \_ \_ de \_ local**.</span><span class="sxs-lookup"><span data-stu-id="08df8-133">For temporary **named\_type** objects, the stub will call **named\_type\_free\_inst** to free any memory allocated by a call to **named\_type\_from\_local**.</span></span>

<span data-ttu-id="08df8-134">Si el tipo representado es un puntero o contiene un puntero, el **tipo con nombre de la rutina \_ \_ \_ local** debe asignar la memoria para los datos a los que apuntan los punteros (el código auxiliar manipula el propio objeto de tipo representado de la manera habitual).</span><span class="sxs-lookup"><span data-stu-id="08df8-134">If the represented type is a pointer or contains a pointer, the **named\_type\_to\_local** routine must allocate memory for the data to which the pointers point (the represented type object itself is manipulated by the stub in the usual way).</span></span> <span data-ttu-id="08df8-135">Para \[ [los](/windows/desktop/Midl/out-idl) \] parámetros out y \[ [in](/windows/desktop/Midl/in), out \] de un tipo que contiene **\[ representan \_ como** o uno de sus componentes, se llama automáticamente a la rutina **\_ \_ \_ local de tipo con nombre** para los objetos de datos que contienen el atributo.</span><span class="sxs-lookup"><span data-stu-id="08df8-135">For \[ [out](/windows/desktop/Midl/out-idl)\] and \[ [in](/windows/desktop/Midl/in), out\] parameters of a type that contain **\[represent\_as** or one of its components, the **named\_type\_free\_local** routine is automatically called for the data objects that contain the attribute.</span></span> <span data-ttu-id="08df8-136">En el caso de los parámetros **\[ in \]** , solo se llama a la rutina **\_ \_ \_ local de tipo con nombre** si el atributo **\[ representated \_ as \]** se ha aplicado al parámetro.</span><span class="sxs-lookup"><span data-stu-id="08df8-136">For **\[in\]** parameters, the **named\_type\_free\_local** routine is called only if the **\[represent\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="08df8-137">Si el atributo se ha aplicado a los componentes del parámetro, no se llama a la rutina \*\* \*\*\* \_ \_ local gratuita\*\*.</span><span class="sxs-lookup"><span data-stu-id="08df8-137">If the attribute has been applied to the components of the parameter, the *\*\*\*\*\_free\_local*\* routine is not called.</span></span> <span data-ttu-id="08df8-138">No se llama a las rutinas de liberación para los datos incrustados y la llamada más de una vez (relacionado con el atributo de nivel superior) para **\[ \] un solo parámetro** .</span><span class="sxs-lookup"><span data-stu-id="08df8-138">Freeing routines are not called for the embedded data and at-most-once call (related to the top-level attribute) for an **\[in\]** only parameter.</span></span>

> [!Note]  
> <span data-ttu-id="08df8-139">Se pueden aplicar los atributos de **\[ transmisión \_ como \]** y de **\[ representación \_ \]** al mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="08df8-139">It is possible to apply both the **\[transmit\_as\]** and **\[represent\_as\]** attributes to the same type.</span></span> <span data-ttu-id="08df8-140">Al calcular las referencias de los datos, se aplica primero la conversión de tipos de **\[ representación \_ \]** y **\[ \_ \]** , a continuación, se aplica la conversión de transmisión.</span><span class="sxs-lookup"><span data-stu-id="08df8-140">When marshaling data, the **\[represent\_as\]** type conversion is applied first and then the **\[transmit\_as\]** conversion is applied.</span></span> <span data-ttu-id="08df8-141">El orden se invierte al anular la serialización de los datos.</span><span class="sxs-lookup"><span data-stu-id="08df8-141">The order is reversed when unmarshaling data.</span></span> <span data-ttu-id="08df8-142">Por lo tanto, cuando se calculan las referencias, \* **\_ desde \_ local** asigna una instancia de un tipo con nombre y la traduce de un objeto de tipo local al objeto de tipo con nombre temporal.</span><span class="sxs-lookup"><span data-stu-id="08df8-142">Thus, when marshaling, \***\_from\_local** allocates an instance of a named type and translates it from a local type object to the temporary named type object.</span></span> <span data-ttu-id="08df8-143">Este objeto es el objeto de tipo presentado utilizado para la rutina de \* **\_ \_ transmisión** .</span><span class="sxs-lookup"><span data-stu-id="08df8-143">This object is the presented type object used for the \***\_to\_xmit** routine.</span></span> <span data-ttu-id="08df8-144">A \* continuación, la rutina **\_ to de \_ transmisión** asigna un objeto de tipo transmitido y lo convierte del objeto presentado (con nombre) en el objeto transmitido.</span><span class="sxs-lookup"><span data-stu-id="08df8-144">The \***\_to\_xmit** routine then allocates a transmitted type object and translates it from the presented (named) object to the transmitted object.</span></span>

 

<span data-ttu-id="08df8-145">Se puede utilizar una matriz de enteros Long para representar una lista vinculada.</span><span class="sxs-lookup"><span data-stu-id="08df8-145">An array of long integers can be used to represent a linked list.</span></span> <span data-ttu-id="08df8-146">De esta manera, la aplicación manipula la lista y la transmisión utiliza una matriz de enteros largos cuando se transmite una lista de este tipo.</span><span class="sxs-lookup"><span data-stu-id="08df8-146">In this way, the application manipulates the list, and the transmission uses an array of long integers when a list of this type is transmitted.</span></span> <span data-ttu-id="08df8-147">Puede empezar con una matriz, pero el uso de una construcción con una matriz abierta de enteros largos es más conveniente.</span><span class="sxs-lookup"><span data-stu-id="08df8-147">You can begin with an array, but using a construct with an open array of long integers is more convenient.</span></span> <span data-ttu-id="08df8-148">El ejemplo siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="08df8-148">The following example shows how to do this.</span></span>

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

<span data-ttu-id="08df8-149">Tenga en cuenta que los prototipos de las rutinas que usan el tipo **LONGARR** se muestran realmente en los archivos stub. h como **PLOC \_ Box** en lugar del tipo **LONGARR** .</span><span class="sxs-lookup"><span data-stu-id="08df8-149">Note that the prototypes of the routines that use the **LONGARR** type are actually displayed in the Stub.h files as **PLOC\_BOX** in place of the **LONGARR** type.</span></span> <span data-ttu-id="08df8-150">Lo mismo se aplica a los códigos auxiliares adecuados en el archivo de código auxiliar \_ c. c.</span><span class="sxs-lookup"><span data-stu-id="08df8-150">The same is true of the appropriate stubs in the Stub\_c.c file.</span></span>

<span data-ttu-id="08df8-151">Debe proporcionar las cuatro funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="08df8-151">You must supply the following four functions:</span></span>

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

<span data-ttu-id="08df8-152">Las rutinas mostradas anteriormente hacen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="08df8-152">The routines shown above do the following:</span></span>

-   <span data-ttu-id="08df8-153">La rutina **LONGARR \_ from \_ local** cuenta los nodos de la lista, asigna un objeto LONGARR con **el tamaño sizeof (\*\*\*\*LONGARR**) + Count \* **sizeof**(**Long**), establece el campo **size** en Count y copia los datos en el campo **DataArr** .</span><span class="sxs-lookup"><span data-stu-id="08df8-153">The **LONGARR\_from\_local** routine counts the nodes of the list, allocates a LONGARR object with the size **sizeof**(**LONGARR**) + Count\***sizeof**(**long**), sets the **Size** field to Count, and copies the data to the **DataArr** field.</span></span>
-   <span data-ttu-id="08df8-154">La rutina **LONGARR \_ to \_ local** crea una lista con nodos de tamaño y transfiere la matriz a los nodos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="08df8-154">The **LONGARR\_to\_local** routine creates a list with Size nodes and transfers the array to the appropriate nodes.</span></span>
-   <span data-ttu-id="08df8-155">La **rutina \_ \_ inst LONGARR Free** libera nada en este caso.</span><span class="sxs-lookup"><span data-stu-id="08df8-155">The **LONGARR\_free\_inst** routine frees nothing in this case.</span></span>
-   <span data-ttu-id="08df8-156">La **rutina \_ \_ local LONGARR Free** libera todos los nodos de la lista.</span><span class="sxs-lookup"><span data-stu-id="08df8-156">The **LONGARR\_free\_local** routine frees all the nodes of the list.</span></span>

 

 