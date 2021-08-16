---
title: Active Directory terminología del esquema
description: Los términos siguientes se usan normalmente para hacer referencia al Active Directory esquema.
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b48256d1df8f9c344fe0acceb2fb6a70ed3033260baea4db7df44dd71e1c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117836450"
---
# <a name="active-directory-schema-terminology"></a>Active Directory terminología del esquema

Los términos siguientes se usan normalmente para hacer referencia al Active Directory esquema.


<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atributo
</dt> <dd>

Elementos de datos utilizados para describir los objetos representados por las clases definidas en el esquema. Los atributos se definen en el esquema por separado de las clases ; esto permite aplicar una definición de atributo única a muchas clases. Por ejemplo, [**Description**](a-description.md) es un atributo que se puede aplicar a cualquier clase del esquema. El **atributo Description** se define una vez en el esquema, lo que asegura la coherencia, en lugar de tener una definición diferente para **Descripción** de un usuario y **Descripción** de una impresora.

> [!Note]  
> La propiedad *term* se usa con frecuencia indistintamente con el atributo *de término*.

 

</dd> <dt>

<span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Instancia de atributo
</dt> <dd>

Repetición de un atributo que se define en el esquema. Este término se usa para distinguir entre la definición de un atributo y una aparición discreta del atributo. Por ejemplo, al almacenar un objeto User para "Jeff Smith" con el atributo [**Common-Name**](a-cn.md) establecido en "Jeff Smith", se crea una instancia [**de Common-Name**](a-cn.md).

</dd> <dt>

<span id="Class"></span><span id="class"></span><span id="CLASS"></span>Clase
</dt> <dd>

Descripción formal de un tipo discreto e identificable de objeto almacenado en el servicio de directorio. Por ejemplo, [**User**](c-user.md), [**Print-Queue**](c-printqueue.md)y [**Group**](c-group.md) son todas clases. Además, hay tres categorías distintas de clases: [clases](classes-structural.md)estructurales, [clases abstractas](classes-abstract.md)y [clases auxiliares.](classes-auxiliary.md)

</dd> <dt>

<span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Instancia de clase
</dt> <dd>

Repetición de una clase que se define en el esquema. Este término se usa para distinguir entre la definición de una clase y una aparición discreta de la clase . Por ejemplo, almacenar un [**objeto User**](c-user.md) para "Jeff Smith" en el servicio de directorio crea una instancia de [**User**](c-user.md).

</dd> <dt>

<span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Reglas de contenido
</dt> <dd>

Definición del posible contenido de las instancias de clase que se almacenan en el servicio de directorio. En NT Directory Services (NTDS), en el que se basa Active Directory, las reglas de contenido se expresan completamente mediante los atributos [**Must-Contain**](a-mustcontain.md) y [**May-Contain**](a-maycontain.md) de las definiciones de esquema para cada clase.

</dd> <dt>

<span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivación
</dt> <dd>

Vea *Herencia.*

</dd> <dt>

<span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Árbol de información de directorio
</dt> <dd>

El propio directorio, representado como una estructura de árbol en la que los vértices son las entradas de directorio (instancias de clase) y las líneas de conexión las relaciones de elementos primarios y secundarios entre las entradas.

</dd> <dt>

<span id="DIT"></span><span id="dit"></span>Dit
</dt> <dd>

Vea *Árbol de información de directorio.*

</dd> <dt>

<span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Control de los derechos de acceso
</dt> <dd>

Clase que describe un derecho de acceso no asociado a un recurso, sino a una acción. Por ejemplo, a un usuario se le puede conceder el derecho de crear valores de identificador relativos.

</dd> <dt>

<span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Herencia
</dt> <dd>

La capacidad de crear nuevas clases de objeto a partir de clases de objeto existentes. El nuevo objeto se define como *una subclase* del objeto primario. El objeto primario se convierte en *una superclase* del nuevo objeto. Una subclase hereda los atributos del elemento primario, incluidas las reglas de estructura y las reglas de contenido.

</dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>Ldap
</dt> <dd>

Consulte *Protocolo ligero de acceso a directorios*.

</dd> <dt>

<span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Protocolo ligero de acceso a directorios
</dt> <dd>

Un protocolo de comunicaciones de Internet estándar que se usa para comunicarse con ntds. Se admiten las versiones 2 y 3 de LDAP.

</dd> <dt>

<span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT Security Descriptor
</dt> <dd>

Vea *Descriptor de seguridad*.

</dd> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Objeto
</dt> <dd>

Unidad de almacenamiento de datos en el servicio de directorio. Los objetos de servicio de directorio no se deben confundir con objetos COM u otros objetos del sistema orientados a objetos, que tienen un componente ejecutable y un comportamiento en tiempo de ejecución. Los objetos de servicio de directorio solo constan de datos. Un objeto de servicio de directorio se define mediante un objeto [**Class-Schema**](c-classschema.md) y un grupo de objetos [**Attribute-Schema**](c-attributeschema.md) a los que hace referencia el [**objeto Class-Schema.**](c-classschema.md)

[**Los objetos Class-Schema**](c-classschema.md) [**y Attribute-Schema**](c-attributeschema.md) son a su vez objetos de servicio de directorio y tienen definiciones en el esquema como cualquier otro objeto. Vea *Clase*.

</dd> <dt>

<span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Identificador de objeto
</dt> <dd>

Valores numéricos únicos, emitidos por varias autoridades emisoras, para identificar de forma única los elementos de datos, las sintaxis y otras partes de las aplicaciones distribuidas. Los identificadores de objeto (SSID) se encuentran en aplicaciones OSI, directorios X.500, SNMP y otras aplicaciones donde la unidad es importante. Los OMISIÓN se basan en una estructura de árbol, en la que una autoridad emisora superior, como la ISO, asigna una rama del árbol a una sub authority, que a su vez puede asignar subrecciones.

Los ESPECIFICACIONES de NTDS incluyen algunos emitidos por iso para clases y atributos X.500, y otros emitidos por Microsoft. La notación OID es una cadena de números de puntos, por ejemplo "1.2.840.113556.1.5.4", que se traduce como se muestra en la lista siguiente. 

| Valor  | Descripción                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| 1      | ISO: la "autoridad raíz", emitió "1.2" a ANSI, que a su vez...                           |
| 2      | Ansi... emitió "1.2.840" a EE. UU., que a su vez...                                            |
| 840    | E.e.u.u... emitido "1.2.840.113556" a Microsoft...                                               |
| 113556 | Microsoft... donde Microsoft administra internamente varias ramas de OID en "1.2.840.113556". |
| 1      | Microsoft DS                                                                                 |
| 5      | Clases NTDS                                                                                 |
| 4      | Builtin-Domain                                                                               |



 

</dd> <dt>

<span id="OID"></span><span id="oid"></span>Oid
</dt> <dd>

Vea *Identificador de objeto*.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Esquema
</dt> <dd>

Definición formal del contenido y la estructura del servicio de directorio. El esquema define todos los atributos y clases. Para cada clase, se definen los atributos [**Poss-Superiors**](a-posssuperiors.md), [**Must-Contain**](a-mustcontain.md)y [**May-Contain.**](a-maycontain.md) [**Poss-Superiors define**](a-posssuperiors.md) las posibles estructuras de árbol para el servicio de directorio especificando qué clases pueden ser el elemento primario de cualquier clase determinada. [**Must-Contain**](a-mustcontain.md) y [**May-Contain**](a-maycontain.md) enumeran los atributos de una clase que debe estar presente para almacenar la clase y qué atributos adicionales pueden estar presentes opcionalmente.

</dd> <dt>

<span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Descriptor de seguridad
</dt> <dd>

Información sobre la propiedad de un objeto y los permisos que tienen otros usuarios en ese objeto. La [**propiedad NT-Security-Descriptor**](a-ntsecuritydescriptor.md) de una entrada de esquema contiene una cadena que representa el descriptor de seguridad del objeto . Para obtener más información sobre el formato de la información de este campo, vea [Formato de cadena del descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-string-format).

</dd> <dt>

<span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Reglas de estructura
</dt> <dd>

Definición de la estructura o estructuras de árbol posibles. En NTDS, las reglas de estructura se expresan completamente mediante el atributo Poss-superiors presente en cada [**objeto Class-Schema.**](c-classschema.md) Vea *Esquema*.

</dd> <dt>

<span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclase
</dt> <dd>

Objeto [**Class-Schema**](c-classschema.md) que hereda de otro [**objeto Class-Schema.**](c-classschema.md) Vea *Herencia.*

</dd> <dt>

<span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclase
</dt> <dd>

Objeto [**Class-Schema**](c-classschema.md) del que heredan uno o varios objetos [**Class-Schema.**](c-classschema.md) Vea *Herencia.*

</dd> <dt>

<span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Árbol
</dt> <dd>

Vea *Árbol de información de directorio.*

</dd> <dt>

<span id="X.500"></span><span id="x.500"></span>X.500
</dt> <dd>

Una familia de estándares desarrollada conjuntamente por iso e ITU, anteriormente conocida como CC SMTP, que especifican los protocolos de nomenclatura, representación de datos y comunicaciones para un servicio de directorio.

</dd> </dl>

 

 