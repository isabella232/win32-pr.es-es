---
description: El modelo de localización del esquema CIM proporciona un mecanismo para localizar los calificadores. No admite la localización directa de los valores de propiedad.
ms.assetid: a88bd873-7132-45b6-831e-64f9bb254c6e
ms.tgt_platform: multiple
title: Localizar valores de propiedad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ccec714557934ca32a878e21fb2a75d24a211a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360578"
---
# <a name="localizing-property-values"></a><span data-ttu-id="187d7-104">Localizar valores de propiedad</span><span class="sxs-lookup"><span data-stu-id="187d7-104">Localizing Property Values</span></span>

<span data-ttu-id="187d7-105">El modelo de localización del esquema CIM proporciona un mecanismo para localizar los calificadores.</span><span class="sxs-lookup"><span data-stu-id="187d7-105">The CIM schema localization model provides a mechanism for localizing qualifiers.</span></span> <span data-ttu-id="187d7-106">No admite la localización directa de los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="187d7-106">It does not support direct localization of property values.</span></span>

<span data-ttu-id="187d7-107">Sin embargo, en algunos casos, los valores de las propiedades de cadena de las instancias estáticas se pueden reemplazar por un tipo entero enumerado y se puede definir una asignación de valores para la propiedad en la definición de clase.</span><span class="sxs-lookup"><span data-stu-id="187d7-107">In some cases, however, the string properties values in the static instances can be replaced by an enumerated integer type and a value map can be defined for the property in the class definition.</span></span> <span data-ttu-id="187d7-108">En estos casos, se debe localizar el calificador de **valores** .</span><span class="sxs-lookup"><span data-stu-id="187d7-108">In these cases, the **Values** qualifier should be localized.</span></span> <span data-ttu-id="187d7-109">El uso de calificadores de enumeración es el mecanismo principal para localizar valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="187d7-109">Using enumeration qualifiers is the primary mechanism for localizing property values.</span></span> <span data-ttu-id="187d7-110">No se admiten otras formas de localización de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="187d7-110">Any other forms of property value localization are not supported.</span></span>

<span data-ttu-id="187d7-111">En el ejemplo siguiente se muestra cómo se pueden localizar las propiedades estáticas mediante mapas de valores parciales con expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="187d7-111">The following example shows how static properties can be localized using partial value maps with regular expressions.</span></span> <span data-ttu-id="187d7-112">En este ejemplo, el subconjunto predefinido de valores se inicializa en el esquema mediante instancias estáticas.</span><span class="sxs-lookup"><span data-stu-id="187d7-112">In this example, the predefined subset of values is initialized in the schema using static instances.</span></span> <span data-ttu-id="187d7-113">El resto de los valores se proporcionan dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="187d7-113">The rest of the values are provided dynamically.</span></span>

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

<span data-ttu-id="187d7-114">Para obtener más información, consulte [localizar propiedades estáticas](localizing-static-properties.md).</span><span class="sxs-lookup"><span data-stu-id="187d7-114">For more information, see [Localizing Static Properties](localizing-static-properties.md).</span></span>

 

 



