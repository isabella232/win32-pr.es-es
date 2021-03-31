---
description: Además de las clases e instancias, WMI permite modificar un método. La razón principal por la que desea modificar un método es si ha cambiado la implementación de un método en un proveedor. Para obtener más información, consulte escribir un proveedor de métodos.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Modificar un método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423596"
---
# <a name="modifying-a-method"></a><span data-ttu-id="60d4e-105">Modificar un método</span><span class="sxs-lookup"><span data-stu-id="60d4e-105">Modifying a Method</span></span>

<span data-ttu-id="60d4e-106">Además de las clases e instancias, WMI permite modificar un método.</span><span class="sxs-lookup"><span data-stu-id="60d4e-106">In addition to classes and instances, WMI allows you to modify a method.</span></span> <span data-ttu-id="60d4e-107">La razón principal por la que desea modificar un método es si ha cambiado la implementación de un método en un proveedor.</span><span class="sxs-lookup"><span data-stu-id="60d4e-107">The main reason you would want to modify a method is if you changed the implementation of a method in a provider.</span></span> <span data-ttu-id="60d4e-108">Para obtener más información, consulte [escribir un proveedor de métodos](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="60d4e-108">For more information, see [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="60d4e-109">Modificar un método no es una operación que se puede realizar en el script.</span><span class="sxs-lookup"><span data-stu-id="60d4e-109">Modifying a method is not an operation that can be done in script.</span></span>

<span data-ttu-id="60d4e-110">En el procedimiento siguiente se describe cómo modificar un método mediante programación.</span><span class="sxs-lookup"><span data-stu-id="60d4e-110">The following procedure describes how to modify a method programmatically.</span></span>

<span data-ttu-id="60d4e-111">**Para modificar un método mediante programación**</span><span class="sxs-lookup"><span data-stu-id="60d4e-111">**To modify a method programmatically**</span></span>

1.  <span data-ttu-id="60d4e-112">Recupere la definición de clase con una llamada a [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span><span class="sxs-lookup"><span data-stu-id="60d4e-112">Retrieve the class definition with a call to [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span></span>

    <span data-ttu-id="60d4e-113">Los dos parámetros out, *ppInSignature* y *ppOutSignature*, contienen la clase in-parameter y la clase out-Parameter, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="60d4e-113">The two out parameters, *ppInSignature* and *ppOutSignature*, contain the in-parameter class and the out-parameter class, respectively.</span></span> <span data-ttu-id="60d4e-114">El valor devuelto se incluye en la clase out-Parameter como una propiedad y se debe denominar **ReturnValue**.</span><span class="sxs-lookup"><span data-stu-id="60d4e-114">The return value is bundled into the out-parameter class as a property, and should be named **ReturnValue**.</span></span>

2.  <span data-ttu-id="60d4e-115">Recupere y modifique los parámetros con llamadas a [**IWbemClassObject:: get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)o [**IWbemClassObject::D iminar**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span><span class="sxs-lookup"><span data-stu-id="60d4e-115">Retrieve and modify the parameters with calls to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put), or [**IWbemClassObject::Delete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span></span>
3.  <span data-ttu-id="60d4e-116">Vuelva a colocar la nueva versión del método en la clase primaria con una llamada a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="60d4e-116">Place your new version of the method back into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="60d4e-117">Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="60d4e-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



