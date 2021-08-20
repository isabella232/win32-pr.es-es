---
title: Reglas de rasterización
description: Las reglas de rasterización definen cómo se asignan los datos vectoriales a los datos de trama.
ms.assetid: 2b3894eb-dff3-401f-8b14-4af98db86e39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e8a0193efb0811fd0bc0826fc9eb4949060ecf9f5db573b0d23f7c69c4919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913996"
---
# <a name="rasterization-rules"></a>Reglas de rasterización

Las reglas de rasterización definen cómo se asignan los datos vectoriales a los datos de trama. Los datos de trama se alinean en ubicaciones enteras que luego se trazan y recortan (para dibujar el número mínimo de píxeles) y los atributos por píxel se interpolan (a partir de atributos por vértice) antes de pasarse a un sombreador de píxeles.

Hay varios tipos de reglas, que dependen del tipo de primitivo que se está asignando, así como de si los datos usan multimuestreo para reducir el alias. En las ilustraciones siguientes se muestra cómo se controlan los casos de esquina.

-   [Reglas de rasterización de triángulos (sin multimuestreo)](#triangle-rasterization-rules-without-multisampling)
-   [Reglas de rasterización de línea (con alias, sin multimuestreo)](#line-rasterization-rules-aliased-without-multisampling)
-   [Reglas de rasterización de línea (suavizadas, sin multimuestreo)](#line-rasterization-rules-antialiased-without-multisampling)
-   [Reglas de rasterización de punto (sin multimuestreo)](#point-rasterization-rules-without-multisampling)
-   [Reglas de rasterización de suavizado de alias multimuestreo](#multisample-anti-aliasing-rasterization-rules)
    -   [Compatibilidad con hardware](#hardware-support)
    -   [Muestreo centroide de atributos al suavizado de contorno de múltiples muestras](#centroid-sampling-of-attributes-when-multisample-antialiasing)
    -   [Cálculos derivados cuando se realiza una multimuestreo](#derivative-calculations-when-multisampling)
-   [Temas relacionados](#related-topics)

## <a name="triangle-rasterization-rules-without-multisampling"></a>Reglas de rasterización de triángulos (sin multimuestreo)

Se dibuja cualquier centro de píxeles que se encuentra dentro de un triángulo; Se supone que un píxel está dentro si pasa la regla de la parte superior izquierda. La regla de la parte superior izquierda es que se define un centro de píxeles para que se encuentra dentro de un triángulo si se encuentra en el borde superior o en el borde izquierdo de un triángulo.

Donde:

-   Un borde superior es un borde que es exactamente horizontal y está por encima de los demás bordes.
-   Un borde izquierdo es un borde que no es exactamente horizontal y está en el lado izquierdo del triángulo. Un triángulo puede tener uno o dos bordes izquierdos.

La regla de la parte superior izquierda garantiza que los triángulos adyacentes se dibujan una vez.

En esta ilustración se muestran ejemplos de píxeles que se dibujan porque se encuentran dentro de un triángulo o siguen la regla de la parte superior izquierda.

![ilustración de ejemplos de rasterización de triángulos de la parte superior izquierda](images/d3d10-rasterrulestriangle.png)

La cobertura de gris claro y oscuro de los píxeles los muestra como grupos de píxeles para indicar qué triángulo están dentro.

## <a name="line-rasterization-rules-aliased-without-multisampling"></a>Reglas de rasterización de línea (con alias, sin multimuestreo)

Las reglas de rasterización de línea usan un área de prueba de rombo para determinar si una línea cubre un píxel. Para las líneas x principales (líneas con -1 <= pendiente <= +1), el área de prueba de rombo incluye (se muestra sólido) el borde inferior izquierdo, el borde inferior derecho y la esquina inferior inferior; el rombo excluye (se muestra con puntos) el borde superior izquierdo, el borde superior derecho, el cable superior, la esquina izquierda y la esquina derecha. Una línea y principal es cualquier línea que no sea una línea x principal; el área de rombo de prueba es la misma que se describe para la línea x principal, salvo que también se incluye la esquina derecha.

Dado el área de rombo, una línea cubre un píxel si la línea sale del área de prueba de rombo del píxel al recorrer la línea desde el principio hacia el final. Una franja de líneas se comporta igual, ya que se dibuja como una secuencia de líneas.

En la ilustración siguiente se muestran algunos ejemplos.

![ilustración de ejemplos de rasterización de línea con alias](images/d3d10-rasterrulesline.png)

## <a name="line-rasterization-rules-antialiased-without-multisampling"></a>Reglas de rasterización de línea (suavizadas, sin multimuestreo)

Una línea suavizada se rasteriza como si fuera un rectángulo (con ancho = 1). El rectángulo forma una intersección con un destino de representación que genera valores de cobertura por píxel, que se multiplican en componentes alfa de salida del sombreador de píxeles. No hay ningún suavizado de contorno preformado al dibujar líneas en un destino de representación multimuestreo.

Se considera que no hay una única manera "mejor" de realizar la representación de línea suavizada. Direct3D 10 adopta como guía el método que se muestra en la ilustración siguiente. Este método se deriva empíricamente y muestra una serie de propiedades visuales que se consideran deseables. El hardware no tiene que coincidir exactamente con este algoritmo; Las pruebas con esta referencia deben tener tolerancias "razonables", guiados por algunos de los principios que se enumeran a continuación, lo que permite varias implementaciones de hardware y tamaños de kernel de filtro. Sin embargo, ninguna de esta flexibilidad permitida en la implementación de hardware se puede comunicar a través de Direct3D 10 a las aplicaciones, más allá de simplemente dibujar líneas y observar o medir su aspecto.

![ilustración de ejemplos de rasterización de línea suavizada](images/d3d10-rasterruleslineaa.png)

Este algoritmo genera líneas relativamente fluidas, con una intensidad uniforme, con bordes irregulares mínimos o acotado. Se minimiza el patrón moire para las líneas de cierre. Hay una buena cobertura para las uniones entre segmentos de línea colocados de un extremo a otro. El kernel de filtro es un equilibrio razonable entre la cantidad de desenfoque del borde y los cambios de intensidad causados por correcciones gamma. El valor de cobertura se multiplica en sombreador de píxeles o0.a (srcAlpha) por la siguiente fórmula por la fase de fusión de salida: srcColor \* srcAlpha + destColor \* (1-srcAlpha).

## <a name="point-rasterization-rules-without-multisampling"></a>Reglas de rasterización de punto (sin multimuestreo)

Un punto se interpreta como si se componese de dos triángulos en un patrón Z, que usan reglas de rasterización de triángulos. La coordenada identifica el centro de un cuadrado ancho de un píxel. No hay ninguna selección de puntos.

En la ilustración siguiente se muestran algunos ejemplos.

![ilustración de ejemplos de rasterización de punto](images/d3d10-rasterrulespoint.png)

## <a name="multisample-anti-aliasing-rasterization-rules"></a>Reglas de rasterización de suavizado de alias multimuestreo

El suavizado de contorno multimuestreo (MSAA) reduce el alias de geometría mediante la cobertura de píxeles y las pruebas de galería de símbolos de profundidad en varias ubicaciones de submuestra. Para mejorar el rendimiento, los cálculos por píxel se realizan una vez para cada píxel cubierto, compartiendo las salidas del sombreador entre los sub píxeles cubiertos. El suavizado de contorno multimuestreo no reduce el alias de superficie. Las ubicaciones de ejemplo y las funciones de reconstrucción dependen de la implementación de hardware.

En la ilustración siguiente se muestran algunos ejemplos.

![ilustración de ejemplos de rasterización de suavizado de contorno multimuestreo](images/d3d10-rasterrulesmsaa.png)

El número de ubicaciones de ejemplo depende del modo multimuestreo. Los atributos de vértice se interpolan en centros de píxeles, ya que aquí es donde se invoca el sombreador de píxeles (esto se convierte en extrapolación si el centro no está cubierto). Los atributos se pueden marcar en el sombreador de píxeles para muestrear centroide, lo que hace que los píxeles no cubiertos interpolan el atributo en la intersección del área del píxel y la primitiva. Un sombreador de píxeles se ejecuta para cada área de 2 x 2 píxeles para admitir cálculos derivados (que usan deltas x e y). Esto significa que las invocaciones del sombreador se producen más de lo que se muestra para rellenar la cantidad mínima de 2x2 (que es independiente de la multimuestreo). El resultado del sombreador se escribe para cada muestra cubierta que pasa la prueba de galería de símbolos de profundidad por ejemplo.

En general, las reglas de rasterización para primitivas no se modifican mediante suavizado de contorno de múltiples muestras, excepto:

-   Para un triángulo, se realiza una prueba de cobertura para cada ubicación de muestra (no para un centro de píxeles). Si se cubre más de una ubicación de ejemplo, un sombreador de píxeles se ejecuta una vez con atributos interpolados en el centro de píxeles. El resultado se almacena (replica) para cada ubicación de muestra cubierta en el píxel que pasa la prueba de profundidad o galería de símbolos.

    Una línea se trata como un rectángulo de dos triángulos, con un ancho de línea de 1,4.

-   Para un punto, se realiza una prueba de cobertura para cada ubicación de muestra (no para un centro de píxeles).

Muchos formatos admiten la multimuestreo (consulte Compatibilidad de hardware con formatos [Direct3D 10),](/previous-versions//cc627090(v=vs.85))algunos formatos se pueden resolver [**(ResolveSubresource,**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource)que reduce el tamaño de ejemplo de un formato multimuestreo a un tamaño de muestra de 1). Los formatos multimuestreo se pueden usar en destinos de representación que se pueden volver a leer en sombreadores mediante la carga [,](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)ya que no se requiere ninguna resolución para las muestras individuales a las que tiene acceso el sombreador. Los formatos de profundidad no se admiten para los recursos multimuestreo, por lo que los formatos de profundidad están restringidos para representar solo los destinos.

Los formatos sin tipo (por ejemplo, R8G8B8A8 TYPELESS) admiten la multimuestreo para permitir que una vista de recursos interprete los datos de \_ maneras diferentes. Por ejemplo, puede crear un recurso multimuestreo mediante R8G8B8A8 TYPELESS, representarlo mediante un recurso render-target-view con un formato UINT R8G8B8A8 Y, a continuación, resolver el contenido en otro recurso con un formato de datos \_ \_ UNORM R8G8B8A8. \_

### <a name="hardware-support"></a>Compatibilidad de hardware

La API informa de la compatibilidad de hardware para la multimuestreo a través del número de niveles de calidad. Por ejemplo, un nivel de calidad 0 significa que el hardware no admite la multimuestreo (en un formato y nivel de calidad determinados). Un 3 para los niveles de calidad significa que el hardware admite tres diseños de ejemplo diferentes o resuelve algoritmos. También puede asumir lo siguiente:

-   Cualquier formato que admita multimuestreo admite el mismo número de niveles de calidad para cada formato de esa familia.
-   Todos los formatos que admiten multimuestreo y que tienen los formatos \_ \_ UNORM, SRGB, \_ SNORM \_ o FLOAT también admiten la resolución.

### <a name="centroid-sampling-of-attributes-when-multisample-antialiasing"></a>Muestreo centroide de atributos al suavizado de contorno de múltiples muestras

De forma predeterminada, los atributos de vértice se interpolan en un centro de píxeles durante el suavizado de contorno de múltiples muestras; Si no se cubre el centro de píxeles, los atributos se extrapolan a un centro de píxeles. Si una entrada de sombreador de píxeles que contiene la semántica centroide (suponiendo que el píxel no está totalmente cubierto) se muestrea en algún lugar dentro del área cubierta del píxel, posiblemente en una de las ubicaciones de ejemplo cubiertas. Se aplica una máscara de ejemplo (especificada por el estado de rasterizador) antes del cálculo de centroide. Por lo tanto, un ejemplo enmascarado no se usará como ubicación de centroide.

El rasterizador de referencia elige una ubicación de muestra para el muestreo centroide similar a la siguiente:

-   La máscara de ejemplo permite todas las muestras. Use un centro de píxeles si el píxel está cubierto o si no se cubre ninguna de las muestras. De lo contrario, se elige el primer ejemplo cubierto, empezando desde el centro de píxeles y avanzando hacia el exterior.
-   La máscara de ejemplo desactiva todas las muestras menos una (un escenario común). Una aplicación puede implementar el supermuestreo multipass si se atraviesan valores de máscara de muestra de un solo bit y se vuelve a representar la escena para cada muestra mediante el muestreo centroide. Esto requeriría que una aplicación ajustara los derivados para seleccionar las mips de textura más detalladas adecuadamente para la mayor densidad de muestreo de textura.

### <a name="derivative-calculations-when-multisampling"></a>Cálculos derivados cuando se realiza la multimuestreo

Los sombreadores de píxeles siempre se ejecutan con un área mínima de 2 x 2 píxeles para admitir cálculos derivados, que se calculan mediante la toma de diferencias entre los datos de píxeles adyacentes (con la suposición de que los datos de cada píxel se han muestreado con espaciado de unidad horizontal o verticalmente). Esto no se ven afectados por el multimuestreo.

Si se solicitan derivados en un atributo del que se ha muestreado centroide, el cálculo de hardware no se ajusta, lo que puede provocar derivados inexactos. Un sombreador esperará un vector de unidad en el espacio de destino de representación, pero puede obtener un vector que no sea de unidad con respecto a algún otro espacio vectorial. Por lo tanto, es responsabilidad de una aplicación mostrar precaución al solicitar derivados de atributos de los que se muestrea centroide. De hecho, se recomienda no combinar derivados y muestreo de centroide. El muestreo de centroide puede ser útil en situaciones en las que es fundamental que los atributos interpolados de una primitiva no se extrapolan, pero esto incluye las recompensas, como los atributos que parecen saltar donde un borde primitivo cruza un píxel (en lugar de cambiar continuamente) o derivados que no se pueden usar en las operaciones de muestreo de textura que derivan loD.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Etapa del rasterizador](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 