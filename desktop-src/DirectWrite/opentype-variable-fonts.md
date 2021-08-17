---
title: Fuentes variables OpenType
description: En este tema se describen las fuentes de variable OpenType, su compatibilidad con DirectWrite y Direct2D, y cómo usarlas en la aplicación. .
ms.assetid: 788558a7-efe7-b075-942f-ac75a5b86b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c671bebce73cf3bdec42d1f7f570add914db7eb33b8a6bfd1b196d569b9975d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649402"
---
# <a name="opentype-variable-fonts"></a>Fuentes variables OpenType

En este tema se describen las fuentes de variable OpenType, su compatibilidad con DirectWrite y Direct2D, y cómo usarlas en la aplicación. 

-   [¿Qué son las fuentes de variable OpenType?](#what-are-opentype-variable-fonts)
-   [Compatibilidad con fuentes de variable OpenType en DirectWrite](#opentype-variable-font-support-in-directwrite)
-   [Uso de fuentes de variable OpenType](#using-opentype-variable-fonts)

## <a name="what-are-opentype-variable-fonts"></a>¿Qué son las fuentes de variable OpenType?

La versión 1.8 de la especificación de formato de fuente [OpenType](https://www.microsoft.com/typography/otspec/) introdujo una nueva extensión al formato conocido como Variaciones de fuente [OpenType.](/typography/opentype/spec/otvaroverview) Las fuentes que usan estas extensiones se conocen como fuentes de variable OpenType. Una fuente de variable OpenType es una sola fuente que puede comportarse como varias fuentes mediante la interpolación continua entre distintos diseños, todo ello definido dentro de la única fuente.

Una fuente de variable OpenType puede definir la variación continua de su diseño a lo largo de uno o varios ejes independientes, como el peso o el ancho: 

 

![Muestra una fuente de variable OpenType con la letra "G" y muestra distintas variaciones a lo largo de un eje de ancho horizontal y un eje de peso vertical.](images/opentype-width-weight.png)

Un desarrollador de fuentes determina un conjunto de ejes de variación que se usarán en una fuente determinada. Estos ejes pueden incluir un conjunto de ejes conocidos (o "registrados") de variación, como el peso y el ancho, pero también pueden incluir ejes arbitrarios personalizados de variación definidos por el desarrollador de fuentes.  

Al seleccionar un conjunto de ejes de variación para una fuente, el desarrollador de fuentes define un espacio abstracto y n dimensional de variación de diseño para la fuente. Los motores de texto pueden especificar potencialmente cualquier posición, o "instancia", dentro de ese espacio continuo para la representación y la representación de texto. 

El desarrollador de fuentes también puede seleccionar y asignar nombres a instancias concretas dentro del espacio de variación de diseño; se conocen como "instancias con nombre". Por ejemplo, una fuente con variación de peso puede admitir una variación continua entre trazos muy ligeros y muy pesados, mientras que el desarrollador de fuentes ha seleccionado pesos concretos a lo largo de esa continuidad y les ha asignado nombres, como "Light", "Regular" y "Semibold". 

El formato de fuente de variable OpenType usa tablas de datos que se encuentran en fuentes OpenType tradicionales, además de ciertas tablas adicionales que describen cómo cambian los valores de varios elementos de datos para diferentes instancias. El formato designa una instancia de variación como una "instancia predeterminada", que usa tablas tradicionales para obtener los valores predeterminados. Todas las demás instancias dependen de los datos predeterminados más otros datos diferenciales. Por ejemplo, una tabla "glyf" puede tener una descripción de curva Bézier de una forma de glifo nominal, que es la forma usada para la instancia predeterminada, mientras que una tabla "gvar" describirá cómo se ajustan los puntos de control Bézier para el glifo para otras instancias. De forma similar, otros valores de fuente pueden tener un valor nominal más datos delta que describen cómo cambian esos valores para instancias diferentes. por ejemplo, x-height y otras métricas de ancho de fuente, o posiciones de anclaje de marca específicas del glifo y ajustes de kerning. 

Dado que las fuentes variables pueden admitir un conjunto arbitrario de ejes de variación, requieren un modelo extensible de familias de fuentes que refleje más directamente cómo los diseñadores de fuentes crean familias de fuentes: una familia de fuentes se define mediante un nombre de familia y determinadas características de diseño que son constantes, con un número arbitrario (determinado por el desarrollador de fuentes) de formas en las que el diseño puede variar. Se puede crear una familia de fuentes con variantes para el peso, pero se puede crear una familia de fuentes diferente con variantes para x-height, serif-size, "iness" o lo que el desarrollador de fuentes desee. En este modelo, una selección de la cara de fuente se describe mejor mediante el nombre de familia general, o "preferido" o "tipográfico", más un conjunto de pares clave-valor, cada uno de los que representa un tipo de variación y un valor específico, siendo los tipos de variación en general un conjunto extensible. Esta noción general de una familia de fuentes se puede aplicar a fuentes tradicionales no variables, así como a fuentes de variables. Por ejemplo, en este modelo de familia tipográfico general, una familia "Selawik VF" podría tener variaciones de peso, tamaño óptico y diseño serif, con instancias como "Semilight Banner Sans". 

Sin embargo, algunas implementaciones de software existentes, incluidas las API de DirectWrite existentes, se pueden diseñar suponiendo un modelo más limitado de familias de fuentes. Por ejemplo, algunas aplicaciones pueden suponer que una familia de fuentes puede tener, como máximo, variantes Regular, Bold, Italic y Bold Italic. Las interfaces [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) e [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) existentes asumen un modelo de familia de peso,stretch/estilo ("WSS"), lo que permite especificar variantes dentro de una familia mediante las enumeraciones [**DWRITE \_ FONT \_ WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), [**DWRITE \_ FONT \_ STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) o [**DWRITE FONT \_ \_ STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) como parámetros. Tomando el ejemplo anterior, los ejes de tamaño óptico y serif no se tratarían como ejes internos de familia de variación en el WSS modelo. 

La compatibilidad completa con las fuentes de variables requeriría API que permitan especificar un miembro de la familia con varios parámetros potencialmente, determinados por la fuente. Sin embargo, los diseños de API existentes pueden proporcionar compatibilidad parcial con las fuentes de variables proyectando las instancias con nombre definidas en una fuente variable en los modelos de familia de fuentes más limitados. En el ejemplo anterior, "Selawik VF Semilight Banner Sans" se podía proyectar en el modelo WSS como una familia "Selawik VF Banner Sans" con "Semilight" como variante de peso. 

Para otro ejemplo, considere una familia de fuentes tipográficos como Sitka, con variantes de peso y tamaño óptico. Las variantes con nombre dentro de la familia incluyen Sitka Text Regular y Sitka Banner Bold (además de muchas otras). El nombre de familia tipográfica es "Sitka", mientras que los nombres de las caras de estas variantes en el modelo de familia tipográfica serían "Text Regular" y "Banner Bold". Los modelos de familia de cuatro miembros y WSS no permiten variantes de tamaño óptico dentro de una familia, por lo que las distinciones de tamaño óptico deben tratarse como distinciones de nivel de familia. En la tabla siguiente se muestra cómo se trataría una selección de fuentes de la familia tipográfica Sitka en el modelo WSS familia: 



Modelo de familia tipográfica

WSS de familia

Familia

Face

Familia

Face

Sitka

Texto normal

Sitka Text

Normal

Sitka

Banner Bold

Sitka Banner

Negrita

Sitka

Título cursiva

Título de Sitka

Cursiva



 

La proyección de nombres de un modelo de familia tipográfico al modelo de familia WSS se puede aplicar a fuentes no variables y a las instancias con nombre de fuentes de variables. Sin embargo, esto no se puede hacer para otras instancias sin nombre del espacio de variación de diseño continuo de una fuente variable. Por esta razón, la compatibilidad con la funcionalidad completa de las fuentes variables requerirá API diseñadas para hacer referencia a caras dentro de una familia tipográfica en términos de un conjunto sin restricciones de ejes de variación y valores de eje. 

## <a name="opentype-variable-font-support-in-directwrite"></a>Compatibilidad con fuentes de variable OpenType en DirectWrite

Desde el lanzamiento de Windows 10 Creators Update, el formato de fuente de la variable OpenType sigue siendo muy nuevo y los proveedores de fuentes, las plataformas y las aplicaciones todavía están en proceso de implementar el nuevo formato. Esta actualización proporciona la implementación inicial para este formato en DirectWrite. 

DirectWrite internos se han actualizado para admitir fuentes de variable OpenType. Con las API actuales, esto proporciona compatibilidad con cualquier instancia con nombre de una fuente de variable. Esta compatibilidad se puede usar para flujos de trabajo completos, desde la enumeración de las instancias con nombre, la selección de una instancia con nombre, el uso en el diseño y la forma, hasta la representación e impresión. En beneficio de las aplicaciones que también usan la interoperabilidad de texto GDI para determinadas operaciones, también se ha agregado compatibilidad similar en las API de GDI existentes. 

En el Windows 10 Creators Update, DirectWrite no admite instancias arbitrarias que usan la funcionalidad de variación continua de las fuentes de variables.

En muchas operaciones, el comportamiento en DirectWrite de instancias con nombre de una fuente de variable no se puede distinguir del comportamiento de las fuentes no variables. Además, dado que se proporciona compatibilidad con las API de DirectWrite existentes, las instancias con nombre de fuentes de variables pueden incluso funcionar en muchas aplicaciones de DirectWrite existentes sin ningún cambio. Sin embargo, se pueden aplicar excepciones en determinadas situaciones:  

-   Si una aplicación procesa los datos de fuente directamente para determinadas operaciones. Por ejemplo, si una aplicación lee los datos de contorno del glifo directamente desde el archivo de fuente para crear determinados efectos visuales.
-   Si una aplicación usa una biblioteca de terceros para determinadas operaciones. Por ejemplo, si una aplicación usa DirectWrite para el diseño, para obtener índices y posiciones de glifo finales, pero luego usa una biblioteca de terceros para la representación.
-   Si una aplicación inserta datos de fuente en un documento o, de alguna otra manera, pasa los datos de fuente a un proceso de bajada.

Si las operaciones se realizan mediante implementaciones que no admiten fuentes variables, es posible que estas operaciones no produzcan los resultados esperados. Por ejemplo, las posiciones de glifo se podrían calcular para una instancia con nombre de la fuente de variable, pero los glifos se podrían representar suponiendo una instancia con nombre diferente. En función de la implementación de la aplicación, los resultados pueden funcionar en algunos contextos, pero no en otros contextos en los que se pueden usar otras bibliotecas. Por ejemplo, el texto puede mostrarse correctamente en pantalla, pero no cuando se imprime. Si los flujos de trabajo de un extremo a otro se implementan utilizando solo DirectWrite, se puede esperar un comportamiento correcto para las instancias con nombre de una fuente variable. 

Dado que las API de DirectWrite existentes admiten la selección de caras mediante el modelo de peso, ajuste y estilo, las instancias con nombre de las fuentes que usan otros ejes de variación se proyectarán desde el modelo de familia tipográfico general en el modelo WSS, como se describió anteriormente. Esto se basa en una fuente variable que incluye una tabla de "atributos de estilo" ('STAT') con subtablas de valor de eje, que DWrite usa para distinguir los tokens de nombre de cara que designan atributos de peso, stretch o style de los tokens que pertenecen a otros ejes de variación.  

Si una fuente de variable no incluye una tabla "STAT", según sea necesario para las fuentes de variables según la especificación OpenType, DirectWrite tratará la fuente como una fuente no variable que contiene solo la instancia predeterminada.  

Si una fuente contiene una tabla "STAT" pero no incluye las subtabla de valores de eje adecuadas, esto puede provocar resultados inesperados, como tener varias caras con nombres de cara idénticos. Estas fuentes no se admiten en este momento. 

La especificación OpenType permite que los datos de contorno del glifo se represente en uno de estos dos formatos: mediante una tabla "glyf", que usa el esquema TrueType y el formato de sugerencias, o una tabla "CFF", que usa una representación de formato de fuente compacto ("CFF"). En una fuente variable con contornos TrueType, se sigue utilizando la tabla "glyf" y se complementa con una tabla "gvar" que proporciona los datos de variación para los contornos. Esto significa que la instancia predeterminada de una fuente de variable con contornos de TrueType solo usa tablas OpenType tradicionales que se admitirán en software anterior que no admite fuentes variables. Sin embargo, en una fuente variable con contornos CFF, la tabla "CFF" se reemplaza por la tabla "CFF2", que encapsula los datos de esquema predeterminados y los datos de variación asociados en una tabla. Los datos de CFF se procesan mediante un rasterizador independiente del que se usa para los datos TrueType, y una tabla "CFF2" requiere un rasterizador CFF actualizado que sea compatible con "CFF2". Los rasterizadores de CFF anteriores no pueden procesar una tabla "CFF2". Para una fuente variable con datos de esquema CFF, esto significa que incluso la instancia predeterminada no funcionará en software anterior. 

En el Windows 10 Creators Update, DirectWrite no admite fuentes variables con datos de esquema CFF mediante la tabla "CFF2". 

## <a name="using-opentype-variable-fonts"></a>Uso de fuentes de variable OpenType

Las fuentes de variable OpenType pueden ser fáciles de usar, teniendo en cuenta las limitaciones actuales que se han indicado anteriormente: 

-   En este momento, solo se admiten instancias con nombre de una fuente de variable.
-   En este momento solo se admiten fuentes variables que usan datos de esquema de glifo TrueType (no esquemas CFF). 
-   En el caso de las fuentes que usan ejes de variación de diseño distintos de peso, stretch o estilo, las instancias con nombre se proyectarán en el modelo de familia WSS, lo que puede dar lugar a que algunas instancias con nombre aparezcan como familias independientes (como sucedería en el pasado para las fuentes no variables). Para admitir esto, las fuentes de variables deben tener una tabla "STAT" que incluya las subtabla de valores de eje adecuadas.
-   Las instancias con nombre de fuentes de variables se admiten en las API de DirectWrite, pero si se realizan determinadas operaciones en implementaciones anteriores que no admiten fuentes de variables, pueden producir resultados incorrectos. 
-   Algunas DIRECTWRITE API usan las enumeraciones [**DWRITE \_ FONT \_ WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), [**DWRITE \_ FONT \_ STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) y [**DWRITE FONT \_ \_ STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) para especificar atributos de peso, ajuste y estilo al seleccionar caras. Si una fuente de variable usa los ejes de variación correspondientes, pero tiene muchas instancias con nombre que requieren una granularidad más precisa, no todas las instancias con nombre se podrán seleccionar en esas API.

Las fuentes de variable OpenType que cumplen estos requisitos se pueden instalar desde el shell de Windows igual que otras fuentes OpenType, y también se pueden usar en conjuntos de fuentes personalizados creados por una aplicación.  

Cuando se instala en el sistema, todas las instancias con nombre de una fuente de variable se incluirán en el conjunto de fuentes devuelto mediante una llamada al método IDWriteFontFamily3::[**GetSystemFontSet.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) Tenga en cuenta que un conjunto de fuentes es una lista plana sin una jerarquía de agrupación de familias, pero cada elemento del conjunto tiene una propiedad de nombre de familia basada en el modelo de familia WSS familia. El conjunto de fuentes se puede filtrar para una instancia con nombre de variable determinada mediante los [**métodos IDWriteFontSet::GetMatchingFonts.**](idwritefontset-getmatchingfonts-overload.md) Sin embargo, si usa la sobrecarga **GetMatchingFonts** que toma un familyName, el familyName especificado debe usar el nombre que se ajusta al modelo de familia de fuentes WSS familia de fuentes. La lista completa de WSS de familia compatibles con dwrite que se producen en un conjunto de fuentes se puede obtener mediante los métodos [**IDWriteFontSet::GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) mediante DWRITE \_ FONT PROPERTY ID FAMILY \_ \_ \_ \_ NAME.  

De forma similar, todas las instancias con nombre de una fuente variable se representarán en la colección de fuentes devuelta por el método IDWriteFactory::[**GetSystemFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) Dado que los elementos de una colección de fuentes son familias de fuentes basadas en el modelo WSS, las instancias con nombre de una fuente variable se pueden representar en una colección como miembros de dos o más familias de fuentes. Si se usa el método [**IDWriteFontCollection::FindFamilyName,**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-findfamilyname) el parámetro familyName debe ser un nombre de familia compatible WSS familia compatible. Para buscar todos los nombres de familia compatibles con WSS de una colección de fuentes, una aplicación puede recorrer en bucle cada familia y llamar a [**IDWriteFontFamily::GetFamilyNames,**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames)aunque puede ser más fácil obtener un conjunto de fuentes correspondiente y usar el método [**GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) como se describió anteriormente. 

Al trabajar con fuentes personalizadas, se pueden usar varios enfoques descritos en el tema [Conjuntos](custom-font-sets-win10.md) de fuentes personalizados para crear un conjunto de fuentes. Para agregar una fuente de variable a un conjunto de fuentes personalizado, se recomienda el método [**IDWriteFontSetBuilder1::AddFontFile,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) ya que admite fuentes de variable y agregará todas las instancias con nombre de una fuente de variable en una sola llamada. En este momento no hay ninguna manera de agregar instancias con nombre individuales de una fuente de variable personalizada a un conjunto de fuentes mediante los métodos [**IDWriteFontSetBuilder::AddFontFaceReference,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) ya que no hay ninguna manera de crear una referencia de la cara de fuente que especifique cuál de las instancias con nombre de un archivo de fuente de variable está pensada. Esto significa que actualmente no hay ninguna manera de agregar instancias con nombre de una fuente personalizada a un conjunto de fuentes personalizado con propiedades personalizadas asignadas. A su vez, esto significa que las fuentes de variables personalizadas actualmente no se pueden usar fácilmente junto con DirectWrite API para fuentes remotas. Sin embargo, si las instancias con nombre de una fuente de variable se incluyen en un conjunto de fuentes del sistema, ya existirán referencias de caras de fuente para cada instancia con nombre y se pueden agregar a conjuntos de fuentes personalizados, incluido el uso de valores de propiedad personalizados. Consulte el tema Conjuntos de fuentes personalizados para obtener más detalles. 

Cuando se trabaja con fuentes variables, las enumeraciones [**DIRECTWRITE DWRITE \_ FONT \_ WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) y [**DWRITE FONT \_ \_ STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) están estrechamente conectadas a los ejes de variación de peso y ancho definidos en la especificación OpenType, pero no son iguales. En primer lugar, la escala numérica de cualquier eje de variación siempre admite valores fraccionales, mientras que fontWeight y fontStretch usan enteros. La escala del eje de peso OpenType usa valores que van de 1 a 1000, que también es compatible con fontWeight. Por lo tanto, el cambio de un valor de eje de peso de variación a fontWeight es relativamente menor: el fontWeight notificado para una instancia con nombre se puede redondear desde el valor preciso utilizado para definir la instancia con nombre dentro de la fuente. La distinción entre DirectWrite fontStretch y la escala del eje de ancho OpenType es mayor: DirectWrite usa valores de 1 a 9, siguiendo los valores [usWidthClass](/typography/opentype/spec/os2#uswidthclass) de la tabla OpenType OS/2, mientras que la escala del eje de ancho OpenType usa valores positivos que representan un porcentaje de ancho normal. La [documentación de usWidthClass](/typography/opentype/spec/os2#uswidthclass) de la especificación OpenType proporciona una asignación entre los valores del 1 al 9 y el porcentaje de valores normales. El valor fontStretch notificado para una instancia con nombre puede implicar redondeo al convertir a partir de valores de eje de ancho. 

Al crear un [**IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)se deben especificar una colección de fuentes y WSS propiedades de fuente compatibles (nombre de familia, peso, stretch y estilo). Esto también se aplica al establecer propiedades de formato de fuente en un [**intervalo de texto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Las propiedades se pueden obtener de un objeto [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) o de objetos [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) e [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) que representan una instancia con nombre determinada. Como se ha observado anteriormente, los valores devueltos por los métodos GetWeight y GetStretch pueden redondear aproximaciones para los valores de eje reales usados para definir la instancia con nombre, pero DirectWrite volverá a asignar la combinación de propiedades a la instancia con nombre deseada. 

De forma similar, si una aplicación usa [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) para crear datos de reserva de fuentes personalizados, se especifican familias para las asignaciones de intervalos de caracteres mediante WSS nombres de familia compatibles. La reserva de fuentes dentro de DirectWrite se basa en familias con DirectWrite seleccionando una variante dentro de una familia de reserva que es la coincidencia más cercana para la variante de la familia inicial. En el caso de las variantes que implican dimensiones distintas del peso, el stretch y el estilo, DirectWrite actualmente no podría seleccionar estas variantes dentro de una familia de reserva a menos que se crearon datos de reserva personalizados específicamente para proporcionar asignaciones de reserva para las familias que tienen atributos no WSS concretos, como variantes de tamaño óptico "Caption".

 

 