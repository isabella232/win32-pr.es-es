---
title: Reglas para usar punteros
description: Trasladar el código para compilar para Windows de 32 y 64 bits es sencillo. Solo necesita seguir unas cuantas reglas simples sobre cómo convertir punteros y usar los nuevos tipos de datos en el código. Las reglas para la manipulación de puntero son las siguientes.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- reglas para usar los punteros programación de Windows de 64 bits
- manipulación de puntero de 64 programación de Windows de bits
- convertir punteros en programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103995699"
---
# <a name="rules-for-using-pointers"></a><span data-ttu-id="9ec14-108">Reglas para usar punteros</span><span class="sxs-lookup"><span data-stu-id="9ec14-108">Rules for Using Pointers</span></span>

<span data-ttu-id="9ec14-109">Trasladar el código para compilar para Windows de 32 y 64 bits es sencillo.</span><span class="sxs-lookup"><span data-stu-id="9ec14-109">Porting your code to compile for both 32- and 64-bit Microsoft Windows is straightforward.</span></span> <span data-ttu-id="9ec14-110">Solo necesita seguir unas cuantas reglas simples sobre cómo convertir punteros y usar los nuevos tipos de datos en el código.</span><span class="sxs-lookup"><span data-stu-id="9ec14-110">You need only follow a few simple rules about casting pointers, and use the new data types in your code.</span></span> <span data-ttu-id="9ec14-111">Las reglas para la manipulación de puntero son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="9ec14-111">The rules for pointer manipulation are as follows.</span></span>

1.  <span data-ttu-id="9ec14-112">No convierta punteros a **int**, **Long**, **ULong** o **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="9ec14-112">Do not cast pointers to **int**, **long**, **ULONG**, or **DWORD**.</span></span>

    <span data-ttu-id="9ec14-113">Si debe convertir un puntero para probar algunos bits, establecer o borrar bits o manipular de otro modo su contenido, use el tipo **uint \_ ptr** o **int \_ ptr** .</span><span class="sxs-lookup"><span data-stu-id="9ec14-113">If you must cast a pointer to test some bits, set or clear bits, or otherwise manipulate its contents, use the **UINT\_PTR** or **INT\_PTR** type.</span></span> <span data-ttu-id="9ec14-114">Estos tipos son tipos enteros que se escalan al tamaño de un puntero para Windows de 32 y 64 bits (por ejemplo, **ULong** para windows de 32 bits y \_ Int64 para Windows de 64 bits).</span><span class="sxs-lookup"><span data-stu-id="9ec14-114">These types are integral types that scale to the size of a pointer for both 32- and 64-bit Windows (for example, **ULONG** for 32-bit Windows and \_int64 for 64-bit Windows).</span></span> <span data-ttu-id="9ec14-115">Por ejemplo, suponga que está migrando el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ec14-115">For example, assume you are porting the following code:</span></span>

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    <span data-ttu-id="9ec14-116">Como parte del proceso de portabilidad, cambiaría el código como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="9ec14-116">As a part of the porting process, you would change the code as follows:</span></span>

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    <span data-ttu-id="9ec14-117">Use **uint \_ ptr** e **int \_ ptr** cuando sea apropiado (y, si no está seguro de si son necesarios, no hay ningún daño en su uso en caso de que se produzcan).</span><span class="sxs-lookup"><span data-stu-id="9ec14-117">Use **UINT\_PTR** and **INT\_PTR** where appropriate (and if you are uncertain whether they are required, there is no harm in using them just in case).</span></span> <span data-ttu-id="9ec14-118">No convierta los punteros a los tipos **ULong**, **Long**, **int**, **uint** o **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="9ec14-118">Do not cast your pointers to the types **ULONG**, **LONG**, **INT**, **UINT**, or **DWORD**.</span></span>

    <span data-ttu-id="9ec14-119">Tenga en cuenta que el **identificador** se define como un valor **\* nulo**, por lo que conversión un valor de **identificador** a un valor **ULong** para probar, establecer o borrar los bits de orden inferior 2 es un error en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9ec14-119">Note that **HANDLE** is defined as a **void\***, so typecasting a **HANDLE** value to a **ULONG** value to test, set, or clear the low-order 2 bits is an error on 64-bit Windows.</span></span>

2.  <span data-ttu-id="9ec14-120">Utilice la función **PtrToLong** o **PtrToUlong** para truncar los punteros.</span><span class="sxs-lookup"><span data-stu-id="9ec14-120">Use the **PtrToLong** or **PtrToUlong** function to truncate pointers.</span></span>

    <span data-ttu-id="9ec14-121">Si debe truncar un puntero a un valor de 32 bits, utilice la función **PtrToLong** o **PtrToUlong** (definida en Basetsd. h).</span><span class="sxs-lookup"><span data-stu-id="9ec14-121">If you must truncate a pointer to a 32-bit value, use the **PtrToLong** or **PtrToUlong** function (defined in Basetsd.h).</span></span> <span data-ttu-id="9ec14-122">Estas funciones deshabilitan la advertencia de truncamiento de puntero mientras dure la llamada.</span><span class="sxs-lookup"><span data-stu-id="9ec14-122">These functions disable the pointer truncation warning for the duration of the call.</span></span>

    <span data-ttu-id="9ec14-123">Use estas funciones con cuidado.</span><span class="sxs-lookup"><span data-stu-id="9ec14-123">Use these functions carefully.</span></span> <span data-ttu-id="9ec14-124">Después de convertir una variable de puntero mediante una de estas funciones, no la use nunca como un puntero de nuevo.</span><span class="sxs-lookup"><span data-stu-id="9ec14-124">After you convert a pointer variable using one of these functions, never use it as a pointer again.</span></span> <span data-ttu-id="9ec14-125">Estas funciones truncan los 32 bits superiores de una dirección, que normalmente son necesarios para tener acceso a la memoria a la que se hace referencia originalmente mediante un puntero.</span><span class="sxs-lookup"><span data-stu-id="9ec14-125">These functions truncate the upper 32 bits of an address, which are usually needed to access the memory originally referenced by pointer.</span></span> <span data-ttu-id="9ec14-126">El uso de estas funciones sin mucha consideración dará como resultado código frágil.</span><span class="sxs-lookup"><span data-stu-id="9ec14-126">Using these functions without careful consideration will result in fragile code.</span></span>

3.  <span data-ttu-id="9ec14-127">Tenga cuidado al usar \_ valores de puntero 32 en el código que se puede compilar como código de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9ec14-127">Be careful when using POINTER\_32 values in code that may be compiled as 64-bit code.</span></span> <span data-ttu-id="9ec14-128">El compilador firmará el puntero cuando se asigne a un puntero nativo en el código de 64 bits, no extiende el puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="9ec14-128">The compiler will sign-extend the pointer when it is assigned to a native pointer in 64-bit code, not zero-extend the pointer.</span></span>
4.  <span data-ttu-id="9ec14-129">Tenga cuidado al usar \_ valores de puntero 64 en el código que se puede compilar como código de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9ec14-129">Be careful when using POINTER\_64 values in code that may be compiled as 32-bit code.</span></span> <span data-ttu-id="9ec14-130">El compilador firmará el puntero en el código de 32 bits, no extiende a cero el puntero.</span><span class="sxs-lookup"><span data-stu-id="9ec14-130">The compiler will sign-extend the pointer in 32-bit code, not zero-extend the pointer.</span></span>
5.  <span data-ttu-id="9ec14-131">Tenga cuidado al usar los parámetros OUT.</span><span class="sxs-lookup"><span data-stu-id="9ec14-131">Be careful using OUT parameters.</span></span>

    <span data-ttu-id="9ec14-132">Por ejemplo, supongamos que tiene una función definida de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9ec14-132">For example, suppose you have a function defined as follows:</span></span>

    `void func( OUT PULONG *PointerToUlong );`

    <span data-ttu-id="9ec14-133">No llame a esta función como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9ec14-133">Do not call this function as follows.</span></span>

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    <span data-ttu-id="9ec14-134">En su lugar, utilice la siguiente llamada.</span><span class="sxs-lookup"><span data-stu-id="9ec14-134">Instead, use the following call.</span></span>

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    <span data-ttu-id="9ec14-135">Conversión &UL a **PULONG \*** evita un error del compilador, pero la función escribirá un valor de puntero de 64 bits en la memoria en &UL.</span><span class="sxs-lookup"><span data-stu-id="9ec14-135">Typecasting &ul to **PULONG\*** prevents a compiler error, but the function will write a 64-bit pointer value into the memory at &ul.</span></span> <span data-ttu-id="9ec14-136">Este código funciona en Windows de 32 bits, pero producirá daños en los datos en Windows de 64 bits y será sutil y difícil de encontrar.</span><span class="sxs-lookup"><span data-stu-id="9ec14-136">This code works on 32-bit Windows, but will cause data corruption on 64-bit Windows and it will be subtle, hard-to-find corruption.</span></span> <span data-ttu-id="9ec14-137">La línea inferior: no reproduzca trucos con el código de C: es mejor y sencillo.</span><span class="sxs-lookup"><span data-stu-id="9ec14-137">The bottom line: Do not play tricks with the C code—straightforward and simple is better.</span></span>

6.  <span data-ttu-id="9ec14-138">Tenga cuidado con las interfaces polimórficas.</span><span class="sxs-lookup"><span data-stu-id="9ec14-138">Be careful with polymorphic interfaces.</span></span>

    <span data-ttu-id="9ec14-139">No cree funciones que acepten parámetros **DWORD** para datos polimórficos.</span><span class="sxs-lookup"><span data-stu-id="9ec14-139">Do not create functions that accept **DWORD** parameters for polymorphic data.</span></span> <span data-ttu-id="9ec14-140">Si los datos pueden ser un puntero o un valor entero, use el \_ tipo uint PTR o **PVOID** .</span><span class="sxs-lookup"><span data-stu-id="9ec14-140">If the data can be a pointer or an integral value, use the UINT\_PTR or **PVOID** type.</span></span>

    <span data-ttu-id="9ec14-141">Por ejemplo, no cree una función que acepte una matriz de parámetros de excepción con el tipo de valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="9ec14-141">For example, do not create a function that accepts an array of exception parameters typed as **DWORD** values.</span></span> <span data-ttu-id="9ec14-142">La matriz debe ser una matriz de valores **DWORD \_ ptr** .</span><span class="sxs-lookup"><span data-stu-id="9ec14-142">The array should be an array of **DWORD\_PTR** values.</span></span> <span data-ttu-id="9ec14-143">Por lo tanto, los elementos de la matriz pueden contener direcciones o valores enteros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9ec14-143">Therefore, the array elements can hold addresses or 32-bit integral values.</span></span> <span data-ttu-id="9ec14-144">(La regla general es que si el tipo original es **DWORD** y debe ser el ancho del puntero, conviértalo en un valor de **DWORD \_ ptr** .</span><span class="sxs-lookup"><span data-stu-id="9ec14-144">(The general rule is that if the original type is **DWORD** and it needs to be pointer width, convert it to a **DWORD\_PTR** value.</span></span> <span data-ttu-id="9ec14-145">Esa es la razón por la que hay tipos de precisión de puntero correspondientes). Si tiene código que usa **DWORD**, **ULong** u otros tipos de 32 bits de forma polimórfica (es decir, desea que el parámetro o el miembro de estructura contengan una dirección), use **uint \_ ptr** en lugar del tipo actual.</span><span class="sxs-lookup"><span data-stu-id="9ec14-145">That is why there are corresponding pointer-precision types.) If you have code that uses **DWORD**, **ULONG**, or other 32-bit types in a polymorphic way (that is, you really want the parameter or structure member to hold an address), use **UINT\_PTR** in place of the current type.</span></span>

7.  <span data-ttu-id="9ec14-146">Use las nuevas funciones de clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="9ec14-146">Use the new window class functions.</span></span>

    <span data-ttu-id="9ec14-147">Si tiene datos privados de ventana o clase que contienen punteros, el código deberá usar las siguientes funciones nuevas:</span><span class="sxs-lookup"><span data-stu-id="9ec14-147">If you have window or class private data that contains pointers, your code will need to use the following new functions:</span></span>

    -   [<span data-ttu-id="9ec14-148">**GetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="9ec14-148">**GetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [<span data-ttu-id="9ec14-149">**GetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="9ec14-149">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [<span data-ttu-id="9ec14-150">**SetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="9ec14-150">**SetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [<span data-ttu-id="9ec14-151">**SetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="9ec14-151">**SetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    <span data-ttu-id="9ec14-152">Estas funciones se pueden usar en Windows de 32 y 64 bits, pero son necesarias en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9ec14-152">These functions can be used on both 32- and 64-bit Windows, but they are required on 64-bit Windows.</span></span> <span data-ttu-id="9ec14-153">Prepárese para la transición mediante el uso de estas funciones ahora.</span><span class="sxs-lookup"><span data-stu-id="9ec14-153">Prepare for the transition by using these functions now.</span></span>

    <span data-ttu-id="9ec14-154">Además, debe tener acceso a los punteros o a los identificadores de los datos privados de la clase mediante las nuevas funciones en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9ec14-154">Additionally, you must access pointers or handles in class private data using the new functions on 64-bit Windows.</span></span> <span data-ttu-id="9ec14-155">Para ayudarle a encontrar estos casos, los siguientes índices no se definen en Winuser. h durante una compilación de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="9ec14-155">To aid you in finding these cases, the following indexes are not defined in Winuser.h during a 64-bit compile:</span></span>

    -   <span data-ttu-id="9ec14-156">GWL \_ WndProc</span><span class="sxs-lookup"><span data-stu-id="9ec14-156">GWL\_WNDPROC</span></span>
    -   <span data-ttu-id="9ec14-157">GWL \_ hInstance</span><span class="sxs-lookup"><span data-stu-id="9ec14-157">GWL\_HINSTANCE</span></span>
    -   <span data-ttu-id="9ec14-158">GWL \_ HWDPARENT</span><span class="sxs-lookup"><span data-stu-id="9ec14-158">GWL\_HWDPARENT</span></span>
    -   <span data-ttu-id="9ec14-159">GWL \_ USERDATA</span><span class="sxs-lookup"><span data-stu-id="9ec14-159">GWL\_USERDATA</span></span>

    <span data-ttu-id="9ec14-160">En su lugar, Winuser. h define los nuevos índices siguientes:</span><span class="sxs-lookup"><span data-stu-id="9ec14-160">Instead, Winuser.h defines the following new indexes:</span></span>

    -   <span data-ttu-id="9ec14-161">GWLP \_ WndProc</span><span class="sxs-lookup"><span data-stu-id="9ec14-161">GWLP\_WNDPROC</span></span>
    -   <span data-ttu-id="9ec14-162">GWLP \_ hInstance</span><span class="sxs-lookup"><span data-stu-id="9ec14-162">GWLP\_HINSTANCE</span></span>
    -   <span data-ttu-id="9ec14-163">GWLP \_ HWNDPARENT</span><span class="sxs-lookup"><span data-stu-id="9ec14-163">GWLP\_HWNDPARENT</span></span>
    -   <span data-ttu-id="9ec14-164">GWLP \_ USERDATA</span><span class="sxs-lookup"><span data-stu-id="9ec14-164">GWLP\_USERDATA</span></span>
    -   <span data-ttu-id="9ec14-165">identificador de GWLP \_</span><span class="sxs-lookup"><span data-stu-id="9ec14-165">GWLP\_ID</span></span>

    <span data-ttu-id="9ec14-166">Por ejemplo, el código siguiente no se compila:</span><span class="sxs-lookup"><span data-stu-id="9ec14-166">For example, the following code does not compile:</span></span>

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    <span data-ttu-id="9ec14-167">Debe cambiarse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9ec14-167">It should be changed as follows:</span></span>

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    <span data-ttu-id="9ec14-168">Al establecer el miembro **cbWndExtra** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) , asegúrese de reservar espacio suficiente para los punteros.</span><span class="sxs-lookup"><span data-stu-id="9ec14-168">When setting the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure, be sure to reserve enough space for pointers.</span></span> <span data-ttu-id="9ec14-169">Por ejemplo, si está reservando bytes de tamaño (DWORD) para un valor de puntero, Reserve bytes de tamaño (DWORD \_ ptr).</span><span class="sxs-lookup"><span data-stu-id="9ec14-169">For example, if you are currently reserving sizeof(DWORD) bytes for a pointer value, reserve sizeof(DWORD\_PTR) bytes.</span></span>

8.  <span data-ttu-id="9ec14-170">Acceder a todos los datos de ventana y de clase mediante el **\_ desplazamiento de campo**.</span><span class="sxs-lookup"><span data-stu-id="9ec14-170">Access all window and class data using **FIELD\_OFFSET**.</span></span>

    <span data-ttu-id="9ec14-171">Es habitual tener acceso a los datos de la ventana mediante desplazamientos codificados de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="9ec14-171">It is common to access window data using hard-coded offsets.</span></span> <span data-ttu-id="9ec14-172">Esta técnica no es portable a Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9ec14-172">This technique is not portable to 64-bit Windows.</span></span> <span data-ttu-id="9ec14-173">Para que el código sea portátil, acceda a los datos de la ventana y de la clase mediante la macro de **\_ desplazamiento de campo** .</span><span class="sxs-lookup"><span data-stu-id="9ec14-173">To make your code portable, access your window and class data using the **FIELD\_OFFSET** macro.</span></span> <span data-ttu-id="9ec14-174">No asuma que el segundo puntero tiene un desplazamiento de 4.</span><span class="sxs-lookup"><span data-stu-id="9ec14-174">Do not assume that the second pointer has an offset of 4.</span></span>

9.  <span data-ttu-id="9ec14-175">Los tipos **lParam**, **wParam** y **LRESULT** cambian el tamaño con la plataforma.</span><span class="sxs-lookup"><span data-stu-id="9ec14-175">The **LPARAM**, **WPARAM**, and **LRESULT** types change size with the platform.</span></span>

    <span data-ttu-id="9ec14-176">Al compilar código de 64 bits, estos tipos se expanden hasta 64 bits, porque normalmente contienen punteros o tipos enteros.</span><span class="sxs-lookup"><span data-stu-id="9ec14-176">When compiling 64-bit code, these types expand to 64 bits, because they typically hold pointers or integral types.</span></span> <span data-ttu-id="9ec14-177">No mezcle estos valores con los valores **DWORD**, **ULong**, **uint**, **int**, **int** o **Long** .</span><span class="sxs-lookup"><span data-stu-id="9ec14-177">Do not mix these values with **DWORD**, **ULONG**, **UINT**, **INT**, **int**, or **long** values.</span></span> <span data-ttu-id="9ec14-178">Examine cómo se usan estos tipos y asegúrese de que no trunca accidentalmente los valores.</span><span class="sxs-lookup"><span data-stu-id="9ec14-178">Examine how you use these types and ensure that you do not inadvertently truncate values.</span></span>

 

 