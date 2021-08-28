---
description: Una colección SNMP se asigna a una clase CIM y los elementos de una colección se asignan a las propiedades de una clase CIM. Todas las definiciones de clase CIM generadas deben derivarse de la clase SnmpObjectType.
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: Colecciones SNMP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df4926ab89a6bb9a936fe5bdb27f921699bbe90a528842d81de96d8049412940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315309"
---
# <a name="snmp-collections"></a>Colecciones SNMP

Una colección SNMP se asigna a una clase CIM y los elementos de una colección se asignan a las propiedades de una clase CIM. Todas las definiciones de clase CIM generadas deben derivarse de **la clase SnmpObjectType.**

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

Las siguientes definiciones de clase son primarias en todas las definiciones de clase generadas:

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a>Comentarios

Las reglas siguientes se aplican al asignar colecciones SNMP a clases CIM. A menos que se especifique lo contrario, estas reglas se aplican a las colecciones escalares y de tabla:

-   El proceso de asignación genera nombres de clase CIM mediante la concatenación de "SNMP", el nombre de identidad del módulo MIB, " " " y el descriptor de objetos de \_ \_ la colección.

    Por ejemplo: **el sistema** se traduce en el sistema **\_ \_ \_ MIB RFC1213** de SNMP, mientras que **ifTable** se traduce en **SNMP \_ RFC1213 \_ MIB \_ ifTable**.

-   En todos los casos, los guiones (-) de los identificadores MIB de SNMP se asignan a caracteres de subrayado ( \_ ) en los nombres de clase CIM.
-   Los conflictos de nomenclatura pueden producirse debido a que el nombre CIM no tiene en cuenta las mayúsculas y minúsculas. Si se produce un conflicto de nomenclatura, el proveedor elige una de las definiciones de grupo en conflicto y omite las definiciones restantes.
-   El nombre de identidad del módulo MIB que contiene la colección se asigna al calificador de clase CIM **Nombre del \_ módulo**.
-   El identificador de objeto de la colección fabricada se asigna al calificador de clase CIM **Group \_ Objectid**.
-   La lista de importaciones del módulo MIB (obtenida de la definición de macro **MODULE-IDENTITY)** se asigna a las importaciones del módulo calificador de **\_ clase** CIM . Este calificador contiene una lista separada por comas de nombres de módulo.

 

 



