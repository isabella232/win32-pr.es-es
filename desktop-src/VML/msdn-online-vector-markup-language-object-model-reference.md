---
title: Referencia del modelo de objetos VML
description: En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa8c608a60cbdb5af0fa5699fb1d458a5f18552
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884167"
---
# <a name="vml-object-model-reference"></a>Referencia del modelo de objetos VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

En este tema:

-   [Introducción](#introduction)
-   [Ejemplo](#example)
-   [Configuración de VML](#setting-up-vml)
-   [Referencia de VML OM](#vml-om-reference)
    -   [Elemento Shape](#shape-element)
-   [Subelementos del elemento Shape](#subelements-of-the-shape-element)
    -   [Elemento Background](#background-element)
    -   [Elemento Desatrusión](#extrusion-element)
    -   [Elemento Fill](#fill-element)
    -   [Elemento Group](#group-element)
    -   [Elemento Imagedata](#imagedata-element)
    -   [Path, elemento](#path-element)
    -   [Elemento Shadow](#shadow-element)
    -   [Elemento Skew](#skew-element)
    -   [Elemento Stroke](#stroke-element)
    -   [Elemento TextPath](#textpath-element)
-   [Tipos de datos usados en el modelo de objetos VML](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a>Introducción

[Lenguaje de marcado de vectores (VML)](https://www.w3.org/TR/NOTE-datetime.html) es un lenguaje basado en texto que usa [XML](https://www.w3.org/TR/REC-xml.mdl) para ampliar HTML con el fin de mostrar información gráfica vectorial. El Document Object Model VML (DOM) define una interfaz de programación para la manipulación de los elementos del documento. Esto permite al usuario crear y modificar dinámicamente gráficos vectoriales a través de una interfaz neutra de la plataforma y del lenguaje. EL DOM de VML se ajusta a la [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) especificación.

VML usa el elemento [Shape](#shape-element) como bloque de creación básico para imágenes gráficas vectoriales. Una vez creada una forma, puede modificarla a través de atributos o subelementos adjuntos. Por ejemplo, para cambiar el color de una forma, asigne un valor de color al **atributo FillColor.**


```HTML
myshape.fillcolor = "red"
```



Varios de los atributos de una forma también son [subelementos y](/windows) tienen sus propios atributos, incluidos los siguientes:

-   [Información preliminar](#background-element)
-   [Extrusión](#extrusion-element)
-   [Fill](#fill-element)
-   [Grupo](#group-element)
-   [Imagedata](#imagedata-element)
-   [Ruta de acceso](#path-element)
-   [Shadow](#shadow-element)
-   [Sesgar](#skew-element)
-   [Golpe](#stroke-element)
-   [TextPath](#textpath-element)

El OM de VML usa varios [tipos de datos](/windows) para definir parámetros. Los tipos de datos con el prefijo "Vg" son enumeraciones y los que tienen el prefijo "IVg" son objetos . Haga clic aquí para obtener una lista. Los tipos de datos menores se enumeran con parámetros específicos.

## <a name="example"></a>Ejemplo

El siguiente código VBScript muestra cómo crear una forma sencilla:


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



En el ejemplo anterior, se crea una forma mediante Document Object Model método **CreateElement**. La forma es una forma rect predefinida de VML. Aunque el objeto existe, no puede formar parte del documento hasta que se adjunta al documento. Con el **método AppendChild,** rect se hace un elemento secundario de un **elemento DIV** denominado MyDiv. Algunos atributos de estilo mínimos **(Position**, **Width**, **Height**, **Top**, **Left)** se establecen para dar a la forma un tamaño específico. Por último, se asigna un color con el **atributo FillColor.** Tenga en cuenta que se puede usar cualquier lenguaje de scripting o cualquier lenguaje que pueda trabajar Document Object Model interfaces.

## <a name="setting-up-vml"></a>Configuración de VML

Una implementación de VML se realiza a través de Microsoft Internet Explorer 5.0 o superior. Para configurar correctamente el objeto de representación en una página web, se deben realizar las siguientes adiciones:

1.  El esquema debe configurarse en la etiqueta &lt; HTML inicial como se muestra a &gt; continuación:
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  El comportamiento de representación debe formar parte del estilo del documento:
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

A continuación se muestra una página web HTML de ejemplo configurada correctamente para VML que muestra la creación dinámica de una forma.


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



Tenga en cuenta que, en las versiones beta, se ActiveX etiqueta de objeto y un estilo de comportamiento diferente.

## <a name="vml-om-reference"></a>Referencia de VML OM

Esta referencia define el [elemento Shape,](#shape-element) [los subelementos](/windows)y [los](/windows) tipos de datos que usa el modelo de objetos de VML.

### <a name="shape-element"></a>Elemento Shape

Las formas son los bloques de creación de imágenes gráficas definidas por Lenguaje de marcado de vectores (VML). La forma es el elemento de nivel superior y varios subelementos ayudan a definir la naturaleza de cada forma.

VML proporciona formas predefinidas:

**Atributos de forma**

-   **Arc**
-   **Curva**
-   **Línea**
-   **Polilínea**
-   **Rect**
-   **RoundRect**



|   Subelemento           |    Descripción                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adj          | [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md). Lista delimitada por comas de números que son los parámetros de las fórmulas de guía que definen el trazado de la forma. Los valores se pueden omitir para permitir el uso de valores predeterminados. Puede haber hasta 8 valores de ajuste.                                                                                                   |
| Alt          | String. Texto alternativo asociado a la forma. Se usa para la exploración no gráfica.                                                                                                                                                                                                                                                                                                 |
| Button       | [DvTriState](msdn-online-vml-vgtristate.md). Muestra el comportamiento del botón al hacer clic.                                                                                                                                                                                                                                                                                                 |
| BWMode       | [DvBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Determina cómo se representará la forma en la vista en blanco y negro en las aplicaciones o cuando se imprime en impresoras en blanco y negro. Los valores incluyen: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**. Valor predeterminado: **Auto**. |
| BWNormal     | DvBlackWhiteMode. Cuando BWMode es Auto, se consulta esta propiedad para obtener información sobre cómo representar la forma en blanco y negro normales. Los valores incluyen: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**. Valor predeterminado: **Auto**.                                                |
| BWPure       | DvBlackWhiteMode. Cuando BWMode es Auto, se consulta esta propiedad para obtener información sobre cómo representar la forma en B/W puro. Los valores incluyen: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**. Valor predeterminado: **Auto**.                                                              |
| ChildShapes  | IVgGroupShapes. Colección de otras formas de este grupo. Esta colección admite los métodos Length y Item estándar.                                                                                                                                                                                                                                                       |
| Chromakey    | [IVgColor](msdn-online-vml-ivgcolor.md). Valor de color que será transparente y mostrará cualquier cosa detrás de la forma.                                                                                                                                                                                                                                                             |
| Control1     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto de control para curva.                                                                                                                                                                                                                                                                                                  |
| Control2     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto de control para curva.                                                                                                                                                                                                                                                                                                  |
| CoordOrigin  | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Coordenadas en la esquina superior izquierda del rectángulo del contenedor. Va de 0 a infinito.                                                                                                                                                                                                                               |
| CoordSize    | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Ancho y alto del espacio de coordenadas dentro del rectángulo de referencia de esta forma. Si no se especifica, es igual que el ancho y alto del rectángulo. Va de 0 a infinito. Valor predeterminado: "1000 1000".                                                                                               |
| EndAngle     | [DvangleInDegrees.](msdn-online-vml-vgangleindegrees-data-type.md) Ángulo final de forma.                                                                                                                                                                                                                                                                                          |
| Extrusión    | IVgExtrusion. Especifica el valor del objeto de extrusión para esta forma. Consulte el [elemento Desatrusión](msdn-online-vml-extrusion-element.md) para obtener más información.                                                                                                                                                                                                                               |
| Rellenar         | FillFillFormat. Especifica el valor de relleno para esta forma. Consulte el [elemento Fill](msdn-online-vml-fill-element.md) para obtener más detalles.                                                                                                                                                                                                                                                |
| FillColor    | [IVgColor](msdn-online-vml-ivgcolor.md). Color principal del pincel que se va a usar para rellenar el trazado de esta forma.                                                                                                                                                                                                                                                                  |
| Lleno       | [DvTriState](msdn-online-vml-vgtristate.md). Si es True, se rellenará la ruta de acceso que define la forma. De forma predeterminada, se rellenará con un color sólido a menos que haya un subelemento Fill que especifique propiedades de relleno más complejas. Si es False, el relleno es transparente.                                                                                                           |
| Voltear         | DvFlipOrientation. Los valores son: X Y XY YX                                                                                                                                                                                                                                                                                                                                         |
| ForceDash    | [DvTriState](msdn-online-vml-vgtristate.md). Indicación de que se debe representar un contorno discontinuo cuando no hay ninguna línea ni relleno para una forma. Este comportamiento suele ser útil para hacer que las formas invisibles sean visibles en las aplicaciones de edición para que se puedan seleccionar y operar, como en un mapa de imágenes.                                                                 |
| Fórmulas     | IVgFormulas. Matriz de fórmulas que define una forma.                                                                                                                                                                                                                                                                                                                          |
| From         | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto inicial de la línea.                                                                                                                                                                                                                                                                                                   |
| Href         | [Cadena](#data-types-used-in-the-vml-object-model). Dirección URL a la que saltar si se hace clic en esta forma.                                                                                                                                                                                                                                                                                 |
| ImageData    | IVgImageData. Información de imagen si la forma es una imagen. Consulte el elemento ImageData para obtener más información.                                                                                                                                                                                                                                                                       |
| OnEd         | [DvTriState](msdn-online-vml-vgtristate.md). Oculta todos los identificadores excepto la parte superior izquierda e inferior derecha, como en los identificadores de un segmento de línea recta.                                                                                                                                                                                                                             |
| Opacidad      | [Accionario](msdn-online-vml-vgfraction-data-type.md). Opacidad de toda la forma. Número entre 0,0 y 1,0.                                                                                                                                                                                                                                                           |
| Ruta de acceso         | IVgPath. Cadena que contiene los comandos que definen la ruta de acceso.                                                                                                                                                                                                                                                                                                                  |
| Puntos       | [IVgPoints](msdn-online-vml-ivgpoints-data-type.md). Colección de puntos que definen una forma.                                                                                                                                                                                                                                                                                   |
| Impresión        | [DvTriState](msdn-online-vml-vgtristate.md). Si es True, esta forma está pensada para imprimirse.                                                                                                                                                                                                                                                                                        |
| Rotación     | [DvangleInDegrees.](msdn-online-vml-vgangleindegrees-data-type.md) Establece la rotación de la forma. El valor se propaga al estilo de forma.                                                                                                                                                                                                                                              |
| Escala        | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Escala de forma.                                                                                                                                                                                                                                                                                                           |
| Shadow       | IVgShadow. Especifica la sombra de esta forma. Consulte el [elemento Shadow](msdn-online-vml-shadow-element.md) para obtener más información.                                                                                                                                                                                                                                                        |
| Spt          | Reservado.                                                                                                                                                                                                                                                                                                                                                                        |
| StartAngle   | [DvangleInDegrees.](msdn-online-vml-vgangleindegrees-data-type.md) Ángulo de inicio de la forma.                                                                                                                                                                                                                                                                                        |
| Carrera       | DvstrokeFormat. Vea Elemento Stroke para obtener más información.                                                                                                                                                                                                                                                                                                                                  |
| Strokecolor  | [IVgColor](msdn-online-vml-ivgcolor.md). Color principal del pincel que se va a usar para acariciar el trazado de esta forma.                                                                                                                                                                                                                                                                |
| Acarició      | [DvTriState](msdn-online-vml-vgtristate.md). Si es True, se trazo el trazado que define la forma.                                                                                                                                                                                                                                                                              |
| StrokeWeight | [SILENGTH](msdn-online-vml-vglength.md). Ancho del pincel que se usará para acariciar la ruta de acceso. Intervalos entre 0 y 1584.                                                                                                                                                                                                                                                           |
| TextPath     | IVgTextPath. Especifica el objeto TextPath de la forma. Consulte el [elemento TextPath](msdn-online-vml-textpath-element.md) para obtener más información.                                                                                                                                                                                                                                  |
| Objetivo           | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto final de la línea.                                                                                                                                                                                                                                                                                                        |
| Tipo         | String. Tipo de forma.                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a>Subelementos del elemento Shape

Los siguientes subelementos forman parte del modelo de objetos VML.

-   [Información preliminar](#background-element)
-   [Extrusión](#extrusion-element)
-   [Fill](#fill-element)
-   [Grupo](#group-element)
-   [Imagedata](#imagedata-element)
-   [Ruta de acceso](#path-element)
-   [Shadow](#shadow-element)
-   [Sesgar](#skew-element)
-   [Golpe](#stroke-element)
-   [TextPath](#textpath-element)

### <a name="background-element"></a>Elemento Background

Describe el relleno del fondo de una página mediante rellenos de VML.


|   Atributo        |   Descripción                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BWMode    | [DvBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Determina cómo se representará la forma en la vista en blanco y negro en las aplicaciones o cuando se imprima.                                     |
| BWNormal  | [DvBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Cuando BWMode es Auto, se consulta esta propiedad para obtener información sobre cómo representar la forma en blanco y negro normales.                        |
| BWPure    | [DvBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Cuando BWMode es Auto, se consulta esta propiedad para obtener información sobre cómo representar la forma en blanco y negro puro.                          |
| Rellenar      | FillFillFormat. Especifica el relleno de esta forma. Vea [Elemento Fill](msdn-online-vml-fill-element.md) para obtener más información.                                                             |
| FillColor | [IVgColor](msdn-online-vml-ivgcolor.md). Color principal del pincel que se va a usar para rellenar el trazado de esta forma. Duplicado del valor Color en el elemento Fill. El valor predeterminado es blanco. |



 

### <a name="extrusion-element"></a>Elemento Desatrusión

Describe una extrusión 3D de la forma.

**Atributos**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>AutoRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Si es True, el centro de rotación del grupo de objetos 3D (de hecho, solo hay un objeto en el grupo) se determina automáticamente como el centro del grupo; De lo contrario, viene determinado por los parámetros RotationCenter, que son una fracción de la forma con 0,0,0 como centro.</td>
</tr>
<tr class="even">
<td>BackDepth</td>
<td><a href="msdn-online-vml-vglength.md"><strong>DvLength</strong></a>. Cantidad de extrusión hacia atrás. Oscila entre 0 y 32767.</td>
</tr>
<tr class="odd">
<td>Luminosidad</td>
<td><a href="#data-types-used-in-the-vml-object-model">DvPositiveNumber</a>. Brillo general de la escena. El valor &quot; predeterminado es 20 000 &quot; .</td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Color de la extrusión. Solo se usa si ColorMode es Personalizado. De lo contrario, Auto establece el color del efecto de extrusión en el mismo que FillColor.</td>
</tr>
<tr class="odd">
<td>ColorMode</td>
<td>Dv3DColorMode. Los valores son:
<ul>
<li>Auto (predeterminado)</li>
<li>Personalizado</li>
</ul></td>
</tr>
<tr class="even">
<td>Diffusity</td>
<td><a href="#data-types-used-in-the-vml-object-model">DvPositiveNumber</a>. Proporción de incidente con luz reflejada difusamente. Los valores menores que 1,0 son normales, pero los valores superiores a uno pueden generar efectos interesantes.</td>
</tr>
<tr class="odd">
<td>Edge</td>
<td><a href="msdn-online-vml-vglength.md">DvLength</a>. Establece el tamaño de un borde biselado redondeado simulado. Oscila entre 0 y 32767 en puntos de punto flotante. El valor predeterminado &quot; es 1pt &quot; .</td>
</tr>
<tr class="even">
<td>Faceta</td>
<td><a href="#data-types-used-in-the-vml-object-model">DvPositiveNumber</a>. Establece la faceta de la escena. El valor &quot; predeterminado es 30 000 &quot; .</td>
</tr>
<tr class="odd">
<td>ForeDepth</td>
<td><a href="msdn-online-vml-vglength.md">DvLength</a>. Cantidad de extrusión hacia delante. Oscila entre 0 y 32767.</td>
</tr>
<tr class="even">
<td>LightFace</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Determina si la cara frontal del objeto responderá a los cambios en la iluminación 3D, por ejemplo, cuando un objeto gira.</td>
</tr>
<tr class="odd">
<td>LightHarsh</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Iluminación desalumbrada para la fuente de luz principal. El valor predeterminado es False.</td>
</tr>
<tr class="even">
<td>LightHarsh2</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Iluminación desalumbrada para la fuente de luz secundaria. El valor predeterminado es False.</td>
</tr>
<tr class="odd">
<td>LightLevel</td>
<td><a href="#data-types-used-in-the-vml-object-model">NumberNumber</a>. Intensidad de la fuente de luz principal. El valor &quot; predeterminado es 38000. &quot;</td>
</tr>
<tr class="even">
<td>LightLevel2</td>
<td><a href="#data-types-used-in-the-vml-object-model">NumberNumber</a>. Intensidad de la fuente de luz secundaria. El valor &quot; predeterminado es 38000. &quot;</td>
</tr>
<tr class="odd">
<td>LightPosition</td>
<td>Vector3D. Posición de la fuente de luz principal. El valor &quot; predeterminado es 50000,0,10000 &quot; .</td>
</tr>
<tr class="even">
<td>LightPosition2</td>
<td>Vector3D. Posición de la fuente de luz secundaria. El valor &quot; predeterminado es -50000,0,10000. &quot;</td>
</tr>
<tr class="odd">
<td>LockRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. &quot;Lockrotationcenter significa que la rotación del grupo se define para que sea mediante ángulo de rotación[1] grados sobre el eje Y de la página seguido de ángulo de rotación[0] grados sobre el eje &quot; X. Cuando LockRotationCenter es False, la rotación se define para que sea por grados de ángulo de orientación sobre el vector definido por la orientación. Por ejemplo, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) equivale a lockrotationcenter=true rotationangle=(0,45).</td>
</tr>
<tr class="even">
<td>Metal</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Hace que la luz reflejada especularmente sea el color del material en lugar del color de la fuente de luz, lo que hace que el objeto parezca más ligero.</td>
</tr>
<tr class="odd">
<td>Activado</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Activa y desactiva la presentación del efecto de extrusión.</td>
</tr>
<tr class="even">
<td>Orientación</td>
<td>Vector3D. Orientación de la cámara.</td>
</tr>
<tr class="odd">
<td>OrientationAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">DvangleInDegrees</a>. Ángulo entre la orientación de la cámara y el plano xy.</td>
</tr>
<tr class="even">
<td>Avión</td>
<td>Dv3DExtrudePlane. Permite la extrusión desde planos ortogonales al plano de pantalla. Requiere que ForeDepth y BackDepth se especifiquen en unidades de dibujo en lugar de emus. Los valores son:
<ul>
<li>XY</li>
<li>ZX</li>
<li>YZ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Representación</td>
<td>Dv3DRenderMode. Los valores son:
<ul>
<li>Solid (predeterminado)</li>
<li>Alambre</li>
<li>BoundingCube</li>
</ul></td>
</tr>
<tr class="even">
<td>RotationAngle</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. AngleX, AngleY o AngleZ se controla mediante el atributo ShapeRotation.</td>
</tr>
<tr class="odd">
<td>RotationCenter</td>
<td>Vector3D. Centro de rotación.</td>
</tr>
<tr class="even">
<td>Brillo</td>
<td><a href="#data-types-used-in-the-vml-object-model">DvPositiveNumber</a>. Determina lo que es la reflexión especular entrelazados o es una reflexión especular. Un valor alto sería de 8 a 10 y se aproximaría a un reflejo, y un valor bajo sería de 2 a 3 y se aproximaría a la ropa entrelazada. Se recomiendan valores de 3 a 7. Los valores altos reflejarán las fuentes de luz precisas.</td>
</tr>
<tr class="odd">
<td>SkewAmt</td>
<td><a href="#data-types-used-in-the-vml-object-model">DvPercentage</a>. Si Type es Parallel, el atributo determina la cantidad de asimetría. Oscila entre 0 y 100.</td>
</tr>
<tr class="even">
<td>SkewAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">DvangleInDegrees</a>. Si Type es Parallel, el atributo determina el grado de asimetría. El valor predeterminado &quot; es -45 &quot; .</td>
</tr>
<tr class="odd">
<td>Especularidad</td>
<td><a href="#data-types-used-in-the-vml-object-model">DvPositiveNumber</a>. Proporción del incidente con la luz reflejada especularmente. Los valores inferiores a 1,0 son normales, pero los valores superiores a uno pueden generar efectos interesantes.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>DvExtrusionType. Los valores son:
<ul>
<li>Parallel (valor predeterminado)</li>
<li>Perspectiva</li>
</ul></td>
</tr>
<tr class="odd">
<td>Mirador</td>
<td>Vector3D. Punto desde el que se está visualizando la escena.</td>
</tr>
<tr class="even">
<td>ViewpointOrigin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Puede tener valores de 0,5 a -0,5 para colocar el origen del punto de vista en el cuadro de límite de forma.</td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a>Elemento Fill

Describe cómo se debe rellenar un trazado para rellenos más complejos que un color sólido.

**Atributos**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>AlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Alinee la imagen con la forma . Si es False, alinee la imagen con la ventana.</td>
</tr>
<tr class="even">
<td>Ángulo</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">DvangleInDegrees</a>. Ángulo a lo largo del cual va el degradado. 0 grados a lo largo del eje horizontal de izquierda a derecha.</td>
</tr>
<tr class="odd">
<td>Aspecto</td>
<td><strong>DvAspectType</strong>. El atributo ImageSize se ajustará para conservar el aspecto de la imagen. Estos valores incluyen:
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignore</td>
<td>Omitir problemas de aspecto.</td>
</tr>
<tr class="even">
<td>Atleast</td>
<td>La imagen es al menos tan grande como el tamaño de la imagen.</td>
</tr>
<tr class="odd">
<td>Atmost</td>
<td>La imagen no es mayor que el tamaño de la imagen.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Color de relleno principal. Igual que el atributo FillColor en forma.</td>
</tr>
<tr class="odd">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Color secundario para un relleno cuando el tipo de imagen es Pattern o un relleno de degradado.</td>
</tr>
<tr class="even">
<td>Colores</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>. Colores intermedios en el degradado y sus posiciones relativas a lo largo del degradado, por ejemplo, &quot; 30 % rojo, 70 % azul, 90 % verde &quot; . El color principal (atributo color en forma) es 0 % y el color secundario (atributo Color2) es 100 %.</td>
</tr>
<tr class="odd">
<td>Foco</td>
<td><a href="#data-types-used-in-the-vml-object-model">DvSignedPercentage</a>. Punto focal para relleno de degradado lineal. Los valores van de -100 a +100.</td>
</tr>
<tr class="even">
<td>FocusPosition</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Posición del rectángulo más interno para degradados radiales. El vector es una fracción (0,0 - 1,0) del ancho y alto de la forma.</td>
</tr>
<tr class="odd">
<td>FocusSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Tamaño del rectángulo más interno para degradados radiales. El vector es una fracción (de 0,0 a 1,0) del ancho y alto de la forma.</td>
</tr>
<tr class="even">
<td>Método</td>
<td>DvsigmaType. Estos valores incluyen:
<ul>
<li>None</li>
<li>Lineal</li>
<li>Sigma</li>
<li>Any</li>
</ul>
<p>El valor predeterminado es Sigma.</p></td>
</tr>
<tr class="odd">
<td>Activado</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Activa la presentación de relleno. Igual que el atributo Fill en forma.</td>
</tr>
<tr class="even">
<td>Opacidad</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">Accionario.</a> Opacidad del relleno.</td>
</tr>
<tr class="odd">
<td>Opacidad2</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">Accionario.</a> Opacidad secundaria de los degradados.</td>
</tr>
<tr class="even">
<td>Origen</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Punto relativo a la esquina superior izquierda de la imagen que se trata como el origen de la imagen. El valor predeterminado es el centro de la imagen. El vector es una fracción (de 0,0 a 1,0) del ancho y alto de la imagen.</td>
</tr>
<tr class="odd">
<td>Posición</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Apunte en el rectángulo de referencia de la forma para colocar el origen de la imagen. El valor predeterminado es el centro del rectángulo del contenedor. El vector es una fracción (0,0 - 1,0) del ancho y alto de la imagen.</td>
</tr>
<tr class="even">
<td>Size</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Tamaño de la imagen. El valor predeterminado es el tamaño de píxel de la imagen. Se puede especificar en coordenadas absolutas o porcentaje.</td>
</tr>
<tr class="odd">
<td>Origen</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadena</a>. Dirección URL de una imagen que se cargará para rellenos de imagen y patrón. Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>TipoDeFillFill. Puede ser uno de los siguientes tipos:
<ul>
<li>Contexto</li>
<li>Frame</li>
<li>Degradado</li>
<li>GradientCenter</li>
<li>GradientRadial</li>
<li>GradientTitle</li>
<li>GradientUnscaled</li>
<li>Patrón</li>
<li>Sólido</li>
<li>Tile</li>
</ul>
Tile, Pattern y Frame requieren que se proporcionan los atributos de imagen. Gradient y GradientRadial requieren que se suministre los atributos de degradado.</td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a>Group, elemento

Un grupo es una colección de formas individuales que se pueden colocar y transformar como una unidad.



|   Atributo        |   Descripción                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| Elemento   | [IVgShape](#data-types-used-in-the-vml-object-model). Elemento especificado en la matriz de formas. |
| Length | [Entero](#data-types-used-in-the-vml-object-model). Número de formas de este grupo.         |



 

### <a name="imagedata-element"></a>Elemento Imagedata

Describe una imagen que se va a representar encima de una forma.



|   Atributo        |   Descripción                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Binivel     | [DvTriState](msdn-online-vml-vgtristate.md). Mostrar la imagen en solo dos colores (normalmente blanco y negro).                                                                                                                                                                                                                                                     |
| BlackLevel  | [Accionario](msdn-online-vml-vgfraction-data-type.md). Permite el ajuste para establecer el nivel de modo que los negro aparezcan como verdaderos negros, y todos los demás colores sean visibles como tonos por encima del negro.                                                                                                                                                                        |
| Chromakey   | [IVgColor](msdn-online-vml-ivgcolor.md). Color transparente de la imagen.                                                                                                                                                                                                                                                                                         |
| CropBottom  | [Numbernumber .](#data-types-used-in-the-vml-object-model) Recortar la distancia desde la parte inferior de la imagen expresada como un porcentaje del tamaño de la imagen.                                                                                                                                                                                                                           |
| CropLeft    | [Numbernumber .](#data-types-used-in-the-vml-object-model) Recortar la distancia desde el borde izquierdo de la imagen expresado como una fracción del tamaño de la imagen (de 0,0 a 1,0). Sin embargo, se admite el "recorte fuera" y, por tanto, se admiten valores de menor que 0 y mayor que 1. Por ejemplo, -5, 20 recortaría los límites 25 veces el tamaño de la imagen con 4/5 en un lado de la imagen. |
| CropRight   | [Numbernumber .](#data-types-used-in-the-vml-object-model) Recortar la distancia desde la derecha de la imagen expresada como un porcentaje del tamaño de la imagen.                                                                                                                                                                                                                            |
| CropTop     | [Numbernumber .](#data-types-used-in-the-vml-object-model) Recortar la distancia desde la parte superior de la imagen expresada como un porcentaje del tamaño de la imagen.                                                                                                                                                                                                                              |
| RelievessColor | [IVgColor](msdn-online-vml-ivgcolor.md). Se establece en un porcentaje del color de sombra para crear un efecto de imagen con relieve.                                                                                                                                                                                                                                 |
| Ganar        | [DvPositiveNumber](#data-types-used-in-the-vml-object-model). Ajusta la intensidad de todos los colores. Básicamente establece lo claro que será el blanco. Oscila entre 0 y 32767.                                                                                                                                                                                           |
| Gamma       | [Accionario](msdn-online-vml-vgfraction-data-type.md). Corrección gamma. Aumentarla proporciona más contraste a una imagen.                                                                                                                                                                                                                                           |
| GrayScale   | [DvTriState](msdn-online-vml-vgtristate.md). Muestra la imagen en colores de escala de grises.                                                                                                                                                                                                                                                                              |
| Origen         | [Cadena](#data-types-used-in-the-vml-object-model). Dirección URL a una imagen que se cargará para los rellenos de imagen y patrón. Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.                                                                                                                                                           |



 

### <a name="path-element"></a>Path, elemento

Define la ruta de acceso que forma la forma, utilizando una cadena que contiene un amplio conjunto de comandos de "movimiento de lápiz".



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Limusina</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>. Define el punto en el que se extiende la forma; Por ejemplo, para una forma de jirafa, el punto de la lira estaría en el cuello, por lo que cuando se cambie el tamaño de la forma, el cuello se ajustará y el resto de la forma mantendrá sus dimensiones.</td>
</tr>
<tr class="even">
<td>TextBoxRect</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>. Matriz que contiene los rectángulos que definen dónde debe ir el texto.</td>
</tr>
<tr class="odd">
<td>V</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadena</a>. Coincide con el atributo v de la etiqueta Path. Tenga en cuenta que path puede corresponder al atributo o elemento Path.</td>
</tr>
<tr class="even">
<td>Valor</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadena</a>. Representación de texto de los comandos que definen la ruta de acceso. Los valores de coordenadas X o y pueden ser una referencia a una fórmula con el formato # es el número ordinal de la fórmula, por &quot; @# &quot; ejemplo, &quot; @2 &quot; . Esta cadena de atributo se forma de un amplio conjunto de comandos, incluidos los siguientes: <br/> 
<table>
<thead>
<tr class="header">
<th>Get-Help</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ae (anglevelopseto)</td>
<td><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong><br/> Dibuje un segmento de una elipse. Se dibuja una línea recta desde el punto actual hasta el punto inicial del segmento.<br/></td>
</tr>
<tr class="even">
<td>al (angleelipse)</td>
<td>Igual que ae, salvo que hay un valor m implícito en el punto inicial del segmento.</td>
</tr>
<tr class="odd">
<td>ar (arc)</td>
<td>Igual que at. Sin embargo, un m implícito inicia una nueva subpath hasta el punto inicial del arco.</td>
</tr>
<tr class="even">
<td>at (arcto)</td>
<td><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y) <br/> Los cuatro primeros valores definen el rectángulo delimitador de una elipse. Los cuatro últimos definen dos vectores radiales. Se dibuja un segmento de la elipse que comienza en el ángulo definido por el vector de radio inicial y termina en el ángulo definido por el vector final. Se dibuja una línea recta desde el punto actual hasta el inicio del arco. El arco siempre se dibuja en sentido contrario a las agujas del reloj. <br/></td>
</tr>
<tr class="odd">
<td>c (curveto)</td>
<td><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>a</strong>(x,y) <br/> Dibuje una curva bézier cúbica desde el punto actual hasta la coordenada que han dado los dos parámetros finales, los puntos de control dados por los cuatro primeros parámetros. El punto actual se convierte en el punto de conexión del bézier.<br/></td>
</tr>
<tr class="even">
<td>e (final)</td>
<td>Finalice el conjunto actual de subpaths. Un conjunto determinado de subpaths (delimitados por el extremo) se rellenan mediante eofill. Los conjuntos posteriores de subpaths se rellenan de forma independiente y se superponen en los existentes.</td>
</tr>
<tr class="odd">
<td>l (lineto)</td>
<td>x,y<br/> Dibuje una línea desde el punto actual hasta la coordenada x,y dada, que se convierte en el nuevo punto actual. Se pueden especificar pares de coordenadas adicionales para formar una polilínea, por ejemplo, &quot; l 10,13,45,27,89,-12 &quot; .<br/></td>
</tr>
<tr class="even">
<td>m (moveto)</td>
<td>x,y<br/> Inicie una nueva subpath en la coordenada x,y dada.<br/></td>
</tr>
<tr class="odd">
<td>nf (nofill)</td>
<td>El conjunto actual de subpaths (delimitado por el final) no se rellenará.</td>
</tr>
<tr class="even">
<td>ns (nostroke)</td>
<td>El conjunto actual de subpaths (delimitado por el final) no se acariciará.</td>
</tr>
<tr class="odd">
<td>qb (quadraticbezier)</td>
<td>(<strong>punto de</strong>control (x, y))*,<strong>final</strong>(x,y) <br/> Define una o varias curvas bézier cuadráticas mediante puntos de control y un punto de conexión. Los puntos intermedios (en curva) se obtienen mediante la interpolación entre puntos de control sucesivos similares a las fuentes TrueType. La subpath no necesita ser un inicio, en cuyo caso el subpath está cerrado y el último punto define el punto inicial.<br/></td>
</tr>
<tr class="even">
<td>qx (ellipticalquadrantx)</td>
<td><strong>end</strong>(x,y) <br/> Se dibuja una elipse de cuarto desde el punto actual hasta el punto de conexión especificado. El segmento elíptico es inicialmente tangencial a una línea paralela al eje X; Es decir, el segmento comienza horizontalmente.<br/></td>
</tr>
<tr class="odd">
<td>qy (ellipticalquadranty)</td>
<td><strong>end</strong>(x,y) <br/> Igual que qx, salvo que el segmento elíptico es inicialmente tangencial a una línea paralela al eje Y; Es decir, el segmento se inicia verticalmente.<br/></td>
</tr>
<tr class="even">
<td>r (rlineto)</td>
<td>x,y <br/> Dibuje una línea desde el punto actual hasta la coordenada relativa (cpx + x, cpy + y). Si se dan pares de coordenadas adicionales, cada nuevo punto se calcula con respecto al último.<br/></td>
</tr>
<tr class="odd">
<td>t (rmoveto)</td>
<td>x,y<br/> Inicie una nueva subpath en las coordenadas relativas (cpx + x, cpy + y) donde cpx, cpy es la posición actual. <br/></td>
</tr>
<tr class="even">
<td>v (curveto)</td>
<td><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>a</strong> (x,y) <br/> Curva bézier cúbica con las coordenadas dadas en relación con el punto actual. Todos los puntos se calculan con respecto al mismo punto inicial.<br/></td>
</tr>
<tr class="odd">
<td>wa (clockwisearcto)</td>
<td>Igual que en , pero el arco se dibuja en el sentido de las agujas del reloj.</td>
</tr>
<tr class="even">
<td>wr (en el sentido de las agujas del reloj)</td>
<td>Igual que ar, pero se dibuja en el sentido de las agujas del reloj.</td>
</tr>
<tr class="odd">
<td>x (cerrar)</td>
<td>Cierre la sub ruta de acceso actual dibujando una línea recta desde el punto actual hasta el punto de movimiento original.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a>Elemento Shadow

Describe un efecto de sombra en una forma.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Color de la sombra principal. El valor predeterminado es RGB(128 128 128)</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Color de la segunda sombra o resaltado en una sombra con relieve o con relieve. El valor predeterminado es RGB(203,203,203).</td>
</tr>
<tr class="odd">
<td>Matriz</td>
<td><a href="#data-types-used-in-the-vml-object-model">IvgMuswMatrix</a>. Una matriz de transformación de perspectiva con el formato &quot; sxx,sxy,syx,syy,px,py &quot; [s=scale, p=perspective]. Los elementos s especifican cómo se debe escalar la sombra con respecto a la forma y los elementos p especifican cómo se debe sesgar la sombra con respecto a la forma. Por ejemplo, la siguiente matriz cambia el tamaño de la forma por un factor de 2 y la sesga por un factor de 4 en todas las direcciones: <br/> &quot;2,2,2,2,4,4&quot;<br/> Esta matriz solo se usa si el tipo de la sombra se establece en perspective.<br/></td>
</tr>
<tr class="even">
<td>Oscurecido</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. La sombra se puede ver a través de si no hay ningún relleno en la forma. El valor predeterminado es False.</td>
</tr>
<tr class="odd">
<td>Offset</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgMuswOffset</a>. Cantidad de desplazamiento x,y desde la ubicación de la forma. El valor &quot; predeterminado es 2pt,2pt &quot; .</td>
</tr>
<tr class="even">
<td>Offset2</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Cantidad de desplazamiento x,y segundo desde la ubicación de la forma. Los valores son una medida absoluta o un valor fraccionrio de forma (de -0,5 a +0,5).</td>
</tr>
<tr class="odd">
<td>Activado</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Activa y desactiva la presentación de la sombra.</td>
</tr>
<tr class="even">
<td>Opacidad</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">DvIon.</a> Opacidad del efecto de sombra.</td>
</tr>
<tr class="odd">
<td>Origen</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Par de valores fraccionales de forma de -0,5 a +0,5.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><a href="#data-types-used-in-the-vml-object-model">DvshadowType</a>. Los valores son:
<ul>
<li>Single (valor predeterminado)</li>
<li>Double</li>
<li>Perspectiva</li>
<li>ShapeRelative</li>
<li>DrawingRelative</li>
<li>Emboss</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a>Elemento Skew

Describe un efecto de asimetría de perspectiva en una forma. La asimetría se aplica a los datos gráficos vectoriales, no a los datos de imagen.



|   Atributo        |   Descripción                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Matriz | [IVgMuswMatrix](#data-types-used-in-the-vml-object-model). Una matriz de transformación de perspectiva con el formato "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective \] . Si offset está en unidades absolutas, px,py están en emu ^ -1 unidades; De lo contrario, son una fracción inversa del tamaño de la forma. |
| Offset | [IvgMuswOffset](#data-types-used-in-the-vml-object-model). Cantidad de desplazamiento x,y desde la ubicación de la forma. El valor predeterminado es "2pt,2pt".                                                                                                                                                   |
| Activado     | [DvTriState](msdn-online-vml-vgtristate.md). Activa o desactiva la presentación del sesgo.                                                                                                                                                                                             |
| Origen | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Par de valores fraccionales de forma de -0,5 a +0,5.                                                                                                                                                                     |



 

### <a name="stroke-element"></a>Elemento Stroke

Describe cómo dibujar el trazado si se desea algo más allá de una línea sólida con un color sólido.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Color de la línea. Igual que el atributo StrokeColor en Shape, pero lo invalida.</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Color secundario. Se usa cuando FillType es Pattern.</td>
</tr>
<tr class="odd">
<td>DashStyle</td>
<td><strong>DvLineDashStyle</strong>. Formato de estilo de guión. Puede ser un valor específico o una secuencia de números con un patrón de guion definido por el usuario. Los valores son:
<ul>
<li>Solid (predeterminado)</li>
<li>ShortDash</li>
<li>ShortDot</li>
<li>ShortDashDot</li>
<li>ShortDashDotDot</li>
<li>Punto</li>
<li>Guión</li>
<li>DashDot</li>
<li>LongDash</li>
<li>LongDashDot</li>
<li>LongDashDotDot</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrow</td>
<td><strong>DomainArrowheadStyle</strong>. Punta de flecha para el final de la línea. Los valores son:
<ul>
<li>Ninguna (valor predeterminado)</li>
<li>Bloquear</li>
<li>Clásico</li>
<li>Diamond</li>
<li>Elipse</li>
<li>Abrir</li>
<li>Comillas angulares</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>EndArrowLength</td>
<td><strong>DvArrowHeadLength</strong>. Longitud de la punta de flecha para el final de la línea. Los valores son:
<ul>
<li>Short</li>
<li>Media (valor predeterminado)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrowWidth</td>
<td><strong>DvArrowheadWidth</strong>. Ancho de flecha para el final de la línea. Los valores son:
<ul>
<li>Estrecho</li>
<li>Media (valor predeterminado)</li>
<li>Ancho</li>
</ul></td>
</tr>
<tr class="odd">
<td>Endcap</td>
<td><strong>DvLineEndCapStyle</strong>. Los valores son:
<ul>
<li>Plano</li>
<li>Square</li>
<li>Round</li>
</ul></td>
</tr>
<tr class="even">
<td>FillType</td>
<td><strong>DvLineFillType</strong>. Los valores son:
<ul>
<li>Solid (predeterminado)</li>
<li>Tile</li>
<li>Patrón</li>
<li>Frame</li>
</ul></td>
</tr>
<tr class="odd">
<td>ImageAlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Alinee la imagen con la forma . Si es False, alinee la imagen con la ventana.</td>
</tr>
<tr class="even">
<td>ImageAspect</td>
<td><strong>DvAspectType</strong>. El atributo ImageSize se ajustará para conservar el aspecto de la imagen. Estos valores incluyen:
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignore</td>
<td>Omitir problemas de aspecto.</td>
</tr>
<tr class="even">
<td>Atleast</td>
<td>La imagen es al menos tan grande como el tamaño de la imagen.</td>
</tr>
<tr class="odd">
<td>Atmost</td>
<td>La imagen no es mayor que el tamaño de la imagen.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>ImageSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Tamaño de la imagen con la que se formará el pincel. El valor predeterminado es el tamaño de la imagen.</td>
</tr>
<tr class="even">
<td>JoinStyle</td>
<td><strong>BvLineJoinStyle</strong>. Los valores son:
<ul>
<li>Redondeada (unión redondeada)</li>
<li>Bisel (juntas biseladas)</li>
<li>Miter (miter joint)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Estilo de línea</td>
<td><strong>StyleLineStyle</strong>. Los valores son:
<ul>
<li>Single</li>
<li>ThinThin (1:1:1)</li>
<li>ThinThick (1:1:2)</li>
<li>ThickThin (2:1:1)</li>
<li>ThickBetweenThin (1:1:2:1:1)</li>
</ul></td>
</tr>
<tr class="even">
<td>MiterLimit</td>
<td><a href="msdn-online-vml-vglength.md">Longitud</a>. Distancia máxima entre el punto interno y el punto exterior de una unión. Este número es un múltiplo del grosor de la línea. Oscila entre 0 y 32 767.</td>
</tr>
<tr class="odd">
<td>Activado</td>
<td><a href="msdn-online-vml-vgtristate.md">DvTriState</a>. Activa y desactiva la presentación de la línea. Igual que el atributo Stroke en Shape, pero lo invalida.</td>
</tr>
<tr class="even">
<td>Opacidad</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">DvIon.</a> Opacidad del trazo.</td>
</tr>
<tr class="odd">
<td>Origen</td>
<td>String. Dirección URL de una imagen que se cargará para rellenos de imagen y patrón. Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.</td>
</tr>
<tr class="even">
<td>StartArrow</td>
<td><strong>DomainArrowheadStyle</strong>. Punta de flecha para el inicio de la línea. Los valores son:
<ul>
<li>Ninguna (valor predeterminado)</li>
<li>Bloquear</li>
<li>Clásico</li>
<li>Diamond</li>
<li>Elipse</li>
<li>Abrir</li>
<li>Comillas angulares</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>StartArrowLength</td>
<td>DomainArrowHeadLength. Longitud de la punta de flecha para el inicio de la línea. Los valores son:
<ul>
<li>Short</li>
<li>Media (valor predeterminado)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>StartArrowWidth</td>
<td>DomainArrowheadWidth. Ancho de punta de flecha para el inicio de la línea. Los valores son:
<ul>
<li>Ancho estrecho medio (valor predeterminado)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Peso</td>
<td><a href="msdn-online-vml-vglength.md">DvLength</a>. Ancho de línea. Oscila entre 0 y 1584.
<div class="alert">
<blockquote>
[!Note]<br />
El atributo DashStyle permite al usuario especificar un patrón de guion definido de forma personalizada. Esto se hace mediante una serie de números. Los estilos de guion se definen en términos de la longitud del guión (la parte dibujada del trazo) y la longitud del espacio entre los guiones. Las longitudes son relativas al ancho de línea; una longitud de &quot; 1 &quot; es igual al ancho de línea. El estilo EndCap se aplica a cada guión, no a los estilos de flecha. La cadena define primero la longitud del guión y, a continuación, la longitud del espacio. Esto se puede repetir para formar estilos de guion complejos. La cadena siempre debe contener un par de números; si contiene un número impar de números, se puede pasar por alto el último. En la tabla siguiente se enumeran algunos valores típicos y una descripción del efecto previsto. &quot;0 &quot; implica un punto que debe ser cuatro veces simétrico (con las puntas de finalización redondeados debe ser un círculo). Si el final de línea es Plano, un visor debe elegir un guión del sistema operativo integrado siempre que sea posible (es decir, algo que es rápido de dibujar). A continuación se muestran algunos ejemplos.
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td>&quot;2 2&quot;</td>
<td>guiones cortos (cada guión y el espacio entre ellos es el doble del ancho de la línea)</td>
</tr>
<tr class="even">
<td>&quot;1 2&quot;</td>
<td>dot (cada guión es el ancho de la línea, mientras que cada espacio tiene el doble de ancho que la línea)</td>
</tr>
<tr class="odd">
<td>&quot;4 2&quot;</td>
<td>dash (cada guión es cuatro veces el ancho de la línea, mientras que cada espacio es el doble del ancho de la línea)</td>
</tr>
<tr class="even">
<td>&quot;8 2&quot;</td>
<td>long-dash</td>
</tr>
<tr class="odd">
<td>&quot;4 2 1 2&quot;</td>
<td>punto de guión</td>
</tr>
<tr class="even">
<td>&quot;8 2 1 2&quot;</td>
<td>punto long-dash</td>
</tr>
<tr class="odd">
<td>&quot;8 2 1 2 1 2&quot;</td>
<td>punto de guion largo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a>Elemento TextPath

Describe una ruta de acceso vectorial basada en los datos de texto, la fuente y los estilos proporcionados. La ruta de acceso de texto se deforma para ajustarse a un **elemento Path** si se proporciona.



|   Atributo        |   Descripción                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| FitPath  | [DvTriState](msdn-online-vml-vgtristate.md). Tamaños del texto para rellenar la ruta de acceso en la que se encuentra.                                 |
| FitShape | [DvTriState](msdn-online-vml-vgtristate.md). Extiende la ruta de texto hasta los bordes del cuadro de forma.                      |
| Activado       | [DvTriState](msdn-online-vml-vgtristate.md). Determina si se muestran o no las rutas de acceso de caracteres.                    |
| String   | String. Texto que se representará como una ruta de acceso de texto.                                                                                    |
| Trim     | [DvTriState](msdn-online-vml-vgtristate.md). Quita cualquier espacio adicional reservado para ascendentes y descendientes si no se usa. |
| Xscale   | [DvTriState](msdn-online-vml-vgtristate.md). Use la medida x recta en lugar de medir a lo largo de la ruta de acceso.                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a>Tipos de datos usados en el modelo de objetos VML

El modelo de objetos VML usa los siguientes tipos de datos.

-   [Double](/windows)
-   [Fijo](/windows)
-   [Entero](/windows)
-   [IVgAdjustments](/windows)
-   [IVgColor](/windows)
-   [IVgEquation](/windows)
-   [IVgFixedRectangle](/windows)
-   [IVgFixedRectangleArray](/windows)
-   [IVgFormula](/windows)
-   [IVgFormulas](/windows)
-   [IVgGradientColorArray](/windows)
-   [IVgPoints](/windows)
-   [IVg DragMatrix](/windows)
-   [IVgMuswOffset](/windows)
-   [IVgVector2D](/windows)
-   [IVgVector3D](/windows)
-   [Duración](/windows)
-   [Medida](/windows)
-   [String](/windows)
-   [DvBlackWhiteMode](/windows)
-   [Accionario](/windows)
-   [DvTriState](/windows)

**Tipo de datos double**

Entero de precisión doble con intervalo de -infinity a infinito.

**Tipo de datos fijo**

Número de punto flotante con un intervalo de -32.766.0 a 32.766,0.

**Tipo de datos entero**

Entero con un intervalo de -infinity a infinity.

**Tipo de datos IVgAdjustments**

Colección de ajustes en una forma que se puede usar para cambiar las dimensiones de una forma. Los ajustes se pueden usar como marcadores de posición temporales o por cualquier motivo usaría variables. Solo hay 8 ajustes en la colección.



| Atributo | Descripción                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exists     | [IVgTriState](msdn-online-vml-vgtristate.md). Determina si existe un ajuste especificado. Tenga en cuenta que se debe usar un índice; es decir, exists( item ) debe usarse para recuperar la existencia de un elemento.                                                                                                                                                                   |
| Elemento       | [Largo.](#data-types-used-in-the-vml-object-model) Matriz de ajustes indizados de 0 a 7. Tenga en cuenta que los ajustes se pueden especificar de forma sparcely; Es decir, es posible que los valores intermedios de la matriz no siempre se llenen. Por ejemplo, los elementos 1, 3 y 5 podrían tener valores para una longitud de 3, con item(0), item(2) y item(4) especificados. Para ver si existe un elemento, use el atributo Exists. |
| Length     | [Entero](#data-types-used-in-the-vml-object-model). Número de ajustes. No puede ser mayor que 8.                                                                                                                                                                                                                                                                          |
| Valor      | [Cadena](#data-types-used-in-the-vml-object-model). Representación de texto de valores numéricos, con comas entre cada número.                                                                                                                                                                                                                                                    |



 

**IVgColor**

Especifica un color.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>RGB</td>
<td><strong>DverGBType</strong>. Valor RGB (Long) del color. Solo es válido si Type es RGB.</td>
</tr>
<tr class="even">
<td>R</td>
<td><a href="#data-types-used-in-the-vml-object-model">Entero</a>. Componente rojo del color. Puede oscilar entre 0 y 255.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><a href="#data-types-used-in-the-vml-object-model">Entero</a>. Componente verde del color. Puede oscilar entre 0 y 255.</td>
</tr>
<tr class="even">
<td>B</td>
<td><a href="#data-types-used-in-the-vml-object-model">Entero</a>. Componente azul del color. Puede oscilar entre 0 y 255.</td>
</tr>
<tr class="odd">
<td>String</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadena</a>. Representación de texto del color. Se admiten los siguientes tipos de colores con nombre:
<ul>
<li>Negro (#000000)</li>
<li>Silver (#C0C0C0)</li>
<li>Gris (#808080)</li>
<li>Blanco (#FFFFFF)</li>
<li>Maroon (#800000)</li>
<li>Rojo (#FF0000)</li>
<li>Púrpura (#800080)</li>
<li>Siia (#FF00FF)</li>
<li>Verde (#008000)</li>
<li>Lime (#00FF00)</li>
<li>Negra (#808000)</li>
<li>Amarillo (#FFFF00)</li>
<li>India (#000080)</li>
<li>Azul (#0000FF)</li>
<li>Teal (#008080)</li>
<li>Aqua (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>DvcolorType</strong>. Tipo de color. Uno de los tipos siguientes:
<ul>
<li>Mixto</li>
<li>con nombre</li>
<li>RGB</li>
<li>Scheme</li>
</ul></td>
</tr>
</tbody>
</table>



 

**IVgEquation**

Ecuaciones usadas para fórmulas.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Operación</td>
<td><strong>BvEquationOperationType</strong> Nombre de la operación que se realizará en los parámetros. Las siguientes operaciones se pueden usar en una ecuación:
<table>
<thead>
<tr class="header">
<th>Operación</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Abs</td>
<td>Valor absoluto. <br/> <strong>abs</strong>(v) <br/></td>
</tr>
<tr class="even">
<td>Atan2</td>
<td>Aritmética polar: da como resultado unidades fd (grados multiplicados por 65536).<br/> <strong>atan2</strong>(p1,v) <br/></td>
</tr>
<tr class="odd">
<td>Cos</td>
<td>Coseno, argumento en unidades fd (grados multiplicados por 65536).<br/> v * <strong>cos</strong>(p1) <br/></td>
</tr>
<tr class="even">
<td>Cosatan2</td>
<td>Conserva la precisión completa en el cálculo intermedio.<br/> v * <strong>cos(atan2(</strong> p2,p1 <strong>))</strong><br/></td>
</tr>
<tr class="odd">
<td>Elipse</td>
<td>Elipse</td>
</tr>
<tr class="even">
<td>Si</td>
<td>Prueba de condición if. v > 0 <strong>?</strong> p1: p2</td>
</tr>
<tr class="odd">
<td>Máx.</td>
<td>Mayor de dos valores. <br/> <strong>max</strong>(v,p1) <br/></td>
</tr>
<tr class="even">
<td>Mid</td>
<td>Average ( v + p1)/2</td>
</tr>
<tr class="odd">
<td>Min</td>
<td>Menor de dos valores. <strong>min</strong>(v,p1)</td>
</tr>
<tr class="even">
<td>Mod</td>
<td>Valor absoluto.</td>
</tr>
<tr class="odd">
<td>Producto</td>
<td>Se usa para la multiplicación y la división. v * p1 / p2</td>
</tr>
<tr class="even">
<td>Seno</td>
<td>Seno, argumento en unidades fd (grados multiplicados por 65536). <br/> v * <strong>sin</strong>(p1) <br/></td>
</tr>
<tr class="odd">
<td>Sinatan2</td>
<td>Conserva la precisión completa en el cálculo intermedio. v * <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</td>
</tr>
<tr class="even">
<td>Sqrt</td>
<td>El resultado es positivo y se redondea hacia abajo. <br/> <strong>sqrt</strong>(v) <br/></td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>Se usa para sumar y restar.<br/> v + p1 p2<br/></td>
</tr>
<tr class="even">
<td>Sumangle</td>
<td>Ángulo existente (escalado en 65536), donde p1 y p2 están en grados.<br/> v + p1 * 65536 + p2 * 65536<br/></td>
</tr>
<tr class="odd">
<td>Tan</td>
<td>Tangente, el argumento está en unidades fd (grados multiplicados por 65536). <br/> v * tan( p1 )<br/></td>
</tr>
<tr class="even">
<td>Val</td>
<td>Define un valor de guía de otro valor.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param1</td>
<td><strong>Entero</strong>. El primer parámetro.</td>
</tr>
<tr class="odd">
<td>Paramtype1</td>
<td><strong>DvFormulaParamType</strong>. Tipo del primer parámetro. Se admiten los valores siguientes:
<table>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor</td>
<td>El parámetro es un valor simple.</td>
</tr>
<tr class="even">
<td>AdjustmentReference</td>
<td>El parámetro es una referencia a un ajuste. Por ejemplo, si el primer parámetro es 1, se usará el valor del primer ajuste.</td>
</tr>
<tr class="odd">
<td>FormulaReference</td>
<td>El parámetro es el resultado de una referencia al resultado de una fórmula anterior. Por ejemplo, si el primer parámetro es 2, se usará el resultado de la fórmula 2.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param2</td>
<td><strong>Entero</strong>. El segundo parámetro.</td>
</tr>
<tr class="odd">
<td>Paramtype2</td>
<td><strong>DvFormulaParamType</strong> Tipo del parámetro 2.</td>
</tr>
<tr class="even">
<td>Val</td>
<td><strong>Entero</strong>. Resultado.</td>
</tr>
<tr class="odd">
<td>Valtype2</td>
<td><strong>DvFormulaParamType</strong>. Tipo del resultado.</td>
</tr>
</tbody>
</table>



 

**IVgFixedRectangle**

Especifica un rectángulo fijo.



| Atributo | Descripción                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Valor      | [Cadena](#data-types-used-in-the-vml-object-model). Valor de texto que especifica la ruta de acceso.         |
| Left       | [Double](#data-types-used-in-the-vml-object-model). Coordenada situada más a la izquierda del rectángulo.   |
| Superior        | [Double](#data-types-used-in-the-vml-object-model). Coordenada superior del rectángulo.    |
| Right      | [Double](#data-types-used-in-the-vml-object-model). Coordenada situada más a la derecha del rectángulo.  |
| Inferior     | [Double](#data-types-used-in-the-vml-object-model). Coordenada inferior del rectángulo. |



 

**IVgFixedRectangleArray**

Matriz de rectángulos fijos.



| Atributo | Descripción                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| Valor      | [Cadena](#data-types-used-in-the-vml-object-model). Representación de texto de la matriz.                           |
| Length     | [Entero](#data-types-used-in-the-vml-object-model). Número de rectángulos de esta matriz.                    |
| Elemento       | [IVgFixedRectangle](#data-types-used-in-the-vml-object-model). Objeto de rectángulo en el índice especificado. |



 

**Tipo de datos IVgFormula**

Definiciones de fórmulas que pueden variar el trazado de una forma o usarse para otros fines de cálculo. Las fórmulas se pueden basar en el **atributo Adj** de una forma, que puede cambiar. Las fórmulas también pueden hacer referencia a otras fórmulas.



| Atributo| Descripción                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eqn        | [IVgEquation](#data-types-used-in-the-vml-object-model). Cada fórmula define un valor único como resultado de la evaluación de la expresión. La expresión se define mediante este atributo y tiene la forma general de una operación seguida de hasta tres argumentos, que pueden ser valores de ajuste (por ejemplo, 2), los resultados de fórmulas anteriores (por ejemplo, ), números fijos o valores \# @2 predefinidos. |



 

**Tipo de datos IVgFormulas**

Colección de objetos de fórmula.



| Atributo | Descripción                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Length     | [Entero](#data-types-used-in-the-vml-object-model). Número de objetos de fórmula de la colección.                                                |
| Elemento       | [IVgFormula](#data-types-used-in-the-vml-object-model). Una fórmula específica. Tenga en cuenta que la matriz de fórmulas se puede heredar en el tipo de forma. |



 

**IVgGradientColorArray**

Matriz de colores que definen un degradado (intervalo combinado de colores).



| Atributo | Descripción                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| Valor      | [Cadena](#data-types-used-in-the-vml-object-model). Especifica la matriz de colores; por ejemplo, "red .2; verde .4; black .7" |
| Length     | [Entero](#data-types-used-in-the-vml-object-model). Número de colores de la matriz.                                          |



 



| Método     | Descripción                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddColor    | [Accionario](msdn-online-vml-vgfraction-data-type.md). Agrega un nuevo color en el punto de conexión especificado por fracción. El nuevo color es blanco de forma predeterminada y es el valor devuelto. A continuación, el color se puede cambiar por referencia. |
| RemoveColor | [Accionario](msdn-online-vml-vgfraction-data-type.md). Quita un color en el punto de conexión especificado por fracción. Nota: Si 0,0 o 1,0 no existe, está implícito y el color blanco se usa en ese momento.          |



 

**Tipo de datos IVgPoints**

Matriz de puntos que definen una forma.



| Atributo | Descripción                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Valor      | [Cadena](#data-types-used-in-the-vml-object-model). Representación de texto de la matriz.           |
| Length     | [Entero](#data-types-used-in-the-vml-object-model). Número de puntos de esta matriz.        |
| Elemento       | [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto en el índice especificado. |



 

**Tipo de datos IVgSkewMatrix**

Matriz usada para sesgar formas, una matriz de transformación de perspectiva con el formato "*sxx,sxy,syx,syy,px,py* " \[ *s* =scale, *p* =perspective \] . Si offset está en unidades absolutas, *px,py* están en unidades emu ^-1; de lo contrario, son una fracción inversa del tamaño de forma.



| Atributo   | Descripción                                         |
|--------------|-----------------------------------------------------|
| XtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| XtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| PerspectiveX | [Double](#data-types-used-in-the-vml-object-model). |
| PerspectiveY | [Double](#data-types-used-in-the-vml-object-model). |



 

**IVgSkewOffset**

Especifica el desplazamiento del sesgo.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadena</a>. Representación de texto de desplazamiento.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente X. Porcentaje o medida. Si no hay unidades, el tipo ShapeRelative está implícito; De lo contrario, el tipo absoluto está implícito.</td>
</tr>
<tr class="odd">
<td>Y</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Y.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>DvTransformwTransformType</strong>. Especifica el tipo de transformación. Los valores válidos son puntos enteros comprendidos entre -infinity e infinity. 
<table>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShapeRelative</td>
<td>Los valores del desplazamiento son porcentajes (relaciones) del tamaño de la forma original; Por ejemplo, un valor de 0,5 significa un desplazamiento a la mitad del tamaño de la forma.</td>
</tr>
<tr class="even">
<td>Absoluto</td>
<td>Los valores son unidades absolutas.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

**Tipo de datos IVgVector2D**

Especifica un vector bidimensional que consta de dos **números Double.**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor</td>
<td><strong>Cadena</strong>. Representación de texto de ambos números vectoriales separados por un espacio.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente X de este vector.</td>
</tr>
<tr class="odd">
<td>S</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Y de este vector.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>DvvectorType</strong>. Unidades esperadas para este vector. Los valores son:
<ul>
<li>Medida</li>
<li>Length</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>Entero de porcentaje de número</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Tipo de datos IVgVector3D**

Especifica un vector tridimensional que consta de tres **números Double.**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Valor</td>
<td><strong>Cadena</strong>. Representación de texto de tres números vectoriales separados por un espacio.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente X de este vector.</td>
</tr>
<tr class="odd">
<td>Y</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Y de este vector.</td>
</tr>
<tr class="even">
<td>Z</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Z de este vector.</td>
</tr>
<tr class="odd">
<td>Tipo</td>
<td><strong>DvvectorType</strong>. Unidades esperadas para este vector. Los valores son:
<ul>
<li>Medida</li>
<li>Length</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>Número</li>
<li>Porcentaje</li>
<li>Entero</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Tipo de datos Length**

Número de punto flotante con un intervalo de 0 a infinito.

**Tipo de datos de medida**

Número de punto flotante de -infinity a infinity.

**Tipo de datos String**

Datos de caracteres de cualquier longitud.

**DvBlackWhiteMode**

Modo de representación para blanco y negro. Los valores posibles son:

-   **Color**
-   **Automático**
-   **Grises**
-   **LightGrayScale**
-   **InverseGray**
-   **GrayOutline**
-   **BlackTextAndLines**
-   **HighContrast**
-   **Negro**
-   **Blanco**
-   **Sin dibujar**

**Tipo de datos Desconexión**

Número de punto flotante con un intervalo de 0,0 a 1,0. Las fracciones también se pueden especificar como porcentaje; Por ejemplo, "50 %".

**Tipo de datos DvTriState**

Enumeración usada para valores que pueden ser uno de tres estados:

-   **TRUE**
-   **FALSE**
-   **COMBINACIÓN**
