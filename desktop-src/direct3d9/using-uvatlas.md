---
description: Muchas técnicas de representación y generación de contenido requieren un mapa único y no superpuesto de una señal 2D (como una textura) en una malla.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Usar UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b335dd6ea94a3db0c0760b0d07a0b8df3fe4c7c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104279709"
---
# <a name="using-uvatlas-direct3d-9"></a>Usar UVAtlas (Direct3D 9)

Muchas técnicas de representación y generación de contenido requieren un mapa único y no superpuesto de una señal 2D (como una textura) en una malla. Estas técnicas incluyen:

-   Asignación normal/de desplazamiento
-   Simulaciones de PRT de espacio de textura y mapas ligeros
-   Dibujo de Surface
-   Iluminación de espacio de textura

La generación manual de una asignación UV es a menudo lenta y tediosa. Esto es especialmente cierto cuando la geometría de entrada es una utilización de espacio de textura compleja y eficiente y de baja distorsión. En la ilustración siguiente se muestra un ejemplo de malla y su Atlas de textura correspondiente.

![Muestra una malla de ejemplo y su Atlas de textura correspondiente.](images/uvatlas1.jpg)

Este ejemplo muestra una malla (a la izquierda) y el mapa normal de espacio UV correspondiente (a la derecha). Tenga en cuenta que el Atlas de textura contiene varios grupos o clústeres de datos. cada clúster se denomina gráfico y en el ejemplo anterior, muestra contiene los datos normales de una parte de la malla.

Las API de D3DX UVAtlas generan automáticamente un Atlas de texturas no superpuestos óptima. Las API proporcionan parámetros de entrada que le permiten:

-   Minimizar el estiramiento de textura, la distorsión y el submuestreo.
-   Maximice la densidad de empaquetado de espacio de textura para un uso eficaz de la memoria.
-   Proporcionar un muestreo uniforme en la malla, lo que minimiza las discontinuidades en la frecuencia de muestreo.

## <a name="how-uvatlas-works"></a>Cómo funciona UVAtlas

Las API de UVAtlas (consulte [funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generan un Atlas de textura mediante la creación de particiones de una superficie en los gráficos y el empaquetado de los gráficos en un Atlas de textura. Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) y [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) para realizar estos pasos por separado. o bien, use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) para particionar, parametrizar y empaquetar en una sola llamada.

-   [Creación de particiones y parametrización de una malla](#partitioning-and-parameterizing-a-mesh)
-   [Usar decenas de métricas integradas para controlar la parametrización](#using-integrated-metric-tensors-to-control-parameterization)
-   [Usar datos de proximidad para las arrugas especificadas por el usuario](#using-adjacency-data-for-user-specified-creases)
-   [Empaquetar gráficos en un Atlas](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a>Creación de particiones y parametrización de una malla

En primer lugar, la malla está dividida en gráficos y, a continuación, cada gráfico tiene parámetros en su propio \[ \] espacio de UV de 0, 1. Un cilindro puede incluir parámetros en un gráfico; por otra parte, una esfera necesitará dos gráficos, como se muestra en la siguiente ilustración.

![Ilustración de una esfera dividida en dos gráficos](images/uvatlas3.jpg)

Una malla que se puede parametrizar con un solo gráfico se clasifica como "homeomorphic a un disco", lo que significa que se puede repartir un disco infinitamente flexible y estirable en el gráfico y cubrir la geometría perfectamente. Esta ampliación, denominada homeomorphism, es una función bidireccional. lo que significa que puede pasar de una parametrización a otra sin perder información.

Muy pocas mallas del mundo real se pueden parametrizar en dos dimensiones sin separar la malla en clústeres o gráficos. En la ilustración siguiente se muestra otra malla de ejemplo y su Atlas de textura correspondiente.

![Muestra una malla de ejemplo con diferentes formas y su Atlas de textura correspondiente.](images/uvatlas2.jpg)

Hay dos parámetros que determinan el número de gráficos creados:

-   El número máximo de gráficos permitidos para Atlas
-   La cantidad máxima de stretch permitida para cada gráfico

La cantidad de stretch determinará el número de gráficos que se generan y la calidad general del muestreo. Estire los intervalos desde 0,0 (sin Stretch) hasta 1,0 (cualquier cantidad de Stretch). D3DXUVAtlasCreate y D3DXUVAtlasPartition devuelven el estiramiento máximo generado por el algoritmo. En la ilustración siguiente se muestra otra malla de ejemplo y su Atlas de textura correspondiente.

![Ilustración de una malla de ejemplo y su Atlas de textura correspondiente](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a>Usar decenas de métricas integradas para controlar la parametrización

La priorización del espacio de textura se puede especificar por triángulo. Se pueden proporcionar decenas de métricas integradas para controlar cómo se ajustan los triángulos en el Atlas de espacio de textura resultante. IMT se puede especificar directamente o calcular según una señal de entrada mediante las funciones de cálculo de D3DX IMT. Una métrica integrada tensores (o IMT) es una matriz de 2x2 simétrica que describe cómo se ajusta un triángulo en el Atlas. Cada IMT se define mediante 3 flotantes, se llama (a, b, c). Se pueden organizar en una matriz de 2x2 simétrica como la siguiente:


```
a b
b c
```



A continuación, se puede usar IMT para encontrar la distancia entre dos vectores. Dados dos vectores v1 y V2, donde:


```
vector v1
vector v2 = v1 + (s,t)
```



La distancia entre V1 y V2 puede calcularse como:


```
sqrt((s, t) * M * (s, t)^T)
```



En otras palabras, el vector (s, t) podría ser la magnitud de stretch en una dirección arbitraria en el espacio u-v. En este caso, el vector s es una dirección entre el primero y el segundo, y t es el producto cruzado de la normal y s. Por ejemplo:


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



IMT se puede especificar directamente o calcular según una señal de entrada mediante las funciones de cálculo de D3DX IMT: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal y D3DXComputeIMTFromTexture \_ Graphics.

Especifique los datos de IMT directamente si desea controlar cómo se asigna el espacio de textura a los triángulos individuales. Al hacerlo, asigne más área en el Atlas a las áreas importantes de una malla (como el logotipo o la esfera de un carácter o las regiones de una escena cerca de la ruta de acceso de un jugador). Al especificar IMT que son múltiplos de la matriz de identidad, los triángulos resultantes se escalarán uniformemente en el espacio de textura.

Por ejemplo, dado un mapa normal de alta resolución, puede calcular IMT para proporcionar más espacio de textura a áreas de señal de mayor frecuencia en el mapa normal. Los triángulos que son "planos" (que se asignan a las regiones constantes del mapa normal original) recibirán menos espacio de textura. Los triángulos que contienen una gran cantidad de detalles de mapa normal recibirán más área de textura en el resultado final. Después, puede volver a muestrear el mapa normal en una textura más pequeña pero mantener los detalles, o bien puede volver a calcular el mapa normal con la asignación UV más óptima.

### <a name="using-adjacency-data-for-user-specified-creases"></a>Usar datos de proximidad para las arrugas especificadas por el usuario

Se puede proporcionar información de adyacencia definida por el usuario a la función de particionamiento para describir las arrugas predefinidas en la malla y, por tanto, definir un límite de gráfico entre caras adyacentes. Esta es una manera sencilla de que el autor de la llamada especifique su propia creación de particiones de gráfico como entrada en el algoritmo, lo que perfeccionará aún más los gráficos para aumentar el tamaño en el máximo permitido.

### <a name="example"></a>Ejemplo

En este ejemplo se muestra cómo podría usar las API de UVAtlas y el visor de DirectX (Dxviewer.exe) para buscar y corregir discontinuidades en el modelo que puede afectar drásticamente al tamaño de su Atlas de textura. Puede obtener Dxviewer.exe y obtener información sobre él desde el SDK de DirectX. Dxviewer.exe se quitó del SDK de DirectX después de la versión de agosto de 2009, por lo que necesitará al menos el SDK de DirectX de agosto de 2009. Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

Supongamos que comenzó con algún modelo en su software de generación de contenido favorito (en este ejemplo se usa un modelo de encabezado Dwarf creado en Maya). Exporte el modelo con textura a un archivo. x y cree un Atlas de textura con D3DXUVAtlasCreate. El Atlas de textura resultante tendría un aspecto similar al de la siguiente ilustración.

![Ilustración de un Atlas para un modelo Dwarf](images/uvatlas5.jpg)

El Atlas tiene 22 gráficos y un ajuste máximo de 0,994.

Ahora Fíjese en el modelo con textura para ver hasta qué grado se asigna el Atlas de textura a la geometría. Para ello, cargue el modelo en la herramienta Visor:

-   Abra la herramienta visor desde las utilidades de DirectX.
-   Cargue el archivo. x haciendo clic en el botón abrir.
-   Habilitar la opción de visualización de arrugas haciendo clic en el botón ver y seleccionando arrugas en el menú emergente.

En la ilustración siguiente se muestra lo que debería ver en la herramienta visor.

![Ilustración de una malla con textura en la herramienta Visor](images/uvatlas6c.jpg)

Cada línea es una arruga que es un borde adyacente entre dos gráficos en el Atlas de textura. El número de gráficos generados por el algoritmo está causado por pequeñas diferencias, quizás debido a discontinuidades en las normales. Estas pequeñas diferencias se pueden reducir con los datos de soldadura, es decir, forzar que los datos que son casi iguales sean iguales. Para soldar las normales y skinweights:

-   Ejecute la herramienta de operaciones de DirectX (dxops.exe) con la siguiente línea de comandos en la malla (reemplace "modelName. x" por el nombre del modelo):
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

Con esto se comparan los valores normales y skinweights, y donde se diferencian por un valor inferior a 2,01, los datos se hacen iguales. En las ilustraciones siguientes se muestra un cierre del ojo para ver las arrugas antes de la soldadura (a la izquierda) y las arrugas después de la soldadura (a la derecha):

![Ilustración de dobleces antes de la soldadura](images/uvatlas6a.jpg)![Ilustración de arrugas tras la soldadura](images/uvatlas6b.jpg)

Figura 7: eliminación de dobleces por soldadura

En este ejemplo, la soldadura quitó 86 vértices de la malla de entrada. Con menos arrugas en la malla, puede volver a generar el Atlas, tal como se muestra en la ilustración siguiente.

![Ilustración del nuevo Atlas con dobleces quitados](images/uvatlas8.jpg)

El Atlas solo tiene 7 gráficos y un ajuste máximo de aproximadamente 0,0776. El nuevo Atlas ahora se ajusta a una textura más pequeña (aproximadamente un 30% más pequeño en este ejemplo).

### <a name="packing-charts-into-an-atlas"></a>Empaquetar gráficos en un Atlas

Una vez que se ha particionado una malla en gráficos con parámetros individuales, los gráficos deben empaquetarse de forma eficaz en un único mapa de textura. Esto se realiza como el segundo paso de D3DXUVAtlasCreate o se puede invocar explícitamente mediante una llamada a D3DXUVAtlasPack.

Los gráficos empaquetados están separados por un ancho de medianil especificado por el usuario. El ancho del medianil es la cantidad de separación entre los gráficos y permite la interpolación bilineal y la asignación de MIP para evitar la representación de artefactos en los límites del gráfico. D3DX proporciona una interfaz para rellenar automáticamente estos medianils; consulte [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) para obtener más información.

## <a name="integrating-uvatlas-into-your-pipeline"></a>Integración de UVAtlas en la canalización

Además de ser invocado por el artista antes del dibujo de texturas, estas funciones se pueden integrar en una canalización de arte automatizada. Por ejemplo, una llamada a UVAtlas se puede emitir automáticamente después de actualizar un recurso, antes de realizar una simulación de PRT o un paso de asignación normal. Esto evita la necesidad de reparar manualmente la asignación UV de un objeto si se ha modificado la topología de la malla.

Consulte la [herramienta de Command-Line de Atlas de UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) para obtener un ejemplo del uso de las funciones de UVAtlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas avanzados](advanced-topics.md)
</dt> </dl>

 

 
