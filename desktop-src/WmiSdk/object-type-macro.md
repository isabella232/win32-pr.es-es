---
description: La macro OBJECT-TYPE contiene cláusulas obligatorias y opcionales que describen las características básicas de un objeto MIB. El proveedor SNMP convierte un MIB en las partes correspondientes de la macro OBJECT-TYPE.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Object-TYPE (Macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973761"
---
# <a name="object-type-macro"></a>Object-TYPE (Macro)

La macro OBJECT-TYPE contiene cláusulas obligatorias y opcionales que describen las características básicas de un objeto MIB. El proveedor SNMP convierte un MIB en las partes correspondientes de la macro OBJECT-TYPE.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configurar el entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

## <a name="components"></a>Componentes

<dl> <dt>

<span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>Objeto MIB
</dt> <dd>

Objeto que contiene la mayoría de los datos en cuestión.

</dd> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descriptor de objetos
</dt> <dd>

Nombre único o descriptor de objeto que identifica cada objeto MIB. Cada descriptor de objeto MIB se asigna exactamente a un nombre de propiedad CIM. Por ejemplo, **ifIndex se** traduce a **ifIndex**.

</dd> <dt>

<span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[CLÁUSULA SYNTAX](syntax-clause.md)
</dt> <dd>

Define los datos y el tipo de un objeto MIB.

</dd> <dt>

<span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[Cláusula INDEX](index-clause.md)
</dt> <dd>

Define una clave para seleccionar una fila de tabla única.

</dd> <dt>

<span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>Cláusula AUGMENTS
</dt> <dd>

Indica que la colección de tablas que especifica se puede considerar una extensión de otra colección de tablas y puede reemplazar la cláusula INDEX en SNMPv2. Las colecciones a las que hace referencia la cláusula AUGMENTS se pueden combinar con la otra colección de tablas para formar una colección. La colección resultante comparte las propiedades de clave principal especificadas en la última colección de tablas de la cadena.

En este caso, las reglas de asignación anteriores especificadas para la cláusula INDEX se aplican a la última colección de tablas de la cadena. A continuación, la colección de objetos se asigna a una definición de clase CIM.

</dd> <dt>

<span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>Cláusula OBJECT-IDENTIFIER
</dt> <dd>

Contiene un identificador de objeto único para un objeto MIB. Este identificador de objeto se asigna al identificador de objeto calificador de **\_ propiedad** CIM .

</dd> <dt>

<span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Cláusulas ACCESS y MAX-ACCESS](access-and-max-access-clauses.md)
</dt> <dd>

Defina los derechos de acceso al objeto MIB.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>CLÁUSULA DESCRIPTION
</dt> <dd>

Proporciona una descripción de texto del objeto , que se asigna al calificador de propiedad CIM **Description**. Esta cláusula puede estar vacía.

Cada **objeto TABLE** y **ENTRY** de una definición de tabla SNMP también contiene una cláusula DESCRIPTION, que también puede estar vacía. Las cláusulas TABLE y ENTRY DESCRIPTION se concatenan y el resultado se asigna al calificador de clase CIM **Description**.

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Status (cláusula)
</dt> <dd>

Indica si el objeto debe ser compatible. Cuando el valor de la cláusula STATUS está **obsoleto,** el proveedor descarta el objeto MIB de la asignación. De lo contrario, la cláusula STATUS se asigna al calificador de propiedad CIM **Status**.

Para SNMPv1, el valor preferido  de **Status** es obligatorio u **opcional,** pero el calificador puede contener algún otro valor. Para SNMPv2C, el valor preferido de **Status** es **actual** o está en desuso, pero el calificador puede contener algún otro valor. 

</dd> <dt>

<span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>Cláusula DEFVAL
</dt> <dd>

Asigna un valor predeterminado a una variable de una fila de tabla lógica y se asigna al calificador de propiedad CIM de cadena **Defval**.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>CLÁUSULA REFERENCE
</dt> <dd>

Hace referencia a otro documento que contiene más información sobre el objeto . Esta cláusula se asigna al calificador de propiedad CIM **Reference**, que es de tipo cadena.

</dd> <dt>

<span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>Cláusula UNITS
</dt> <dd>

Proporciona una definición precisa de lo que representa el objeto. Esta cláusula se asigna al calificador de propiedad CIM **Units**, que es de tipo cadena.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La macro OBJECT-TYPE describe las características básicas de un objeto MIB individual. Un conjunto de macros OBJECT-TYPE se puede considerar como un grupo de objetos relacionados. En SNMPv2C, use la macro OBJECT-GROUP para agrupar formalmente conjuntos de objetos relacionados en una colección. Sin embargo, no hay ningún mecanismo formal para crear colecciones en SNMPv1. Para los fines del proveedor SNMP, se omite la macro OBJECT-GROUP, pero puede inventar relaciones de agrupación y crear colecciones.

 

 



