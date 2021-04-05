---
title: Referencia del modelo de objetos VML
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889c977260548c26bbfd8196160e4537ccb8895d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078275"
---
# <a name="vml-object-model-reference"></a>Referencia del modelo de objetos VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

En este tema:

-   [Introducción](#introduction)
-   [Ejemplo](#example)
-   [Configurar VML](#setting-up-vml)
-   [Referencia de OM de VML](#vml-om-reference)
    -   [Elemento de forma](#shape-element)
-   [Subelementos del elemento de forma](#subelements-of-the-shape-element)
    -   [Background (elemento)](#background-element)
    -   [Elemento extrusión](#extrusion-element)
    -   [Elemento Fill](#fill-element)
    -   [Group, elemento](#group-element)
    -   [Elemento ImageData](#imagedata-element)
    -   [Path, elemento](#path-element)
    -   [Elemento Shadow](#shadow-element)
    -   [Sesgar elemento](#skew-element)
    -   [Elemento stroke](#stroke-element)
    -   [Elemento TextPath](#textpath-element)
-   [Tipos de datos utilizados en el modelo de objetos VML](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a>Introducción

[Lenguaje de marcado de vectores (VML)](https://www.w3.org/TR/NOTE-datetime.html) es un lenguaje basado en texto que usa [XML](https://www.w3.org/TR/REC-xml.mdl) para extender HTML con el fin de Mostrar información de gráficos vectoriales. El Document Object Model VML (DOM) define una interfaz de programación para la manipulación de los elementos de documento. Esto permite al usuario crear y modificar dinámicamente gráficos vectoriales a través de una interfaz independiente de la plataforma y del lenguaje. DOM de VML se ajusta a la especificación [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) .

VML usa el elemento de [forma](#shape-element) como el bloque de creación básico para las imágenes de gráficos vectoriales. Una vez creada una forma, puede modificar la forma a través de atributos o de subelementos adjuntos. Por ejemplo, para cambiar el color de una forma, asigne un valor de color al atributo **fillColor** .


```HTML
myshape.fillcolor = "red"
```



Algunos de los atributos de una forma también son [subelementos](/windows) y tienen sus propios atributos, entre los que se incluyen los siguientes:

-   [Información preliminar](#background-element)
-   [Trusión](#extrusion-element)
-   [Fill](#fill-element)
-   [Grupo](#group-element)
-   [Imagedata](#imagedata-element)
-   [Ruta de acceso](#path-element)
-   [Shadow](#shadow-element)
-   [Sesgar](#skew-element)
-   [Stroke](#stroke-element)
-   [TextPath](#textpath-element)

El modelo de objetos de VML usa varios [tipos de datos](/windows) para definir parámetros. Los tipos de objeto que tienen el prefijo "VG" son enumeraciones y los que tienen el prefijo "IVg" son objetos. Haga clic aquí para obtener una lista. Los tipos de información secundarios se enumeran con parámetros específicos.

## <a name="example"></a>Ejemplo

El siguiente código VBScript muestra cómo crear una forma simple:


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



En el ejemplo anterior, se crea una forma mediante el método Document Object Model **createElement**. La forma es una forma Rect predefinida de VML. Aunque existe el objeto, no puede formar parte del documento hasta que se adjunte al documento. Con el método **appendChild** , el Rect se convierte en un elemento secundario de un elemento **div** denominado MyDiv. Algunos atributos de estilo mínimos (**posición**, **ancho**, **alto**, **superior**, **izquierda**) se establecen para dar a la forma un tamaño específico. Por último, se asigna un color con el atributo **fillColor** . Tenga en cuenta que se puede usar cualquier lenguaje de scripting o cualquier lenguaje que pueda trabajar con interfaces Document Object Model.

## <a name="setting-up-vml"></a>Configurar VML

Una implementación de VML se realiza a través de Microsoft Internet Explorer 5,0 o superior. Para configurar correctamente el objeto de representación en una página web, se deben realizar las siguientes adiciones:

1.  El esquema se debe configurar en la <HTML> como se indica a continuación:
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



Tenga en cuenta que en las versiones beta, se necesitaba una etiqueta de objeto ActiveX y un estilo de comportamiento diferente.

## <a name="vml-om-reference"></a>Referencia de OM de VML

Esta referencia define el elemento de [forma](#shape-element) , los [subelementos](/windows)y los [tipos de datos](/windows) que usa el modelo de objetos de VML.

### <a name="shape-element"></a>Elemento de forma

Las formas son los bloques de creación de las imágenes gráficas definidas por Lenguaje de marcado de vectores (VML). La forma es el elemento de nivel superior y varios subelementos ayudan a definir la naturaleza de cada forma.

VML proporciona formas predefinidas:

**Atributos de forma**

-   **Arc**
-   **Sensible**
-   **Line**
-   **PolyLine**
-   **Rect**
-   **RoundRect**



|              |                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ajustar          | [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md). Una lista delimitada por comas de números que son los parámetros de las fórmulas de la guía que definen la ruta de acceso de la forma. Se pueden omitir los valores para permitir el uso de los valores predeterminados. Puede haber hasta 8 valores de ajuste.                                                                                                   |
| Alt          | String. Texto alternativo asociado con la forma. Se usa para la exploración no gráfica.                                                                                                                                                                                                                                                                                                 |
| Botón       | [VgTriState](msdn-online-vml-vgtristate.md). Muestra el comportamiento del botón al hacer clic.                                                                                                                                                                                                                                                                                                 |
| BWMode       | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Determina cómo se representará la forma en la vista de blanco y negro en las aplicaciones o cuando se imprima en impresoras en blanco y negro. Los valores incluyen: **color**, **auto**, **escala de grises**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undrawan**. Valor predeterminado: **auto**. |
| BWNormal     | VgBlackWhiteMode. Cuando BWMode es auto, se consulta a esta propiedad cómo representar la forma en blanco y negro normales. Los valores incluyen: **color**, **auto**, **escala de grises**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undrawan**. Valor predeterminado: **auto**.                                                |
| BWPure       | VgBlackWhiteMode. Cuando BWMode es auto, se consulta a esta propiedad cómo representar la forma en B/W puro. Los valores incluyen: **color**, **auto**, **escala de grises**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undrawan**. Valor predeterminado: **auto**.                                                              |
| ChildShapes  | IVgGroupShapes. Colección de otras formas de este grupo. Esta colección admite los métodos de longitud y elemento estándar.                                                                                                                                                                                                                                                       |
| Chromakey    | [IVgColor](msdn-online-vml-ivgcolor.md). Un valor de color que será transparente y mostrará todo lo que hay detrás de la forma.                                                                                                                                                                                                                                                             |
| Control1     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto de control de la curva.                                                                                                                                                                                                                                                                                                  |
| Control2     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto de control de la curva.                                                                                                                                                                                                                                                                                                  |
| CoordOrigin  | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Coordenadas en la esquina superior izquierda del rectángulo del contenedor. Oscila entre 0 y infinito.                                                                                                                                                                                                                               |
| CoordSize    | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Ancho y alto del espacio de coordenadas dentro del rectángulo de referencia de esta forma. Si no se especifica, es el mismo que el ancho y el alto del rectángulo. Oscila entre 0 y infinito. Valor predeterminado: "1000, 1000".                                                                                               |
| Inpendientes     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Ángulo final de la forma.                                                                                                                                                                                                                                                                                          |
| Trusión    | IVgExtrusion. Especifica el valor del objeto de extrusión para esta forma. Vea el elemento [extrusión](msdn-online-vml-extrusion-element.md) para obtener más información.                                                                                                                                                                                                                               |
| Fill         | VgFillFormat. Especifica el valor de relleno para esta forma. Vea el elemento [Fill](msdn-online-vml-fill-element.md) para obtener más detalles.                                                                                                                                                                                                                                                |
| Relleno    | [IVgColor](msdn-online-vml-ivgcolor.md). Color principal del pincel que se va a usar para rellenar la ruta de acceso de esta forma.                                                                                                                                                                                                                                                                  |
| Has       | [VgTriState](msdn-online-vml-vgtristate.md). Si es true, se rellenará la ruta de acceso que define la forma. De forma predeterminada, se rellenará con un color sólido a menos que haya un subelemento Fill que especifique propiedades de relleno más complejas. Si es false, el relleno es transparente.                                                                                                           |
| Voltear         | VgFlipOrientation. Los valores son: X Y XY YX                                                                                                                                                                                                                                                                                                                                         |
| ForceDash    | [VgTriState](msdn-online-vml-vgtristate.md). Indica que se debe representar un contorno discontinuo cuando no haya ninguna línea y sin relleno para una forma. Este comportamiento suele ser útil para hacer que las formas invisibles estén visibles en la edición de aplicaciones para que se puedan seleccionar y gestionar, como en un mapa de imágenes.                                                                 |
| Fórmulas     | IVgFormulas. Matriz de fórmulas que define una forma.                                                                                                                                                                                                                                                                                                                          |
| From         | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto inicial de la línea.                                                                                                                                                                                                                                                                                                   |
| Referencia         | [Cadena](#data-types-used-in-the-vml-object-model). Dirección URL a la que se va a saltar si se hace clic en esta forma.                                                                                                                                                                                                                                                                                 |
| ImageData    | IVgImageData. Información de imagen si la forma es una imagen. Vea el elemento ImageData para obtener más información.                                                                                                                                                                                                                                                                       |
| OnEd         | [VgTriState](msdn-online-vml-vgtristate.md). Oculta todos los identificadores excepto la parte superior izquierda e inferior derecha, como en los controladores de un segmento de línea recta.                                                                                                                                                                                                                             |
| Opacidad      | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Opacidad de la forma completa. Un número entre 0,0 y 1,0.                                                                                                                                                                                                                                                           |
| Ruta         | IVgPath. Cadena que contiene los comandos que definen la ruta de acceso.                                                                                                                                                                                                                                                                                                                  |
| Puntos       | [IVgPoints](msdn-online-vml-ivgpoints-data-type.md). Colección de puntos que definen una forma.                                                                                                                                                                                                                                                                                   |
| Impresión        | [VgTriState](msdn-online-vml-vgtristate.md). Si es true, esta forma está pensada para imprimirse.                                                                                                                                                                                                                                                                                        |
| Rotación     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Establece la rotación de la forma. El valor se propaga al estilo de la forma.                                                                                                                                                                                                                                              |
| Escala        | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Escala de la forma.                                                                                                                                                                                                                                                                                                           |
| Shadow       | IVgShadow. Especifica la sombra para esta forma. Vea el elemento [Shadow](msdn-online-vml-shadow-element.md) para obtener más información.                                                                                                                                                                                                                                                        |
| Corta          | Reservado.                                                                                                                                                                                                                                                                                                                                                                        |
| StartAngle   | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Ángulo inicial de la forma.                                                                                                                                                                                                                                                                                        |
| Carrera       | VgStrokeFormat. Vea Stroke (elemento) para obtener más información.                                                                                                                                                                                                                                                                                                                                  |
| StrokeColor  | [IVgColor](msdn-online-vml-ivgcolor.md). Color principal del pincel que se va a usar para trazar la ruta de acceso de esta forma.                                                                                                                                                                                                                                                                |
| Traza      | [VgTriState](msdn-online-vml-vgtristate.md). Si es true, se trazará la ruta de acceso que define la forma.                                                                                                                                                                                                                                                                              |
| StrokeWeight | [VGLength](msdn-online-vml-vglength.md). Ancho del pincel que se va a usar para trazar la ruta de acceso. Oscila entre 0 y 1584.                                                                                                                                                                                                                                                           |
| TextPath     | IVgTextPath. Especifica el objeto TextPath de la forma. Vea el elemento [TextPath](msdn-online-vml-textpath-element.md) para obtener más información.                                                                                                                                                                                                                                  |
| En           | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto final de la línea.                                                                                                                                                                                                                                                                                                        |
| Tipo         | String. Tipo de forma.                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a>Subelementos del elemento de forma

Los siguientes subelementos forman parte del modelo de objetos de VML.

-   [Información preliminar](#background-element)
-   [Trusión](#extrusion-element)
-   [Fill](#fill-element)
-   [Grupo](#group-element)
-   [Imagedata](#imagedata-element)
-   [Ruta de acceso](#path-element)
-   [Shadow](#shadow-element)
-   [Sesgar](#skew-element)
-   [Stroke](#stroke-element)
-   [TextPath](#textpath-element)

### <a name="background-element"></a>Background (elemento)

Describe el relleno del fondo de una página mediante los rellenos de VML.

**Atributos**



|           |                                                                                                                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BWMode    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Determina cómo se representará la forma en la vista de blanco y negro en las aplicaciones o cuando se imprima.                                     |
| BWNormal  | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Cuando BWMode es auto, se consulta a esta propiedad cómo representar la forma en blanco y negro normales.                        |
| BWPure    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Cuando BWMode es auto, se consulta a esta propiedad cómo representar la forma en blanco y negro puros.                          |
| Fill      | VgFillFormat. Especifica el relleno para esta forma. Vea [Fill](msdn-online-vml-fill-element.md) (elemento) para obtener más información.                                                             |
| Relleno | [IVgColor](msdn-online-vml-ivgcolor.md). Color principal del pincel que se va a usar para rellenar la ruta de acceso de esta forma. Duplicado del valor de color en el elemento Fill. El valor predeterminado es blanco. |



 

### <a name="extrusion-element"></a>Elemento extrusión

Describe una extrusión 3D de la forma.

**Atributos**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>AutoRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Si es true, el centro de rotación del grupo de objetos 3D (de hecho, solo hay un objeto en el grupo) se determina automáticamente como el centro del grupo; de lo contrario, viene determinado por los parámetros RotationCenter, que son una fracción de la forma con 0, 0, 0, que es el centro.</td>
</tr>
<tr class="even">
<td>Nivel de detalle</td>
<td><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>. Cantidad de extrusión hacia atrás. Oscila entre 0 y 32767.</td>
</tr>
<tr class="odd">
<td>Luminosidad</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Brillo general de la escena. El valor predeterminado es &quot; 20.000 &quot; .</td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Color de la extrusión. Solo se usa si ColorMode es personalizado. De lo contrario, establece automáticamente el color del efecto de extrusión en el mismo que el FillColor.</td>
</tr>
<tr class="odd">
<td>Property</td>
<td>Vg3DColorMode. Los valores son:
<ul>
<li>Auto (predeterminado)</li>
<li>Personalizados</li>
</ul></td>
</tr>
<tr class="even">
<td>Difusión</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. La relación entre el incidente y el reflejo difuso. Los valores inferiores a 1,0 son normales, pero los valores superiores a uno pueden generar efectos interesantes.</td>
</tr>
<tr class="odd">
<td>Edge</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Establece el tamaño de un borde biselado redondeado simulado. Oscila entre 0 y 32767 en el punto flotante pts. El valor predeterminado es &quot; 1PT. &quot; .</td>
</tr>
<tr class="even">
<td>Faceta</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Establece la faceta de la escena. El valor predeterminado es &quot; 30.000 &quot; .</td>
</tr>
<tr class="odd">
<td>ForeDepth</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Cantidad de extrusión hacia delante. Oscila entre 0 y 32767.</td>
</tr>
<tr class="even">
<td>LightFace</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Determimes si la cara frontal del objeto responderá a los cambios en la iluminación 3D, por ejemplo, cuando un objeto se rote.</td>
</tr>
<tr class="odd">
<td>LightHarsh</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Iluminación severa para la fuente de luz principal. El valor predeterminado es False.</td>
</tr>
<tr class="even">
<td>LightHarsh2</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Iluminación severa para la fuente de luz secundaria. El valor predeterminado es False.</td>
</tr>
<tr class="odd">
<td>LightLevel</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensidad de la fuente de luz principal. El valor predeterminado es &quot; 38000 &quot; .</td>
</tr>
<tr class="even">
<td>LightLevel2</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensidad de la fuente de luz secundaria. El valor predeterminado es &quot; 38000 &quot; .</td>
</tr>
<tr class="odd">
<td>LightPosition</td>
<td>Vector3D. Posición de la fuente de luz primaria. El valor predeterminado es &quot; 50000, 0, 10000 &quot; .</td>
</tr>
<tr class="even">
<td>LightPosition2</td>
<td>Vector3D. Posición de la fuente de luz secundaria. El valor predeterminado es &quot; -50000, 0, 10000 &quot; .</td>
</tr>
<tr class="odd">
<td>LockRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. &quot;Lockrotationcenter &quot; significa que el giro del grupo se define para que sea por el ángulo de rotación [1] grados sobre el eje y en la Página seguido de un ángulo de rotación [0] grados sobre el eje x. Cuando LockRotationCenter es false, el giro se define como por grados de ángulo de orientación sobre el vector definido por orientación. Por lo tanto, por ejemplo, lockrotationcenter = false orientationangle = 45 Orientation = (0, 1, 0) es equivalente a lockrotationcenter = true RotationAngle = (0, 45).</td>
</tr>
<tr class="even">
<td>Metal</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Hace que la luz reflejada especular sea el color del material en lugar del color de la fuente de luz, lo que hace que el objeto parezca más metálico.</td>
</tr>
<tr class="odd">
<td>Activado</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Activa y desactiva la presentación del efecto de extrusión.</td>
</tr>
<tr class="even">
<td>Orientación</td>
<td>Vector3D. Orientación de la cámara.</td>
</tr>
<tr class="odd">
<td>OrientationAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Ángulo entre la orientación de la cámara y el plano XY.</td>
</tr>
<tr class="even">
<td>Plano</td>
<td>Vg3DExtrudePlane. Permite la extrusión de los planos ortogonales al plano de pantalla. Requiere que se especifiquen ForeDepth y postdepth en las unidades de dibujo en lugar de en emus. Los valores son:
<ul>
<li>XY</li>
<li>ZX</li>
<li>YZ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Representación</td>
<td>Vg3DRenderMode. Los valores son:
<ul>
<li>Solid (predeterminado)</li>
<li>Estructura</li>
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
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Determina cómo se concentra o propaga la reflexión especular. Un valor alto sería de 8 a 10 y se aproximaría a un reflejo, y un valor bajo sería de 2 a 3 y se aproximaría la ropa de sequined. Se recomiendan los valores 3 a 7. Los valores altos reflejarán los orígenes de luz del Pinpoint.</td>
</tr>
<tr class="odd">
<td>SkewAmt</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>. Si el tipo es Parallel, el atributo determina la cantidad de sesgo. Oscila entre 0 y 100.</td>
</tr>
<tr class="even">
<td>SkewAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Si el tipo es Parallel, el atributo determina el grado de sesgo. El valor predeterminado es &quot; -45 &quot; .</td>
</tr>
<tr class="odd">
<td>Especulación</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. La relación del incidente con la luz reflejada especular. Los valores inferiores a 1,0 son normales, pero los valores superiores a uno pueden generar efectos interesantes.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>VgExtrusionType. Los valores son:
<ul>
<li>Parallel (valor predeterminado)</li>
<li>Perspectiva</li>
</ul></td>
</tr>
<tr class="odd">
<td>Cuánto</td>
<td>Vector3D. El punto desde el que se está viendo la escena.</td>
</tr>
<tr class="even">
<td>ViewpointOrigin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Puede tener valores de 0,5 a-0,5 para colocar el origen del punto de vista en el cuadro de límite de la forma.</td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a>Elemento Fill

Describe cómo se debe rellenar una ruta de acceso para los rellenos más complejos que un color sólido.

**Atributos**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>AlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Alinee la imagen con la forma. Si es false, alinea la imagen con la ventana.</td>
</tr>
<tr class="even">
<td>Ángulo</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. El ángulo a lo largo del que se dirige el degradado. 0 grados está a lo largo del eje horizontal de izquierda a derecha.</td>
</tr>
<tr class="odd">
<td>Aspecto</td>
<td><strong>VgAspectType</strong>. El atributo ImageSize se ajustará para conservar el aspecto de la imagen. Estos valores incluyen:
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignorar</td>
<td>Omitir problemas de aspecto.</td>
</tr>
<tr class="even">
<td>Al menos</td>
<td>La imagen es al menos tan grande como el tamaño de la imagen.</td>
</tr>
<tr class="odd">
<td>AtMos</td>
<td>La imagen no es mayor que el tamaño de la imagen.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Color de relleno principal. Igual que el atributo FillColor de Shape.</td>
</tr>
<tr class="odd">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Color secundario de un relleno cuando el tipo de imagen es el patrón o un relleno de degradado.</td>
</tr>
<tr class="even">
<td>Colores</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>. Colores intermedios del degradado y sus posiciones relativas a lo largo del degradado; por ejemplo, &quot; 30% rojo, 70% azul, 90% verde &quot; . El color principal (atributo de color de la forma) es 0% y el color secundario (atributo color2) es 100%.</td>
</tr>
<tr class="odd">
<td>Foco</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>. Punto focal del relleno de degradado lineal. Los valores van de-100 a + 100.</td>
</tr>
<tr class="even">
<td>FocusPosition</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Posición del rectángulo más interior de los degradados radiales. El vector es una fracción (0,0-1,0) del ancho y el alto de la forma.</td>
</tr>
<tr class="odd">
<td>FocusSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Tamaño del rectángulo más interno de los degradados radiales. El vector es una fracción (de 0,0 a 1,0) del ancho y el alto de la forma.</td>
</tr>
<tr class="even">
<td>Método</td>
<td>VgSigmaType. Estos valores incluyen:
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
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Activa la presentación de relleno. Igual que el atributo Fill de la forma.</td>
</tr>
<tr class="even">
<td>Opacidad</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacidad del relleno.</td>
</tr>
<tr class="odd">
<td>Opacity2</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. La opacidad secundaria de los degradados.</td>
</tr>
<tr class="even">
<td>Origen</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Punto relativo a la esquina superior izquierda de la imagen que se trata como el origen de la imagen. El valor predeterminado es el centro de la imagen. El vector es una fracción (de 0,0 a 1,0) del ancho y el alto de la imagen.</td>
</tr>
<tr class="odd">
<td>Posición</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Señale el rectángulo de referencia de la forma para colocar el origen de la imagen. El valor predeterminado es el centro del rectángulo del contenedor. El vector es una fracción (0,0-1,0) del ancho y el alto de la imagen.</td>
</tr>
<tr class="even">
<td>Tamaño</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Tamaño de la imagen. El valor predeterminado es el tamaño en píxeles de la imagen. Se puede especificar en coordenadas absolutas o en porcentaje.</td>
</tr>
<tr class="odd">
<td>Origen</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadena</a>. Dirección URL de una imagen que se va a cargar para los rellenos de imagen y de patrón. Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>VgFillType. Puede ser uno de los siguientes tipos:
<ul>
<li>Información previa</li>
<li>Fotograma</li>
<li>Degradado</li>
<li>GradientCenter</li>
<li>GradientRadial</li>
<li>GradientTitle</li>
<li>GradientUnscaled</li>
<li>Patrón</li>
<li>Sólido</li>
<li>Tile</li>
</ul>
Mosaico, patrón y marco requieren que se proporcionen los atributos de la imagen. Gradiente y GradientRadial requieren que se proporcionen los atributos de degradado.</td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a>Group, elemento

Un grupo es una colección de formas individuales que se pueden colocar y transformar como una unidad.



|        |                                                                                              |
|--------|----------------------------------------------------------------------------------------------|
| Elemento   | [IVgShape](#data-types-used-in-the-vml-object-model). Elemento especificado en la matriz de formas. |
| Length | [Entero](#data-types-used-in-the-vml-object-model). Número de formas de este grupo.         |



 

### <a name="imagedata-element"></a>Elemento ImageData

Describe una imagen que se va a representar en la parte superior de una forma.



|             |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Suavizado     | [VgTriState](msdn-online-vml-vgtristate.md). Mostrar imagen en solo dos colores (normalmente blanco y negro).                                                                                                                                                                                                                                                     |
| BlackLevel  | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Permite ajustar para establecer el nivel de modo que los negros aparezcan como verdaderos negros, y todos los demás colores estén visibles como sombras por encima del negro.                                                                                                                                                                        |
| Chromakey   | [IVgColor](msdn-online-vml-ivgcolor.md). Color transparente de la imagen.                                                                                                                                                                                                                                                                                         |
| CropBottom  | [VgNumber](#data-types-used-in-the-vml-object-model). Recortar la distancia desde la parte inferior de la imagen expresada como un porcentaje del tamaño de la imagen.                                                                                                                                                                                                                           |
| CropLeft    | [VgNumber](#data-types-used-in-the-vml-object-model). Recortar la distancia desde el borde izquierdo de la imagen expresado como una fracción del tamaño de la imagen (de 0,0 a 1,0). Sin embargo, se admite "out-recortar" y, por tanto, se admiten los valores menores que 0 y mayores que 1; por ejemplo,-5, 20 recortarían los límites 25X el tamaño de la imagen con 4/5 en un lado de la imagen. |
| CropRight   | [VgNumber](#data-types-used-in-the-vml-object-model). Recortar la distancia a la derecha de la imagen expresada como un porcentaje del tamaño de la imagen.                                                                                                                                                                                                                            |
| CropTop     | [VgNumber](#data-types-used-in-the-vml-object-model). Recortar la distancia desde la parte superior de la imagen expresada como un porcentaje del tamaño de la imagen.                                                                                                                                                                                                                              |
| EmbossColor | [IVgColor](msdn-online-vml-ivgcolor.md). Se establece en un porcentaje del color de la sombra para crear un efecto de imagen en relieve.                                                                                                                                                                                                                                 |
| Beneficios        | [VgPositiveNumber](#data-types-used-in-the-vml-object-model). Ajusta la intensidad de todos los colores. En esencia, establece cómo será el blanco brillante. Oscila entre 0 y 32767.                                                                                                                                                                                           |
| Gamma       | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Corrección gamma. Al aumentarlo, se obtiene una imagen más contrastada.                                                                                                                                                                                                                                           |
| GrayScale   | [VgTriState](msdn-online-vml-vgtristate.md). Mostrar imagen en colores de escala de grises.                                                                                                                                                                                                                                                                              |
| Origen         | [Cadena](#data-types-used-in-the-vml-object-model). Dirección URL de una imagen que se va a cargar para los rellenos de imagen y de patrón. Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.                                                                                                                                                           |



 

### <a name="path-element"></a>Path, elemento

Define la ruta de acceso que conforma la forma usando una cadena que contiene un conjunto completo de comandos de "movimiento del lápiz".



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Limo</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>. Define el punto en el que se estira la forma; por ejemplo, en el caso de una forma Giraffe, el punto limo sería el cuello, por lo que cuando se cambia el tamaño de la forma, el cuello se estira y el resto de la forma mantendrá sus dimensiones.</td>
</tr>
<tr class="even">
<td>TextBoxRect</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>. Matriz que contiene los rectángulos que definen dónde debe ir el texto.</td>
</tr>
<tr class="odd">
<td>V</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadena</a>. Coincide con el atributo v de la etiqueta path. Tenga en cuenta que la ruta de acceso puede corresponder al atributo o elemento de ruta de acceso.</td>
</tr>
<tr class="even">
<td>Value</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadena</a>. Representación de texto de los comandos que definen la ruta de acceso. Los valores de la coordenada X o y pueden ser una referencia a una fórmula en el formulario &quot; @# &quot; donde # es el número ordinal de la fórmula, por ejemplo, &quot; @2 &quot; . Esta cadena de atributo se compone de un amplio conjunto de comandos, entre los que se incluyen los siguientes: <br/> 
<table>
<thead>
<tr class="header">
<th>Get-Help</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AE (angleellipseto)</td>
<td><strong>Center</strong>(x, y) <strong>tamaño</strong>(w, h) <strong>ángulo inicial</strong>, <strong>ángulo final</strong><br/> Dibuja un segmento de una elipse. Una línea recta se dibuja desde el punto actual hasta el punto inicial del segmento.<br/></td>
</tr>
<tr class="even">
<td>al (angleelipse)</td>
<td>Igual que AE, salvo que hay una m implícita al punto inicial del segmento.</td>
</tr>
<tr class="odd">
<td>ar (arco)</td>
<td>Igual que en. Sin embargo, un nuevo subtrazado lo inicia un m implícito en el punto inicial del arco.</td>
</tr>
<tr class="even">
<td>a las (ArcTo)</td>
<td><strong>izquierda</strong>, <strong>superior</strong>, <strong>derecha</strong>, <strong>inferior</strong>, <strong>Inicio</strong>(x, y) <strong>final</strong>(x, y) <br/> Los primeros cuatro valores definen el rectángulo de selección de una elipse. Los cuatro últimos definen dos vectores radiales. Se dibuja un segmento de la elipse que comienza en el ángulo definido por el vector de radio de inicio y termina en el ángulo definido por el vector final. Una línea recta se dibuja desde el punto actual hasta el principio del arco. El arco siempre se dibuja en sentido contrario a las agujas del reloj. <br/></td>
</tr>
<tr class="odd">
<td>c (curvato)</td>
<td><strong>Control1</strong>(x, y) <strong>control2</strong>(x, y) <strong>a</strong>(x, y) <br/> Dibuja una curva Bézier cúbica desde el punto actual a la coordenada proporcionada por los dos parámetros finales, los puntos de control especificados por los cuatro primeros parámetros. El punto actual se convierte en el extremo de la curva.<br/></td>
</tr>
<tr class="even">
<td>e (fin)</td>
<td>Finaliza el conjunto actual de subtrazados. Un conjunto determinado de subrutas (como delimitado por end) se rellenan con eofill. Los conjuntos posteriores de subtrazados se rellenan de forma independiente y se superponen a los existentes.</td>
</tr>
<tr class="odd">
<td>l (lineTo)</td>
<td>x, y<br/> Dibuja una línea del punto actual a la coordenada x, y determinada, que se convierte en el nuevo punto actual. Se pueden especificar pares de coordenadas adicionales para formar una polilínea, por ejemplo, &quot; l 10, 13, 45, 27, 89,-12 &quot; .<br/></td>
</tr>
<tr class="even">
<td>m (moveTo)</td>
<td>x, y<br/> Inicia un nuevo subtrazado en la coordenada x, y dada.<br/></td>
</tr>
<tr class="odd">
<td>NF (noFill)</td>
<td>El conjunto actual de subtrazados (delimitados por end) no se rellenará.</td>
</tr>
<tr class="even">
<td>NS (noStroke)</td>
<td>No se trazará el conjunto actual de subtrazados (delimitados por end).</td>
</tr>
<tr class="odd">
<td>QB (quadraticbezier)</td>
<td>(<strong>ControlPoint</strong>(x, y)) *,<strong>End</strong>(x, y) <br/> Define una o varias curvas Bézier cuadráticas por medio de puntos de control y un punto de conexión. Los puntos intermedios (en curva) se obtienen mediante la interpolación entre los puntos de control sucesivos similares a las fuentes TrueType. No es necesario que el subtrazado sea un inicio, en cuyo caso el subtrazado está cerrado y el último punto define el punto inicial.<br/></td>
</tr>
<tr class="even">
<td>QX (ellipticalquadrantx)</td>
<td><strong>End</strong>(x, y) <br/> Una elipse de cuarto se dibuja desde el punto actual hasta el punto de conexión dado. Inicialmente, el segmento elíptico es tangencial a una línea paralela al eje x; es decir, el segmento comienza horizontalmente.<br/></td>
</tr>
<tr class="odd">
<td>qy (ellipticalquadranty)</td>
<td><strong>End</strong>(x, y) <br/> Igual que QX, salvo que el segmento elíptico es inicialmente tangencial a una línea paralela al eje y; es decir, el segmento comienza verticalmente.<br/></td>
</tr>
<tr class="even">
<td>r (rlineto)</td>
<td>x, y <br/> Dibuja una línea del punto actual a la coordenada relativa (CPX + x, CPY + y). Si se proporcionan pares de coordenadas adicionales, cada punto nuevo se calcula en relación con el último.<br/></td>
</tr>
<tr class="odd">
<td>t (rmoveto)</td>
<td>x, y<br/> Inicia un nuevo subtrazado en las coordenadas relativas (CPX + x, CPY + y) donde CPX, CPY es la posición actual. <br/></td>
</tr>
<tr class="even">
<td>v (curvato)</td>
<td><strong>Control1</strong>(x, y) <strong>control2</strong>(x, y) <strong>a</strong> (x, y) <br/> Curva Bézier cúbica que usa las coordenadas especificadas en relación con el punto actual. Todos los puntos se calculan en relación con el mismo punto inicial.<br/></td>
</tr>
<tr class="odd">
<td>WA (clockwisearcto)</td>
<td>Igual que en, pero el arco se dibuja en sentido de las agujas del reloj.</td>
</tr>
<tr class="even">
<td>WR (clockwisearc)</td>
<td>Igual que ar pero se dibuja en sentido de las agujas del reloj.</td>
</tr>
<tr class="odd">
<td>x (cerrar)</td>
<td>Cerrar el subtrazado actual dibujando una línea recta desde el punto actual hasta el punto de movimiento.</td>
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
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Color de la sombra principal. El valor predeterminado es RGB (128128128)</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Color de la segunda sombra o resaltado en una sombra en relieve o grabado. El valor predeterminado es RGB (203203203).</td>
</tr>
<tr class="odd">
<td>Matrix</td>
<td><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>. Una matriz de transformación de perspectiva con el formato, &quot; SXX, SXY, SYX, SYY, PX, py &quot; [s = Scale, p = Perspective]. Los elementos s especifican cómo se debe escalar la sombra con respecto a la forma y los elementos p especifican cómo debe sesgar la sombra con respecto a la forma. Por ejemplo, la siguiente matriz cambia el tamaño de la forma por un factor de 2 y lo sesga por un factor de 4 en todas las direcciones: <br/> &quot;2, 2, 2, 2, 4, 4&quot;<br/> Esta matriz solo se utiliza si el tipo de la sombra se establece en Perspective.<br/></td>
</tr>
<tr class="even">
<td>Oculta</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. La sombra puede verse a través de si no hay ningún relleno en la forma. El valor predeterminado es False.</td>
</tr>
<tr class="odd">
<td>Offset</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>. Cantidad de desplazamiento x, y de la ubicación de la forma. El valor predeterminado es &quot; 2PT, 2PT &quot; .</td>
</tr>
<tr class="even">
<td>Offset2</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Cantidad de desplazamiento x, y segundo de la ubicación de la forma. Los valores son una medida absoluta o un valor fraccionario de forma (de-0,5 a + 0,5).</td>
</tr>
<tr class="odd">
<td>Activado</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Activa y desactiva la presentación de la sombra.</td>
</tr>
<tr class="even">
<td>Opacidad</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacidad del efecto de sombra.</td>
</tr>
<tr class="odd">
<td>Origen</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Un par de valores fraccionarios de la forma de-0,5 a + 0,5.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>. Los valores son:
<ul>
<li>Single (valor predeterminado)</li>
<li>Doble</li>
<li>Perspectiva</li>
<li>ShapeRelative</li>
<li>DrawingRelative</li>
<li>Emboss</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a>Sesgar elemento

Describe un efecto de sesgo de perspectiva en una forma. El sesgo se aplica a los datos de gráficos vectoriales, no a los datos de imagen.



|        |                                                                                                                                                                                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Matrix | [IVgSkewMatrix](#data-types-used-in-the-vml-object-model). Una matriz de transformación de perspectiva con el formato "SXX, SXY, SYX, SYY, PX, py" \[ s = Scale, p = Perspective \] . Si el desplazamiento está en unidades absolutas, PX, py se encuentran en las unidades de la UEM ^-1. en caso contrario, son una fracción inversa del tamaño de la forma. |
| Offset | [IvgSkewOffset](#data-types-used-in-the-vml-object-model). Cantidad de desplazamiento x, y de la ubicación de la forma. El valor predeterminado es "2PT, 2PT".                                                                                                                                                   |
| Activado     | [VgTriState](msdn-online-vml-vgtristate.md). Activa o desactiva la presentación del sesgo.                                                                                                                                                                                             |
| Origen | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Un par de valores fraccionarios de la forma de-0,5 a + 0,5.                                                                                                                                                                     |



 

### <a name="stroke-element"></a>Elemento stroke

Describe cómo dibujar la ruta de acceso si se desea algo más allá de una línea sólida con un color sólido.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Color de la línea. Igual que el atributo StrokeColor de la forma, pero lo reemplaza.</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Color secundario. Se usa cuando FillType es pattern.</td>
</tr>
<tr class="odd">
<td>DashStyle</td>
<td><strong>VgLineDashStyle</strong>. Formato de estilo de guión. Puede ser un valor específico o una secuencia de números con un patrón de guiones definido por el usuario. Los valores son:
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
<td><strong>VgArrowheadStyle</strong>. Punta de flecha del final de la línea. Los valores son:
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
<td><strong>VgArrowHeadLength</strong>. Longitud de la punta de flecha para el final de la línea. Los valores son:
<ul>
<li>Short</li>
<li>Media (valor predeterminado)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrowWidth</td>
<td><strong>VgArrowheadWidth</strong>. Ancho de la punta de flecha para el final de la línea. Los valores son:
<ul>
<li>Restrictiv</li>
<li>Media (valor predeterminado)</li>
<li>Ancho</li>
</ul></td>
</tr>
<tr class="odd">
<td>EndCap</td>
<td><strong>VgLineEndCapStyle</strong>. Los valores son:
<ul>
<li>Plano</li>
<li>Square</li>
<li>Round</li>
</ul></td>
</tr>
<tr class="even">
<td>FillType</td>
<td><strong>VgLineFillType</strong>. Los valores son:
<ul>
<li>Solid (predeterminado)</li>
<li>Tile</li>
<li>Patrón</li>
<li>Fotograma</li>
</ul></td>
</tr>
<tr class="odd">
<td>ImageAlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Alinee la imagen con la forma. Si es false, alinea la imagen con la ventana.</td>
</tr>
<tr class="even">
<td>ImageAspect</td>
<td><strong>VgAspectType</strong>. El atributo ImageSize se ajustará para conservar el aspecto de la imagen. Estos valores incluyen:
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignorar</td>
<td>Omitir problemas de aspecto.</td>
</tr>
<tr class="even">
<td>Al menos</td>
<td>La imagen es al menos tan grande como el tamaño de la imagen.</td>
</tr>
<tr class="odd">
<td>AtMos</td>
<td>La imagen no es mayor que el tamaño de la imagen.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>ImageSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Tamaño de la imagen con la que se va a formar el pincel. El valor predeterminado es el tamaño de la imagen.</td>
</tr>
<tr class="even">
<td>JoinStyle</td>
<td><strong>VgLineJoinStyle</strong>. Los valores son:
<ul>
<li>Round (Unión redondeada)</li>
<li>Bisel (unión biselada)</li>
<li>Angular (unión angular)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Estilo de línea</td>
<td><strong>VgLineStyle</strong>. Los valores son:
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
<td><a href="msdn-online-vml-vglength.md">Longitud</a>. Distancia máxima entre el punto interno y el punto exterior de una Unión. Este número es un múltiplo del grosor de la línea. Oscila entre 0 y 32.767.</td>
</tr>
<tr class="odd">
<td>Activado</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Activa y desactiva la presentación de la línea. Igual que el atributo stroke de la forma, pero lo reemplaza.</td>
</tr>
<tr class="even">
<td>Opacidad</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacidad del trazo.</td>
</tr>
<tr class="odd">
<td>Origen</td>
<td>String. Dirección URL de una imagen que se va a cargar para los rellenos de imagen y de patrón. Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen.</td>
</tr>
<tr class="even">
<td>StartArrow</td>
<td><strong>VgArrowheadStyle</strong>. Punta de flecha del inicio de la línea. Los valores son:
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
<td>VgArrowHeadLength. Longitud de la punta de flecha para el inicio de la línea. Los valores son:
<ul>
<li>Short</li>
<li>Media (valor predeterminado)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>StartArrowWidth</td>
<td>VgArrowheadWidth. Ancho de la punta de flecha para el inicio de la línea. Los valores son:
<ul>
<li>Ancho medio estrecho (predeterminado)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Peso</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Ancho de línea. Oscila entre 0 y 1584.
<div class="alert">
<blockquote>
[!Note]<br />
El atributo DashStyle permite al usuario especificar un patrón de guiones definido de forma personalizada. Esto se hace mediante una serie de números. Los estilos de guión se definen en términos de la longitud del guión (la parte dibujada del trazo) y la longitud del espacio entre los guiones. Las longitudes son relativas al ancho de línea; una longitud de &quot; 1 &quot; es igual al ancho de línea. El estilo EndCap se aplica a cada guión; los estilos de flecha no lo son. La cadena define primero la longitud del guión y, a continuación, la longitud del espacio. Esto puede repetirse para formar estilos de guiones complejos. La cadena siempre debe contener un par de números; Si contiene un número impar de números, es posible que se descarte la última. En la tabla siguiente se enumeran algunos valores típicos y una descripción del efecto previsto. &quot;0 &quot; implica un punto que debe ser fourfold simétrico (con Endcaps redondeada debe ser un círculo). Si el Endcap de línea es plano, un visor debe elegir un guion del sistema operativo integrado siempre que sea posible (es decir, algo que sea rápido de dibujar). A continuación se muestran algunos ejemplos.
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td>&quot;2 2&quot;</td>
<td>guiones cortos (cada guion y el espacio entre dos es el doble del ancho de la línea)</td>
</tr>
<tr class="even">
<td>&quot;1 2&quot;</td>
<td>punto (cada guión es el ancho de la línea, mientras que cada espacio es dos veces el ancho de la línea)</td>
</tr>
<tr class="odd">
<td>&quot;4 2&quot;</td>
<td>Dash (cada guion es cuatro veces el ancho de la línea, mientras que cada espacio es dos veces el ancho de la línea)</td>
</tr>
<tr class="even">
<td>&quot;8 2&quot;</td>
<td>Guion largo</td>
</tr>
<tr class="odd">
<td>&quot;4 2 1 2&quot;</td>
<td>guión punto</td>
</tr>
<tr class="even">
<td>&quot;8 2 1 2&quot;</td>
<td>guión largo (punto)</td>
</tr>
<tr class="odd">
<td>&quot;8 2 1 2 1 2&quot;</td>
<td>guión largo (punto)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a>Elemento TextPath

Describe una ruta de acceso vectorial basada en los datos de texto, la fuente y los estilos proporcionados. La ruta de acceso de texto se distorsiona para ajustarse a un elemento de **ruta de acceso** si se proporciona.



|          |                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| FitPath  | [VgTriState](msdn-online-vml-vgtristate.md). Ajusta el tamaño del texto para rellenar la ruta en la que se encuentra.                                 |
| FitShape | [VgTriState](msdn-online-vml-vgtristate.md). Estira la ruta de acceso del texto hasta los bordes del cuadro de forma.                      |
| Activado       | [VgTriState](msdn-online-vml-vgtristate.md). Determina si las rutas de acceso de caracteres se muestran o no.                    |
| String   | String. Texto que se va a representar como una ruta de acceso de texto.                                                                                    |
| Trim     | [VgTriState](msdn-online-vml-vgtristate.md). Quita cualquier espacio adicional reservado para ascendentes y descendentes si no se usa. |
| XScale   | [VgTriState](msdn-online-vml-vgtristate.md). Use la medida x recta en lugar de medir a lo largo del trazado.                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a>Tipos de datos utilizados en el modelo de objetos VML

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
-   [IVgSkewMatrix](/windows)
-   [IVgSkewOffset](/windows)
-   [IVgVector2D](/windows)
-   [IVgVector3D](/windows)
-   [Duración](/windows)
-   [Measure](/windows) (Medida)
-   [String](/windows)
-   [VgBlackWhiteMode](/windows)
-   [VgFraction](/windows)
-   [VgTriState](/windows)

**Double (tipo de datos)**

Un entero de precisión doble con un intervalo de-infinito a infinito.

**Tipo de datos Fixed**

Número de punto flotante con un intervalo comprendido entre-32.766,0 y 32.766,0.

**Tipo de datos Integer**

Entero con un intervalo de-infinito a infinito.

**IVgAdjustments, tipo de datos**

Colección de ajustes de una forma que se puede utilizar para cambiar las dimensiones de una forma. Los ajustes se pueden usar como marcadores de posición temporales o, por cualquier motivo, se usarían variables. Solo hay 8 ajustes en la colección.



| Atributos | Descripción                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exists     | [IVgTriState](msdn-online-vml-vgtristate.md). Determina si existe un ajuste especificado. Tenga en cuenta que se debe usar un índice; es decir, exists (Item) se debe usar para recuperar la existencia de un elemento.                                                                                                                                                                   |
| Elemento       | [Largo](#data-types-used-in-the-vml-object-model). Matriz de ajustes indizada de 0 a 7. Tenga en cuenta que los ajustes pueden especificarse de SPARC. es decir, es posible que no siempre se rellenen los valores de matriz intermedios. Por ejemplo, los elementos 1, 3 y 5 podrían tener valores para una longitud de 3, con el elemento (0), el elemento (2) y el elemento (4) especificado. Para ver si existe un elemento, utilice el atributo EXISTS. |
| Length     | [Entero](#data-types-used-in-the-vml-object-model). Número de ajustes. No puede ser mayor que 8.                                                                                                                                                                                                                                                                          |
| Value      | [Cadena](#data-types-used-in-the-vml-object-model). Representación de texto de valores numéricos, con comas entre cada número.                                                                                                                                                                                                                                                    |



 

**IVgColor**

Especifica un color.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td><strong>VgRGBType</strong>. Valor RGB (Long) del color. Solo es válido si el tipo es RGB.</td>
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
<li>Granate (#800000)</li>
<li>Rojo (#FF0000)</li>
<li>Púrpura (#800080)</li>
<li>Fuchsia (#FF00FF)</li>
<li>Verde (#008000)</li>
<li>Lima (#00FF00)</li>
<li>Oliva (#808000)</li>
<li>Amarillo (#FFFF00)</li>
<li>Navy (#000080)</li>
<li>Blue (#0000FF)</li>
<li>Verde azulado (#008080)</li>
<li>Aguamarina (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>VgColorType</strong>. Tipo de color. Uno de los siguientes tipos:
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

Ecuaciones utilizadas para las fórmulas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Operación</td>
<td><strong>VgEquationOperationType</strong> Nombre de la operación que se va a realizar en los parámetros. En una ecuación se pueden usar las siguientes operaciones:
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
<td>Valor absoluto. <br/> <strong>ABS</strong>(v) <br/></td>
</tr>
<tr class="even">
<td>Atan2</td>
<td>Aritmética polar: resultados en unidades FD (grados multiplicado por 65536).<br/> <strong>ATAN2</strong>(P1, v) <br/></td>
</tr>
<tr class="odd">
<td>Cos</td>
<td>Coseno, argumento en unidades FD (grados multiplicado por 65536).<br/> v * <strong>cos</strong>(P1) <br/></td>
</tr>
<tr class="even">
<td>Cosatan2</td>
<td>Conserva la precisión completa en el cálculo intermedio.<br/> v * <strong>cos (ATAN2 (</strong> P2, P1 <strong>))</strong><br/></td>
</tr>
<tr class="odd">
<td>Elipse</td>
<td>Elipse</td>
</tr>
<tr class="even">
<td>Si</td>
<td>Condición if test. v > 0 <strong>?</strong> P1: P2</td>
</tr>
<tr class="odd">
<td>Máx.</td>
<td>El mayor de dos valores. <br/> <strong>máx</strong>. (v, P1) <br/></td>
</tr>
<tr class="even">
<td>Mid</td>
<td>Promedio (v + P1)/2</td>
</tr>
<tr class="odd">
<td>Min</td>
<td>El menor de dos valores. <strong>mín</strong>. (v, P1)</td>
</tr>
<tr class="even">
<td>Mod</td>
<td>Valor absoluto.</td>
</tr>
<tr class="odd">
<td>Producto</td>
<td>Se utiliza para la multiplicación y la división. v * P1/P2</td>
</tr>
<tr class="even">
<td>Sin</td>
<td>Seno, argumento en unidades FD (grados multiplicado por 65536). <br/> v * <strong>sin</strong>(P1) <br/></td>
</tr>
<tr class="odd">
<td>Sinatan2</td>
<td>Conserva la precisión completa en el cálculo intermedio. v * <strong>sin</strong>(<strong>ATAN2</strong>(P2, P1))</td>
</tr>
<tr class="even">
<td>Sqrt</td>
<td>El resultado es positivo y se redondea hacia abajo. <br/> <strong>sqrt</strong>(v) <br/></td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>Se utiliza para sumar y restar.<br/> v + P1 P2<br/></td>
</tr>
<tr class="even">
<td>Sumangle</td>
<td>Ángulo existente (escalado por 65536), donde P1 y P2 están en grados.<br/> v + P1 * 65536 + P2 * 65536<br/></td>
</tr>
<tr class="odd">
<td>Tan</td>
<td>Tangente, el argumento está en unidades FD (grados multiplicado por 65536). <br/> v * tan (P1)<br/></td>
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
<td>Parámetro1</td>
<td><strong>Entero</strong>. El primer parámetro.</td>
</tr>
<tr class="odd">
<td>Paramtype1</td>
<td><strong>VgFormulaParamType</strong>. Tipo del primer parámetro. Se admiten los valores siguientes:
<table>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Value</td>
<td>El parámetro es un valor simple.</td>
</tr>
<tr class="even">
<td>AdjustmentReference</td>
<td>Parámetro es una referencia a un ajuste. Por ejemplo, si el primer parámetro es 1, se utilizará el valor del primer ajuste.</td>
</tr>
<tr class="odd">
<td>FormulaReference</td>
<td>Es el resultado de una referencia al resultado de una fórmula anterior. Por ejemplo, si el primer parámetro es 2, se usará el resultado de la fórmula 2.</td>
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
<td><strong>VgFormulaParamType</strong> Tipo del parámetro 2.</td>
</tr>
<tr class="even">
<td>Val</td>
<td><strong>Entero</strong>. Resultado.</td>
</tr>
<tr class="odd">
<td>Valtype2</td>
<td><strong>VgFormulaParamType</strong>. Tipo del resultado.</td>
</tr>
</tbody>
</table>



 

**IVgFixedRectangle**

Especifica un rectángulo fijo.



| Atributos | Descripción                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Value      | [Cadena](#data-types-used-in-the-vml-object-model). Valor de texto que especifica la ruta de acceso.         |
| Left       | [Double](#data-types-used-in-the-vml-object-model). Coordenada izquierda del rectángulo.   |
| Superior        | [Double](#data-types-used-in-the-vml-object-model). Coordenada superior del rectángulo.    |
| Right      | [Double](#data-types-used-in-the-vml-object-model). Coordenada derecha del rectángulo.  |
| Bottom     | [Double](#data-types-used-in-the-vml-object-model). Coordenada inferior del rectángulo. |



 

**IVgFixedRectangleArray**

Matriz de rectángulos fijos.



| Atributos | Descripción                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| Value      | [Cadena](#data-types-used-in-the-vml-object-model). Representación de texto de la matriz.                           |
| Length     | [Entero](#data-types-used-in-the-vml-object-model). Número de rectángulos en esta matriz.                    |
| Elemento       | [IVgFixedRectangle](#data-types-used-in-the-vml-object-model). Objeto de rectángulo en el índice especificado. |



 

**IVgFormula** , tipo de datos

Definiciones de fórmulas que pueden variar la ruta de acceso de una forma o que se pueden usar para otros fines de cálculo. Las fórmulas se pueden basar en el atributo **ADJ** de una forma, que puede cambiar. Las fórmulas también pueden hacer referencia a otras fórmulas.



| Atributos | Descripción                                                                                                                                                                                                                                                                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eqn        | [IVgEquation](#data-types-used-in-the-vml-object-model). Cada fórmula define un valor único como el resultado de la evaluación de la expresión. Este atributo define la expresión y tiene la forma general de una operación seguida de hasta tres argumentos, que pueden ser valores de ajuste (por ejemplo, \# 2), los resultados de las fórmulas anteriores (por ejemplo, @2 ), números fijos o valores predefinidos. |



 

**IVgFormulas, tipo de datos**

Colección de objetos de fórmula.



| Atributos | Descripción                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Length     | [Entero](#data-types-used-in-the-vml-object-model). Número de objetos de fórmula en la colección.                                                |
| Elemento       | [IVgFormula](#data-types-used-in-the-vml-object-model). Una fórmula específica. Tenga en cuenta que la matriz de fórmulas puede ser heredada pantalla el tipo de forma. |



 

**IVgGradientColorArray**

Matriz de colores que definen un degradado (rango de colores mezclado).



| Atributos | Descripción                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| Value      | [Cadena](#data-types-used-in-the-vml-object-model). Especifica la matriz de colores; por ejemplo, "red. 2; verde. 4; negro. 7 " |
| Length     | [Entero](#data-types-used-in-the-vml-object-model). Número de colores de la matriz.                                          |



 



| Métodos     | Descripción                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddColor    | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Agrega un nuevo color en el extremo especificado por fracción. El nuevo color es blanco de forma predeterminada y es el valor devuelto. Después, se puede cambiar el color por referencia. |
| RemoveColor | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Quita un color en el extremo especificado por fracción. Nota: Si 0,0 o 1,0 no existe, es implícito y se usa el color blanco en ese punto.          |



 

**Tipo de IVgPoints**

Matriz de puntos que definen una forma.



| Atributos | Descripción                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Value      | [Cadena](#data-types-used-in-the-vml-object-model). Representación de texto de la matriz.           |
| Length     | [Entero](#data-types-used-in-the-vml-object-model). Número de puntos de esta matriz.        |
| Elemento       | [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto en el índice especificado. |



 

**Tipo de IVgSkewMatrix**

Matriz que se usa para sesgar formas, una matriz de transformación de perspectiva con el formato "*SXX, SXY, SYX, SYY, PX, py* " \[ *s* = Scale, *p* = Perspective \] . Si el desplazamiento está en unidades absolutas, *PX, py* se encuentran en unidades de la UEM ^-1. en caso contrario, son una fracción inversa del tamaño de la forma.



| Atributos   | Descripción                                         |
|--------------|-----------------------------------------------------|
| XtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| XtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| PerspectiveX | [Double](#data-types-used-in-the-vml-object-model). |
| Perspectiva | [Double](#data-types-used-in-the-vml-object-model). |



 

**IVgSkewOffset**

Especifica el desplazamiento del sesgo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Value</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadena</a>. Representación de texto de desplazamiento.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente X. Porcentaje o medida. Si no hay unidades, el tipo ShapeRelative es implícito; de lo contrario, el tipo absoluto es implícito.</td>
</tr>
<tr class="odd">
<td>Y</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Y.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>VgSkewTransformType</strong>. Especifica el tipo de transformación. Los valores válidos son los puntos enteros comprendidos entre-Infinity y Infinity. 
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
<td>Los valores de desplazamiento son porcentajes (proporciones) del tamaño de la forma original; por ejemplo, un valor de 0,5 significa una desfase de la mitad del tamaño de la forma.</td>
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



 

**IVgVector2D, tipo de datos**

Especifica un vector bidimensional que consta de dos números **Double** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Value</td>
<td><strong>Cadena</strong>. Representación de texto de ambos números vectoriales separados por un espacio.</td>
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
<td>Tipo</td>
<td><strong>VgVectorType</strong>. Unidades previstas para este vector. Los valores son:
<ul>
<li>Medida</li>
<li>Length</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>Número entero de porcentaje</li>
</ul></td>
</tr>
</tbody>
</table>



 

**IVgVector3D, tipo de datos**

Especifica un vector tridimensional que consta de tres números **dobles** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Value</td>
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
<td><strong>VgVectorType</strong>. Unidades previstas para este vector. Los valores son:
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



 

**Tipo de datos de longitud**

Número de punto flotante con un intervalo comprendido entre 0 y infinito.

**Tipo de datos Measure**

Un número de punto flotante desde-Infinity hasta el infinito.

**String (tipo de datos)**

Datos de caracteres de cualquier longitud.

**VgBlackWhiteMode**

Modo de representación de blanco y negro. Los valores posibles son:

-   **Color**
-   **Automático**
-   **Aclarar**
-   **LightGrayScale**
-   **InverseGray**
-   **GrayOutline**
-   **BlackTextAndLines**
-   **HighContrast**
-   **Negro**
-   **Blanco**
-   **No dibujado**

**VgFraction, tipo de datos**

Número de punto flotante con un intervalo de 0,0 a 1,0. Las fracciones también se pueden especificar como un porcentaje; por ejemplo, "50%".

**Tipo de VgTriState**

Enumeración utilizada para los valores que pueden ser de uno de estos tres Estados:

-   **TRUE**
-   **FALSE**
-   **COMBINACIÓN**