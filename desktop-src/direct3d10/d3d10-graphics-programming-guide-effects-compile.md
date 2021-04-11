---
description: Una vez creado un efecto, el primer paso consiste en compilar el código para comprobar si hay problemas de sintaxis.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Compilación de un efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274890"
---
# <a name="compile-an-effect-direct3d-10"></a>Compilación de un efecto (Direct3D 10)

Una vez creado un efecto, el primer paso consiste en compilar el código para comprobar si hay problemas de sintaxis. Esto se hace mediante una llamada a una de las API de compilación (como D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory). Estas API invocan el compilador de efecto fxc.exe que es el compilador que se usa para compilar código HLSL. Este es el motivo por el que la sintaxis del código de un efecto es muy similar a la del código HLSL (hay algunas excepciones que se tratarán más adelante). Por la forma, el compilador de efectos compilador/HLSL (fxc.exe) está en el SDK de la carpeta Utilities para que pueda compilar los sombreadores (o efectos) sin conexión si lo desea. Consulte la documentación para ejecutar el compilador desde la línea de comandos.

-   [Presenta](#includes)
-   [Macros](#macros)
-   [Marcas de sombreador HLSL](#hlsl-shader-flags)
-   [Marcas FX](#fx-flags)
-   [Comprobar errores](#checking-errors)
-   [Temas relacionados](#related-topics)

A continuación se muestra un ejemplo de cómo compilar un archivo de efectos (desde el ejemplo BasicHLSL10).


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a>Includes

Un parámetro es una interfaz include. Genere uno de estos si desea incluir un comportamiento personalizado al leer un archivo de inclusión. Este comportamiento personalizado se ejecuta cada vez que se crea un efecto (que usa el puntero include) o cuando se compila un efecto (que usa el puntero include). Para implementar el comportamiento de inclusión personalizado, derive una clase de la interfaz include. Esto proporciona a los dos métodos de la clase: abrir y cerrar. Implemente el comportamiento personalizado en los métodos de apertura y cierre.

## <a name="macros"></a>Macros

La compilación del efecto también puede tomar un puntero a las macros que se definen en otro lugar. Por ejemplo, supongamos que va a modificar el efecto en BasicHLSL10 para usar dos macros: cero y uno. Aquí se muestra el código de efecto que usa las dos macros.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Esta es la declaración de las dos macros.


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



Las macros son una matriz terminada en NULL de macros; donde cada macro se define con un struct de [**\_ \_ macros de sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .

Por último, modifique la llamada al efecto compilar para que tome un puntero a las macros.


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a>Marcas de sombreador HLSL

Las marcas del sombreador especifican las restricciones del sombreador en el compilador de HLSL. Estas marcas afectan al código generado por el compilador del sombreador, incluidos:

-   Consideraciones de tamaño: optimice el código.
-   Consideraciones sobre depuración: incluir información de depuración, evitar el control de flujo.
-   Consideraciones de hardware: el destino de compilación y si un sombreador puede ejecutarse en hardware heredado.

En general, estas marcas se pueden combinar lógicamente, suponiendo que no se han especificado dos características conflictivas. Para obtener una lista de las marcas [, vea constantes de efecto (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="fx-flags"></a>Marcas FX

Estas marcas se usan al crear un efecto para definir el comportamiento de la compilación o del efecto en tiempo de ejecución. Para obtener una lista de las marcas [, vea constantes de efecto (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="checking-errors"></a>Comprobar errores

Si durante la compilación se produce un error, la API devuelve una interfaz que contiene los errores devueltos por el compilador de efectos. Esta interfaz se denomina ID3D10Blob. Sin embargo, no se puede leer directamente; si se devuelve un puntero al búfer que contiene los datos (que es una cadena), se pueden ver los errores de compilación.

En este ejemplo, se ha introducido un error en el efecto BasicHLSL. FX mediante la copia de la primera declaración de variable dos veces.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Este error hizo que el compilador devolvera el siguiente error, como se muestra en la siguiente captura de pantalla de la ventana Inspección en Microsoft Visual Studio.

![captura de pantalla de la ventana Inspección de Visual Studio](images/effect-compile-errors-2.jpg)

Dado que el error se devuelve en un puntero LPVOID, conviértalo en una cadena de caracteres en la ventana Inspección.

Este es el código que se usa para devolver el error de la compilación con errores.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar un efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



