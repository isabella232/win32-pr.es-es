---
description: Un calificador es una cadena de datos que proporciona más información sobre una clase, una instancia, una propiedad, un método o un parámetro.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Adición de un calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697892"
---
# <a name="adding-a-qualifier"></a>Adición de un calificador

Un calificador es una cadena de datos que proporciona más información sobre una clase, una instancia, una propiedad, un método o un parámetro.

La definición de clase siguiente es un ejemplo de una clase derivada que tiene calificadores de clase.

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

Los calificadores se pueden dividir en calificadores estándar, calificadores CIM y calificadores únicos, entre los que se incluyen los siguientes:

-   Calificador estándar

    Un calificador estándar es un calificador definido por WMI que se usa habitualmente en código MOF. Por ejemplo, los calificadores [**dinámicos**](dynamic-qualifier.md) y de [**lectura**](standard-qualifiers.md) son calificadores estándar. Para obtener más información, vea [calificadores de WMI](wmi-qualifiers.md).

-   Calificador de CIM

    Un calificador de CIM es un calificador incluido en la especificación CIM. Aunque use calificadores CIM en código MOF, los calificadores estándar se han diseñado específicamente con WMI en mente. Para obtener más información, consulte la [especificación de CIM](https://www.dmtf.org/spec/cims.html/)de DMTF.

-   Calificador único

    Un calificador único es un calificador definido específicamente para una nueva clase por parte de un proveedor de clases. Por ejemplo, el calificador de [**unidades**](standard-qualifiers.md) es un calificador no estándar específico del proveedor. Puede crear sus propios calificadores para usarlos con su proveedor. Para obtener más información sobre la creación de un proveedor, vea [desarrollar un proveedor WMI](developing-a-wmi-provider.md).

Sea cual sea su calificador, el proceso principal que realice es usar el calificador en el código MOF. Para obtener más información, vea [aplicar un calificador](applying-a-qualifier.md). Puede describir más detalladamente un calificador con un tipo de calificador. Un tipo de calificador contiene más información sobre cómo un proveedor debe usar un calificador. Para obtener más información, vea [Descripción de un calificador con un tipo de calificador](describing-a-qualifier-with-a-qualifier-flavor.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases de Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



