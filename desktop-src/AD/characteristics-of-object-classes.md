---
title: Características de las clases de objeto
description: Cada clase de objeto de Active Directory Domain Services se define mediante un objeto classSchema en el contenedor de esquemas.
ms.assetid: 88a2b2a3-e8e2-4be1-9784-9709cbea08d6
ms.tgt_platform: multiple
keywords:
- Características de las clases de objeto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00c7e750d53597d1532d48c3c463315f8a48bd6d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789622"
---
# <a name="characteristics-of-object-classes"></a>Características de las clases de objeto

Cada clase de objeto de Active Directory Domain Services se define mediante un objeto **ClassSchema** en el contenedor de esquemas. Los atributos de un objeto **ClassSchema** especifican las características de la clase, como:

-   Identificadores de clase: las clases tienen varios identificadores, entre los que se incluyen **LDAPDisplayName**, que son utilizados por los clientes LDAP para identificar la clase en los filtros de búsqueda y **schemaIDGUID**, que se usan en los descriptores de seguridad para controlar el acceso a la clase.
-   Posibles atributos: una definición de clase de objeto incluye listas de los atributos obligatorios y opcionales que se pueden establecer en una instancia de la clase.
-   Posibles elementos primarios: cada instancia de objeto, excepto la raíz de la jerarquía de directorios, tiene exactamente un elemento primario. Una definición de clase de objeto incluye listas de elementos primarios posibles, es decir, de las clases de objeto que pueden contener una instancia de la clase.
-   Superclases y clases auxiliares: cada clase de objeto (excepto la [*parte superior*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85))) se deriva de otra clase. Una clase hereda los posibles atributos y los posibles elementos primarios de las clases anteriores en la jerarquía de clases. Una clase también puede tener cualquier número de clases auxiliares de las que hereda listas de posibles atributos. Para obtener más información, vea [herencia de clases en el esquema de Active Directory](class-inheritance-in-the-active-directory-schema.md).

En la tabla siguiente se muestra el **lDAPDisplayName** y la descripción de los atributos clave de un objeto **ClassSchema** . Para obtener más información y una lista completa de los atributos obligatorios y opcionales de un objeto **ClassSchema** , vea [**ClassSchema**](/windows/desktop/ADSchema/c-classschema).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>lDAPDisplayName</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CN</strong></td>
<td>Cada objeto de Active Directory Domain Services tiene un atributo de nombre del que se forma el nombre distintivo relativo (RDN). El atributo de nomenclatura de los objetos <strong>ClassSchema</strong> es <strong>CN</strong> (Common-Name). El valor asignado a <strong>CN</strong> es el valor que tendrá la clase de objeto como RDN. Por ejemplo, el <strong>CN</strong> de la clase de objeto <strong>OrganizationalUnit</strong> es unidad organizativa, que aparecería en un nombre distintivo como CN = Organization-Unit. El <strong>CN</strong> debe ser único en el contenedor de esquemas.</td>
</tr>
<tr class="even">
<td><strong>lDAPDisplayName</strong></td>
<td>Nombre utilizado por los clientes LDAP, como el proveedor LDAP de ADSI, para hacer referencia a la clase, por ejemplo, para especificar la clase en un filtro de búsqueda. El <strong>lDAPDisplayName</strong> de una clase debe ser único en el contenedor de esquema, lo que significa que debe ser único en todos los objetos <strong>ClassSchema</strong> y <strong>attributeSchema</strong> . Para obtener más información sobre la composición de un <strong>CN</strong> y un <strong>lDAPDisplayName</strong> para una nueva clase, vea <a href="naming-attributes-and-classes.md">asignar nombres a atributos y clases</a>.</td>
</tr>
<tr class="odd">
<td><strong>schemaIDGUID</strong></td>
<td>GUID almacenado como una cadena de octeto. Este GUID identifica la clase de forma única. Este GUID se puede usar en entradas de control de acceso para controlar el acceso a los objetos de esta clase. Para obtener más información, vea <a href="setting-permissions-on-child-object-operations.md">establecer permisos en operaciones de objetos secundarios</a>. Al crear el objeto <strong>ClassSchema</strong> , el servidor de Active Directory genera este valor si no se especifica. Si crea una nueva clase, genere su propio GUID para cada clase para que todas las instalaciones de la extensión usen el mismo <strong>schemaIDGUID</strong> para hacer referencia a la clase.<br/></td>
</tr>
<tr class="even">
<td><strong>adminDisplayName</strong></td>
<td>Nombre para mostrar de la clase que se va a usar en herramientas administrativas. Si no se especifica <strong>adminDisplayName</strong> cuando se crea una clase, el sistema utiliza el valor Common-Name como nombre para mostrar. Este nombre para mostrar solo se utiliza si no existe una asignación en la propiedad <strong>classDisplayName</strong> del especificador de presentación para la clase. Para obtener más información, vea <a href="display-specifiers.md">especificadores de pantalla</a> y <a href="class-and-attribute-display-names.md">nombres para mostrar de clases y atributos</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>governsID</strong></td>
<td>OID de la clase. Este valor debe ser único entre el <strong>governsIDs</strong> de todos los objetos <strong>ClassSchema</strong> y el <strong>AttributeIDs</strong> de todos los objetos <strong>attributeSchema</strong> . Para obtener más información, vea <a href="object-identifiers.md">identificadores de objetos</a>.</td>
</tr>
<tr class="even">
<td><strong>rDnAttId</strong></td>
<td>Identifica el atributo de asignación de nombres, que es el atributo que proporciona el RDN para esta clase si es diferente del valor predeterminado (<strong>CN</strong>). No se recomienda el uso de un atributo de nomenclatura distinto de <strong>CN</strong> . Los atributos de nomenclatura deben extraerse del conjunto conocido (OU, CN, O, L y DC) que comprenden todos los clientes LDAP versión 3. Para obtener más información, vea <a href="object-names-and-identities.md">nombres de objeto e identidades</a> y <a href="syntaxes-for-attributes-in-active-directory-domain-services.md">sintaxis para los atributos de Active Directory Domain Services</a>. Un atributo de nomenclatura debe tener la sintaxis de la cadena de directorio. Para obtener más información, vea <a href="syntaxes-for-attributes-in-active-directory-domain-services.md">Sintaxis de atributos en Active Directory Domain Services</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>mustContain</strong>, <strong>systemMustContain</strong></td>
<td>Par de propiedades de varios valores que especifican los atributos que deben estar presentes en las instancias de esta clase. Son atributos obligatorios que deben estar presentes durante la creación y no se pueden borrar después de la creación. Después de crear la clase, estas propiedades no se pueden cambiar. El conjunto completo de atributos obligatorios para una clase es la Unión de los valores <strong>systemMustContain</strong> y <strong>mustContain</strong> en esta clase y todas las clases heredadas.<br/></td>
</tr>
<tr class="even">
<td><strong>mayContain</strong>, <strong>systemMayContain</strong></td>
<td>Par de propiedades de varios valores que especifican los atributos que pueden estar presentes en las instancias de esta clase. Son atributos opcionales que no son obligatorios y, por tanto, pueden o no estar presentes en una instancia de esta clase. Puede Agregar o quitar los valores de <strong>mayContain</strong> de un objeto <strong>ClassSchema</strong> de categoría 1 o categoría 2 existente. Antes de quitar un valor de <strong>mayContain</strong> de un objeto <strong>ClassSchema</strong> , debe buscar instancias de la clase de objeto y borrar los valores del atributo que está quitando. Después de crear la clase, no se puede cambiar la propiedad <strong>SystemMayContain</strong> el conjunto completo de atributos opcionales para una clase es la Unión de los valores <strong>systemMayContain</strong> y <strong>mayContain</strong> de esta clase y todas las clases heredadas.<br/></td>
</tr>
<tr class="odd">
<td><strong>possSuperiors</strong>, <strong>systemPossSuperiors</strong></td>
<td>Par de propiedades de varios valores que especifican las clases estructurales que pueden ser elementos primarios legales de las instancias de esta clase. El conjunto completo de los valores superiores posibles es la Unión de los valores <strong>systemPossSuperiors</strong> y <strong>possSuperiors</strong> de esta clase y cualquier clase abstracta o estructural heredada. los valores <strong>systemPossSuperiors</strong> y <strong>possSuperiors</strong> no se heredan de las clases auxiliares. Puede Agregar o quitar los valores de <strong>possSuperiors</strong> de un objeto <strong>ClassSchema</strong> de categoría 1 o categoría 2 existente. Después de crear la clase, no se puede cambiar la propiedad <strong>systemPossSuperiors</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>objectClassCategory</strong></td>
<td>Valor entero que especifica la categoría de la clase, que puede ser una de las siguientes:
<ul>
<li>Estructural, lo que significa que se pueden crear instancias en el directorio.</li>
<li>Abstracto, lo que significa que la clase proporciona una definición básica de una clase que se puede usar para formar clases estructurales.</li>
<li>Auxiliar, es decir, una clase que se puede utilizar para ampliar la definición de una clase que hereda de ella pero no se puede usar para formar una clase por sí sola.</li>
</ul>
Para obtener más información, vea <a href="structural-abstract-and-auxiliary-classes.md">clases estructurales, abstractas y auxiliares</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>subClassOf</strong></td>
<td>Un OID para la superclase inmediata de esta clase, es decir, la clase de la que se deriva esta clase. En el caso de las clases estructurales, <strong>Subclassa</strong> puede ser una clase abstracta o estructural.<br/> En el caso de las clases abstractas, <strong>Subclassa</strong> solo puede ser una clase abstracta.<br/> En el caso de las clases auxiliares, <strong>Subclassa</strong> puede ser una clase abstracta o auxiliar.<br/> Si define una nueva clase, asegúrese de que la clase <strong>Subclassa</strong> existe o existirá cuando la nueva clase se escriba en el directorio. Si la clase no existe, el objeto <strong>ClassSchema</strong> no se agrega al directorio.<br/></td>
</tr>
<tr class="even">
<td><strong>auxiliaryClass</strong>, <strong>systemAuxiliaryClass</strong></td>
<td>Par de propiedades de varios valores que especifican las clases auxiliares de las que esta clase hereda. El conjunto completo de clases auxiliares es la Unión de los valores <strong>systemAuxiliaryClass</strong> y <strong>auxiliaryClass</strong> en esta clase y todas las clases heredadas. En el caso de un objeto <strong>ClassSchema</strong> existente, los valores se pueden agregar a la propiedad <strong>auxiliaryClass</strong> , pero no se pueden quitar. Después de crear la clase, no se puede cambiar la propiedad <strong>systemAuxiliaryClass</strong> .<br/></td>
</tr>
<tr class="odd">
<td><strong>defaultObjectCategory</strong></td>
<td>Nombre distintivo de esta clase de objeto o de una de sus superclases. Cuando se crea una instancia de esta clase de objeto, el sistema establece la propiedad <strong>objectCategory</strong> de la nueva instancia en el valor especificado en la propiedad <strong>defaultObjectCategory</strong> de su clase de objeto. La propiedad <strong>objectCategory</strong> es una propiedad indizada que se usa para aumentar la eficacia de las búsquedas de clases de objetos. Si no se especifica <strong>defaultObjectCategory</strong> cuando se crea una clase, el sistema la establece en el nombre distintivo (DN) del objeto <strong>ClassSchema</strong> de esta clase. Si este objeto se consulta con frecuencia por el valor de una superclase en lugar de la propia clase del objeto, puede establecer <strong>defaultObjectCategory</strong> en el DN de la superclase. Por ejemplo, si está subclase de una clase predefinida (categoría 1), el procedimiento recomendado es establecer <strong>defaultObjectCategory</strong> en el mismo valor que la superclase. Esto permite a la interfaz de usuario estándar &quot; Buscar &quot; la subclase.<br/> Para obtener más información, vea <a href="object-class-and-object-category.md">clase de objeto y categoría de objeto</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>defaultHidingValue</strong></td>
<td>Valor booleano que especifica el valor predeterminado de la propiedad <strong>del showinadvancedviewonly</strong> de las nuevas instancias de esta clase. Muchos objetos de directorio no son interesantes para los usuarios finales. Para evitar que estos objetos ocupen la interfaz de usuario, todos los objetos tienen un atributo booleano denominado <strong>del showinadvancedviewonly</strong>. Si <strong>defaultHidingValue</strong> se establece en <strong>true</strong>, las nuevas instancias de objeto están ocultas en los complementos administrativos y en el shell de Windows. Un elemento de menú de la clase de objeto no aparecerá en el menú <strong>contextual de los</strong> complementos administrativos, aunque las propiedades del Asistente para la creación adecuada se establezcan en el objeto <strong>displaySpecifier</strong> de la clase de objeto.<br/> Si <strong>defaultHidingValue</strong> se establece en <strong>false</strong>, las nuevas instancias del objeto se muestran en los complementos administrativos y en el shell de Windows. Establezca esta propiedad en <strong>false</strong> para ver las instancias de la clase en los complementos administrativos y el Shell y habilitar un asistente para creación y su elemento de menú en el menú <strong>nuevo</strong> de los complementos administrativos.<br/> Si no se establece el valor de <strong>defaultHidingValue</strong> , el valor predeterminado es <strong>true</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>systemFlags</strong></td>
<td>Valor entero que contiene las marcas que definen las propiedades adicionales de la clase. El bit 0x10 identifica una clase de categoría 1 (una clase que forma parte del esquema base incluido en el sistema). No se puede establecer este bit, lo que significa que no se establece el bit en clases de categoría 2 (que son extensiones del esquema).</td>
</tr>
<tr class="even">
<td><strong>systemOnly</strong></td>
<td>Valor booleano que especifica si solo el servidor de Active Directory puede modificar la clase. Solo el agente de sistema de directorio (DSA) puede crear o eliminar las clases del sistema. Las clases solo del sistema son las que dependen del sistema para las operaciones normales.</td>
</tr>
<tr class="odd">
<td><strong>defaultSecurityDescriptor</strong></td>
<td>Especifica el descriptor de seguridad predeterminado para los nuevos objetos de esta clase. Para obtener más información, vea <a href="default-security-descriptor.md">descriptor de seguridad predeterminado</a> y cómo se establecen los descriptores <a href="how-security-descriptors-are-set-on-new-directory-objects.md">de seguridad en los nuevos objetos de directorio</a>.</td>
</tr>
<tr class="even">
<td><strong>isDefunct</strong></td>
<td>Valor booleano que indica si la clase está inactiva. Para obtener más información, vea <a href="disabling-existing-classes-and-attributes.md">deshabilitar clases y atributos existentes</a>.</td>
</tr>
<tr class="odd">
<td><strong>description</strong></td>
<td>Una descripción de texto de la clase para que la usen las aplicaciones administrativas.</td>
</tr>
<tr class="even">
<td><strong>objectClass</strong></td>
<td>Identifica la clase de objeto de la que es una instancia de este objeto, que es la clase de objeto <strong>ClassSchema</strong> para todas las definiciones de clase y la clase de objeto <strong>attributeSchema</strong> para todas las definiciones de atributo.</td>
</tr>
</tbody>
</table>



 

 

