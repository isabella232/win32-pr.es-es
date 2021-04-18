---
title: Trabajo con cadenas
description: .
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c74530a1acd0eb94f0d88662924203a8c58116
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149228"
---
# <a name="working-with-strings"></a><span data-ttu-id="099d5-103">Trabajo con cadenas</span><span class="sxs-lookup"><span data-stu-id="099d5-103">Working with Strings</span></span>

<span data-ttu-id="099d5-104">Windows admite de forma nativa cadenas Unicode para elementos de interfaz de usuario, nombres de archivo, etc.</span><span class="sxs-lookup"><span data-stu-id="099d5-104">Windows natively supports Unicode strings for UI elements, file names, and so forth.</span></span> <span data-ttu-id="099d5-105">Unicode es la codificación de caracteres preferida, ya que admite todos los juegos de caracteres e idiomas.</span><span class="sxs-lookup"><span data-stu-id="099d5-105">Unicode is the preferred character encoding, because it supports all character sets and languages.</span></span> <span data-ttu-id="099d5-106">Windows representa caracteres Unicode mediante la codificación UTF-16, en la que cada carácter se codifica como un valor de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="099d5-106">Windows represents Unicode characters using UTF-16 encoding, in which each character is encoded as a 16-bit value.</span></span> <span data-ttu-id="099d5-107">Los caracteres UTF-16 se denominan caracteres *anchos* para distinguirlos de caracteres ANSI de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="099d5-107">UTF-16 characters are called *wide* characters, to distinguish them from 8-bit ANSI characters.</span></span> <span data-ttu-id="099d5-108">El compilador Visual C++ admite el tipo de datos integrado **WCHAR \_ t** para caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="099d5-108">The Visual C++ compiler supports the built-in data type **wchar\_t** for wide characters.</span></span> <span data-ttu-id="099d5-109">El archivo de encabezado Winnt. h también define el siguiente **typedef**.</span><span class="sxs-lookup"><span data-stu-id="099d5-109">The header file WinNT.h also defines the following **typedef**.</span></span>


```C++
typedef wchar_t WCHAR;
```



<span data-ttu-id="099d5-110">Verá ambas versiones en el código de ejemplo de MSDN.</span><span class="sxs-lookup"><span data-stu-id="099d5-110">You will see both versions in MSDN example code.</span></span> <span data-ttu-id="099d5-111">Para declarar un literal de carácter ancho o un literal de cadena de caracteres anchos, coloque **L** delante del literal.</span><span class="sxs-lookup"><span data-stu-id="099d5-111">To declare a wide-character literal or a wide-character string literal, put **L** before the literal.</span></span>


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



<span data-ttu-id="099d5-112">Estas son algunas de las definiciones de tipo relacionadas con cadenas que verá:</span><span class="sxs-lookup"><span data-stu-id="099d5-112">Here are some other string-related typedefs that you will see:</span></span>



| <span data-ttu-id="099d5-113">Definición de tipo</span><span class="sxs-lookup"><span data-stu-id="099d5-113">Typedef</span></span>                   | <span data-ttu-id="099d5-114">Definición</span><span class="sxs-lookup"><span data-stu-id="099d5-114">Definition</span></span>       |
|---------------------------|------------------|
| <span data-ttu-id="099d5-115">**CHAR**</span><span class="sxs-lookup"><span data-stu-id="099d5-115">**CHAR**</span></span>                  | `char`           |
| <span data-ttu-id="099d5-116">**PSTR** o **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="099d5-116">**PSTR** or **LPSTR**</span></span>     | `char*`          |
| <span data-ttu-id="099d5-117">**PCSTR** o **LPCSTR**</span><span class="sxs-lookup"><span data-stu-id="099d5-117">**PCSTR** or **LPCSTR**</span></span>   | `const char*`    |
| <span data-ttu-id="099d5-118">**PWSTR** o **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="099d5-118">**PWSTR** or **LPWSTR**</span></span>   | `wchar_t*`       |
| <span data-ttu-id="099d5-119">**PCWSTR** o **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="099d5-119">**PCWSTR** or **LPCWSTR**</span></span> | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a><span data-ttu-id="099d5-120">Funciones Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="099d5-120">Unicode and ANSI Functions</span></span>

<span data-ttu-id="099d5-121">Cuando Microsoft presentó la compatibilidad con Unicode en Windows, facilitó la transición proporcionando dos conjuntos paralelos de API: uno para las cadenas ANSI y el otro para las cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="099d5-121">When Microsoft introduced Unicode support to Windows, it eased the transition by providing two parallel sets of APIs, one for ANSI strings and the other for Unicode strings.</span></span> <span data-ttu-id="099d5-122">Por ejemplo, hay dos funciones para establecer el texto de la barra de título de una ventana:</span><span class="sxs-lookup"><span data-stu-id="099d5-122">For example, there are two functions to set the text of a window's title bar:</span></span>

-   <span data-ttu-id="099d5-123">**SetWindowTextA** toma una cadena ANSI.</span><span class="sxs-lookup"><span data-stu-id="099d5-123">**SetWindowTextA** takes an ANSI string.</span></span>
-   <span data-ttu-id="099d5-124">**SetWindowTextW** toma una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="099d5-124">**SetWindowTextW** takes a Unicode string.</span></span>

<span data-ttu-id="099d5-125">Internamente, la versión ANSI traduce la cadena a Unicode.</span><span class="sxs-lookup"><span data-stu-id="099d5-125">Internally, the ANSI version translates the string to Unicode.</span></span> <span data-ttu-id="099d5-126">Los encabezados de Windows también definen una macro que se resuelve en la versión Unicode cuando se define el símbolo de preprocesador `UNICODE` o la versión ANSI, en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="099d5-126">The Windows headers also define a macro that resolves to the Unicode version when the preprocessor symbol `UNICODE` is defined or the ANSI version otherwise.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



<span data-ttu-id="099d5-127">En MSDN, la función se documenta con el nombre [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), aunque es en realidad el nombre de la macro, no el nombre de función real.</span><span class="sxs-lookup"><span data-stu-id="099d5-127">In MSDN, the function is documented under the name [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), even though that is really the macro name, not the actual function name.</span></span>

<span data-ttu-id="099d5-128">Las aplicaciones nuevas siempre deben llamar a las versiones Unicode.</span><span class="sxs-lookup"><span data-stu-id="099d5-128">New applications should always call the Unicode versions.</span></span> <span data-ttu-id="099d5-129">Muchos idiomas internacionales requieren Unicode.</span><span class="sxs-lookup"><span data-stu-id="099d5-129">Many world languages require Unicode.</span></span> <span data-ttu-id="099d5-130">Si usa cadenas ANSI, no será posible localizar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="099d5-130">If you use ANSI strings, it will be impossible to localize your application.</span></span> <span data-ttu-id="099d5-131">Las versiones ANSI también son menos eficaces, ya que el sistema operativo debe convertir las cadenas ANSI en Unicode en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="099d5-131">The ANSI versions are also less efficient, because the operating system must convert the ANSI strings to Unicode at run time.</span></span> <span data-ttu-id="099d5-132">En función de sus preferencias, puede llamar a las funciones Unicode explícitamente, como **SetWindowTextW**, o usar las macros.</span><span class="sxs-lookup"><span data-stu-id="099d5-132">Depending on your preference, you can call the Unicode functions explicitly, such as **SetWindowTextW**, or use the macros.</span></span> <span data-ttu-id="099d5-133">El código de ejemplo de MSDN normalmente llama a las macros, pero las dos formas son exactamente equivalentes.</span><span class="sxs-lookup"><span data-stu-id="099d5-133">The example code on MSDN typically calls the macros, but the two forms are exactly equivalent.</span></span> <span data-ttu-id="099d5-134">La mayoría de las API más recientes de Windows tienen solo una versión Unicode, sin ninguna versión ANSI correspondiente.</span><span class="sxs-lookup"><span data-stu-id="099d5-134">Most newer APIs in Windows have just a Unicode version, with no corresponding ANSI version.</span></span>

## <a name="tchars"></a><span data-ttu-id="099d5-135">TCHARs</span><span class="sxs-lookup"><span data-stu-id="099d5-135">TCHARs</span></span>

<span data-ttu-id="099d5-136">De vuelta cuando las aplicaciones necesarias para admitir tanto Windows NT como Windows 95, Windows 98 y Windows me, resultaba útil compilar el mismo código para cadenas ANSI o Unicode, en función de la plataforma de destino.</span><span class="sxs-lookup"><span data-stu-id="099d5-136">Back when applications needed to support both Windows NT as well as Windows 95, Windows 98, and Windows Me, it was useful to compile the same code for either ANSI or Unicode strings, depending on the target platform.</span></span> <span data-ttu-id="099d5-137">Para este fin, el Windows SDK proporciona macros que asignan cadenas a Unicode o ANSI, dependiendo de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="099d5-137">To this end, the Windows SDK provides macros that map strings to Unicode or ANSI, depending on the platform.</span></span>



| <span data-ttu-id="099d5-138">Macro</span><span class="sxs-lookup"><span data-stu-id="099d5-138">Macro</span></span>     | <span data-ttu-id="099d5-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="099d5-139">Unicode</span></span>   | <span data-ttu-id="099d5-140">ANSI</span><span class="sxs-lookup"><span data-stu-id="099d5-140">ANSI</span></span>   |
|-----------|-----------|--------|
| <span data-ttu-id="099d5-141">TCHAR</span><span class="sxs-lookup"><span data-stu-id="099d5-141">TCHAR</span></span>     | `wchar_t` | `char` |
| <span data-ttu-id="099d5-142">TEXTO ("x")</span><span class="sxs-lookup"><span data-stu-id="099d5-142">TEXT("x")</span></span> | `L"x"`    | `"x"`  |



 

<span data-ttu-id="099d5-143">Por ejemplo, el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="099d5-143">For example, the following code:</span></span>


```C++
SetWindowText(TEXT("My Application"));
```



<span data-ttu-id="099d5-144">se resuelve como uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="099d5-144">resolves to one of the following:</span></span>


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



<span data-ttu-id="099d5-145">Las macros **Text** y **TCHAR** son menos útiles hoy en día, ya que todas las aplicaciones deben usar Unicode.</span><span class="sxs-lookup"><span data-stu-id="099d5-145">The **TEXT** and **TCHAR** macros are less useful today, because all applications should use Unicode.</span></span> <span data-ttu-id="099d5-146">Sin embargo, es posible que los vea en código anterior y en algunos de los ejemplos de código de MSDN.</span><span class="sxs-lookup"><span data-stu-id="099d5-146">However, you might see them in older code and in some of the MSDN code examples.</span></span>

<span data-ttu-id="099d5-147">Los encabezados de las bibliotecas en tiempo de ejecución de C de Microsoft definen un conjunto similar de macros.</span><span class="sxs-lookup"><span data-stu-id="099d5-147">The headers for the Microsoft C run-time libraries define a similar set of macros.</span></span> <span data-ttu-id="099d5-148">Por ejemplo, **\_ tcslen** se resuelve como **strlen** si `_UNICODE` no está definido; de lo contrario, se resuelve como **wcslen**, que es la versión con caracteres anchos de **strlen**.</span><span class="sxs-lookup"><span data-stu-id="099d5-148">For example, **\_tcslen** resolves to **strlen** if `_UNICODE` is undefined; otherwise it resolves to **wcslen**, which is the wide-character version of **strlen**.</span></span>


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



<span data-ttu-id="099d5-149">Tenga cuidado: algunos encabezados utilizan el símbolo de preprocesador `UNICODE` y otros usan `_UNICODE` con un prefijo de subrayado.</span><span class="sxs-lookup"><span data-stu-id="099d5-149">Be careful: Some headers use the preprocessor symbol `UNICODE`, others use `_UNICODE` with an underscore prefix.</span></span> <span data-ttu-id="099d5-150">Defina siempre ambos símbolos.</span><span class="sxs-lookup"><span data-stu-id="099d5-150">Always define both symbols.</span></span> <span data-ttu-id="099d5-151">Visual C++ los establece de forma predeterminada al crear un nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="099d5-151">Visual C++ sets them both by default when you create a new project.</span></span>

## <a name="next"></a><span data-ttu-id="099d5-152">Siguientes</span><span class="sxs-lookup"><span data-stu-id="099d5-152">Next</span></span>

[<span data-ttu-id="099d5-153">¿Qué es una ventana?</span><span class="sxs-lookup"><span data-stu-id="099d5-153">What Is a Window?</span></span>](what-is-a-window-.md)

 

 