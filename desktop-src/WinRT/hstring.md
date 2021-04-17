---
description: Identificador de una cadena de Windows Runtime.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9e73d7627a4bab8f02a95056e5b208569d922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686780"
---
# <a name="hstring"></a><span data-ttu-id="d7887-103">HSTRING</span><span class="sxs-lookup"><span data-stu-id="d7887-103">HSTRING</span></span>

<span data-ttu-id="d7887-104">Identificador de una cadena de Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="d7887-104">A handle to a Windows Runtime string.</span></span>


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a><span data-ttu-id="d7887-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7887-105">Remarks</span></span>

<span data-ttu-id="d7887-106">Use **HSTRING** para representar cadenas inmutables en el Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="d7887-106">Use **HSTRING** to represent immutable strings in the Windows Runtime.</span></span>

<span data-ttu-id="d7887-107">JavaScript y otros lenguajes, como C \# y Microsoft Visual Basic, pueden usar cadenas que se representan mediante **HSTRING**.</span><span class="sxs-lookup"><span data-stu-id="d7887-107">JavaScript and other languages, such as C\#, and Microsoft Visual Basic, can use strings that are represented by using **HSTRING**.</span></span> <span data-ttu-id="d7887-108">En la tabla siguiente se muestra cómo se representa un **HSTRING** en otros lenguajes.</span><span class="sxs-lookup"><span data-stu-id="d7887-108">The following table shows how an **HSTRING** is represented in other languages.</span></span>



| <span data-ttu-id="d7887-109">Lenguaje de programación</span><span class="sxs-lookup"><span data-stu-id="d7887-109">Programming Language</span></span>                                                                    | <span data-ttu-id="d7887-110">Representación de cadena</span><span class="sxs-lookup"><span data-stu-id="d7887-110">String Representation</span></span>                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="d7887-111">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="d7887-111">C++/WinRT</span></span>](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | <span data-ttu-id="d7887-112">[winrt:: hstring](/uwp/cpp-ref-for-winrt/hstring) (clase)</span><span class="sxs-lookup"><span data-stu-id="d7887-112">[winrt::hstring](/uwp/cpp-ref-for-winrt/hstring) class</span></span>     |
| <span data-ttu-id="d7887-113">Extensiones de componentes Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span><span class="sxs-lookup"><span data-stu-id="d7887-113">Visual C++ component extensions ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span></span> | <span data-ttu-id="d7887-114">[Platform:: String](/cpp/cppcx/platform-string-class) (clase)</span><span class="sxs-lookup"><span data-stu-id="d7887-114">[Platform::String](/cpp/cppcx/platform-string-class) class</span></span> |
| <span data-ttu-id="d7887-115">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d7887-115">JavaScript</span></span>                                                                              | <span data-ttu-id="d7887-116">objeto de cadena</span><span class="sxs-lookup"><span data-stu-id="d7887-116">String object</span></span>                                              |
| <span data-ttu-id="d7887-117">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="d7887-117">.NET Framework</span></span>                                                                          | <span data-ttu-id="d7887-118">clase System.String</span><span class="sxs-lookup"><span data-stu-id="d7887-118">System.String class</span></span>                                        |



 

<span data-ttu-id="d7887-119">El identificador de **HSTRING** es un tipo de identificador estándar.</span><span class="sxs-lookup"><span data-stu-id="d7887-119">The **HSTRING** handle is a standard handle type.</span></span> <span data-ttu-id="d7887-120">Semánticamente, un **HSTRING** que contiene el valor **null** representa la cadena vacía, que consta de cero caracteres de contenido y un carácter **nulo** de terminación.</span><span class="sxs-lookup"><span data-stu-id="d7887-120">Semantically, an **HSTRING** containing the value **NULL** represents the empty string, which consists of zero content characters and a terminating **NULL** character.</span></span> <span data-ttu-id="d7887-121">Al crear una cadena a través de [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) con cero caracteres, se generará el valor **null** del identificador.</span><span class="sxs-lookup"><span data-stu-id="d7887-121">Creating a string via [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) with zero characters will produce the handle value **NULL**.</span></span> <span data-ttu-id="d7887-122">Al llamar a [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) con el valor **null**, se devolverá un puntero a una cadena vacía seguida solo por el carácter de terminación **NUL** .</span><span class="sxs-lookup"><span data-stu-id="d7887-122">When calling [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) with the value **NULL**, a pointer to an empty string followed only by the **NUL** terminating character will be returned.</span></span> <span data-ttu-id="d7887-123">No existe ningún valor distinto para representar un **HSTRING** que no está inicializado.</span><span class="sxs-lookup"><span data-stu-id="d7887-123">No distinct value exists to represent an **HSTRING** that is uninitialized.</span></span>

<span data-ttu-id="d7887-124">Llame a la función [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) para crear un nuevo **HSTRING** y llame a la función [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) para liberar la referencia a la memoria de la cadena de respaldo.</span><span class="sxs-lookup"><span data-stu-id="d7887-124">Call the [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) function to create a new **HSTRING**, and call the [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) function to release the reference to the backing string memory.</span></span> <span data-ttu-id="d7887-125">Llame a la función [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) para crear una referencia de cadena, que también se denomina *cadena de paso rápido*.</span><span class="sxs-lookup"><span data-stu-id="d7887-125">Call the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function to create a string reference, which is also called a *fast-pass string*.</span></span>

<span data-ttu-id="d7887-126">Copie un **HSTRING** mediante una llamada a la función [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) .</span><span class="sxs-lookup"><span data-stu-id="d7887-126">Copy an **HSTRING** by calling the [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) function.</span></span>

<span data-ttu-id="d7887-127">Concatene dos cadenas mediante una llamada a la función [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) .</span><span class="sxs-lookup"><span data-stu-id="d7887-127">Concatenate two strings by calling the [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) function.</span></span>

<span data-ttu-id="d7887-128">Obtenga acceso a la memoria de la cadena de respaldo llamando a la función [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) .</span><span class="sxs-lookup"><span data-stu-id="d7887-128">Access the backing string memory by calling the [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) function.</span></span>

<span data-ttu-id="d7887-129">**HSTRING** puede almacenar y usar caracteres **null** incrustados.</span><span class="sxs-lookup"><span data-stu-id="d7887-129">**HSTRING** can store and use embedded **NUL** characters.</span></span> <span data-ttu-id="d7887-130">Utilice la función [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) para comprobar los caracteres **null** incrustados antes de usar las funciones que pueden producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="d7887-130">Use the [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) function to check for embedded **NUL** characters before using any functions which may produce unexpected results.</span></span> <span data-ttu-id="d7887-131">Por ejemplo, la mayoría de las funciones de Windows usan **LPCWSTR** como parámetro de entrada y calculan la longitud de la cadena solo hasta que se encuentra el primer **NUL** .</span><span class="sxs-lookup"><span data-stu-id="d7887-131">For example, most of the Windows functions use **LPCWSTR** as an input parameter, and they compute the length of the string only until the first **NUL** is encountered.</span></span>

<span data-ttu-id="d7887-132">La cadena de respaldo debe permanecer inmutable y terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="d7887-132">The backing string must remain immutable and null-terminated.</span></span> <span data-ttu-id="d7887-133">Cuando el código de llamada crea una referencia de cadena mediante la función [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , el autor de la llamada es el propietario de la memoria que contiene la representación de la cadena de respaldo.</span><span class="sxs-lookup"><span data-stu-id="d7887-133">When calling code creates a string reference by using the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function, the memory containing the backing string representation is owned by the caller.</span></span> <span data-ttu-id="d7887-134">El Windows Runtime se basa en el contenido de la cadena original para permanecer sin cambios.</span><span class="sxs-lookup"><span data-stu-id="d7887-134">The Windows Runtime relies on the contents of the original string to remain unchanged.</span></span> <span data-ttu-id="d7887-135">Al pasar una referencia de cadena en el Windows Runtime, es responsabilidad del autor de la llamada asegurarse de que el contenido de la cadena no cambia y **NUL** se termina mientras dure la llamada.</span><span class="sxs-lookup"><span data-stu-id="d7887-135">When passing a string reference into the Windows Runtime, it is the caller’s responsibility to ensure that the string’s contents are unchanging and **NUL** terminated for the duration of the call.</span></span> <span data-ttu-id="d7887-136">El Windows Runtime libera todas las referencias a la referencia de cadena cuando se devuelve la llamada.</span><span class="sxs-lookup"><span data-stu-id="d7887-136">The Windows Runtime releases all references to the string reference when the call returns.</span></span>

<span data-ttu-id="d7887-137">Cuando reciba un **HSTRING** como parámetro de salida, se recomienda establecer el identificador en **null** cuando termine de usarlo.</span><span class="sxs-lookup"><span data-stu-id="d7887-137">When you receive an **HSTRING** as an out parameter, it is good practice to set the handle to **NULL** when you are finished with it.</span></span>

<span data-ttu-id="d7887-138">Llame a la función [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para asignar un búfer de cadena mutable que puede usar para crear un **HSTRING** inmutable.</span><span class="sxs-lookup"><span data-stu-id="d7887-138">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to allocate a mutable string buffer that you can use to create an immutable **HSTRING**.</span></span> <span data-ttu-id="d7887-139">Cuando haya terminado de rellenar el búfer, llame a la función [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) para crear el **HSTRING**.</span><span class="sxs-lookup"><span data-stu-id="d7887-139">When you have finished populating the buffer, you call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) function to create the **HSTRING**.</span></span> <span data-ttu-id="d7887-140">Este patrón de construcción en dos fases habilita una funcionalidad similar a un "generador de cadenas".</span><span class="sxs-lookup"><span data-stu-id="d7887-140">This two-phase construction pattern enables functionality that is similar to a "string builder."</span></span>

## <a name="requirements"></a><span data-ttu-id="d7887-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7887-141">Requirements</span></span>



| <span data-ttu-id="d7887-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7887-142">Requirement</span></span> | <span data-ttu-id="d7887-143">Value</span><span class="sxs-lookup"><span data-stu-id="d7887-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d7887-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7887-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d7887-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d7887-145">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="d7887-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7887-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d7887-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d7887-147">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="d7887-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7887-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7887-149"><dt>Hstring. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7887-149"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7887-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7887-150">See also</span></span>

<dl> <span data-ttu-id="d7887-151"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="d7887-151"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="d7887-152">**WindowsCreateString**</span><span class="sxs-lookup"><span data-stu-id="d7887-152">**WindowsCreateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[<span data-ttu-id="d7887-153">**WindowsDeleteString**</span><span class="sxs-lookup"><span data-stu-id="d7887-153">**WindowsDeleteString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[<span data-ttu-id="d7887-154">**WindowsDuplicateString**</span><span class="sxs-lookup"><span data-stu-id="d7887-154">**WindowsDuplicateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[<span data-ttu-id="d7887-155">**WindowsPreallocateStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="d7887-155">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
