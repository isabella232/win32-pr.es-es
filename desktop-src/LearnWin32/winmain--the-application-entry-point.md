---
title: WinMain el punto de entrada de la aplicación
description: .
ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef44c4d31aa53dfd60f579b68c438a539058b85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104270903"
---
# <a name="winmain-the-application-entry-point"></a><span data-ttu-id="8b142-103">WinMain: el punto de entrada de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8b142-103">WinMain: The Application Entry Point</span></span>

<span data-ttu-id="8b142-104">Cada programa de Windows incluye una función de punto de entrada que se denomina **WinMain** o **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="8b142-104">Every Windows program includes an entry-point function that is named either **WinMain** or **wWinMain**.</span></span> <span data-ttu-id="8b142-105">Esta es la firma de **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="8b142-105">Here is the signature for **wWinMain**.</span></span>


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



<span data-ttu-id="8b142-106">Los cuatro parámetros son:</span><span class="sxs-lookup"><span data-stu-id="8b142-106">The four parameters are:</span></span>

-   <span data-ttu-id="8b142-107">*hInstance* es algo denominado "identificador de una instancia" o "identificador de un módulo".</span><span class="sxs-lookup"><span data-stu-id="8b142-107">*hInstance* is something called a "handle to an instance" or "handle to a module."</span></span> <span data-ttu-id="8b142-108">El sistema operativo usa este valor para identificar el archivo ejecutable (EXE) cuando se carga en la memoria.</span><span class="sxs-lookup"><span data-stu-id="8b142-108">The operating system uses this value to identify the executable (EXE) when it is loaded in memory.</span></span> <span data-ttu-id="8b142-109">El identificador de instancia es necesario para ciertas funciones de Windows, por ejemplo, para cargar iconos o mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="8b142-109">The instance handle is needed for certain Windows functions—for example, to load icons or bitmaps.</span></span>
-   <span data-ttu-id="8b142-110">*hPrevInstance* no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="8b142-110">*hPrevInstance* has no meaning.</span></span> <span data-ttu-id="8b142-111">Se usaba en Windows de 16 bits, pero ahora siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="8b142-111">It was used in 16-bit Windows, but is now always zero.</span></span>
-   <span data-ttu-id="8b142-112">*pCmdLine* contiene los argumentos de la línea de comandos como una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="8b142-112">*pCmdLine* contains the command-line arguments as a Unicode string.</span></span>
-   <span data-ttu-id="8b142-113">*nCmdShow* es una marca que indica si la ventana de la aplicación principal se minimizará, maximizará o se mostrará normalmente.</span><span class="sxs-lookup"><span data-stu-id="8b142-113">*nCmdShow* is a flag that says whether the main application window will be minimized, maximized, or shown normally.</span></span>

<span data-ttu-id="8b142-114">La función devuelve un valor **int** .</span><span class="sxs-lookup"><span data-stu-id="8b142-114">The function returns an **int** value.</span></span> <span data-ttu-id="8b142-115">El sistema operativo no utiliza el valor devuelto, pero puede usar el valor devuelto para transmitir un código de estado a algún otro programa que escriba.</span><span class="sxs-lookup"><span data-stu-id="8b142-115">The return value is not used by the operating system, but you can use the return value to convey a status code to some other program that you write.</span></span>

<span data-ttu-id="8b142-116">**WINAPI** es la Convención de llamada.</span><span class="sxs-lookup"><span data-stu-id="8b142-116">**WINAPI** is the calling convention.</span></span> <span data-ttu-id="8b142-117">Una *Convención de llamada* define cómo una función recibe parámetros del llamador.</span><span class="sxs-lookup"><span data-stu-id="8b142-117">A *calling convention* defines how a function receives parameters from the caller.</span></span> <span data-ttu-id="8b142-118">Por ejemplo, define el orden en que aparecen los parámetros en la pila.</span><span class="sxs-lookup"><span data-stu-id="8b142-118">For example, it defines the order that parameters appear on the stack.</span></span> <span data-ttu-id="8b142-119">Solo tiene que asegurarse de declarar la función **wWinMain** como se muestra.</span><span class="sxs-lookup"><span data-stu-id="8b142-119">Just make sure to declare your **wWinMain** function as shown.</span></span>

<span data-ttu-id="8b142-120">La función **WinMain** es idéntica a **wWinMain**, salvo que los argumentos de la línea de comandos se pasan como una cadena ANSI.</span><span class="sxs-lookup"><span data-stu-id="8b142-120">The **WinMain** function is identical to **wWinMain**, except the command-line arguments are passed as an ANSI string.</span></span> <span data-ttu-id="8b142-121">Se prefiere la versión Unicode.</span><span class="sxs-lookup"><span data-stu-id="8b142-121">The Unicode version is preferred.</span></span> <span data-ttu-id="8b142-122">Puede utilizar la función de ANSI **WinMain** incluso si compila el programa como Unicode.</span><span class="sxs-lookup"><span data-stu-id="8b142-122">You can use the ANSI **WinMain** function even if you compile your program as Unicode.</span></span> <span data-ttu-id="8b142-123">Para obtener una copia Unicode de los argumentos de la línea de comandos, llame a la función [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) .</span><span class="sxs-lookup"><span data-stu-id="8b142-123">To get a Unicode copy of the command-line arguments, call the [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function.</span></span> <span data-ttu-id="8b142-124">Esta función devuelve todos los argumentos en una sola cadena.</span><span class="sxs-lookup"><span data-stu-id="8b142-124">This function returns all of the arguments in a single string.</span></span> <span data-ttu-id="8b142-125">Si desea los argumentos como una matriz de estilo *argv*, pase esta cadena a [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span><span class="sxs-lookup"><span data-stu-id="8b142-125">If you want the arguments as an *argv*-style array, pass this string to [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span></span>

<span data-ttu-id="8b142-126">¿Cómo sabe el compilador que debe invocar **wWinMain** en lugar de la función **principal** estándar?</span><span class="sxs-lookup"><span data-stu-id="8b142-126">How does the compiler know to invoke **wWinMain** instead of the standard **main** function?</span></span> <span data-ttu-id="8b142-127">Lo que sucede en realidad es que la biblioteca en tiempo de ejecución de Microsoft C (CRT) proporciona una implementación de **Main** que llama a **WinMain** o **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="8b142-127">What actually happens is that the Microsoft C runtime library (CRT) provides an implementation of **main** that calls either **WinMain** or **wWinMain**.</span></span>

> [!Note]  
> <span data-ttu-id="8b142-128">CRT realiza algunas tareas adicionales en **Main**.</span><span class="sxs-lookup"><span data-stu-id="8b142-128">The CRT does some additional work inside **main**.</span></span> <span data-ttu-id="8b142-129">Por ejemplo, se llama a cualquier inicializador estático antes de **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="8b142-129">For example, any static initializers are called before **wWinMain**.</span></span> <span data-ttu-id="8b142-130">Aunque puede indicar al enlazador que use una función de punto de entrada diferente, utilice el valor predeterminado si se vincula a CRT.</span><span class="sxs-lookup"><span data-stu-id="8b142-130">Although you can tell the linker to use a different entry-point function, use the default if you link to the CRT.</span></span> <span data-ttu-id="8b142-131">De lo contrario, se omitirá el código de inicialización de CRT, con resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="8b142-131">Otherwise, the CRT initialization code will be skipped, with unpredictable results.</span></span> <span data-ttu-id="8b142-132">(Por ejemplo, los objetos globales no se inicializarán correctamente).</span><span class="sxs-lookup"><span data-stu-id="8b142-132">(For example, global objects will not be initialized correctly.)</span></span>

 

<span data-ttu-id="8b142-133">Esta es una función **WinMain** vacía.</span><span class="sxs-lookup"><span data-stu-id="8b142-133">Here is an empty **WinMain** function.</span></span>


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



<span data-ttu-id="8b142-134">Ahora que tiene el punto de entrada y comprende algunas de las convenciones básicas de codificación y terminología, está listo para crear un programa de ventana completo.</span><span class="sxs-lookup"><span data-stu-id="8b142-134">Now that you have the entry point and understand some of the basic terminology and coding conventions, you are ready to create a complete Window program.</span></span>

## <a name="next"></a><span data-ttu-id="8b142-135">Siguientes</span><span class="sxs-lookup"><span data-stu-id="8b142-135">Next</span></span>

<span data-ttu-id="8b142-136">[Módulo 1. Su primer programa de Windows](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="8b142-136">[Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

 

 