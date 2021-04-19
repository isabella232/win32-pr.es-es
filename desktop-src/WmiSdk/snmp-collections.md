---
description: Una colección SNMP se asigna a una clase CIM y los elementos de una colección se asignan a las propiedades de una clase CIM. Todas las definiciones de clases CIM generadas deben derivarse de la clase SnmpObjectType.
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
ms.openlocfilehash: a85473a394ce715ff9759e974a47824e5621509f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715752"
---
# <a name="snmp-collections"></a>Colecciones SNMP

Una colección SNMP se asigna a una clase CIM y los elementos de una colección se asignan a las propiedades de una clase CIM. Todas las definiciones de clases CIM generadas deben derivarse de la clase **SnmpObjectType** .

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Las siguientes definiciones de clase primarias todas las definiciones de clase generadas:

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

## <a name="remarks"></a>Observaciones

Las siguientes reglas se aplican al asignar colecciones SNMP a clases CIM. A menos que se especifique lo contrario, estas reglas se aplican a las colecciones escalares y de tabla:

-   El proceso de asignación genera nombres de clase CIM mediante la concatenación de "SNMP \_ ", el nombre de identidad del módulo MIB, " \_ " y el descriptor de objeto de la colección.

    Por ejemplo: **sistema** se traduce al **\_ \_ \_ sistema MIB SNMP RFC1213**, mientras que **ifTable** se traduce en **SNMP \_ RFC1213 \_ MIB \_ ifTable**.

-   En todos los casos, los guiones (-) de los identificadores SNMP MIB se asignan a los guiones bajos ( \_ ) en los nombres de clase CIM.
-   Pueden producirse conflictos de nomenclatura debido a que el nombre de CIM no distingue mayúsculas de minúsculas. Si se produce un conflicto de nomenclatura, el proveedor elige una de las definiciones de grupo en conflicto y omite las definiciones restantes.
-   El nombre de identidad del módulo MIB que contiene la colección se asigna al **\_ nombre del módulo** calificador de clase CIM.
-   El identificador de objeto de la colección fabricada se asigna al **grupo \_** de calificador de clase CIM.
-   La lista de importaciones de módulos MIB (obtenida de la definición de macro **de identidad de módulo** ) se asigna a las **\_ importaciones del módulo** calificador de clase CIM. Este calificador contiene una lista separada por comas de nombres de módulos.

 

 



