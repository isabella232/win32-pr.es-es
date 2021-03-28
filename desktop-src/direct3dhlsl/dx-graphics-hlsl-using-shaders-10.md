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
ms.openlocfilehash: 0e19275532ce8fd034813d8574f6bdc04d72f966
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104358989"
---
# <a name="using-shaders-in-direct3d-10"></a>Usar sombreadores en Direct3D 10

La canalización tiene tres fases del sombreador y cada una se programa con un sombreador HLSL. Todos los sombreadores de Direct3D 10 están escritos en HLSL y tienen como destino el modelo de sombreador 4.



|                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10:<br/> A diferencia de los modelos de sombreador de Direct3D 9 que podrían crearse en un lenguaje de ensamblado intermedio, los sombreadores de modelo de sombreador 4,0 solo se crean en HLSL. Todavía se admite la compilación sin conexión de los sombreadores en código de bytes consumible por dispositivo y se recomienda para la mayoría de los escenarios.<br/> |



 

En este ejemplo se usa solo un sombreador de vértices. Dado que todos los sombreadores se crean a partir de la base de sombreador común, aprender a usar un sombreador de vértices es muy similar al uso de una geometría o un sombreador de píxeles.

Una vez que haya creado un sombreador HLSL (en este ejemplo se usa el sombreador de vértices HLSLWithoutFX. VSH), deberá prepararlo para la fase de canalización concreta que lo usará. Para ello, debe hacer lo siguiente:

-   [Compilar un sombreador](#compile-a-shader)
-   [Crear un objeto de sombreador](#create-a-shader-object)
-   [Establecimiento del objeto de sombreador](#set-the-shader-object)
-   [Repetir para las tres fases del sombreador](#repeat-for-all-3-shader-stages)

Estos pasos deben repetirse para cada sombreador de la canalización.

## <a name="compile-a-shader"></a>Compilar un sombreador

El primer paso consiste en compilar el sombreador para comprobar que ha codificado las instrucciones de HLSL correctamente. Esto se hace llamando a D3D10CompileShader y proporcionando varios parámetros, como se muestra aquí:


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



Esta función toma los parámetros siguientes:

-   El nombre del archivo (y la longitud de la cadena de nombre en bytes) que contiene el sombreador. En este ejemplo solo se usa un sombreador de vértices (en el archivo HLSLWithoutFX. VSH de archivo donde la extensión de archivo. VSH es una abreviatura del sombreador de vértices).
-   Nombre de la función de sombreador. En este ejemplo se compila un sombreador de vértices de la función rizo que toma una sola entrada y devuelve un struct de salida (la función es del ejemplo HLSLWithoutFX):
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   Puntero a todas las macros utilizadas por el sombreador. Use \_ \_ la macro D3D10 Shader para ayudar a definir las macros; simplemente cree una cadena de nombre que contenga todos los nombres de macro (con cada nombre separado por un espacio) y una cadena de definición (con cada cuerpo de macro separado por un espacio). Ambas cadenas deben terminar en NULL.
-   Un puntero a cualquier otro archivo que se necesite para obtener los sombreadores que se van a compilar. Usa la interfaz ID3D10Include, que tiene dos métodos implementados por el usuario: abrir y cerrar. Para realizar este trabajo, debe implementar el cuerpo de los métodos Open y Close; en el método Open, agregue el código que desea utilizar para abrir los archivos de inclusión que desee, en la función Close agregue el código para cerrar los archivos cuando haya terminado con ellos.
-   Nombre de la función de sombreador que se va a compilar. Este sombreador compila la función Ripple.
-   Perfil del sombreador al que se va a compilar. Dado que puede compilar una función en un sombreador de píxeles, geometría o vértice, el perfil indica al compilador qué tipo de sombreador y en qué modelo de sombreador comparar el código.
-   Marcas de compilador de sombreador. Estas marcas indican al compilador qué información debe incluir en la salida compilada y cómo desea optimizar el código de salida: para la velocidad, para la depuración, etc. Vea [constantes de efecto (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) para obtener una lista de las marcas disponibles. El ejemplo contiene código que se puede usar para establecer los valores de la marca del compilador para el proyecto; esto es principalmente una pregunta sobre si se desea o no generar información de depuración.
-   Puntero al búfer que contiene el código del sombreador compilado. El búfer también contiene cualquier información de la tabla de símbolos y depuración insertada solicitada por las marcas del compilador.
-   Un puntero a un búfer que contiene una lista de errores y advertencias encontrados durante la compilación, que son los mismos mensajes que se verán en la salida de depuración si se estaba ejecutando el depurador mientras se compilaba el sombreador. **Null** es un valor aceptable cuando no se desea que los errores se devuelvan a un búfer.

Si el sombreador se compila correctamente, se devuelve un puntero al código del sombreador como una interfaz ID3D10Blob. Se denomina interfaz de blobs porque el puntero está en una ubicación de memoria que se compone de una matriz de DWORD. La interfaz se proporciona para que pueda obtener un puntero al sombreador compilado que necesitará en el paso siguiente.

A partir del SDK de diciembre de 2006, el compilador de HLSL de DirectX 10 es ahora el compilador predeterminado en DirectX 9 y DirectX 10. Consulte [herramienta de compilador de efectos](/windows/desktop/direct3dtools/fxc) para más información.

### <a name="get-a-pointer-to-a-compiled-shader"></a>Obtener un puntero a un sombreador compilado

Varios métodos de API requieren un puntero a un sombreador compilado. Este argumento se denomina normalmente *pShaderBytecode* porque apunta a un sombreador compilado representado como una secuencia de códigos de bytes. Para obtener un puntero a un sombreador compilado, primero compile el sombreador llamando a [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) o a una función similar. Si la compilación se realiza correctamente, el sombreador compilado se devuelve en una interfaz [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) . Por último, use el método [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) para devolver el puntero.

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



Para crear el objeto de sombreador, pase el puntero al sombreador compilado en CreateVertexShader. Como antes tenía que compilar el sombreador correctamente, esta llamada se realizará casi con toda certeza, a menos que tenga un problema de memoria en el equipo.

Puede crear tantos objetos de sombreador como desee y simplemente mantener punteros a ellos. Este mismo mecanismo funciona para los sombreadores de píxeles y de geometría, siempre que se haga coincidir los perfiles del sombreador (cuando se llama al método compile) con los nombres de interfaz (cuando se llama al método Create).

## <a name="set-the-shader-object"></a>Establecimiento del objeto de sombreador

El último paso es establecer el sombreador en la fase de canalización. Dado que hay tres fases del sombreador en la canalización, tendrá que realizar tres llamadas API, una para cada fase.


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



La llamada a VSSetShader toma el puntero al sombreador de vértices creado en el paso 1. Esto establece el sombreador en el dispositivo. La fase del sombreador de vértices se inicializa ahora con el código del sombreador de vértices; todo lo que queda es inicializar las variables de sombreador.

## <a name="repeat-for-all-3-shader-stages"></a>Repetir para las tres fases del sombreador

Repita este mismo conjunto de pasos para compilar cualquier sombreador de vértices o píxeles, o incluso un sombreador de geometría que genere el sombreador de píxeles.

## <a name="related-topics"></a>Temas relacionados

[Compilación de sombreadores](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

