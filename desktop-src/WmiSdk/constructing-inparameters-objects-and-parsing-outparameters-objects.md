---
description: Normalmente, el acceso directo es adecuado para llamar a un método de proveedor WMI.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Construir objetos Parameters y analizar objetos Parameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002435"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a><span data-ttu-id="09a1c-103">Construir objetos Parameters y analizar objetos Parameters</span><span class="sxs-lookup"><span data-stu-id="09a1c-103">Constructing InParameters Objects and Parsing OutParameters Objects</span></span>

<span data-ttu-id="09a1c-104">Normalmente, el acceso directo es adecuado para llamar a un [*método de proveedor*](gloss-p.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="09a1c-104">Normally, direct access is adequate to call a WMI [*provider method*](gloss-p.md).</span></span> <span data-ttu-id="09a1c-105">El acceso directo significa ejecutar un método usando la sintaxis *Object. Method* .</span><span class="sxs-lookup"><span data-stu-id="09a1c-105">Direct access means executing a method by using *object.method* syntax.</span></span> <span data-ttu-id="09a1c-106">Sin embargo, en algunos casos, no se puede usar el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="09a1c-106">However, in some cases, direct access cannot be used.</span></span> <span data-ttu-id="09a1c-107">Además, llamar a un método de proveedor de forma asincrónica desde un script requiere un tipo de llamada [**ExecMethodAsync**](swbemobject-execmethodasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="09a1c-107">Also, calling a provider method asynchronously from a script requires an [**ExecMethodAsync**](swbemobject-execmethodasync-.md) type of call.</span></span>

> [!Note]  
> <span data-ttu-id="09a1c-108">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="09a1c-108">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="09a1c-109">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="09a1c-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="09a1c-110">El orden de los parámetros de entrada y salida del método se define en el esquema de Managed Object Format (MOF) del método.</span><span class="sxs-lookup"><span data-stu-id="09a1c-110">The order of method input and output parameters is defined in the Managed Object Format (MOF) schema for the method.</span></span> <span data-ttu-id="09a1c-111">WMI no impide que se cambie el orden de los parámetros cuando [MOFCOMP](mofcomp.md)vuelve a compilar la clase.</span><span class="sxs-lookup"><span data-stu-id="09a1c-111">WMI does not prevent the parameter order from being changed when the class is recompiled by [mofcomp](mofcomp.md).</span></span> <span data-ttu-id="09a1c-112">Mediante el uso de un objeto [**Parameters**](swbemmethod-inparameters.md) , puede evitar problemas derivados del esquema modificado porque los parámetros de entrada se identifican por su nombre.</span><span class="sxs-lookup"><span data-stu-id="09a1c-112">By using an [**InParameters**](swbemmethod-inparameters.md) object, you can avoid problems that result from changed schema because the input parameters are identified by name.</span></span> <span data-ttu-id="09a1c-113">El parámetro correcto puede verse examinando el calificador de **identificador** de cada parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="09a1c-113">The correct parameter can be seen by examining the **ID** qualifier of each input parameter.</span></span> <span data-ttu-id="09a1c-114">El primer parámetro tiene un valor de **identificador** de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="09a1c-114">The first parameter has an **ID** value of 0 (zero).</span></span>

<span data-ttu-id="09a1c-115">[**Los métodos SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)y [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) proporcionan una manera alternativa de ejecutar un método de proveedor en los casos en los que no es posible ejecutar un método directamente.</span><span class="sxs-lookup"><span data-stu-id="09a1c-115">[**The SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods provide an alternate way to execute a provider method in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="09a1c-116">Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="09a1c-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="09a1c-117">Para obtener más información sobre los parámetros, vea [construir objetos Parameters](constructing-inparameters-objects.md) y [analizar objetos Parameters](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="09a1c-117">For more information about parameters, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

 

 



