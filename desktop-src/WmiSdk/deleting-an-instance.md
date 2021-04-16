---
description: La eliminación de una instancia es el comando de eliminación más común que es probable que se realice en WMI.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Eliminar una instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706167"
---
# <a name="deleting-an-instance"></a><span data-ttu-id="95984-103">Eliminar una instancia</span><span class="sxs-lookup"><span data-stu-id="95984-103">Deleting an Instance</span></span>

<span data-ttu-id="95984-104">La eliminación de una instancia es el comando de eliminación más común que es probable que se realice en WMI.</span><span class="sxs-lookup"><span data-stu-id="95984-104">Deleting an instance is the most common delete command you are likely to perform in WMI.</span></span> <span data-ttu-id="95984-105">Al igual que cuando se elimina una clase, el comando real es bastante sencillo.</span><span class="sxs-lookup"><span data-stu-id="95984-105">Like deleting a class, the actual command is fairly simple.</span></span> <span data-ttu-id="95984-106">Sin embargo, WMI funciona de forma bastante diferente según el tipo de instancia que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="95984-106">However, WMI performs quite differently depending on the type of instance you are deleting.</span></span> <span data-ttu-id="95984-107">Si la instancia es estática, WMI simplemente elimina la instancia del repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="95984-107">If the instance is static, WMI simply deletes the instance from the WMI repository.</span></span> <span data-ttu-id="95984-108">Para obtener información acerca de cómo quitar clases e instancias del repositorio WMI, vea el comando de preprocesador [**pragma deleteclass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="95984-108">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="95984-109">Si la instancia es dinámica, WMI debe llamar a [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) en los proveedores responsables de las siguientes clases:</span><span class="sxs-lookup"><span data-stu-id="95984-109">If the instance is dynamic, WMI must call [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) on the providers that are responsible for the following classes:</span></span>

-   <span data-ttu-id="95984-110">Clase a la que pertenece la instancia.</span><span class="sxs-lookup"><span data-stu-id="95984-110">The class that owns the instance.</span></span>
-   <span data-ttu-id="95984-111">Cada clase primaria de la clase a la que pertenece la instancia.</span><span class="sxs-lookup"><span data-stu-id="95984-111">Every parent class of the class that owns the instance.</span></span>
-   <span data-ttu-id="95984-112">Cada subclase de la clase a la que pertenece la instancia.</span><span class="sxs-lookup"><span data-stu-id="95984-112">Every subclass of the class that owns the instance.</span></span>

<span data-ttu-id="95984-113">El éxito de la eliminación depende de la clase no abstracta de nivel superior para la instancia original.</span><span class="sxs-lookup"><span data-stu-id="95984-113">The success of the deletion depends on the topmost nonabstract class for the original instance.</span></span> <span data-ttu-id="95984-114">Si el proveedor de cualquier clase no abstracta de nivel superior consigue completar la eliminación, la operación se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="95984-114">If the provider for any topmost nonabstract class succeeds in completing the deletion, the operation succeeds.</span></span> <span data-ttu-id="95984-115">Para obtener más información, vea la sección Comentarios de [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span><span class="sxs-lookup"><span data-stu-id="95984-115">For more information, see the Remarks section of [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span></span>

<span data-ttu-id="95984-116">La [API de com para WMI](com-api-for-wmi.md) tiene distintos métodos para eliminar una instancia y eliminar un objeto.</span><span class="sxs-lookup"><span data-stu-id="95984-116">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="95984-117">En el procedimiento siguiente se describe cómo usar C++ para eliminar una instancia de una clase base o una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="95984-117">The following procedure describes how to use C++ to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="95984-118">**Para eliminar una instancia de una clase base o una clase derivada mediante C++**</span><span class="sxs-lookup"><span data-stu-id="95984-118">**To delete an instance of a base class or derived class using C++**</span></span>

-   <span data-ttu-id="95984-119">Llame a los métodos [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="95984-119">Call either the [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) methods.</span></span>

    <span data-ttu-id="95984-120">Como sugiere el nombre, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) elimina una instancia de forma asincrónica mientras que [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) elimina una instancia sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="95984-120">As the name suggests, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) deletes an instance asynchronously while [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) deletes an instance synchronously.</span></span> <span data-ttu-id="95984-121">Para usar **DeleteInstanceAsync**, también debe implementar un objeto [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="95984-121">To use **DeleteInstanceAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="95984-122">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="95984-122">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="95984-123">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="95984-123">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="95984-124">La [API de scripting para WMI](scripting-api-for-wmi.md) usa los mismos métodos para eliminar un objeto de clase o una instancia de.</span><span class="sxs-lookup"><span data-stu-id="95984-124">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span>

<span data-ttu-id="95984-125">En el procedimiento siguiente se describe cómo usar VBScript para eliminar una instancia de una clase base o una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="95984-125">The following procedure describes how to use VBScript to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="95984-126">**Para eliminar una instancia de una clase base o una clase derivada mediante VBScript**</span><span class="sxs-lookup"><span data-stu-id="95984-126">**To delete an instance of a base class or derived class using VBScript**</span></span>

-   <span data-ttu-id="95984-127">Llame a los métodos [**SWbemObject. \_ Delete**](swbemobject-delete-.md) o [**SWbemObject. \_ DeleteAsync**](swbemobject-deleteasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="95984-127">Call either the [**SWbemObject.Delete\_**](swbemobject-delete-.md) or [**SWbemObject.DeleteAsync\_**](swbemobject-deleteasync-.md) methods.</span></span>

    <span data-ttu-id="95984-128">Como sugiere el nombre, [**Delete \_**](swbemobject-delete-.md) elimina una instancia sincrónicamente, mientras que [**DeleteAsync \_**](swbemobject-deleteasync-.md) elimina una instancia de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="95984-128">As the name suggests, [**Delete\_**](swbemobject-delete-.md) deletes an instance synchronously while [**DeleteAsync\_**](swbemobject-deleteasync-.md) deletes an instance asynchronously.</span></span> <span data-ttu-id="95984-129">Para obtener más información sobre cómo eliminar una instancia de forma asincrónica, vea [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="95984-129">For more information about deleting an instance asynchronously, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="95984-130">En el ejemplo siguiente se describe cómo eliminar una instancia de mediante VBScript.</span><span class="sxs-lookup"><span data-stu-id="95984-130">The following example describes how to delete an instance using VBScript.</span></span>

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> <span data-ttu-id="95984-131">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="95984-131">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="95984-132">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="95984-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



