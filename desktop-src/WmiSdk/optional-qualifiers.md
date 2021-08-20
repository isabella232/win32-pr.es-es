---
description: Los calificadores opcionales abordan situaciones periódicas no comunes a todas las implementaciones compatibles con CIM, que no son necesarias para interpretar estos calificadores.
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: Calificadores opcionales
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05cd80cbccf2c67baaeac2982c896a0c74ead227619bfb17517a039fadf24a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050543"
---
# <a name="optional-qualifiers"></a>Calificadores opcionales

Los calificadores opcionales abordan situaciones periódicas no comunes a todas las implementaciones compatibles con CIM, que no son necesarias para interpretar estos calificadores. En la especificación se proporcionan calificadores opcionales para evitar calificadores aleatorios definidos por el usuario que puedan producirse en estas situaciones periódicas.

<dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Eliminar**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: asociaciones, referencias

En el caso de las asociaciones, indica si se debe eliminar la asociación calificada si se elimina alguno de los objetos a los que se hace referencia en la asociación y si el objeto correspondiente al que se hace referencia en la asociación se califica con **IfDeleted**. El valor predeterminado es **FALSE.**

Para las referencias, este calificador indica si se debe eliminar el objeto al que se hace referencia si la asociación que contiene la referencia se elimina y se califica con **IfDeleted,** o si se elimina cualquiera de los objetos a los que se hace referencia en la asociación y el objeto correspondiente al que se hace referencia en la asociación se califica con **IfDeleted.**

Uso: las aplicaciones deben realizar un seguimiento de las asociaciones y las referencias marcadas con el **calificador Delete** y eliminar la asociación o referencia adecuadamente. Si se ha eliminado un objeto de la asociación pero no está marcado con **IfDeleted**, no se debe eliminar la asociación.

Esta regla de uso debe comprobarse cuando se define el modelo de seguridad CIM.

</dd> <dt>

<span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Caro**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades, referencias, clases, asociaciones, métodos

Indica si la acción implícita requiere un cálculo exhaustivo. El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: asociaciones y referencias

Indica si todos los objetos de una asociación calificados por **Delete** deben eliminarse si se elimina el objeto al que se hace referencia o la asociación. El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexadas**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades, métodos

Indica si se debe indexar una propiedad de clase. Cuando se aplica a las propiedades de las clases hospedadas por el repositorio, esto solo tiene el significado de crear (en el momento de la creación de clases) una búsqueda de consulta secundaria rápida para esa propiedad.

Solo se permite **el valor TRUE** (valor predeterminado).

</dd> <dt>

<span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisible**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: asociaciones, propiedades, métodos, referencias, clases

Indica si la asociación solo se define con fines internos (por ejemplo, para la definición de semántica de dependencia) y no debe mostrarse (por ejemplo, en mapas). El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Grande**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades, clases

Indica si la propiedad o clase requiere una gran cantidad de espacio de almacenamiento. El valor predeterminado es **FALSE.**

</dd> <dt>

<span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Not \_ Null**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica si una propiedad de clase no puede tomar un valor de **NULL** **(VT \_ NULL).** Solo se permite **el valor TRUE** (valor predeterminado).

Si se especifica este calificador, WMI no permite la creación de instancias con la propiedad establecida en **NULL** y las propiedades **NULL** devuelven el código de error **WBEM E \_ ILLEGAL \_ \_ NULL.**

Tenga en cuenta [**que los calificadores**](standard-qualifiers.md) Clave e **Indexado** ya implican este comportamiento.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Proveedor**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: Cualquiera

Indicación de que el elemento de esquema es dinámico y, por tanto, lo rellena un proveedor. El valor predeterminado es **NULL.** Este calificador es un identificador específico de la implementación de la instrumentación.

</dd> <dt>

<span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Experimental**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: cualquier

Indica que el elemento especificado se ha propuesto para formar parte de una versión futura de los esquemas CIM, pero aún no forma parte del esquema estándar. En su lugar, el elemento está disponible para que los usuarios experimenten, implementen y proporcionen comentarios sobre ellos. En función de los comentarios, el elemento puede agregarse al estándar tal como se presenta, modifica o quita. El valor predeterminado es **FALSE.** Una implementación no tiene que admitir un elemento con este calificador.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, referencias, métodos, parámetros

Tipo específico asignado a un elemento de datos. El valor predeterminado es **NULL.**

Uso: debe usar el calificador **SyntaxType** con este calificador.

</dd> <dt>

<span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, referencias, métodos, parámetros

Formato del **calificador de sintaxis.** El valor predeterminado es **NULL.**

Uso: debe usar el calificador **de sintaxis** con este calificador.

</dd> <dt>

<span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases, propiedades, métodos, asociaciones, indicaciones, referencias

Circunstancias en las que se desencadena un desencadenador. El valor predeterminado es **NULL.** Los tipos de desencadenador varían según la construcción del meta model.

Para las clases y asociaciones, los valores legales son:

Crear

Eliminar

Actualizar

Acceso

Para las propiedades y referencias, los valores legales son: Update y Access.

En el caso de los métodos , los valores legales son Before y After.

Para las indicaciones, el valor legal es Thrown.

</dd> <dt>

<span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades

Conjunto de valores que indican que el valor de la propiedad asociada es desconocido (no se puede considerar que la propiedad tiene un valor válido o significativo). El valor predeterminado es **NULL.**

Las convenciones y restricciones usadas para definir valores desconocidos son las mismas que las aplicables al [**calificador ValueMap.**](standard-qualifiers.md)

Tenga en cuenta que este calificador no se puede invalidar. No es razonable permitir que una subclase trate un valor como un valor conocido cuando alguna clase primaria lo trata como desconocido.

</dd> <dt>

<span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades

Conjunto de valores que indican que no se admite el valor de la propiedad asociada (no se puede considerar que la propiedad tiene un valor válido o significativo). El valor predeterminado es **NULL.**

Las convenciones y restricciones usadas para definir valores no admitidos son las mismas que las aplicables al [**calificador ValueMap.**](standard-qualifiers.md)

Tenga en cuenta que este calificador no se puede invalidar. No es razonable permitir que una subclase trate un valor como un valor admitido que alguna clase primaria trata como desconocido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Calificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Agregar un calificador](adding-a-qualifier.md)
</dt> </dl>

 

 




