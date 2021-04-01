---
title: Fuentes variables OpenType
description: En este tema se describen las fuentes de variables OpenType, su compatibilidad en DirectWrite y Direct2D, y cómo usarlas en la aplicación. .
ms.assetid: 788558a7-efe7-b075-942f-ac75a5b86b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a9e6bdf27da0d70841973515636736859294dd
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "103913966"
---
# <a name="opentype-variable-fonts"></a>Fuentes variables OpenType

En este tema se describen las fuentes de variables OpenType, su compatibilidad en DirectWrite y Direct2D, y cómo usarlas en la aplicación. 

-   [¿Qué son las fuentes de variables OpenType?](#what-are-opentype-variable-fonts)
-   [Compatibilidad con fuentes variables OpenType en DirectWrite](#opentype-variable-font-support-in-directwrite)
-   [Usar fuentes de variables OpenType](#using-opentype-variable-fonts)

## <a name="what-are-opentype-variable-fonts"></a>¿Qué son las fuentes de variables OpenType?

La versión 1,8 de la [especificación de formato de fuente OpenType](https://www.microsoft.com/typography/otspec/) presentó una nueva extensión al formato conocido como [variaciones de fuentes OpenType](/typography/opentype/spec/otvaroverview). Las fuentes que usan estas extensiones se conocen como fuentes de variables OpenType. Una fuente de variable OpenType es una fuente única que puede comportarse como varias fuentes mediante la interpolación continua entre distintos diseños, todos definidos dentro de la misma fuente.

Una fuente de variable OpenType puede definir la variación continua de su diseño a lo largo de uno o más ejes independientes, como el peso o el ancho: 

 

![Muestra una fuente de variable OpenType que usa la letra ' G ' y muestra distintas variaciones a lo largo de un eje de ancho horizontal y un eje de peso vertical.](images/opentype-width-weight.png)

Un desarrollador de fuentes determina un conjunto de ejes de variación para usar en una fuente determinada. Estos ejes pueden incluir un conjunto de ejes conocidos (o "registrados") de variación, como peso y ancho, pero también pueden incluir ejes arbitrarios personalizados de variación definidos por el desarrollador de fuentes.  

Al seleccionar un conjunto de ejes de variación para una fuente, el desarrollador de fuentes define un espacio abstracto y n de la variación de diseño para la fuente. Los motores de texto pueden especificar potencialmente cualquier posición, o "instancia", dentro de ese espacio continuo para diseñar y representar el texto. 

El desarrollador de fuentes también puede seleccionar y asignar nombres a determinadas instancias en el espacio de variación del diseño; Estos se conocen como "instancias con nombre". Por ejemplo, una fuente con una variación de peso puede admitir una variación continua entre trazos muy claros y muy gruesos, mientras que el desarrollador de fuentes ha seleccionado pesos determinados junto con el continuum y los nombres asignados, como "Light", "regular" y "Semibold". 

El formato de fuente OpenType variable usa tablas de datos que se encuentran en fuentes OpenType tradicionales, además de algunas tablas adicionales que describen cómo cambian los valores de varios elementos de datos para las distintas instancias. El formato designa una instancia de variación como una "instancia predeterminada", que usa tablas tradicionales para obtener los valores predeterminados. Todas las demás instancias dependen de los datos predeterminados, además de otros datos Delta. Por ejemplo, una tabla ' glyf ' puede tener una descripción de curva Bézier de una forma de glifo nominal, que es la forma utilizada para la instancia predeterminada, mientras que una tabla ' GVAR ' describirá cómo se ajustan los puntos de control de Bézier para el glifo para otras instancias. Del mismo modo, otros valores de fuente pueden tener un valor nominal además de datos Delta que describen cómo cambian esos valores para diferentes instancias; por ejemplo, altura x y otras métricas de toda la fuente, o posiciones de anclaje de marca específicas del glifo y ajustes de interletraje. 

Dado que las fuentes variables pueden admitir un conjunto arbitrario de ejes de variación, requieren un modelo extensible de familias de fuentes que refleja más directamente cómo los diseñadores de fuentes crean familias de fuentes: una familia de fuentes se define mediante un nombre de familia y ciertas características de diseño que son constantes, con un número arbitrario (determinado por el desarrollador de fuentes) de formas en que el diseño puede variar. Se puede crear una familia de fuentes con variantes de peso, pero se puede crear una familia de fuentes distinta con variantes de x-height, Serif-size, "Funk" o lo que el desarrollador de fuentes desee. En este modelo, la selección de una fuente de fuentes se describe mejor mediante el nombre de familia general o "preferido" o "tipográfico" más un conjunto de pares clave-valor, cada uno de los cuales representa un tipo de variación y un valor específico, con los tipos de variación en general como un conjunto extensible. Esta noción general de una familia de fuentes se puede aplicar a fuentes tradicionales y no variables, así como a fuentes de variables. Por ejemplo, en este modelo de familia tipográfica general, una familia "Selawik VF" puede tener variaciones de peso, tamaño óptico y serifa de diseño, con instancias como "San de banner semiligero". 

Sin embargo, algunas implementaciones de software existentes, incluidas las API de DirectWrite existentes, se pueden diseñar suponiendo un modelo más limitado de familias de fuentes. Por ejemplo, algunas aplicaciones pueden suponer que una familia de fuentes puede tener, como máximo, las variantes normal, negrita, cursiva y negrita cursiva. Las interfaces [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) y [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) existentes suponen un modelo de familia de peso/Stretch/Style ("WSS"), lo que permite especificar variantes dentro de una familia mediante las enumeraciones de [**\_ \_ estilo**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) de fuente DWRITE, DWRITE o DWRITE Font [**\_ \_ Stretch**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) como parámetros. [**\_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) Tomando el ejemplo anterior, el tamaño óptico y los ejes Serif no se tratarían como ejes internos de la familia de variación en el modelo de WSS. 

La compatibilidad completa con las fuentes variables requeriría las API que permiten especificar un miembro de la familia con potencialmente varios parámetros, según lo determinado por la fuente. Sin embargo, los diseños de API existentes pueden proporcionar compatibilidad parcial con las fuentes variables al proyectar las instancias con nombre definidas en una fuente variable en los modelos de familia de fuentes más limitados. En el ejemplo anterior, "Selawik VF semiligera San" se podía proyectar en el modelo de WSS como una familia "Selawik de banner de VF" con "semilight" como variante de peso. 

En otro ejemplo, considere una familia de fuentes tipográficas como Sitka, con variantes de peso y de tamaño óptico. Las variantes con nombre dentro de la familia incluyen Sitka Text regular y Sitka banner Bold (más muchas otras). El nombre de la familia tipográfica es "Sitka", mientras que los nombres de las variantes del modelo de la familia tipográfica serían "Text regular" y "banner Bold". Los modelos de cuatro miembros y de la familia WSS no permiten las variantes de tamaño óptico dentro de una familia, por lo que las distinciones de tamaño óptico deben tratarse como distinciones en el nivel de familia. En la tabla siguiente se muestra cómo se trataría una selección de fuentes de la familia tipográfica Sitka en el modelo de la familia WSS: 



Modelo de familia tipográfica

Modelo de la familia WSS

Familia

Face

Familia

Face

Sitka

Texto normal

Texto Sitka

Normal

Sitka

Pancarta en negrita

Banner de Sitka

Bold

Sitka

Título en cursiva

Título Sitka

Cursiva



 

La proyección de los nombres de un modelo de familia tipográfico en el modelo de la familia WSS se puede aplicar a fuentes no variables y a las instancias con nombre de las fuentes variables. Sin embargo, esto no se puede hacer para otras instancias sin nombre del espacio de variación de diseño continuo de una fuente de variable. Por esta razón, la compatibilidad con la funcionalidad completa de las fuentes variables requerirá las API diseñadas para hacer referencia a rostros dentro de una familia tipográfica en términos de un conjunto sin restricciones de ejes de variación y valores de eje. 

## <a name="opentype-variable-font-support-in-directwrite"></a>Compatibilidad con fuentes variables OpenType en DirectWrite

A partir del lanzamiento de Windows 10 Creators Update, el formato de fuente OpenType variable sigue siendo muy nuevo y los proveedores de fuentes, las plataformas y las aplicaciones todavía están en proceso de implementar el nuevo formato. Esta actualización proporciona una implementación inicial para este formato en DirectWrite. 

Los elementos internos de DirectWrite se han actualizado para admitir fuentes de variables OpenType. Con las API actuales, proporciona compatibilidad con las instancias con nombre de una fuente de variable. Esta compatibilidad se puede usar para flujos de trabajo completos: desde la enumeración de las instancias con nombre, la selección de una instancia con nombre, el uso en el diseño y la forma, hasta la representación y la impresión. En el caso de las aplicaciones que también usan la interoperabilidad de texto GDI para ciertas operaciones, también se ha agregado compatibilidad similar en las API de GDI existentes. 

En Windows 10 Creators Update, DirectWrite no admite instancias arbitrarias que usan la funcionalidad de variación continua de las fuentes variables.

En muchas operaciones, el comportamiento en DirectWrite de las instancias con nombre de una fuente variable no se puede distinguir del comportamiento de las fuentes no variables. Y como la compatibilidad se proporciona mediante las API de DirectWrite existentes, las instancias con nombre de las fuentes variables pueden incluso trabajar en muchas aplicaciones de DirectWrite existentes sin ningún cambio. Sin embargo, es posible que se apliquen excepciones en determinadas situaciones:  

-   Si una aplicación procesa los datos de fuente directamente para determinadas operaciones. Por ejemplo, si una aplicación lee datos de contorno de glifos directamente desde el archivo de fuente para crear determinados efectos visuales.
-   Si una aplicación usa una biblioteca de terceros para determinadas operaciones. Por ejemplo, si una aplicación usa DirectWrite para el diseño, para obtener índices y posiciones finales del glifo, pero usa una biblioteca de terceros para la representación.
-   Si una aplicación inserta datos de fuentes en un documento o de otra manera pasa los datos de fuente a un proceso de nivel inferior.

Si las operaciones se realizan mediante implementaciones que no admiten fuentes variables, es posible que estas operaciones no produzcan los resultados esperados. Por ejemplo, las posiciones del glifo se pueden calcular para una instancia con nombre de la fuente variable, pero los glifos se pueden representar suponiendo una instancia con nombre diferente. Dependiendo de la implementación de la aplicación, los resultados pueden funcionar en algunos contextos, pero no en otros contextos en los que se pueden usar otras bibliotecas. Por ejemplo, el texto puede mostrarse correctamente en la pantalla, pero no cuando se imprime. Si los flujos de trabajo de un extremo a otro se implementan usando solo DirectWrite, se puede esperar el comportamiento correcto de las instancias con nombre de una fuente variable. 

Dado que las API de DirectWrite existentes admiten la selección de caras con el modelo de estilo pondera/Stretch/, las instancias con nombre de las fuentes que usan otros ejes de variación se proyectarán desde el modelo de familia tipográfica general en el modelo de WSS, tal y como se ha descrito anteriormente. Esto se basa en una fuente variable que incluye una tabla "atributos de estilo" (' STAT ') con subtablas de valores de eje, que DWrite usa para distinguir los tokens de nombre de fuente que designan los atributos weight, stretch o style de los tokens que pertenecen a otros ejes de variación.  

Si una fuente de variable no incluye una tabla ' STAT ', tal como se requiere para las fuentes variables mediante la especificación OpenType, DirectWrite tratará la fuente como una fuente no variable que contenga solo la instancia predeterminada.  

Si una fuente contiene una tabla ' STAT ' pero no incluye las subtablas de valores de eje apropiadas, esto puede dar lugar a resultados inesperados, como tener varias caras que tengan nombres de caras idénticos. Estas fuentes no se admiten en este momento. 

La especificación OpenType permite que los datos del contorno del glifo se representen en uno de los dos formatos siguientes: usar una tabla ' glyf ', que usa el esquema TrueType y el formato sugerido, o el uso de una tabla ' CFF ', que usa la representación del formato de fuente compacta ("CFF"). En una fuente variable con los esquemas TrueType, la tabla ' glyf ' se sigue usando y se complementa con una tabla ' GVAR ' que proporciona los datos de variación de los contornos. Esto significa que la instancia predeterminada de una fuente variable con los esquemas TrueType solo usa las tablas OpenType tradicionales que se admitirán en el software antiguo y que no tenga compatibilidad con fuentes variables. Sin embargo, en una fuente de variable con esquemas CFF, la tabla ' CFF ' se sustituye por la tabla ' CFF2 ', que encapsula los datos de esquema predeterminados y los datos de variación asociados en una tabla. Los datos CFF los procesa un rasterizador independiente de los que se usan para los datos TrueType, y una tabla ' CFF2 ' requiere un rasterizador CFF actualizado que tenga compatibilidad con ' CFF2 '. Una tabla ' CFF2 ' no puede ser procesada por los rasterizadores de CFF anteriores. En el caso de una fuente variable con datos de esquema CFF, esto significa que incluso la instancia predeterminada no funcionará en software anterior. 

En Windows 10 Creators Update, DirectWrite no admite fuentes variables con datos de esquema CFF mediante la tabla ' CFF2 '. 

## <a name="using-opentype-variable-fonts"></a>Usar fuentes de variables OpenType

Las fuentes de variables OpenType pueden ser fáciles de usar, teniendo en cuenta las limitaciones actuales indicadas anteriormente: 

-   En este momento, solo se admiten las instancias con nombre de una fuente variable.
-   En este momento solo se admiten las fuentes variables que usan datos de contorno de glifos TrueType (no CFF). 
-   En el caso de las fuentes que usan ejes de variación de diseño distintas de weight, stretch o Style, las instancias con nombre se proyectarán en el modelo de la familia WSS, lo que puede dar lugar a que algunas instancias con nombre aparezcan como familias independientes (como ocurre en el pasado para las fuentes no variables). Para admitir esto, las fuentes variables deben tener una tabla ' STAT ' que incluya las subtablas de valores de eje apropiadas.
-   Las instancias con nombre de las fuentes de variables se admiten en las API de DirectWrite, pero si ciertas operaciones se realizan en implementaciones anteriores que no admiten fuentes variables, pueden producir resultados incorrectos. 
-   Ciertas API de DirectWrite usan las enumeraciones [**DWRITE Font \_ \_ Weight**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), [**DWRITE \_ Font \_ Stretch**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) y [**DWRITE \_ Font \_ Style**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) para especificar los atributos weight, stretch y Style al seleccionar caras. Si una fuente de variable usa ejes de variación correspondientes pero tiene muchas instancias con nombre que requieren una granularidad más fina, no todas las instancias con nombre se podrán seleccionar en esas API.

Las fuentes de variables OpenType que cumplen estos requisitos se pueden instalar desde el shell de Windows, al igual que otras fuentes OpenType, y también se pueden usar en conjuntos de fuentes personalizados creados por una aplicación.  

Cuando se instalan en el sistema, todas las instancias con nombre de una fuente de variable se incluirán en el conjunto de fuentes devuelto mediante una llamada al método IDWriteFontFamily3::[**GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) . Tenga en cuenta que un conjunto de fuentes es una lista plana sin una jerarquía de agrupación de familia, pero cada elemento del conjunto tiene una propiedad de nombre de familia basada en el modelo de la familia WSS. Se puede filtrar el conjunto de fuentes para una instancia determinada de la fuente variable con nombre mediante los métodos [**IDWriteFontSet:: GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) . Sin embargo, si se usa la sobrecarga **GetMatchingFonts** que toma familyName, el familyName especificado debe usar el nombre conforme al modelo de la familia de fuentes WSS. La lista completa de los nombres de familia compatibles con WSS que se producen en un conjunto de fuentes se puede obtener mediante los métodos [**IDWriteFontSet:: GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) con el \_ nombre de familia de identificador de propiedad de fuente DWRITE \_ \_ \_ \_ .  

Del mismo modo, todas las instancias con nombre de una fuente variable se representarán en la colección de fuentes devuelta por el método IDWriteFactory::[**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Dado que los elementos de una colección de fuentes son familias de fuentes basadas en el modelo de WSS, las instancias con nombre de una fuente variable se pueden representar en una colección como miembros de dos o más familias de fuentes. Si se usa el método [**IDWriteFontCollection:: FindFamilyName**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-findfamilyname) , el parámetro familyName debe ser un nombre de familia compatible con WSS. Para buscar todos los nombres de familia compatibles con WSS de una colección de fuentes, una aplicación puede recorrer en bucle cada familia y llamar a [**IDWriteFontFamily:: GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames), aunque puede ser más fácil obtener un conjunto de fuentes correspondiente y usar el método [**GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) tal y como se ha descrito anteriormente. 

Al trabajar con fuentes personalizadas, se pueden usar varios enfoques descritos en el tema [conjuntos de fuentes personalizados](custom-font-sets-win10.md) para crear un conjunto de fuentes. Para agregar una fuente variable a un conjunto de fuentes personalizado, se recomienda el método [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) , ya que admite fuentes variables y agregará todas las instancias con nombre de una fuente variable en una sola llamada. En este momento, no hay ninguna manera de agregar instancias con nombre individuales de una fuente de variable personalizada a un conjunto de fuentes mediante los métodos [**IDWriteFontSetBuilder:: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) , ya que no hay forma de crear una referencia de fuente que especifique cuál de las instancias con nombre de un archivo de fuente variable está pensada. Esto significa que actualmente no hay ninguna manera de agregar instancias con nombre de una fuente personalizada a un conjunto de fuentes personalizado con propiedades personalizadas asignadas. Esto significa que, a su vez, las fuentes de variables personalizadas no se pueden usar con facilidad junto con las API de DirectWrite para fuentes remotas. Sin embargo, si las instancias con nombre de una fuente de variable se incluyen en un conjunto de fuentes del sistema, las referencias de las fuentes con nombre ya existirán y se pueden agregar a los conjuntos de fuentes personalizados, incluido el uso de valores de propiedad personalizados. Vea el tema sobre conjuntos de fuentes personalizadas para obtener más detalles. 

Al trabajar con fuentes variables, las enumeraciones de DWRITE de fuente de DirectWrite y [**\_ \_ espesor de fuente**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) de DWRITE están estrechamente conectadas a los ejes de variación de peso y ancho definidos en la especificación OpenType, pero no son iguales. [**\_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) En primer lugar, la escala numérica de cualquier eje de variación siempre admite valores fraccionarios, mientras que EspesorDeFuente y fontStretch usan enteros. La escala del eje de peso OpenType usa valores comprendidos entre 1 y 1000, que también es compatible con fontWeight. Por lo tanto, el cambio de un valor de eje de peso de variación a fontWeight es relativamente pequeño: los valores de fontWeight indicados para una instancia con nombre se pueden redondear del valor preciso que se usa para definir la instancia con nombre dentro de la fuente. La distinción entre la escala del eje de ancho de DirectWrite y de OpenType es mayor: DirectWrite usa valores de 1 a 9, siguiendo los valores de [usWidthClass](/typography/opentype/spec/os2#uswidthclass) de la tabla de sistema operativo OpenType/2, mientras que la escala del eje de ancho OpenType usa valores positivos que representan un porcentaje del ancho normal. La documentación de [usWidthClass](/typography/opentype/spec/os2#uswidthclass) en la especificación OpenType proporciona una asignación entre los valores 1 a 9 y el porcentaje de valores normales. El valor de fontStretch indicado para una instancia con nombre puede implicar el redondeo al convertir los valores del eje de ancho. 

Al crear un [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), deben especificarse una colección de fuentes y las propiedades de fuente compatibles con WSS (nombre de familia, peso, stretch y estilo). Esto también se aplica cuando se establecen las propiedades de formato de fuente en un intervalo de texto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Las propiedades se pueden obtener de un objeto [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) o de objetos [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) y [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) que representan una instancia con nombre determinada. Como se observó anteriormente, los valores devueltos por los métodos GetWeight y GetStretch pueden ser aproximaciones redondeadas para los valores de eje reales usados para definir la instancia con nombre, pero DirectWrite asignará la combinación de propiedades a la instancia con nombre deseada. 

Del mismo modo, si una aplicación usa [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) para crear datos de reserva de fuentes personalizados, las familias se especifican para las asignaciones de intervalos de caracteres que usan nombres de familia compatibles con WSS. La reserva de fuentes en DirectWrite se basa en las familias con DirectWrite seleccionando una variante dentro de una familia de reserva que es una coincidencia más cercana para la variante de la familia inicial. En el caso de las variantes que implican dimensiones distintas del peso, el ajuste y el estilo, DirectWrite no podría seleccionar tales variantes en una familia de reserva a menos que los datos de reserva personalizados se crearan específicamente para proporcionar asignaciones de reserva para familias que tienen atributos que no son de WSS, como las variantes de tamaño óptico de "título".

 

 