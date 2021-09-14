---
description: El modelo de localización del esquema CIM proporciona un mecanismo para la localización de calificadores. No admite la localización directa de valores de propiedad.
ms.assetid: a88bd873-7132-45b6-831e-64f9bb254c6e
ms.tgt_platform: multiple
title: Localización de valores de propiedad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ccec714557934ca32a878e21fb2a75d24a211a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249356"
---
# <a name="localizing-property-values"></a>Localización de valores de propiedad

El modelo de localización del esquema CIM proporciona un mecanismo para la localización de calificadores. No admite la localización directa de valores de propiedad.

Sin embargo, en algunos casos, los valores de propiedades de cadena de las instancias estáticas se pueden reemplazar por un tipo entero enumerado y se puede definir un mapa de valores para la propiedad en la definición de clase. En estos casos, se **debe localizar el** calificador Valores. El uso de calificadores de enumeración es el mecanismo principal para la localización de valores de propiedad. No se admiten otras formas de localización de valores de propiedad.

En el ejemplo siguiente se muestra cómo se pueden localizar las propiedades estáticas mediante mapas de valores parciales con expresiones regulares. En este ejemplo, el subconjunto predefinido de valores se inicializa en el esquema mediante instancias estáticas. El resto de los valores se proporcionan dinámicamente.

``` syntax
[abstract]
class DataGroup
{
   [key] string GUID;
   [Description("data group display name"): Amended,
                     ValueMap{"Logical Disk",
                     "CPU Utilization", ".+"}]
                     string GroupDisplayName;
   [ValueMap{"Monitors percentage of disk free space",
                  "Monitors percentage CPU utilization", ".+"}] 
                   string GroupDescription;
};

[static, Description ("pre-configured parameters") :amended]
class InitialGroup : DataGroup {
};

[dynamic, provider("HMProvider"),
    Description ("user-defined parameters") :amended]
class UserDefionedGroup : DataGroup {
};

instance of InitialGroup {
   GUID = "abc";
   GroupDisplayName = "Logical Disk";
   GroupDescription = "Monitors percentage of disk free space";
};

instance of InitialGroup {
   GUID = "def";
   GroupDisplayName = "CPU Utilization";
   GroupDescription = "Monitors percentage CPU utilization";
};
```

Para obtener más información, [vea Localización de propiedades estáticas.](localizing-static-properties.md)

 

 



