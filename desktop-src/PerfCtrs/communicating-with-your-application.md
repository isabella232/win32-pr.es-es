---
description: Normalmente, un proveedor proporciona datos en nombre de una aplicación.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Comunicación con la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909749"
---
# <a name="communicating-with-your-application"></a><span data-ttu-id="f72c6-103">Comunicación con la aplicación</span><span class="sxs-lookup"><span data-stu-id="f72c6-103">Communicating With Your Application</span></span>

<span data-ttu-id="f72c6-104">Normalmente, un proveedor proporciona datos en nombre de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f72c6-104">Typically, a provider provides data on behalf of an application.</span></span> <span data-ttu-id="f72c6-105">Por ejemplo, un servidor puede crear un archivo DLL de rendimiento para proporcionar los datos del contador.</span><span class="sxs-lookup"><span data-stu-id="f72c6-105">For example, a server might create a performance DLL to provide its counter data.</span></span> <span data-ttu-id="f72c6-106">La comunicación entre una aplicación y su proveedor varía en lo que se refiere a las aplicaciones en modo de usuario y de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="f72c6-106">Communication between an application and its provider differs for user-mode and kernel-mode applications.</span></span> <span data-ttu-id="f72c6-107">Los proveedores se ejecutan en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="f72c6-107">Providers execute in user mode.</span></span> <span data-ttu-id="f72c6-108">Debido a esto, las aplicaciones de modo de usuario, como las aplicaciones de impresión y visualización, pueden utilizar cualquier técnica para la comunicación entre procesos, como canalizaciones con nombre, asignación de archivos o RPC.</span><span class="sxs-lookup"><span data-stu-id="f72c6-108">Because of this, user-mode applications, such as print and display applications, can use any technique for interprocess communication, such as named pipes, file mapping, or RPC.</span></span> <span data-ttu-id="f72c6-109">Sin embargo, las aplicaciones de modo kernel deben proporcionar una interfaz IOCTL que devuelva los datos de rendimiento al proveedor.</span><span class="sxs-lookup"><span data-stu-id="f72c6-109">However, kernel-mode applications must provide an IOCTL interface that returns the performance data to the provider.</span></span>

> [!WARNING]
> <span data-ttu-id="f72c6-110">No utilice COM como mecanismo IPC.</span><span class="sxs-lookup"><span data-stu-id="f72c6-110">Do not use COM as the IPC mechanism.</span></span> <span data-ttu-id="f72c6-111">El sistema no puede garantizar el estado de inicialización de COM del subproceso que llama a la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f72c6-111">The system cannot guarantee the COM initialization state of the thread calling the interface.</span></span> <span data-ttu-id="f72c6-112">Por lo tanto, es posible que la DLL no pueda inicializar COM correctamente y recopilar los datos.</span><span class="sxs-lookup"><span data-stu-id="f72c6-112">Therefore, the DLL may not be able to successfully initialize COM and collect the data.</span></span>

 

 

 



