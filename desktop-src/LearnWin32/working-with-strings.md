---
title: Trabajo con cadenas
description: Trabajo con cadenas
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4661c6b07a267d90e0fca05d04354c018be04527
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110973"
---
# <a name="working-with-strings"></a><span data-ttu-id="2747d-103">Trabajo con cadenas</span><span class="sxs-lookup"><span data-stu-id="2747d-103">Working with Strings</span></span>

<span data-ttu-id="2747d-104">Windows admite de forma nativa cadenas Unicode para elementos de interfaz de usuario, nombres de archivo, etc.</span><span class="sxs-lookup"><span data-stu-id="2747d-104">Windows natively supports Unicode strings for UI elements, file names, and so forth.</span></span> <span data-ttu-id="2747d-105">Unicode es la codificación de caracteres preferida, ya que admite todos los idiomas y conjuntos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2747d-105">Unicode is the preferred character encoding, because it supports all character sets and languages.</span></span> <span data-ttu-id="2747d-106">Windows representa caracteres Unicode mediante la codificación UTF-16, en la que cada carácter se codifica como un valor de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2747d-106">Windows represents Unicode characters using UTF-16 encoding, in which each character is encoded as a 16-bit value.</span></span> <span data-ttu-id="2747d-107">Los caracteres UTF-16 se *denominan caracteres anchos,* para distinguirlos de los caracteres ANSI de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="2747d-107">UTF-16 characters are called *wide* characters, to distinguish them from 8-bit ANSI characters.</span></span> <span data-ttu-id="2747d-108">El Visual C++ admite el tipo de datos **integrado wchar \_ t para** caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="2747d-108">The Visual C++ compiler supports the built-in data type **wchar\_t** for wide characters.</span></span> <span data-ttu-id="2747d-109">El archivo de encabezado WinNT.h también define la definición **de tipo siguiente.**</span><span class="sxs-lookup"><span data-stu-id="2747d-109">The header file WinNT.h also defines the following **typedef**.</span></span>


```C++
typedef wchar_t WCHAR;
```



<span data-ttu-id="2747d-110">Verá ambas versiones en código de ejemplo de MSDN.</span><span class="sxs-lookup"><span data-stu-id="2747d-110">You will see both versions in MSDN example code.</span></span> <span data-ttu-id="2747d-111">Para declarar un literal de caracteres anchos o un literal de cadena de caracteres anchos, coloque **L** delante del literal.</span><span class="sxs-lookup"><span data-stu-id="2747d-111">To declare a wide-character literal or a wide-character string literal, put **L** before the literal.</span></span>


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



<span data-ttu-id="2747d-112">Estas son algunas otras definiciones de tipos relacionadas con cadenas que verá:</span><span class="sxs-lookup"><span data-stu-id="2747d-112">Here are some other string-related typedefs that you will see:</span></span>



| <span data-ttu-id="2747d-113">Definición de tipo</span><span class="sxs-lookup"><span data-stu-id="2747d-113">Typedef</span></span>                   | <span data-ttu-id="2747d-114">Definición</span><span class="sxs-lookup"><span data-stu-id="2747d-114">Definition</span></span>       |
|---------------------------|------------------|
| <span data-ttu-id="2747d-115">**CHAR**</span><span class="sxs-lookup"><span data-stu-id="2747d-115">**CHAR**</span></span>                  | `char`           |
| <span data-ttu-id="2747d-116">**PSTR** o **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="2747d-116">**PSTR** or **LPSTR**</span></span>     | `char*`          |
| <span data-ttu-id="2747d-117">**PCSTR** o **LPCSTR**</span><span class="sxs-lookup"><span data-stu-id="2747d-117">**PCSTR** or **LPCSTR**</span></span>   | `const char*`    |
| <span data-ttu-id="2747d-118">**PWSTR** o **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2747d-118">**PWSTR** or **LPWSTR**</span></span>   | `wchar_t*`       |
| <span data-ttu-id="2747d-119">**PCWSTR** o **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="2747d-119">**PCWSTR** or **LPCWSTR**</span></span> | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a><span data-ttu-id="2747d-120">Funciones Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="2747d-120">Unicode and ANSI Functions</span></span>

<span data-ttu-id="2747d-121">Cuando Microsoft introdujo la compatibilidad con Unicode en Windows, se facilitaba la transición proporcionando dos conjuntos paralelos de API, uno para cadenas ANSI y otro para cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="2747d-121">When Microsoft introduced Unicode support to Windows, it eased the transition by providing two parallel sets of APIs, one for ANSI strings and the other for Unicode strings.</span></span> <span data-ttu-id="2747d-122">Por ejemplo, hay dos funciones para establecer el texto de la barra de título de una ventana:</span><span class="sxs-lookup"><span data-stu-id="2747d-122">For example, there are two functions to set the text of a window's title bar:</span></span>

-   <span data-ttu-id="2747d-123">**SetWindowTextA toma** una cadena ANSI.</span><span class="sxs-lookup"><span data-stu-id="2747d-123">**SetWindowTextA** takes an ANSI string.</span></span>
-   <span data-ttu-id="2747d-124">**SetWindowTextW toma** una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="2747d-124">**SetWindowTextW** takes a Unicode string.</span></span>

<span data-ttu-id="2747d-125">Internamente, la versión ANSI traduce la cadena a Unicode.</span><span class="sxs-lookup"><span data-stu-id="2747d-125">Internally, the ANSI version translates the string to Unicode.</span></span> <span data-ttu-id="2747d-126">Los encabezados de Windows también definen una macro que se resuelve en la versión Unicode cuando se define el símbolo de preprocesador o la versión ANSI en caso `UNICODE` contrario.</span><span class="sxs-lookup"><span data-stu-id="2747d-126">The Windows headers also define a macro that resolves to the Unicode version when the preprocessor symbol `UNICODE` is defined or the ANSI version otherwise.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



<span data-ttu-id="2747d-127">En MSDN, la función se documenta con el nombre [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), aunque ese es realmente el nombre de la macro, no el nombre real de la función.</span><span class="sxs-lookup"><span data-stu-id="2747d-127">In MSDN, the function is documented under the name [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), even though that is really the macro name, not the actual function name.</span></span>

<span data-ttu-id="2747d-128">Las nuevas aplicaciones siempre deben llamar a las versiones Unicode.</span><span class="sxs-lookup"><span data-stu-id="2747d-128">New applications should always call the Unicode versions.</span></span> <span data-ttu-id="2747d-129">Muchos idiomas del mundo requieren Unicode.</span><span class="sxs-lookup"><span data-stu-id="2747d-129">Many world languages require Unicode.</span></span> <span data-ttu-id="2747d-130">Si usa cadenas ANSI, será imposible encontrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2747d-130">If you use ANSI strings, it will be impossible to localize your application.</span></span> <span data-ttu-id="2747d-131">Las versiones ANSI también son menos eficaces, ya que el sistema operativo debe convertir las cadenas ANSI a Unicode en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2747d-131">The ANSI versions are also less efficient, because the operating system must convert the ANSI strings to Unicode at run time.</span></span> <span data-ttu-id="2747d-132">Según sus preferencias, puede llamar explícitamente a las funciones Unicode, como **SetWindowTextW,** o usar las macros .</span><span class="sxs-lookup"><span data-stu-id="2747d-132">Depending on your preference, you can call the Unicode functions explicitly, such as **SetWindowTextW**, or use the macros.</span></span> <span data-ttu-id="2747d-133">El código de ejemplo de MSDN normalmente llama a las macros, pero las dos formas son exactamente equivalentes.</span><span class="sxs-lookup"><span data-stu-id="2747d-133">The example code on MSDN typically calls the macros, but the two forms are exactly equivalent.</span></span> <span data-ttu-id="2747d-134">La mayoría de las API más recientes de Windows solo tienen una versión Unicode, sin la versión ANSI correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2747d-134">Most newer APIs in Windows have just a Unicode version, with no corresponding ANSI version.</span></span>

## <a name="tchars"></a><span data-ttu-id="2747d-135">TCHAR</span><span class="sxs-lookup"><span data-stu-id="2747d-135">TCHARs</span></span>

<span data-ttu-id="2747d-136">Cuando las aplicaciones necesitaban admitir Windows NT, así como Windows 95, Windows 98 y Windows Me, resultaba útil compilar el mismo código para cadenas ANSI o Unicode, en función de la plataforma de destino.</span><span class="sxs-lookup"><span data-stu-id="2747d-136">Back when applications needed to support both Windows NT as well as Windows 95, Windows 98, and Windows Me, it was useful to compile the same code for either ANSI or Unicode strings, depending on the target platform.</span></span> <span data-ttu-id="2747d-137">Con este fin, el Windows SDK proporciona macros que asignan cadenas a Unicode o ANSI, en función de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="2747d-137">To this end, the Windows SDK provides macros that map strings to Unicode or ANSI, depending on the platform.</span></span>



| <span data-ttu-id="2747d-138">Macro</span><span class="sxs-lookup"><span data-stu-id="2747d-138">Macro</span></span>     | <span data-ttu-id="2747d-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="2747d-139">Unicode</span></span>   | <span data-ttu-id="2747d-140">ANSI</span><span class="sxs-lookup"><span data-stu-id="2747d-140">ANSI</span></span>   |
|-----------|-----------|--------|
| <span data-ttu-id="2747d-141">TCHAR</span><span class="sxs-lookup"><span data-stu-id="2747d-141">TCHAR</span></span>     | `wchar_t` | `char` |
| <span data-ttu-id="2747d-142">TEXT("x")</span><span class="sxs-lookup"><span data-stu-id="2747d-142">TEXT("x")</span></span> | `L"x"`    | `"x"`  |



 

<span data-ttu-id="2747d-143">Por ejemplo, el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="2747d-143">For example, the following code:</span></span>


```C++
SetWindowText(TEXT("My Application"));
```



<span data-ttu-id="2747d-144">se resuelve en uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2747d-144">resolves to one of the following:</span></span>


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



<span data-ttu-id="2747d-145">Las **macros TEXT** y **TCHAR** son menos útiles hoy en día, porque todas las aplicaciones deben usar Unicode.</span><span class="sxs-lookup"><span data-stu-id="2747d-145">The **TEXT** and **TCHAR** macros are less useful today, because all applications should use Unicode.</span></span> <span data-ttu-id="2747d-146">Sin embargo, es posible que los vea en código anterior y en algunos de los ejemplos de código de MSDN.</span><span class="sxs-lookup"><span data-stu-id="2747d-146">However, you might see them in older code and in some of the MSDN code examples.</span></span>

<span data-ttu-id="2747d-147">Los encabezados de las bibliotecas en tiempo de ejecución de Microsoft C definen un conjunto similar de macros.</span><span class="sxs-lookup"><span data-stu-id="2747d-147">The headers for the Microsoft C run-time libraries define a similar set of macros.</span></span> <span data-ttu-id="2747d-148">Por ejemplo, **\_ tcslen** se resuelve como **strlen** si no está definido; de lo contrario, se resuelve como wcslen , que es la versión de caracteres `_UNICODE` anchos **de strlen**. </span><span class="sxs-lookup"><span data-stu-id="2747d-148">For example, **\_tcslen** resolves to **strlen** if `_UNICODE` is undefined; otherwise it resolves to **wcslen**, which is the wide-character version of **strlen**.</span></span>


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



<span data-ttu-id="2747d-149">Tenga cuidado: algunos encabezados usan el símbolo de preprocesador `UNICODE` y otros usan con un prefijo de `_UNICODE` subrayado.</span><span class="sxs-lookup"><span data-stu-id="2747d-149">Be careful: Some headers use the preprocessor symbol `UNICODE`, others use `_UNICODE` with an underscore prefix.</span></span> <span data-ttu-id="2747d-150">Defina siempre ambos símbolos.</span><span class="sxs-lookup"><span data-stu-id="2747d-150">Always define both symbols.</span></span> <span data-ttu-id="2747d-151">Visual C++ establece ambos de forma predeterminada al crear un proyecto.</span><span class="sxs-lookup"><span data-stu-id="2747d-151">Visual C++ sets them both by default when you create a new project.</span></span>

## <a name="next"></a><span data-ttu-id="2747d-152">Siguientes</span><span class="sxs-lookup"><span data-stu-id="2747d-152">Next</span></span>

[<span data-ttu-id="2747d-153">¿Qué es una ventana?</span><span class="sxs-lookup"><span data-stu-id="2747d-153">What Is a Window?</span></span>](what-is-a-window-.md)

 

 
