---
title: Habilitar STRICT
description: Al definir el símbolo STRICT, se habilitan las características que requieren más atención en la declaración y el uso de tipos.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "105707503"
---
# <a name="enabling-strict"></a><span data-ttu-id="c9977-103">Habilitar STRICT</span><span class="sxs-lookup"><span data-stu-id="c9977-103">Enabling STRICT</span></span>

<span data-ttu-id="c9977-104">Al definir el símbolo **STRICT** , se habilitan las características que requieren más atención en la declaración y el uso de tipos.</span><span class="sxs-lookup"><span data-stu-id="c9977-104">When you define the **STRICT** symbol, you enable features that require more care in declaring and using types.</span></span> <span data-ttu-id="c9977-105">Esto le ayuda a escribir código más portable.</span><span class="sxs-lookup"><span data-stu-id="c9977-105">This helps you write more portable code.</span></span> <span data-ttu-id="c9977-106">Este cuidado adicional también reducirá el tiempo de depuración.</span><span class="sxs-lookup"><span data-stu-id="c9977-106">This extra care will also reduce your debugging time.</span></span> <span data-ttu-id="c9977-107">Al habilitar **STRICT** , se redefinen determinados tipos de datos para que el compilador no permita la asignación de un tipo a otro sin una conversión explícita.</span><span class="sxs-lookup"><span data-stu-id="c9977-107">Enabling **STRICT** redefines certain data types so that the compiler does not permit assignment from one type to another without an explicit cast.</span></span> <span data-ttu-id="c9977-108">Esto es especialmente útil con el código de Windows.</span><span class="sxs-lookup"><span data-stu-id="c9977-108">This is especially helpful with Windows code.</span></span> <span data-ttu-id="c9977-109">Los errores al pasar tipos de datos se informan en tiempo de compilación en lugar de producir errores irrecuperables en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c9977-109">Errors in passing data types are reported at compile time instead of causing fatal errors at run time.</span></span>

<span data-ttu-id="c9977-110">Con Visual C++, la comprobación **estricta** de tipos se define de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c9977-110">With Visual C++, **STRICT** type checking is defined by default.</span></span>

<span data-ttu-id="c9977-111">Para definir **STRICT** cada archivo, inserte una instrucción de **\# definición** antes de incluir Windows. h:</span><span class="sxs-lookup"><span data-stu-id="c9977-111">To define **STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define STRICT
#include <windows.h>
```



<span data-ttu-id="c9977-112">Cuando se define **STRICT** , las definiciones de [tipos de datos](windows-data-types.md) cambian como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="c9977-112">When **STRICT** is defined, [data type](windows-data-types.md) definitions change as follows:</span></span>

-   <span data-ttu-id="c9977-113">Los tipos de identificador específicos se definen para ser mutuamente excluyentes; por ejemplo, no podrá pasar un **hWnd** en el que sea necesario un argumento de tipo **HDC** .</span><span class="sxs-lookup"><span data-stu-id="c9977-113">Specific handle types are defined to be mutually exclusive; for example, you will not be able to pass an **HWND** where an **HDC** type argument is required.</span></span> <span data-ttu-id="c9977-114">Sin **STRICT**, todos los identificadores se definen como **Handle**, por lo que el compilador no impide usar un tipo de identificador donde se espera otro tipo.</span><span class="sxs-lookup"><span data-stu-id="c9977-114">Without **STRICT**, all handles are defined as **HANDLE**, so the compiler does not prevent you from using one type of handle where another type is expected.</span></span>
-   <span data-ttu-id="c9977-115">Todos los tipos de función de devolución de llamada (como procedimientos de diálogo, procedimientos de ventana y procedimientos de enlace) se definen con prototipos completos.</span><span class="sxs-lookup"><span data-stu-id="c9977-115">All callback function types (such as dialog procedures, window procedures, and hook procedures) are defined with full prototypes.</span></span> <span data-ttu-id="c9977-116">Esto evita que se declaren funciones de devolución de llamada con listas de parámetros incorrectas.</span><span class="sxs-lookup"><span data-stu-id="c9977-116">This prevents you from declaring callback functions with incorrect parameter lists.</span></span>
-   <span data-ttu-id="c9977-117">Los tipos de parámetro y valor devuelto que deben usar un puntero genérico se declaran correctamente como **LPVOID** en lugar de como **LPSTR** u otro tipo de puntero.</span><span class="sxs-lookup"><span data-stu-id="c9977-117">Parameter and return value types that should use a generic pointer are declared correctly as **LPVOID** instead of as **LPSTR** or another pointer type.</span></span>
-   <span data-ttu-id="c9977-118">La estructura [**comstat**](/windows/desktop/api/winbase/ns-winbase-comstat) se declara según el estándar ANSI.</span><span class="sxs-lookup"><span data-stu-id="c9977-118">The [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) structure is declared according to the ANSI standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9977-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9977-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9977-120">Deshabilitar STRICT</span><span class="sxs-lookup"><span data-stu-id="c9977-120">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="c9977-121">Cumplimiento estricto</span><span class="sxs-lookup"><span data-stu-id="c9977-121">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 
