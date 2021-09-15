---
title: Usar sombreadores en Direct3D 10
description: Usar sombreadores en Direct3D 10
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0d6212851e4603aac4db7ec85dd20714dc87774
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466945"
---
# <a name="using-shaders-in-direct3d-10"></a>Usar sombreadores en Direct3D 10

La canalización tiene tres fases de sombreador y cada una de ellas se programa con un sombreador HLSL. Todos los sombreadores de Direct3D 10 se escriben en HLSL y tienen como destino el modelo de sombreador 4.


Diferencias entre Direct3D 9 y Direct3D 10:

- A diferencia de los modelos de sombreador de Direct3D 9 que podrían crearse en un lenguaje de ensamblado intermedio, los sombreadores del modelo de sombreador 4.0 solo se han creado en HLSL. Todavía se admite la compilación sin conexión de sombreadores en el código de bytes que se puede consumir del dispositivo y se recomienda para la mayoría de los escenarios.



 

En este ejemplo solo se usa un sombreador de vértices. Dado que todos los sombreadores se compilan a partir del núcleo común del sombreador, aprender a usar un sombreador de vértices es muy similar al uso de un sombreador de geometría o píxeles.

Una vez que haya creado un sombreador HLSL (en este ejemplo se usa el sombreador de vértices HLSLWithoutFX.vsh), deberá prepararlo para la fase de canalización concreta que lo usará. Para ello, debe:

-   [Compilar un sombreador](#compile-a-shader)
-   [Crear un objeto de sombreador](#create-a-shader-object)
-   [Establecer el objeto Shader](#set-the-shader-object)
-   [Repetir para las tres fases del sombreador](#repeat-for-all-3-shader-stages)

Estos pasos deben repetirse para cada sombreador de la canalización.

## <a name="compile-a-shader"></a>Compilar un sombreador

El primer paso consiste en compilar el sombreador para comprobar que ha codificado correctamente las instrucciones HLSL. Para ello, se llama a D3D10CompileShader y se le suministran varios parámetros, como se muestra aquí:


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



Esta función toma los parámetros siguientes:

-   Nombre del archivo ( y longitud de la cadena de nombre en bytes ) que contiene el sombreador. En este ejemplo solo se usa un sombreador de vértices (en el archivo HLSLWithoutFX.vsh, donde la extensión de archivo .vsh es una abreviatura del sombreador de vértices).
-   Nombre de la función de sombreador. En este ejemplo se compila un sombreador de vértices a partir de la función Ripple que toma una sola entrada y devuelve una estructura de salida (la función es del ejemplo HLSLWithoutFX):
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   Puntero a todas las macros utilizadas por el sombreador. Use D3D10 SHADER MACRO para ayudar a definir las macros; simplemente cree una cadena de nombre que contenga todos los nombres de macro (con cada nombre separado por un espacio) y una cadena de definición (con cada cuerpo de macro separado por \_ \_ un espacio). Ambas cadenas deben terminar en NULL.
-   Puntero a cualquier otro archivo que necesite incluir para que los sombreadores se compilen. Esto usa la interfaz ID3D10Include que tiene dos métodos implementados por el usuario: Open y Close. Para que esto funcione, deberá implementar el cuerpo de los métodos Open y Close. En el método Open, agregue el código que usaría para abrir los archivos de incluir que desee; en la función Cerrar, agregue el código para cerrar los archivos cuando haya terminado con ellos.
-   Nombre de la función de sombreador que se compilará. Este sombreador compila la función Ripple.
-   Perfil de sombreador de destino al compilar. Puesto que puede compilar una función en un sombreador de vértices, geometría o píxeles, el perfil indica al compilador qué tipo de sombreador y con qué modelo de sombreador comparar el código.
-   Marcas del compilador del sombreador. Estas marcas le informan al compilador qué información se debe colocar en la salida compilada y cómo desea optimizar el código de salida: para la velocidad, para la depuración, etc. Consulte [Constantes de efecto (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) para obtener una lista de las marcas disponibles. El ejemplo contiene código que se puede usar para establecer los valores de marca del compilador para el proyecto; se trata principalmente de una pregunta sobre si desea o no generar información de depuración.
-   Puntero al búfer que contiene el código del sombreador compilado. El búfer también contiene cualquier información de tabla de símbolos y depuración incrustada solicitada por las marcas del compilador.
-   Puntero a un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación, que son los mismos mensajes que vería en la salida de depuración si estuviera ejecutando el depurador mientras compilaba el sombreador. **NULL** es un valor aceptable cuando no desea que se devuelvan los errores a un búfer.

Si el sombreador se compila correctamente, se devuelve un puntero al código del sombreador como una interfaz ID3D10Blob. Se denomina interfaz blob porque el puntero se encuentra en una ubicación en memoria que está integrada por una matriz de DWORD. La interfaz se proporciona para que pueda obtener un puntero al sombreador compilado que necesitará en el paso siguiente.

A partir del SDK de diciembre de 2006, el compilador HLSL de DirectX 10 es ahora el compilador predeterminado en DirectX 9 y DirectX 10. Vea [Effect-Compiler Tool para](/windows/desktop/direct3dtools/fxc) obtener más información.

### <a name="get-a-pointer-to-a-compiled-shader"></a>Obtener un puntero a un sombreador compilado

Varios métodos de API requieren un puntero a un sombreador compilado. Este argumento se suele *denominar pShaderBytecode porque* apunta a un sombreador compilado representado como una secuencia de códigos de bytes. Para obtener un puntero a un sombreador compilado, compile primero el sombreador llamando a [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) o a una función similar. Si la compilación se realiza correctamente, el sombreador compilado se devuelve en una [**interfaz ID3D10Blob.**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) Por último, use [**el método GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) para devolver el puntero.

## <a name="create-a-shader-object"></a>Crear un objeto de sombreador

Una vez compilado el sombreador, llame a CreateVertexShader para crear el objeto de sombreador:


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



Para crear el objeto de sombreador, pase el puntero al sombreador compilado a CreateVertexShader. Puesto que antes tenía que compilar correctamente el sombreador, esta llamada casi seguro pasará, a menos que tenga un problema de memoria en el equipo.

Puede crear tantos objetos de sombreador como quiera y simplemente mantener punteros a ellos. Este mismo mecanismo funciona para sombreadores de geometría y píxeles suponiendo que coincida con los perfiles de sombreador (cuando se llama al método de compilación) con los nombres de interfaz (cuando se llama al método create).

## <a name="set-the-shader-object"></a>Establecer el objeto Shader

El último paso es establecer el sombreador en la fase de canalización. Dado que hay tres fases de sombreador en la canalización, deberá realizar tres llamadas API, una para cada fase.


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



La llamada a VSSetShader toma el puntero al sombreador de vértices creado en el paso 1. Esto establece el sombreador en el dispositivo. La fase del sombreador de vértices ahora se inicializa con su código de sombreador de vértices, lo único que queda es inicializar cualquier variable de sombreador.

## <a name="repeat-for-all-3-shader-stages"></a>Repetir para las tres fases del sombreador

Repita este mismo conjunto de pasos para crear cualquier sombreador de vértices o píxeles o incluso un sombreador de geometría que genere el sombreador de píxeles.

## <a name="related-topics"></a>Temas relacionados

[Compilación de sombreadores](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

