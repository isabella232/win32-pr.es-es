---
description: Las clases que se usan para almacenar los datos del registro se definen con varios calificadores estándar.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Definir una clase del registro con calificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908679"
---
# <a name="defining-a-registry-class-with-qualifiers"></a><span data-ttu-id="2017d-103">Definir una clase del registro con calificadores</span><span class="sxs-lookup"><span data-stu-id="2017d-103">Defining a Registry Class With Qualifiers</span></span>

<span data-ttu-id="2017d-104">Las clases que se usan para almacenar los datos del registro se definen con varios calificadores estándar.</span><span class="sxs-lookup"><span data-stu-id="2017d-104">The classes used to hold registry data are defined with several standard qualifiers.</span></span>

<span data-ttu-id="2017d-105">A continuación se muestra una lista de los calificadores estándar:</span><span class="sxs-lookup"><span data-stu-id="2017d-105">The following is a list of the standard qualifiers:</span></span>

-   <span data-ttu-id="2017d-106">[Dynamic](standard-wmi-qualifiers.md) y [ **Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="2017d-106">[Dynamic](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>

    <span data-ttu-id="2017d-107">Puede asociar el calificador **dinámico** a una clase o una instancia.</span><span class="sxs-lookup"><span data-stu-id="2017d-107">You can attach the **Dynamic** qualifier to either a class or an instance.</span></span> <span data-ttu-id="2017d-108">El calificador **dinámico** marca la clase o instancia como administrada dinámicamente por un proveedor.</span><span class="sxs-lookup"><span data-stu-id="2017d-108">The **Dynamic** qualifier marks the class or instance as managed dynamically by a provider.</span></span> <span data-ttu-id="2017d-109">Cuando se muestra **Dynamic** en una clase o instancia, también debe aparecer el calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="2017d-109">When **Dynamic** appears on a class or instance, the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier must also appear.</span></span> <span data-ttu-id="2017d-110">El calificador de **proveedor** identifica el proveedor determinado que debe administrar la clase dinámica o la instancia.</span><span class="sxs-lookup"><span data-stu-id="2017d-110">The **Provider** qualifier identifies the particular provider that must manage the dynamic class or instance.</span></span>

-   [<span data-ttu-id="2017d-111">ClassContext</span><span class="sxs-lookup"><span data-stu-id="2017d-111">ClassContext</span></span>](standard-wmi-qualifiers.md)

    <span data-ttu-id="2017d-112">El calificador **ClassContext** se adjunta a una clase.</span><span class="sxs-lookup"><span data-stu-id="2017d-112">The **ClassContext** qualifier is attached to a class.</span></span> <span data-ttu-id="2017d-113">Especifica la ruta de acceso a la clave del registro que contiene la información que la clase representa.</span><span class="sxs-lookup"><span data-stu-id="2017d-113">It specifies the path to the registry key that contains the information the class represents.</span></span>

    <span data-ttu-id="2017d-114">El calificador **ClassContext** tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="2017d-114">The **ClassContext** qualifier has the following format.</span></span>

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    <span data-ttu-id="2017d-115">El valor de la ruta de clave puede ser largo si incluye claves con subclaves.</span><span class="sxs-lookup"><span data-stu-id="2017d-115">The value for KeyPath can be long if it includes keys with subkeys.</span></span>

    <span data-ttu-id="2017d-116">En el ejemplo siguiente se muestra el calificador **ClassContext** que contiene la ruta de acceso a un dispositivo de transporte de equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="2017d-116">The following example shows the **ClassContext** qualifier that contains the path to a particular computer transport device.</span></span>

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

<span data-ttu-id="2017d-117">La plantilla siguiente para una definición de clase muestra el uso de los calificadores **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)y **ClassContext** .</span><span class="sxs-lookup"><span data-stu-id="2017d-117">The following template for a class definition illustrates the use of the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **ClassContext** qualifiers.</span></span> <span data-ttu-id="2017d-118">El proveedor denominado por el calificador de **proveedor** es el proveedor del registro del sistema de la instancia.</span><span class="sxs-lookup"><span data-stu-id="2017d-118">The provider named by the **Provider** qualifier is the instance System Registry provider.</span></span> <span data-ttu-id="2017d-119">Tenga en cuenta que las rutas de acceso del registro no distinguen mayúsculas de minúsculas, como son los nombres de los calificadores.</span><span class="sxs-lookup"><span data-stu-id="2017d-119">Be aware that registry paths are case-insensitive, as are qualifier names.</span></span>

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

<span data-ttu-id="2017d-120">Las aplicaciones de administración también pueden utilizar el proveedor del registro del sistema para recuperar y modificar los datos del registro de una clave determinada.</span><span class="sxs-lookup"><span data-stu-id="2017d-120">Management applications can also use the System Registry provider to retrieve and modify registry data for a particular key.</span></span>

 

 



