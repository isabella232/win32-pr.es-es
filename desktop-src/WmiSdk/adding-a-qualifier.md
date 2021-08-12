---
description: Un calificador es una cadena de datos que proporciona más información sobre una clase, instancia, propiedad, método o parámetro.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Agregar un calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333c24e89d711a8998c58c6201776d5d4c50cc1107f4c9ca4308d9cc992b44dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557828"
---
# <a name="adding-a-qualifier"></a>Agregar un calificador

Un calificador es una cadena de datos que proporciona más información sobre una clase, instancia, propiedad, método o parámetro.

La siguiente definición de clase es un ejemplo de una clase derivada que tiene calificadores de clase.

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

Los calificadores se pueden dividir en calificadores estándar, calificadores CIM y calificadores únicos:

-   Calificador estándar

    Un calificador estándar es un calificador definido por WMI y que se usa normalmente en el código MOF. Por ejemplo, los [**calificadores Dynamic**](dynamic-qualifier.md) [**y Read**](standard-qualifiers.md) son calificadores estándar. Para obtener más información, vea [Calificadores WMI](wmi-qualifiers.md).

-   Calificador CIM

    Un calificador CIM es un calificador incluido en la especificación CIM. Aunque se usan calificadores CIM en código MOF, los calificadores estándar se diseñan específicamente con WMI en mente. Para obtener más información, vea la especificación [CIM de](https://www.dmtf.org/spec/cims.html/)DMTF .

-   Calificador único

    Un calificador único es un calificador definido específicamente para una nueva clase por un proveedor de clases. Por ejemplo, el [**calificador Units**](standard-qualifiers.md) es un calificador no estándar específico del proveedor. Puede crear sus propios calificadores para usarlos con el proveedor. Para obtener más información sobre cómo crear un proveedor, vea [Desarrollar un proveedor WMI.](developing-a-wmi-provider.md)

Independientemente de lo que haga el calificador, el proceso principal que realice es usar el calificador en el código MOF. Para obtener más información, [vea Aplicar un calificador](applying-a-qualifier.md). Puede describir aún más un calificador con un formato de calificador. Un calificador contiene más información sobre cómo un proveedor debe usar un calificador. Para obtener más información, vea [Describing a Qualifier with a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



