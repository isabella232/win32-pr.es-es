---
title: Nivel de compatibilidad de esquema
description: En esta sección se tratan los detalles sobre el nivel de compatibilidad con esquemas.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Servicios Web de nivel de compatibilidad de esquemas para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104568212"
---
# <a name="schema-support-level"></a>Nivel de compatibilidad de esquema

En esta sección se tratan los detalles sobre el nivel de compatibilidad con esquemas.


El esquema admite directamente lo siguiente:

-   Secuencias de elementos.
-   Derivación de tipos de elemento.
-   Opciones sencillas de los elementos (los que se asignan a una Unión etiquetada).
-   Tipos básicos definidos por el formato binario XSD/.NET que incluye intervalos (min/max).
-   Compatibilidad simple con cualquier elemento (sin restricciones en el tipo de elemento).
-   Elementos y atributos opcionales con valores predeterminados.
-   Elementos repetidos con intervalos (min/max).
-   Elementos nillable.

El esquema no admite lo siguiente directamente (lo que implica el comportamiento de "reserva"):

-   Tipos básicos definidos por el usuario.
-   Opciones más complicadas.
-   Rechazar atributos desconocidos.
-   Ida y vuelta: atributos desconocidos.
-   Compatibilidad más complicada con cualquier elemento.
-   Construcción ALL.
-   Key/keyref.

A continuación se ofrece un desglose detallado de la compatibilidad de varios componentes de esquema. Se compara con el contrato de datos de WCF porque la similitud en la funcionalidad. Se describirá la diferencia.

Por lo general, para los comportamientos de reserva:

-   los atributos están respaldados en la \_ cadena WS;
-   el contenido del elemento se encuentra respaldado en el \_ búfer XML de WS \_ .
-   los complexType están respaldados en la estructura que contiene un campo de \_ búfer XML de WS \_ .
-   Los tipos simples se incluyen en la \_ cadena WS.

wsutil genera advertencias para los componentes de esquema que actualmente no se admiten por completo. Es posible que la aplicación tenga que realizar una comprobación adicional para que esos componentes sean necesarios. Se puede mejorar la wsutil de horas extras para controlar algunas de las características que se admiten actualmente en tiempo de ejecución, como la compatibilidad con valores predeterminados. wsutil también se puede mejorar junto con la serialización para admitir otras características como Abstract. El número de componentes de esquema no admitidos puede reducirse con el tiempo.

## <a name="the-overall-schema-document"></a>Documento de esquema general

Definición global que puede afectar a las definiciones incrustadas en el esquema. Son atributos globales que se aplican a todas las definiciones del esquema.

Atributos <XS: Schema>

-   attributeFromDefault omitido.
-   se omitió blockDefault.
-   elementFormDefault omitido. Esto es diferente de DataContract, ya que se admiten elementos incompletos en tiempo de ejecución.
-   no se ha pasado el finalDefault. No hay compatibilidad con el lenguaje C para el concepto de final.
-   identificador omitido.
-   targetNamespace se admite y se asigna al espacio de nombres de servicio.
-   versión omitida.

<XS: Schema> contenido

-   incluye compatible; wsutil requiere que todas las definiciones necesarias estén disponibles como archivos de entrada durante el tiempo de compilación.
-   redefinición omitida. wsutil no lo admite.
-   importación admitida; wsutil requiere que todas las definiciones necesarias estén disponibles como archivos de entrada durante el tiempo de compilación.
-   Compatible con simpleType; vea la sección de tipo simple a continuación.
-   complexType compatible: Consulte la sección ' complexType '
-   Grupo omitido.
-   attributeGroup omitido.
-   elemento compatible; asigna a definiciones de elementos globales.
-   atributo admitido; asigna a definiciones de atributos globales.
-   notación omitida

## <a name="complex-type"></a>Tipo complejo

El tipo complejo, representado por <XS: complexType>, podría ser una restricción del tipo simple o tipo complejo, la extensión de tipo simple, matrices o estructura. Observe que, en la extensión de los tipos simples, no hay ninguna herencia ni compatibilidad con xsi: Type.

Atributos de> <XS: complexType

-   Resumen de generación de advertencia sobre característica no admitida, sin cambios en la generación de código.
-   bloquear generar Advertencia sobre característica no admitida, sin cambios en la generación de código.
-   última generación de advertencia acerca de la característica no admitida, sin cambios en la generación de código.
-   identificador omitido.
-   mixed genera una advertencia sobre la característica no admitida, reserva a la estructura con el búfer de WS \_ XML \_ si es true.
-   nombre admitido y asignado al nombre del tipo de estructura.

<el contenido de> XS: complexType

Esta es la definición de tipo de la estructura. no se admite la restricción complexContent.

-   complexContent admite la extensión de contenido complejo. Asigna a la herencia de la estructura.
-   Agrupe actualmente la reserva en la estructura con el \_ campo de búfer XML de WS \_ . Se puede admitir según la partícula subyacente.
-   elección admitida como Unión. Esto no se admite en el contrato de datos.
-   Sequence Supported: se asigna a los campos de una estructura
-   atributo compatible con una excepción de ' prohibido '. Reserva para la estructura con el \_ búfer XML de WS \_ si está prohibido.
-   attributeGroup compatible: se asigna a la secuencia de atributos
-   anyAttribute omitido
-   AttributeGroupRef admitido: se asigna a la secuencia de atributos.
-   GroupRef actualmente se reserva en la estructura con el \_ campo de búfer XML de WS \_ . Se puede admitir según el grupo subyacente.
-   Cualquier mapa compatible, se asigna a un \_ búfer XML
-   (en blanco) se admite la asignación a una descripción de struct vacía sin ninguna estructura generada.

<xs:sequence> en un tipo complejo: contenido

wsutil solo admite totalmente la secuencia de minOccurs = 1 y maxOccurs = 1; de lo contrario, el tipo complejo se encuentra actualmente respaldado por el \_ búfer XML de WS \_ . Se puede admitir como una matriz de estructuras.

-   elemento compatible; cada instancia se asigna a un campo de la estructura.
-   Reserva de grupo; complexType es fallback en el \_ búfer XML de WS \_ .
-   Toda la reserva; complexType es fallback en el \_ búfer XML de WS \_ .
-   elección admitida; asignar a campo de Unión.
-   Reserva de secuencia; complexType es fallback en el \_ búfer XML de WS \_ .
-   cualquier compatible; asignado a \_ búfer XML.
-   (en blanco) admitido; complexType puede ser una estructura vacía si no hay ningún atributo.

## <a name="elements"></a>Elementos

<XS: Element>pueden aparecer en tres contextos.

-   Puede producirse dentro de una <XS: Sequence>, que describe un campo de un struct normal. En este caso, el atributo maxOccurs debe ser 1. El campo es opcional si minOccurs es 0.
-   Puede producirse dentro de una <XS: Sequence>, que describe un campo de una matriz. En este caso, el atributo maxOccurs debe ser mayor que 1 o "ilimitado".
-   Puede producirse dentro de una <XS: Schema> como una descripción de elemento global.

<> XS: Element dentro de un <XS: Sequence> o <XS: Choice> como un campo en una estructura

-   referencia admitida; se resuelve como una referencia a un elemento global.
-   nombre admitido, se asigna al nombre del campo.
-   tipo admitido, se asigna al tipo de campo. Para obtener más información, vea ' asignación de tipos '. Si no se especifica (y el elemento no contiene un tipo anónimo), se supone XS: anyType.
-   bloquear generar Advertencia sobre característica no admitida, sin cambios en la generación de código.
-   Generar ADVERTENCIA predeterminada sobre la característica no admitida, sin cambios en la generación de código.
-   se corrigió la advertencia generada sobre la característica no admitida, sin cambios en la generación de código.
-   formulario omitido. Nuestra capa de serialización admite formularios completos e incompletos.
-   identificador omitido.
-   maxOccurs se asigna a un único campo de datos si es igual a 1. se asigna a un campo de matriz (elemento repetitivo) si maxOccurs es mayor que 1.
-   minOccurs si es 0, las opciones de campo se establecen en campo \_ opcional, si no se establece nillable.
-   nillable el campo es nillable. Vea [serialización](serialization.md) para obtener más detalles.

<XS: Element> como elemento global: Attributes

los atributos minOccurs y maxOccurs no son válidos como descripción de elementos globales. La aplicación puede usar la descripción de elementos generados directamente en capas de canal o de nivel de serialización.

-   Resumen de generación de advertencia sobre característica no admitida, sin cambios en la generación de código.
-   bloquear generar Advertencia sobre característica no admitida, sin cambios en la generación de código.
-   Generar ADVERTENCIA predeterminada sobre la característica no admitida, sin cambios en la generación de código.
-   última generación de advertencia acerca de la característica no admitida, sin cambios en la generación de código.
-   se corrigió la advertencia generada sobre la característica no admitida, sin cambios en la generación de código.
-   identificador omitido.
-   Name Supported: asignar al nombre de la descripción del elemento global y es la base para el tipo anónimo cuando se especifica.
-   se omitieron los nillable: la aplicación debe llamar a con la marca derecha.
-   Reserva de substitutionGroup en la estructura con el búfer de WS \_ XML \_ si está establecido. wsutil no admite substitutionGroup.
-   Escriba compatible y asígnelo al tipo del elemento.

<XS: Element> como elemento global: Contents

-   simpleType compatible; asigna a la definición de tipo.
-   complexType compatible; se asigna a un tipo complejo.
-   Unique genera una advertencia sobre la característica no admitida, sin cambios en la generación de código. wsutil no admite restricciones Element.
-   clave genera una advertencia sobre la característica no admitida, sin cambios en la generación de código. wsutil no admite restricciones Element.
-   keyref genera una advertencia sobre la característica no admitida, sin cambios en la generación de código. wsutil no admite restricciones Element.
-   en blanco Realizar el elemento sin especificación de tipo se trata como XS: anyType.

## <a name="simple-types"></a>Tipos simples

<atributos> XS: simpleType

-   Última generación de advertencia acerca de la característica no admitida, sin cambios en la generación de código.
-   Identificador omitido
-   Nombre admitido, se asigna al nombre de tipo.

<el contenido de> XS: simpleType

-   Restricción admitida, se asigna al tipo de enumeración o intervalo. Vea la sección "restricciones XS: simpleType".
-   List generar Advertencia sobre la característica no admitida, reserva a \_ búfer XML.
-   La Unión genera una advertencia sobre la característica no admitida, reserva a \_ búfer XML.

## <a name="simple-type-restriction"></a>Restricción de tipo simple

Se permiten ciertas caras en tipos enteros y cadenas de tipo para permitir la compatibilidad con el intervalo y la enumeración.

compatibilidad de enumeración

<XS: Enumeration> restricción de tipo simple para el tipo base de cadena se trata como tipo de enumeración. En este caso, el atributo base debe ser de tipo cadena. En el caso de la enumeración, se omiten todas las demás caras.

intervalo en compatibilidad con tipos simples

Algunas de las caras son compatibles con los tipos simples, lo que permite un intervalo eficaz permitido en el tipo. A continuación se enumeran las restricciones para los tipos enteros y los tipos float/double. Los tipos simples con otras caras se incluyen en el tipo de \_ cadena WS

-   minExclusive compatible
-   minInclusive compatible
-   maxExclusive compatible
-   maxInclusive compatible
-   totalDigits genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   fractionDigits genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   la longitud genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   minLength genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   maxLength generar Advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   la enumeración genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   el espacio en blanco genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   patrón generar Advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   en blanco Realizar.

en la actualidad, minLength y maxLength en una cadena no se admiten, pero es una característica deseable para admitir.

## <a name="inheritance"></a>Herencia

Wsutil admite la herencia de tipos complejos, es decir, una estructura puede heredar de otra estructura, similar a la herencia de interfaces en C++. Esto se hace a través de <> XS: complexContentExtension. Se admite <> XS: simpleContentExtension, pero se genera como una estructura sin formato con el tipo base como primer campo en lugar de herencia de tipos.

## <a name="typeprimitive-mapping"></a>Asignación de tipo/primitivo.

Los identificadores deben normalizarse al traducir de NCName en XML. Las cadenas son nillable; los tipos de puntero son nillable; los tipos enteros y float/double son nillable y defaultValue se establece en 0.

![Tabla que muestra la asignación entre los tipos XSD y los tipos de datos Sapphire.](images/schematypemap.png)

 

 




