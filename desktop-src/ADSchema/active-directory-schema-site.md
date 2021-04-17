---
title: Terminología de esquemas Active Directory
description: Los siguientes términos se utilizan normalmente para hacer referencia al esquema de Active Directory.
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efca7057a79d87c45cc3e3da4b604e842143fedd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105656441"
---
# <a name="active-directory-schema-terminology"></a>Terminología de esquemas Active Directory

Los siguientes términos se utilizan normalmente para hacer referencia al esquema de Active Directory.


<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atribui
</dt> <dd>

Elementos de datos utilizados para describir los objetos representados por las clases que se definen en el esquema. Los atributos se definen en el esquema de forma independiente de las clases; Esto permite aplicar una definición de un solo atributo a muchas clases. Por ejemplo, la [**Descripción**](a-description.md) es un atributo que se puede aplicar a cualquier clase del esquema. El atributo **Description** se define una vez en el esquema, lo que garantiza la coherencia, en lugar de tener una definición diferente para la **Descripción** de un usuario y la **Descripción** de una impresora.

> [!Note]  
> La *propiedad* term se usa con frecuencia indistintamente con el término *Attribute*.

 

</dd> <dt>

<span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Instancia de atributo
</dt> <dd>

Instancia de un atributo que se define en el esquema. Este término se usa para distinguir entre la definición de un atributo y una repetición discreta del atributo. Por ejemplo, si se almacena un objeto de usuario para "Jeff Smith" con el atributo [**common-name**](a-cn.md) establecido en "Jeff Smith", se crea una instancia de [**common-name**](a-cn.md).

</dd> <dt>

<span id="Class"></span><span id="class"></span><span id="CLASS"></span>Las
</dt> <dd>

Una descripción formal de un tipo discreto e identificable de un objeto almacenado en el servicio de directorio. Por ejemplo, el [**usuario**](c-user.md), [**la cola de impresión y el**](c-printqueue.md) [**Grupo**](c-group.md) son todas las clases. Además, hay 3 categorías distintas de clases: [clases estructurales](classes-structural.md), [clases abstractas](classes-abstract.md)y [clases auxiliares](classes-auxiliary.md).

</dd> <dt>

<span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Instancia de clase
</dt> <dd>

Una aparición de una clase que se define en el esquema. Este término se usa para distinguir entre la definición de una clase y una instancia discreta de la clase. Por ejemplo, si se almacena un objeto de [**usuario**](c-user.md) para "Jeff Smith" en el servicio de directorio, se crea una instancia del [**usuario**](c-user.md).

</dd> <dt>

<span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Reglas de contenido
</dt> <dd>

La definición del posible contenido de las instancias de clase que se almacenan en el servicio de directorio. En los servicios de directorio de NT (NTDS), en los que se basa Active Directory, las reglas de contenido se expresan por completo en los atributos [**debe contener**](a-mustcontain.md) y [**puede contener**](a-maycontain.md) de las definiciones de esquema para cada clase.

</dd> <dt>

<span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Deriva
</dt> <dd>

Vea *herencia*.

</dd> <dt>

<span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Árbol de información de directorio
</dt> <dd>

El propio directorio, representado como una estructura de árbol en la que los vértices son las entradas de directorio (instancias de clase) y las líneas de conexión que las relaciones de elementos primarios y secundarios entre las entradas.

</dd> <dt>

<span id="DIT"></span><span id="dit"></span>PARTICIONA
</dt> <dd>

Vea *árbol de información de directorio*.

</dd> <dt>

<span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Derechos de acceso de control
</dt> <dd>

Una clase que describe un derecho de acceso que no está asociado a un recurso, sino una acción. Por ejemplo, se puede conceder a un usuario el derecho a crear valores de identificador relativos.

</dd> <dt>

<span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Ella
</dt> <dd>

La capacidad de crear nuevas clases de objeto a partir de clases de objeto existentes. El nuevo objeto se define como una *subclase* del objeto primario. El objeto primario se convierte en una *superclase* del nuevo objeto. Una subclase hereda los atributos del elemento primario, incluidas las reglas de estructura y las reglas de contenido.

</dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>LDAP
</dt> <dd>

Consulte *Protocolo ligero de acceso a directorios*.

</dd> <dt>

<span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Protocolo ligero de acceso a directorios
</dt> <dd>

Protocolo estándar de comunicaciones de Internet que se usa para comunicarse con NTDS. Se admiten las versiones 2 y 3 de LDAP.

</dd> <dt>

<span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>Descriptor de seguridad de NT
</dt> <dd>

Consulte *descriptor de seguridad*.

</dd> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Objeto
</dt> <dd>

Unidad de almacenamiento de datos en el servicio de directorio. Los objetos de servicio de directorio no se deben confundir con objetos COM u otros objetos del sistema orientados a objetos, que tienen un componente ejecutable y un comportamiento en tiempo de ejecución. Los objetos de servicio de directorio solo se componen de datos. Un objeto de servicio de directorio se define mediante un objeto de [**esquema de clase**](c-classschema.md) y un grupo de objetos de [**esquema de atributos**](c-attributeschema.md) a los que hace referencia el objeto de esquema de [**clase**](c-classschema.md) .

Los objetos de esquema de [**clase**](c-classschema.md) y [**de esquema de atributo**](c-attributeschema.md) son objetos de servicio de directorio y tienen definiciones en el esquema como cualquier otro objeto. Vea la *clase*.

</dd> <dt>

<span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Identificador de objeto
</dt> <dd>

Valores numéricos únicos, emitidos por varias autoridades emisoras, para identificar de forma única los elementos de datos, las sintaxis y otras partes de las aplicaciones distribuidas. Los identificadores de objeto (OID) se encuentran en las aplicaciones OSI, los directorios X. 500, el SNMP y otras aplicaciones en las que la unicidad es importante. Los OID se basan en una estructura de árbol, en la que una entidad de emisión superior, como la ISO, asigna una rama del árbol a una subentidad, que a su vez puede asignar subbifurcaciones.

Los OID de NTDS incluyen algunos emitidos por la ISO para las clases y atributos X. 500 y otros emitidos por Microsoft. La notación OID es una cadena de números con puntos, por ejemplo "1.2.840.113556.1.5.4", que se traduce como se muestra en la lista siguiente. 

| Value  | Descripción                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| 1      | ISO: la "entidad de certificación raíz", emitida "1,2" a ANSI, que, a su vez,...                           |
| 2      | ANSI... se emitió "1.2.840" a EE. UU., que, a su vez,...                                            |
| 840    | ESTADOS UNIDOS... se emitió "1.2.840.113556" a Microsoft...                                               |
| 113556 | Microsoft... donde Microsoft administra internamente varias ramas OID en "1.2.840.113556". |
| 1      | Microsoft DS                                                                                 |
| 5      | Clases NTDS                                                                                 |
| 4      | Builtin-Domain                                                                               |



 

</dd> <dt>

<span id="OID"></span><span id="oid"></span>OID
</dt> <dd>

Vea *identificador de objeto*.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Esquema
</dt> <dd>

Una definición formal de la estructura y el contenido del servicio de directorio. El esquema define todos los atributos y las clases. Para cada clase, se definen los atributos [**Poss-superior**](a-posssuperiors.md), [**debe contener**](a-mustcontain.md)y [**puede-contener**](a-maycontain.md) . [**Poss:**](a-posssuperiors.md) define las posibles estructuras de árbol para el servicio de directorio mediante la especificación de las clases que pueden ser el elemento primario de cualquier clase dada. [**Debe contener**](a-mustcontain.md) la lista y [**puede contener**](a-maycontain.md) los atributos de una clase que debe estar presente para almacenar la clase y los atributos adicionales que pueden estar presentes opcionalmente.

</dd> <dt>

<span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Descriptor de seguridad
</dt> <dd>

Información sobre la propiedad de un objeto y los permisos que otros usuarios tienen en ese objeto. La propiedad [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) de una entrada de esquema contiene una cadena que representa el descriptor de seguridad del objeto. Para obtener más información sobre el formato de la información de este campo, vea [formato de cadena de descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-string-format).

</dd> <dt>

<span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Reglas de estructura
</dt> <dd>

La definición de la estructura o estructuras de árbol posibles. En NTDS, las reglas de la estructura se expresan completamente mediante el atributo Poss-superior presente en cada objeto [**de esquema de clase**](c-classschema.md) . Vea *esquema*.

</dd> <dt>

<span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclase
</dt> <dd>

Objeto de [**esquema de clase**](c-classschema.md) que hereda de otro objeto de esquema de [**clase**](c-classschema.md) . Vea *herencia*.

</dd> <dt>

<span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Dados
</dt> <dd>

Objeto de [**esquema de clase**](c-classschema.md) del que heredan uno o más objetos [**de esquema de clase**](c-classschema.md) . Vea *herencia*.

</dd> <dt>

<span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Palmera
</dt> <dd>

Vea *árbol de información de directorio*.

</dd> <dt>

<span id="X.500"></span><span id="x.500"></span>X. 500
</dt> <dd>

Familia de normas desarrolladas conjuntamente por ISO e ITU, anteriormente conocidas como CCITt, que especifican la nomenclatura, la representación de datos y los protocolos de comunicaciones para un servicio de directorio.

</dd> </dl>

 

 