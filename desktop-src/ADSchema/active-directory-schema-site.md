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
# <a name="active-directory-schema-terminology"></a><span data-ttu-id="2a29c-103">Terminología de esquemas Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a29c-103">Active Directory Schema Terminology</span></span>

<span data-ttu-id="2a29c-104">Los siguientes términos se utilizan normalmente para hacer referencia al esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2a29c-104">The following terms are commonly used to refer to the Active Directory schema.</span></span>


<dl> <dt>

<span data-ttu-id="2a29c-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atribui</span><span class="sxs-lookup"><span data-stu-id="2a29c-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-106">Elementos de datos utilizados para describir los objetos representados por las clases que se definen en el esquema.</span><span class="sxs-lookup"><span data-stu-id="2a29c-106">Data items used to describe the objects that are represented by the classes that are defined in the schema.</span></span> <span data-ttu-id="2a29c-107">Los atributos se definen en el esquema de forma independiente de las clases; Esto permite aplicar una definición de un solo atributo a muchas clases.</span><span class="sxs-lookup"><span data-stu-id="2a29c-107">Attributes are defined in the schema separately from the classes; this allows a single attribute definition to be applied to many classes.</span></span> <span data-ttu-id="2a29c-108">Por ejemplo, la [**Descripción**](a-description.md) es un atributo que se puede aplicar a cualquier clase del esquema.</span><span class="sxs-lookup"><span data-stu-id="2a29c-108">For example, [**Description**](a-description.md) is an attribute that can be applied to any class in the schema.</span></span> <span data-ttu-id="2a29c-109">El atributo **Description** se define una vez en el esquema, lo que garantiza la coherencia, en lugar de tener una definición diferente para la **Descripción** de un usuario y la **Descripción** de una impresora.</span><span class="sxs-lookup"><span data-stu-id="2a29c-109">The **Description** attribute is defined once in the schema, assuring consistency, rather than having a different definition for **Description** of a user and **Description** of a printer.</span></span>

> [!Note]  
> <span data-ttu-id="2a29c-110">La *propiedad* term se usa con frecuencia indistintamente con el término *Attribute*.</span><span class="sxs-lookup"><span data-stu-id="2a29c-110">The term *property* is frequently used interchangeably with the term *attribute*.</span></span>

 

</dd> <dt>

<span data-ttu-id="2a29c-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Instancia de atributo</span><span class="sxs-lookup"><span data-stu-id="2a29c-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Attribute Instance</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-112">Instancia de un atributo que se define en el esquema.</span><span class="sxs-lookup"><span data-stu-id="2a29c-112">An occurrence of an attribute that is defined in the schema.</span></span> <span data-ttu-id="2a29c-113">Este término se usa para distinguir entre la definición de un atributo y una repetición discreta del atributo.</span><span class="sxs-lookup"><span data-stu-id="2a29c-113">This term is used to distinguish between the definition of an attribute and a discrete occurrence of the attribute.</span></span> <span data-ttu-id="2a29c-114">Por ejemplo, si se almacena un objeto de usuario para "Jeff Smith" con el atributo [**common-name**](a-cn.md) establecido en "Jeff Smith", se crea una instancia de [**common-name**](a-cn.md).</span><span class="sxs-lookup"><span data-stu-id="2a29c-114">For example, storing a User object for "Jeff Smith" with the [**Common-Name**](a-cn.md) attribute set to "Jeff Smith" creates an instance of [**Common-Name**](a-cn.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Las</span><span class="sxs-lookup"><span data-stu-id="2a29c-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Class</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-116">Una descripción formal de un tipo discreto e identificable de un objeto almacenado en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="2a29c-116">A formal description of a discrete, identifiable type of object stored in the directory service.</span></span> <span data-ttu-id="2a29c-117">Por ejemplo, el [**usuario**](c-user.md), [**la cola de impresión y el**](c-printqueue.md) [**Grupo**](c-group.md) son todas las clases.</span><span class="sxs-lookup"><span data-stu-id="2a29c-117">For example, [**User**](c-user.md), [**Print-Queue**](c-printqueue.md), and [**Group**](c-group.md) are all classes.</span></span> <span data-ttu-id="2a29c-118">Además, hay 3 categorías distintas de clases: [clases estructurales](classes-structural.md), [clases abstractas](classes-abstract.md)y [clases auxiliares](classes-auxiliary.md).</span><span class="sxs-lookup"><span data-stu-id="2a29c-118">Furthermore, there are 3 distinct categories of classes: [Structural Classes](classes-structural.md), [Abstract Classes](classes-abstract.md), and [Auxiliary Classes](classes-auxiliary.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Instancia de clase</span><span class="sxs-lookup"><span data-stu-id="2a29c-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Class Instance</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-120">Una aparición de una clase que se define en el esquema.</span><span class="sxs-lookup"><span data-stu-id="2a29c-120">An occurrence of a class that is defined in the schema.</span></span> <span data-ttu-id="2a29c-121">Este término se usa para distinguir entre la definición de una clase y una instancia discreta de la clase.</span><span class="sxs-lookup"><span data-stu-id="2a29c-121">This term is used to distinguish between the definition of a class and a discrete occurrence of the class.</span></span> <span data-ttu-id="2a29c-122">Por ejemplo, si se almacena un objeto de [**usuario**](c-user.md) para "Jeff Smith" en el servicio de directorio, se crea una instancia del [**usuario**](c-user.md).</span><span class="sxs-lookup"><span data-stu-id="2a29c-122">For example, storing a [**User**](c-user.md) object for "Jeff Smith" in the directory service creates an instance of [**User**](c-user.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Reglas de contenido</span><span class="sxs-lookup"><span data-stu-id="2a29c-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Content Rules</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-124">La definición del posible contenido de las instancias de clase que se almacenan en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="2a29c-124">The definition of the possible contents of the class instances that are stored in the directory service.</span></span> <span data-ttu-id="2a29c-125">En los servicios de directorio de NT (NTDS), en los que se basa Active Directory, las reglas de contenido se expresan por completo en los atributos [**debe contener**](a-mustcontain.md) y [**puede contener**](a-maycontain.md) de las definiciones de esquema para cada clase.</span><span class="sxs-lookup"><span data-stu-id="2a29c-125">In NT Directory Services (NTDS), upon which Active Directory is based, the content rules are completely expressed by the [**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) attributes of the schema definitions for each class.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Deriva</span><span class="sxs-lookup"><span data-stu-id="2a29c-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivation</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-127">Vea *herencia*.</span><span class="sxs-lookup"><span data-stu-id="2a29c-127">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Árbol de información de directorio</span><span class="sxs-lookup"><span data-stu-id="2a29c-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Directory Information Tree</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-129">El propio directorio, representado como una estructura de árbol en la que los vértices son las entradas de directorio (instancias de clase) y las líneas de conexión que las relaciones de elementos primarios y secundarios entre las entradas.</span><span class="sxs-lookup"><span data-stu-id="2a29c-129">The directory itself, represented as a tree structure in which the vertices are the directory entries (class instances) and the connecting lines the parent-child relationships between the entries.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-130"><span id="DIT"></span><span id="dit"></span>PARTICIONA</span><span class="sxs-lookup"><span data-stu-id="2a29c-130"><span id="DIT"></span><span id="dit"></span>DIT</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-131">Vea *árbol de información de directorio*.</span><span class="sxs-lookup"><span data-stu-id="2a29c-131">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Derechos de acceso de control</span><span class="sxs-lookup"><span data-stu-id="2a29c-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Control Access Rights</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-133">Una clase que describe un derecho de acceso que no está asociado a un recurso, sino una acción.</span><span class="sxs-lookup"><span data-stu-id="2a29c-133">A class that describes an access right not tied to a resource, but an action.</span></span> <span data-ttu-id="2a29c-134">Por ejemplo, se puede conceder a un usuario el derecho a crear valores de identificador relativos.</span><span class="sxs-lookup"><span data-stu-id="2a29c-134">For example, a user can be granted the right to create relative ID values.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Ella</span><span class="sxs-lookup"><span data-stu-id="2a29c-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Inheritance</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-136">La capacidad de crear nuevas clases de objeto a partir de clases de objeto existentes.</span><span class="sxs-lookup"><span data-stu-id="2a29c-136">The ability to build new object classes from existing object classes.</span></span> <span data-ttu-id="2a29c-137">El nuevo objeto se define como una *subclase* del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="2a29c-137">The new object is defined as a *subclass* of the parent object.</span></span> <span data-ttu-id="2a29c-138">El objeto primario se convierte en una *superclase* del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="2a29c-138">The parent object becomes a *superclass* of the new object.</span></span> <span data-ttu-id="2a29c-139">Una subclase hereda los atributos del elemento primario, incluidas las reglas de estructura y las reglas de contenido.</span><span class="sxs-lookup"><span data-stu-id="2a29c-139">A subclass inherits the attributes of the parent, including structure rules and content rules.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span><span class="sxs-lookup"><span data-stu-id="2a29c-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-141">Consulte *Protocolo ligero de acceso a directorios*.</span><span class="sxs-lookup"><span data-stu-id="2a29c-141">See *Lightweight Directory Access Protocol*.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Protocolo ligero de acceso a directorios</span><span class="sxs-lookup"><span data-stu-id="2a29c-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-143">Protocolo estándar de comunicaciones de Internet que se usa para comunicarse con NTDS.</span><span class="sxs-lookup"><span data-stu-id="2a29c-143">A standard Internet communications protocol used to communicate with the NTDS.</span></span> <span data-ttu-id="2a29c-144">Se admiten las versiones 2 y 3 de LDAP.</span><span class="sxs-lookup"><span data-stu-id="2a29c-144">LDAP version 2 and version 3 are supported.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>Descriptor de seguridad de NT</span><span class="sxs-lookup"><span data-stu-id="2a29c-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-146">Consulte *descriptor de seguridad*.</span><span class="sxs-lookup"><span data-stu-id="2a29c-146">See *Security Descriptor*.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Objeto</span><span class="sxs-lookup"><span data-stu-id="2a29c-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Object</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-148">Unidad de almacenamiento de datos en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="2a29c-148">A unit of data storage in the directory service.</span></span> <span data-ttu-id="2a29c-149">Los objetos de servicio de directorio no se deben confundir con objetos COM u otros objetos del sistema orientados a objetos, que tienen un componente ejecutable y un comportamiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2a29c-149">Directory service objects are not to be confused with COM objects or other object-oriented system objects, which have an executable component and run-time behavior.</span></span> <span data-ttu-id="2a29c-150">Los objetos de servicio de directorio solo se componen de datos.</span><span class="sxs-lookup"><span data-stu-id="2a29c-150">Directory service objects consist only of data.</span></span> <span data-ttu-id="2a29c-151">Un objeto de servicio de directorio se define mediante un objeto de [**esquema de clase**](c-classschema.md) y un grupo de objetos de [**esquema de atributos**](c-attributeschema.md) a los que hace referencia el objeto de esquema de [**clase**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="2a29c-151">A directory service object is defined by a [**Class-Schema**](c-classschema.md) object and a group of [**Attribute-Schema**](c-attributeschema.md) objects referenced by the [**Class-Schema**](c-classschema.md) object.</span></span>

<span data-ttu-id="2a29c-152">Los objetos de esquema de [**clase**](c-classschema.md) y [**de esquema de atributo**](c-attributeschema.md) son objetos de servicio de directorio y tienen definiciones en el esquema como cualquier otro objeto.</span><span class="sxs-lookup"><span data-stu-id="2a29c-152">[**Class-Schema**](c-classschema.md) and [**Attribute-Schema**](c-attributeschema.md) objects are themselves directory service objects, and have definitions in the schema like any other objects.</span></span> <span data-ttu-id="2a29c-153">Vea la *clase*.</span><span class="sxs-lookup"><span data-stu-id="2a29c-153">See *Class*.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="2a29c-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Object Identifier</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-155">Valores numéricos únicos, emitidos por varias autoridades emisoras, para identificar de forma única los elementos de datos, las sintaxis y otras partes de las aplicaciones distribuidas.</span><span class="sxs-lookup"><span data-stu-id="2a29c-155">Unique numeric values, issued by various issuing authorities, to uniquely identify data elements, syntaxes, and various other parts of distributed applications.</span></span> <span data-ttu-id="2a29c-156">Los identificadores de objeto (OID) se encuentran en las aplicaciones OSI, los directorios X. 500, el SNMP y otras aplicaciones en las que la unicidad es importante.</span><span class="sxs-lookup"><span data-stu-id="2a29c-156">Object Identifiers (OIDs) are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="2a29c-157">Los OID se basan en una estructura de árbol, en la que una entidad de emisión superior, como la ISO, asigna una rama del árbol a una subentidad, que a su vez puede asignar subbifurcaciones.</span><span class="sxs-lookup"><span data-stu-id="2a29c-157">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a sub-authority, which in turn can allocate sub-branches.</span></span>

<span data-ttu-id="2a29c-158">Los OID de NTDS incluyen algunos emitidos por la ISO para las clases y atributos X. 500 y otros emitidos por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a29c-158">OIDs in the NTDS include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft.</span></span> <span data-ttu-id="2a29c-159">La notación OID es una cadena de números con puntos, por ejemplo "1.2.840.113556.1.5.4", que se traduce como se muestra en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="2a29c-159">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.4", which translates as listed in the following list.</span></span> 

| <span data-ttu-id="2a29c-160">Value</span><span class="sxs-lookup"><span data-stu-id="2a29c-160">Value</span></span>  | <span data-ttu-id="2a29c-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a29c-161">Description</span></span>                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a29c-162">1</span><span class="sxs-lookup"><span data-stu-id="2a29c-162">1</span></span>      | <span data-ttu-id="2a29c-163">ISO: la "entidad de certificación raíz", emitida "1,2" a ANSI, que, a su vez,...</span><span class="sxs-lookup"><span data-stu-id="2a29c-163">ISO - the "root authority", issued "1.2" to ANSI, which in turn...</span></span>                           |
| <span data-ttu-id="2a29c-164">2</span><span class="sxs-lookup"><span data-stu-id="2a29c-164">2</span></span>      | <span data-ttu-id="2a29c-165">ANSI... se emitió "1.2.840" a EE. UU., que, a su vez,...</span><span class="sxs-lookup"><span data-stu-id="2a29c-165">ANSI ...issued "1.2.840" to USA, which in turn...</span></span>                                            |
| <span data-ttu-id="2a29c-166">840</span><span class="sxs-lookup"><span data-stu-id="2a29c-166">840</span></span>    | <span data-ttu-id="2a29c-167">ESTADOS UNIDOS... se emitió "1.2.840.113556" a Microsoft...</span><span class="sxs-lookup"><span data-stu-id="2a29c-167">USA ...issued "1.2.840.113556" to Microsoft...</span></span>                                               |
| <span data-ttu-id="2a29c-168">113556</span><span class="sxs-lookup"><span data-stu-id="2a29c-168">113556</span></span> | <span data-ttu-id="2a29c-169">Microsoft... donde Microsoft administra internamente varias ramas OID en "1.2.840.113556".</span><span class="sxs-lookup"><span data-stu-id="2a29c-169">Microsoft ...where Microsoft internally manages several OID branches under "1.2.840.113556".</span></span> |
| <span data-ttu-id="2a29c-170">1</span><span class="sxs-lookup"><span data-stu-id="2a29c-170">1</span></span>      | <span data-ttu-id="2a29c-171">Microsoft DS</span><span class="sxs-lookup"><span data-stu-id="2a29c-171">Microsoft DS</span></span>                                                                                 |
| <span data-ttu-id="2a29c-172">5</span><span class="sxs-lookup"><span data-stu-id="2a29c-172">5</span></span>      | <span data-ttu-id="2a29c-173">Clases NTDS</span><span class="sxs-lookup"><span data-stu-id="2a29c-173">NTDS Classes</span></span>                                                                                 |
| <span data-ttu-id="2a29c-174">4</span><span class="sxs-lookup"><span data-stu-id="2a29c-174">4</span></span>      | <span data-ttu-id="2a29c-175">Builtin-Domain</span><span class="sxs-lookup"><span data-stu-id="2a29c-175">Builtin-Domain</span></span>                                                                               |



 

</dd> <dt>

<span data-ttu-id="2a29c-176"><span id="OID"></span><span id="oid"></span>OID</span><span class="sxs-lookup"><span data-stu-id="2a29c-176"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-177">Vea *identificador de objeto*.</span><span class="sxs-lookup"><span data-stu-id="2a29c-177">See *Object Identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Esquema</span><span class="sxs-lookup"><span data-stu-id="2a29c-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schema</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-179">Una definición formal de la estructura y el contenido del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="2a29c-179">A formal definition of the directory service contents and structure.</span></span> <span data-ttu-id="2a29c-180">El esquema define todos los atributos y las clases.</span><span class="sxs-lookup"><span data-stu-id="2a29c-180">The schema defines all attributes and classes.</span></span> <span data-ttu-id="2a29c-181">Para cada clase, se definen los atributos [**Poss-superior**](a-posssuperiors.md), [**debe contener**](a-mustcontain.md)y [**puede-contener**](a-maycontain.md) .</span><span class="sxs-lookup"><span data-stu-id="2a29c-181">For each class, the [**Poss-Superiors**](a-posssuperiors.md), [**Must-Contain**](a-mustcontain.md), and [**May-Contain**](a-maycontain.md) attributes are defined.</span></span> <span data-ttu-id="2a29c-182">[**Poss:**](a-posssuperiors.md) define las posibles estructuras de árbol para el servicio de directorio mediante la especificación de las clases que pueden ser el elemento primario de cualquier clase dada.</span><span class="sxs-lookup"><span data-stu-id="2a29c-182">[**Poss-Superiors**](a-posssuperiors.md) defines the possible tree structures for the directory service by specifying what classes can be the parent for any given class.</span></span> <span data-ttu-id="2a29c-183">[**Debe contener**](a-mustcontain.md) la lista y [**puede contener**](a-maycontain.md) los atributos de una clase que debe estar presente para almacenar la clase y los atributos adicionales que pueden estar presentes opcionalmente.</span><span class="sxs-lookup"><span data-stu-id="2a29c-183">[**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) list the attributes for a class that must be present to store the class and what additional attributes may optionally be present.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="2a29c-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-185">Información sobre la propiedad de un objeto y los permisos que otros usuarios tienen en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="2a29c-185">Information about the ownership of an object and the permissions that other users have on that object.</span></span> <span data-ttu-id="2a29c-186">La propiedad [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) de una entrada de esquema contiene una cadena que representa el descriptor de seguridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="2a29c-186">The [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) property of a schema entry contains a string that represents the security descriptor of the object.</span></span> <span data-ttu-id="2a29c-187">Para obtener más información sobre el formato de la información de este campo, vea [formato de cadena de descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span><span class="sxs-lookup"><span data-stu-id="2a29c-187">For more information about the format of the information in this field, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Reglas de estructura</span><span class="sxs-lookup"><span data-stu-id="2a29c-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Structure Rules</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-189">La definición de la estructura o estructuras de árbol posibles.</span><span class="sxs-lookup"><span data-stu-id="2a29c-189">The definition of the possible tree structure or structures.</span></span> <span data-ttu-id="2a29c-190">En NTDS, las reglas de la estructura se expresan completamente mediante el atributo Poss-superior presente en cada objeto [**de esquema de clase**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="2a29c-190">In the NTDS, the structure rules are completely expressed by the Poss-superiors attribute present on each [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="2a29c-191">Vea *esquema*.</span><span class="sxs-lookup"><span data-stu-id="2a29c-191">See *Schema*.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclase</span><span class="sxs-lookup"><span data-stu-id="2a29c-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclass</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-193">Objeto de [**esquema de clase**](c-classschema.md) que hereda de otro objeto de esquema de [**clase**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="2a29c-193">A [**Class-Schema**](c-classschema.md) object that inherits from another [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="2a29c-194">Vea *herencia*.</span><span class="sxs-lookup"><span data-stu-id="2a29c-194">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Dados</span><span class="sxs-lookup"><span data-stu-id="2a29c-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclass</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-196">Objeto de [**esquema de clase**](c-classschema.md) del que heredan uno o más objetos [**de esquema de clase**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="2a29c-196">A [**Class-Schema**](c-classschema.md) object from which one or more other [**Class-Schema**](c-classschema.md) objects inherit.</span></span> <span data-ttu-id="2a29c-197">Vea *herencia*.</span><span class="sxs-lookup"><span data-stu-id="2a29c-197">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Palmera</span><span class="sxs-lookup"><span data-stu-id="2a29c-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Tree</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-199">Vea *árbol de información de directorio*.</span><span class="sxs-lookup"><span data-stu-id="2a29c-199">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="2a29c-200"><span id="X.500"></span><span id="x.500"></span>X. 500</span><span class="sxs-lookup"><span data-stu-id="2a29c-200"><span id="X.500"></span><span id="x.500"></span>X.500</span></span>
</dt> <dd>

<span data-ttu-id="2a29c-201">Familia de normas desarrolladas conjuntamente por ISO e ITU, anteriormente conocidas como CCITt, que especifican la nomenclatura, la representación de datos y los protocolos de comunicaciones para un servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="2a29c-201">A family of standards developed jointly by the ISO and ITU, formerly known as the CCITT, that specify the naming, data representation, and communications protocols for a directory service.</span></span>

</dd> </dl>

 

 