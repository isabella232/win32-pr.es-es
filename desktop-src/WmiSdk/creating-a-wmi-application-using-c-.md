---
description: 'Para crear una aplicación para WMI mediante C++: debe inicializar COM, obtener acceso y establecer los protocolos WMI y realizar una limpieza manual.'
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Crear una aplicación WMI con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361280"
---
# <a name="creating-a-wmi-application-using-c"></a><span data-ttu-id="06134-103">Crear una aplicación WMI con C++</span><span class="sxs-lookup"><span data-stu-id="06134-103">Creating a WMI Application Using C++</span></span>

<span data-ttu-id="06134-104">Para crear una aplicación para WMI mediante C++: debe inicializar COM, obtener acceso y establecer los protocolos WMI y realizar una limpieza manual.</span><span class="sxs-lookup"><span data-stu-id="06134-104">To create an application for WMI using C++: you must initialize COM, access and set WMI protocols, and perform a manual cleanup.</span></span> <span data-ttu-id="06134-105">Sin embargo, C++ tiene la ventaja de flexibilidad y eficacia.</span><span class="sxs-lookup"><span data-stu-id="06134-105">However, C++ does have the advantage of flexibility and power.</span></span> <span data-ttu-id="06134-106">Por lo tanto, aunque se puede atender mejor en el uso de Visual Basic Scripting Edition (VBScript) o Windows PowerShell para procesos sencillos, C++ funciona mejor para aplicaciones más sofisticadas y es necesario para escribir [proveedores](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="06134-106">Therefore, while you are better served in using Visual Basic Scripting Edition (VBScript) or Windows PowerShell for simple processes, C++ works better for more sophisticated applications and is required for writing [providers](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="06134-107">En el procedimiento siguiente se describe cómo crear una aplicación WMI.</span><span class="sxs-lookup"><span data-stu-id="06134-107">The following procedure describes how to create a WMI application.</span></span>

<span data-ttu-id="06134-108">**Para crear una aplicación WMI**</span><span class="sxs-lookup"><span data-stu-id="06134-108">**To create a WMI application**</span></span>

1.  <span data-ttu-id="06134-109">[Inicializar com](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="06134-109">[Initialize COM](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="06134-110">Dado que WMI se basa en la tecnología COM, debe realizar llamadas a las funciones [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para tener acceso a WMI.</span><span class="sxs-lookup"><span data-stu-id="06134-110">Because WMI is based on COM technology, you must perform calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span>

2.  <span data-ttu-id="06134-111">[Cree una conexión a un espacio de nombres WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="06134-111">[Create a connection to a WMI namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

    <span data-ttu-id="06134-112">Por definición, WMI se ejecuta en un proceso diferente del de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="06134-112">By definition, WMI runs in a different process than your application.</span></span> <span data-ttu-id="06134-113">Por lo tanto, debe crear una conexión entre la aplicación y WMI.</span><span class="sxs-lookup"><span data-stu-id="06134-113">Therefore, you must create a connection between your application and WMI.</span></span>

3.  <span data-ttu-id="06134-114">[Establezca los niveles de seguridad en la conexión WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="06134-114">[Set the security levels on the WMI connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

    <span data-ttu-id="06134-115">Para usar la conexión que cree a WMI, debe establecer los niveles de suplantación y autenticación para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="06134-115">To use the connection you create to WMI, you must set the impersonation and authentication levels for your application.</span></span>

4.  <span data-ttu-id="06134-116">Implemente el propósito de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="06134-116">Implement the purpose of your application.</span></span>

    <span data-ttu-id="06134-117">WMI expone una variedad de interfaces COM que se usan para obtener acceso a los datos de toda la empresa y manipularlos.</span><span class="sxs-lookup"><span data-stu-id="06134-117">WMI exposes a variety of COM interfaces use to access and manipulate data across your enterprise.</span></span> <span data-ttu-id="06134-118">Para obtener más información, vea [manipular información de clase e instancia](manipulating-class-and-instance-information.md), [recibir un evento WMI](receiving-a-wmi-event.md)y [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="06134-118">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Receiving a WMI Event](receiving-a-wmi-event.md), and [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="06134-119">Aquí es donde debe existir la mayor parte de la aplicación cliente WMI, como el acceso a objetos WMI o la manipulación de datos.</span><span class="sxs-lookup"><span data-stu-id="06134-119">This is where the bulk of your WMI client application should exist, such as accessing WMI objects or manipulating data.</span></span>

5.  <span data-ttu-id="06134-120">[Limpieza y cierre de la aplicación](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="06134-120">[Cleanup and shut down your application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

    <span data-ttu-id="06134-121">Después de completar las consultas en WMI, debe destruir todos los punteros COM y cerrar la aplicación correctamente.</span><span class="sxs-lookup"><span data-stu-id="06134-121">After you complete your queries to WMI, you should destroy all COM pointers and shut down your application correctly.</span></span>

<span data-ttu-id="06134-122">Para obtener más información y un ejemplo de código sobre cómo crear una aplicación WMI, vea [ejemplo: crear una aplicación WMI](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="06134-122">For more information and a code example about how to create a WMI application, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

 

 
