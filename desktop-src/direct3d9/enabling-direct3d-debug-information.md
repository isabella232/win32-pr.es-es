---
description: ¿Está intentando obtener más información sobre los objetos de Direct3D durante la depuración? Por ejemplo, en la siguiente captura de pantalla se muestra lo que se ve normalmente al mirar una interfaz Direct3D en la ventana Inspección.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Habilitar la información de depuración de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151947"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a><span data-ttu-id="d60c3-104">Habilitar la información de depuración de Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d60c3-104">Enabling Direct3D Debug Information (Direct3D 9)</span></span>

<span data-ttu-id="d60c3-105">¿Está intentando obtener más información sobre los objetos de Direct3D durante la depuración?</span><span class="sxs-lookup"><span data-stu-id="d60c3-105">Are you trying to find out more information about Direct3D objects during debug?</span></span> <span data-ttu-id="d60c3-106">Por ejemplo, en la siguiente captura de pantalla se muestra lo que se ve normalmente al mirar una interfaz Direct3D en la ventana Inspección.</span><span class="sxs-lookup"><span data-stu-id="d60c3-106">For instance, the following screen shot shows what you typically see when you look at a Direct3D interface in the watch window.</span></span>

![captura de pantalla de una interfaz Direct3D en la ventana Inspección](images/d3d-debug-info1.png)

<span data-ttu-id="d60c3-108">Puede habilitar los objetos de depuración principales para que un objeto reflejado que contenga todas las propiedades del objeto se pueda ver en la ventana Inspección.</span><span class="sxs-lookup"><span data-stu-id="d60c3-108">You can enable the core debug objects so that a mirrored object which contains all of the properties of the object can be viewed in the watch window.</span></span> <span data-ttu-id="d60c3-109">Simplemente incluya la siguiente \# definición en el código antes del archivo D3D9. h:</span><span class="sxs-lookup"><span data-stu-id="d60c3-109">Simply include the following \#define in your code before the D3D9.h file:</span></span>


```
#define D3D_DEBUG_INFO
```



<span data-ttu-id="d60c3-110">Para habilitar la información de depuración, la \# definición se debe compilar antes que el archivo D3D9. h (cualquier programa que use DXUT habilitará automáticamente la \_ información de depuración D3D \_ cuando el programa se compile para depurar).</span><span class="sxs-lookup"><span data-stu-id="d60c3-110">To enable debug information, the \#define must get built before the D3D9.h file (Any program using DXUT will automatically enable D3D\_DEBUG\_INFO when the program is compiled for debug).</span></span> <span data-ttu-id="d60c3-111">Si está ejecutando un ejemplo de SDK, puede verlo en DXStdAfx. h (que afecta a todos los ejemplos de C++).</span><span class="sxs-lookup"><span data-stu-id="d60c3-111">If you are running a SDK sample, you can see this in DXStdAfx.h (which affects all the C++ samples).</span></span> <span data-ttu-id="d60c3-112">También debe ejecutar el tiempo de ejecución de depuración de Direct3D (que se puede habilitar desde el panel de control si es necesario).</span><span class="sxs-lookup"><span data-stu-id="d60c3-112">You must also be running the debug Direct3D runtime (which can be enabled from the Control Panel if necessary).</span></span>

<span data-ttu-id="d60c3-113">Este es un ejemplo en el que se usa el [ejemplo BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="d60c3-113">Here's an example using the [BasicHLSL Sample](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span></span>

1.  <span data-ttu-id="d60c3-114">Agregue la \# definición al archivo Dxstdafx. h antes de la línea 37.</span><span class="sxs-lookup"><span data-stu-id="d60c3-114">Add the \#define to the Dxstdafx.h file before line 37.</span></span>
2.  <span data-ttu-id="d60c3-115">Compilar un proyecto de depuración.</span><span class="sxs-lookup"><span data-stu-id="d60c3-115">Build a debug project.</span></span>
3.  <span data-ttu-id="d60c3-116">Establecer un punto de interrupción en la línea 307 en BasicHLSL. cpp</span><span class="sxs-lookup"><span data-stu-id="d60c3-116">Set a breakpoint at line 307 in BasicHLSL.cpp</span></span>
4.  <span data-ttu-id="d60c3-117">Ejecutar el depurador.</span><span class="sxs-lookup"><span data-stu-id="d60c3-117">Run the debugger.</span></span>

<span data-ttu-id="d60c3-118">En la captura de pantalla siguiente se muestra el tipo de información detallada que puede obtener sobre un objeto de textura de Direct3D desde la ventana Inspección.</span><span class="sxs-lookup"><span data-stu-id="d60c3-118">The following screen shot shows the kind of detailed information you can get about a Direct3D texture object from the watch window.</span></span>

![captura de pantalla de un objeto de textura de Direct3D en la ventana Inspección](images/d3d-debug-info2.png)

> [!Note]
>
> <span data-ttu-id="d60c3-120">Los nombres de las propiedades del objeto son visibles y los valores solo son correctos cuando se habilita el tiempo de ejecución de depuración.</span><span class="sxs-lookup"><span data-stu-id="d60c3-120">The object property names are visible and the values are correct only when the debug runtime is enabled.</span></span> <span data-ttu-id="d60c3-121">Cuando se ejecuta en el Runtime de venta directa, los valores no son válidos.</span><span class="sxs-lookup"><span data-stu-id="d60c3-121">When running against the retail runtime, the values are invalid.</span></span>

 

## <a name="use-the-call-stack-for-extended-debug"></a><span data-ttu-id="d60c3-122">Usar la pila de llamadas para la depuración extendida</span><span class="sxs-lookup"><span data-stu-id="d60c3-122">Use the Call Stack for Extended Debug</span></span>

<span data-ttu-id="d60c3-123">Con la depuración de Direct3D habilitada, también puede examinar una pila de llamadas cada vez que se crea un objeto.</span><span class="sxs-lookup"><span data-stu-id="d60c3-123">With Direct3D debug enabled, you can also look at a call stack each time an object is created.</span></span> <span data-ttu-id="d60c3-124">Esto hará que la aplicación sea muy lenta, pero se puede usar para comprobar si hay pérdidas de recursos.</span><span class="sxs-lookup"><span data-stu-id="d60c3-124">This will make your application very slow, but can be used to check for resource leaks.</span></span> <span data-ttu-id="d60c3-125">Para escribir la pila de llamadas, establezca la siguiente clave del registro en 1:</span><span class="sxs-lookup"><span data-stu-id="d60c3-125">To write out the call stack, set the following registry key to 1:</span></span>


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



<span data-ttu-id="d60c3-126">Al compilar la aplicación con depuración habilitada, obtendrá acceso a esta variable adicional:</span><span class="sxs-lookup"><span data-stu-id="d60c3-126">Building your application with debug enabled will give you access to this additional variable:</span></span>


```
  LPCWSTR CreationCallStack;
```



<span data-ttu-id="d60c3-127">Esta variable almacenará la pila de llamadas cada vez que se cree un objeto.</span><span class="sxs-lookup"><span data-stu-id="d60c3-127">This variable will store the call stack each time that an object is created.</span></span> <span data-ttu-id="d60c3-128">Esto hará que la aplicación sea muy lenta, pero se puede usar para depurar pérdidas de recursos.</span><span class="sxs-lookup"><span data-stu-id="d60c3-128">This will make your application very slow, but can be used to debug resource leaks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d60c3-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d60c3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d60c3-130">Sugerencias de programación</span><span class="sxs-lookup"><span data-stu-id="d60c3-130">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



