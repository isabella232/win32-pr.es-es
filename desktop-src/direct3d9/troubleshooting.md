---
description: En este tema se enumeran las categorías comunes de problemas que pueden surgir al escribir aplicaciones de Direct3D y cómo evitarlos.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Solución de problemas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6726e761dd8c15e2da18e6c370472a73e82cef0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714770"
---
# <a name="troubleshooting-direct3d-9"></a><span data-ttu-id="a2db0-103">Solución de problemas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2db0-103">Troubleshooting (Direct3D 9)</span></span>

<span data-ttu-id="a2db0-104">En este tema se enumeran las categorías comunes de problemas que pueden surgir al escribir aplicaciones de Direct3D y cómo evitarlos.</span><span class="sxs-lookup"><span data-stu-id="a2db0-104">This topic lists common categories of problems that you might encounter when writing Direct3D applications, and how to prevent them.</span></span>

## <a name="device-creation"></a><span data-ttu-id="a2db0-105">Creación de dispositivos</span><span class="sxs-lookup"><span data-stu-id="a2db0-105">Device Creation</span></span>

<span data-ttu-id="a2db0-106">Si se produce un error en la aplicación durante la creación del dispositivo, compruebe los siguientes errores comunes.</span><span class="sxs-lookup"><span data-stu-id="a2db0-106">If your application fails during device creation, check for the following common errors.</span></span>

-   <span data-ttu-id="a2db0-107">Asegúrese de comprobar las capacidades del dispositivo, especialmente las profundidades de representación.</span><span class="sxs-lookup"><span data-stu-id="a2db0-107">Make sure you check the device capabilities, particularly the render depths.</span></span>
-   <span data-ttu-id="a2db0-108">Examine el código de error.</span><span class="sxs-lookup"><span data-stu-id="a2db0-108">Examine the error code.</span></span> <span data-ttu-id="a2db0-109">D3DERR \_ OUTOFVIDEOMEMORY siempre es posible.</span><span class="sxs-lookup"><span data-stu-id="a2db0-109">D3DERR\_OUTOFVIDEOMEMORY is always possible.</span></span>
-   <span data-ttu-id="a2db0-110">Use las bibliotecas de vínculos dinámicos (dll) de DirectX de depuración y revise los mensajes de salida en el depurador.</span><span class="sxs-lookup"><span data-stu-id="a2db0-110">Use the debug DirectX dynamic-link libraries (DLLs) and review output messages under the debugger.</span></span>

## <a name="using-lit-vertices"></a><span data-ttu-id="a2db0-111">Usar vértices iluminados</span><span class="sxs-lookup"><span data-stu-id="a2db0-111">Using Lit Vertices</span></span>

<span data-ttu-id="a2db0-112">Las aplicaciones que usan vértices Lit deben deshabilitar el motor de iluminación de Direct3D estableciendo el \_ Estado de representación de iluminación D3DRS en **false**.</span><span class="sxs-lookup"><span data-stu-id="a2db0-112">Applications that use lit vertices should disable the Direct3D lighting engine by setting the D3DRS\_LIGHTING render state to **FALSE**.</span></span> <span data-ttu-id="a2db0-113">De forma predeterminada, cuando se habilita la iluminación, el sistema establece el color de cualquier vértice que no contenga un vector normal en 0 (negro), incluso si el vértice de entrada contenía un valor de color distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a2db0-113">By default, when lighting is enabled, the system sets the color for any vertex that doesn't contain a normal vector to 0 (black), even if the input vertex contained a nonzero color value.</span></span> <span data-ttu-id="a2db0-114">Dado que los vértices iluminados no, por su naturaleza, contienen un vértice normal, cualquier información de color pasada a Direct3D se pierde durante la representación si está habilitado el motor de iluminación.</span><span class="sxs-lookup"><span data-stu-id="a2db0-114">Because lit-vertices don't, by their nature, contain a vertex normal, any color information passed to Direct3D is lost during rendering if the lighting engine is enabled.</span></span>

<span data-ttu-id="a2db0-115">Obviamente, el color de vértice es importante para cualquier aplicación que realice su propia iluminación.</span><span class="sxs-lookup"><span data-stu-id="a2db0-115">Obviously, vertex color is important to any application that performs its own lighting.</span></span> <span data-ttu-id="a2db0-116">Para evitar que el sistema imponga los valores predeterminados, asegúrese de establecer la \_ iluminación D3DRS en **false**.</span><span class="sxs-lookup"><span data-stu-id="a2db0-116">To prevent the system from imposing the default values, make sure you set D3DRS\_LIGHTING to **FALSE**.</span></span>

<span data-ttu-id="a2db0-117">Si la aplicación se ejecuta pero no hay nada visible, busque los siguientes errores comunes.</span><span class="sxs-lookup"><span data-stu-id="a2db0-117">If your application runs but nothing is visible, check for the following common errors.</span></span>

-   <span data-ttu-id="a2db0-118">Asegúrese de que los triángulos no se degeneran.</span><span class="sxs-lookup"><span data-stu-id="a2db0-118">Ensure that your triangles are not degenerate.</span></span>
-   <span data-ttu-id="a2db0-119">Asegúrese de que los triángulos no se seleccionan.</span><span class="sxs-lookup"><span data-stu-id="a2db0-119">Ensure that your triangles are not being culled.</span></span>
-   <span data-ttu-id="a2db0-120">Asegúrese de que las transformaciones son coherentes internamente.</span><span class="sxs-lookup"><span data-stu-id="a2db0-120">Make sure that your transformations are internally consistent.</span></span>
-   <span data-ttu-id="a2db0-121">Compruebe la configuración de la ventanilla para asegurarse de que permite que se vean los triángulos.</span><span class="sxs-lookup"><span data-stu-id="a2db0-121">Check the viewport settings to be sure they allow your triangles to be seen.</span></span>

## <a name="debugging"></a><span data-ttu-id="a2db0-122">Depuración</span><span class="sxs-lookup"><span data-stu-id="a2db0-122">Debugging</span></span>

<span data-ttu-id="a2db0-123">La depuración de una aplicación Direct3D puede ser desafiante.</span><span class="sxs-lookup"><span data-stu-id="a2db0-123">Debugging a Direct3D application can be challenging.</span></span> <span data-ttu-id="a2db0-124">Pruebe las siguientes técnicas, además de comprobar todos los valores devueltos, una parte de consejos especialmente importante en la programación de Direct3D, que depende de implementaciones de hardware muy diferentes.</span><span class="sxs-lookup"><span data-stu-id="a2db0-124">Try the following techniques, in addition to checking all the return values - a particularly important piece of advice in Direct3D programming, which is dependent on very different hardware implementations.</span></span>

-   <span data-ttu-id="a2db0-125">Cambie a dll de depuración.</span><span class="sxs-lookup"><span data-stu-id="a2db0-125">Switch to debug DLLs.</span></span>
-   <span data-ttu-id="a2db0-126">Fuerce un dispositivo solo de software, desactivando la aceleración de hardware incluso cuando esté disponible.</span><span class="sxs-lookup"><span data-stu-id="a2db0-126">Force a software-only device, turning off hardware acceleration even when it is available.</span></span>
-   <span data-ttu-id="a2db0-127">Fuerce las superficies en la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="a2db0-127">Force surfaces into system memory.</span></span>
-   <span data-ttu-id="a2db0-128">Cree una opción para ejecutarla en una ventana, de modo que pueda usar un depurador integrado.</span><span class="sxs-lookup"><span data-stu-id="a2db0-128">Create an option to run in a window, so that you can use an integrated debugger.</span></span>

<span data-ttu-id="a2db0-129">La segunda y tercera opciones de esta lista pueden ayudarle a evitar el bloqueo de Win16 que, de lo contrario, puede hacer que el depurador se bloquee.</span><span class="sxs-lookup"><span data-stu-id="a2db0-129">The second and third options in this list can help you avoid the Win16 lock which can otherwise cause your debugger to hang.</span></span>

<span data-ttu-id="a2db0-130">Además, intente agregar las siguientes entradas a Win.ini.</span><span class="sxs-lookup"><span data-stu-id="a2db0-130">Also, try adding the following entries to Win.ini.</span></span>


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a><span data-ttu-id="a2db0-131">Inicialización de Borland Floating-Point</span><span class="sxs-lookup"><span data-stu-id="a2db0-131">Borland Floating-Point Initialization</span></span>

<span data-ttu-id="a2db0-132">Los compiladores de Borland notifican las excepciones de punto flotante de una manera que es incompatible con Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a2db0-132">Compilers from Borland report floating-point exceptions in a manner that is incompatible with Direct3D.</span></span> <span data-ttu-id="a2db0-133">Para solucionar este problema, incluya un \_ controlador de excepciones de matherr similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="a2db0-133">To solve this problem, include a \_matherr exception handler like the following:</span></span>


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a><span data-ttu-id="a2db0-134">Validación de parámetros</span><span class="sxs-lookup"><span data-stu-id="a2db0-134">Parameter Validation</span></span>

<span data-ttu-id="a2db0-135">Por motivos de rendimiento, la versión de depuración del tiempo de ejecución del modo inmediato de Direct3D realiza más validaciones de parámetros que la versión comercial, que a veces no realiza ninguna validación.</span><span class="sxs-lookup"><span data-stu-id="a2db0-135">For performance reasons, the debug version of the Direct3D Immediate Mode run time performs more parameter validation than the retail version, which sometimes performs no validation at all.</span></span> <span data-ttu-id="a2db0-136">Esto permite que las aplicaciones realicen una depuración sólida con el componente de tiempo de ejecución de depuración más lento antes de usar la versión comercial más rápida para el ajuste del rendimiento y la versión final.</span><span class="sxs-lookup"><span data-stu-id="a2db0-136">This enables applications to perform robust debugging with the slower debug run-time component before using the faster retail version for performance tuning and final release.</span></span>

<span data-ttu-id="a2db0-137">Aunque varios métodos de modo inmediato de Direct3D imponen límites a los valores que pueden aceptar, a menudo estos límites solo se comprueban y aplican mediante la versión de depuración del tiempo de ejecución del modo inmediato de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a2db0-137">Although several Direct3D Immediate Mode methods impose limits on the values that they can accept, these limits are often only checked and enforced by the debug version of the Direct3D Immediate Mode run time.</span></span> <span data-ttu-id="a2db0-138">Las aplicaciones deben cumplir estos límites, o bien se pueden producir resultados imprevisibles y no deseados cuando se ejecutan en la versión comercial de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a2db0-138">Applications must conform to these limits, or unpredictable and undesirable results can occur when running on the retail version of Direct3D.</span></span> <span data-ttu-id="a2db0-139">Por ejemplo, el método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) acepta un parámetro (PrimitiveCount) que indica el número de primitivas que representará el método.</span><span class="sxs-lookup"><span data-stu-id="a2db0-139">For example, the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method accepts a parameter (PrimitiveCount) that indicates the number of primitives that the method will render.</span></span> <span data-ttu-id="a2db0-140">El método solo puede aceptar valores entre 0 y D3DMAXNUMPRIMITIVES.</span><span class="sxs-lookup"><span data-stu-id="a2db0-140">The method can only accept values between 0 and D3DMAXNUMPRIMITIVES.</span></span> <span data-ttu-id="a2db0-141">En la versión de depuración de Direct3D, si se pasan más de D3DMAXNUMPRIMITIVES primitivos, se produce un error en el método correctamente, se imprime un mensaje de error en el registro de errores y se devuelve un valor de error a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a2db0-141">In the debug version of Direct3D, if you pass more than D3DMAXNUMPRIMITIVES primitives, the method fails gracefully, printing an error message to the error log, and returning an error value to your application.</span></span> <span data-ttu-id="a2db0-142">Por el contrario, si la aplicación realiza el mismo error cuando se ejecuta con la versión comercial del tiempo de ejecución, el comportamiento es indefinido.</span><span class="sxs-lookup"><span data-stu-id="a2db0-142">Conversely, if your application makes the same error when it is running with the retail version of the run time, behavior is undefined.</span></span> <span data-ttu-id="a2db0-143">Por motivos de rendimiento, el método no valida los parámetros, lo que da lugar a un comportamiento impredecible y completamente inexistente cuando no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a2db0-143">For performance reasons, the method does not validate the parameters, resulting in unpredictable and completely situational behavior when they are not valid.</span></span> <span data-ttu-id="a2db0-144">En algunos casos, la llamada podría funcionar y, en otros casos, podría provocar un error de memoria en Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a2db0-144">In some cases the call might work, and in other cases it might cause a memory fault in Direct3D.</span></span> <span data-ttu-id="a2db0-145">Si una llamada no válida funciona constantemente con una configuración de hardware determinada y la versión de DirectX, no hay ninguna garantía de que siga funcionando en otro hardware o con versiones posteriores de DirectX.</span><span class="sxs-lookup"><span data-stu-id="a2db0-145">If an invalid call consistently works with a particular hardware configuration and DirectX version, there is no guarantee that it will continue to function on other hardware or with later releases of DirectX.</span></span>

<span data-ttu-id="a2db0-146">Si la aplicación detecta errores no explicados cuando se ejecuta con el archivo de tiempo de ejecución de Direct3D comercial, pruebe con la versión de depuración y Mire atentamente los casos en los que la aplicación pase parámetros no válidos.</span><span class="sxs-lookup"><span data-stu-id="a2db0-146">If your application encounters unexplained failures when running with the retail Direct3D run-time file, test against the debug version and look closely for cases where your application passes invalid parameters.</span></span> <span data-ttu-id="a2db0-147">Use el applet del panel de control de DirectX, cambie al tiempo de ejecución de depuración si es necesario y active la opción "interrumpir en D3DError".</span><span class="sxs-lookup"><span data-stu-id="a2db0-147">Use the DirectX control panel applet, switch to the debug runtime if necessary, and check the "Break on D3DError" option.</span></span> <span data-ttu-id="a2db0-148">Esta opción forzará al tiempo de ejecución a utilizar el método DebugBreak de Windows para forzar que la aplicación se detenga cuando se detecte un error de aplicación.</span><span class="sxs-lookup"><span data-stu-id="a2db0-148">This option will force the runtime to use the Windows DebugBreak method in order to force the application to stop when an application bug is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2db0-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2db0-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2db0-150">Sugerencias de programación</span><span class="sxs-lookup"><span data-stu-id="a2db0-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
