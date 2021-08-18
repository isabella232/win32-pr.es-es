---
title: Compilación sin conexión
description: La herramienta de compilador de efectos (fxc.exe) está diseñada para la compilación sin conexión de sombreadores HLSL.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- fxc, compilación sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a15d3a71dbfb79541a75bd38cb28140d832b45e75a88a52b2d0c8988865f12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406335"
---
# <a name="offline-compiling"></a>Compilación sin conexión

La herramienta de compilador de efectos (fxc.exe) está diseñada para la compilación sin conexión de sombreadores HLSL.

## <a name="compiling-with-the-current-compiler"></a>Compilación con el compilador actual

Los modelos de sombreador admitidos por el compilador actual se muestran en [Perfiles](dx-graphics-tools-fxc-syntax.md). En este ejemplo se compila un sombreador de píxeles para el destino del modelo de sombreador 5.1.

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

En este ejemplo:

-   ps \_ 5 \_ 1 es el perfil de destino.
-   PixelShader1.fxc es el archivo de objeto de salida que contiene el sombreador compilado.
-   PixelShader1.hlsl es el origen.

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

Las opciones de depuración incluyen opciones adicionales para deshabilitar las optimizaciones del compilador (Od) y habilitar la información de depuración (Zi), como números de línea y símbolos.

Para obtener una lista completa de las opciones de línea de comandos, vea la [página Sintaxis.](dx-graphics-tools-fxc-syntax.md)

## <a name="compiling-with-the-legacy-compiler"></a>Compilación con el compilador heredado

A partir de Direct3D 10, ya no se admiten algunos modelos de sombreador. Estos incluyen modelos de sombreador de píxeles: ps \_ \_ 1 1, ps \_ \_ 2, ps \_ 1 3 y ps \_ \_ 1 \_ 4 que admiten recursos muy limitados y dependen del hardware. El compilador se ha rediseñado con el modelo de sombreador 2 (o superior) que permite mayores eficiencias con la compilación. Por supuesto, esto requerirá que se ejecute en hardware que admita los modelos de sombreador 2 y superiores.

Tenga en cuenta también que debe consultar las notas de la versión del SDK asociadas a la versión del compilador de FXC para conocer el comportamiento afectado por el modificador /Gec.

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a>Uso de la herramienta del compilador de efectos en un subproceso

Si fxc.exe genera una aplicación como un subproceso, es importante asegurarse de que la aplicación comprueba y lee los datos de las canalizaciones de salida o de error que se pasan a la función CreateProcess. Si la aplicación solo espera a que finalice el subproceso y una de las canalizaciones se llena, el subproceso nunca finalizará.

El código de ejemplo siguiente muestra la espera en un subproceso y la lectura de las canalizaciones de salida y error asociadas al subproceso. El contenido de la matriz corresponde a los identificadores del subproceso, la canalización para stdout y la `WaitHandles` canalización para stderr.

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

Para obtener información adicional sobre cómo generar un proceso, consulte la página de referencia [**de CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).

## <a name="related-topics"></a>Temas relacionados

* [Herramienta Del compilador de efectos](fxc.md)