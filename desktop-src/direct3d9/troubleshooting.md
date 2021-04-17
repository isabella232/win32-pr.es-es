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
# <a name="troubleshooting-direct3d-9"></a>Solución de problemas (Direct3D 9)

En este tema se enumeran las categorías comunes de problemas que pueden surgir al escribir aplicaciones de Direct3D y cómo evitarlos.

## <a name="device-creation"></a>Creación de dispositivos

Si se produce un error en la aplicación durante la creación del dispositivo, compruebe los siguientes errores comunes.

-   Asegúrese de comprobar las capacidades del dispositivo, especialmente las profundidades de representación.
-   Examine el código de error. D3DERR \_ OUTOFVIDEOMEMORY siempre es posible.
-   Use las bibliotecas de vínculos dinámicos (dll) de DirectX de depuración y revise los mensajes de salida en el depurador.

## <a name="using-lit-vertices"></a>Usar vértices iluminados

Las aplicaciones que usan vértices Lit deben deshabilitar el motor de iluminación de Direct3D estableciendo el \_ Estado de representación de iluminación D3DRS en **false**. De forma predeterminada, cuando se habilita la iluminación, el sistema establece el color de cualquier vértice que no contenga un vector normal en 0 (negro), incluso si el vértice de entrada contenía un valor de color distinto de cero. Dado que los vértices iluminados no, por su naturaleza, contienen un vértice normal, cualquier información de color pasada a Direct3D se pierde durante la representación si está habilitado el motor de iluminación.

Obviamente, el color de vértice es importante para cualquier aplicación que realice su propia iluminación. Para evitar que el sistema imponga los valores predeterminados, asegúrese de establecer la \_ iluminación D3DRS en **false**.

Si la aplicación se ejecuta pero no hay nada visible, busque los siguientes errores comunes.

-   Asegúrese de que los triángulos no se degeneran.
-   Asegúrese de que los triángulos no se seleccionan.
-   Asegúrese de que las transformaciones son coherentes internamente.
-   Compruebe la configuración de la ventanilla para asegurarse de que permite que se vean los triángulos.

## <a name="debugging"></a>Depuración

La depuración de una aplicación Direct3D puede ser desafiante. Pruebe las siguientes técnicas, además de comprobar todos los valores devueltos, una parte de consejos especialmente importante en la programación de Direct3D, que depende de implementaciones de hardware muy diferentes.

-   Cambie a dll de depuración.
-   Fuerce un dispositivo solo de software, desactivando la aceleración de hardware incluso cuando esté disponible.
-   Fuerce las superficies en la memoria del sistema.
-   Cree una opción para ejecutarla en una ventana, de modo que pueda usar un depurador integrado.

La segunda y tercera opciones de esta lista pueden ayudarle a evitar el bloqueo de Win16 que, de lo contrario, puede hacer que el depurador se bloquee.

Además, intente agregar las siguientes entradas a Win.ini.


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a>Inicialización de Borland Floating-Point

Los compiladores de Borland notifican las excepciones de punto flotante de una manera que es incompatible con Direct3D. Para solucionar este problema, incluya un \_ controlador de excepciones de matherr similar al siguiente:


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

Por motivos de rendimiento, la versión de depuración del tiempo de ejecución del modo inmediato de Direct3D realiza más validaciones de parámetros que la versión comercial, que a veces no realiza ninguna validación. Esto permite que las aplicaciones realicen una depuración sólida con el componente de tiempo de ejecución de depuración más lento antes de usar la versión comercial más rápida para el ajuste del rendimiento y la versión final.

Aunque varios métodos de modo inmediato de Direct3D imponen límites a los valores que pueden aceptar, a menudo estos límites solo se comprueban y aplican mediante la versión de depuración del tiempo de ejecución del modo inmediato de Direct3D. Las aplicaciones deben cumplir estos límites, o bien se pueden producir resultados imprevisibles y no deseados cuando se ejecutan en la versión comercial de Direct3D. Por ejemplo, el método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) acepta un parámetro (PrimitiveCount) que indica el número de primitivas que representará el método. El método solo puede aceptar valores entre 0 y D3DMAXNUMPRIMITIVES. En la versión de depuración de Direct3D, si se pasan más de D3DMAXNUMPRIMITIVES primitivos, se produce un error en el método correctamente, se imprime un mensaje de error en el registro de errores y se devuelve un valor de error a la aplicación. Por el contrario, si la aplicación realiza el mismo error cuando se ejecuta con la versión comercial del tiempo de ejecución, el comportamiento es indefinido. Por motivos de rendimiento, el método no valida los parámetros, lo que da lugar a un comportamiento impredecible y completamente inexistente cuando no son válidos. En algunos casos, la llamada podría funcionar y, en otros casos, podría provocar un error de memoria en Direct3D. Si una llamada no válida funciona constantemente con una configuración de hardware determinada y la versión de DirectX, no hay ninguna garantía de que siga funcionando en otro hardware o con versiones posteriores de DirectX.

Si la aplicación detecta errores no explicados cuando se ejecuta con el archivo de tiempo de ejecución de Direct3D comercial, pruebe con la versión de depuración y Mire atentamente los casos en los que la aplicación pase parámetros no válidos. Use el applet del panel de control de DirectX, cambie al tiempo de ejecución de depuración si es necesario y active la opción "interrumpir en D3DError". Esta opción forzará al tiempo de ejecución a utilizar el método DebugBreak de Windows para forzar que la aplicación se detenga cuando se detecte un error de aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sugerencias de programación](programming-tips.md)
</dt> </dl>

 

 
