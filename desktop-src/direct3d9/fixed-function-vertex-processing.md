---
description: En la canalización de vértices de función fija, el procesamiento de los vértices en un búfer de vértices aplica las matrices de transformación actuales al dispositivo.
ms.assetid: a882a5c5-b05e-4659-9040-92d3e2ccd89c
title: Procesamiento de vértices de función fija (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827a293a4fbd552327d93076de773aec90dbd895faf3c086f4794036978984fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988025"
---
# <a name="fixed-function-vertex-processing-direct3d-9"></a>Procesamiento de vértices de función fija (Direct3D 9)

En la canalización de vértices de función fija, el procesamiento de los vértices en un búfer de vértices aplica las matrices de transformación actuales al dispositivo. Opcionalmente, también se pueden aplicar operaciones de vértice como iluminación, generación de marcas de recorte y extensiones de actualización. Cuando se usa el procesamiento de vértices de función fija, la modificación de los elementos del búfer de vértices de destino se controla mediante la marca [ \_ DONOTCOPYDATA de D3DPV.](other-direct3d-constants.md) Esta marca solo se aplica al procesamiento de vértices de función fija. La [**interfaz IDirect3DDevice9**](/windows/desktop/api) expone el método [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) para procesar vértices. Los vértices se procesan desde un sombreador de vértices hasta el conjunto de flujos de datos de entrada, generando una sola secuencia de datos de vértice intercalados en el búfer de vértices de destino mediante una llamada al método **IDirect3DDevice9::P rocessVertices.** El método acepta cinco parámetros que describen la ubicación y la cantidad de vértices que el método tiene como destino, el búfer de vértices de destino y las opciones de procesamiento. Después de la llamada, el búfer de destino contiene los datos de vértice procesados.

Los parámetros primero, segundo y tercero, SrcStartIndex, DestIndex y VertexCount, reflejan el índice del primer vértice que se va a cargar, el índice dentro del búfer de destino en el que se colocarán los vértices y el número total de vértices que se procesarán y colocarán en el búfer de destino, respectivamente. El cuarto parámetro, pDestBuffer, debe establecerse en la dirección de la interfaz [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) del objeto de búfer de vértices que recibirá los vértices de origen. El parámetro SrcStartIndex especifica el índice en el que el método debe empezar a procesar vértices.

El parámetro final, Flags, determina las opciones de procesamiento especiales para el método . Puede establecer este parámetro en 0 para el procesamiento de vértices predeterminado o en [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) para optimizar el procesamiento en algunas situaciones. También puede combinar el valor D3DPV DONOTCOPYDATA con uno o varios \_ [valores D3DLOCK](d3dlock.md) adecuados para el búfer de destino. Al establecer Marcas en 0, los componentes de vértice del formato de vértice del búfer de vértices de destino que no se ven afectados por la operación de vértice se siguen copiando del sombreador de vértices o se establecen en 0. Sin embargo, al usar D3DPV \_ DONOTCOPYDATA, [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) no sobrescribe la información de coordenadas de color y textura en el búfer de destino a menos que Direct3D genere estos datos. El color difuso se genera cuando se habilita la iluminación, es decir, D3DRS \_ LIGHTING se establece en **TRUE.** El color especular se genera cuando se habilita la iluminación y el especular, es decir, D3DRS \_ SPECULARENABLE y D3DRS LIGHTING se establecen \_ en **TRUE.** El color especular también se genera cuando se habilita el color especular. Las coordenadas de textura se generan cuando se habilita la transformación de textura o la generación de texturas. **IDirect3DDevice9::P rocessVertices** usa los estados de representación actuales para determinar qué procesamiento de vértices debe realizarse.

## <a name="fvf-usage-settings-for-destination-vertex-buffers"></a>Uso de FVF Configuración búferes de vértices de destino

El [**método IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) requiere una configuración específica para [D3DFVF](d3dfvf.md) del búfer de vértices de destino. La configuración de uso de FVF debe ser compatible con la configuración actual para el procesamiento de vértices.

Para el procesamiento fijo de vértices de función, [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) requiere la siguiente configuración de FVF:

-   El tipo de posición siempre es [D3DFVF \_ XYZRHW;](d3dfvf.md) por lo tanto, D3DFVF XYZ y \_ D3DFVF \_ XYZB1 hasta D3DFVF \_ XYZB5 no son válidos.
-   No se deben establecer las marcas [D3DFVF \_ NORMAL,](d3dfvf.md)D3DFVF RESERVED0 y \_ D3DFVF \_ RESERVED2.
-   La [marca \_ DIFUSO D3DFVF](d3dfvf.md) debe establecerse si una operación OR de las condiciones siguientes devuelve true:
    -   La iluminación está habilitada; es decir, D3DRS \_ LIGHTING es **TRUE.**
    -   La iluminación está deshabilitada, el color difuso está presente en los flujos de vértices de entrada y [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) no está establecido.
-   La [marca \_ SPECULAR D3DFVF](d3dfvf.md) debe establecerse si una operación OR de las condiciones siguientes devuelve true:
    -   La iluminación está habilitada y el color especular está habilitado; es decir, D3DRS \_ SPECULARENABLE es **TRUE.**
    -   La iluminación está deshabilitada, el color especular está presente en los flujos de vértices de entrada y [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) no está establecido.
    -   Vértices habilitados; Es decir, \_ D3DRSOGVERTEXMODE no está establecido en D3DFOG \_ NONE.

Además, el recuento de coordenadas de textura debe establecerse de la siguiente manera:

-   Si la transformación de textura y la generación de texturas están deshabilitadas para todas las fases de textura activas y no se establece [ \_ DONOTCOPYDATA de D3DPV,](other-direct3d-constants.md) el número y el tipo de coordenadas de textura de salida son necesarios para que coincidan con los de las coordenadas de textura del vértice de entrada. Si se establece D3DPV DONOTCOPYDATA y se deshabilita la transformación de textura y la generación de texturas, se omiten las coordenadas de textura \_ de salida.
-   Si la transformación de textura o la generación de texturas están habilitadas para cualquier fase de textura activa, es posible que el vértice de salida tenga que contener más conjuntos de coordenadas de textura que el vértice de entrada. Esto se debe a la proliferación de coordenadas de textura a partir de las generadas por la generación de texturas o derivadas por transformaciones de textura. Tenga en cuenta que una proliferación similar de coordenadas de textura se produce durante las llamadas [**IDirect3DDevice9::D rawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) pero no es visible para el programador de la aplicación. En este caso, Direct3D genera un nuevo conjunto de coordenadas de textura. El nuevo conjunto de coordenadas de textura se deriva del paso a paso por las fases de textura y el análisis de la configuración de la generación de texturas, la transformación de textura y el índice de coordenadas de textura para determinar si se necesita un conjunto único de coordenadas de textura para esa fase. Cada vez que se requiere un nuevo conjunto, se asigna en orden creciente. Tenga en cuenta que el requisito máximo y típico es un conjunto por fase, aunque puede ser menor debido al uso compartido de coordenadas de textura notransformadas a través de D3DTSS \_ TEXCOORDINDEX.

Por lo tanto, para cada fase de textura, se genera un nuevo conjunto de coordenadas de textura si una textura está enlazada a esa fase y se cumple cualquiera de las condiciones siguientes:

-   La generación de texturas está habilitada para esa fase.
-   La transformación de textura está habilitada para esa fase.
-   Se hace referencia a las coordenadas de textura de entrada notransformadas a través de D3DTSS \_ TEXCOORDINDEX por primera vez.

Cuando Direct3D genera coordenadas de textura, la aplicación es necesaria para realizar las siguientes acciones:

1.  Use un búfer de vértices de destino con el uso de FVF adecuado.
2.  Reprograme D3DTSS TEXCOORDINDEX de la fase de textura según la ubicación de las \_ coordenadas de textura postprocesadas. Tenga en cuenta que la reprogramación de la configuración D3DTSS TEXCOORDINDEX se produce cuando se usa el búfer de vértices procesado en las llamadas \_ [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) e [**IDirect3DDevice9::D rawIndexedPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

Por último, la dimensionalidad de la coordenada de textura[(D3DFVF \_ TEX0](d3dfvf.md) a D3DFVF \_ TEX8) debe establecerse de la siguiente manera:

-   Para cada conjunto de coordenadas de textura, si la transformación de textura y la generación de texturas están deshabilitadas, la dimensionalidad de la coordenada de textura de salida debe coincidir con la entrada. Si la transformación de textura está habilitada, la dimensionalidad de salida debe coincidir con el recuento definido por los valores de D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF COUNT3 o \_ D3DTTFF \_ COUNT4. Si la transformación de textura está deshabilitada y la generación de texturas está habilitada, la dimensionalidad de salida debe coincidir con la configuración del modo de generación de texturas. actualmente, todos los modos generan tres valores float.

Cuando se produce un error [**en IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) debido a un código FVF de búfer de vértices de destino incompatible, el código esperado se imprime en la salida de depuración (solo compilaciones de depuración).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> </dl>

 

 
