---
title: Compilación sin conexión
description: La herramienta de compilador de efectos (fxc.exe) está diseñada para la compilación sin conexión de los sombreadores HLSL.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- FXC, compilación sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c2bf96a24cb586a5d229a395cbf6dc0cb9ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793582"
---
# <a name="offline-compiling"></a><span data-ttu-id="e18a0-104">Compilación sin conexión</span><span class="sxs-lookup"><span data-stu-id="e18a0-104">Offline compiling</span></span>

<span data-ttu-id="e18a0-105">La herramienta de compilador de efectos (fxc.exe) está diseñada para la compilación sin conexión de los sombreadores HLSL.</span><span class="sxs-lookup"><span data-stu-id="e18a0-105">The effect-compiler tool (fxc.exe) is designed for offline compilation of HLSL shaders.</span></span>

## <a name="compiling-with-the-current-compiler"></a><span data-ttu-id="e18a0-106">Compilar con el compilador actual</span><span class="sxs-lookup"><span data-stu-id="e18a0-106">Compiling with the current compiler</span></span>

<span data-ttu-id="e18a0-107">Los modelos de sombreador admitidos por el compilador actual se muestran en [perfiles](dx-graphics-tools-fxc-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e18a0-107">The shader models supported by the current compiler are shown in [Profiles](dx-graphics-tools-fxc-syntax.md).</span></span> <span data-ttu-id="e18a0-108">En este ejemplo se compila un sombreador de píxeles para el destino del modelo de sombreador 5,1.</span><span class="sxs-lookup"><span data-stu-id="e18a0-108">This example compiles a pixel shader for the shader model 5.1 target.</span></span>

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="e18a0-109">En este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e18a0-109">In this example:</span></span>

-   <span data-ttu-id="e18a0-110">PS \_ 5 \_ 1 es el perfil de destino.</span><span class="sxs-lookup"><span data-stu-id="e18a0-110">ps\_5\_1 is the target profile.</span></span>
-   <span data-ttu-id="e18a0-111">PixelShader1. FXC es el archivo de objeto de salida que contiene el sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="e18a0-111">PixelShader1.fxc is the output object file containing the compiled shader.</span></span>
-   <span data-ttu-id="e18a0-112">PixelShader1. HLSL es el origen.</span><span class="sxs-lookup"><span data-stu-id="e18a0-112">PixelShader1.hlsl is the source.</span></span>

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="e18a0-113">Las opciones de depuración incluyen opciones adicionales para deshabilitar las optimizaciones del compilador (OD) y habilitar la información de depuración (Zi) como los números de línea y los símbolos.</span><span class="sxs-lookup"><span data-stu-id="e18a0-113">The debug options include additional options to disable compiler optimizations (Od) and enable debug information (Zi) like line numbers and symbols.</span></span>

<span data-ttu-id="e18a0-114">Para obtener una lista completa de las opciones de línea de comandos, vea la página [Sintaxis](dx-graphics-tools-fxc-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="e18a0-114">For a full listing of the command-line options, see the [Syntax](dx-graphics-tools-fxc-syntax.md) page.</span></span>

## <a name="compiling-with-the-legacy-compiler"></a><span data-ttu-id="e18a0-115">Compilar con el compilador heredado</span><span class="sxs-lookup"><span data-stu-id="e18a0-115">Compiling with the legacy compiler</span></span>

<span data-ttu-id="e18a0-116">A partir de Direct3D 10, ya no se admiten algunos modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e18a0-116">Beginning with Direct3D 10, some shader models are no longer supported.</span></span> <span data-ttu-id="e18a0-117">Estos incluyen modelos de sombreador de píxeles: PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 y PS \_ 1 \_ 4, que admiten recursos muy limitados y dependen del hardware.</span><span class="sxs-lookup"><span data-stu-id="e18a0-117">These include pixel shader models: ps\_1\_1, ps\_1\_2, ps\_1\_3, and ps\_1\_4 which support very limited resources and are dependent on hardware.</span></span> <span data-ttu-id="e18a0-118">El compilador se ha rediseñado con el modelo de sombreador 2 (o superior), lo que permite mayores eficiencias con la compilación.</span><span class="sxs-lookup"><span data-stu-id="e18a0-118">The compiler has been redesigned with shader model 2 (or greater) which allows for greater efficiencies with compilation.</span></span> <span data-ttu-id="e18a0-119">Esto requiere que se ejecute en hardware que admita los modelos de sombreador 2 y superiores.</span><span class="sxs-lookup"><span data-stu-id="e18a0-119">This of course will require that you are running on hardware that supports shader models 2 and greater.</span></span>

<span data-ttu-id="e18a0-120">Tenga en cuenta también que debe consultar las notas de la versión del SDK asociadas a su versión del compilador FXC para el comportamiento afectado por el modificador/GEC.</span><span class="sxs-lookup"><span data-stu-id="e18a0-120">Also note that you should consult the SDK release notes associated with your version of the FXC compiler for behavior affected by the /Gec switch.</span></span>

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a><span data-ttu-id="e18a0-121">Usar la herramienta de compilador de efectos en un subproceso</span><span class="sxs-lookup"><span data-stu-id="e18a0-121">Using the effect-compiler tool in a subprocess</span></span>

<span data-ttu-id="e18a0-122">Si una aplicación genera fxc.exe como subproceso, es importante asegurarse de que la aplicación comprueba y Lee los datos de los conductos de salida o de error pasados a la función CreateProcess.</span><span class="sxs-lookup"><span data-stu-id="e18a0-122">If fxc.exe is spawned as a subprocess by an application it is important to ensure that the application checks for and reads any data in output or error pipes passed to the CreateProcess function.</span></span> <span data-ttu-id="e18a0-123">Si la aplicación solo espera a que finalice el subproceso y una de las canalizaciones se llena, el subproceso nunca finalizará.</span><span class="sxs-lookup"><span data-stu-id="e18a0-123">If the application only waits for the subprocess to finish and one of the pipes becomes full the subprocess will never finish.</span></span>

<span data-ttu-id="e18a0-124">En el ejemplo de código siguiente se muestra la espera en un subproceso y la lectura de las canalizaciones de salida y de error adjuntas al subproceso.</span><span class="sxs-lookup"><span data-stu-id="e18a0-124">The following example code illustrates waiting on a subprocess and reading the output and error pipes attached to the subprocess.</span></span> <span data-ttu-id="e18a0-125">El contenido de la `WaitHandles` matriz se corresponde con los identificadores del subproceso, la canalización de stdout y la canalización para stderr.</span><span class="sxs-lookup"><span data-stu-id="e18a0-125">The contents of the `WaitHandles` array correspond to handles for the subprocess, the pipe for stdout and the pipe for stderr.</span></span>

```cpp
HANDLE WaitHandles[] = {
  piProcInfo.hProcess, hReadOutPipe, hReadErrorPipe
};

const DWORD BUFSIZE = 4096;
BYTE buff[BUFSIZE];

while (1)
{
    DWORD dwBytesRead, dwBytesAvailable;

    dwWaitResult = WaitForMultipleObjects(3, WaitHandles, FALSE, 60000L);

    // Read from the pipes...
    while (PeekNamedPipe(hReadOutPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadOutPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamOut << std::string((char*)buff, (size_t)dwBytesRead);
    }
    while (PeekNamedPipe(hReadErrorPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadErrorPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamError << std::string((char*)buff, (size_t)dwBytesRead);
    }

    // Process is done, or we timed out:
    if (dwWaitResult == WAIT_OBJECT_0 || dwWaitResult == WAIT_TIMEOUT)
        break;
}
```

<span data-ttu-id="e18a0-126">Para obtener información adicional sobre cómo generar un proceso, vea la página de referencia de [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="e18a0-126">For additional information on spawning a process see the reference page for [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e18a0-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e18a0-127">Related topics</span></span>

* [<span data-ttu-id="e18a0-128">Efecto: herramienta de compilador</span><span class="sxs-lookup"><span data-stu-id="e18a0-128">Effect-Compiler Tool</span></span>](fxc.md)