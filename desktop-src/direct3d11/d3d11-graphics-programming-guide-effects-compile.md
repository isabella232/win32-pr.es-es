---
title: Compilar un efecto (Direct3D 11)
description: Una vez creado un efecto, el paso siguiente consiste en compilar el código para comprobar si hay problemas de sintaxis.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995372"
---
# <a name="compile-an-effect-direct3d-11"></a>Compilar un efecto (Direct3D 11)

Una vez creado un efecto, el paso siguiente consiste en compilar el código para comprobar si hay problemas de sintaxis.

Para ello, llame a una de las API de compilación ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)o [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ). Estas API invocan el efecto compilador fxc.exe, que compila el código HLSL. Este es el motivo por el que la sintaxis del código de un efecto es muy parecida a la del código HLSL. (Hay algunas excepciones que se tratarán más adelante). El compilador de efecto compilador o HLSL, fxc.exe, está disponible en el SDK en la carpeta Utilities para que los sombreadores (o efectos) se puedan compilar sin conexión si así lo desea. Consulte la documentación para ejecutar el compilador desde la línea de comandos.

-   [Ejemplo](#example)
-   [Presenta](#includes)
-   [Buscar archivos de inclusión](#searching-for-include-files)
-   [Macros](#macros)
-   [Marcas de sombreador HLSL](#hlsl-shader-flags)
-   [Marcas FX](#fx-flags)
-   [Comprobar errores](#checking-errors)
-   [Temas relacionados](#related-topics)

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo de cómo compilar un archivo de efectos.


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a>Includes

Un parámetro de las API de compilación es una interfaz de inclusión. Genere uno de estos si desea incluir un comportamiento personalizado cuando el compilador lea un archivo de inclusión. El compilador ejecuta este comportamiento personalizado cada vez que crea o compila un efecto (que usa el puntero include). Para implementar el comportamiento de inclusión personalizado, derive una clase de la interfaz [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) . Esto proporciona a la clase dos métodos: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) y [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close). Implemente el comportamiento personalizado en estos métodos.

## <a name="searching-for-include-files"></a>Buscar archivos de inclusión

El puntero que el compilador pasa en el parámetro *pParentData* al método [**abierto**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) del controlador de inclusión podría no señalar al contenedor que incluye el \# archivo de inclusión que el compilador necesita para compilar el código del sombreador. Es decir, el compilador podría pasar **null** en *pParentData*. Por lo tanto, se recomienda que el controlador de inclusión busque en su propia lista de ubicaciones de inclusión para el contenido. El controlador de inclusión puede agregar dinámicamente nuevas ubicaciones de inclusión al recibir esas ubicaciones en llamadas a su método **abierto** .

En el ejemplo siguiente, suponga que los archivos de inclusión del código del sombreador se almacenan en el directorio *somewhereelse* . Cuando el compilador llama al método [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) del controlador de inclusión para abrir y leer el contenido de *somewhereelse \\ foo. h*, el controlador de inclusión puede guardar la ubicación del directorio **somewhereelse** . Más adelante, cuando el compilador llama al método **Open** del controlador de inclusión para abrir y leer el contenido de *bar. h*, el controlador de inclusión puede buscar automáticamente en el directorio *somewhereelse* de *bar. h*.


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a>Macros

La compilación del efecto también puede tomar un puntero a las macros que se definen en otro lugar. Por ejemplo, supongamos que desea modificar el efecto en BasicHLSL10 para usar dos macros: cero y uno. Aquí se muestra el código de efecto que usa las dos macros.


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



Las macros son una matriz terminada en NULL de macros; donde cada macro se define mediante un struct [**de \_ \_ macros de sombreador D3D10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .

Modifique la llamada al efecto compilar para que tome un puntero a las macros.


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a>Marcas de sombreador HLSL

Las marcas del sombreador especifican las restricciones del sombreador en el compilador de HLSL. Estas marcas afectan al código generado por el compilador del sombreador de las siguientes maneras:

-   Optimizar el tamaño del código.
-   Incluye información de depuración, que impide el control de flujo.
-   Afecta al destino de compilación y si un sombreador puede ejecutarse en hardware heredado.

Estas marcas se pueden combinar lógicamente si no se han especificado dos características conflictivas. Para obtener una lista de las marcas, vea [D3D10 ( \_ constantes del sombreador](/windows/desktop/direct3d10/d3d10-shader)).

## <a name="fx-flags"></a>Marcas FX

Use estas marcas cuando cree un efecto para definir el comportamiento de la compilación o del efecto en tiempo de ejecución. Para obtener una lista de las marcas, consulte [ \_ constantes Effect D3D10](/windows/desktop/direct3d10/d3d10-effect).

## <a name="checking-errors"></a>Comprobar errores

Si durante la compilación se produce un error, la API devuelve una interfaz que contiene los errores del compilador de efectos. Esta interfaz se denomina [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)). No se puede leer directamente; sin embargo, al devolver un puntero al búfer que contiene los datos (que es una cadena), puede ver los errores de compilación.

Este ejemplo contiene un error en BasicHLSL. FX, la primera declaración de variable aparece dos veces.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Este error hace que el compilador devuelva el siguiente error, como se muestra en la siguiente captura de pantalla del ventana Inspección en Microsoft Visual Studio.

![captura de pantalla de la ventana Inspección de Visual Studio con un error 0x01997fb8](images/effect-compile-errors-2.jpg)

Dado que el compilador devuelve el error en un puntero LPVOID, conviértalo en una cadena de caracteres en el ventana Inspección.

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

[Representar un efecto (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 