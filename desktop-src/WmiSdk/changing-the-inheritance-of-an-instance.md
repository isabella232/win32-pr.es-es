---
description: Es posible que encuentre una situación en la que una instancia creada como elemento secundario de una clase primaria debe cambiar las clases primarias y convertirse en el elemento secundario de una clase primaria diferente.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Cambiar la herencia de una instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910294"
---
# <a name="changing-the-inheritance-of-an-instance"></a><span data-ttu-id="aa3c7-103">Cambiar la herencia de una instancia</span><span class="sxs-lookup"><span data-stu-id="aa3c7-103">Changing the Inheritance of an Instance</span></span>

<span data-ttu-id="aa3c7-104">Es posible que encuentre una situación en la que una instancia creada como elemento secundario de una clase primaria debe cambiar las clases primarias y convertirse en el elemento secundario de una clase primaria diferente.</span><span class="sxs-lookup"><span data-stu-id="aa3c7-104">You may find a situation where an instance that was created as a child of one parent class must change parent classes and become the child of a different parent class.</span></span> <span data-ttu-id="aa3c7-105">Por ejemplo, puede tener una clase derivada, **ManualService**, que describe un servicio manual y una clase derivada, **autoservicio**, que describe un servicio automático.</span><span class="sxs-lookup"><span data-stu-id="aa3c7-105">For example, you may have a derived class, **ManualService**, describing a manual service, and a derived class, **AutoService**, describing an automatic service.</span></span> <span data-ttu-id="aa3c7-106">Ambas clases tienen un gran número de propiedades.</span><span class="sxs-lookup"><span data-stu-id="aa3c7-106">Both classes have a large number of properties.</span></span> <span data-ttu-id="aa3c7-107">No todas las propiedades son idénticas.</span><span class="sxs-lookup"><span data-stu-id="aa3c7-107">Not all properties are identical.</span></span> <span data-ttu-id="aa3c7-108">Para cambiar un servicio de manual a automático, también debe cambiar la instancia que representa el servicio de **ManualService** a **autoservicio**.</span><span class="sxs-lookup"><span data-stu-id="aa3c7-108">To change a service from manual to automatic, you must also change the instance representing the service from **ManualService** to **AutoService**.</span></span> <span data-ttu-id="aa3c7-109">En la versión actual de WMI, no se puede llamar al método [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) con el parámetro *PIN* que apunta a una instancia de **Autoservice** y a las propiedades de clave que describen la instancia de **ManualService** .</span><span class="sxs-lookup"><span data-stu-id="aa3c7-109">In the current version of WMI, you cannot call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) method with the *pInst* parameter pointing to an instance of **AutoService** and the key properties describing the **ManualService** instance.</span></span> <span data-ttu-id="aa3c7-110">Si lo hace, se elimina implícitamente la instancia de **ManualService** original.</span><span class="sxs-lookup"><span data-stu-id="aa3c7-110">If you do, you implicitly delete the original **ManualService** instance.</span></span> <span data-ttu-id="aa3c7-111">En esencia, después de establecer la clase de una instancia, solo se puede cambiar la clase primaria de una instancia mediante la eliminación de la instancia y volver a crear la instancia como una instancia de la nueva clase primaria.</span><span class="sxs-lookup"><span data-stu-id="aa3c7-111">In essence, after you establish the class of an instance, you can only change the parent class of an instance by deleting the instance and recreating the instance as an instance of the new parent class.</span></span>

<span data-ttu-id="aa3c7-112">En el procedimiento siguiente se describe cómo se mueve una instancia de una clase a otra.</span><span class="sxs-lookup"><span data-stu-id="aa3c7-112">The following procedure describes how to move an instance from one class to another class.</span></span>

<span data-ttu-id="aa3c7-113">**Para trasladar una instancia de una clase a otra**</span><span class="sxs-lookup"><span data-stu-id="aa3c7-113">**To move an instance from one class to another class**</span></span>

1.  <span data-ttu-id="aa3c7-114">Elimine la instancia de la clase original.</span><span class="sxs-lookup"><span data-stu-id="aa3c7-114">Delete the instance from the original class.</span></span>
2.  <span data-ttu-id="aa3c7-115">Cree la instancia en la nueva clase.</span><span class="sxs-lookup"><span data-stu-id="aa3c7-115">Create the instance under the new class.</span></span>

    <span data-ttu-id="aa3c7-116">WMI no permite que las aplicaciones muevan una instancia creando en la nueva clase y, a continuación, actualizándolos con la clave de la instancia original.</span><span class="sxs-lookup"><span data-stu-id="aa3c7-116">WMI does not allow applications to move an instance by creating it in the new class and then updating it with the key of the original instance.</span></span>

<span data-ttu-id="aa3c7-117">Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c7-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



