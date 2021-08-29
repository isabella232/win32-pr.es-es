---
title: Compilar un efecto (Direct3D 11)
description: Después de crear un efecto, el siguiente paso consiste en compilar el código para comprobar si hay problemas de sintaxis.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83209db3ea32242e1eb9a40eccacc846567e3e6bc6401d74950a379fc1d24bcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046613"
---
# <a name="compile-an-effect-direct3d-11"></a>Compilar un efecto (Direct3D 11)

Después de crear un efecto, el siguiente paso consiste en compilar el código para comprobar si hay problemas de sintaxis.

Para ello, llame a una de las API de compilación ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)o [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ). Estas API invocan el compilador de fxc.exe, que compila código HLSL. Este es el motivo por el que la sintaxis del código en un efecto se parece mucho al código HLSL. (Hay algunas excepciones que se controlarán más adelante). El compilador de efectos/compilador hlsl, fxc.exe, está disponible en el SDK en la carpeta utilities para que los sombreadores (o efectos) se puedan compilar sin conexión si lo desea. Consulte la documentación para ejecutar el compilador desde la línea de comandos.

-   [Ejemplo](#example)
-   [Incluye](#includes)
-   [Búsqueda de archivos de incluir](#searching-for-include-files)
-   [Macros](#macros)
-   [Marcas de sombreador HLSL](#hlsl-shader-flags)
-   [Marcas de FX](#fx-flags)
-   [Comprobación de errores](#checking-errors)
-   [Temas relacionados](#related-topics)

## <a name="example"></a>Ejemplo

Este es un ejemplo de compilación de un archivo de efecto.


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a>Includes

Un parámetro de las API de compilación es una interfaz include. Genere uno de estos si desea incluir un comportamiento personalizado cuando el compilador lea un archivo de incluir. El compilador ejecuta este comportamiento personalizado cada vez que crea o compila un efecto (que usa el puntero include). Para implementar el comportamiento de incluir personalizado, derive una clase de la [**interfaz ID3DInclude.**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) Esto proporciona a la clase dos métodos: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) y [**Close.**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close) Implemente el comportamiento personalizado en estos métodos.

## <a name="searching-for-include-files"></a>Búsqueda de archivos de incluir

El puntero que el compilador pasa en el parámetro *pParentData* al método [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) del controlador de include podría no apuntar al contenedor que incluye el archivo de incluir que el compilador necesita para compilar el código del \# sombreador. Es decir, el compilador podría pasar **NULL** en *pParentData.* Por lo tanto, se recomienda que el controlador de include busque su propia lista de ubicaciones de incluyeción para el contenido. El controlador de include puede agregar dinámicamente nuevas ubicaciones de include a medida que recibe esas ubicaciones en las llamadas a su **método Open.**

En el ejemplo siguiente, suponga que los archivos de incluir del código del sombreador se almacenan en el *directorio somewhereelse.* Cuando el compilador llama al método [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) del controlador de incluyeción para abrir y leer el contenido de *somewhereelse \\ foo.h*, el controlador de incluye puede guardar la ubicación del directorio **somewhereelse.** Más adelante, cuando el compilador llama al método **Open** del controlador de incluyeción para abrir y leer el contenido de *bar.h*, el controlador de incluye puede buscar automáticamente *bar.h* en el directorio *somewhereelse* .


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a>Macros

La compilación de efectos también puede tomar un puntero a las macros que se definen en otra parte. Por ejemplo, supongamos que quiere modificar el efecto en BasicHLSL10 para usar dos macros: cero y una. Aquí se muestra el código de efecto que usa las dos macros.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Esta es la declaración de las dos macros.


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



Las macros son una matriz de macros terminada en NULL; donde cada macro se define mediante un [**struct DE \_ MACRO \_ SOMBREADOR D3D10.**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)

Modifique la llamada de efecto de compilación para tomar un puntero a las macros.


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a>Marcas de sombreador HLSL

Las marcas de sombreador especifican restricciones de sombreador para el compilador HLSL. Estas marcas afectan al código generado por el compilador del sombreador de las maneras siguientes:

-   Optimice el tamaño del código.
-   Incluir información de depuración, que impide el control de flujo.
-   Afecta al destino de compilación y a si un sombreador se puede ejecutar en hardware heredado.

Estas marcas se pueden combinar lógicamente si no se han especificado dos características en conflicto. Para obtener una lista de las marcas, [vea D3D10 \_ SHADER Constants](/windows/desktop/direct3d10/d3d10-shader).

## <a name="fx-flags"></a>Marcas de FX

Use estas marcas al crear un efecto para definir el comportamiento de compilación o el comportamiento del efecto en tiempo de ejecución. Para obtener una lista de las marcas, [vea D3D10 \_ EFFECT Constants](/windows/desktop/direct3d10/d3d10-effect).

## <a name="checking-errors"></a>Comprobación de errores

Si durante la compilación se produce un error, la API devuelve una interfaz que contiene los errores del compilador de efectos. Esta interfaz se denomina [**ID3DBlob.**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) No es legible directamente; sin embargo, al devolver un puntero al búfer que contiene los datos (que es una cadena), puede ver los errores de compilación.

Este ejemplo contiene un error en BasicHLSL.fx; la primera declaración de variable se produce dos veces.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Este error hace que el compilador devuelva el siguiente error, como se muestra en la siguiente captura de pantalla del ventana Inspección en Microsoft Visual Studio.

![captura de pantalla de la ventana de inspección de Visual Studio con un 0x01997fb8 error](images/effect-compile-errors-2.jpg)

Dado que el compilador devuelve el error en un puntero LPVOID, conéctelo a una cadena de caracteres en el ventana Inspección.

Este es el código que devuelve el error de la compilación con errores.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de un efecto (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 