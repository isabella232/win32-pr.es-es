---
description: Muchas técnicas de representación y generación de contenido requieren un mapa único y no superpuesto de una señal 2D (como una textura) en una malla.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Uso de UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8faeaa0a416f6f062c81c4101ff47d5222ca75d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580141"
---
# <a name="using-uvatlas-direct3d-9"></a>Uso de UVAtlas (Direct3D 9)

> [!NOTE]
> UVAtlas se envió originalmente en la biblioteca de utilidad D3DX9 ahora en desuso. La versión más reciente está disponible en [UV Atlas Command-Line Tool (uvatlas.exe).](https://github.com/Microsoft/UVAtlas)

Muchas técnicas de representación y generación de contenido requieren un mapa único y no superpuesto de una señal 2D (como una textura) en una malla. Estas técnicas incluyen:

-   Asignación normal o de desplazamiento
-   Simulaciones de PRT de espacio de textura y mapas claros
-   Cuadro de superficie
-   Iluminación de espacio de textura

La generación manual de una asignación UV única suele llevar mucho tiempo y tediosa. Esto es especialmente cierto cuando la geometría de entrada es compleja y se desea un uso eficaz o de baja distorsión del espacio de textura. En la ilustración siguiente se muestra una malla de ejemplo y su atlas de textura correspondiente.

![Muestra una malla de ejemplo y su atlas de textura correspondiente.](images/uvatlas1.jpg)

En este ejemplo se muestra una malla (a la izquierda) y el mapa normal de espacio UV correspondiente (a la derecha). Observe que el atlas de textura contiene varios grupos o clústeres de datos; Cada clúster se denomina gráfico y, en el ejemplo anterior, muestra los datos normales de una parte de la malla.

Las API de UVAtlas D3DX generan automáticamente un atlas de textura óptimo y no superpuesto. Las API proporcionan parámetros de entrada que le permiten:

-   Minimice la extensión de textura, la distorsión y el bajomuestreo.
-   Maximice la densidad de empaquetado del espacio de textura para un uso eficaz de la memoria.
-   Proporcione un muestreo uniforme en la malla, lo que minimiza las discontinuidades en la frecuencia de muestreo.

## <a name="how-uvatlas-works"></a>Funcionamiento de UVAtlas

Las API de UVAtlas (consulte FUNCIONES DE [UVAtlas)](dx9-graphics-reference-d3dx-functions-uvatlas.md)generan un atlas de textura mediante la creación de particiones de una superficie en gráficos y el empaquetado de los gráficos en un atlas de textura. Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) y [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) para realizar estos pasos por separado; o use [**D3DXUVAtlasCreate para**](d3dxuvatlascreate.md) crear particiones, parametrizar y empaquetar en una sola llamada.

-   [Creación de particiones y parametrización de una malla](#partitioning-and-parameterizing-a-mesh)
-   [Uso de tensores de métricas integrados para controlar la parametrización](#using-integrated-metric-tensors-to-control-parameterization)
-   [Usar datos de adyacencia para los creases especificados por el usuario](#using-adjacency-data-for-user-specified-creases)
-   [Empaquetado de gráficos en un atlas](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a>Creación de particiones y parametrización de una malla

En primer lugar, la malla se divide en gráficos y, a continuación, cada gráfico se parametriza en su propio \[ espacio UV 0,1. \] Un cilindro se puede parametrizar mediante un gráfico; Por otro lado, una esfera requerirá dos gráficos, como se muestra en la ilustración siguiente.

![ilustración de una esfera particionada en dos gráficos](images/uvatlas3.jpg)

Una malla que se puede parametrizar con un solo gráfico se clasifica como "homeomórfica en un disco", lo que significa que podría extender un disco infinitamente flexible y que se puede extender infinitamente sobre el gráfico y cubrir la geometría perfectamente. Esta extensión, denominada homeomorfismo, es una función bidireccional; lo que significa que puede pasar de una parametrización a otra sin perder información.

Muy pocas mallas reales se pueden parametrizar en dos dimensiones sin separar la malla en clústeres o gráficos. En la ilustración siguiente se muestra otra malla de ejemplo y su atlas de textura correspondiente.

![Muestra una malla de ejemplo con distintas formas y su atlas de textura correspondiente.](images/uvatlas2.jpg)

Hay dos parámetros que determinan el número de gráficos creados:

-   El número máximo de gráficos permitido para el atlas
-   La cantidad máxima de extensión permitida para cada gráfico

La cantidad de stretch determinará el número de gráficos que se generan y la calidad general del muestreo. Stretch oscila entre 0,0 (sin stretch) y 1,0 (cualquier cantidad de stretch). D3DXUVAtlasCreate y D3DXUVAtlasPartition devuelven el stretch máximo generado por el algoritmo. En la ilustración siguiente se muestra otra malla de ejemplo y su atlas de textura correspondiente.

![ilustración de una malla de ejemplo y su atlas de textura correspondiente](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a>Uso de tensores de métricas integrados para controlar la parametrización

La priorización del espacio de textura se puede especificar por triángulo. Se pueden proporcionar tensores de métricas integrados para controlar cómo se extienden los triángulos en el atlas de espacio de textura resultante. Las IMT se pueden especificar directamente o calcular en función de una señal de entrada mediante las funciones de cálculo D3DX IMT. Un tensor de métrica integrado (o IMT) es una matriz simétrica de 2x2 que describe cómo se extiende un triángulo en el atlas. Cada IMT se define mediante 3 flotantes, llámelos (a,b,c). Se pueden organizar en una matriz simétrica de 2x2 como la siguiente:


```
a b
b c
```



A continuación, el IMT se puede usar para buscar la distancia entre dos vectores. Dados dos vectores v1 y v2, donde :


```
vector v1
vector v2 = v1 + (s,t)
```



La distancia entre v1 y v2 se puede calcular como:


```
sqrt((s, t) * M * (s, t)^T)
```



En otras palabras, el vector (s,t) podría ser la magnitud del stretch en una dirección arbitraria en el espacio u-v. En este caso, el vector de es una dirección desde el primer al segundo vértice, y t es el producto cruzado de los valores normales y s. Por ejemplo:


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



Las IMT se pueden especificar directamente o calcular en función de una señal de entrada mediante las funciones de cálculo D3DX IMT: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal y D3DXComputeIMTFromTexture. \_

Especifique los datos IMT directamente si desea controlar cómo se asigna el espacio de textura a triángulos individuales. Al hacerlo, asigne más área en el atlas a áreas importantes de una malla (como la cara de un carácter o el logotipo de un logotipo de cuello o regiones de una escena cerca de la ruta de acceso de un jugador). Al especificar IMT que son múltiplo de la matriz de identidad, los triángulos resultantes se escalarán uniformemente en el espacio de textura.

Por ejemplo, dado un mapa normal de alta resolución, puede calcular IMT para proporcionar más espacio de textura a las áreas de señal de mayor frecuencia en el mapa normal. Los triángulos que son "planos" (que se asignan a regiones constantes del mapa normal original) recibirán menos espacio de textura. Los triángulos que contienen una gran cantidad de detalles de mapa normal recibirán más área de textura en el resultado final. A continuación, puede volver a muestrear el mapa normal en una textura más pequeña, pero mantener los detalles, o puede volver a compilar el mapa normal con la asignación UV más óptima.

### <a name="using-adjacency-data-for-user-specified-creases"></a>Usar datos de adyacencia para los creases especificados por el usuario

Se puede proporcionar información de adyacencia definida por el usuario a la función de creación de particiones para describir los contornos predefinidos en la malla y, por tanto, definir un límite de gráfico entre las caras adyacentes. Se trata de una manera sencilla para que el autor de la llamada especifique su propia creación de particiones de gráfico como entrada en el algoritmo, lo que refinará aún más los gráficos para poner el ajuste por debajo del máximo permitido.

### <a name="example"></a>Ejemplo

En este ejemplo se muestra cómo podría usar las API de UVAtlas y el Visor de DirectX (Dxviewer.exe) para buscar y corregir discontinuidades en el modelo que pueden afectar drásticamente al tamaño del atlas de textura. Puede obtener información Dxviewer.exe y obtener información sobre él desde el SDK de DirectX. Dxviewer.exe se quitó del SDK de DirectX después de la versión de agosto de 2009, por lo que para obtenerlo necesitará al menos el SDK de DirectX de agosto de 2009. Para obtener información sobre el SDK de DirectX, [consulte ¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

Supongamos que empezó con algún modelo en su software de generación de contenido favorito (en este ejemplo se usa un modelo de cabeza desaprobado que se creó en Maya). Exporte el modelo con textura a un archivo .x y cree un atlas de textura con D3DXUVAtlasCreate. El atlas de textura resultante tendría un aspecto parecido al de la ilustración siguiente.

![ilustración de un atlas para un modelo de árboles](images/uvatlas5.jpg)

El atlas tiene 22 gráficos y una extensión máxima de 0,994.

Ahora, mire el modelo con textura para ver cómo se asigna el atlas de textura a la geometría. Para ello, cargue el modelo en la herramienta de visor:

-   Abra la herramienta de visor desde Utilidades de DirectX.
-   Cargue el archivo .x haciendo clic en el botón Abrir.
-   Para habilitar la opción de visualización de crease, haga clic en el botón ver y seleccione Creases from popup (Creases en el menú emergente).

En la ilustración siguiente se muestra lo que debería ver en la herramienta de visor.

![ilustración de una malla con textura en la herramienta de visor](images/uvatlas6c.jpg)

Cada línea es un crease que es un borde adyacente entre dos gráficos del atlas de textura. El número de gráficos generados por el algoritmo se debe a ligeras diferencias, quizás debido a discontinuidades en las normales. Estas pequeñas diferencias se pueden reducir mediante la gran cantidad de datos, es decir, forzar que los datos que son casi iguales sean iguales. Para cambiar los normales y los pesos de máscara:

-   Ejecute la herramienta DirectX Ops (dxops.exe) con la siguiente línea de comandos en la malla (reemplazando "modelName.x" por el nombre del modelo):
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

Esto compara los normales y los pesos de máscara, y donde difieren en el valor en menos de 2,01, los datos se hacen iguales. En las ilustraciones siguientes se muestra un primer lugar en el ojo para ver los creas antes de la deserción (a la izquierda) y los creas después de la deserción (a la derecha):

![ilustración de creases antes de la desafilación](images/uvatlas6a.jpg)![ilustración de creases después de la resalte](images/uvatlas6b.jpg)

Figura 7: Eliminación de creases por insensible

En este ejemplo, elimina 86 vértices de la malla de entrada. Con menos creases en la malla, puede volver a generar el atlas, como se muestra en la ilustración siguiente.

![ilustración del nuevo atlas con los creases quitados](images/uvatlas8.jpg)

El atlas solo tiene 7 gráficos y una extensión máxima de aproximadamente 0,0776. El nuevo atlas ahora se ajusta a una textura más pequeña (aproximadamente un 30 % más pequeña en este ejemplo).

### <a name="packing-charts-into-an-atlas"></a>Empaquetado de gráficos en un atlas

Una vez que una malla se ha particionado en gráficos con parámetros individuales, los gráficos deben empaquetarse de forma eficaz en un único mapa de textura. Esto se realiza como el segundo paso de D3DXUVAtlasCreate o se puede invocar explícitamente llamando a D3DXUVAtlasPack.

Los gráficos empaquetados están separados por un ancho de medianía especificado por el usuario. El ancho del medianía es la cantidad de separación entre los gráficos y permite la interpolación bilineal y la asignación de mip para evitar la representación de artefactos en los límites del gráfico. D3DX proporciona una interfaz para rellenar automáticamente estos canales; vea [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) para obtener más información.

## <a name="integrating-uvatlas-into-your-pipeline"></a>Integración de UVAtlas en la canalización

Además de ser invocadas por el autor antes de pintar texturas, estas funciones se pueden integrar en una canalización de arte automatizada. Por ejemplo, una llamada UVAtlas se puede emitir automáticamente después de actualizar un recurso, antes de realizar una simulación de PRT o un paso de asignación normal. Esto evita la necesidad de reparar manualmente la asignación UV de un objeto si se ha modificado la topología de la malla.

Consulte la [herramienta atlas Command-Line UV (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) para ver un ejemplo del uso de las funciones UVAtlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas avanzados](advanced-topics.md)
</dt> </dl>

 

 
