---
description: Puede utilizar el proveedor del registro del sistema como una instancia o un proveedor de propiedades.
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: Usar el proveedor del registro del sistema como proveedor de propiedades
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64fc701843438b4d173b1914ed2ac86214fe685e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706747"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a><span data-ttu-id="dd319-103">Usar el proveedor del registro del sistema como proveedor de propiedades</span><span class="sxs-lookup"><span data-stu-id="dd319-103">Use the System Registry Provider as a Property Provider</span></span>

<span data-ttu-id="dd319-104">Puede utilizar el [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) como una instancia o un proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="dd319-104">You can use the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) as either an instance or a property provider.</span></span>

<span data-ttu-id="dd319-105">Si opta por tener acceso a las interfaces del proveedor de propiedades, debe marcar las clases WMI para indicar su intención.</span><span class="sxs-lookup"><span data-stu-id="dd319-105">If you choose to access the property provider interfaces, you must mark your WMI classes to indicate your intention.</span></span>

<span data-ttu-id="dd319-106">**Para utilizar el proveedor del registro del sistema como proveedor de propiedades**</span><span class="sxs-lookup"><span data-stu-id="dd319-106">**To use the system registry provider as a property provider**</span></span>

-   <span data-ttu-id="dd319-107">Defina la clase WMI con los calificadores estándar **DynProps**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)y **PropertyContext** .</span><span class="sxs-lookup"><span data-stu-id="dd319-107">Define your WMI class with the **DynProps**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** standard qualifiers.</span></span>

    <span data-ttu-id="dd319-108">El calificador **DynProps** identifica una clase que tiene las propiedades que mantiene el proveedor de propiedades identificado por el calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="dd319-108">The **DynProps** qualifier identifies a class as having properties that are maintained by the property provider identified by the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span> <span data-ttu-id="dd319-109">El calificador **PropertyContext** especifica el nombre del valor del registro que la propiedad va a almacenar.</span><span class="sxs-lookup"><span data-stu-id="dd319-109">The **PropertyContext** qualifier specifies the name of the registry value to be stored by the property.</span></span> <span data-ttu-id="dd319-110">El formato del calificador **PropertyContext** es el mismo que el formato del calificador **ClassContext** con valores de *expresión* y *ValueName* adicionales.</span><span class="sxs-lookup"><span data-stu-id="dd319-110">The format of the **PropertyContext** qualifier is the same as the format of the **ClassContext** qualifier with additional *valuename* and *expression* values.</span></span>

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    <span data-ttu-id="dd319-111">*ValueName* y *Expression* son opcionales.</span><span class="sxs-lookup"><span data-stu-id="dd319-111">Both *valuename* and *expression* are optional.</span></span> <span data-ttu-id="dd319-112">El valor de *ValueName* solo se utiliza si el valor del registro tiene un nombre.</span><span class="sxs-lookup"><span data-stu-id="dd319-112">The *valuename* setting is only used if the registry value has a name.</span></span> <span data-ttu-id="dd319-113">La *expresión* también es opcional y se usa para los datos del descriptor de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd319-113">The *expression* is also optional and is used for resource descriptor data.</span></span> <span data-ttu-id="dd319-114">Para obtener más información, vea [Descripción de un recurso para el registro](describing-a-resource-for-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="dd319-114">For more information, see [Describing a Resource for the Registry](describing-a-resource-for-the-registry.md).</span></span>

    <span data-ttu-id="dd319-115">En el ejemplo de código siguiente se muestra cómo la clase utiliza el proveedor del registro del sistema como un proveedor de propiedades para mantener sus propiedades sin clave.</span><span class="sxs-lookup"><span data-stu-id="dd319-115">The following code example shows how the class uses the System Registry provider as a property provider to maintain its nonkey properties.</span></span>

    ``` syntax
    [DYNPROPS]
    class PropReg {

        [KEY]  STRING  MyKey;
        STRING Logging;
        STRING Events;
        uint32 Resource1;
    };

    [DYNPROPS]
    instance of PropReg
    {
      MyKey = "a";

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|Logging"), Dynamic, Provider("RegPropProv")]  Logging;

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|EnableEvents"), Dynamic, Provider("RegPropProv")]
       Events;

      [PropertyContext("local|hkey_local_Machine\\hardware\\
       ResourceMap\\Hardware Abstraction Layer\\PC Compatible Eisa/isa 
       hal|.raw(\"Internal\")(0)(0)(\"interrupt.vector\")"), Dynamic, 
       Provider("RegPropProv")]  Resource1;
    };
    ```

 

 
