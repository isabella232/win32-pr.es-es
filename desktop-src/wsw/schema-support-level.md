---
title: Nivel de compatibilidad del esquema
description: En esta sección se tratan los detalles sobre el nivel de compatibilidad con esquemas.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Servicios web de nivel de compatibilidad de esquema para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360904"
---
# <a name="schema-support-level"></a>Nivel de compatibilidad del esquema

En esta sección se tratan los detalles sobre el nivel de compatibilidad con esquemas.


El esquema admite directamente lo siguiente:

-   Secuencias de elementos.
-   Derivación de tipos de elemento.
-   Opciones sencillas de elementos (las que se asignan a una unión etiquetada).
-   Tipos básicos definidos por el formato binario XSD/.NET, incluidos los intervalos (mín./máx.).
-   Compatibilidad sencilla con cualquier elemento (sin restricciones en el tipo de elemento).
-   Elementos y atributos opcionales con valores predeterminados.
-   Repetir elementos con intervalos (min/max).
-   Elementos Nillable.

El esquema no admite directamente lo siguiente (lo que implica el comportamiento de "reserva"):

-   Tipos básicos definidos por el usuario.
-   Opciones más complicadas.
-   Rechazar atributos desconocidos.
-   Atributos desconocidos de ida y vuelta.
-   Compatibilidad más complicada con cualquier elemento.
-   La construcción all.
-   Key/keyref.

A continuación se muestra un desglose detallado de la compatibilidad con diferentes componentes de esquema. Se compara con el contrato de datos en WCF debido a la similitud en la funcionalidad. Se describirá la diferencia.

Por lo general, para los comportamientos de reserva:

-   Los atributos se reservan a WS \_ STRING;
-   El contenido del elemento se reserva al búfer XML de \_ \_ WS.
-   complexType se reservan a la estructura que contiene un campo de BÚFER XML de \_ \_ WS.
-   Los tipos simples se reservan a WS \_ STRING.

wsutil genera advertencias para los componentes de esquema que no son totalmente compatibles actualmente. Es posible que la aplicación tenga que realizar una comprobación adicional para esos componentes. Wsutil de tiempo extra se puede mejorar para controlar algunas de las características que se admiten actualmente en tiempo de ejecución, como la compatibilidad con valores predeterminados. wsutil también se puede mejorar junto con la serialización para admitir otras características como abstract. El número de componentes de esquema no admitidos se puede reducir con el tiempo.

## <a name="the-overall-schema-document"></a>Documento de esquema general

Definición global que podría afectar a las definiciones incrustadas en el esquema. Se trata de atributos globales que se aplican a todas las definiciones del esquema.

<xs:schema> atributos

-   attributeFromDefault Omitido.
-   blockDefault Omitido.
-   elementFormDefault Omitido. Esto es diferente de dataContract, ya que los elementos no calificados se admiten en tiempo de ejecución.
-   finalDefault Omitido. No hay compatibilidad con el lenguaje C para el concepto de final.
-   id Omitido.
-   targetNamespace Compatible y asignado al espacio de nombres del servicio.
-   versión omitido.

<xs:schema> contenido

-   include Supported; wsutil requiere que toda la definición necesaria esté disponible como archivos de entrada durante el tiempo de compilación.
-   redefinir Omitido. wsutil no admite esto.
-   import Supported; wsutil requiere que toda la definición necesaria esté disponible como archivos de entrada durante el tiempo de compilación.
-   simpleType Compatible: consulte la sección de tipo simple a continuación.
-   complexType Supported: consulte la sección "complexType".
-   group Ignored.
-   attributeGroup omitido.
-   element Supported; se asigna a definiciones de elementos globales.
-   attribute Supported; se asigna a definiciones de atributos globales.
-   notation Ignored

## <a name="complex-type"></a>Tipo complejo

El tipo complejo, representado por <xs:complexType>, podría ser una restricción de tipo simple o tipo complejo, extensión de tipo simple, matrices o estructura. Hemos observado que, en la extensión de tipos simples, no hay herencia ni compatibilidad con xsi:type.

<xs:complexType> atributos

-   abstract Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   block Genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   final Genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   id Omitido.
-   mixto Genera una advertencia sobre la característica no admitida, reserva a la estructura con WS \_ XML BUFFER si es \_ true.
-   name Compatible y asignado al nombre del tipo de estructura.

<xs:complexType> contenido

Esta es la definición de tipo para structure. No se admite la restricción complexContent.

-   complexContent Admite la extensión de contenido complejo. Mapas estructurar la herencia.
-   group Reserva actualmente a la estructura con el campo \_ BÚFER XML de WS. \_ Se puede usar según la partícula subyacente.
-   opción admitida como unión. Esto no se admite en el contrato de datos.
-   sequence Supported: se asigna a campos de una estructura
-   Se admite el atributo con una excepción de "prohibido". reserva a la estructura con WS \_ XML BUFFER si está \_ "prohibido".
-   attributeGroup compatible: se asigna a la secuencia de atributos
-   anyAttribute omitido
-   AttributeGroupRef compatible: se asigna a la secuencia de atributos.
-   GroupRef Actualmente se reserva a la estructura con el campo \_ BÚFER XML de WS. \_ Puede ser compatible según el grupo subyacente.
-   Cualquier compatible, se asigna a BÚFER \_ XML
-   (en blanco) se admite la asignación a una descripción de struct vacía sin ningún struct generado.

<xs:sequence> en un tipo complejo: contenido

wsutil solo admite completamente la secuencia de minOccurs = 1 y maxOccurs = 1; De lo contrario, el tipo complejo se reserva actualmente al búfer XML de \_ \_ WS. Se puede admite como matriz de estructuras.

-   element Supported; cada instancia se asigna a un campo de la estructura .
-   Reserva de grupo; complexType es una reserva para WS \_ XML \_ BUFFER.
-   Toda la reserva; complexType es una reserva para WS \_ XML \_ BUFFER.
-   opción admitida; asignar al campo de unión.
-   reserva de secuencia; complexType es una reserva para WS \_ XML \_ BUFFER.
-   cualquier compatible; asignado a XML \_ BUFFER.
-   (en blanco) admitido; complexType puede ser una estructura vacía si no hay atributos.

## <a name="elements"></a>Elementos

<xs:element>pueden producirse en tres contextos.

-   Puede producirse dentro de un <xs:sequence> describe un campo de una estructura normal. En este caso, el atributo maxOccurs debe ser 1. El campo es opcional si minOccurs es 0.
-   Puede producirse dentro de un <xs:sequence>, que describe un campo de una matriz. En este caso, el atributo maxOccurs debe ser mayor que 1 o "sin enlazar".
-   Puede producirse dentro de un <xs:schema> como una descripción de elemento global.

<xs:element> dentro de un <xs:sequence> o <xs:choice> como un campo en una estructura

-   ref Supported; se resolvió para hacer referencia al elemento global.
-   name Supported, se asigna al nombre del campo.
-   tipo Compatible, se asigna al tipo de campo. Para obtener más información, vea "Asignación de tipos". Si no se especifica (y el elemento no contiene un tipo anónimo), se supone xs:anyType.
-   bloquear Generación de advertencias sobre características no admitidas, sin cambios en la generación de código.
-   valor predeterminado Generar advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   se ha corregido Generación de una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   form Ignored. Nuestra capa de serialización admite formularios calificados y no calificados.
-   Id Omitido.
-   maxOccurs se asigna a un solo campo de datos si es igual a 1. se asigna a un campo de matriz (elemento de repetición) si maxOccurs es mayor que 1.
-   minOccurs si es 0, las opciones de campo se establecen en FIELD OPTIONAL, si no se establece \_ nillable.
-   nillable El campo es nillable. Consulte [Serialización para](serialization.md) obtener más detalles.

<xs:element> como elemento global: atributos

Los atributos minOccurs y maxOccurs no son válidos como descripción del elemento global. La aplicación puede usar la descripción del elemento generado en capas de serialización o capas de canal directamente.

-   abstract Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   bloquear Generación de advertencias sobre características no admitidas, sin cambios en la generación de código.
-   valor predeterminado Generar advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   final Generar advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   se ha corregido Generación de una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   Id Omitido.
-   name Supported: se asigna al nombre de la descripción del elemento global y es la base del tipo anónimo cuando se especifica.
-   Nillable Ignored-application debe llamar a con la marca right.
-   substitutionGroup reserva a la estructura con WS \_ XML BUFFER si se \_ establece. wsutil no admite substitutionGroup.
-   escriba Supported y asigne al tipo del elemento.

<xs:element> como elemento global: contenido

-   simpleType compatible; se asigna a la definición de tipo.
-   complexType compatible; se asigna a un tipo complejo.
-   unique Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código. wsutil no admite restricciones de elementos.
-   key Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código. wsutil no admite restricciones de elementos.
-   keyref Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código. wsutil no admite restricciones de elementos.
-   (en blanco) Compatible; El elemento sin especificación de tipo se trata como xs:anyType.

## <a name="simple-types"></a>Tipos simples

<xs:simpleType> atributos

-   Última generación de advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   Identificador omitido
-   Nombre admitido, se asigna al nombre de tipo.

<contenido de> xs:simpleType

-   Restricción admitida, se asigna al tipo de enumeración o al intervalo. Consulte la sección "xs:simpleType restrictions" (restricciones de xs:simpleType).
-   Lista Generar advertencia sobre la característica no admitida, reserva a BÚFER \_ XML.
-   Unión Genera una advertencia sobre la característica no admitida, reserva a XML \_ BUFFER.

## <a name="simple-type-restriction"></a>Restricción de tipo simple

Se permiten ciertas facetas en tipos enteros y tipos de cadenas para permitir la compatibilidad con intervalos y enumeraciones.

compatibilidad con enumeración

<xs:enumeration> restricción de tipo simple para el tipo base de cadena se trata como tipo de enumeración. En este caso, el atributo Base DEBE ser de tipo cadena. En el caso de enumeración, se omiten todas las demás facetas.

range en compatibilidad con tipos simples

Algunas facetas son compatibles con tipos simples que admiten un intervalo eficaz permitido en el tipo. A continuación se muestra una restricción para los tipos enteros y los tipos float/double. Los tipos simples con otras facetas se reservan al tipo STRING de WS \_

-   minExclusive compatible
-   minInclusive compatible
-   maxExclusive compatible
-   maxInclusive compatible
-   totalDigits Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   fractionDigits Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   length Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   minLength Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   maxLength Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   enumeración Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   whiteSpace Genere una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   patrón Genera una advertencia sobre la característica no admitida, sin cambios en la generación de código.
-   (en blanco) Apoyado.

minLength y maxLength en la cadena no se admiten actualmente, pero es una característica deseable para admitir.

## <a name="inheritance"></a>Herencia

Wsutil admite la herencia de tipos complejos, es decir, una estructura puede heredar de otra estructura, similar a la herencia de interfaz en C++. Esto se realiza mediante <xs:complexContentExtension>. <xs:simpleContentExtension> se admite, pero se genera como estructura sin formato con el tipo base como primer campo en lugar de la herencia de tipos.

## <a name="typeprimitive-mapping"></a>Asignación de tipo/primitivo.

Los identificadores deben normalizarse al traducir desde NCNames en XML. Las cadenas son nillables; Los tipos de puntero son nillables; Los tipos enteros y float/double son nillable y defaultValue se establece en 0.

![Tabla en la que se muestra la asignación entre los tipos XSD y los tipos de datos Desfila.](images/schematypemap.png)

 

 




