---
title: Algoritmos de creación de transformaciones de WCS
description: Algoritmos de creación de transformaciones de WCS
ms.assetid: 526bbbfc-fb60-415d-b4f0-6a44a5d11a55
keywords:
- Windows Sistema de colores (WCS), creación de transformaciones
- WCS (Windows color), creación de transformaciones
- administración del color de imagen, creación de transformaciones
- administración de colores, creación de transformaciones
- colors,transform creation
- creación de transformaciones
- Creación de transformaciones de WCS
- algorithms,transform creation
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df199f0fa649e7ce545a7b371f1caba65686746766f5572bac8e43b47413eace
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118446037"
---
# <a name="wcs-transform-creation-algorithms"></a>Algoritmos de creación de transformaciones de WCS

[Creación de transformaciones](#creation-of-transforms)

 

[Ejecución de transformación secuencial](#sequential-transform-execution)

 

[Creación de transformaciones optimizadas](#creation-of-optimized-transforms)

 

[ICCProfileFromWCSProfile](#iccprofilefromwcsprofile)

 

[Conservación de negro y generación de negro](#black-preservation-and-black-generation)

 

[Comprobación de la gama](#checkgamut)

## <a name="creation-of-transforms"></a>Creación de transformaciones

Para explicar correctamente cómo funcionan las transformaciones de color, resulta útil explicar la ruta de procesamiento completa a través de ICM 2.0 y los internos de CTE. La ICM 2.0 [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) crea una transformación de color que las aplicaciones pueden usar para realizar la administración de colores. Esta función crea un contexto de color a partir de [**las entradas LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) y intent. Las intenciones se asignan a las correlaciones del algoritmo de asignación de gama DE LÍNEA BASE DE LA FIRMA. A continuación, la función ICM función [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/) de 2.0 para un procesamiento de color coherente. Por lo general, la **función CreateColorTransform** copia los datos en la estructura de transformación optimizada interna.

La ICM 2.0 CreateMultiProfileTransform acepta una matriz de perfiles y una matriz de intenciones o un único perfil de vínculo de dispositivo y crea una transformación de color que las aplicaciones pueden usar para realizar la asignación de colores. Procesa esos perfiles de entrada e intenciones para crear modelos de dispositivo, modelos de apariencia de color, descripciones de límites de gama y modelos de asignación de gama. Este es el modo en que se hace esto:

-   Los modelos de dispositivo se inicializan directamente desde perfiles de DM. Hay un modelo de dispositivo creado para cada perfil en la llamada a [**CreateMultiProfileTransform.**](/windows/desktop/api/Wingdi/)
-   Los modelos de apariencia de color se inicializan directamente desde perfiles DE MES. Hay un perfil DEME para cada perfil en la llamada a [**CreateMultiProfileTransform.**](/windows/desktop/api/Wingdi/) Sin embargo, se puede especificar el mismo perfil DE MES para más de un perfil.
-   Las descripciones de límites de gama se inicializan a partir de un objeto de modelo de dispositivo y un objeto DEM. Hay una descripción de límite de gama para cada perfil en la llamada a [**CreateMultiProfileTransform.**](/windows/desktop/api/Wingdi/)
-   Los modelos de asignación de gama se inicializan desde dos límites de gama y una intención. Debe crear un modelo de asignación de gamas entre cada par de modelos de dispositivo creados a partir de la llamada a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/). Tenga en cuenta que esto significa que usa un modelo de mapa de gama menos que el modelo de dispositivo. Dado que el número de intenciones coincide con el número de modelos de dispositivo, también hay una intención más de la necesaria. Se omite la primera intención de la lista. Puede recorrer la lista de modelos de dispositivo e intenciones, creando modelos de asignación de gamas. Seleccione los modelos de primer y segundo dispositivo y la segunda intención y, a continuación, inicialice el primer modelo de asignación de gama. Seleccione los modelos de segundo y tercer dispositivo y la tercera intención y, a continuación, inicialice el segundo modelo de asignación de gamas. Continúe de esta manera hasta que haya creado todos los modelos de asignación de gama.

Cuando los perfiles se han procesado correctamente y se han creado e inicializado todos los objetos intermedios, puede crear la transformación cite con la siguiente llamada. *pDestCAM* y *pDestDM son* los asociados al último perfil de la llamada a [**CreateMultiProfileTransform.**](/windows/desktop/api/Wingdi/)


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

Un problema implicado en la configuración de la lista de transformaciones es validar si hay disponible un complemento necesario. El siguiente modificador de modelo proporciona esta directiva para controlar este comportamiento. La administración de esta lista de transformaciones es un método de la estructura de transformación optimizada interna, pero cada método de modelo proporciona el puntero a sí mismo y a su propio conjunto de valores de parámetro.

El modo debe ser uno de los siguientes.

-   TfmRobust: si un perfil de medida especifica un complemento preferido y el complemento no está disponible, el nuevo sistema CTE usará el complemento de línea base. Si no hay ningún complemento disponible, la transformación notificaría un error.
-   TfmStrict: si ColorContext especifica un complemento preferido, el complemento debe estar disponible. Si no se encuentra ningún complemento preferido, se usará el complemento de línea base. Si no hay ningún complemento disponible, la transformación notificaría un error.
-   TfmBaseline: solo se pueden usar complementos de línea base en AddMeasurementStep. Si ColorContext especifica un complemento preferido, se omitirá el complemento. Si el complemento de línea base no está disponible, la transformación notificaría un error.

## <a name="transform-execution"></a>Ejecución de transformación

La ICM [**translateColors**](/windows/win32/api/icm/nf-icm-translatecolors) de la API de ICM 2.0 traduce una matriz de colores del espacio [de colores](c.md) de origen al espacio de colores de destino, tal como se define mediante una transformación de color. Esta función comprueba internamente una matriz de colores almacenados en caché para habilitar la coincidencia inmediata de colores transformados habitualmente. Esta transformación admite matrices de bytes de 8 bits por canal y matrices float de 32 bits por canal. Todos los demás formatos se convertirán antes de pasar a la nueva CTE.

La ICM [**translateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) de la API de ICM 2.0 traduce los colores de un mapa de bits con un formato definido para generar otro mapa de bits en un formato solicitado. Esta función comprueba internamente una matriz de colores almacenados en caché para habilitar la coincidencia inmediata de colores transformados habitualmente. Para evitar demasiadas rutas de acceso de código, compatibilidad y complejidad de pruebas, solo se admite realmente un número limitado de formatos de mapa de bits en el motor de transformación e interpolación. Esta función debe traducir los formatos de mapa de bits entrantes y salientes no nativos en formatos admitidos de forma nativa para su procesamiento. Esta transformación solo admite mapas de bits de bytes de 8 bits por canal y mapas de bits flotantes de 32 bits por canal. Todos los demás formatos se convertirán antes de pasar a la nueva CTE.

 

### <a name="sequential-transform-execution"></a>Ejecución de transformación secuencial

Si el *parámetro dwFlags* tiene el bit DE TRANSFORMACIÓN SECUENCIAL establecido cuando se llama a las funciones de \_ ICM [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) o **CreateMultiProfileTransform,** los pasos de transformación se ejecutan secuencialmente. Esto significa que el código pasa por cada modelo de dispositivo, el modelo de apariencia de color y el modelo de asignación de gamas por separado, tal y como se especifica en la llamada **CreateColorTransform** o **CreateMultiProfileTransform.** Esto puede ser útil para depurar módulos de complemento, pero es mucho más lento que ejecutar a través de una transformación optimizada. Por lo tanto, no se recomienda ejecutar en modo secuencial para software de producción. Además, puede haber ligeras diferencias en los resultados obtenidos en modo secuencial y en modo optimizado. Esto se debe a las variaciones introducidas cuando las funciones se concatenan juntas.

### <a name="creation-of-optimized-transforms"></a>Creación de transformaciones optimizadas

Una transformación optimizada es una tabla de búsqueda multidimensional. La tabla se puede procesar mediante un motor de interpolación multidimensional, como la interpolación leal, que aplica los colores de entrada a la transformación. En la sección siguiente se describe cómo se crean las tablas de búsqueda optimizadas. En la sección siguiente se describe cómo interpolar dentro de las tablas de búsqueda optimizadas.

## <a name="sparse-lookup-tables"></a>Tablas de búsqueda dispersas

Las impresoras convencionales tienen manuscritas UV. Para ampliar la gama, un enfoque es agregar nuevas entrada de lápiz al sistema. Las entrada de lápiz que se suelen agregar son colores que las manuscritas UV tienen dificultades para reproducirse. Las opciones comunes son naranja, verde, rojo, azul, etc. Para aumentar la "resolución aparente", se pueden usar las inks con distintos tonos, por ejemplo, el cian claro, el verde verde claro, y así sucesivamente. En efecto, el dispositivo de impresora tiene más de cuatro canales.

Aunque las impresoras son dispositivos de salida, también realizan la conversión de color del espacio del dispositivo a otro espacio de color. En el caso de una impresora USB, se trataría de una transformación de XYZ a XYZ, o el "modelo hacia delante" de la impresora. Mediante la combinación del modelo hacia delante con otras transformaciones, es posible emular una impresión COMBINE en otro dispositivo. Por ejemplo, una SUPERVISE de impresora a un monitor RGB haría posible un mecanismo de prueba que emula una impresión de esa impresora SUPERVISE en un monitor. De forma similar, lo mismo se aplica a las impresoras hi-fi. Una conversión OGOG a RGB permite la prueba de la impresora OGOG en un monitor.

El enfoque convencional para implementar esta conversión de color es mediante un LUT uniforme. Por ejemplo, en un perfil DE C#para una impresora OGOG, la especificación DE ACUERDO exige una etiqueta A2B1 que almacena un LUT uniforme que representa un muestreo uniforme en el espacio del dispositivo OGOG del modelo hacia delante, que va de OGOG al espacio de conexión del perfil DE ACUERDO (ya sea CIELAB o CIEXYZ). El perfil de vínculo de dispositivo DE ACUERDO permite una transformación directa del espacio del dispositivo OGOG a cualquier espacio de color, incluido un espacio de dispositivo, también en forma de un LUT muestreado uniformemente en el espacio OGOG. El muestreo nunca se realiza con 256 niveles (profundidad de bits 8) debido al enorme LUT resultante, excepto en el caso de dispositivos monocromáticos (1 canal). En su lugar, se usa el muestreo con una profundidad de bits inferior; Algunas opciones típicas son 9 (profundidad de bits 3), 17 (profundidad de bits 4), 33 (profundidad de bits 5). Con el número de niveles inferior a 256 en cada canal, el LUT se usa junto con un algoritmo de interpolación para generar el resultado si un nivel está entre dos niveles muestreados.

Aunque un LUT uniforme es conceptualmente fácil de implementar y la interpolación en un LUT uniforme suele ser eficaz, el tamaño de LUT aumenta exponencialmente con la dimensión de entrada. De hecho, si *d* es el número de pasos usados en el LUT uniforme y *n* es el número de canales en el espacio de color de origen, el número de nodos del LUT es Muestra la variable para el número de nodos de un ![ LUT. ](images/transformcreation-image002.gif) Claramente, el número de nodos requiere rápidamente tanto almacenamiento en memoria que incluso los sistemas informáticos de primera línea tienen dificultades para controlar la demanda. En el caso de los dispositivos con seis u ocho canales, una implementación DESECHA del perfil de dispositivo requiere el uso de algunos pasos en el LUT, a veces incluso hasta cinco pasos en la tabla A2B1 para mantener el perfil en megabytes en lugar de gigabytes. Claramente, el uso de un número menor de pasos aumenta el error de interpolación, ya que ahora hay menos muestras. Dado que el LUT debe ser uniforme, la precisión de todo el espacio de color se degrada incluso en aquellas regiones del espacio donde una diferencia de color significativa puede deberse a un pequeño cambio en el valor del dispositivo.

En los dispositivos con más de cuatro colores, ciertos subespacios de todo el espacio del dispositivo son más importantes que otros. Por ejemplo, en el espacio OGOG, las manuscritas cian y verde rara vez se usan juntas porque sus matiz se superponen en gran medida entre sí. Del mismo modo, las manuscritas amarillas y naranjas se superponen en gran medida entre sí. Una reducción uniforme en el número de pasos se puede ver como una degradación general de la calidad en todo el espacio de color, que es algo que se puede permitir para las combinaciones improbables de entrada de lápiz, pero no para las combinaciones probables o importantes.

Aunque un LUT muestreado uniformemente es sencillo y eficaz para la interpolación, impone enormes requisitos de memoria a medida que aumenta la dimensión. En realidad, aunque un dispositivo puede tener seis u ocho canales, rara vez se usan simultáneamente. En la mayoría de los casos, la transformación de color a color de entrada tiene solo algunos colores "activos", por lo que reside en un espacio de colores dimensional inferior. Esto también significa que la interpolación se puede realizar de forma más eficaz en ese espacio dimensional inferior, ya que la interpolación es más rápida cuando la dimensión es inferior.

Por lo tanto, el enfoque es estratificar todo el espacio del dispositivo en subespacios de varias dimensiones. Y dado que las dimensiones inferiores (que combinan tres o cuatro colores) son más importantes, mediante la estratificación del espacio, también puede aplicar diferentes velocidades de muestreo. es decir, un número diferente de pasos, a las piezas; aumentar las tasas de muestreo para las dimensiones inferiores, lo que las reduce para dimensiones superiores.

Para corregir las notaciones, *n* es el número de canales en el espacio de color de origen de la transformación de color que desea muestrear. También puede hacer referencia a *n* como dimensión de entrada y ![ Muestra n mayor o igual que 5.](images/transformcreation-image004.gif) , a menos que se especifique lo contrario.

Los bloques de creación básicos  son LUN de varias dimensiones y tamaños de entrada, en lugar de un LUT uniforme con dimensión de *entrada n*. Para ser más precisos,*un LUT* es un entramado rectangular impuesto en un cubo de unidad; es decir, todas las coordenadas del dispositivo se normalizan en el \[ intervalo 0, 1 \] ). si es la dimensión de entrada del lut (tenga en cuenta que no tiene que ser igual a *n*, aunque Muestra V menor ![ o igual que n.](images/transformcreation-image006.gif) es necesario) y, a continuación, consta de cuadrículas de muestreo unidimensionales:

Se *muestra una* cuadrícula de muestreo ![ unidimensional.](images/transformcreation-image008.gif)

donde todas *las x <sub>j</sub>s deben* encontrarse en el intervalo \[ 0, 1 \] , muestra un ![ superíndice d(i).](images/transformcreation-image010.gif) es el número de pasos para el muestreo del canal *i,* que debe ser al menos 1, y muestra un ![ spuperscript de X (subíndice) d(i).](images/transformcreation-image012.gif) debe ser 1. Por otro lado, ![ muestra una X de superíndice (subíndice 1).](images/transformcreation-image014.gif) no es necesario que sea 0.

Solo se definirán los dos casos especiales siguientes de LUT.

*LUT cerrado:* se trata de un LUT con el requisito adicional de que para cada *<sub>Uno</sub>* de ellos, muestra un superíndice ![ X (subíndice 1) igual a 0.](images/transformcreation-image016.gif) , y ![ Muestra un superíndice d(i) mayor o igual que 2.](images/transformcreation-image018.gif) . Un LUT cerrado uniforme es un LUT cerrado que tiene el mismo que ![ muestra un superíndice d(i).](images/transformcreation-image010.gif) para cada canal, y los nodos se espaciadon uniformemente entre 0 y 1.

*OPEN LUT:* se trata de un LUT con el requisito adicional de que para cada *uno* de ellos, ![ sHows a superscript X (subíndice 1) mayor que 0.](images/transformcreation-image020.gif) . Es correcto que muestre ![ un superíndice d(i) igual a 1.](images/transformcreation-image022.gif) .

El objetivo es estratificar el cubo de unidad 0, 1 n en una colección de LUN cerrados y LUT abiertos, de modo que toda la colección cubra el cubo \[ \]  de unidades. Conceptualmente, es más sencillo organizar estos "niveles lut" por sus dimensiones, de modo que en el nivel superior:

![Muestra el nivel superior para organizar los niveles de L U T por sus dimensiones.](images/transformcreation-image024.png)

donde ![ muestra el subíndice sigma k.](images/transformcreation-image026.gif) es la *"colección k* -dimensional strata". Tenga en cuenta que la dimensión de capa empieza por 3 en lugar de 0; es decir, puntos, porque la interpolación de combinaciones de tres colores se puede controlar sin necesidad de demasiada memoria.

## <a name="description-of-the-lut-strata"></a>Descripción del nivel de LUT

En esta implementación:

1. ![Muestra el subíndice sigma 3.](images/transformcreation-image028.gif) consta de LUN cerrados con tres entradas, una de cada combinación posible de tres colorants elegidos de *los n* colorants.

2. ![Muestra el subíndice sigma 4.](images/transformcreation-image030.gif) consta de un LUT cerrado para la combinación CHAN (o los cuatro primeros colorantes), junto con ![Muestra (n sobre 4) menos 1.](images/transformcreation-image032.png) abrir LUT para todas las demás combinaciones de cuatro colores. Al interpretar la combinación de MIENTO, se reconoce que es una combinación importante.

3. Para ![ Muestra k igual a 5, ..., n.](images/transformcreation-image034.gif) , ![ muestra el subíndice sigma k.](images/transformcreation-image026.gif) consta de ![ Shows (n sobre k).](images/transformcreation-image037.gif) abrir LUT, uno para cada combinación posible de elegir *k* colorants del total *de n* colorants.

Queda para especificar los tamaños de los LUN. La diferencia clave entre los LUT abiertos y los cerrados es que los LUT abiertos no se superponen y los LUN cerrados pueden superponerse en las caras de límite. El hecho de que el muestreo unidimensional en un LUT abierto no contenga 0, significa básicamente que a un LUT abierto le falta la mitad de las caras de límite, de ahí el nombre "open". Si dos LUT no se superponen, puede usar un número diferente de pasos o ubicaciones de nodo en cada canal. No ocurre lo mismo si dos LUT se superponen. En ese caso, si el número de pasos o las ubicaciones del nodo son diferentes, un punto situado en la intersección de los dos LUN recibirá un valor de interpolación diferente en función del LUT que se utilice en la interpolación. Una solución sencilla a este problema es usar el muestreo uniforme con el mismo número de pasos cada vez que dos LUT se superponen. En otras palabras:

Todos los LUT cerrados (los LUN de tres colores y el LUT de TROP en esta implementación) deben ser uniformes y tener el mismo número de pasos, que se indican *como .*

Los dos algoritmos siguientes se pueden usar para determinar el número de pasos *d* para los LUN cerrados y el número de pasos para los LUN abiertos.

## <a name="algorithm-1"></a>Algoritmo \# 1

Este algoritmo no requiere entrada externa.

Todos los LUT cerrados serán uniformes con *d* número de pasos.

Todos los LUT abiertos de la *dimensión k* tendrán el mismo número de pasos ![ Muestra d(k).](images/transformcreation-image039.gif) en cada canal de entrada, y los nodos están igualmente espaciados; es decir, para cada ![ muestra, es igual a 1, 2, ..., k.](images/transformcreation-image041.gif) .

Noé *i:* ![ muestra el algoritmo i.](images/transformcreation-image043.png)

Por último, *especifique d* y *d* (*k* ) en la tabla 1 siguiente. Los tres modos, "proof", "normal" y "best" son los valores de calidad ICM 2.0. En esta implementación, el modo de prueba tiene la superficie de memoria más pequeña y el mejor modo tiene la superficie de memoria más grande.

Para implementar este algoritmo, debe llamar al siguiente algoritmo \# 2. Los usuarios pueden especificar sus propias ubicaciones de muestreo mediante las tablas como guía.

## <a name="algorithm-2"></a>Algoritmo \# 2

Este algoritmo requiere una entrada externa en forma de una lista de ubicaciones de muestreo "importantes", pero es más adaptable y puede ahorrar espacio en memoria potencialmente.

La entrada necesaria es una matriz de valores de dispositivo proporcionados por el usuario. Estos valores de dispositivo indican qué región del espacio de color del dispositivo es importante; es decir, qué región se debe muestrear más.

Todos los LUT cerrados serán uniformes con *d número* de pasos, como se describe en Algoritmo \# 1. Los valores *de d* se proporcionan en la tabla 1.

*(a) LUT cerrado uniforme*



|         | Modo de prueba | Modo Normal | Mejor modo |
|---------|------------|-------------|-----------|
| ***d*** | 9          | 17          | 33        |



 

*(b) Abrir LUT*



| Dimensión de entrada | Modo de prueba | Modo Normal | Mejor modo |
|-----------------|------------|-------------|-----------|
| 4               | 5          | 7           | 9         |
| 5               | 2          | 3           | 3         |
| 6               | 2          | 3           | 3         |
| 7               | 2          | 2           | 2         |
| 8 o más       | 2          | 2           | 2         |



 

**Tabla 1:** Tamaños de LUT usados en el algoritmo

Cada LUT abierto puede tener un número diferente de pasos en cada canal de entrada y las ubicaciones de muestreo no tienen que estar igualmente espaciados. Para un estratega lut abierto determinado, hay una combinación de colores asociada, por ejemplo, ![ Muestra el subíndice C 1, ..., subíndice C k.](images/transformcreation-image045.gif) , donde muestra ![ el subíndice C i.](images/transformcreation-image047.gif) s son enteros distintos entre 1 y *n*. Son los índices de canal correspondientes a los colorantes "activos" de este nivel.

PASO 1: Filtre la matriz especificada de valores de dispositivo que no están incluidos en este nivel. Un valor de ![ dispositivo Muestra X subíndice 1, X subíndice 2, ..., X subíndice n.](images/transformcreation-image049.gif) está contenido en el strata, si y solo si ![ muestra un conjunto de valores para un canal.](images/transformcreation-image051.gif) y todos los demás canales son 0. Si el conjunto filtrado tiene *N* entradas, deje

![Muestra una ecuación que se usará si el conjunto filtrado tiene N entradas.](images/transformcreation-image053.png)

Para cada uno ![Muestra i igual a 1, 2, ..., k.](images/transformcreation-image041.gif) , itera los pasos 2 a 5 siguientes:

PASO 2: Si ![ muestra d subíndice provisional (k) igual a 1.](images/transformcreation-image055.gif) , *Vai* solo tiene 1 punto, que debe ser 1,0. Pase a la siguiente *i*. De lo contrario, continúe con el PASO 3.

PASO 3: Ordenar las muestras filtradas en orden ascendente en el ![Muestra el subíndice I de C.](images/transformcreation-image047.gif) canal.

PASO 4: Definición de la cuadrícula de muestreo "provisional" mediante los nodos

![Muestra los nodos usados para definir la cuadrícula de muestreo "provisional".](images/transformcreation-image057.png)

where ![Muestra j igual a 1, 2, ..., d subíndice provisional (k).](images/transformcreation-image059.gif) .

PASO 5: Regularizar la cuadrícula provisional para asegurarse de que se ajusta a la monotonía estricta y también de que termina con 1.0. Dado que la matriz ya está ordenada, los nodos de la cuadrícula provisional ya no disminuyen de forma monotónica. Sin embargo, los nodos adyacentes pueden ser idénticos. Puede corregirlo quitando nodos idénticos, si es necesario. Por último, después de este procedimiento, si el punto final es menor que 1.0, reemplázlo por 1.0.

Tenga en cuenta que el PASO 5 es la razón por la que el nivel de LUT puede tener un número diferente de pasos en cada canal. Después de la regularización, el número de pasos de un canal puede ser menor que ![Muestra d subíndice provisional (k).](images/transformcreation-image061.gif) .

## <a name="interpolation"></a>Interpolación

Para construir la estratificación del cubo de unidades, abra los niveles lut y los niveles de LUT cerrados. Para realizar la interpolación mediante esta "estructura dispersa de LUT", siga estos pasos. Asumir un valor de dispositivo de entrada determinado ![Muestra (X subíndice 1, X subíndice 2, ..., X subíndice n).](images/transformcreation-image049.gif) .

PASO 1: Determinar el número de canales "activos". Este es el número de canales distintos de cero. Esto determina la dimensión de capa *k* para buscar el estratega que lo contiene. Más concretamente, la dimensión de capa es 3 si el número de canales activos es ![ Muestra menor o igual que 3.](images/transformcreation-image063.gif) , de lo contrario, la dimensión de capa es la misma que el número de canales activos.

PASO 2: Dentro de ![Muestra el subíndice sigma k.](images/transformcreation-image026.gif) , busque el estratega que lo contiene. Un valor de dispositivo se encuentra en un estratega abierto si todos los canales correspondientes al estratega tienen un valor distinto de cero y todos los demás canales son cero. Un valor de dispositivo se encuentra en un estratega cerrado si cada canal no representado por el estratega es cero. Si no se encuentra ningún estratega que contenga, hay una condición de error. Cancelar e informar de un error. Si se encuentra un estratega que contiene , continúe con el paso siguiente.

PASO 3: Si se cierra el estratega que lo contiene, cualquier algoritmo de interpolación conocido puede realizar la interpolación dentro del estratega. En esta implementación, la elección del algoritmo es la interpolación de paréntesis. Si el estratega que contiene está abierto y el valor del dispositivo se encuentra estrictamente dentro del estratega, es decir,

![Muestra X subíndice i mayor o igual que... ](images/transformcreation-image065.gif) primer nodo en *el canal i.*

donde *i* es un índice de canal para el estratega y, a continuación, funciona el algoritmo de interpolación estándar, como la interpolación de paréntesis.

Si muestra el subíndice X i less than... first node in i th channel for some i , el valor del dispositivo se encuentra en la "brecha" entre el estrama y los ![ ](images/transformcreation-image067.gif) subespacios dimensionales inferiores.   Este MOI no se refiere a un algoritmo de interpolación por se, por lo que se puede usar cualquier algoritmo de interpolación para interpolar dentro de esta "brecha", aunque el algoritmo preferido es la siguiente interpolación transfinite.

La arquitectura del módulo de interpolación se ilustra en las dos partes de la figura 1.

![Diagrama que muestra la primera parte de la arquitectura del módulo de interpolación.](images/transformcreation-image068.png)

![Diagrama que muestra la segunda parte de la arquitectura del módulo de interpolación.](images/transformcreation-image070.png)

**Figura 1:** Arquitectura del módulo de intepolación

Como se explicó anteriormente, este algoritmo es capaz de lograr un muestreo razonablemente denso en regiones del espacio del dispositivo que contienen una combinación importante de colorantes, a la vez que minimiza el tamaño total de los LUN necesarios. En la tabla siguiente se muestra una comparación del número de nodos necesarios para la implementación dispersa de LUT (mediante el algoritmo 1 y el modo normal) y la implementación uniforme \# de LUT correspondiente.



| **Número de canales de entrada** | **LUT disperso** | **LUT uniforme** |
|------------------------------|----------------|-----------------|
| 5                            | 142498         | 1419857         |
| 6                            | 217582         | 24137567        |
| 7                            | 347444         | 410338673       |
| 8                            | 559618         | 6975757441      |



 

## <a name="interpolation-within-a-unit-cube"></a>Interpolación dentro de un cubo de unidad

Un paso básico en el caso de la cuadrícula rectangular es la interpolación dentro de una celda que lo incluye. Para un punto de entrada, puede determinar fácilmente la celda que lo incluye. En una cuadrícula rectangular, se especifica el valor de salida en cada uno de los vértices (puntos de esquina) de la celda que lo incluye. También son las únicas condiciones de límite (BCs) que debe cumplir un interpolador: el interpolador debe pasar a través de todos estos puntos. Tenga en cuenta que estas condiciones de límite se encuentran en puntos "discretos", en este caso los puntos de esquina 2n de la celda, donde n es la dimensión del espacio de color.

Es útil formalizar el concepto de condiciones de límite antes de seguir adelante. Para cualquier subconjunto S del límite de la celda de entrada (el cubo de unidad en n dimensiones), una condición de límite en S es una especificación de una función BC: S → Rm, donde m es la dimensión de salida. En otras palabras, se requiere un interpolante, que se puede anotar como Interp: \[ 0,1 \] n→ Rm, para satisfacer: Interp(x) = BC(x) para todas las x en S.

En el escenario estándar de interpolación en el cubo de unidad, S es el conjunto de puntos discretos que son los vértices de 2n del cubo.

Ahora puede generalizar las condiciones de límite para resolver los problemas descritos anteriormente y proporcionar un nuevo algoritmo de interpolación dentro del cubo de unidad. En lugar de permitir solo puntos de límite discretos, se pueden imponer condiciones de límite en una cara de límite completa del cubo. Las suposiciones precisas son las siguientes:

(a) El punto vn =(1,1,...,1) es especial y solo se permite una condición de límite discreta. En otras palabras, no se pueden imponer condiciones de límite continuas en las caras de n límite xi=1 (i=1,...,n).

(b) Para cada una de las caras restantes de n límites xi=0 (i=1,...,n), la condición de límite se puede imponer en toda la cara, con la condición de compatibilidad de que si dos caras se cruzan, las condiciones de límite de las caras deben coincidir en la intersección.

(c) Los vértices que no contengan las caras con condición de límite tendrán una condición de límite individual (discreta).

Puede hacer referencia a una condición de límite discreta como datos finitos y a una condición de límite continua como datos transfinite para analizar la interpolación en datos finitos y transfinite.

En primer lugar, revise la interpolación estándar (por ejemplo, la que se usa en la charca de Momento), que ayuda a establecer las notaciones para esta formulación concreta del problema. Se sabe que el cubo de \[ unidad 0,1 n se puede \] subdividir en n. , parametrizado por el conjunto de permutaciones en n símbolos. Más concretamente, cada uno de estos hahedron se define mediante desigualdades.

![Muestra la fórmula para las desigualdades de los hadas.](images/transformcreation-image073.gif)

donde σ:{1,2,..,n}→{1,2,...,n} es una permutación de "símbolos" 1, 2, ..., n, es decir, es una asignación bijetiva del conjunto de n símbolos. Por ejemplo, si n = 3 y σ = (3, 2, 1), lo que significa σ(1)=3, σ(2)=2, σ(3)=1, entonces la función correspondiente se define mediante z≥y≥x, donde la notación común x, y, z se usa para x1, x2, x3. Tenga en cuenta que estos paréntesis no se unen entre sí. Para la interpolación, los puntos situados en una cara común de dos leales distintos tendrán el mismo valor de interpolación, independientemente de qué paréntesis se utilice en la interpolación. Aun así, en el escenario estándar de interpolación en puntos finitos, para un punto de entrada determinado (x1, ..., xn), primero determine en qué paréntesis se encuentra, o equivalentemente, el valor de permutación correspondiente σ; a continuación, el interpolador de hadas se define como .

![Muestra la ecuación que define el interpolador de paréntesis.](images/transformcreation-image075.png)

where ![Muestra la ecuación de los vectores de base estándar.](images/transformcreation-image077.png) para i=1, ..., n y e1, ..., en son los vectores de base estándar. Antes de pasar a la generalización, tenga en cuenta que v0, v1, ..., vn son los vértices del botón y ![Muestra las coordenadas baricéntricas.](images/transformcreation-image079.png) son las "coordenadas centradas en barras".

En el caso general de los BCs en las caras de límite, puede usar el concepto de proyección centrada en barras. Como antes, para un punto de entrada determinado (x1, ..., xn), determine primero en qué paréntesis se encuentra, o equivalentemente, la permutación correspondiente σ. A continuación, realice una serie de proyecciones centradas en barras, como se muestra a continuación. La primera proyección ![Muestra el subíndice BProj 1 (x).](images/transformcreation-image081.gif) envía el punto al plano ![Muestra X subíndice delta (1) igual a 0.](images/transformcreation-image083.gif) Salvo ![Muestra X igual a V subíndice n.](images/transformcreation-image085.gif) en cuyo caso no se cambia. La definición precisa del mapa BProj se define de la siguiente manera:

![Muestra la ecuación para la definición precisa del mapa BProj.](images/transformcreation-image087.png)

con ![Muestra la ecuación de P subíndice k.](images/transformcreation-image089.png) y k = 1, 2, ..., n.

En el caso ![Muestra que X es igual a V subíndice n.](images/transformcreation-image085.gif) , puede detenerse, porque BC se define en vn por Assumption (a). En el caso ![Muestra que X no es igual a V subíndice n.](images/transformcreation-image091.gif) , está claro que ![Muestra el subíndice BProj 1 (X).](images/transformcreation-image081.gif) tiene el σ(1)th componente anniated. En otras palabras, se encuentra en una de las caras de límite. O bien se encuentra en una cara en la que se define BC, en cuyo caso puede detenerse, o bien realizar otra proyección centrada en la barra ![Muestra el subíndice BProj 2 (X').](images/transformcreation-image093.gif) where ![Muestra X' igual al subíndice BProj 1 (X).](images/transformcreation-image095.gif) . Y si ![Muestra el subíndice X''= Bproj 1 (X').](images/transformcreation-image097.gif) está en una cara en la que se define BC, puede detenerse. de lo contrario, realice otra proyección. ![Muestra el subíndice BProj 3 (X'').](images/transformcreation-image099.gif) . Dado que cada proyección anímica un componente, la dimensión efectiva disminuye, por lo que sabe que el proceso debe detenerse finalmente. En el peor de los casos, se realizan n proyecciones hasta la dimensión 0, es decir, los vértices del cubo, que según Suposición (c), sabe que BC se definirá.

Suponiendo que se han realizado proyecciones K, con

![Muestra una ecuación que se usará suponiendo que se haya realizado la proyección K.](images/transformcreation-image101.png)

x(0)= x, el punto de entrada y BC se definen en x(k). A continuación, desenreda las proyecciones mediante la definición de una serie de vectores de salida:

![Muestra ecuaciones para una serie de vectores de salida.](images/transformcreation-image103.png)

where ![Muestra la ecuación para el superíndice Y (K).](images/transformcreation-image105.gif) y, por último, obtiene la respuesta.

![Muestra Interp(x) igual a y superíndice (0).](images/transformcreation-image107.gif)

## <a name="worked-example"></a>Ejemplo práctico

![Diagrama que muestra un ejemplo trabajado de interpolación con un cubo de unidad.](images/transformcreation-image108.png)

**Figura 2:** Ejemplo de trabajo

Tenga en cuenta la situación que se muestra en la figura 2, donde n = 3, m = 1, y tiene los siguientes BCs:

(a) Cuatro BCs discretos en los vértices

(0, 0, 1): β001

(0, 1, 1): β011

(1, 0, 1): β101

(1, 1, 1): β111

(b) Un BC continuo en la cara x3=0: F(x1, x2)

Cálculo \# 1: punto de entrada x = (0,8, 0,5, 0,2). El entrelazamiento está asociado a la permutación &lt; 1, 2, 3 &gt; .

Primera proyección: ![Muestra la ecuación de la primera proyección.](images/transformcreation-image110.png)

Ya está en la cara x3=0, por lo que puede detenerse. A continuación, la sustitución con versiones anteriores proporciona

![Muestra la respuesta de la primera proyección.](images/transformcreation-image112.png) que es la respuesta.

Cálculo \# 2: punto de entrada x = (0,2, 0,5, 0,8). El entrelazamiento está asociado a la permutación &lt; 3, 2, &gt; 1.

Primera proyección: ![Muestra la ecuación de la primera proyección del cálculo 2.](images/transformcreation-image113.png)

Segunda proyección: ![Muestra la ecuación de la segunda proyección del cálculo 2.](images/transformcreation-image115.png)

Tercera proyección: ![Muestra la ecuación de la tercera proyección del cálculo 2.](images/transformcreation-image117.png) , que está en la cara x3=0. A continuación, la sustitución con versiones anteriores proporciona

![Muestra las dos primeras ecuaciones para la sustitución hacia atrás.](images/transformcreation-image119.png)

![Muestra la tercera ecuación para la sustitución hacia atrás.](images/transformcreation-image123.png), que es la respuesta final.

## <a name="applications"></a>Aplicaciones

*(a) Interpolación secuencial de paréntesis*

![Diagrama que muestra la interpolación secuencial.](images/transformcreation-image124.png)

**Figura 3:** Interpolación secuencial

Consulte la figura 3. Para interpolar entre dos planos en los que se han impuesto cuadrículas incompatibles, considere una celda que incluye un punto determinado P que se muestra en la ilustración. Los vértices "superiores" de la celda proceden directamente de la cuadrícula del plano superior. Los vértices de la cara inferior no son compatibles con la cuadrícula del plano inferior, por lo que toda la cara se trata como si fuera un BC con valores obtenidos por la interpolación en la cuadrícula del plano inferior. A continuación, queda claro que esta configuración satisface las suposiciones (a), (b) y (c) anteriores, y puede aplicar el algoritmo de interpolación.

También está claro que el algoritmo ha reducido la dimensión del problema de interpolación en 1, porque el resultado es una combinación lineal de valores en los vértices de la cuadrícula superior y la interpolación en el plano inferior, que tiene una dimensión menor que 1. Si existe una configuración de plano de sándwich similar en el plano inferior, puede aplicar el procedimiento en ese plano, lo que reduce aún más la dimensión en 1. Este procedimiento puede continuar hasta llegar a la dimensión 0. Esta cascada de proyecciones e interpolaciones se puede denominar "Interpolación secuencial de paréntesis".

*(b) Interpolación de intervalos*

![Diagrama que muestra la interpolación de brechas.](images/transformcreation-image126.jpg)

**Figura 4:** Interpolación de brechas

Se trata de una cuadrícula impuesta en un cubo que se encuentra estrictamente dentro del cuadrante positivo. El cubo en sí tiene una cuadrícula y cada plano de coordenadas tiene cuadrículas que no son necesariamente compatibles. La "brecha" entre el cubo y los planos de coordenadas tiene una sección cruzada que tiene "forma de L" y no es aceptable para las técnicas estándar. Sin embargo, con la técnica introducida aquí, puede introducir fácilmente celdas que cubren esta brecha. En la figura 4 se muestra uno de estos. Las cuadrículas de los planos de coordenadas admiten la interpolación que proporciona los BCs necesarios para todas las caras inferiores de la celda, con un vértice restante cuyo BC se proporciona mediante la esquina inferior del cubo.

## <a name="final-note-on-implementation"></a>Nota final sobre la implementación

En la aplicación real, el "cubo de unidad" que es la configuración básica del algoritmo se extrae de las ropas más grandes y los valores de los vértices pueden requerir un cálculo costoso. Por otro lado, también está claro que la interpolación de paréntesis solo requiere los valores en los vértices del cúverhedr, que es un subconjunto de todos los vértices del cubo de unidad. Por lo tanto, es más eficaz implementar lo que se puede denominar "evaluación aplazada". En una implementación de software del algoritmo anterior, es habitual tener una subrutina que toma el cubo de unidad y los valores en sus vértices como entrada. La evaluación diferida significa que, en lugar de pasar los valores en los vértices, se pasa la información necesaria para evaluar los valores de los vértices, sin llevar a cabo realmente la evaluación. Dentro de la subrutina, la evaluación real de estos valores solo se llevará a cabo para los vértices que pertenecen a la cadena de entrada, una vez que se determina el hahedron de encierre.

## <a name="lookup-table-for-use-with-high-dynamic-range-virtual-rgb-source-devices"></a>Tabla de búsqueda para su uso con dispositivos de origen RGB virtuales de alto rango dinámico

En el caso de que una transformación se construya con un dispositivo de origen modelado como un dispositivo RGB virtual, es posible que los valores coloreantes de origen puedan ser negativos o mayores que unity (1.0). Cuando esto sucede, se hace referencia al dispositivo de origen como que tiene un rango dinámico alto (HDR). En este caso, se debe tener en cuenta de forma especial.

En el caso de las transformaciones HDR, los valores mínimo y máximo de cada canal coloreante se pueden determinar a partir del límite de gama del dispositivo. Con estos valores, se aplica un escalado simple para cada canal coloreante para que los valores coloreantes iguales al colorante mínimo se conviertan en 0,0 y los valores coloreantes iguales al colorante máximo se conviertan en 1,0, con un escalado lineal de valores entre para asignar linealmente entre 0,0 y 1,0.

### <a name="iccprofilefromwcsprofile"></a>CCIProfileFromWCSProfile

Dado que el propósito principal de esta característica es admitir las versiones anteriores a Vista de Windows, debe generar perfiles DE LA VERSIÓN 2.2 DE LA SERIE DE CLAVES tal y como se define en especificación DE LA ORDEN DE PROPIEDAD.1:1998-09. En determinados casos (consulte la tabla siguiente "Asignación de clases de perfil de dispositivo de línea base a WC"), puede crear una matriz o un perfil DE MATRIX basado en TRC a partir de un perfil WCS. En otros casos, el perfil DEER consta de LUT. En el siguiente proceso se describe cómo crear los LUN de AToB y BToA. Por supuesto, los perfiles DE LAN también tienen otros campos. Algunos de los datos se pueden derivar del perfil de WCS. Para otros datos, tendrá que desarrollar valores predeterminados inteligentes. El copyright se asignará a Microsoft; puesto que es la tecnología de Microsoft la que se usa para crear los LUN.

Este diseño debe funcionar para todos los tipos de modelos de dispositivo, incluidos los complementos. Siempre que el complemento tenga un modelo de dispositivo de línea base asociado, se puede determinar el tipo de dispositivo subyacente.

La parte fundamental de la creación de un perfil DEER ES la creación de las tablas de búsqueda AToB y BToA. Estas tablas se asignan entre el espacio del dispositivo, por ejemplo, RGB o SPACE, y el espacio de conexión de perfil (PCS), que es una variante de CIELAB. Esto es fundamentalmente lo mismo que el proceso de administración de colores que se usa en la transformación cite para asignar el espacio del dispositivo al espacio del dispositivo. Sin embargo, debe tener la siguiente información para realizar la transformación.

1) Condiciones de visualización de referencia para pcs.

2) Gama de PCS de referencia.

3) Modelo de dispositivo que convierte entre los valores de PCS y la colorimetría.

El perfil wcs y su CÁMARA asociada se proporcionan como parámetros. Hay dos modelos de dispositivo de línea base que convierten entre la colorimetría y la codificación PCS. La razón por la que necesita dos se explica a continuación.

1) Puede obtener las condiciones de visualización de referencia para el PCS a partir de la especificación de formato de perfil DEIA. La información proporcionada en la especificación de formato de perfil DEER es suficiente para calcular todos los datos necesarios para inicializar la CÁMARA usada por CMS. Por coherencia y flexibilidad, esta información se almacena en un perfil de color WCS.

2) También puede usar un perfil de WCS para almacenar ejemplos que definen la gama de referencia del PCS. El sistema de administración de colores (CMS) de CITE tiene dos maneras de crear límites de gama. Una es muestrear el espacio completo del dispositivo y usar el modelo de dispositivo para crear valores de medida. El segundo método consiste en usar muestras medidas del perfil para crear un límite de gama de referencia. Dado que la gama de PCS DE LA CORTE es demasiado grande para crear una gama de referencia útil, el primer método no es adecuado. Pero el segundo método es un enfoque flexible y basado en perfiles. Para volver a definir la gama de PCS de referencia, puede cambiar los datos de medida en el perfil de dispositivo PCS.

3) EL PCS DE CORTE es un modelado de un dispositivo ideal. Al crear un modelo de PCS como un dispositivo real, puede aprovechar el proceso de administración de colores que se usa en Smart CMM. Crear un modelo de dispositivo desde la colorimetría a la codificación PCS es sencillo. Basta con asignar entre los valores colorimétricos verdaderos y los valores codificados por PCS. Puesto que la interfaz cms para los modelos de dispositivo solo admite valores XYZ, es posible que también tenga que asignar entre XYZ y LAB. Se trata de una transformación conocida. Este modelo se describe en el documento 2.2.02 "Modelos de dispositivo de línea base" en las secciones 7.9 y 7.10.

Es posible que tenga que realizar alguna asignación de gama si la gama del dispositivo es mayor que la gama del PCS. Los MMG de línea de base se pueden usar para este propósito. Tenga en cuenta que un perfil DEER creado correctamente tiene tablas de búsqueda para las intenciones Colorimétrica relativa, Perceptual y Saturación, aunque todas pueden apuntar internamente al mismo LUT.

![Diagrama que muestra la creación de un A T o B L U T.](images/transformcreation-image128.png)

**Figura 5:** Creación de un LUT de AToB

Este proceso se ilustra en la figura 5. En primer lugar, el modelo de dispositivo se inicializa a partir de los datos del perfil dm. A continuación, construya un límite de gama de dispositivos como se muestra a continuación. Se ejecuta un muestreo de datos del modelo de dispositivo a través del modelo de dispositivo para obtener datos colorimétricos. Los datos colorimétricos se ejecutan a través de LA CÁMARA para crear datos de apariencia. Los datos de apariencia se usan para crear el límite de gama del dispositivo.

A continuación, use los datos del perfil de medida de PCS de referencia para crear un límite de gama para el PCS.

Use los dos límites de gama que acaba de crear para inicializar un GMM. A continuación, use el modelo de dispositivo, el GMM y el modelo de dispositivo PCS para crear una transformación. Ejecute un muestreo del espacio del dispositivo a través de la transformación para crear un LUT de AToB.

![Diagrama que muestra la creación de un A T o B L U T mediante un muestreo de espacio P C S.](images/transformcreation-image130.png)

**Figura 6:** Creación de un LUT de BToA

En la figura 6 se muestra la creación del LUT de BToA. Esto es casi idéntico a la creación de un LUT de AToB, con los roles de origen y destino intercambiados. Además, debe muestrear la gama completa de PCS para crear el LUT.

Tenga en cuenta que, dado que la CÁMARA (CIECAM02 en WCS) está implicada en el proceso, la adaptación tóctica entre el punto blanco del medio y el punto blanco pcs (que exige QUE SEA el de D50) se hace de forma transparente mediante la CÁMARA.

## <a name="hdr-virtual-rgb-devices"></a>Dispositivos RGB virtuales HDR

Debe tenerse en cuenta especial al generar perfiles para dispositivos RGB virtuales HDR; es decir, los dispositivos para los que los valores coloreantes pueden ser menores que 0,0 o mayores que 1,0. En la generación del LUT ATOB, se genera un conjunto mayor de LUN de entrada 1D. Los valores coloreantes se escalan y se desplazan hasta el intervalo 0 . 1 usando los valores de coloración mínimo y máximo en el perfil de WCS.

Dado que no es probable que el espacio coloreante de los dispositivos HDR se rellene por completo, también se proporciona compatibilidad especial en el LUT 3D para la etiqueta. Para controlar los colores de la región con poco relleno, los colorantes se codifican de forma que se pueda lograr la extrapolación más allá de 0,0 y 1,0. El intervalo utilizado es -1 . +4.

Debido al escalado aplicado para el LUT 3D, se ha creado un conjunto de LUN de salida 1D para asignar el resultado de vuelta al intervalo 0 . 1.

## <a name="more-than-one-pcs"></a>Más de un PCS

El CENTRO de control de datos encontró que un PCS no era lo suficientemente flexible para satisfacer todos los usos previstos de un CMS. En la versión 4 de la especificación de perfil, la HERRAMIENTA de cifrado de perfiles aclaró que realmente hay dos codificaciones PCS. Uno se usa para las intenciones colorimétricas; otro se usa para la intención perceptual. (No se especifica NINGÚN PCS para la intención Saturación. EL ELEMENTO DE LA COLA ha dejado esta parte ambigua). El PCS colorimétrico tiene una lumez mínima y máxima especificada, pero los valores de color y tonalidad oscilan aproximadamente ± 127. Este PCS parece un prisma rectangular. Como se mencionó anteriormente, el volumen de PCS perceptual se parece a la gama de una impresora inkjet.

Los dos PCS DE LA MONEDA también tienen dos codificaciones digitales diferentes. En el PCS perceptual, un valor de cero representa una lumez de cero. En el PCS colorimétrico, un valor de cero representa la lumíz mínima del PCS, que es mayor que cero. Puede resolver este problema si tiene un modelo de dispositivo diferente para cada una de las codificaciones PCS.

## <a name="gamut-mapping"></a>Asignación de gama

Para crear los LUT de AToB en un perfil DEIA, asigne desde la gama de dispositivos al espacio PCS adecuado. Para crear los LUN de BToA, debe asignar desde el espacio PCS a la gama de dispositivos. La asignación de los LUN de AToB es bastante similar a la que se usa en un CMS basado en medidas. Para el PCS perceptual, asigne la gama plausible del dispositivo al límite perceptual de la gama de PCS, mediante recorte o compresión para cualquier color fuera de gama. Para las intenciones colorimétricas, es posible que tenga que recortar la lumez, pero los valores de color y matiz se ajustarán a la gama colorimétrica de PCS.

La asignación de los LUN de BToA es un poco diferente. Las intenciones colorimétricas siguen siendo fáciles; simplemente recorta los valores de PCS en la gama de dispositivos. Sin embargo, LAT requiere que todos los valores de PCS posibles se asignen a algún valor de dispositivo, no solo a los que se encuentran dentro de la gama de referencia del PCS perceptual. Por lo tanto, debe asegurarse de que los GMG pueden controlar los colores de origen que están fuera de la gama de referencia. Esto se puede controlar recortando esos colores al límite de la gama del dispositivo.

## <a name="baseline-device-to-icc-profile-class-mapping"></a>Asignación de clases de perfil de dispositivo de línea de base a CLASS



| Tipo de dispositivo de línea de base              | CLASE DE PERFIL DE LA CLASE DE PERFIL DE LA CLASE       | Comentario                                                                      |
|-----------------------------------|-------------------------|-----------------------------------------------------------------------------|
| Dispositivo de captura RGB                | Dispositivo de entrada ("scnr")   | PCS es CIELAB. AToB0Tag es Device to PCS con intención colorimétrica relativa. |
| MONITOR CRT, MONITOR DE CRT                  | Mostrar dispositivo ("mntr") | PCS es CIEXYZ. Consulte lo siguiente para la conversión de modelos.                      |
| Proyector RGB                     | Espacio de color ("spac")    | PCS es CIELAB.                                                              |
| Impresora RGB y PRINTER              | Dispositivo de salida ("prtr")  | PCS es CIELAB.                                                              |
| Dispositivo virtual RGB (caso distinto de HDR) | Mostrar dispositivo ("mntr") | PCS es CIEXYZ.                                                              |
| Dispositivo virtual RGB (caso HDR)     | Espacio de color ("spac")    | PCS es CIELAB.                                                              |



 

La conversión de perfiles de monitor no implica la creación de LUN, sino que consiste en crear una matriz o un modelo TRC. El modelo que se usa en CRT es ligeramente diferente del que se usa en el modelado DE CRT o DE CRT de WCS en el que falta el término "corrección negra". Concretamente, puede:

Modelo de WCS: ![Muestra un modelo de W C S.](images/transformcreation-image132.png)

Modelo DE CSIC: ![Muestra un modelo de I C C.](images/transformcreation-image134.png)

La conversión del modelo WCS al modelo DE LA MONEDA se realiza de la manera siguiente.

Definir nuevas curvas:

![Muestra una matriz para definir nuevas curvas.](images/transformcreation-image136.png)

No se trata de curvas de reproducción de tono porque no asignan de 1 a 1. Una normalización lo logrará. Las definiciones finales del modelo DEA SON:

![Muestra las definiciones finales del modelo de C de I.](images/transformcreation-image138.png)

![Muestra la matriz final para el modelo de C de I.](images/transformcreation-image140.png)

En el caso de los dispositivos virtuales RGB que no son RGB, también está generando un perfil de DISPLAY DE LA MONEDA para mejorar la eficacia del espacio. En ese caso, la matriz Tmulmulus *M MATRIX* se puede obtener directamente de las primarias del perfil WCS sin la conversión del modelo anterior. Una última, pero importante, es que esta matriz tmulus debe adaptarse a D50 para ajustarse a la especificación DEER del PCS. En otras palabras, las entradas de cada fila de la matriz que se va a codificar en el perfil DECEI deben sumar respectivamente a 96,42, 100 y 82,49. En la implementación actual, la adaptación tóctica la realiza CAT02, que también es la transformación de adaptación tóctica que se usa en CAM02.

## <a name="black-preservation-and-black-generation"></a>Conservación de negro y generación de negro

La implementación de la conservación del negro se vincula con la generación del canal negro en dispositivos que admiten un canal negro. Para ello, se recopila información sobre cada color de origen para permitir que los modelos de dispositivo que admiten un canal negro determinen la mejor manera de establecer el canal negro en la salida. Aunque la conservación del negro es pertinente para las transformaciones de color que se convierten entre un dispositivo de canal negro en otro, la generación de negro se implementa para todas las transformaciones que implican un dispositivo de destino de canal negro.

La información del canal negro se registra en una estructura de datos denominada [**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation). La **estructura BlackInformation** contiene un valor booleano que indica si el color contiene solo un colorante negro y un valor numérico que indica el grado de "blackness" denominado peso negro. En el caso de los dispositivos de origen que admiten un canal negro, el peso negro es el porcentaje de colorante negro en el color de origen. En el caso de los dispositivos de origen que no contienen un canal negro, el peso negro se calcula con los demás colorantes y el valor de apariencia. Un valor denominado "color purity" se calcula tomando la diferencia entre el valor de colorante máximo y el valor de colorante mínimo dividido por el valor de colorante máximo. Un valor denominado " lightness relativa" se calcula tomando la diferencia entre la lumíz del color y la lumíz mínima para el dispositivo de destino dividida por la diferencia entre la lumíz mínima y máxima del dispositivo de destino. Si el dispositivo de origen es un dispositivo aditivo (monitor o proyector), se determina que el peso negro es 1,0 menos la purga de color multiplicada por la lumíz relativa. Por ejemplo, si el dispositivo de origen es un monitor RGB, el valor máximo y el valor mínimo de R, G y B para cada color se calculan y el peso negro viene determinado por la fórmula:

BW = (1.0 – (max(R,G,B) – min(R,G,B)) / max(R, G, B)) \* lumíz relativa

Si el dispositivo de origen admite la coloración resta, por ejemplo, una impresora CMY, los colores individuales deben ser "complementarios" (restados de 1,0) antes de usarlos en la fórmula anterior. Por lo tanto, para una impresora CMY, R = 1,0 – C, G = 1,0 – M y B = 1,0 – Y.

La información de color negro para cada color procesado por la transformación de color se determina durante el proceso de traducción de colores. La información de solo negro solo se determina si se especifica la conservación del negro. El peso negro siempre se determina si el modelo de dispositivo de destino admite un colorete negro. La información negra se pasa al modelo de dispositivo de destino mediante el método [**ColorimetricToDeviceColorsWithBlack,**](/previous-versions/windows/desktop/api/WcsPlugIn/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack) que usa el LUT resultante.

Tenga en cuenta que, debido a la optimización de la transformación de color, el proceso anterior solo se produce durante la creación del LUT de transformación optimizada, no durante la ejecución del método TranslateColors.

## <a name="optimization-for-transforms-with-more-than-three-source-channels"></a>Optimización de transformaciones con más de tres canales de origen

El tamaño de la transformación optimizada viene determinado por varios factores: el número de canales de color en el dispositivo de origen, el número de pasos de la tabla para cada canal de color de origen y el número de canales de color en el dispositivo de salida. La fórmula para determinar el tamaño de la tabla de transformación es:

Size = Number of steps per channel <sub>source\ device(Number\ of\ channels\ in\ source\ device)</sub> x number of channels in output device

Como puede ver, el tamaño de la tabla crece exponencialmente en función del número de canales del dispositivo de origen. Muchos dispositivos de origen admiten tres canales de color, por ejemplo, Rojo, Verde y Azul. Sin embargo, si un dispositivo de origen admite cuatro canales, como FACTOR, el tamaño de la tabla y el tiempo necesario para construir la tabla aumentan en un factor del número de pasos. En un CMS basado en medida en el que las transformaciones se construyen "sobre la marcha", esta vez puede ser inaceptable.

Para reducir el tiempo necesario para construir la tabla de conversión de colores, es posible aprovechar dos hechos. En primer lugar, aunque el dispositivo de origen puede admitir más de tres canales de color, el espacio de color independiente del dispositivo intermedio (CIECAM02 Ja <sub>C</sub> b <sub>C)</sub> solo tiene tres canales de color. En segundo lugar, la parte más lenta del procesamiento no es el modelado de dispositivos (conversión de coordenadas de color del dispositivo a valores tmulmulus), sino la asignación de gama. Con estos hechos, puede construir una tabla de conversión de colores preliminar que convierta los colores en el espacio de colores independiente del dispositivo a través de los pasos de asignación de gama y, por último, a través del modelo de color del dispositivo de salida. La construcción de esta tabla es de la dimensión tres. A continuación, creamos la tabla de conversión de colores final de dimensión cuatro mediante la conversión de las combinaciones de colores de origen en un espacio intermedio independiente del dispositivo y, a continuación, con la tabla de conversión de colores preliminar, finalizamos la conversión al espacio de color del dispositivo de salida. Por lo tanto, puede reducir de la computación (número de pasos en la tabla de búsqueda) <sub>número\ de\</sub> cálculos de asignación de gamas de canales al número de pasos de la tabla intermedia ₃ cálculos de asignación de gamas. Aunque tenga que realizar un número de pasos en los cálculos de los canales (tabla de búsqueda) <sub>de\</sub> de modelado de dispositivos y búsquedas de tablas tridimensionales, esto sigue siendo mucho más rápido que el cálculo original.

El proceso anterior funcionará bien siempre que no sea necesario pasar información entre el modelo de dispositivo de origen y cualquier otro componente de la transformación de color. Sin embargo, si el dispositivo de salida y el dispositivo de origen admiten un colorante negro y el colorante negro de origen se usa para determinar el colorante negro de salida, el proceso no podrá comunicar correctamente la información de color negro de origen. Un proceso alternativo es construir una tabla de conversión de colores preliminar que convierta los colores en el espacio de colores independiente del dispositivo solo mediante los pasos de asignación de gama. A continuación, construya la tabla de conversión de colores final de dimensión cuatro mediante los pasos siguientes: a) convierta las combinaciones de colores de origen en un espacio intermedio independiente del dispositivo, b) realice los pasos de asignación de gamas mediante la interpolación en la tabla de colores preliminar en lugar de aplicar los procesos de asignación de gama reales, y c) use los valores resultantes de los pasos de asignación de gama y cualquier información del canal negro de origen para calcular los colores del dispositivo de salida mediante el modelo de dispositivo de salida. Este proceso también se puede usar cuando hay información transferida entre los modelos de dispositivo de origen y salida, incluso si no hay ningún canal negro; por ejemplo, si los dos módulos se implementan con una arquitectura de complemento que permite el intercambio de datos entre módulos.

Los dos procesos anteriores se pueden usar para mejorar eficazmente el tiempo necesario para construir la tabla de transformación de color tridimensional.

### <a name="checkgamut"></a>CheckGamut

Las ICM a CreateTransform y **CreateMultiProfileTransform** toman una palabra de valores de marca, uno de los cuales es ENABLE \_ GAMUT \_ CHECKING. Cuando se establece esta marca, CITE debe crear la transformación de forma diferente. Los pasos iniciales son los mismos: se deben inicializar las CAM de origen y destino y, a continuación, se deben inicializar los descriptores de límite de la gama de origen y destino. Independientemente de la intención especificada, se debe usar el GMM CheckGamut. El GMM CheckGamut debe inicializarse con los modelos de dispositivo de origen y destino y los descriptores de límite de gama. Sin embargo, la transformación debe crear una transformación truncada que incluya el modelo de dispositivo de origen, la CÁMARA de origen, cualquier GMM que intervenga y el GMM CheckGamut. Esto garantiza que los valores delta J, delta C y delta h que genera la CMM CheckGamut se convierten en los valores resultantes finales.

El significado de CheckGamut es claro cuando solo hay dos perfiles de dispositivo en la transformación. Cuando hay más de dos perfiles de dispositivo y más de dos GMA, CheckGamut informa de si los colores que se han transformado a través del primer modelo de dispositivo y todos menos el último GMM se encuentran dentro de la gama del dispositivo de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de administración de colores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos y esquemas del Sistema de colores de Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




