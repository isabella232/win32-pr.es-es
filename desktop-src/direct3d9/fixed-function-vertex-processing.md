---
description: En la canalización de vértices de función fija, el procesamiento de los vértices en un búfer de vértices aplica las matrices de transformación actuales para el dispositivo.
ms.assetid: a882a5c5-b05e-4659-9040-92d3e2ccd89c
title: Procesamiento de vértices de funciones fijas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da30dd0fb6cf6e055d8b1bbb31fdfdb01d9e1e20
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152168"
---
# <a name="fixed-function-vertex-processing-direct3d-9"></a>Procesamiento de vértices de funciones fijas (Direct3D 9)

En la canalización de vértices de función fija, el procesamiento de los vértices en un búfer de vértices aplica las matrices de transformación actuales para el dispositivo. También se pueden aplicar operaciones de vértices como la iluminación, la generación de marcas de recorte y la actualización de extensiones, opcionalmente. Al utilizar el procesamiento de vértices de función fija, la marca [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) controla los elementos del búfer de vértices de destino. Esta marca solo se aplica al procesamiento de vértices de funciones fijas. La interfaz [**IDirect3DDevice9**](/windows/desktop/api) expone el método [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) para procesar los vértices. Los vértices de un sombreador de vértices se procesan en el conjunto de flujos de datos de entrada, lo que genera una única secuencia de datos de vértice intercalados en el búfer de vértices de destino llamando al método **IDirect3DDevice9::P rocessvertices** . El método acepta cinco parámetros que describen la ubicación y la cantidad de vértices a los que se destina el método, el búfer de vértices de destino y las opciones de procesamiento. Después de la llamada, el búfer de destino contiene los datos de vértice procesados.

Los parámetros primero, segundo y tercero, SrcStartIndex, DestIndex y VertexCount, reflejan el índice del primer vértice que se va a cargar, el índice dentro del búfer de destino en el que se colocarán los vértices y el número total de vértices que se van a procesar y colocar en el búfer de destino, respectivamente. El cuarto parámetro, pDestBuffer, debe establecerse en la dirección de la interfaz [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) del objeto de búfer de vértice que recibirá los vértices de origen. El parámetro SrcStartIndex especifica el índice en el que el método debe empezar a procesar los vértices.

El parámetro final, flags, determina opciones de procesamiento especiales para el método. Puede establecer este parámetro en 0 para el procesamiento de vértices predeterminado o en [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) para optimizar el procesamiento en algunas situaciones. También puede combinar el valor de \_ DONOTCOPYDATA de D3DPV con uno o varios valores de [D3DLOCK](d3dlock.md) adecuados para el búfer de destino. Al establecer Flags en 0, los componentes de vértice del formato de vértice del búfer de vértice de destino que no se ven afectados por la operación de vértice se copian del sombreador de vértices o se establecen en 0. Sin embargo, cuando se usa D3DPV \_ DONOTCOPYDATA, [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) no sobrescribe la información de coordenadas de color y textura en el búfer de destino a menos que Direct3D genere estos datos. El color difuso se genera cuando se habilita la iluminación, es decir, la \_ iluminación D3DRS se establece en **true**. El color especular se genera cuando se habilita la iluminación y el reflejo está habilitado, es decir, D3DRS \_ SPECULARENABLE y D3DRS \_ Lighting se establecen en **true**. El color especular también se genera cuando se habilita la niebla. Las coordenadas de textura se generan cuando la transformación de textura o la generación de texturas están habilitadas. **IDirect3DDevice9::P rocessvertices** usa los Estados de representación actuales para determinar qué procesamiento de vértices se debe realizar.

## <a name="fvf-usage-settings-for-destination-vertex-buffers"></a>Configuración de uso de FVF para búferes de vértices de destino

El método [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) requiere una configuración específica para [D3DFVF](d3dfvf.md) del búfer de vértice de destino. La configuración de uso de FVF debe ser compatible con la configuración actual del procesamiento de vértices.

Para el procesamiento de vértices de función fija, [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) requiere la siguiente configuración de FVF:

-   El tipo de posición siempre es [D3DFVF \_ XYZRHW](d3dfvf.md) ; por lo tanto, D3DFVF \_ XYZ y D3DFVF \_ XYZB1 a D3DFVF XYZB5 \_ no son válidos.
-   No se deben establecer las marcas [D3DFVF \_ normal](d3dfvf.md), D3DFVF \_ RESERVED0 y D3DFVF \_ RESERVED2.
-   La [marca \_ difusa D3DFVF](d3dfvf.md) debe establecerse si una operación OR de las condiciones siguientes devuelve true:
    -   La iluminación está habilitada; es decir, D3DRS \_ Lighting es **true**.
    -   La iluminación está deshabilitada, el color difuso está presente en los flujos de vértices de entrada y no se ha establecido [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) .
-   La [marca \_ especular D3DFVF](d3dfvf.md) se debe establecer si una operación OR de las condiciones siguientes devuelve true:
    -   La iluminación está habilitada y el color especular está habilitado; es decir, D3DRS \_ SPECULARENABLE es **true**.
    -   La iluminación está deshabilitada, el color especular está presente en los flujos de vértices de entrada y no se ha establecido [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) .
    -   La niebla de vértice está habilitada; es decir, D3DRS \_ FOGVERTEXMODE no se establece en D3DFOG \_ None.

Además, el recuento de coordenadas de textura debe establecerse de la siguiente manera:

-   Si la transformación de textura y la generación de texturas están deshabilitadas para todas las fases de texturas activas y no se establece el valor de [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) , el número y el tipo de coordenadas de textura de salida deben coincidir con los de las coordenadas de textura de los vértices de entrada. Si \_ se establece D3DPV DONOTCOPYDATA y la transformación de textura y la generación de texturas están deshabilitadas, se omiten las coordenadas de textura de salida.
-   Si la transformación de textura o la generación de texturas están habilitadas para cualquier fase de textura activa, es posible que el vértice de salida tenga que contener más conjuntos de coordenadas de textura que el vértice de entrada. Esto se debe a la proliferación de coordenadas de textura de las generadas por la generación de texturas o derivadas de las transformaciones de textura. Tenga en cuenta que se produce una proliferación similar de coordenadas de textura durante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) llama a, pero no es visible para el programador de la aplicación. En este caso, Direct3D genera un nuevo conjunto de coordenadas de textura. El nuevo conjunto de coordenadas de textura se deriva recorriendo las fases de textura y analizando la configuración de la generación de texturas, la transformación de texturas y el índice de coordenadas de textura para determinar si se requiere un conjunto único de coordenadas de textura para esa fase. Cada vez que se requiere un nuevo conjunto, se asigna en orden ascendente. Tenga en cuenta que el requisito máximo y típico es un conjunto por fase, aunque podría ser menos debido al uso compartido de coordenadas de textura no transformadas a través de D3DTSS \_ TEXCOORDINDEX.

Por lo tanto, para cada fase de textura, se genera un nuevo conjunto de coordenadas de textura si una textura se enlaza a esa fase y se cumple cualquiera de las condiciones siguientes:

-   La generación de texturas está habilitada para esa fase.
-   La transformación textura está habilitada para esa fase.
-   Se hace referencia a las coordenadas de textura de entrada no transformadas a través \_ de D3DTSS TEXCOORDINDEX por primera vez.

Cuando Direct3D está generando coordenadas de textura, se requiere la aplicación para realizar las siguientes acciones:

1.  Use un búfer de vértice de destino con el uso de FVF adecuado.
2.  Vuelva a programar el D3DTSS \_ TEXCOORDINDEX de la fase de textura según la posición de las coordenadas de textura postprocesadas. Tenga en cuenta que la reprogramación de la configuración de TEXCOORDINDEX de D3DTSS \_ se produce cuando el búfer de vértices procesado se usa en las llamadas [**IDirect3DDevice9::D Rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) y [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) posteriores.

Por último, la dimensionalidad de la coordenada de textura ([D3DFVF \_ TEX0](d3dfvf.md) a D3DFVF \_ TEX8) debe establecerse de la siguiente manera:

-   Para cada conjunto de coordenadas de textura, si la transformación de textura y la generación de texturas están deshabilitadas, la dimensión de la textura de salida debe coincidir con la entrada. Si la transformación de textura está habilitada, la dimensionalidad de salida debe coincidir con el recuento definido por la configuración de D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3 o D3DTTFF \_ COUNT4. Si la transformación de textura está deshabilitada y la generación de textura está habilitada, la dimensionalidad de salida debe coincidir con la configuración del modo de generación de texturas; Actualmente, todos los modos generan tres valores float.

Cuando [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) produce un error debido a un búfer de vértice de destino incompatible FVF código, el código esperado se imprime en la salida de depuración (solo compilaciones de depuración).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> </dl>

 

 
