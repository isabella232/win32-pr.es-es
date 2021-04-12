---
title: Prácticas de codificación COM
description: En este tema se describen las formas de hacer que el código COM sea más eficaz y robusto.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104149692"
---
# <a name="com-coding-practices"></a><span data-ttu-id="98794-103">Prácticas de codificación COM</span><span class="sxs-lookup"><span data-stu-id="98794-103">COM Coding Practices</span></span>

<span data-ttu-id="98794-104">En este tema se describen las formas de hacer que el código COM sea más eficaz y robusto.</span><span class="sxs-lookup"><span data-stu-id="98794-104">This topic describes ways to make your COM code more effective and robust.</span></span>

-   [<span data-ttu-id="98794-105">El \_ \_ operador uuidof</span><span class="sxs-lookup"><span data-stu-id="98794-105">The \_\_uuidof Operator</span></span>](/windows)
-   [<span data-ttu-id="98794-106">La macro del IID \_ PPV \_ args</span><span class="sxs-lookup"><span data-stu-id="98794-106">The IID\_PPV\_ARGS Macro</span></span>](/windows)
-   [<span data-ttu-id="98794-107">El patrón SafeRelease</span><span class="sxs-lookup"><span data-stu-id="98794-107">The SafeRelease Pattern</span></span>](#the-saferelease-pattern)
-   [<span data-ttu-id="98794-108">Punteros inteligentes COM</span><span class="sxs-lookup"><span data-stu-id="98794-108">COM Smart Pointers</span></span>](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a><span data-ttu-id="98794-109">El \_ \_ operador uuidof</span><span class="sxs-lookup"><span data-stu-id="98794-109">The \_\_uuidof Operator</span></span>

<span data-ttu-id="98794-110">Al compilar el programa, es posible que obtenga errores del vinculador similares a los siguientes:</span><span class="sxs-lookup"><span data-stu-id="98794-110">When you build your program, you might get linker errors similar to the following:</span></span>

`unresolved external symbol "struct _GUID const IID_IDrawable"`

<span data-ttu-id="98794-111">Este error significa que una constante GUID se declaró con vinculación externa (**extern**) y el vinculador no encontró la definición de la constante.</span><span class="sxs-lookup"><span data-stu-id="98794-111">This error means that a GUID constant was declared with external linkage (**extern**), and the linker could not find the definition of the constant.</span></span> <span data-ttu-id="98794-112">Normalmente, el valor de una constante GUID se exporta desde un archivo de biblioteca estática.</span><span class="sxs-lookup"><span data-stu-id="98794-112">The value of a GUID constant is usually exported from a static library file.</span></span> <span data-ttu-id="98794-113">Si usa Microsoft Visual C++, puede evitar la necesidad de vincular una biblioteca estática mediante el operador **\_ \_ uuidof** .</span><span class="sxs-lookup"><span data-stu-id="98794-113">If you are using Microsoft Visual C++, you can avoid the need to link a static library by using the **\_\_uuidof** operator.</span></span> <span data-ttu-id="98794-114">Este operador es una extensión de lenguaje de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="98794-114">This operator is a Microsoft language extension.</span></span> <span data-ttu-id="98794-115">Devuelve un valor GUID de una expresión.</span><span class="sxs-lookup"><span data-stu-id="98794-115">It returns a GUID value from an expression.</span></span> <span data-ttu-id="98794-116">La expresión puede ser un nombre de tipo de interfaz, un nombre de clase o un puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="98794-116">The expression can be an interface type name, a class name, or an interface pointer.</span></span> <span data-ttu-id="98794-117">Con **\_ \_ uuidof**, puede crear el objeto de cuadro de diálogo de elementos comunes de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="98794-117">Using **\_\_uuidof**, you can create the Common Item Dialog object as follows:</span></span>


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



<span data-ttu-id="98794-118">El compilador extrae el valor GUID del encabezado, por lo que no se necesita ninguna exportación de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="98794-118">The compiler extracts the GUID value from the header, so no library export is necessary.</span></span>

> [!Note]  
> <span data-ttu-id="98794-119">El valor GUID se asocia al nombre de tipo declarando `__declspec(uuid( ... ))` en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="98794-119">The GUID value is associated with the type name by declaring `__declspec(uuid( ... ))` in the header.</span></span> <span data-ttu-id="98794-120">Para obtener más información, vea la documentación de **\_ \_ declspec** en la documentación de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="98794-120">For more information, see the documentation for **\_\_declspec** in the Visual C++ documentation.</span></span>

 

## <a name="the-iid_ppv_args-macro"></a><span data-ttu-id="98794-121">La macro del IID \_ PPV \_ args</span><span class="sxs-lookup"><span data-stu-id="98794-121">The IID\_PPV\_ARGS Macro</span></span>

<span data-ttu-id="98794-122">Vimos que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) y [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) requieren la coerción del parámetro final a un tipo **void \* \*** .</span><span class="sxs-lookup"><span data-stu-id="98794-122">We saw that both [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) require coercing the final parameter to a **void\*\*** type.</span></span> <span data-ttu-id="98794-123">Esto crea la posibilidad de que un tipo no coincida.</span><span class="sxs-lookup"><span data-stu-id="98794-123">This creates the potential for a type mismatch.</span></span> <span data-ttu-id="98794-124">Observe el fragmento de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="98794-124">Consider the following code fragment:</span></span>


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



<span data-ttu-id="98794-125">Este código solicita la interfaz [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , pero pasa un puntero [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) .</span><span class="sxs-lookup"><span data-stu-id="98794-125">This code asks for the [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) interface, but passes in an [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) pointer.</span></span> <span data-ttu-id="98794-126">La expresión **reinterpretar \_ conversión** elude el sistema de tipos de C++, por lo que el compilador no detectará este error.</span><span class="sxs-lookup"><span data-stu-id="98794-126">The **reinterpret\_cast** expression circumvents the C++ type system, so the compiler will not catch this error.</span></span> <span data-ttu-id="98794-127">En el mejor de los casos, si el objeto no implementa la interfaz solicitada, la llamada simplemente produce un error.</span><span class="sxs-lookup"><span data-stu-id="98794-127">In the best case, if the object does not implement the requested interface, the call simply fails.</span></span> <span data-ttu-id="98794-128">En el peor de los casos, la función se ejecuta correctamente y tiene un puntero que no coincide.</span><span class="sxs-lookup"><span data-stu-id="98794-128">In the worst case, the function succeeds and you have a mismatched pointer.</span></span> <span data-ttu-id="98794-129">En otras palabras, el tipo de puntero no coincide con la vtable real en la memoria.</span><span class="sxs-lookup"><span data-stu-id="98794-129">In other words, the pointer type does not match the actual vtable in memory.</span></span> <span data-ttu-id="98794-130">Como puede imaginar, no se puede producir nada bueno en ese momento.</span><span class="sxs-lookup"><span data-stu-id="98794-130">As you can imagine, nothing good can happen at that point.</span></span>

> [!Note]  
> <span data-ttu-id="98794-131">Una *vtable* (tabla de métodos virtuales) es una tabla de punteros de función.</span><span class="sxs-lookup"><span data-stu-id="98794-131">A *vtable* (virtual method table) is a table of function pointers.</span></span> <span data-ttu-id="98794-132">El vtable es la forma en que COM enlaza una llamada al método a su implementación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="98794-132">The vtable is how COM binds a method call to its implementation at run time.</span></span> <span data-ttu-id="98794-133">No casualmente, las vtables son la forma en que la mayoría de los compiladores de C++ implementan métodos virtuales.</span><span class="sxs-lookup"><span data-stu-id="98794-133">Not coincidentally, vtables are how most C++ compilers implement virtual methods.</span></span>

 

<span data-ttu-id="98794-134">La macro del [**IID \_ PPV \_ args**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) ayuda a evitar esta clase de error.</span><span class="sxs-lookup"><span data-stu-id="98794-134">The [**IID\_PPV\_ARGS**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) macro helps to avoid this class of error.</span></span> <span data-ttu-id="98794-135">Para usar esta macro, reemplace el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="98794-135">To use this macro, replace the following code:</span></span>


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



<span data-ttu-id="98794-136">por este:</span><span class="sxs-lookup"><span data-stu-id="98794-136">with this:</span></span>


```C++
IID_PPV_ARGS(&pFileOpen)
```



<span data-ttu-id="98794-137">La macro inserta automáticamente el `__uuidof(IFileOpenDialog)` identificador de interfaz, por lo que se garantiza que coincida con el tipo de puntero.</span><span class="sxs-lookup"><span data-stu-id="98794-137">The macro automatically inserts `__uuidof(IFileOpenDialog)` for the interface identifier, so it is guaranteed to match the pointer type.</span></span> <span data-ttu-id="98794-138">Este es el código modificado (y correcto):</span><span class="sxs-lookup"><span data-stu-id="98794-138">Here is the modified (and correct) code:</span></span>


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



<span data-ttu-id="98794-139">Puede usar la misma macro con [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span><span class="sxs-lookup"><span data-stu-id="98794-139">You can use the same macro with [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a><span data-ttu-id="98794-140">El patrón SafeRelease</span><span class="sxs-lookup"><span data-stu-id="98794-140">The SafeRelease Pattern</span></span>

<span data-ttu-id="98794-141">El recuento de referencias es uno de los elementos de programación que es muy sencillo, pero también es tedioso, lo que facilita la obtención de un error.</span><span class="sxs-lookup"><span data-stu-id="98794-141">Reference counting is one of those things in programming that is basically easy, but is also tedious, which makes it easy to get wrong.</span></span> <span data-ttu-id="98794-142">Entre los errores típicos se incluyen:</span><span class="sxs-lookup"><span data-stu-id="98794-142">Typical errors include:</span></span>

-   <span data-ttu-id="98794-143">No se puede liberar un puntero de interfaz cuando se ha terminado de usarlo.</span><span class="sxs-lookup"><span data-stu-id="98794-143">Failing to release an interface pointer when you are done using it.</span></span> <span data-ttu-id="98794-144">Esta clase de error hará que el programa pierda memoria y otros recursos, ya que los objetos no se destruyen.</span><span class="sxs-lookup"><span data-stu-id="98794-144">This class of bug will cause your program to leak memory and other resources, because objects are not destroyed.</span></span>
-   <span data-ttu-id="98794-145">Llamando a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) con un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="98794-145">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with an invalid pointer.</span></span> <span data-ttu-id="98794-146">Por ejemplo, este error puede producirse si el objeto no se ha creado nunca.</span><span class="sxs-lookup"><span data-stu-id="98794-146">For example, this error can happen if the object was never created.</span></span> <span data-ttu-id="98794-147">Esta categoría de error probablemente hará que el programa se bloquee.</span><span class="sxs-lookup"><span data-stu-id="98794-147">This category of bug will probably cause your program to crash.</span></span>
-   <span data-ttu-id="98794-148">Desreferenciación de un puntero de interfaz después de llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="98794-148">Dereferencing an interface pointer after [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) is called.</span></span> <span data-ttu-id="98794-149">Este error puede provocar que el programa se bloquee.</span><span class="sxs-lookup"><span data-stu-id="98794-149">This bug may cause your program to crash.</span></span> <span data-ttu-id="98794-150">Lo que es peor, puede hacer que el programa se bloquee de forma aleatoria más adelante, lo que dificulta el seguimiento del error original.</span><span class="sxs-lookup"><span data-stu-id="98794-150">Worse, it may cause your program to crash at a random later time, making it hard to track down the original error.</span></span>

<span data-ttu-id="98794-151">Una manera de evitar estos errores es llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) a través de una función que libera el puntero de forma segura.</span><span class="sxs-lookup"><span data-stu-id="98794-151">One way to avoid these bugs is to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) through a function that safely releases the pointer.</span></span> <span data-ttu-id="98794-152">En el código siguiente se muestra una función que lo hace:</span><span class="sxs-lookup"><span data-stu-id="98794-152">The following code shows a function that does this:</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



<span data-ttu-id="98794-153">Esta función toma un puntero de interfaz COM como parámetro y hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="98794-153">This function takes a COM interface pointer as a parameter and does the following:</span></span>

1.  <span data-ttu-id="98794-154">Comprueba si el puntero es **null**.</span><span class="sxs-lookup"><span data-stu-id="98794-154">Checks whether the pointer is **NULL**.</span></span>
2.  <span data-ttu-id="98794-155">Llama a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) si el puntero no es **null**.</span><span class="sxs-lookup"><span data-stu-id="98794-155">Calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) if the pointer is not **NULL**.</span></span>
3.  <span data-ttu-id="98794-156">Establece el puntero en **null**.</span><span class="sxs-lookup"><span data-stu-id="98794-156">Sets the pointer to **NULL**.</span></span>

<span data-ttu-id="98794-157">A continuación se muestra un ejemplo de cómo usar `SafeRelease` :</span><span class="sxs-lookup"><span data-stu-id="98794-157">Here is an example of how to use `SafeRelease`:</span></span>


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



<span data-ttu-id="98794-158">Si [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) se realiza correctamente, la llamada a `SafeRelease` libera el puntero.</span><span class="sxs-lookup"><span data-stu-id="98794-158">If [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) succeeds, the call to `SafeRelease` releases the pointer.</span></span> <span data-ttu-id="98794-159">Si se produce un error de **CoCreateInstance** , *PFileOpen* sigue siendo **null**.</span><span class="sxs-lookup"><span data-stu-id="98794-159">If **CoCreateInstance** fails, *pFileOpen* remains **NULL**.</span></span> <span data-ttu-id="98794-160">La `SafeRelease` función comprueba esto y omite la llamada a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="98794-160">The `SafeRelease` function checks for this and skips the call to [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span>

<span data-ttu-id="98794-161">También es seguro llamar a `SafeRelease` más de una vez en el mismo puntero, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="98794-161">It is also safe to call `SafeRelease` more than once on the same pointer, as shown here:</span></span>


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a><span data-ttu-id="98794-162">Punteros inteligentes COM</span><span class="sxs-lookup"><span data-stu-id="98794-162">COM Smart Pointers</span></span>

<span data-ttu-id="98794-163">La `SafeRelease` función es útil, pero requiere que recuerde dos cosas:</span><span class="sxs-lookup"><span data-stu-id="98794-163">The `SafeRelease` function is useful, but it requires you to remember two things:</span></span>

-   <span data-ttu-id="98794-164">Inicialice todos los punteros de interfaz en **null**.</span><span class="sxs-lookup"><span data-stu-id="98794-164">Initialize every interface pointer to **NULL**.</span></span>
-   <span data-ttu-id="98794-165">Llame a `SafeRelease` antes de que cada puntero salga del ámbito.</span><span class="sxs-lookup"><span data-stu-id="98794-165">Call `SafeRelease` before each pointer goes out of scope.</span></span>

<span data-ttu-id="98794-166">Como programador de C++, es probable que piense que no debe recordar nada de esto.</span><span class="sxs-lookup"><span data-stu-id="98794-166">As a C++ programmer, you are probably thinking that you shouldn't have to remember either of these things.</span></span> <span data-ttu-id="98794-167">Después de todo, este es el motivo por el que C++ tiene constructores y destructores.</span><span class="sxs-lookup"><span data-stu-id="98794-167">After all, that's why C++ has constructors and destructors.</span></span> <span data-ttu-id="98794-168">Estaría bien tener una clase que contiene el puntero de interfaz subyacente e inicializa y libera automáticamente el puntero.</span><span class="sxs-lookup"><span data-stu-id="98794-168">It would be nice to have a class that wraps the underlying interface pointer and automatically initializes and releases the pointer.</span></span> <span data-ttu-id="98794-169">En otras palabras, queremos algo parecido a esto:</span><span class="sxs-lookup"><span data-stu-id="98794-169">In other words, we want something like this:</span></span>


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



<span data-ttu-id="98794-170">La definición de clase que se muestra aquí está incompleta y no se puede usar como se muestra.</span><span class="sxs-lookup"><span data-stu-id="98794-170">The class definition shown here is incomplete, and is not usable as shown.</span></span> <span data-ttu-id="98794-171">Como mínimo, debe definir un constructor de copias, un operador de asignación y una manera de tener acceso al puntero COM subyacente.</span><span class="sxs-lookup"><span data-stu-id="98794-171">At a minimum, you would need to define a copy constructor, an assignment operator, and a way to access the underlying COM pointer.</span></span> <span data-ttu-id="98794-172">Afortunadamente, no es necesario realizar ninguna tarea, ya que Microsoft Visual Studio ya proporciona una clase de puntero inteligente como parte del Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="98794-172">Fortunately, you don't need to do any of this work, because Microsoft Visual Studio already provides a smart pointer class as part of the Active Template Library (ATL).</span></span>

<span data-ttu-id="98794-173">La clase de puntero inteligente ATL se denomina **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="98794-173">The ATL smart pointer class is named **CComPtr**.</span></span> <span data-ttu-id="98794-174">(También hay una clase **CComQIPtr** , que no se trata aquí). Este es el ejemplo de [cuadro de diálogo Abrir](example--the-open-dialog-box.md) que se ha vuelto a escribir para usar **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="98794-174">(There is also a **CComQIPtr** class, which is not discussed here.) Here is the [Open Dialog Box](example--the-open-dialog-box.md) example rewritten to use **CComPtr**.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="98794-175">La diferencia principal entre este código y el ejemplo original es que esta versión no llama explícitamente a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="98794-175">The main difference between this code and the original example is that this version does not explicitly call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="98794-176">Cuando la instancia de **CComPtr** sale del ámbito, el destructor llama a **Release** en el puntero subyacente.</span><span class="sxs-lookup"><span data-stu-id="98794-176">When the **CComPtr** instance goes out of scope, the destructor calls **Release** on the underlying pointer.</span></span>

<span data-ttu-id="98794-177">**CComPtr** es una plantilla de clase.</span><span class="sxs-lookup"><span data-stu-id="98794-177">**CComPtr** is a class template.</span></span> <span data-ttu-id="98794-178">El argumento de plantilla es el tipo de interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="98794-178">The template argument is the COM interface type.</span></span> <span data-ttu-id="98794-179">Internamente, **CComPtr** contiene un puntero de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="98794-179">Internally, **CComPtr** holds a pointer of that type.</span></span> <span data-ttu-id="98794-180">**CComPtr** invalida **Operator-> ()** y **Operator& ()** para que la clase actúe como el puntero subyacente.</span><span class="sxs-lookup"><span data-stu-id="98794-180">**CComPtr** overrides **operator->()** and **operator&()** so that the class acts like the underlying pointer.</span></span> <span data-ttu-id="98794-181">Por ejemplo, el código siguiente es equivalente a llamar al método **IFileOpenDialog:: show** directamente:</span><span class="sxs-lookup"><span data-stu-id="98794-181">For example, the following code is equivalent to calling the **IFileOpenDialog::Show** method directly:</span></span>


```C++
hr = pFileOpen->Show(NULL);
```



<span data-ttu-id="98794-182">**CComPtr** también define un método **CComPtr:: CoCreateInstance** , que llama a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) de com con algunos valores de parámetro predeterminados.</span><span class="sxs-lookup"><span data-stu-id="98794-182">**CComPtr** also defines a **CComPtr::CoCreateInstance** method, which calls the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function with some default parameter values.</span></span> <span data-ttu-id="98794-183">El único parámetro necesario es el identificador de clase, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="98794-183">The only required parameter is the class identifier, as the next example shows:</span></span>


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



<span data-ttu-id="98794-184">El método **CComPtr:: CoCreateInstance** se proporciona únicamente por comodidad; puede seguir llamando a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) de com, si lo prefiere.</span><span class="sxs-lookup"><span data-stu-id="98794-184">The **CComPtr::CoCreateInstance** method is provided purely as a convenience; you can still call the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, if you prefer.</span></span>

## <a name="next"></a><span data-ttu-id="98794-185">Siguientes</span><span class="sxs-lookup"><span data-stu-id="98794-185">Next</span></span>

[<span data-ttu-id="98794-186">Control de errores en COM</span><span class="sxs-lookup"><span data-stu-id="98794-186">Error Handling in COM</span></span>](error-handling-in-com.md)

 

 