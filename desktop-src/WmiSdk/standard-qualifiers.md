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
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706080"
---
# <a name="standard-qualifiers"></a>Calificadores estándar

Todas las implementaciones compatibles con CIM deben controlar un conjunto estándar de calificadores. Cualquier objeto específico no tiene todos los calificadores enumerados. Normalmente, las clases de extensión proporcionan calificadores adicionales para facilitar el aprovisionamiento de instancias de clase y otras operaciones en la clase.

Es responsabilidad del proveedor aplicar los calificadores. WMI no aplica calificadores, pero solo los utiliza para informar al usuario sobre cómo se usa la propiedad.

> [!Note]  
> WMI es compatible con la especificación CIM 2,5.

 

Los calificadores tienen las siguientes limitaciones:

-   No todos los calificadores estándar se pueden usar juntos.
-   No todos los calificadores se pueden aplicar a todas las construcciones, como Association o Reference. Estas limitaciones se identifican en la lista se aplica a.
-   Para una construcción determinada, como Association o Reference, el uso de los calificadores legales se puede restringir aún más porque algunos calificadores son mutuamente excluyentes, el uso de un calificador puede implicar algunas restricciones en el valor de otro, etc. Estas reglas de uso están documentadas.
-   Los calificadores válidos son heredados por entidades como propiedades, métodos, instancias o subclases únicamente, no por asociaciones ni referencias. Por ejemplo, las referencias no heredan el calificador **MaxLen** que se aplica a las propiedades.

A continuación se enumeran los calificadores estándar de WMI.

<dt>

<span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Descripción**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases, asociaciones, indicaciones

Indica si la clase es abstracta y solo sirve como base para las nuevas clases. El valor predeterminado es **false**. No se pueden crear instancias de clases abstractas. La ausencia de este calificador indica que la clase no es abstracta; por lo tanto, este calificador es necesario para todas las clases abstractas.

</dd> <dt>

<span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Agregado**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: referencias

Indica si la referencia es el componente primario de una asociación de agregación. El valor predeterminado es **false**.

Uso: los **calificadores de agregación y** **agregado** se usan juntos la   **agregación** califica la asociación y **Aggregate** especifica la referencia primaria.

</dd> <dt>

<span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Concentrado**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: asociaciones

Indica si la asociación es una agregación. El valor predeterminado es **false**. Se utiliza con **Aggregate**. Este calificador es necesario para todas las asociaciones de agregación.

</dd> <dt>

<span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, referencias, métodos

Nombre alternativo para una propiedad o un método en el esquema. El valor predeterminado es **null**.

</dd> <dt>

<span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, parámetros

Tipo de la matriz calificada.

Los valores válidos son:

-   bolsa (valor predeterminado)
-   indizadas
-   ordered

Uso: aplique este tipo de calificador solo a las propiedades y los parámetros que son matrices (definidas mediante la sintaxis de paréntesis).

</dd> <dt>

<span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**MyBitmap**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades, métodos, parámetros

Asignación de posiciones de bits significativas en las que cada posición significativa puede ser "ON" u "OFF". Cada bit "ON" se asigna a un valor correspondiente en la matriz **BitValues** . Al tener varios bits "ON", se indican varios valores simultáneos en la matriz **BitValues** . El valor predeterminado es **null**.

Para obtener más información, consulte [Bitmap y BitValues](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades, métodos, parámetros

Traducción de un valor de posición de bits en una **cadena** asociada. El valor predeterminado es **null**.

Para obtener más información, consulte [Bitmap y BitValues](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructor**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: métodos

Indica si el método crea instancias de. Estos métodos no están restringidos a actuar en una sola instancia o en una sola clase. Por ejemplo, un constructor puede crear instancias de asociación, así como instancias de la clase que define el constructor.

El calificador de **constructor** está pensado únicamente para información y no se espera que lo actúe el administrador de objetos. El administrador de objetos no tiene que llamar a métodos de constructor cuando se crea un objeto. Además, cuando se llama a un constructor, el administrador de objetos no tiene que invocar ningún método de constructor definido para cualquier clase primaria de la clase original. El valor predeterminado es **false**.

</dd> <dt>

<span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases

Nombre del método por el que se crean las instancias de esta clase. El valor es "PutInstance" o el nombre de otro método que crea las instancias. El valor predeterminado es **null**.

Uso: este calificador solo se puede usar si el calificador **SupportsCreate** está presente.

</dd> <dt>

<span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases

Nombre del método por el que se eliminan las instancias de esta clase. El valor es "DeleteInstance" o el nombre de otro método que elimina las instancias. El valor predeterminado es **null**.

Uso: este calificador solo se puede usar si el calificador **SupportsDelete** está presente.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: any

Descripción de un elemento con nombre. El valor predeterminado es **null**.

</dd> <dt>

<span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructor**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: métodos

Indica si el método elimina instancias. Los métodos que usan el calificador de **destructor** eliminan las instancias a las que se aplica el destructor y no están restringidas a actuar en una sola instancia o clase. Por ejemplo, un destructor podría eliminar las instancias de asociación, así como las instancias de la clase que define el destructor.

El calificador de **destructor** está pensado únicamente para la información y no se espera que lo actúe el administrador de objetos. El administrador de objetos no tiene ninguna obligación de llamar a un método que tiene el calificador de **destructor** cuando se elimina una instancia. Además, cuando se llama a un destructor, el administrador de objetos no tiene que invocar los métodos de destructor definidos para cualquier clase primaria de la clase original. El valor predeterminado es **false**.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Mostrar**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: any

Nombre que se muestra en la interfaz de usuario en lugar del nombre real del elemento. El valor predeterminado es **null**.

</dd> <dt>

<span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: any

El elemento de tipo de cadena calificado contiene una instancia incrustada. El valor de calificador especifica el nombre de una clase CIM en el mismo espacio de nombres que la clase propietaria del elemento calificado. La instancia incrustada es una instancia de la clase especificada, incluidas las instancias de sus subclases. El valor predeterminado es **null**.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gálibo**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: any

Indica si la propiedad representa un entero no negativo, que puede aumentar o disminuir, pero nunca superar un valor máximo. El valor predeterminado es **false**.

El valor máximo de la propiedad no puede ser mayor que 2 ^*n* -1. *N* puede ser 8, 16, 32 o 64, dependiendo del tipo de datos de la propiedad a la que se aplica este calificador. El valor de un medidor tiene su valor máximo siempre que la información que se está modelando sea mayor o igual que ese valor máximo. Si la información que se modela se reduce posteriormente por debajo del valor máximo, el medidor también se reduce. Este calificador solo es aplicable a las propiedades con un tipo de datos entero sin signo.

</dd> <dt>

<span id="In"></span><span id="in"></span><span id="IN"></span>**De**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: parámetros

Indica si el parámetro se utiliza para pasar valores a un método. El valor predeterminado es **true**.

</dd> <dt>

<span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, out**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: parámetros

Indica si el parámetro es un parámetro de entrada y de salida.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Clave**](key-qualifier.md)
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades, referencias

Indica si la propiedad forma parte del identificador de espacio de nombres. Si hay más de una propiedad que tiene el calificador de [**clave**](key-qualifier.md) , todas estas propiedades forman colectivamente la clave (una clave compuesta). Cuando se toman juntas, las propiedades clave deben proporcionar una referencia única para cada instancia de clase. Si este calificador se coloca en una propiedad, solo se permite el valor **true** .

</dd> <dt>

<span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Vago**
</dt> <dd>

Se aplica a: propiedades

Indica que la propiedad utiliza muchos recursos para devolver y requiere mucha memoria y tiempo de procesador. WMI mejora el rendimiento de las consultas al no intentar devolver las propiedades marcadas con el calificador **Lazy** .

</dd> <dt>

<span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: clases, propiedades, asociaciones, indicaciones, referencias

Conjunto de valores que indican una ruta de acceso a una ubicación donde puede encontrar más información sobre el origen de una propiedad, clase, Asociación, indicación o referencia. La cadena de asignación puede ser una ruta de acceso de directorio, una dirección URL, una clave del registro, un archivo de inclusión, una referencia a una clase CIM o algún otro formato. El valor predeterminado es **null**.

</dd> <dt>

<span id="Max"></span><span id="max"></span><span id="MAX"></span>**Máx.**
</dt> <dd>

Tipo de datos: **int**

Se aplica a: referencias

Número máximo de valores que puede tener una referencia determinada para cada conjunto de valores de referencia de la asociación. El valor predeterminado es **null**. Por ejemplo, si una asociación relaciona una instancia con instancias B y debe haber como máximo una instancia para cada instancia B, la referencia a debe tener un máximo de un calificador.

</dd> <dt>

<span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**
</dt> <dd>

Tipo de datos: **int**

Se aplica a: propiedades, métodos, parámetros

Longitud máxima (en caracteres) de un elemento de datos de **cadena** e indica la compatibilidad con matrices de longitud fija.

Si se encuentra una matriz de longitud fija, el calificador **MaxLen** contiene la longitud fija encontrada durante el análisis. Si se encuentra una matriz de longitud variable, no se utiliza este calificador. **MaxLen** se utiliza para sugerir el número máximo de elementos que deben almacenarse en una matriz. Al invalidar el valor predeterminado, se puede especificar cualquier valor entero sin signo (**UInt32**). Un valor **null** (valor predeterminado) implica una longitud ilimitada.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**
</dt> <dd>

Tipo de datos: **int**

Se aplica a: propiedades, métodos, parámetros

Valor máximo del objeto. El valor predeterminado es **null**.

</dd> <dt>

<span id="Min"></span><span id="min"></span><span id="MIN"></span>**Minuto**
</dt> <dd>

Tipo de datos: **int**

Se aplica a: referencias

Cardinalidad mínima de la referencia (el número mínimo de valores que puede tener una referencia determinada para cada conjunto de valores de referencia de la Asociación). El valor predeterminado es 0.

Por ejemplo, si una asociación relaciona una instancia con instancias de B y debe haber al menos una instancia de para cada instancia B, la referencia a debe tener como mínimo un calificador.

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**
</dt> <dd>

Tipo de datos: **int**

Se aplica a: propiedades, métodos, parámetros

Indica el valor mínimo del objeto. El valor predeterminado es **null**.

</dd> <dt>

<span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades

Conjunto de valores que indican la correspondencia entre la propiedad de un objeto y otras propiedades del esquema CIM. El valor predeterminado es **null**.

Las propiedades de objeto se identifican con la sintaxis siguiente.

<schema name> "\_" <class or association name> "." <property name>

</dd> <dt>

<span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**No locales**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: referencias

Ubicación de una instancia, cuyo valor es <*espacio*>://<*namespacehandle*> el valor predeterminado es **null**.

Uso: este calificador no se puede usar con el calificador **NonlocalType** .

</dd> <dt>

<span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: referencias

Tipo de ubicación de una instancia. Su valor es <namespacetype> . El valor predeterminado es **null**.

Uso: este calificador no se puede usar con el calificador no **local** .

</dd> <dt>

<span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades

Valor que indica que la propiedad asociada es **null** (la propiedad no tiene un valor válido o significativo). El valor predeterminado es **null**.

Las convenciones y restricciones que se usan para definir valores **null** son las mismas que las aplicables al calificador **ValueMap** . Nota: este calificador no se puede invalidar. No es razonable permitir que una subclase devuelva un valor **null** diferente al de la clase primaria.

</dd> <dt>

<span id="Out"></span><span id="out"></span><span id="OUT"></span>**Enuncia**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: parámetros

Indica si el parámetro devuelve valores de un método. El valor predeterminado es **false**.

</dd> <dt>

<span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Estima**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, métodos, referencias

Clase primaria o construcción subordinada (propiedad, método o referencia) que es reemplazada por la propiedad, el método o la referencia del mismo nombre en la clase derivada. El valor predeterminado es **null**.

El formato es:

\[<> de *clase* . \] < *construcción subordinada*>

Si se omite el nombre de clase, la invalidación se aplica a la construcción subordinada en la clase primaria en la jerarquía de clases.

Uso: el calificador de **invalidación** puede hacer referencia a construcciones basadas solo en el mismo metamodelo. No se permite cambiar el nombre o la firma de una construcción durante una operación de invalidación.

</dd> <dt>

<span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**
</dt> <dd>

Se aplica a: clases

Indica si el valor de propiedad en una subclase invalida el valor de una clase primaria. La implicación funcional es que, si realiza una consulta en la clase primaria, y si la cláusula **Where** incluye esta propiedad, el elemento primario debe devolver una instancia de con el valor invalidado. Como resultado, la administración de Windows ajusta la cláusula **Where** de la consulta enviada a la clase primaria para excluir las referencias a esta propiedad.

</dd> <dt>

<span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagan**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades

Nombre de la clave que se va a propagar. El valor predeterminado es **null**.

El uso de este calificador supone la existencia de un solo calificador débil en una referencia que tiene la clase contenedora como su destino. La propiedad asociada debe tener el mismo valor que la propiedad denominada por el calificador de la clase en el otro lado de la Asociación débil. El formato es:

\[<> de *clase* . \] < *construcción subordinada*>

Uso: cuando se usa el calificador **propagado** , el calificador de [**clave**](key-qualifier.md) debe especificarse con un valor de **true**.

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>**Lectura**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica si la propiedad es legible. El valor predeterminado es **true**.

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Obligatorio**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica si se requiere un valor distinto de null para la propiedad. El valor predeterminado es **false**.

</dd> <dt>

<span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revisión**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases, asociaciones, indicaciones, esquemas

Número de revisión secundaria del objeto de esquema. El valor predeterminado es **null**.

Uso: el calificador de **versión** debe estar presente para proporcionar el número de versión principal cuando se use el calificador de **revisión** .

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Esquema**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, métodos

Nombre del esquema en el que se define la característica. El valor predeterminado es **null**.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Fuentes**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases, asociaciones, indicaciones, referencias

Ubicación de una instancia de. El valor predeterminado es **null**.

El valor del calificador es <*espacio*>://<*namespacehandle*>.

Uso: el calificador de **origen** no se puede usar con el calificador **sourceType** .

</dd> <dt>

<span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases, asociaciones, indicaciones, referencias

Tipo de ubicación de una instancia. El valor de este calificador es <*espacio*>. El valor predeterminado es **null**.

Uso: el calificador **sourceType** no se puede usar con el calificador de **origen** .

</dd> <dt>

<span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase admite la creación de instancias de. El valor predeterminado es **false**.

</dd> <dt>

<span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase admite la eliminación de instancias de. El valor predeterminado es **false**.

</dd> <dt>

<span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase admite la modificación (actualización) de instancias de. El valor predeterminado es **false**.

</dd> <dt>

<span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica si la clase puede tener subclases. El valor predeterminado es **false**.

Si se declara una subclase, el compilador genera un error.

Uso: este calificador no puede coexistir con el calificador **abstracto** . Si se especifican los calificadores de **terminal** y **abstractos** , el compilador genera un error.

</dd> <dt>

<span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Participa**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, métodos, parámetros

Tipo de unidad en la que se expresa el elemento de datos asociado. El valor predeterminado es **null**.

Por ejemplo, un elemento de datos de tamaño podría tener un valor de "bytes" para las **unidades**.

</dd> <dt>

<span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades, métodos, parámetros

Conjunto de valores permitidos para una propiedad, un tipo de valor devuelto de método o un parámetro de método. El valor predeterminado es **null**.

Uso: este calificador se puede usar por sí solo o en combinación con el calificador de **valores** . Cuando se usa en combinación con el calificador de **valores** , la ubicación del valor en la matriz **ValueMap** proporciona la ubicación de la entrada correspondiente en la matriz de **valores** . Use el calificador **ValueMap** solo con valores de cadena y enteros. La sintaxis para representar un valor entero en la matriz de mapa de valores es dígito digit \[ + \| = \] \[ \* \] . El contenido, el número máximo de dígitos y el valor representado están restringidos por el tipo de la propiedad asociada. Por ejemplo, Uint8 no puede estar firmado, debe tener menos de cuatro dígitos y debe representar un valor inferior a 256.

</dd> <dt>

<span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Valor**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades, métodos, parámetros

Conjunto de valores que traducen un valor entero en una cadena asociada. El valor predeterminado es **null**.

Esta propiedad también especifica una matriz de valores de cadena que se va a asignar a una propiedad de enumeración. Este calificador se puede aplicar a una propiedad de entero o a una propiedad de cadena, y la asignación puede ser implícita o explícita. Si la asignación es implícita, los valores de propiedad de cadena o entero representan las posiciones ordinales en la matriz de **valores** . Si la asignación es explícita, la propiedad debe ser un entero y los valores de propiedad válidos se muestran en la matriz definida por el calificador **ValueMap** . Para obtener más información, consulte [asignación de valores](value-map.md).

Si no hay ningún calificador **ValueMap** , la matriz **Values** está indizada (relativa a cero) mediante el valor de la propiedad asociada, el tipo de valor devuelto del método o el parámetro de método. Si hay un calificador **ValueMap** , el índice de valores se define mediante la ubicación del valor de propiedad en el mapa de valores.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versión**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases, esquemas, asociaciones, indicaciones

Número de versión principal del objeto de esquema. El valor predeterminado es **null**. El número de versión se incrementa cuando se realizan cambios en el esquema que modifica la interfaz.

</dd> <dt>

<span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Segura**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: referencias

Indica si las claves de la clase a la que se hace referencia incluyen las claves de los otros participantes de la asociación. El valor predeterminado es **false**.

Este calificador se utiliza cuando la identidad de la clase a la que se hace referencia depende de la identidad de los otros participantes de la asociación. No puede haber más de una referencia a una clase determinada. Las demás clases de la Asociación deben definir una clave. Las claves de las otras clases de la asociación se repiten en la clase a la que se hace referencia y se etiquetan con un calificador **propagado** .

</dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Escribi**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica que las aplicaciones o los scripts pueden cambiar el valor de la propiedad. La cuenta que ejecuta la aplicación debe tener acceso al espacio de nombres que contiene las instancias de la clase. La implementación del proveedor también puede limitar el acceso a los datos del proveedor. Un valor de **true** indica que la propiedad es legible y grabable por los consumidores a los que se les permite el acceso mediante WMI y el proveedor. El valor predeterminado es **false**.

Todavía es posible escribir en una propiedad que no tenga el calificador de **escritura** . La implementación del proveedor puede permitir que se modifiquen las propiedades de las clases del proveedor, tanto si el calificador de **escritura** está presente.

</dd> <dt>

<span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica si la propiedad es grabable en la creación de la instancia. Este calificador se puede usar junto con el calificador **WriteAtCreate** . El valor predeterminado es **false**.

</dd> <dt>

<span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica si la propiedad es grabable en la actualización de la instancia. Este calificador se puede usar junto con el calificador **WriteAtCreate** . El valor predeterminado es **false**.

</dd> </dl>

## <a name="examples"></a>Ejemplos

Para obtener más información sobre cómo recuperar calificadores, vea el ejemplo de código de PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) en la galería de TechNet.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Calificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Adición de un calificador](adding-a-qualifier.md)
</dt> </dl>

 

 




