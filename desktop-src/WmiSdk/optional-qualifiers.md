---
description: Los calificadores opcionales abordan situaciones recurrentes que no son comunes a todas las implementaciones compatibles con CIM, que no son necesarias para interpretar estos calificadores.
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
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707209"
---
# <a name="optional-qualifiers"></a>Calificadores opcionales

Los calificadores opcionales abordan situaciones recurrentes que no son comunes a todas las implementaciones compatibles con CIM, que no son necesarias para interpretar estos calificadores. Se proporcionan calificadores opcionales en la especificación para evitar calificadores definidos por el usuario aleatorios que puedan producirse en estas situaciones recurrentes.

<dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Elimínelos**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: asociaciones, referencias

En el caso de las asociaciones, indica si se debe eliminar la Asociación calificada si se elimina cualquiera de los objetos a los que se hace referencia en la asociación y si el objeto correspondiente al que se hace referencia en la asociación está calificado con **IfDeleted**. El valor predeterminado es **false**.

En el caso de las referencias, este calificador indica si el objeto al que se hace referencia debe eliminarse si la asociación que contiene la referencia se elimina y se califica con **IfDeleted**, o si se elimina cualquiera de los objetos a los que se hace referencia en la asociación y el objeto al que se hace referencia en la asociación está calificado con **IfDeleted**.

Uso: las aplicaciones deben realizar un seguimiento de las asociaciones y las referencias marcadas con el calificador de **eliminación** y eliminar la asociación o la referencia de forma adecuada. Si se ha eliminado un objeto de la asociación, pero no está marcado con **IfDeleted**, no se debe eliminar la asociación.

Esta regla de uso debe comprobarse cuando se define el modelo de seguridad de CIM.

</dd> <dt>

<span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Alto**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades, referencias, clases, asociaciones, métodos

Indica si la acción implícita requiere un cálculo extensivo. El valor predeterminado es **false**.

</dd> <dt>

<span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: asociaciones y referencias

Indica si se deben eliminar todos los objetos dentro de una asociación que califique por **Delete** si se elimina el objeto al que se hace referencia o la asociación. El valor predeterminado es **false**.

</dd> <dt>

<span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indizó**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades, métodos

Indica si se debe indizar una propiedad de clase. Cuando se aplica a las propiedades de las clases hospedadas por el repositorio, solo tiene el significado de crear (en el momento de crear la clase) una búsqueda rápida de consultas secundarias para esa propiedad.

Solo se permite el valor **true** (predeterminado).

</dd> <dt>

<span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Ve**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: asociaciones, propiedades, métodos, referencias, clases

Indica si la asociación se define solo para fines internos (por ejemplo, para la definición de la semántica de dependencia) y no debe mostrarse (por ejemplo, en Maps). El valor predeterminado es **false**.

</dd> <dt>

<span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Amplíe**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades, clases

Indica si la propiedad o la clase requieren una gran cantidad de espacio de almacenamiento. El valor predeterminado es **false**.

</dd> <dt>

<span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**No \_ null**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: propiedades

Indica si una propiedad de clase no puede tomar un valor **null** (**VT \_ null**). Solo se permite el valor **true** (predeterminado).

Si se especifica este calificador, WMI no permite la creación de instancias con la propiedad establecida en **null** y las propiedades **null** devuelven el código de error **null de WBEM \_ e \_ no válido \_** .

Tenga en cuenta que la [**clave**](standard-qualifiers.md) y los calificadores **indizados** ya implican este comportamiento.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Presta**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: any

Indica que el elemento de esquema es dinámico y, por tanto, lo rellena un proveedor. El valor predeterminado es **null**. Este calificador es un identificador específico de la implementación para la instrumentación.

</dd> <dt>

<span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Ensayo**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: any

Indica que se ha propuesto que el elemento especificado forme parte de una versión futura de los esquemas CIM, pero que aún no forma parte del esquema estándar. En su lugar, el elemento está disponible para que los usuarios experimenten, implementen y proporcionen comentarios sobre. En función de los comentarios, el elemento se puede Agregar al estándar como se presenta, se modifica o se quita. El valor predeterminado es **false**. Una implementación de no tiene que admitir un elemento con este calificador.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, referencias, métodos, parámetros

Tipo específico asignado a un elemento de datos. El valor predeterminado es **null**.

Uso: debe usar el calificador **SyntaxType** con este calificador.

</dd> <dt>

<span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: propiedades, referencias, métodos, parámetros

Formato del calificador de **Sintaxis** . El valor predeterminado es **null**.

Uso: debe utilizar el calificador de **Sintaxis** con este calificador.

</dd> <dt>

<span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases, propiedades, métodos, asociaciones, indicaciones, referencias

Circunstancias en las que se activa un desencadenador. El valor predeterminado es **null**. Los tipos de desencadenador varían según la construcción de metamodelo.

En el caso de las clases y asociaciones, los valores válidos son:

Crear

Eliminar

Actualizar

Access

En el caso de las propiedades y referencias, los valores válidos son: Update y Access.

En el caso de los métodos, los valores válidos son Before y after.

En el caso de las indicaciones, se produce el valor legal.

</dd> <dt>

<span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades

Conjunto de valores que indican que el valor de la propiedad asociada es desconocido (la propiedad no se puede considerar como si tuviera un valor válido o significativo). El valor predeterminado es **null**.

Las convenciones y restricciones que se usan para definir valores desconocidos son las mismas que las aplicables al calificador [**ValueMap**](standard-qualifiers.md) .

Tenga en cuenta que este calificador no se puede invalidar. No es razonable permitir que una subclase trate un valor como un valor conocido cuando alguna clase primaria lo trata como desconocido.

</dd> <dt>

<span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades

Conjunto de valores que indican que el valor de la propiedad asociada no se admite (la propiedad no se puede considerar como si tuviera un valor válido o significativo). El valor predeterminado es **null**.

Las convenciones y restricciones que se usan para definir valores no admitidos son las mismas que las aplicables al calificador [**ValueMap**](standard-qualifiers.md) .

Nota: este calificador no se puede invalidar. No es razonable permitir que una subclase trate un valor como un valor admitido que alguna clase primaria trata como desconocido.

</dd> </dl>

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

 

 




