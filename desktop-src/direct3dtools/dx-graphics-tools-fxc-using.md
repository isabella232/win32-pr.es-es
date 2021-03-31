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
# <a name="offline-compiling"></a>Compilación sin conexión

La herramienta de compilador de efectos (fxc.exe) está diseñada para la compilación sin conexión de los sombreadores HLSL.

## <a name="compiling-with-the-current-compiler"></a>Compilar con el compilador actual

Los modelos de sombreador admitidos por el compilador actual se muestran en [perfiles](dx-graphics-tools-fxc-syntax.md). En este ejemplo se compila un sombreador de píxeles para el destino del modelo de sombreador 5,1.

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

En este ejemplo:

-   PS \_ 5 \_ 1 es el perfil de destino.
-   PixelShader1. FXC es el archivo de objeto de salida que contiene el sombreador compilado.
-   PixelShader1. HLSL es el origen.

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

Las opciones de depuración incluyen opciones adicionales para deshabilitar las optimizaciones del compilador (OD) y habilitar la información de depuración (Zi) como los números de línea y los símbolos.

Para obtener una lista completa de las opciones de línea de comandos, vea la página [Sintaxis](dx-graphics-tools-fxc-syntax.md) .

## <a name="compiling-with-the-legacy-compiler"></a>Compilar con el compilador heredado

A partir de Direct3D 10, ya no se admiten algunos modelos de sombreador. Estos incluyen modelos de sombreador de píxeles: PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 y PS \_ 1 \_ 4, que admiten recursos muy limitados y dependen del hardware. El compilador se ha rediseñado con el modelo de sombreador 2 (o superior), lo que permite mayores eficiencias con la compilación. Esto requiere que se ejecute en hardware que admita los modelos de sombreador 2 y superiores.

Tenga en cuenta también que debe consultar las notas de la versión del SDK asociadas a su versión del compilador FXC para el comportamiento afectado por el modificador/GEC.

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a>Usar la herramienta de compilador de efectos en un subproceso

Si una aplicación genera fxc.exe como subproceso, es importante asegurarse de que la aplicación comprueba y Lee los datos de los conductos de salida o de error pasados a la función CreateProcess. Si la aplicación solo espera a que finalice el subproceso y una de las canalizaciones se llena, el subproceso nunca finalizará.

En el ejemplo de código siguiente se muestra la espera en un subproceso y la lectura de las canalizaciones de salida y de error adjuntas al subproceso. El contenido de la `WaitHandles` matriz se corresponde con los identificadores del subproceso, la canalización de stdout y la canalización para stderr.

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

Para obtener información adicional sobre cómo generar un proceso, vea la página de referencia de [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).

## <a name="related-topics"></a>Temas relacionados

* [Efecto: herramienta de compilador](fxc.md)