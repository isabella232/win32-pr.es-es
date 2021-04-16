---
description: Otra forma de crear un espacio de nombres es usar la API de WMI para crear el espacio de nombres mediante programación.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Crear un espacio de nombres con la API de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715840"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a><span data-ttu-id="7b60f-103">Crear un espacio de nombres con la API de WMI</span><span class="sxs-lookup"><span data-stu-id="7b60f-103">Creating a Namespace with the WMI API</span></span>

<span data-ttu-id="7b60f-104">Otra forma de crear un espacio de nombres es usar la API de WMI para crear el espacio de nombres mediante programación.</span><span class="sxs-lookup"><span data-stu-id="7b60f-104">Another way of creating a namespace is to use the WMI API to create the namespace programmatically.</span></span> <span data-ttu-id="7b60f-105">La ventaja de crear un espacio de nombres mediante programación es que se puede crear el espacio de nombres desde dentro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="7b60f-105">The advantage to creating a namespace programmatically is that you can create the namespace from within an application.</span></span> <span data-ttu-id="7b60f-106">Sin embargo, el uso de la API de WMI es más complejo que el uso de código de Managed Object Format (MOF) y no se pueden compartir fácilmente los espacios de nombres con otros desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="7b60f-106">However, using the WMI API is more complex than using Managed Object Format (MOF) code, and you cannot as easily share your namespaces with other developers.</span></span>

<span data-ttu-id="7b60f-107">En el procedimiento siguiente se describe cómo crear un espacio de nombres mediante la API de WMI.</span><span class="sxs-lookup"><span data-stu-id="7b60f-107">The following procedure describes how to create a namespace using the WMI API.</span></span>

<span data-ttu-id="7b60f-108">**Para crear un espacio de nombres mediante la API de WMI**</span><span class="sxs-lookup"><span data-stu-id="7b60f-108">**To create a namespace using the WMI API**</span></span>

1.  <span data-ttu-id="7b60f-109">Use [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar un puntero a un objeto [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que apunte a la clase de sistema de [**\_ \_ espacio de nombres**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="7b60f-109">Use [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a pointer to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) object that points to the [**\_\_Namespace**](--namespace.md) system class.</span></span>
2.  <span data-ttu-id="7b60f-110">Defina una instancia de la clase de sistema de [**\_ \_ espacio de nombres**](--namespace.md) con una llamada a [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span><span class="sxs-lookup"><span data-stu-id="7b60f-110">Define an instance of the [**\_\_Namespace**](--namespace.md) system class with a call to [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span></span>
3.  <span data-ttu-id="7b60f-111">Establezca la propiedad **Name** de la instancia de [**\_ \_ espacio de nombres**](--namespace.md) con una llamada a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="7b60f-111">Set the **Name** property of the [**\_\_Namespace**](--namespace.md) instance with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>
4.  <span data-ttu-id="7b60f-112">Cree el espacio de nombres con una llamada a [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span><span class="sxs-lookup"><span data-stu-id="7b60f-112">Create the namespace with a call to [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span></span>

    <span data-ttu-id="7b60f-113">El parámetro *PIN* de [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) debe apuntar a la nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="7b60f-113">The *pInst* parameter of [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) should point to the new instance.</span></span>

 

 



