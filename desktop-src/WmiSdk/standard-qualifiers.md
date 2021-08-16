---
description: Todas las implementaciones compatibles con CIM deben controlar un conjunto estándar de calificadores.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Calificadores estándar
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67877cfc07a247d6b5e3309270d145bc64fbb814416fa4288c6e85ff2ad2e986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315141"
---
# <a name="standard-qualifiers"></a>Calificadores estándar

Todas las implementaciones compatibles con CIM deben controlar un conjunto estándar de calificadores. Cualquier objeto específico no tiene todos los calificadores enumerados. Normalmente, las clases de extensión suministran calificadores adicionales para facilitar el aprovisionamiento de instancias de clase y otras operaciones en la clase.

Es responsabilidad del proveedor aplicar los calificadores. WMI no aplica calificadores, pero solo los usa para informar al usuario sobre cómo se usa la propiedad .

> [!Note]  
> WMI es compatible con la especificación CIM 2.5.

 

Los calificadores tienen las siguientes limitaciones:

-   No todos los calificadores estándar se pueden usar juntos.
-   No todos los calificadores se pueden aplicar a todas las construcciones, como la asociación o la referencia. Estas limitaciones se identifican en la lista Se aplica a .
-   Para una construcción determinada, como asociación o referencia, el uso de los calificadores legales se puede restringir aún más porque algunos calificadores son mutuamente excluyentes, el uso de un calificador puede implicar algunas restricciones en el valor de otro, y así sucesivamente. Estas reglas de uso están documentadas.
-   Las entidades como propiedades, métodos, instancias o subclases solo heredan calificadores legales, no asociaciones o referencias. Por ejemplo, las referencias no heredan el calificador **MaxLen** que se aplica a las propiedades.

A continuación se enumeran los calificadores estándar de WMI.

<dt>

<span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstracto**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases, asociaciones e indicaciones

Indica si la clase es abstracta y solo sirve como base para las clases nuevas. El valor predeterminado es **FALSE.** No se pueden crear instancias de clases abstractas. La ausencia de este calificador indica que la clase no es abstracta; por lo tanto, este calificador es necesario para todas las clases abstractas.

</dd> <dt>

<span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Agregado**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: referencias

Indica si la referencia es el componente primario de una asociación de agregación. El valor predeterminado es **FALSE.**

Uso: los **calificadores Aggregation** y **Aggregate** se usan juntos   **Agregación** califica la asociación y **Aggregate** especifica la referencia primaria.

</dd> <dt>

<span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Agregación**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: asociaciones

Indica si la asociación es una agregación. El valor predeterminado es **FALSE.** Se usa con **Aggregate**. Este calificador es necesario para todas las asociaciones de agregación.

</dd> <dt>

<span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, referencias, métodos

Nombre alternativo de una propiedad o método en el esquema. El valor predeterminado es **NULL.**

</dd> <dt>

<span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, parámetros

Tipo de la matriz calificada.

Los valores válidos son:

-   bag (valor predeterminado)
-   indizadas
-   ordered

Uso: aplique este tipo de calificador solo a las propiedades y parámetros que son matrices (definidas mediante la sintaxis de corchetes).

</dd> <dt>

<span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bits**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades, métodos, parámetros

Mapa de posiciones de bits significativas donde cada posición significativa puede ser "on" o "off". Cada bit "on" se asigna a un valor correspondiente en la **matriz BitValues.** Al tener varios bits "on", se indican varios valores simultáneos en **la matriz BitValues.** El valor predeterminado es **NULL.**

Para obtener más información, [vea BitMap y BitValues.](bitmap-and-bitvalues.md)

</dd> <dt>

<span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades, métodos, parámetros

Traducción de un valor de posición de bits en una cadena **asociada.** El valor predeterminado es **NULL.**

Para obtener más información, [vea BitMap y BitValues.](bitmap-and-bitvalues.md)

</dd> <dt>

<span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructor**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: métodos

Indica si el método crea instancias de . Estos métodos no están restringidos a actuar en una sola instancia o una sola clase. Por ejemplo, un constructor puede crear instancias de asociación, así como instancias de la clase que define el constructor.

El **calificador** Constructor solo está pensado para obtener información y no se espera que el administrador de objetos actúe sobre él. El administrador de objetos no tiene que llamar a métodos de constructor cuando se crea un objeto . Además, cuando se llama a un constructor, el administrador de objetos no tiene que invocar ningún método de constructor definido para ninguna clase primaria de la clase original. El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases

Nombre del método por el que se crean instancias de esta clase. El valor es "PutInstance" o el nombre de otro método que crea las instancias. El valor predeterminado es **NULL.**

Uso: este calificador solo se puede usar si el calificador **SupportsCreate** está presente.

</dd> <dt>

<span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases

Nombre del método por el que se eliminan las instancias de esta clase. El valor es "DeleteInstance" o el nombre de otro método que elimina las instancias. El valor predeterminado es **NULL.**

Uso: este calificador solo se puede usar si el calificador **SupportsDelete** está presente.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: any

Descripción de un elemento con nombre. El valor predeterminado es **NULL.**

</dd> <dt>

<span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructor**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: métodos

Indica si el método elimina instancias. Los métodos que usan el calificador **Destructor** eliminan las instancias a las que se aplica el destructor y no están restringidos a actuar en una sola instancia o clase. Por ejemplo, un destructor podría eliminar instancias de asociación, así como instancias de la clase que define el destructor.

El **calificador** Destructor solo está pensado para obtener información y no se espera que el administrador de objetos actúe sobre él. No hay ninguna obligación para que el administrador de objetos llame a un método que tenga el **calificador Destructor** cuando se elimina una instancia. Además, cuando se llama a un destructor, el administrador de objetos no tiene que invocar ningún método de destructor definido para ninguna clase primaria de la clase original. El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: cualquier

Nombre que se muestra en la interfaz de usuario en lugar del nombre real del elemento. El valor predeterminado es **NULL.**

</dd> <dt>

<span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: cualquier

El elemento de tipo de cadena completo contiene una instancia incrustada. El valor del calificador especifica el nombre de una clase CIM en el mismo espacio de nombres que la clase propietaria del elemento completo. La instancia insertada es una instancia de la clase especificada, incluidas las instancias de sus subclases. El valor predeterminado es **NULL.**

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Calibre**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: cualquier

Indica si la propiedad representa un entero no negativo, que puede aumentar o disminuir, pero nunca superar un valor máximo. El valor predeterminado es **FALSE.**

El valor máximo de la propiedad no puede ser mayor que 2^*n* - 1. *N* puede ser 8, 16, 32 o 64, según el tipo de datos de la propiedad a la que se aplica este calificador. El valor de un medidor tiene su valor máximo siempre que la información que se va a modelar sea mayor o igual que ese valor máximo. Si la información que se va a modelar posteriormente disminuye por debajo del valor máximo, el medidor también disminuye. Este calificador solo es aplicable a las propiedades con un tipo de datos entero sin signo.

</dd> <dt>

<span id="In"></span><span id="in"></span><span id="IN"></span>**En**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: parámetros

Indica si el parámetro se usa para pasar valores a un método. El valor predeterminado es **TRUE.**

</dd> <dt>

<span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, Out**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: parámetros

Indica si el parámetro es un parámetro de entrada y salida.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Clave**](key-qualifier.md)
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades, referencias

Indica si la propiedad forma parte del identificador del espacio de nombres. Si más de una propiedad tiene el [**calificador Key,**](key-qualifier.md) todas estas propiedades forman colectivamente la clave (una clave compuesta). Cuando se toman juntas, las propiedades de clave deben proporcionar una referencia única para cada instancia de clase. Si este calificador se coloca en una propiedad, solo se permite el valor **TRUE.**

</dd> <dt>

<span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Perezoso**
</dt> <dd>

Se aplica a: propiedades

Indica que la propiedad consume muchos recursos para devolver y requiere una gran cantidad de tiempo y memoria del procesador. WMI mejora el rendimiento de las consultas al no intentar devolver las propiedades marcadas con **el calificador Diferido.**

</dd> <dt>

<span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: clases, propiedades, asociaciones, indicaciones, referencias

Conjunto de valores que indican una ruta de acceso a una ubicación donde puede encontrar más información sobre el origen de una propiedad, clase, asociación, indicación o referencia. La cadena de asignación puede ser una ruta de acceso de directorio, una dirección URL, una clave del Registro, un archivo de include, una referencia a una clase CIM o algún otro formato. El valor predeterminado es **NULL.**

</dd> <dt>

<span id="Max"></span><span id="max"></span><span id="MAX"></span>**máximo**
</dt> <dd>

Tipo de datos: **int**

Se aplica a: referencias

Número máximo de valores que puede tener una referencia determinada para cada conjunto de otros valores de referencia de la asociación. El valor predeterminado es **NULL.** Por ejemplo, si una asociación relaciona instancias A con instancias B y debe haber como máximo una instancia A para cada instancia B, la referencia a A debe tener un máximo de un calificador.

</dd> <dt>

<span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**
</dt> <dd>

Tipo de datos: **int**

Se aplica a: propiedades, métodos, parámetros

Longitud máxima (en caracteres) de un elemento **de** datos de cadena e indica compatibilidad con matrices de longitud fija.

Si se encuentra una matriz de longitud fija, el calificador **MaxLen** contiene la longitud fija encontrada durante el análisis. Si se encuentra una matriz de longitud variable, no se usa este calificador. **MaxLen** se usa para sugerir el número máximo de elementos que se deben almacenar en una matriz. Al reemplazar el valor predeterminado, se puede especificar cualquier valor entero sin signo (**uint32**). Un valor NULL **(valor** predeterminado) implica una longitud ilimitada.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**
</dt> <dd>

Tipo de datos: **int**

Se aplica a: propiedades, métodos, parámetros

Valor máximo del objeto. El valor predeterminado es **NULL.**

</dd> <dt>

<span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**
</dt> <dd>

Tipo de datos: **int**

Se aplica a: referencias

Cardinalidad mínima de la referencia (el número mínimo de valores que puede tener una referencia determinada para cada conjunto de otros valores de referencia de la asociación). El valor predeterminado es 0.

Por ejemplo, si una asociación relaciona instancias A con instancias B y debe haber al menos una instancia A para cada instancia B, la referencia a A debe tener un mínimo de un calificador.

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**
</dt> <dd>

Tipo de datos: **int**

Se aplica a: propiedades, métodos, parámetros

Indica el valor mínimo del objeto. El valor predeterminado es **NULL.**

</dd> <dt>

<span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades

Conjunto de valores que indican la correspondencia entre la propiedad de un objeto y otras propiedades del esquema CIM. El valor predeterminado es **NULL.**

Las propiedades de objeto se identifican mediante la sintaxis siguiente.

<schema name> "\_" <class or association name> "." <property name>

</dd> <dt>

<span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**No local**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: referencias

Ubicación de una instancia de , cuyo valor es <*namespacetype*>://<*namespacehandle*> El valor predeterminado es **NULL.**

Uso: este calificador no se puede usar con el **calificador NonlocalType.**

</dd> <dt>

<span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: referencias

Tipo de ubicación de una instancia. Su valor es <namespacetype> . El valor predeterminado es **NULL.**

Uso: este calificador no se puede usar con el **calificador no** local.

</dd> <dt>

<span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades

Valor que indica que la propiedad asociada es **NULL** (la propiedad no tiene un valor válido o significativo). El valor predeterminado es **NULL.**

Las convenciones y restricciones usadas para definir **valores NULL** son las mismas que las aplicables al **calificador ValueMap.** Tenga en cuenta que este calificador no se puede invalidar. No es razonable permitir que una subclase devuelva un valor **NULL** diferente al de la clase primaria.

</dd> <dt>

<span id="Out"></span><span id="out"></span><span id="OUT"></span>**Salida**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: parámetros

Indica si el parámetro devuelve valores de un método. El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Anular**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, métodos, referencias

Clase primaria o construcción subordinada (propiedad, método o referencia) que se reemplaza por la propiedad, el método o la referencia del mismo nombre en la clase derivada. El valor predeterminado es **NULL.**

El formato es:

\[<*Clase>.* \] < *construcción subordinada*>

Si se omite el nombre de clase, la invalidación se aplica a la construcción subordinada en la clase primaria de la jerarquía de clases.

Uso: el **calificador Override** solo puede hacer referencia a construcciones basadas en el mismo meta model. No se permite cambiar un nombre de construcción o una firma durante una operación de invalidación.

</dd> <dt>

<span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**
</dt> <dd>

Se aplica a: clases

Indica si el valor de propiedad de una subclase invalida el valor de una clase primaria. La implicación funcional es que, si realiza una consulta en la clase primaria y la cláusula **WHERE** incluye esta propiedad, el elemento primario debe devolver una instancia con el valor invalidado. Como resultado, Windows Management ajusta la cláusula **WHERE** de la consulta enviada a la clase primaria para excluir referencias a esta propiedad.

</dd> <dt>

<span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagado**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades

Nombre de la clave que se propaga. El valor predeterminado es **NULL.**

El uso de este calificador supone la existencia de solo un calificador débil en una referencia que tiene la clase que contiene como destino. La propiedad asociada debe tener el mismo valor que la propiedad denominada por el calificador en la clase del otro lado de la asociación débil. El formato es:

\[<*Clase>.* \] < *construcción subordinada*>

Uso: cuando se **usa el calificador Propagated,** el [**calificador key**](key-qualifier.md) debe especificarse con un valor de **TRUE.**

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>**Leer**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica si la propiedad es legible. El valor predeterminado es **TRUE.**

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Obligatorio**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica si se requiere un valor distinto de NULL para la propiedad . El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revisión**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases, asociaciones, indicaciones, esquemas

Número de revisión menor del objeto de esquema. El valor predeterminado es **NULL.**

Uso: el **calificador** de versión debe estar presente para proporcionar el número de versión principal cuando se usa **el** calificador de revisión.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Esquema**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, métodos

Nombre del esquema en el que se define la característica. El valor predeterminado es **NULL.**

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Fuente**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases, asociaciones, indicaciones, referencias

Ubicación de una instancia. El valor predeterminado es **NULL.**

El valor del calificador es <*namespacetype*>://<*namespacehandle*>.

Uso: el **calificador Source** no se puede usar con el **calificador SourceType.**

</dd> <dt>

<span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**Sourcetype**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases, asociaciones, indicaciones, referencias

Tipo de ubicación de una instancia. El valor de este calificador es <*namespacetype*>. El valor predeterminado es **NULL.**

Uso: el **calificador SourceType** no se puede usar con el **calificador Source.**

</dd> <dt>

<span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase admite la creación de instancias. El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase admite la eliminación de instancias. El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase admite la modificación (actualización) de instancias. El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase puede tener subclases. El valor predeterminado es **FALSE.**

Si se declara una subclase, el compilador genera un error.

Uso: este calificador no puede coexistir con el **calificador abstracto.** Si se especifican **los calificadores Terminal** y **Abstract,** el compilador genera un error.

</dd> <dt>

<span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Unidades**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, métodos, parámetros

Tipo de unidad en la que se expresa el elemento de datos asociado. El valor predeterminado es **NULL.**

Por ejemplo, un elemento de datos de tamaño podría tener un valor de "bytes" para **unidades**.

</dd> <dt>

<span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades, métodos, parámetros

Conjunto de valores permitidos para una propiedad, tipo de valor devuelto de método o parámetro de método. El valor predeterminado es **NULL.**

Uso: este calificador se puede usar solo o en combinación con el **calificador Valores.** Cuando se usa en combinación con el calificador **Values,** la ubicación del valor en la matriz **ValueMap** proporciona la ubicación de la entrada correspondiente en la **matriz Values.** Use el **calificador ValueMap** solo con valores de cadena y enteros. La sintaxis para representar un valor entero en la matriz de asignación de valores es \[ + \| = \] el \[ \* dígito \] . El contenido, el número máximo de dígitos y el valor representado están restringidos por el tipo de la propiedad asociada. Por ejemplo, uint8 puede no estar firmado, debe tener menos de cuatro dígitos y debe representar un valor menor que 256.

</dd> <dt>

<span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Valores**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades, métodos, parámetros

Conjunto de valores que traducen un valor entero en una cadena asociada. El valor predeterminado es **NULL.**

Esta propiedad también especifica una matriz de valores de cadena que se asignarán a una propiedad de enumeración. Este calificador se puede aplicar a una propiedad de entero o una propiedad de cadena, y la asignación puede ser implícita o explícita. Si la asignación es implícita, los valores de propiedad integer o string representan posiciones ordinales en la **matriz Values.** Si la asignación es explícita, la propiedad debe ser un entero y los valores de propiedad válidos se enumeran en la matriz definida por el **calificador ValueMap.** Para obtener más información, vea [Asignación de valores.](value-map.md)

Si un **calificador ValueMap** no está presente, la matriz **Values** se indexa (relativa a cero) mediante el valor de la propiedad asociada, el tipo de valor devuelto del método o el parámetro de método. Si hay **un calificador ValueMap,** el índice de valores se define mediante la ubicación del valor de propiedad en el mapa de valores.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versión**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases, esquemas, asociaciones, indicaciones

Número de versión principal del objeto de esquema. El valor predeterminado es **NULL.** El número de versión se incrementa cuando se realizan cambios en el esquema que modifican la interfaz.

</dd> <dt>

<span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Débil**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: referencias

Indica si las claves de la clase a la que se hace referencia incluyen las claves de los demás participantes de la asociación. El valor predeterminado es **FALSE.**

Este calificador se usa cuando la identidad de la clase a la que se hace referencia depende de la identidad de los demás participantes de la asociación. No puede haber más de una referencia a una clase determinada. Las demás clases de la asociación deben definir una clave. Las claves de las otras clases de la asociación se repiten en la clase a la que se hace referencia y se etiquetan con un **calificador Propagated.**

</dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Escribir**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica que las aplicaciones o scripts pueden cambiar el valor de propiedad. La cuenta que ejecuta la aplicación debe tener acceso al espacio de nombres que contiene instancias de la clase . La implementación del proveedor también puede limitar el acceso a los datos del proveedor. Un valor **TRUE indica** que los consumidores a los que WMI y el proveedor permiten el acceso a la propiedad son legibles y fáciles de escribir. El valor predeterminado es **FALSE.**

Es posible que una propiedad que no tenga **el calificador Write** todavía pueda escribirse. La implementación del proveedor puede permitir que se cambien las propiedades de las clases de proveedor, independientemente de si el **calificador Write** está presente.

</dd> <dt>

<span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica si la propiedad se puede escribir en la creación de la instancia. Este calificador se puede usar junto con el **calificador WriteAtCreate.** El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica si la propiedad se puede escribir en la actualización de la instancia. Este calificador se puede usar junto con el **calificador WriteAtCreate.** El valor predeterminado es **FALSE.**

</dd> </dl>

## <a name="examples"></a>Ejemplos

Para obtener más información sobre cómo recuperar calificadores, vea el ejemplo de código de PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) en la Galería de TechNet.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Calificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Agregar un calificador](adding-a-qualifier.md)
</dt> </dl>

 

 




