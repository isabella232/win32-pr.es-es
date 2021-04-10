---
title: Registrar servidores COM
description: Registrar servidores COM
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149642"
---
# <a name="registering-com-servers"></a><span data-ttu-id="e3f16-103">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="e3f16-103">Registering COM Servers</span></span>

<span data-ttu-id="e3f16-104">Después de haber definido una clase en el código (asegurándose de que implementa [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) o [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) y le ha asignado un CLSID, debe colocar información en el registro que permita que com, a petición de un cliente con el CLSID, cree instancias de sus objetos.</span><span class="sxs-lookup"><span data-stu-id="e3f16-104">After you have defined a class in code (ensuring that it implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) and assigned it a CLSID, you need to put information in the registry that will allow COM, on request of a client with the CLSID, to create instances of its objects.</span></span> <span data-ttu-id="e3f16-105">Esta información indica al sistema, para un CLSID determinado, donde se encuentra el código del archivo DLL o EXE para esa clase y cómo se inicia.</span><span class="sxs-lookup"><span data-stu-id="e3f16-105">This information tells the system, for a given CLSID, where the DLL or EXE code for that class is located and how it is to be launched.</span></span>

<span data-ttu-id="e3f16-106">Hay más de una manera de registrar una clase en el registro.</span><span class="sxs-lookup"><span data-stu-id="e3f16-106">There is more than one way of registering a class in the registry.</span></span> <span data-ttu-id="e3f16-107">Además, hay otras maneras de "registrar" una clase en el sistema cuando se está ejecutando, de modo que el sistema tenga en cuenta que un objeto en ejecución está actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e3f16-107">In addition, there are other ways of "registering" a class with the system when it is running, so that the system is aware that a running object is currently in the system.</span></span>

<span data-ttu-id="e3f16-108">Vea los temas siguientes para obtener más información acerca del registro:</span><span class="sxs-lookup"><span data-stu-id="e3f16-108">See the following topics for more information about registering:</span></span>

-   [<span data-ttu-id="e3f16-109">Registrar una clase durante la instalación</span><span class="sxs-lookup"><span data-stu-id="e3f16-109">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
-   [<span data-ttu-id="e3f16-110">Registrar un servidor EXE en ejecución</span><span class="sxs-lookup"><span data-stu-id="e3f16-110">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
-   [<span data-ttu-id="e3f16-111">Registrar objetos en la tabla ROT</span><span class="sxs-lookup"><span data-stu-id="e3f16-111">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
-   [<span data-ttu-id="e3f16-112">Registro automático</span><span class="sxs-lookup"><span data-stu-id="e3f16-112">Self-Registration</span></span>](self-registration.md)
-   [<span data-ttu-id="e3f16-113">Instalar como una aplicación de servicio</span><span class="sxs-lookup"><span data-stu-id="e3f16-113">Installing as a Service Application</span></span>](installing-as-a-service-application.md)

## <a name="related-topics"></a><span data-ttu-id="e3f16-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3f16-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3f16-115">Responsabilidades del servidor COM</span><span class="sxs-lookup"><span data-stu-id="e3f16-115">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 