---
title: Crear un objeto en COM
description: Para usar una interfaz COM, el programa crea primero una instancia de un objeto que implementa esa interfaz.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420624"
---
# <a name="creating-an-object-in-com"></a><span data-ttu-id="6ef41-103">Crear un objeto en COM</span><span class="sxs-lookup"><span data-stu-id="6ef41-103">Creating an Object in COM</span></span>

<span data-ttu-id="6ef41-104">Una vez que un subproceso ha inicializado la biblioteca COM, es seguro que el subproceso use las interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="6ef41-104">After a thread has initialized the COM library, it is safe for the thread to use COM interfaces.</span></span> <span data-ttu-id="6ef41-105">Para usar una interfaz COM, el programa crea primero una instancia de un objeto que implementa esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="6ef41-105">To use a COM interface, your program first creates an instance of an object that implements that interface.</span></span>

<span data-ttu-id="6ef41-106">En general, hay dos maneras de crear un objeto COM:</span><span class="sxs-lookup"><span data-stu-id="6ef41-106">In general, there are two ways to create a COM object:</span></span>

-   <span data-ttu-id="6ef41-107">El módulo que implementa el objeto podría proporcionar una función diseñada específicamente para crear instancias de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="6ef41-107">The module that implements the object might provide a function specifically designed to create instances of that object.</span></span>
-   <span data-ttu-id="6ef41-108">Como alternativa, COM proporciona una función de creación genérica denominada [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="6ef41-108">Alternatively, COM provides a generic creation function named [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="6ef41-109">Por ejemplo, tome el `Shape` objeto hipotético del tema [¿Qué es una interfaz com?](what-is-a-com-interface-.md).</span><span class="sxs-lookup"><span data-stu-id="6ef41-109">For example, take the hypothetical `Shape` object from the topic [What Is a COM Interface?](what-is-a-com-interface-.md).</span></span> <span data-ttu-id="6ef41-110">En ese ejemplo, el `Shape` objeto implementa una interfaz denominada `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="6ef41-110">In that example, the `Shape` object implements an interface named `IDrawable`.</span></span> <span data-ttu-id="6ef41-111">La biblioteca de gráficos que implementa el `Shape` objeto podría exportar una función con la siguiente firma.</span><span class="sxs-lookup"><span data-stu-id="6ef41-111">The graphics library that implements the `Shape` object might export a function with the following signature.</span></span>


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



<span data-ttu-id="6ef41-112">Dada esta función, podría crear un nuevo `Shape` objeto como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="6ef41-112">Given this function, you could create a new `Shape` object as follows.</span></span>


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="6ef41-113">El parámetro *ppShape* es de tipo puntero a puntero a `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="6ef41-113">The *ppShape* parameter is of type pointer-to-pointer-to-`IDrawable`.</span></span> <span data-ttu-id="6ef41-114">Si no ha encontrado este patrón antes, el direccionamiento indirecto doble podría ser desconcertantes.</span><span class="sxs-lookup"><span data-stu-id="6ef41-114">If you have not seen this pattern before, the double indirection might be puzzling.</span></span>

<span data-ttu-id="6ef41-115">Tenga en cuenta los requisitos de la `CreateShape` función.</span><span class="sxs-lookup"><span data-stu-id="6ef41-115">Consider the requirements of the `CreateShape` function.</span></span> <span data-ttu-id="6ef41-116">La función debe devolver un `IDrawable` puntero al llamador.</span><span class="sxs-lookup"><span data-stu-id="6ef41-116">The function must give an `IDrawable` pointer back to the caller.</span></span> <span data-ttu-id="6ef41-117">Pero el valor devuelto de la función ya se usa para el código de error o de operación correcta.</span><span class="sxs-lookup"><span data-stu-id="6ef41-117">But the function's return value is already used for the error/success code.</span></span> <span data-ttu-id="6ef41-118">Por lo tanto, el puntero se debe devolver a través de un argumento a la función.</span><span class="sxs-lookup"><span data-stu-id="6ef41-118">Therefore, the pointer must be returned through an argument to the function.</span></span> <span data-ttu-id="6ef41-119">El autor de la llamada pasará una variable de tipo `IDrawable*` a la función y la función sobrescribirá esta variable con un nuevo `IDrawable` puntero.</span><span class="sxs-lookup"><span data-stu-id="6ef41-119">The caller will pass a variable of type `IDrawable*` to the function, and the function will overwrite this variable with a new `IDrawable` pointer.</span></span> <span data-ttu-id="6ef41-120">En C++, solo hay dos maneras de que una función sobrescriba un valor de parámetro: pasar por referencia o pasar por dirección.</span><span class="sxs-lookup"><span data-stu-id="6ef41-120">In C++, there are only two ways for a function to overwrite a parameter value: pass by reference, or pass by address.</span></span> <span data-ttu-id="6ef41-121">COM utiliza el último, pass-by-Address.</span><span class="sxs-lookup"><span data-stu-id="6ef41-121">COM uses the latter, pass-by-address.</span></span> <span data-ttu-id="6ef41-122">Y la dirección de un puntero es un puntero a un puntero, por lo que el tipo de parámetro debe ser `IDrawable**` .</span><span class="sxs-lookup"><span data-stu-id="6ef41-122">And the address of a pointer is a pointer-to-a-pointer, so the parameter type must be `IDrawable**`.</span></span>

<span data-ttu-id="6ef41-123">Este es un diagrama que le ayudará a visualizar lo que está ocurriendo.</span><span class="sxs-lookup"><span data-stu-id="6ef41-123">Here is a diagram to help visualize what's going on.</span></span>

![diagrama que muestra el direccionamiento indirecto de puntero doble](images/com03.png)

<span data-ttu-id="6ef41-125">La `CreateShape` función usa la dirección de *pShape* ( `&pShape` ) para escribir un nuevo valor de puntero en *pShape*.</span><span class="sxs-lookup"><span data-stu-id="6ef41-125">The `CreateShape` function uses the address of *pShape* (`&pShape`) to write a new pointer value to *pShape*.</span></span>

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a><span data-ttu-id="6ef41-126">CoCreateInstance: una manera genérica de crear objetos</span><span class="sxs-lookup"><span data-stu-id="6ef41-126">CoCreateInstance: A Generic Way to Create Objects</span></span>

<span data-ttu-id="6ef41-127">La función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) proporciona un mecanismo genérico para crear objetos.</span><span class="sxs-lookup"><span data-stu-id="6ef41-127">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function provides a generic mechanism for creating objects.</span></span> <span data-ttu-id="6ef41-128">Para comprender **CoCreateInstance**, tenga en cuenta que dos objetos com pueden implementar la misma interfaz y un objeto puede implementar dos o más interfaces.</span><span class="sxs-lookup"><span data-stu-id="6ef41-128">To understand **CoCreateInstance**, keep in mind that two COM objects can implement the same interface, and one object can implement two or more interfaces.</span></span> <span data-ttu-id="6ef41-129">Por lo tanto, una función genérica que crea objetos necesita dos fragmentos de información.</span><span class="sxs-lookup"><span data-stu-id="6ef41-129">Thus, a generic function that creates objects needs two pieces of information.</span></span>

-   <span data-ttu-id="6ef41-130">Objeto que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="6ef41-130">Which object to create.</span></span>
-   <span data-ttu-id="6ef41-131">La interfaz que se va a obtener del objeto.</span><span class="sxs-lookup"><span data-stu-id="6ef41-131">Which interface to get from the object.</span></span>

<span data-ttu-id="6ef41-132">Pero, ¿cómo se indica esta información cuando se llama a la función?</span><span class="sxs-lookup"><span data-stu-id="6ef41-132">But how do we indicate this information when we call the function?</span></span> <span data-ttu-id="6ef41-133">En COM, un objeto o una interfaz se identifica asignando un número de 128 bits, denominado *identificador único global* (GUID).</span><span class="sxs-lookup"><span data-stu-id="6ef41-133">In COM, an object or an interface is identified by assigning it a 128-bit number, called a *globally unique identifier* (GUID).</span></span> <span data-ttu-id="6ef41-134">Los GUID se generan de forma que sean realmente únicos.</span><span class="sxs-lookup"><span data-stu-id="6ef41-134">GUIDs are generated in a way that makes them effectively unique.</span></span> <span data-ttu-id="6ef41-135">Los GUID son una solución para el problema de cómo crear identificadores únicos sin una entidad de registro central.</span><span class="sxs-lookup"><span data-stu-id="6ef41-135">GUIDs are a solution to the problem of how to create unique identifiers without a central registration authority.</span></span> <span data-ttu-id="6ef41-136">Los GUID a veces se denominan *identificadores únicos universales* (UUID).</span><span class="sxs-lookup"><span data-stu-id="6ef41-136">GUIDs are sometimes called *universally unique identifiers* (UUIDs).</span></span> <span data-ttu-id="6ef41-137">Antes de COM, se usaban en DCE/RPC (entorno informático distribuido o llamada a procedimiento remoto).</span><span class="sxs-lookup"><span data-stu-id="6ef41-137">Prior to COM, they were used in DCE/RPC (Distributed Computing Environment/Remote Procedure Call).</span></span> <span data-ttu-id="6ef41-138">Existen varios algoritmos para crear nuevos GUID.</span><span class="sxs-lookup"><span data-stu-id="6ef41-138">Several algorithms exist for creating new GUIDs.</span></span> <span data-ttu-id="6ef41-139">No todos estos algoritmos garantizan estrictamente la unicidad, pero la probabilidad de crear accidentalmente el mismo valor GUID dos veces es extremadamente pequeña, pero es realmente cero.</span><span class="sxs-lookup"><span data-stu-id="6ef41-139">Not all of these algorithms strictly guarantee uniqueness, but the probability of accidentally creating the same GUID value twice is extremely small—effectively zero.</span></span> <span data-ttu-id="6ef41-140">Los GUID se pueden usar para identificar cualquier tipo de entidad, no solo objetos e interfaces.</span><span class="sxs-lookup"><span data-stu-id="6ef41-140">GUIDs can be used to identify any sort of entity, not just objects and interfaces.</span></span> <span data-ttu-id="6ef41-141">Sin embargo, este es el único uso que nos preocupa en este módulo.</span><span class="sxs-lookup"><span data-stu-id="6ef41-141">However, that is the only use that concerns us in this module.</span></span>

<span data-ttu-id="6ef41-142">Por ejemplo, la `Shapes` biblioteca podría declarar dos constantes GUID:</span><span class="sxs-lookup"><span data-stu-id="6ef41-142">For example, the `Shapes` library might declare two GUID constants:</span></span>


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



<span data-ttu-id="6ef41-143">(Puede suponer que los valores numéricos reales de 128 bits para estas constantes se definen en otro lugar). La **\_ forma de CLSID** constante identifica el `Shape` objeto, mientras que el **IID constante \_ IDrawable** identifica la `IDrawable` interfaz.</span><span class="sxs-lookup"><span data-stu-id="6ef41-143">(You can assume that the actual 128-bit numeric values for these constants are defined elsewhere.) The constant **CLSID\_Shape** identifies the `Shape` object, while the constant **IID\_IDrawable** identifies the `IDrawable` interface.</span></span> <span data-ttu-id="6ef41-144">El prefijo "CLSID" representa el *identificador de clase* y el *IID* de prefijo representa el identificador de *interfaz*.</span><span class="sxs-lookup"><span data-stu-id="6ef41-144">The prefix "CLSID" stands for *class identifier*, and the prefix *IID* stands for *interface identifier*.</span></span> <span data-ttu-id="6ef41-145">Se trata de convenciones de nomenclatura estándar en COM.</span><span class="sxs-lookup"><span data-stu-id="6ef41-145">These are standard naming conventions in COM.</span></span>

<span data-ttu-id="6ef41-146">Dados estos valores, crearía una nueva `Shape` instancia de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6ef41-146">Given these values, you would create a new `Shape` instance as follows:</span></span>


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="6ef41-147">La función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) tiene cinco parámetros.</span><span class="sxs-lookup"><span data-stu-id="6ef41-147">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function has five parameters.</span></span> <span data-ttu-id="6ef41-148">Los parámetros primero y cuarto son el identificador de clase y el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="6ef41-148">The first and fourth parameters are the class identifier and interface identifier.</span></span> <span data-ttu-id="6ef41-149">En efecto, estos parámetros indican a la función "cree el objeto de forma y proporcione un puntero a la interfaz IDrawable".</span><span class="sxs-lookup"><span data-stu-id="6ef41-149">In effect, these parameters tell the function, "Create the Shape object, and give me a pointer to the IDrawable interface."</span></span>

<span data-ttu-id="6ef41-150">Establezca el segundo parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="6ef41-150">Set the second parameter to **NULL**.</span></span> <span data-ttu-id="6ef41-151">(Para obtener más información sobre el significado de este parámetro, vea la [agregación](/windows/desktop/com/aggregation) de temas en la documentación de com). El tercer parámetro toma un conjunto de marcas cuyo propósito principal es especificar el *contexto de ejecución* para el objeto.</span><span class="sxs-lookup"><span data-stu-id="6ef41-151">(For more information about the meaning of this parameter, see the topic [Aggregation](/windows/desktop/com/aggregation) in the COM documentation.) The third parameter takes a set of flags whose main purpose is to specify the *execution context* for the object.</span></span> <span data-ttu-id="6ef41-152">El contexto de ejecución especifica si el objeto se ejecuta en el mismo proceso que la aplicación; en un proceso diferente en el mismo equipo; o en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="6ef41-152">The execution context specifies whether the object runs in the same process as the application; in a different process on the same computer; or on a remote computer.</span></span> <span data-ttu-id="6ef41-153">En la tabla siguiente se muestran los valores más comunes para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="6ef41-153">The following table shows the most common values for this parameter.</span></span>



| <span data-ttu-id="6ef41-154">Marca</span><span class="sxs-lookup"><span data-stu-id="6ef41-154">Flag</span></span>                       | <span data-ttu-id="6ef41-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ef41-155">Description</span></span>                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef41-156">**\_servidor INproc de CLSCTX \_**</span><span class="sxs-lookup"><span data-stu-id="6ef41-156">**CLSCTX\_INPROC\_SERVER**</span></span> | <span data-ttu-id="6ef41-157">Mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="6ef41-157">Same process.</span></span>                                                                                                                                                      |
| <span data-ttu-id="6ef41-158">**\_servidor local de CLSCTX \_**</span><span class="sxs-lookup"><span data-stu-id="6ef41-158">**CLSCTX\_LOCAL\_SERVER**</span></span>  | <span data-ttu-id="6ef41-159">Proceso diferente, el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="6ef41-159">Different process, same computer.</span></span>                                                                                                                                  |
| <span data-ttu-id="6ef41-160">**\_servidor remoto \_ CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="6ef41-160">**CLSCTX\_REMOTE\_SERVER**</span></span> | <span data-ttu-id="6ef41-161">Equipo diferente.</span><span class="sxs-lookup"><span data-stu-id="6ef41-161">Different computer.</span></span>                                                                                                                                                |
| <span data-ttu-id="6ef41-162">**CLSCTX \_ todo**</span><span class="sxs-lookup"><span data-stu-id="6ef41-162">**CLSCTX\_ALL**</span></span>            | <span data-ttu-id="6ef41-163">Use la opción más eficaz que admite el objeto.</span><span class="sxs-lookup"><span data-stu-id="6ef41-163">Use the most efficient option that the object supports.</span></span> <span data-ttu-id="6ef41-164">(La clasificación, de más eficaz a menos eficiente, es: en proceso, fuera de proceso y entre equipos).</span><span class="sxs-lookup"><span data-stu-id="6ef41-164">(The ranking, from most efficient to least efficient, is: in-process, out-of-process, and cross-computer.)</span></span> |



 

<span data-ttu-id="6ef41-165">La documentación de un componente determinado puede indicarle el contexto de ejecución que admite el objeto.</span><span class="sxs-lookup"><span data-stu-id="6ef41-165">The documentation for a particular component might tell you which execution context the object supports.</span></span> <span data-ttu-id="6ef41-166">Si no es así, use **CLSCTX \_ All**.</span><span class="sxs-lookup"><span data-stu-id="6ef41-166">If not, use **CLSCTX\_ALL**.</span></span> <span data-ttu-id="6ef41-167">Si solicita un contexto de ejecución que no admite el objeto, la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) devuelve el código de error **REGDB \_ E \_ CLASSNOTREG**.</span><span class="sxs-lookup"><span data-stu-id="6ef41-167">If you request an execution context that the object does not support, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function returns the error code **REGDB\_E\_CLASSNOTREG**.</span></span> <span data-ttu-id="6ef41-168">Este código de error también puede indicar que el CLSID no corresponde a ningún componente registrado en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="6ef41-168">This error code can also indicate that the CLSID does not correspond to any component registered on the user's computer.</span></span>

<span data-ttu-id="6ef41-169">El quinto parámetro de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) recibe un puntero a la interfaz.</span><span class="sxs-lookup"><span data-stu-id="6ef41-169">The fifth parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) receives a pointer to the interface.</span></span> <span data-ttu-id="6ef41-170">Dado que **CoCreateInstance** es un mecanismo genérico, este parámetro no se puede escribir fuertemente tipado.</span><span class="sxs-lookup"><span data-stu-id="6ef41-170">Because **CoCreateInstance** is a generic mechanism, this parameter cannot be strongly typed.</span></span> <span data-ttu-id="6ef41-171">En su lugar, el tipo de datos es **void \* \*** y el llamador debe forzar la dirección del puntero a un **tipo \* \* void** .</span><span class="sxs-lookup"><span data-stu-id="6ef41-171">Instead, the data type is **void\*\***, and the caller must coerce the address of the pointer to a **void\*\*** type.</span></span> <span data-ttu-id="6ef41-172">Este es el propósito de la **\_ conversión de reinterpretación** en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="6ef41-172">That is the purpose of the **reinterpret\_cast** in the previous example.</span></span>

<span data-ttu-id="6ef41-173">Es fundamental comprobar el valor devuelto de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="6ef41-173">It is crucial to check the return value of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="6ef41-174">Si la función devuelve un código de error, el puntero de interfaz COM no es válido y, al intentar desreferenciarlo, puede provocar que el programa se bloquee.</span><span class="sxs-lookup"><span data-stu-id="6ef41-174">If the function returns an error code, the COM interface pointer is invalid, and attempting to dereference it can cause your program to crash.</span></span>

<span data-ttu-id="6ef41-175">Internamente, la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utiliza varias técnicas para crear un objeto.</span><span class="sxs-lookup"><span data-stu-id="6ef41-175">Internally, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function uses various techniques to create an object.</span></span> <span data-ttu-id="6ef41-176">En el caso más simple, busca el identificador de clase en el registro.</span><span class="sxs-lookup"><span data-stu-id="6ef41-176">In the simplest case, it looks up the class identifier in the registry.</span></span> <span data-ttu-id="6ef41-177">La entrada del registro señala a un archivo DLL o EXE que implementa el objeto.</span><span class="sxs-lookup"><span data-stu-id="6ef41-177">The registry entry points to a DLL or EXE that implements the object.</span></span> <span data-ttu-id="6ef41-178">**CoCreateInstance** también puede usar información de un catálogo com+ o un manifiesto en paralelo (SxS).</span><span class="sxs-lookup"><span data-stu-id="6ef41-178">**CoCreateInstance** can also use information from a COM+ catalog or a side-by-side (SxS) manifest.</span></span> <span data-ttu-id="6ef41-179">Independientemente de, los detalles son transparentes para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6ef41-179">Regardless, the details are transparent to the caller.</span></span> <span data-ttu-id="6ef41-180">Para obtener más información acerca de los detalles internos de **CoCreateInstance**, consulte [com clients and Servers](/windows/desktop/com/com-clients-and-servers).</span><span class="sxs-lookup"><span data-stu-id="6ef41-180">For more information about the internal details of **CoCreateInstance**, see [COM Clients and Servers](/windows/desktop/com/com-clients-and-servers).</span></span>

<span data-ttu-id="6ef41-181">El `Shapes` ejemplo que hemos usado es algo inventado, por lo que ahora vamos a pasar a un ejemplo real de com en acción: mostrar el cuadro de diálogo **abrir** para que el usuario seleccione un archivo.</span><span class="sxs-lookup"><span data-stu-id="6ef41-181">The `Shapes` example that we have been using is somewhat contrived, so now let's turn to a real-world example of COM in action: displaying the **Open** dialog box for the user to select a file.</span></span>

## <a name="next"></a><span data-ttu-id="6ef41-182">Siguientes</span><span class="sxs-lookup"><span data-stu-id="6ef41-182">Next</span></span>

[<span data-ttu-id="6ef41-183">Ejemplo: el cuadro de diálogo abrir</span><span class="sxs-lookup"><span data-stu-id="6ef41-183">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)

 

 