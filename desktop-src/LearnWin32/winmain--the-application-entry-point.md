---
<span data-ttu-id="c9b93-101">title: WinMain The Application Entry Point description: WinMain: The Application Entry Point ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="c9b93-101">title: WinMain The Application Entry Point description: WinMain: The Application Entry Point ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="winmain-the-application-entry-point"></a><span data-ttu-id="c9b93-102">WinMain: el punto de entrada de la aplicación</span><span class="sxs-lookup"><span data-stu-id="c9b93-102">WinMain: The Application Entry Point</span></span>

<span data-ttu-id="c9b93-103">Cada programa de Windows incluye una función de punto de entrada denominada **WinMain** o **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="c9b93-103">Every Windows program includes an entry-point function that is named either **WinMain** or **wWinMain**.</span></span> <span data-ttu-id="c9b93-104">Esta es la firma de **wWinMain.**</span><span class="sxs-lookup"><span data-stu-id="c9b93-104">Here is the signature for **wWinMain**.</span></span>


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



<span data-ttu-id="c9b93-105">Los cuatro parámetros son:</span><span class="sxs-lookup"><span data-stu-id="c9b93-105">The four parameters are:</span></span>

-   <span data-ttu-id="c9b93-106">*hInstance* es algo denominado "identificador de una instancia" o "identificador de un módulo".</span><span class="sxs-lookup"><span data-stu-id="c9b93-106">*hInstance* is something called a "handle to an instance" or "handle to a module."</span></span> <span data-ttu-id="c9b93-107">El sistema operativo usa este valor para identificar el ejecutable (EXE) cuando se carga en memoria.</span><span class="sxs-lookup"><span data-stu-id="c9b93-107">The operating system uses this value to identify the executable (EXE) when it is loaded in memory.</span></span> <span data-ttu-id="c9b93-108">El identificador de instancia es necesario para determinadas funciones de Windows, por ejemplo, para cargar iconos o mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="c9b93-108">The instance handle is needed for certain Windows functions—for example, to load icons or bitmaps.</span></span>
-   <span data-ttu-id="c9b93-109">*hPrevInstance* no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="c9b93-109">*hPrevInstance* has no meaning.</span></span> <span data-ttu-id="c9b93-110">Se usó en Windows de 16 bits, pero ahora es siempre cero.</span><span class="sxs-lookup"><span data-stu-id="c9b93-110">It was used in 16-bit Windows, but is now always zero.</span></span>
-   <span data-ttu-id="c9b93-111">*pCmdLine contiene* los argumentos de línea de comandos como una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="c9b93-111">*pCmdLine* contains the command-line arguments as a Unicode string.</span></span>
-   <span data-ttu-id="c9b93-112">*nCmdShow* es una marca que indica si la ventana principal de la aplicación se minimizará, maximizará o se mostrará con normalidad.</span><span class="sxs-lookup"><span data-stu-id="c9b93-112">*nCmdShow* is a flag that says whether the main application window will be minimized, maximized, or shown normally.</span></span>

<span data-ttu-id="c9b93-113">La función devuelve un **valor** int.</span><span class="sxs-lookup"><span data-stu-id="c9b93-113">The function returns an **int** value.</span></span> <span data-ttu-id="c9b93-114">El sistema operativo no usa el valor devuelto, pero puede usar el valor devuelto para transmitir un código de estado a algún otro programa que escriba.</span><span class="sxs-lookup"><span data-stu-id="c9b93-114">The return value is not used by the operating system, but you can use the return value to convey a status code to some other program that you write.</span></span>

<span data-ttu-id="c9b93-115">**WINAPI** es la convención de llamada.</span><span class="sxs-lookup"><span data-stu-id="c9b93-115">**WINAPI** is the calling convention.</span></span> <span data-ttu-id="c9b93-116">Una *convención de llamada* define cómo una función recibe parámetros del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="c9b93-116">A *calling convention* defines how a function receives parameters from the caller.</span></span> <span data-ttu-id="c9b93-117">Por ejemplo, define el orden en que aparecen los parámetros en la pila.</span><span class="sxs-lookup"><span data-stu-id="c9b93-117">For example, it defines the order that parameters appear on the stack.</span></span> <span data-ttu-id="c9b93-118">Asegúrese de declarar la función **wWinMain** como se muestra.</span><span class="sxs-lookup"><span data-stu-id="c9b93-118">Just make sure to declare your **wWinMain** function as shown.</span></span>

<span data-ttu-id="c9b93-119">La **función WinMain** es idéntica a **wWinMain,** salvo que los argumentos de la línea de comandos se pasan como una cadena ANSI.</span><span class="sxs-lookup"><span data-stu-id="c9b93-119">The **WinMain** function is identical to **wWinMain**, except the command-line arguments are passed as an ANSI string.</span></span> <span data-ttu-id="c9b93-120">Se prefiere la versión Unicode.</span><span class="sxs-lookup"><span data-stu-id="c9b93-120">The Unicode version is preferred.</span></span> <span data-ttu-id="c9b93-121">Puede usar la función **ANSI WinMain** incluso si compila el programa como Unicode.</span><span class="sxs-lookup"><span data-stu-id="c9b93-121">You can use the ANSI **WinMain** function even if you compile your program as Unicode.</span></span> <span data-ttu-id="c9b93-122">Para obtener una copia Unicode de los argumentos de la línea de comandos, llame a la [**función GetCommandLine.**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea)</span><span class="sxs-lookup"><span data-stu-id="c9b93-122">To get a Unicode copy of the command-line arguments, call the [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function.</span></span> <span data-ttu-id="c9b93-123">Esta función devuelve todos los argumentos de una sola cadena.</span><span class="sxs-lookup"><span data-stu-id="c9b93-123">This function returns all of the arguments in a single string.</span></span> <span data-ttu-id="c9b93-124">Si desea que los argumentos como una *matriz argv*-style, pase esta cadena a [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span><span class="sxs-lookup"><span data-stu-id="c9b93-124">If you want the arguments as an *argv*-style array, pass this string to [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span></span>

<span data-ttu-id="c9b93-125">¿Cómo sabe el compilador invocar **wWinMain en** lugar de la **función main** estándar?</span><span class="sxs-lookup"><span data-stu-id="c9b93-125">How does the compiler know to invoke **wWinMain** instead of the standard **main** function?</span></span> <span data-ttu-id="c9b93-126">Lo que sucede realmente es que la biblioteca en tiempo de ejecución de Microsoft C (CRT) proporciona una implementación de **main** que llama a **WinMain** o **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="c9b93-126">What actually happens is that the Microsoft C runtime library (CRT) provides an implementation of **main** that calls either **WinMain** or **wWinMain**.</span></span>

> [!Note]  
> <span data-ttu-id="c9b93-127">CRT realiza algún trabajo adicional dentro de **main**.</span><span class="sxs-lookup"><span data-stu-id="c9b93-127">The CRT does some additional work inside **main**.</span></span> <span data-ttu-id="c9b93-128">Por ejemplo, se llama a cualquier inicializador estático antes **que wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="c9b93-128">For example, any static initializers are called before **wWinMain**.</span></span> <span data-ttu-id="c9b93-129">Aunque puede decir al vinculador que use una función de punto de entrada diferente, use el valor predeterminado si vincula a CRT.</span><span class="sxs-lookup"><span data-stu-id="c9b93-129">Although you can tell the linker to use a different entry-point function, use the default if you link to the CRT.</span></span> <span data-ttu-id="c9b93-130">De lo contrario, se omitirá el código de inicialización de CRT, con resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="c9b93-130">Otherwise, the CRT initialization code will be skipped, with unpredictable results.</span></span> <span data-ttu-id="c9b93-131">(Por ejemplo, los objetos globales no se inicializarán correctamente).</span><span class="sxs-lookup"><span data-stu-id="c9b93-131">(For example, global objects will not be initialized correctly.)</span></span>

 

<span data-ttu-id="c9b93-132">Esta es una función **vacía de WinMain.**</span><span class="sxs-lookup"><span data-stu-id="c9b93-132">Here is an empty **WinMain** function.</span></span>


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



<span data-ttu-id="c9b93-133">Ahora que tiene el punto de entrada y comprende algunas de las convenciones básicas de terminología y codificación, está listo para crear un programa de Ventana completo.</span><span class="sxs-lookup"><span data-stu-id="c9b93-133">Now that you have the entry point and understand some of the basic terminology and coding conventions, you are ready to create a complete Window program.</span></span>

## <a name="next"></a><span data-ttu-id="c9b93-134">Siguientes</span><span class="sxs-lookup"><span data-stu-id="c9b93-134">Next</span></span>

<span data-ttu-id="c9b93-135">[Módulo 1. Su primer programa de Windows.](your-first-windows-program.md)</span><span class="sxs-lookup"><span data-stu-id="c9b93-135">[Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

 

 
