---
description: En este tema se enumeran las categorías comunes de problemas que pueden surgir al escribir aplicaciones de Direct3D y cómo evitarlos.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Solución de problemas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637ac4b43e8947a6011e35ae9a36db7829ed47fd4d5740f93778116e4ee8f9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044083"
---
# <a name="troubleshooting-direct3d-9"></a>Solución de problemas (Direct3D 9)

En este tema se enumeran las categorías comunes de problemas que pueden surgir al escribir aplicaciones de Direct3D y cómo evitarlos.

## <a name="device-creation"></a>Creación de dispositivos

Si se produce un error en la aplicación durante la creación del dispositivo, compruebe los siguientes errores comunes.

-   Asegúrese de comprobar las funcionalidades del dispositivo, especialmente las profundidades de representación.
-   Examine el código de error. D3DERR \_ OUTOFVIDEOMEMORY siempre es posible.
-   Use las bibliotecas de vínculos dinámicos (DLL) de DirectX de depuración y revise los mensajes de salida en el depurador.

## <a name="using-lit-vertices"></a>Uso de vértices encendidos

Las aplicaciones que usan vértices encendidos deben deshabilitar el motor de iluminación de Direct3D estableciendo el estado de representación D3DRS \_ LIGHTING en **FALSE.** De forma predeterminada, cuando la iluminación está habilitada, el sistema establece el color de cualquier vértice que no contenga un vector normal en 0 (negro), incluso si el vértice de entrada contenía un valor de color distinto de cero. Dado que los vértices encendidos no contienen, por su naturaleza, un vértice normal, se pierde cualquier información de color que se pase a Direct3D durante la representación si el motor de iluminación está habilitado.

Obviamente, el color de vértice es importante para cualquier aplicación que realice su propia iluminación. Para evitar que el sistema imponga los valores predeterminados, asegúrese de establecer D3DRS \_ LIGHTING en **FALSE.**

Si la aplicación se ejecuta pero no hay nada visible, compruebe los siguientes errores comunes.

-   Asegúrese de que los triángulos no están degenerados.
-   Asegúrese de que los triángulos no se están culled.
-   Asegúrese de que las transformaciones sean coherentes internamente.
-   Compruebe la configuración de la ventanilla para asegurarse de que permiten ver los triángulos.

## <a name="debugging"></a>Depuración

Depurar una aplicación Direct3D puede ser un desafío. Pruebe las técnicas siguientes, además de comprobar todos los valores devueltos, un artículo de consejos especialmente importante en la programación de Direct3D, que depende de implementaciones de hardware muy diferentes.

-   Cambie a archivos DLL de depuración.
-   Forzar un dispositivo solo de software y desactivar la aceleración de hardware incluso cuando esté disponible.
-   Forzar superficies en la memoria del sistema.
-   Cree una opción para ejecutarla en una ventana, de modo que pueda usar un depurador integrado.

La segunda y la tercera opción de esta lista pueden ayudarle a evitar el bloqueo win16, lo que de lo contrario puede hacer que el depurador se bloquee.

Además, intente agregar las siguientes entradas a Win.ini.


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a>Inicialización de Floating-Point Borland

Los compiladores de Borland informan de excepciones de punto flotante de una manera incompatible con Direct3D. Para solucionar este problema, incluya un \_ controlador de excepciones matherr como el siguiente:


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



## <a name="parameter-validation"></a>Validación de parámetros

Por motivos de rendimiento, la versión de depuración del tiempo de ejecución del modo inmediato de Direct3D realiza más validación de parámetros que la versión comercial, que a veces no realiza ninguna validación. Esto permite a las aplicaciones realizar una depuración sólida con el componente de tiempo de ejecución de depuración más lento antes de usar la versión comercial más rápida para optimizar el rendimiento y la versión final.

Aunque varios métodos de modo inmediato de Direct3D imponen límites en los valores que pueden aceptar, estos límites a menudo solo se comprueban y aplican mediante la versión de depuración del tiempo de ejecución del modo inmediato de Direct3D. Las aplicaciones deben cumplir estos límites o pueden producirse resultados imprevisibles e no deseados cuando se ejecutan en la versión comercial de Direct3D. Por ejemplo, el método [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) acepta un parámetro (PrimitiveCount) que indica el número de primitivas que representará el método. El método solo puede aceptar valores entre 0 y D3DMAXNUMPRIMITIVES. En la versión de depuración de Direct3D, si pasa más de primitivas D3DMAXNUMPRIMITIVES, el método produce un error correctamente, al imprimir un mensaje de error en el registro de errores y devolver un valor de error a la aplicación. Por el contrario, si la aplicación produce el mismo error cuando se ejecuta con la versión comercial del tiempo de ejecución, el comportamiento no está definido. Por motivos de rendimiento, el método no valida los parámetros, lo que produce un comportamiento impredecible y completamente situacional cuando no son válidos. En algunos casos, la llamada podría funcionar y, en otros casos, podría producir un error de memoria en Direct3D. Si una llamada no válida funciona de forma coherente con una configuración de hardware determinada y una versión de DirectX, no hay ninguna garantía de que seguirá funcionando en otro hardware o con versiones posteriores de DirectX.

Si la aplicación encuentra errores inexplicados al ejecutarse con el archivo en tiempo de ejecución de Direct3D comercial, pruebe con la versión de depuración y busque con atención los casos en los que la aplicación pasa parámetros no válidos. Use el applet del panel de control de DirectX, cambie al tiempo de ejecución de depuración si es necesario y active la opción "Interrumpir en D3DError". Esta opción obligará al runtime a usar el método Windows DebugBreak para forzar que la aplicación se detenga cuando se detecte un error de aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programación Sugerencias](programming-tips.md)
</dt> </dl>

 

 
