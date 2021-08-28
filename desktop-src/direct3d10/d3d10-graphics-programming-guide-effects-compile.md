---
description: Una vez que se ha generado un efecto, el primer paso es compilar el código para comprobar si hay problemas de sintaxis.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Compilación de un efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e0c4364fab67b0e0e7c97b7478a023f6394b5515e6f1d16cf2d352172af6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128437"
---
# <a name="compile-an-effect-direct3d-10"></a>Compilación de un efecto (Direct3D 10)

Una vez que se ha generado un efecto, el primer paso es compilar el código para comprobar si hay problemas de sintaxis. Para ello, se llama a una de las API de compilación (como D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory). Estas API invocan el compilador de fxc.exe que es el compilador que se usa para compilar código HLSL. Este es el motivo por el que la sintaxis del código en un efecto se parece mucho al código HLSL (hay algunas excepciones que se controlarán más adelante). Por cierto, el compilador de efectos/compilador hlsl (fxc.exe) está en el SDK de la carpeta utilities para que pueda compilar los sombreadores (o efectos) sin conexión si lo desea. Consulte la documentación para ejecutar el compilador desde la línea de comandos.

-   [Incluye](#includes)
-   [Macros](#macros)
-   [Marcas de sombreador HLSL](#hlsl-shader-flags)
-   [Marcas de FX](#fx-flags)
-   [Comprobación de errores](#checking-errors)
-   [Temas relacionados](#related-topics)

Este es un ejemplo de compilación de un archivo de efecto (del ejemplo BasicHLSL10).


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a>Includes

Un parámetro es una interfaz include. Genere uno de estos si desea incluir un comportamiento personalizado al leer un archivo de incluir. Este comportamiento personalizado se ejecuta cada vez que se crea un efecto (que usa el puntero include) o cuando se compila un efecto (que usa el puntero include). Para implementar el comportamiento de incluir personalizado, derive una clase de la interfaz Include. Esto proporciona a la clase dos métodos: Open y Close. Implemente el comportamiento personalizado en los métodos Open y Close.

## <a name="macros"></a>Macros

La compilación de efectos también puede tomar un puntero a las macros que se definen en otra parte. Por ejemplo, suponga que va a modificar el efecto en BasicHLSL10 para usar dos macros: cero y una. Aquí se muestra el código de efecto que usa las dos macros.


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



Las macros son una matriz terminada en NULL de macros; donde cada macro se define con una estructura [**DE \_ MACRO \_ SOMBREADOR D3D.**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)

Por último, modifique la llamada de efecto de compilación para tomar un puntero a las macros.


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a>Marcas de sombreador HLSL

Las marcas de sombreador especifican restricciones de sombreador para el compilador HLSL. Estas marcas afectan al código generado por el compilador del sombreador, lo que incluye:

-   Consideraciones de tamaño: optimice el código.
-   Consideraciones de depuración: incluir información de depuración, evitar el control de flujo.
-   Consideraciones de hardware: el destino de compilación y si un sombreador se puede ejecutar o no en hardware heredado.

En general, estas marcas se pueden combinar lógicamente, suponiendo que no se han especificado dos características en conflicto. Para obtener una lista de las marcas, [vea Constantes de efecto (Direct3D 10).](d3d10-graphics-reference-effect-constants.md)

## <a name="fx-flags"></a>Marcas de FX

Estas marcas se usan al crear un efecto para definir el comportamiento de compilación o el comportamiento del efecto en tiempo de ejecución. Para obtener una lista de las marcas, [vea Constantes de efecto (Direct3D 10).](d3d10-graphics-reference-effect-constants.md)

## <a name="checking-errors"></a>Comprobación de errores

Si durante la compilación se produce un error, la API devuelve una interfaz que contiene los errores devueltos por el compilador de efectos. Esta interfaz se denomina ID3D10Blob. Sin embargo, no es legible directamente devolviendo un puntero al búfer que contiene los datos (que es una cadena), puede ver los errores de compilación.

En este ejemplo, se introdujo un error en el efecto BasicHLSL.fx copiando la primera declaración de variable dos veces.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Este error hizo que el compilador devolvía el siguiente error, como se muestra en la siguiente captura de pantalla de la ventana de Microsoft Visual Studio.

![captura de pantalla de la ventana de inspección de Visual Studio](images/effect-compile-errors-2.jpg)

Puesto que el error se devuelve en un puntero LPVOID, conéctelo a una cadena de caracteres en la ventana de reloj.

Este es el código usado para devolver el error de la compilación con errores.


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

[Representación de un efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



