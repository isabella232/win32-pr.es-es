---
description: A diferencia de la eliminación de una instancia dinámica, la eliminación de una clase es un procedimiento sencillo.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Eliminar una clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706815"
---
# <a name="deleting-a-class"></a><span data-ttu-id="3413b-103">Eliminar una clase</span><span class="sxs-lookup"><span data-stu-id="3413b-103">Deleting a Class</span></span>

<span data-ttu-id="3413b-104">A diferencia de la eliminación de una instancia dinámica, la eliminación de una clase es un procedimiento sencillo.</span><span class="sxs-lookup"><span data-stu-id="3413b-104">Unlike deleting a dynamic instance, deleting a class is a simple procedure.</span></span> <span data-ttu-id="3413b-105">Sin embargo, como se explicó anteriormente, las clases base o derivadas rara vez se eliminan.</span><span class="sxs-lookup"><span data-stu-id="3413b-105">However, as discussed earlier, base or derived classes are rarely deleted.</span></span> <span data-ttu-id="3413b-106">En su lugar, una instancia se elimina más comúnmente.</span><span class="sxs-lookup"><span data-stu-id="3413b-106">Instead, an instance is more commonly deleted.</span></span> <span data-ttu-id="3413b-107">La [API de scripting para WMI](scripting-api-for-wmi.md) usa los mismos métodos para eliminar un objeto de clase o una instancia de.</span><span class="sxs-lookup"><span data-stu-id="3413b-107">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span> <span data-ttu-id="3413b-108">Para obtener más información, consulte [eliminar una instancia](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="3413b-108">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span> <span data-ttu-id="3413b-109">Para obtener información acerca de cómo quitar clases e instancias del repositorio WMI, vea el comando de preprocesador [**pragma deleteclass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="3413b-109">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="3413b-110">La [API de com para WMI](com-api-for-wmi.md) tiene distintos métodos para eliminar una instancia y eliminar un objeto.</span><span class="sxs-lookup"><span data-stu-id="3413b-110">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="3413b-111">En el procedimiento siguiente se describe cómo eliminar una clase base o una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="3413b-111">The following procedure describes how to delete a base class or derived class.</span></span>

<span data-ttu-id="3413b-112">**Para eliminar una clase base o una clase derivada**</span><span class="sxs-lookup"><span data-stu-id="3413b-112">**To delete a base class or derived class**</span></span>

-   <span data-ttu-id="3413b-113">Llame al método [**IWbemServices::D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) o [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) .</span><span class="sxs-lookup"><span data-stu-id="3413b-113">Call either the [**IWbemServices::DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) or [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) method.</span></span>

    <span data-ttu-id="3413b-114">Como sugiere el nombre, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) elimina una instancia de forma asincrónica, mientras que [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) elimina una instancia sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="3413b-114">As the name suggests, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) deletes an instance asynchronously while [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) deletes an instance synchronously.</span></span> <span data-ttu-id="3413b-115">Para usar **DeleteClassAsync**, también debe implementar un objeto [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="3413b-115">To use **DeleteClassAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="3413b-116">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3413b-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="3413b-117">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="3413b-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



