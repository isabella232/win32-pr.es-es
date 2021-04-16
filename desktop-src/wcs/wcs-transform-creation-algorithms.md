---
title: Algoritmos de creación de transformaciones de WCS
description: Algoritmos de creación de transformaciones de WCS
ms.assetid: 526bbbfc-fb60-415d-b4f0-6a44a5d11a55
keywords:
- Sistema de color de Windows (WCS), creación de transformación
- WCS (sistema de colores de Windows), creación de transformación
- Administración del color de imagen, creación de transformación
- Administración del color, creación de transformación
- colores, creación de transformación
- creación de transformación
- Creación de transformación WCS
- algoritmos, creación de transformación
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418596c0e57571f3e504727d4606921d36ff9461
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104571197"
---
# <a name="wcs-transform-creation-algorithms"></a>Algoritmos de creación de transformaciones de WCS

[Creación de transformaciones](#creation-of-transforms)

 

[Ejecución de transformación secuencial](#sequential-transform-execution)

 

[Creación de transformaciones optimizadas](#creation-of-optimized-transforms)

 

[ICCProfileFromWCSProfile](#iccprofilefromwcsprofile)

 

[Preservación de negro y generación de negro](#black-preservation-and-black-generation)

 

[Comprobar la gama](#checkgamut)

## <a name="creation-of-transforms"></a>Creación de transformaciones

Para explicar correctamente el funcionamiento de las transformaciones de color, es útil explicar la ruta de acceso de procesamiento completa a través de ICM 2,0 y el interior de la CTE. La función ICM 2,0 [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) crea una transformación de color que las aplicaciones pueden usar para realizar la administración del color. Esta función crea un contexto de color a partir de las entradas de [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) y intención. Los inconvenientes se asignan al algoritmo de asignación de gama ICC de línea base en correlación. A continuación, la función llama a la función [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/) de ICM 2,0 para el procesamiento de color coherente. La función **CreateColorTransform** generalmente copia los datos en la estructura de transformación optimizada interna.

La función ICM 2,0 CreateMultiProfileTransform acepta una matriz de perfiles y una matriz de intenciones o un perfil de vínculo de dispositivo único y crea una transformación de color que las aplicaciones pueden usar para realizar la asignación de colores. Procesa estos perfiles de entrada y sus intenciones para crear modelos de dispositivos, modelos de apariencia de color, descripciones de límites de gama y modelos de asignación de gama. Aquí se muestra cómo hacerlo:

-   Los modelos de dispositivo se inicializan directamente desde perfiles de DM. Hay un modelo de dispositivo creado para cada perfil en la llamada a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).
-   Los modelos de apariencia de color se inicializan directamente desde los perfiles de CAM. Hay un perfil de CAM para cada perfil en la llamada a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/). Sin embargo, se puede especificar el mismo perfil de CAM para más de un perfil.
-   Las descripciones de los límites de la gama se inicializan a partir de un objeto de modelo de dispositivo y un objeto CAM. Hay una descripción de límite de gama para cada perfil en la llamada a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).
-   Los modelos de asignación de gamas se inicializan a partir de dos límites de gama y un intento. Debe crear un modelo de asignación de gama entre cada par de modelos de dispositivo creados a partir de la llamada a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/). Tenga en cuenta que esto significa que se usa un modelo de mapa de gama menos que el modelo de dispositivo. Dado que el número de intentos coincide con el número de modelos de dispositivo, también hay una intención más de lo necesario. Se omite el primer intento de la lista. Le guiará a través de la lista de modelos de dispositivos y intenciones, creando modelos de asignación de gama. Seleccione los modelos de dispositivo primero y segundo y el segundo intento y, a continuación, inicialice el modelo de asignación de la primera gama. Seleccione los modelos de dispositivo segundo y tercero y el tercer intento y, a continuación, inicialice el modelo de asignación de la segunda gama. Continúe de esta manera hasta que haya creado todos los modelos de asignación de gama.

Cuando los perfiles se han procesado correctamente y todos los objetos intermedios se han creado e inicializado, puede crear la transformación CITE con la siguiente llamada. *PDestCAM* y *pDestDM* son los asociados al último perfil en la llamada a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).


```C++
HRESULT CreateCITEColorTransform(
 __inout     IDeviceModel          *pSourceDM,
 __inout     IColorAppearanceModel *pSourceCAM,
 __in        GamutMapArray         *pGamutMapArray,
 __inout     IColorAppearanceModel *pDestCAM,
 __inout     IDeviceModel          *pDestDM,
             EColorTransformMode    eTransformMode,
 __deref_out IColorTransform      **ppCTS
 );
```



## <a name="support-for-plug-ins"></a>Compatibilidad con complementos

Un problema relacionado con la configuración de la lista de transformación es validar si un complemento necesario está disponible. El siguiente modificador de modelo proporciona esta directiva para controlar este comportamiento. La administración de esta lista de transformación es un método de la estructura de transformación optimizada interna, pero cada método de modelo proporciona el puntero a sí mismo y su propio conjunto de valores de parámetro.

El modo debe ser uno de los siguientes.

-   TfmRobust: Si un perfil de medición especifica un complemento preferido y el complemento no está disponible, el nuevo sistema CTE usará el complemento de línea de base. Si ninguno de los complementos está disponible, la transformación informará de un error.
-   TfmStrict: si ColorContext especifica un complemento preferido, el complemento debe estar disponible. Si no se encuentra ningún complemento preferido, se usará el complemento de línea de base. Si ninguno de los complementos está disponible, la transformación informará de un error.
-   TfmBaseline: solo se pueden usar complementos de línea de base en AddMeasurementStep. Si ColorContext especifica un complemento preferido, se omitirá el complemento. Si el complemento de línea de base no está disponible, la transformación informará de un error.

## <a name="transform-execution"></a>Ejecución de transformación

La función [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) de la API de ICM 2,0 convierte una matriz de colores del [espacio de colores](c.md) de origen en el espacio de colores de destino, tal y como se define en una transformación de color. Esta función comprueba internamente una matriz de colores en caché para habilitar la coincidencia inmediata de los colores transformados normalmente. Esta transformación admite matrices de bytes por canal de 8 bits y matrices de tipo float de 32 bits por canal. Todos los demás formatos se convertirán antes de pasar a la nueva CTE.

La función [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) de la API de ICM 2,0 traduce los colores de un mapa de bits con un formato definido para producir otro mapa de bits en un formato solicitado. Esta función comprueba internamente una matriz de colores en caché para habilitar la coincidencia inmediata de los colores transformados normalmente. Para evitar demasiadas rutas de acceso de código, compatibilidad y la complejidad de las pruebas, en realidad solo se admite un número limitado de formatos de mapa de bits en el motor de transformación y interpolación. Esta función debe traducir los formatos de mapa de bits entrantes y salientes no nativos en formatos admitidos de forma nativa para su procesamiento. Esta transformación solo admite mapas de bits de bytes por canal de 8 bits y mapas de bits Float de canal de 32. Todos los demás formatos se convertirán antes de pasar a la nueva CTE.

 

### <a name="sequential-transform-execution"></a>Ejecución de transformación secuencial

Si el parámetro *dwFlags* tiene el \_ bit de transformación secuencial establecido cuando se llama a las funciones ICM [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) o **CreateMultiProfileTransform** , los pasos de transformación se ejecutan secuencialmente. Esto significa que el código recorre cada modelo de dispositivo, modelo de apariencia de color y modelo de asignación de gama por separado, según lo especificado por la llamada a **CreateColorTransform** o **CreateMultiProfileTransform** . Esto puede ser útil para depurar los módulos de complemento, pero es mucho más lento que la ejecución a través de una transformación optimizada. Por lo tanto, la ejecución en modo secuencial no se recomienda para el software de producción. Además, puede haber pequeñas diferencias en los resultados obtenidos en modo secuencial y en modo optimizado. Esto se debe a las variaciones introducidas cuando las funciones se concatenan juntas.

### <a name="creation-of-optimized-transforms"></a>Creación de transformaciones optimizadas

Una transformación optimizada es una tabla de búsqueda multidimensional. La tabla puede ser procesada por un motor de interpolación multidimensional, como la interpolación tetrahedral, que aplica los colores de entrada a la transformación. En la siguiente sección se describe cómo se crean las tablas de búsqueda optimizadas. En la sección siguiente se describe cómo interpolar dentro de las tablas de búsqueda optimizadas.

## <a name="sparse-lookup-tables"></a>Tablas de búsqueda dispersas

Las impresoras convencionales tienen tintas CMYK. Para ampliar la gama, un enfoque consiste en agregar nuevas tintas al sistema. Las tintas que se agregan normalmente son colores que las tintas CMYK tienen dificultades de reproducción. Las opciones comunes son naranja, verde, rojo, azul, etc. Para aumentar la "resolución aparente", se pueden usar tintas con diferentes matices, por ejemplo, cian claro, magenta claro, etc. En efecto, el dispositivo de impresora tiene más de cuatro canales.

Aunque las impresoras son dispositivos de salida, también realizan la conversión de color del espacio de dispositivo a otro espacio de colores. En el caso de una impresora CMYK, esto sería una transformación de CMYK a XYZ o el "modelo de avance" de la impresora. Al combinar el modelo hacia delante con otras transformaciones, es posible emular una impresión CMYK en otro dispositivo. Por ejemplo, una impresora CMYK en un monitor RGB haría posible un mecanismo de prueba que eMule una impresión de esa impresora CMYK en un monitor. Del mismo modo, también se aplica a las impresoras de alta fidelidad. Una conversión CMYKOG a RGB permite la prueba de la impresora CMYKOG en un monitor.

El enfoque convencional para implementar esa conversión de color es mediante una LUT uniforme. Por ejemplo, en un perfil ICC para una impresora CMYKOG, la especificación ICC asigna una etiqueta A2B1 que almacena un LUT uniforme que representa un muestreo uniforme en el espacio de dispositivo CMYKOG del modelo de avance, que va desde CMYKOG hasta el espacio de conexión del perfil ICC (CIELAB o CIEXYZ). El perfil de vínculo de dispositivo ICC permite una transformación directa desde el espacio de dispositivo CMYKOG a cualquier espacio de colores, incluido un espacio de dispositivo, también en forma de un LUT muestreado de manera uniforme en el espacio CMYKOG. El muestreo nunca se realiza con los niveles 256 (profundidad de bits 8) debido al enorme LUT resultante, excepto en el caso de los dispositivos monocromáticos (1 canal). En su lugar, se usa el muestreo con profundidad de bits inferior; algunas opciones típicas son 9 (profundidad de bits 3), 17 (profundidad de bits 4), 33 (profundidad de bits 5). Con el número de niveles inferior a 256 en cada canal, el LUT se usa junto con un algoritmo de interpolación para generar el resultado si un nivel está entre dos niveles muestreados.

Aunque un LUT uniforme es conceptualmente sencillo de implementar y la interpolación en un LUT uniforme suele ser eficaz, el tamaño de LUT aumenta exponencialmente con la dimensión de entrada. De hecho, si *d* es el número de pasos que se usan en el LUT uniforme y *n* es el número de canales en el espacio de colores de origen, el número de nodos de LUT ![ muestra la variable para el número de nodos de una LUT. ](images/transformcreation-image002.gif) Claramente, el número de nodos demanda rápidamente tanto almacenamiento en memoria como los sistemas informáticos de primera línea tienen dificultades para controlar la demanda. En el caso de los dispositivos con seis o ocho canales, una implementación de ICC del perfil de dispositivo requiere el uso de pocos pasos en el LUT, a veces, incluso hasta cinco pasos en la tabla A2B1 para mantener el perfil en megabytes en lugar de en gigabytes. Obviamente, el uso de un menor número de pasos aumenta el error de interpolación, ya que ahora hay menos ejemplos. Dado que LUT debe ser uniforme, la precisión en todo el espacio de colores se degrada incluso en esas regiones del espacio donde una diferencia de color significativa puede deberse a un pequeño cambio en el valor del dispositivo.

En dispositivos con más de cuatro Colorants, algunos subespacios de todo el espacio de dispositivo son más importantes que otros. Por ejemplo, en el espacio CMYKOG, las tintas aguamarina y verde rara vez se usan juntas porque sus matices se superponen en gran medida. Del mismo modo, las tintas amarillas y naranjas se superponen en gran medida. Una reducción uniforme en el número de pasos se puede ver como una degradación general de la calidad en todo el espacio de colores, que es algo que se puede permitir para las combinaciones de tinta improbables, pero no para las combinaciones más probables o importantes.

Aunque una LUT muestreada de forma uniforme es sencilla y eficaz para la interpolación, impone grandes requisitos de memoria a medida que aumenta la dimensión. En realidad, mientras un dispositivo puede tener seis o ocho canales, rara vez se usan simultáneamente. En la mayoría de los casos, la transformación color de entrada a color tiene solo unos pocos Colorants "activos" y, por tanto, reside en un espacio de colores inferior. Esto también significa que la interpolación se puede realizar de forma más eficaz en ese espacio inferior dimensional porque la interpolación es más rápida cuando la dimensión es menor.

Por lo tanto, el enfoque consiste en le interese estratificar el espacio de dispositivo completo en subespacios de varias dimensiones. Y dado que las dimensiones inferiores (las que combinan tres o cuatro Colorants) son más importantes, stratifying el espacio, también puede aplicar diferentes tasas de muestreo; es decir, un número diferente de pasos, a las partes; aumento de las tasas de muestreo para las dimensiones más bajas, lo que reduce las dimensiones más altas.

Para corregir las anotaciones, *n* es el número de canales en el espacio de colores de origen de la transformación de color que desea muestrear. También puede hacer referencia a *n* como la dimensión de entrada y ![ muestra n mayor o igual que 5.](images/transformcreation-image004.gif) , a menos que se especifique lo contrario.

Los bloques de creación básicos son LUTs de varias *dimensiones* de entrada y tamaños, en lugar de un LUT uniforme con la dimensión de entrada *n*. Para ser más precisos, un *LUT* es un Lattice rectangular impuesto en un cubo de unidad; es decir, todas las coordenadas del dispositivo se normalizan en el intervalo \[ 0, 1 \] ). Si es la dimensión de entrada de LUT (tenga en cuenta que no tiene que ser igual a *n*, aunque ![ muestra V menor o igual que n.](images/transformcreation-image006.gif) se requiere) y se compone de cuadrículas de muestreo unidimensionales de ν:

Samp *i*: ![ muestra una cuadrícula de muestreo unidimensional.](images/transformcreation-image008.gif)

donde todos los *x <sub>j</sub>s* deben estar en el intervalo \[ 0, 1 \] , ![ muestra un superíndice (i).](images/transformcreation-image010.gif) es el número de pasos para el muestreo de *canal n que* debe ser al menos 1 y ![ muestra un spuperscript de X (subíndice) d (i).](images/transformcreation-image012.gif) debe ser 1. Por otro lado, ![ muestra un superíndice X (subíndice 1).](images/transformcreation-image014.gif) no es necesario que sea 0.

Solo se definirán los dos casos especiales siguientes de LUT.

*Closed LUT*: se trata de un LUT con el requisito adicional que, para cada samp *<sub>i</sub>*, ![ muestra un superíndice X (subíndice 1) es igual a 0.](images/transformcreation-image016.gif) y ![ muestra un superíndice (i) mayor o igual que 2.](images/transformcreation-image018.gif) . Un LUT cerrado uniforme es un LUT cerrado que tiene el mismo ![ muestra un superíndice d (i).](images/transformcreation-image010.gif) para cada canal, los nodos se espacian uniformemente entre 0 y 1.

*Open LUT*: se trata de un LUT con el requisito adicional que, para cada samp *i*, ![ muestra un superíndice X (subíndice 1) mayor que 0.](images/transformcreation-image020.gif) . Es correcto que se ![ muestre un superíndice d (i) igual a 1.](images/transformcreation-image022.gif) .

El objetivo es le interese estratificar el cubo de unidad \[ 0, 1 \] *n* en una colección de LUTs cerrados y abrir LUTs, de forma que toda la colección abarque el cubo de unidad. Es conceptualmente más sencillo organizar estas "LUT estratos" por sus dimensiones, de modo que en el nivel superior:

![Muestra el nivel superior para la organización de las estratoss de U T según sus dimensiones.](images/transformcreation-image024.png)

donde ![ muestra el subíndice del Sigma k.](images/transformcreation-image026.gif) es la "colección *estratos de dimensiones* ". Tenga en cuenta que la dimensión estratos comienza en 3 en lugar de 0; es decir, Points, dado que la interpolación de combinaciones de tres Colorant se puede controlar sin necesidad de demasiados requisitos de memoria.

## <a name="description-of-the-lut-strata"></a>Descripción de LUT estratos

En esta implementación:

1. ![Muestra el subíndice 3 de Sigma.](images/transformcreation-image028.gif) se compone de LUTs cerrados con tres entradas, una de cada combinación posible de tres Colorants elegidos fuera de la Colorants *n* .

2. ![Muestra el subíndice de Sigma 4.](images/transformcreation-image030.gif) consta de un LUT cerrado para la combinación CMYK (o los cuatro primeros Colorants), junto con ![Muestra (n en 4) menos 1.](images/transformcreation-image032.png) Abra LUTs para todas las demás combinaciones de cuatro Colorant. Al crear la combinación CMYK, se reconoce que es una combinación importante.

3. Para ![ muestra k igual a 5,..., n.](images/transformcreation-image034.gif) , ![ Muestra el subíndice del Sigma k.](images/transformcreation-image026.gif) consta de los ![ programas (n sobre k).](images/transformcreation-image037.gif) Abra LUTs, uno para cada combinación posible de elegir *k* Colorants del total de *n* Colorants.

Sigue especificando los tamaños de LUTs. La diferencia clave entre el LUTs abierto y el cerrado es que el LUTs abierto no se superpone y el LUTs cerrado podría superponerse en las caras del límite. El hecho de que el muestreo unidimensional en un LUT abierto no contenga 0, esencialmente significa que a un LUT abierto le falta la mitad de los lados del límite; por lo tanto, el nombre "abrir". Si dos LUTs no se superponen, puede usar un número diferente de pasos o ubicaciones de nodo en cada canal. Lo mismo no es cierto si dos LUTs se superponen. En ese caso, si el número de pasos o las ubicaciones de nodo son diferentes, un punto que esté en la intersección de los dos LUTs recibirá un valor de interpolación diferente en función de la LUT que se use en la interpolación. Una solución sencilla a este problema es usar el muestreo uniforme con el mismo número de pasos cada vez que dos LUTs se superponen. En otras palabras:

Todos los LUTs cerrados (los tres Colorant LUTs y el LUT CMYK de esta implementación) deben ser uniformes y tener el mismo número de pasos, que se indican como *d*.

Los dos algoritmos siguientes se pueden usar para determinar el número de pasos *d* para LUTs cerrados y el número de pasos para LUTs abierto.

## <a name="algorithm-1"></a>Algoritmo \# 1

Este algoritmo no requiere una entrada externa.

Todos los LUTs cerrados serán uniformes con un número *d* de pasos.

Todo el LUTs abierto de la dimensión *k* tendrá el mismo número de pasos que ![ d (k).](images/transformcreation-image039.gif) en cada canal de entrada, los nodos se espacian equitativamente. es decir, para cada ![ muestra, es igual a 1, 2,..., k.](images/transformcreation-image041.gif) .

Samp *i*: ![ muestra el algoritmo samp i.](images/transformcreation-image043.png)

Por último, especifique *d* y *d* (*k* ) en la tabla 1 siguiente. Los tres modos, "prueba", "normal" y "mejor" son los valores de calidad de ICM 2,0. En esta implementación, el modo de prueba tiene la superficie de memoria más pequeña y el mejor modo tiene la superficie de memoria más grande.

Para implementar este algoritmo, debe llamar al siguiente algoritmo \# 2. Los usuarios pueden especificar sus propias ubicaciones de muestreo, usando las tablas como guía.

## <a name="algorithm-2"></a>Algoritmo \# 2

Este algoritmo requiere una entrada externa en forma de una lista de ubicaciones de muestreo "importantes", pero es más adaptable y puede ahorrar espacio en memoria.

La entrada necesaria es una matriz de valores de dispositivo proporcionada por el usuario. Estos valores de dispositivo indican qué región del espacio de colores del dispositivo es importante; es decir, qué región se debe muestrear más.

Todos los LUTs cerrados serán uniformes con el número *d* de pasos descritos en el algoritmo \# 1. Los valores de *d* se proporcionan en la tabla 1.

*(a) LUT cerrado uniforme*



|         | Modo de prueba | Modo Normal | Mejor modo |
|---------|------------|-------------|-----------|
| ***d*** | 9          | 17          | 33        |



 

*(b) abrir LUT*



| Dimensión de entrada | Modo de prueba | Modo Normal | Mejor modo |
|-----------------|------------|-------------|-----------|
| 4               | 5          | 7           | 9         |
| 5               | 2          | 3           | 3         |
| 6               | 2          | 3           | 3         |
| 7               | 2          | 2           | 2         |
| 8 o más       | 2          | 2           | 2         |



 

**Tabla 1:** Tamaños de LUT usados en el algoritmo

Cada LUT abierto puede tener un número diferente de pasos en cada canal de entrada, y las ubicaciones de muestreo no tienen que estar equidistantes. En el caso de una capa de LUT abierta determinada, existe una combinación Colorant asociada, por ejemplo, el ![ subíndice 1,..., c subscript k.](images/transformcreation-image045.gif) , donde ![ muestra el subíndice de C.](images/transformcreation-image047.gif) s son enteros distintos entre 1 y *n*. Son los índices de canal que se corresponden con el Colorants "activo" en este estratos.

Paso 1: filtrar la matriz de valores de dispositivo inscritos que no están incluidos en este estratos. Un valor de dispositivo muestra el subíndice ![ x subíndice 1, x subscript 2,..., x n.](images/transformcreation-image049.gif) se incluye en estratos, si y solo si ![ muestra un conjunto de valores para un canal.](images/transformcreation-image051.gif) y todos los demás canales son 0. Si el conjunto filtrado tiene *N* entradas, Let

![Muestra una ecuación que se va a utilizar si el conjunto filtrado tiene N entradas.](images/transformcreation-image053.png)

Para cada ![Muestra el valor 1, 2,..., k.](images/transformcreation-image041.gif) , recorra en iteración los pasos siguientes 2-5:

Paso 2: Si ![ muestra el valor provisional de subíndice d (k) igual a 1.](images/transformcreation-image055.gif) , Samp *i* solo tiene un punto, que debe ser 1,0. Pase a *la siguiente.* En caso contrario, continúe con el paso 3.

Paso 3: ordene los ejemplos filtrados en orden ascendente en el ![Muestra el subíndice de C.](images/transformcreation-image047.gif) canal.

Paso 4: definir la cuadrícula de muestreo "provisional" mediante los nodos

![Muestra los nodos que se usan para definir la cuadrícula de muestreo "provisional".](images/transformcreation-image057.png)

where ![Muestra j igual a 1, 2,..., d suscript provisional (k).](images/transformcreation-image059.gif) .

Paso 5: regular la cuadrícula tentativa para asegurarse de que se ajusta a la monotónica estricta y que termina con 1,0. Dado que la matriz ya está ordenada, los nodos de la cuadrícula tentativa ya son nondecreasing monotónica. Sin embargo, los nodos adyacentes podrían ser idénticos. Puede corregirlo quitando nodos idénticos, si es necesario. Por último, después de este procedimiento, si el punto final es inferior a 1,0, reemplácelo por 1,0.

Tenga en cuenta que el paso 5 es el motivo por el que el estratos de LUT puede tener un número diferente de pasos en cada canal. Después de regularización, el número de pasos de un canal puede ser menor que ![Muestra el provisional de subíndice d (k).](images/transformcreation-image061.gif) .

## <a name="interpolation"></a>Interpolación

Puede construir la estratificación del cubo de unidad mediante Open LUT estratos y Closed LUT estratos. Para realizar la interpolación con esta "estructura LUT dispersa", siga estos pasos. Asuma un valor de dispositivo de entrada determinado ![Muestra el subíndice 1, x subíndice 2,..., X subscript n).](images/transformcreation-image049.gif) .

Paso 1: determinar el número de canales "activos". Es el número de canales distintos de cero. Esto determina la dimensión estratos *k* para buscar la capa que lo contiene. Más concretamente, la dimensión estratos es 3 si el número de canales activos es ![ menor o igual que 3.](images/transformcreation-image063.gif) de lo contrario, la dimensión estratos es la misma que el número de canales activos.

Paso 2: dentro de ![Muestra el subíndice del Sigma k.](images/transformcreation-image026.gif) , busque la capa que lo contiene. Un valor de dispositivo se encuentra en un estrato abierto si todos los canales correspondientes a la capa tienen un valor distinto de cero y todos los demás canales son cero. Un valor de dispositivo se encuentra en un estrato cerrado si cada canal no representado por el estrato es cero. Si no se encuentra ninguna capa que contenga, hay una condición de error. Cancelar e informar de un error. Si se encuentra una capa que contiene, continúe con el paso siguiente.

Paso 3: si se cierra la capa que lo contiene, cualquier algoritmo de interpolación conocido puede realizar la interpolación dentro de la capa. En esta implementación, la elección del algoritmo es la interpolación tetrahedral. Si el estrato que lo contiene está abierto y el valor del dispositivo se encuentra estrictamente dentro de la capa, es decir,

![Muestra el subíndice X es mayor o igual que... ](images/transformcreation-image065.gif) primer nodo en *i* TH Channel

donde *i* es un índice de canal para la capa, el algoritmo de interpolación estándar, como la interpolación tetrahedral, funciona.

Si ![ muestra el primer nodo X de subíndice i menor que... ](images/transformcreation-image067.gif) en el canal *i* TH , el valor del dispositivo entra en el "intervalo" entre la capa y los subespacios de la dimensión inferior. Este MOI no está relacionado con un algoritmo de interpolación por se, por lo que se puede usar cualquier algoritmo de interpolación para interpolar dentro de este "intervalo", aunque el algoritmo preferido es la interpolación transfinita siguiente.

La arquitectura del módulo de interpolación se muestra en las dos partes de la ilustración 1.

![Diagrama que muestra la parte uno de la arquitectura del módulo de interpolación.](images/transformcreation-image068.png)

![Diagrama que muestra la segunda parte de la arquitectura del módulo de interpolación.](images/transformcreation-image070.png)

**Figura 1:** Arquitectura del módulo Intepolation

Como se explicó anteriormente, este algoritmo es capaz de obtener un muestreo razonablemente denso en las regiones del espacio del dispositivo que contiene una combinación importante de Colorants, a la vez que minimiza el tamaño total de LUTs necesario. En la tabla siguiente se muestra una comparación del número de nodos necesarios para la implementación LUT dispersa (mediante \# el algoritmo 1 y el modo normal) y la implementación de LUT uniforme correspondiente.



| **Número de canales de entrada** | **LUT disperso** | **LUT uniforme** |
|------------------------------|----------------|-----------------|
| 5                            | 142498         | 1419857         |
| 6                            | 217582         | 24137567        |
| 7                            | 347444         | 410338673       |
| 8                            | 559618         | 6975757441      |



 

## <a name="interpolation-within-a-unit-cube"></a>Interpolación dentro de un cubo de unidad

Un paso básico en el caso de la cuadrícula rectangular es la interpolación dentro de una celda envolvente. Para un punto de entrada, puede determinar fácilmente la celda envolvente. En una cuadrícula rectangular, se especifica el valor de salida en cada uno de los vértices (puntos de vértices) de la celda envolvente. También son las únicas condiciones de límite (BCs) que un interpolant debe cumplir: el interpolant debe atravesar todos estos puntos. Tenga en cuenta que estas condiciones de límite están en puntos "discretos", en este caso los puntos de esquina 2n de la celda, donde n es la dimensión del espacio de colores.

Resulta útil formalizar el concepto de condiciones de límite antes de continuar. Para cualquier subconjunto del límite de la celda envolvente (el cubo de unidad en n dimensiones), una condición de límite en S es una especificación de una función BC: S → RM, donde m es la dimensión de salida. En otras palabras, un interpolant, que puede estar indicado como interp: \[ 0, 1 \] n → RM, es necesario para satisfacer: interp (x) = BC (x) para todo x en S.

En el escenario estándar de interpolación en el cubo de unidad, S es el conjunto de puntos discretos que son los vértices 2N del cubo.

Ahora puede generalizar las condiciones de límite para solucionar los problemas descritos anteriormente y proporcionar un nuevo algoritmo de interpolación dentro del cubo de unidad. En lugar de permitir solo puntos de límite discretos, se pueden imponer condiciones de límite en todo el límite del cubo. Las suposiciones exactas son las siguientes:

(a) el punto vn = (1,1,..., 1) es especial y solo se permite una condición de límite discreto. En otras palabras, no se pueden imponer condiciones de límite continuo en las n caras del límite XI = 1 (i = 1,..., n).

(b) para cada una de las n caras de límite restantes XI = 0 (i = 1,..., n), la condición de límite se puede imponer en todo el rostro, con la condición de compatibilidad que si dos caras intersectan, las condiciones de límite en las caras deben coincidir en la intersección.

(c) los vértices no incluidos en las caras con condición de límite tendrán una condición de límite individual (discreta).

Puede hacer referencia a una condición de límite discreto como datos finitos y una condición de límite continuo como datos transfinitos en la explicación de la interpolación en datos finitos y transfinitos.

En primer lugar, revise la interpolación estándar de tetrahedral (por ejemplo, la usada en la patente de Sakamoto) que ayuda a establecer las notaciones para esta formulación determinada del problema. Se sabe que el cubo de unidad \[ 0, 1 \] n se puede subdividir en n. tetrahedra, parametrizado por el conjunto de permutaciones en n símbolos. Más concretamente, cada Tetrahedron se define mediante desigualdades.

![Muestra la fórmula para el inequalites de tetrahedrons.](images/transformcreation-image073.gif)

donde σ: {1, 2,.., n} → {1,2,..., n} es una permutación de "Symbols" 1, 2,..., n, es decir, es una asignación de bijective del conjunto de n símbolos. Por ejemplo, si n = 3 y σ = (3, 2, 1), es decir, σ (1) = 3, σ (2) = 2, σ (3) = 1, el Tetrahedron correspondiente se define mediante z ≥ y ≥ x, donde la notación común x, y, z se usa para x1, x2, X3. Tenga en cuenta que estos tetrahedrons no están separados entre sí. En lo que respecta a la interpolación, los puntos que se basan en una esfera común de dos tetrahedrons distintos tendrán el mismo valor de interpolación independientemente de qué Tetrahedron se use en la interpolación. Aun así, en el escenario estándar de la interpolación en puntos finitos, para un punto de entrada determinado (x1,..., xn), determine en primer lugar en qué Tetrahedron se encuentra, o de forma equivalente, el σ de permutación correspondiente, tetrahedral interpolant se define como

![Muestra la ecuación que define el interpolant de tetrahedral.](images/transformcreation-image075.png)

where ![Muestra la ecuación para los vectores de base estándar.](images/transformcreation-image077.png) para i = 1,..., n y E1,..., en son los vectores de base estándar. Antes de pasar a la generalización, tenga en cuenta que V0, V1,..., vn son los vértices de Tetrahedron y ![Muestra las coordenadas Barycentric.](images/transformcreation-image079.png) son las "coordenadas Barycentric".

Para el caso general de BCs en caras limítrofes, puede usar el concepto de proyección Barycentric. Como antes, para un punto de entrada determinado (x1,..., xn), determine primero en qué Tetrahedron se encuentra, o equivalente, el σ de permutación correspondiente. A continuación, realice una serie de proyecciones de Barycentric, como se indica a continuación. La primera proyección ![Muestra el subíndice BProj 1 (x).](images/transformcreation-image081.gif) envía el punto al plano. ![Muestra la diferencia de subíndice X (1) igual a 0.](images/transformcreation-image083.gif) vaya ![Muestra el subíndice X igual a V n.](images/transformcreation-image085.gif) en cuyo caso no se cambia. La definición precisa de la asignación BProj se define de la siguiente manera:

![Muestra la ecuación para la definición precisa de la asignación BProj.](images/transformcreation-image087.png)

con ![Muestra la ecuación del subíndice P.](images/transformcreation-image089.png) y k = 1, 2,..., n.

En el caso ![Muestra que X es igual al subíndice n de V.](images/transformcreation-image085.gif) , puede detenerse porque BC se define en vn por hipótesis (a). En el caso ![Muestra que X no es igual a subíndice n.](images/transformcreation-image091.gif) , está claro que ![Muestra el subíndice BProj 1 (X).](images/transformcreation-image081.gif) tiene el componente σ (1) TH Annihilated. En otras palabras, está en una de las caras del límite. O bien, está en una superficie en la que se define BC, en cuyo caso puede detenerse o realizar otra proyección Barycentric ![Muestra el subscript BProj 2 (X ').](images/transformcreation-image093.gif) where ![Muestra el subíndice X ' igual al BProj 1 (X).](images/transformcreation-image095.gif) . Y si ![Muestra X ' ' = Bproj subscript 1 (X ').](images/transformcreation-image097.gif) está en una superficie en la que se define BC, puede detenerse; en caso contrario, realice otra proyección ![Muestra el subscript BProj 3 (X ' ').](images/transformcreation-image099.gif) . Dado que cada proyección annihilates un componente, la dimensión efectiva disminuye, por lo que sabe que el proceso debe detenerse finalmente. En el peor de los casos, realizará n proyecciones en la dimensión 0, es decir, los vértices del cubo, que se ajustan a la hipótesis (c), sabrá que se definirá BC en.

Suponiendo que se han realizado K proyecciones, con

![Muestra una ecuación que se va a usar suponiendo que se han realizado K proyecciones.](images/transformcreation-image101.png)

x (0) = x, el punto de entrada y BC se definen en x (k). A continuación, desenredar las proyecciones definiendo una serie de vectores de salida:

![Muestra las ecuaciones de una serie de vectores de salida.](images/transformcreation-image103.png)

where ![Muestra la ecuación del superíndice Y (K).](images/transformcreation-image105.gif) y, por último, obtiene la respuesta.

![Muestra interp (x) igual a y superíndice (0).](images/transformcreation-image107.gif)

## <a name="worked-example"></a>Ejemplo práctico

![Diagrama que muestra un ejemplo de cómo funciona la interpolación con un cubo de unidad.](images/transformcreation-image108.png)

**Figura 2:** Ejemplo de trabajo

Considere la situación que se muestra en la figura 2, donde n = 3, m = 1, y tiene el siguiente BCs:

(a) cuatro BCs discretos en los vértices

(0, 0, 1): β001

(0, 1, 1): β011

(1, 0, 1): β 101

(1, 1, 1): β 111

(b) un BC continuo en la esfera x3 = 0: F (x1, x2)

Cálculo \# 1: punto de entrada x = (0,8, 0,5, 0,2). La Tetrahedron envolvente está asociada a la permutación &lt; 1, 2, 3 &gt; .

primera proyección: ![Muestra la ecuación de la primera proyección.](images/transformcreation-image110.png)

Ya está en la esfera x3 = 0, por lo que puede detenerse. La sustitución hacia atrás proporciona entonces

![Muestra la respuesta para la primera proyección.](images/transformcreation-image112.png) que es la respuesta.

Cálculo \# 2: punto de entrada x = (0,2, 0,5, 0,8). La Tetrahedron envolvente está asociada a la permutación &lt; 3, 2, 1 &gt; .

primera proyección: ![Muestra la ecuación de la primera proyección del cálculo 2.](images/transformcreation-image113.png)

segunda proyección: ![Muestra la ecuación para la segunda proyección del cálculo 2.](images/transformcreation-image115.png)

tercera proyección: ![Muestra la ecuación para la tercera proyección del cálculo 2.](images/transformcreation-image117.png) , que se encuentra en la esfera x3 = 0. La sustitución hacia atrás proporciona entonces

![Muestra las dos primeras ecuaciones para la sustitución hacia atrás.](images/transformcreation-image119.png)

![Muestra la tercera ecuación para la sustitución hacia atrás.](images/transformcreation-image123.png), que es la respuesta final.

## <a name="applications"></a>APLICACIONES

*(a) interpolación Tetrahedral secuencial*

![Diagrama que muestra la interpolación tetrahedral secuencial.](images/transformcreation-image124.png)

**Figura 3:** Interpolación tetrahedral secuencial

Consulte la figura 3. Para interpolar entre dos planos en los que se han impuesto cuadrículas incompatibles, considere la posibilidad de que una celda incluya un punto P determinado en la ilustración. Los vértices "superiores" de la celda proceden directamente de la cuadrícula del plano superior. Los vértices de la parte inferior no son compatibles con la cuadrícula del plano inferior, por lo que toda la superficie se trata como si tuviera un BC con valores obtenidos mediante la interpolación en la cuadrícula del plano inferior. A continuación, se desactiva que este programa de instalación cumple las suposiciones (a), (b) y (c) anteriores, y se puede aplicar el algoritmo de interpolación.

También está claro que el algoritmo ha reducido la dimensión del problema de interpolación en 1, ya que el resultado es una combinación lineal de valores en los vértices de la cuadrícula superior y la interpolación en el plano inferior, que tiene una dimensión menos 1. Si existe una configuración de plano de sándwich similar en el plano inferior, puede aplicar el procedimiento en dicho plano, lo que reduce la dimensión en 1. Este procedimiento puede continuar hasta que llegue a la dimensión 0. Esta cascada de proyecciones y interpolaciones puede denominarse "interpolación Tetrahedral secuencial".

*(b) interpolación de huecos*

![Diagrama que muestra la interpolación de huecos.](images/transformcreation-image126.jpg)

**Figura 4:** Interpolación de huecos

Se trata de una cuadrícula impuesta en un cubo que se encuentra estrictamente dentro del cuadrante positivo. El cubo tiene una cuadrícula en él y cada plano de coordenadas tiene cuadrículas que no tienen necesariamente compatibilidad. Los "huecos" entre el cubo y los planos de coordenadas tienen una sección transversal en la que se "forma L" y no es receptiva a las técnicas estándar. Sin embargo, con la técnica introducida aquí, puede introducir fácilmente las celdas que cubren este intervalo. En la ilustración 4 se muestra una de estas. Las cuadrículas de los planos de coordenadas admiten la interpolación que proporciona la BCs necesaria para todas las caras inferiores de la celda, con un vértice restante cuya BC se proporciona en la esquina inferior del cubo.

## <a name="final-note-on-implementation"></a>Nota final sobre la implementación

En la aplicación real, el "cubo de unidad" que es la configuración básica del algoritmo se extrae de lattices más grandes y los valores en los vértices pueden requerir un cálculo caro. Por otro lado, también está claro que la interpolación tetrahedral requiere solo los valores en los vértices de Tetrahedron, que es un subconjunto de todos los vértices del cubo de unidad. Por lo tanto, es más eficaz implementar lo que se puede llamar "evaluación diferida". En una implementación de software del algoritmo anterior, es habitual tener una subrutina que toma el cubo de unidad y los valores en sus vértices como entrada. La evaluación diferida significa que en lugar de pasar los valores en los vértices, se pasa la información necesaria para evaluar los valores de los vértices, sin llevar a cabo realmente la evaluación. Dentro de la subrutina, la evaluación real de estos valores solo se llevará a cabo para los vértices que pertenezcan al Tetrahedron envolvente, una vez que se determine la Tetrahedron envolvente.

## <a name="lookup-table-for-use-with-high-dynamic-range-virtual-rgb-source-devices"></a>Tabla de búsqueda para su uso con dispositivos de origen RGB virtuales de rango dinámico alto

En el caso de que una transformación se construya con un dispositivo de origen modelado como un dispositivo RGB virtual, es posible que los valores de Colorant de origen sean negativos o mayores que Unity (1,0). Cuando esto ocurre, se hace referencia al dispositivo de origen como con un intervalo dinámico alto (HDR). En este caso, se debe tener en cuenta una consideración especial.

En el caso de las transformaciones HDR, los valores mínimo y máximo de cada canal Colorant se pueden determinar a partir del límite de la gama del dispositivo. Mediante el uso de estos valores, se aplica un escalado simple para cada canal de Colorant de forma que los valores de Colorant iguales al valor de Colorant mínimo se conviertan en 0,0 y los valores Colorant iguales a los Colorant máximos se conviertan en 1,0, con un ajuste de escala lineal de los valores entre para asignar linealmente entre 0,0 y 1,0.

### <a name="iccprofilefromwcsprofile"></a>ICCProfileFromWCSProfile

Dado que el propósito principal de esta característica es admitir versiones anteriores a la vista de Windows, debe generar perfiles ICC de la versión 2,2 como se define en la especificación ICC ICC. 1:1998-09. En algunos casos (consulte la siguiente tabla "línea de base para la asignación de clases de Perfil de ICC"), puede crear un perfil ICC basado en una matriz o en TRC desde un perfil WCS. En otros casos, el perfil de ICC se compone de LUTs. En el siguiente proceso se describe cómo crear AToB y BToA LUTs. Por supuesto, los perfiles de ICC también tienen otros campos. Algunos de los datos se pueden derivar del perfil WCS. Para otros datos, tendrá que desarrollar valores predeterminados inteligentes. El copyright se asignará a Microsoft; puesto que es la tecnología de Microsoft que se usa para crear el LUTs.

Este diseño debe funcionar para todos los tipos de modelos de dispositivos, incluidos los complementos. Siempre que el complemento tenga un modelo de dispositivo de línea de base asociado, se puede determinar el tipo de dispositivo subyacente.

La parte más difícil de crear un perfil de ICC es crear las tablas de búsqueda de AToB y BToA. Estas tablas se asignan entre el espacio del dispositivo, por ejemplo RGB o CMYK, y el espacio de conexión del perfil (PC), que es una variante de CIELAB. Esto es fundamentalmente el mismo que el proceso de administración del color que se usa en la transformación CITE para asignar desde el espacio de dispositivo al espacio de dispositivo. Sin embargo, debe tener la siguiente información para realizar la transformación.

1) Referencia de las condiciones de visualización de los equipos.

2) Gama de equipos de referencia.

3) Modelo de dispositivo que convierte entre los valores de los equipos y la colorimétrico.

El perfil WCS y su CAM asociado se proporcionan como parámetros. Hay dos modelos de dispositivo de línea base que convierten entre la codificación de los equipos y de la base de referencia. A continuación se explica el motivo por el que necesita dos.

1) Puede obtener las condiciones de visualización de referencia para los equipos de la especificación de formato de Perfil de ICC. La información proporcionada en la especificación de formato de Perfil de ICC es suficiente para calcular todos los datos necesarios para inicializar el CAM que usa el CMS. Para mantener la coherencia y la flexibilidad, esta información se almacena en un perfil de color WCS.

2) También puede usar un perfil WCS para almacenar ejemplos que definan la gama de referencia de los equipos. El sistema de administración del color (CMS) de CITE tiene dos maneras de crear límites de gama. Uno es para muestrear el espacio de dispositivo completo y usar el modelo de dispositivo para crear valores de medida. El segundo método consiste en usar ejemplos medidos del perfil para crear un límite de gama de referencia. Dado que la gama de equipos ICC es demasiado grande para crear una gama de referencia útil, el primer método no es adecuado. Pero el segundo método es un enfoque flexible basado en perfiles. Para volver a definir la gama de equipos de referencia, puede cambiar los datos de medición en el perfil de dispositivo PCS.

3) Los equipos ICC son un modelo de un dispositivo ideal. Al crear un modelo de los equipos como un dispositivo real, puede aprovechar el proceso de administración del color que se usa en la CMM inteligente. La creación de un modelo de dispositivo desde la colorimétrico a la codificación de equipos es sencilla. Simplemente se asigna entre los valores de colorimétrico verdadero y los valores codificados de los equipos. Dado que la interfaz CMS para los modelos de dispositivos solo admite valores XYZ, es posible que también tenga que asignar entre XYZ y LAB. Se trata de una transformación conocida. Este modelo se describe en el documento 2.2.02 "Baseline Device models" en las secciones 7,9 y 7,10.

Es posible que tenga que realizar una asignación de gama, si la gama del dispositivo es mayor que la gama de los equipos. La línea de base GMMs se puede usar para este propósito. Tenga en cuenta que un perfil ICC creado correctamente tiene tablas de búsqueda para los intentos de referencia colorimétrica, perceptual y saturación relativos, aunque puede que todos señalen al mismo LUT internamente.

![Diagrama que muestra la creación de una T o B L U T.](images/transformcreation-image128.png)

**Figura 5:** Creación de un LUT de AToB

Este proceso se muestra en la figura 5. En primer lugar, el modelo de dispositivo se inicializa a partir de los datos del perfil de DM. A continuación, construya un límite de gama de dispositivos como se indica a continuación. Un muestreo de datos del modelo de dispositivo se ejecuta a través del modelo de dispositivo para obtener datos de la colorimétrico. Los datos de la colorimétrico se ejecutan a través del CAM para crear los datos de apariencia. Los datos de apariencia se usan para crear el límite de la gama de dispositivos.

A continuación, use los datos del perfil de medición de PCS de referencia para crear un límite de gama para los equipos.

Use los dos límites de la gama que acaba de crear para inicializar un GMM. A continuación, use el modelo de dispositivo, GMM y el modelo de dispositivo PCS para crear una transformación. Ejecute un muestreo del espacio del dispositivo a través de la transformación para crear un LUT de AToB.

![Diagrama que muestra la creación de una T o B L U T mediante un muestreo de espacio de P C S.](images/transformcreation-image130.png)

**Ilustración 6:** Creación de un LUT de BToA

En la ilustración 6 se muestra la creación de BToA LUT. Esto es casi idéntico a la creación de un AToB LUT, con los roles de origen y destino intercambiados. Además, debe obtener una muestra de la gama completa de PCS para crear el LUT.

Tenga en cuenta que, dado que el CAM (CIECAM02 en WCS) participa en el proceso, la adaptación cromática entre el punto blanco del medio y el punto blanco de los equipos (asignada por ICC a la de D50) se aplica de forma transparente al CAM.

## <a name="hdr-virtual-rgb-devices"></a>Dispositivos RGB virtuales de HDR

Se debe tener en cuenta una consideración especial al generar perfiles para dispositivos RGB virtuales de HDR; es decir, los dispositivos para los que los valores de Colorant pueden ser menores que 0,0 o superior a 1,0. En la generación de ATOB LUT, se crea un conjunto mayor de LUTs de entrada 1D. Los valores Colorant se escalan y se desplazan al rango 0.. 1 usar los valores mínimos y máximos de Colorant en el perfil WCS.

Dado que es probable que no se llene completamente el espacio Colorant de los dispositivos HDR, también se proporciona compatibilidad especial en el LUT 3D de la etiqueta. Para controlar los colores de la región dispersa, los Colorants se vuelven a codificar para que se pueda lograr la extrapolación más allá de 0,0 y 1,0. El intervalo utilizado es-1.. + 4.

Debido al cambio de escalado aplicado para el LUT en 3D, se crea un conjunto de LUTs de salida 1D para asignar el resultado al intervalo 0. 1.

## <a name="more-than-one-pcs"></a>Más de un PC

El ICC encontró que un PC no era lo suficientemente flexible como para satisfacer todos los usos previstos de un CMS. En la versión 4 de la especificación de perfil, el ICC ha aclarado que en realidad hay dos codificaciones de equipos. Se usa uno para los intentos de la colorimétrico. otro se usa para la intención perceptual. (No se especifica ningún PC para la intención de saturación. El ICC ha dejado este elemento ambiguo). Los equipos colorimétrico tienen una luminosidad mínima y máxima especificada, pero los valores croma y matiz van a aproximadamente ± 127. Este PC es similar a un prisma rectangular. Como se mencionó anteriormente, el volumen de los equipos perceptuales es similar a la gama de una impresora de inyección de tinta.

Los dos PCSs ICC también tienen dos codificaciones digitales diferentes. En los equipos perceptuales, un valor de cero representa una luminosidad de cero. En los equipos colorimétrico, un valor de cero representa la luminosidad mínima de los equipos, que es mayor que cero. Puede resolver este problema si tiene un modelo de dispositivo diferente para cada una de las codificaciones de equipos.

## <a name="gamut-mapping"></a>Asignación de gamas

Para crear el LUTs de AToB en un perfil ICC, asigne desde la gama de dispositivos al espacio de equipos adecuado. Para crear el LUTs BToA, puede asignar desde el espacio PCS a la gama de dispositivos. La asignación para AToB LUTs es bastante similar a la que se usa en un CMS basado en medida. En el caso de los equipos perceptuales, asigne la gama plausible del dispositivo al límite de la gama de equipos perceptuales, mediante el recorte o la compresión para cualquier color fuera de la gama. En el caso de las intenciones colorimétrica, es posible que tenga que recortar la luminosidad, pero los valores croma y matiz van a caber en la gama de equipos de la colorimétrico.

La asignación para el LUTs BToA es un poco diferente. Los intentos de la colorimétrico son fáciles de seguir; solo tiene que recortar los valores de PC a la gama de dispositivos. Pero el ICC requiere que todos los valores posibles de los equipos se asignen a algún valor de dispositivo, no solo a los de la gama de referencia de los equipos perceptuales. Por lo tanto, debe asegurarse de que GMMs pueda controlar los colores de origen que se encuentran fuera de la gama de referencia. Esto puede controlarse recortando esos colores en el límite de la gama de dispositivos.

## <a name="baseline-device-to-icc-profile-class-mapping"></a>Asignación de clase de Perfil de dispositivo de línea base a ICC



| Tipo de dispositivo de línea de base              | Clase de Perfil de ICC       | Comentario                                                                      |
|-----------------------------------|-------------------------|-----------------------------------------------------------------------------|
| Dispositivo de captura RGB                | Dispositivo de entrada ("SCNR")   | Los equipos son CIELAB. AToB0Tag es el dispositivo a los equipos con intención colorimétrica relativa. |
| CRT, monitor LCD                  | Mostrar dispositivo ("MNTR") | Los equipos son CIEXYZ. Vea lo siguiente para la conversión de modelos.                      |
| Proyector RGB                     | Espacio de colores ("espacio")    | Los equipos son CIELAB.                                                              |
| Impresora RGB y CMYK              | Dispositivo de salida ("PRTR")  | Los equipos son CIELAB.                                                              |
| Dispositivo virtual RGB (caso no HDR) | Mostrar dispositivo ("MNTR") | Los equipos son CIEXYZ.                                                              |
| Dispositivo virtual RGB (caso de HDR)     | Espacio de colores ("espacio")    | Los equipos son CIELAB.                                                              |



 

La conversión de perfiles de monitor no implica la creación de LUTs, sino que consiste en crear un modelo de matriz o TRC. El modelo usado en ICC es ligeramente diferente del que se usa en el modelado de CRT o LCD WCS en el que falta el término "corrección negra". Concretamente, puede:

Modelo WCS: ![Muestra un modelo de W C.](images/transformcreation-image132.png)

Modelo ICC: ![Muestra un modelo I de c.](images/transformcreation-image134.png)

La conversión del modelo WCS al modelo ICC se realiza como se indica a continuación.

Definir nuevas curvas:

![Muestra una matriz para definir las curvas nuevas.](images/transformcreation-image136.png)

No son curvas de reproducción de tonos porque no se asignan de 1 a 1. Una normalización lo logrará. Las definiciones finales del modelo ICC son:

![Muestra las definiciones finales del modelo I de c.](images/transformcreation-image138.png)

![Muestra la matriz final del modelo I de c.](images/transformcreation-image140.png)

En el caso de los dispositivos virtuales RGB no HDR, también está generando un perfil ICC de visualización para la eficiencia de espacio. En ese caso, la matriz de triestímulos de la matriz *M ICC* se puede obtener directamente de las principales del perfil WCS sin la conversión de modelo anterior. Un último, pero importante, tenga en cuenta que esta matriz de triestímulo debe adaptarse de forma cromática a D50 para cumplir con la especificación de ICC de los equipos. En otras palabras, las entradas de cada fila de la matriz que se va a codificar en el perfil de ICC deben sumar respectivamente a 96,42, 100 y 82,49. En la implementación actual, la adaptación cromática se realiza mediante CAT02, que también es la transformación de adaptación cromática utilizada en CAM02.

## <a name="black-preservation-and-black-generation"></a>Preservación de negro y generación de negro

La implementación de la preservación de negro está ligada a la generación del canal negro en los dispositivos que admiten un canal negro. Para ello, se recopila información sobre cada color de origen para permitir que los modelos de dispositivo que admiten un canal negro determinen la mejor manera de establecer el canal negro en la salida. Aunque la preservación negra es pertinente para las transformaciones de color que convierten entre un dispositivo de canal negro en otro, la generación en negro se implementa para todas las transformaciones que implican un dispositivo de destino de canal negro.

La información del canal negro se registra en una estructura de datos denominada [**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation). La estructura **BlackInformation** contiene un valor booleano que indica si el color contiene solo Colorant de color negro y un valor numérico que indica el grado de "negro" llamado peso negro. En el caso de los dispositivos de origen que admiten un canal negro, el peso negro es el porcentaje de Colorant negros en el color de origen. En el caso de los dispositivos de origen que no contienen un canal negro, el peso negro se calcula utilizando el otro Colorants y el valor de apariencia. Un valor denominado "pureza del color" se calcula tomando la diferencia entre el valor de Colorant máximo y el valor de Colorant mínimo dividido por el valor de Colorant máximo. Un valor denominado "luminosidad relativa" se calcula tomando la diferencia entre la luminosidad del color y la luminosidad mínima del dispositivo de destino dividida por la diferencia entre la luminosidad mínima y máxima del dispositivo de destino. Si el dispositivo de origen es un dispositivo aditivo (monitor o proyector), el peso negro se determina como 1,0 menos la pureza de color multiplicada por la luminosidad relativa. Por ejemplo, si el dispositivo de origen es un monitor RGB, se calculan el valor máximo y el valor mínimo de R, G y B para cada color y el peso negro viene determinado por la fórmula:

BW = (1,0 – (Max (R, G, B) – min (R, G, B))/Max (R, G, B)) \* luminosidad relativa

Si el dispositivo de origen admite la coloración de sustracción, por ejemplo, una impresora CMY, el Colorants individual debe ser "uno complementado" (restado de 1,0) antes de usarse en la fórmula anterior. Por lo tanto, para una impresora CMY, R = 1,0 – C, G = 1,0 – M y B = 1,0 – Y.

La información en negro de cada color procesado por la transformación de color se determina durante el proceso de traducción del color. La información solo en negro solo se determina si se especifica la conservación negra. El peso negro siempre se determina si el modelo de dispositivo de destino admite un Colorant negro. La información de color negro se pasa al modelo de dispositivo de destino a través del método [**ColorimetricToDeviceColorsWithBlack**](/previous-versions/windows/desktop/api/WcsPlugIn/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack) , que usa el LUT resultante.

Tenga en cuenta que, debido a la optimización de la transformación de color, el proceso anterior solo se produce durante la creación de la transformación optimizada LUT, no durante la ejecución del método TranslateColors.

## <a name="optimization-for-transforms-with-more-than-three-source-channels"></a>Optimización de transformaciones con más de tres canales de origen

El tamaño de la transformación optimizada viene determinado por varios factores: el número de canales de color en el dispositivo de origen, el número de pasos en la tabla para cada canal de color de origen y el número de canales de color en el dispositivo de salida. La fórmula para determinar el tamaño de la tabla de transformación es la siguiente:

Tamaño = número de pasos por origen de canal <sub>\ dispositivo (número \ de \ canales \ en \ origen \ dispositivo)</sub> x número de canales en el dispositivo de salida

Como puede ver, el tamaño de la tabla crece exponencialmente en función del número de canales en el dispositivo de origen. Muchos dispositivos de origen admiten tres canales de color, por ejemplo, rojo, verde y azul. Sin embargo, si un dispositivo de origen admite cuatro canales, como CMYK, el tamaño de la tabla y el tiempo necesario para construir la tabla aumentan en función del número de pasos. En un CMS basado en medida donde las transformaciones se construyen "sobre la marcha", este tiempo puede ser inaceptable.

Para reducir el tiempo necesario para construir la tabla de conversión de colores, es posible aprovechar dos hechos. En primer lugar, mientras que el dispositivo de origen puede admitir más de tres canales de color, el espacio de colores independiente del dispositivo intermedio (CIECAM02 ja <sub>c</sub> b <sub>c</sub> ) tiene solo tres canales de color. En segundo lugar, la parte que consume más tiempo del procesamiento no es el modelado de dispositivos (la conversión de coordenadas de color del dispositivo a valores triestímulos), sino la asignación de la gama. Con estos hechos, puede crear una tabla de conversión de colores preliminar que convierta los colores en el espacio de colores independiente del dispositivo a través de los pasos de asignación de gamas y, por último, a través del modelo de color del dispositivo de salida. La construcción de esta tabla es de dimensión tres. A continuación, construimos la tabla de conversión de colores final de la dimensión, convirtiendo las combinaciones de colores de origen en un espacio intermedio independiente del dispositivo y, a continuación, usando la tabla de conversión de colores preliminar, finaliza la conversión en el espacio de colores del dispositivo de salida. Por lo tanto, se reduce de los cálculos (número de pasos en la tabla de búsqueda) <sub>número \ de</sub> la asignación de gamas de la gama de canales al número de pasos de la tabla intermedia ₃ los cálculos de asignación de gamas. Aunque tenga que realizar el número de pasos en el número de (tabla de búsqueda) <sub>\ de</sub> los cálculos de los modelos de dispositivos y las búsquedas de tablas tridimensionales, esto es mucho más rápido que el cálculo original.

El proceso anterior funcionará bien siempre que no sea necesario pasar información entre el modelo del dispositivo de origen y cualquier otro componente de la transformación de color. Sin embargo, si el dispositivo de salida y el dispositivo de origen admiten un Colorant negro y el Colorant de origen negro se usa para determinar la salida Colorant de negro, el proceso no podrá comunicar correctamente la información de negro de origen. Un proceso alternativo consiste en construir una tabla de conversión de colores preliminar que convierta los colores en el espacio de colores independiente del dispositivo a través de los pasos de asignación de gamas únicamente. A continuación, construya la última tabla de conversión de colores de la dimensión con los pasos siguientes: a) convertir las combinaciones de colores de origen en espacio independiente del dispositivo intermedio, b) realizar los pasos de asignación de la gama mediante la interpolación en la tabla de colores preliminar en lugar de aplicar los procesos de asignación de gama real y c) usar los valores resultantes de los pasos de asignación de gamas y cualquier información de canal negro de origen para calcular el dispositivo de salida Colorants mediante el modelo Este proceso también se puede usar cuando se transfiere información entre los modelos de dispositivos de origen y salida, aunque no haya ningún canal negro. por ejemplo, si los dos módulos se implementan con una arquitectura de complemento que permite el intercambio de datos entre los módulos.

Los dos procesos anteriores se pueden usar para mejorar de forma eficaz el tiempo necesario para construir la tabla de transformación de color de cuatro dimensiones.

### <a name="checkgamut"></a>CheckGamut

El ICM llama a CreateTransform y **CreateMultiProfileTransform** toman una palabra de valores de marca, uno de los cuales es habilitar la comprobación de la \_ gama \_ . Cuando se establece esta marca, CITE debe crear la transformación de manera diferente. Los pasos iniciales son los mismos: se deben inicializar las levas de origen y de destino. a continuación, se deben inicializar los descriptores de límite de la gama de origen y de destino. Independientemente de la intención especificada, se debe usar CheckGamut GMM. CheckGamut GMM se debe inicializar con los modelos de dispositivos de origen y de destino, y los descriptores de límite de gama. Sin embargo, la transformación debe crear una transformación truncada que comprenda el modelo del dispositivo de origen, el CAM de origen, cualquier GMMs que intervenga y el GMM de CheckGamut. Esto garantiza que los valores Delta, delta C y Delta h generados por la CMM CheckGamut se convierten en los valores resultantes finales.

El significado de CheckGamut es claro cuando solo hay dos perfiles de dispositivo en la transformación. Cuando hay más de dos perfiles de dispositivo y más de dos GMMs, CheckGamut informa de si los colores que se han transformado a través del primer modelo de dispositivo y todo menos el último GMM se encuentran dentro de la gama del dispositivo de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de la administración del color](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos y esquemas del Sistema de colores de Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




