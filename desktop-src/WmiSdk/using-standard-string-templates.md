---
description: Varios consumidores, como el consumidor de eventos de script activo o el consumidor de eventos de línea de comandos, tienen propiedades de cadena con el calificador de plantilla.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Usar plantillas de cadena estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911485"
---
# <a name="using-standard-string-templates"></a><span data-ttu-id="7e17b-103">Usar plantillas de cadena estándar</span><span class="sxs-lookup"><span data-stu-id="7e17b-103">Using Standard String Templates</span></span>

<span data-ttu-id="7e17b-104">Varios consumidores, como el consumidor de eventos de script activo o el consumidor de eventos de línea de comandos, tienen propiedades de cadena con el calificador de **plantilla** .</span><span class="sxs-lookup"><span data-stu-id="7e17b-104">Several consumers, such as the Active Script Event Consumer or the Command Line Event Consumer, have string properties with the **Template** qualifier.</span></span> <span data-ttu-id="7e17b-105">Estas propiedades usan plantillas de cadena estándar para construir una cadena que está configurada en la parte por la instancia del consumidor y en parte por un evento.</span><span class="sxs-lookup"><span data-stu-id="7e17b-105">These properties use standard string templates to construct a string that is configured in part by the consumer instance and in part by an event.</span></span> <span data-ttu-id="7e17b-106">La estructura de una plantilla de cadena estándar es similar a la especificación de variable de entorno de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7e17b-106">The structure of a standard string template is similar to the Microsoft Windows environment variable specification.</span></span>

<span data-ttu-id="7e17b-107">En la lista siguiente se muestran algunos ejemplos del lenguaje de la plantilla:</span><span class="sxs-lookup"><span data-stu-id="7e17b-107">The following list shows some examples of the template language:</span></span>

-   <span data-ttu-id="7e17b-108">La cadena "Some Text here" siempre genera la cadena "Some Text here".</span><span class="sxs-lookup"><span data-stu-id="7e17b-108">The string "Some text here" always produces the string "Some text here".</span></span>
-   <span data-ttu-id="7e17b-109">"% Gráfico%" siempre genera el valor de la propiedad **gráfico** del evento que se va a entregar.</span><span class="sxs-lookup"><span data-stu-id="7e17b-109">"%CPUUtilization%" always produces the value of the **CPUUtilization** property of the event being delivered.</span></span> <span data-ttu-id="7e17b-110">Si la propiedad no es una cadena, se convierte en una cadena; por ejemplo, "90" o "TRUE".</span><span class="sxs-lookup"><span data-stu-id="7e17b-110">If the property is not a string, it is converted to a string; for example, "90" or "TRUE".</span></span>
-   <span data-ttu-id="7e17b-111">"El uso de CPU de este procesador es% gráfico% en este momento" inserta el valor de la propiedad **gráfico** del evento en la cadena, lo que genera algo parecido a "el uso de CPU de este procesador es 90 en este momento".</span><span class="sxs-lookup"><span data-stu-id="7e17b-111">"The CPU utilization of this processor is %CPUUtilization% at this time" embeds the value of the **CPUUtilization** property of the event into the string, producing something like, "The CPU utilization of this processor is 90 at this time".</span></span>
-   <span data-ttu-id="7e17b-112">"% TargetInstance. gráfico%" recupera el valor de la propiedad **gráfico** en la instancia insertada de la propiedad **TargetInstance** .</span><span class="sxs-lookup"><span data-stu-id="7e17b-112">"%TargetInstance.CPUUtilization%" retrieves the value of the **CPUUtilization** property in the embedded instance of the **TargetInstance** property.</span></span>
-   <span data-ttu-id="7e17b-113">"%%" genera un único signo de%.</span><span class="sxs-lookup"><span data-stu-id="7e17b-113">"%%" produces a single % sign.</span></span>
-   <span data-ttu-id="7e17b-114">Si la propiedad que se va a recuperar es una matriz, toda la matriz se produce con el siguiente formato: "(1, 5, 10, 1024)".</span><span class="sxs-lookup"><span data-stu-id="7e17b-114">If the property being retrieved is an array, the entire array is produced in the following format: "(1,5,10,1024)".</span></span> <span data-ttu-id="7e17b-115">Si solo hay un elemento en la matriz, se omiten los paréntesis.</span><span class="sxs-lookup"><span data-stu-id="7e17b-115">If there is only one element in the array, the parentheses are omitted.</span></span> <span data-ttu-id="7e17b-116">Si no hay ningún elemento en la matriz, se genera "()".</span><span class="sxs-lookup"><span data-stu-id="7e17b-116">If there are no elements in the array, "()" is produced.</span></span>
-   <span data-ttu-id="7e17b-117">Si una propiedad es un objeto incrustado, se genera la representación MOF del objeto (similar al método [**IWbemClassObject:: GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) ).</span><span class="sxs-lookup"><span data-stu-id="7e17b-117">If a property is an embedded object, the MOF representation of the object is produced (similar to the [**IWbemClassObject::GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) method).</span></span>
-   <span data-ttu-id="7e17b-118">Si se solicita una propiedad de una matriz incrustada de objetos, se trata como una propiedad con un valor de matriz.</span><span class="sxs-lookup"><span data-stu-id="7e17b-118">If a property of an embedded array of objects is requested, it is treated as a property with an array value.</span></span> <span data-ttu-id="7e17b-119">Por ejemplo:% DoEvents. TargetInstance. DriverLetter% podría producir ' ("C:", "D:") ' si DoEvents es una matriz de eventos de modificación de instancia incrustados.</span><span class="sxs-lookup"><span data-stu-id="7e17b-119">For example: %MyEvents.TargetInstance.DriverLetter% could produce '("C:","D:")' if MyEvents is an array of embedded instance modification events.</span></span>

## <a name="string-literals"></a><span data-ttu-id="7e17b-120">Literales de cadena</span><span class="sxs-lookup"><span data-stu-id="7e17b-120">String Literals</span></span>

<span data-ttu-id="7e17b-121">Todo lo que se encuentre dentro de un par de Comillas se considera un literal de cadena y no se reemplazará.</span><span class="sxs-lookup"><span data-stu-id="7e17b-121">Anything inside a pair of quotes is considered a string literal and will not be replaced.</span></span>

<span data-ttu-id="7e17b-122">En el ejemplo siguiente se muestra la cadena que el compilador ve para "el uso de la CPU es% gráfico%".</span><span class="sxs-lookup"><span data-stu-id="7e17b-122">The following example shows the string that the compiler sees for "CPU utilization is %CPUUtilization%".</span></span>

``` syntax
CPU utilization is %CPUUtilization%
```

<span data-ttu-id="7e17b-123">Esta cadena genera el siguiente resultado.</span><span class="sxs-lookup"><span data-stu-id="7e17b-123">This string produces the following output.</span></span>

``` syntax
CPU utilization is 90
```

<span data-ttu-id="7e17b-124">Por otro lado, el compilador verá la cadena "el uso de CPU es \\ "% gráfico% \\ "" como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="7e17b-124">On the other hand, the string "CPU utilization is \\"%CPUUtilization%\\"" is seen by the compiler as follows.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

<span data-ttu-id="7e17b-125">Esta cadena genera el siguiente resultado, sin sustitución de variables.</span><span class="sxs-lookup"><span data-stu-id="7e17b-125">This string produces the following output, with no variable substitution.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a><span data-ttu-id="7e17b-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e17b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e17b-127">Supervisión y respuesta a eventos con consumidores estándar</span><span class="sxs-lookup"><span data-stu-id="7e17b-127">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



