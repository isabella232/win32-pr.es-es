---
title: Registro de aplicaciones COM
description: Registro de aplicaciones COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357555"
---
# <a name="registering-com-applications"></a><span data-ttu-id="13f57-103">Registro de aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="13f57-103">Registering COM Applications</span></span>

<span data-ttu-id="13f57-104">El registro es una base de datos del sistema que contiene información acerca de la configuración del hardware y el software del sistema, así como sobre los usuarios del sistema.</span><span class="sxs-lookup"><span data-stu-id="13f57-104">The registry is a system database that contains information about the configuration of system hardware and software as well as about users of the system.</span></span> <span data-ttu-id="13f57-105">Cualquier programa basado en Windows puede agregar información al registro y leer información del registro.</span><span class="sxs-lookup"><span data-stu-id="13f57-105">Any Windows-based program can add information to the registry and read information back from the registry.</span></span> <span data-ttu-id="13f57-106">Los clientes buscan en el registro los componentes interesantes que se van a usar.</span><span class="sxs-lookup"><span data-stu-id="13f57-106">Clients search the registry for interesting components to use.</span></span>

<span data-ttu-id="13f57-107">El registro mantiene información acerca de todos los objetos COM instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="13f57-107">The registry maintains information about all the COM objects installed in the system.</span></span> <span data-ttu-id="13f57-108">Cada vez que una aplicación crea una instancia de un componente COM, se consulta el registro para resolver el CLSID o ProgID del componente en el directorio del archivo DLL o EXE del servidor que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="13f57-108">Whenever an application creates an instance of a COM component, the registry is consulted to resolve either the CLSID or ProgID of the component into the pathname of the server DLL or EXE that contains it.</span></span> <span data-ttu-id="13f57-109">Después de determinar el servidor del componente, Windows carga el servidor en el espacio de proceso de la aplicación cliente (componentes en proceso) o inicia el servidor en su propio espacio de proceso (servidores locales y remotos).</span><span class="sxs-lookup"><span data-stu-id="13f57-109">After determining the component's server, Windows either loads the server into the process space of the client application (in-process components) or starts the server in its own process space (local and remote servers).</span></span> <span data-ttu-id="13f57-110">El servidor crea una instancia del componente y devuelve al cliente una referencia a una de las interfaces del componente.</span><span class="sxs-lookup"><span data-stu-id="13f57-110">The server creates an instance of the component and returns to the client a reference to one of the component's interfaces.</span></span>

<span data-ttu-id="13f57-111">Para obtener más información sobre el registro de Windows, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="13f57-111">For more information about the Windows registry, see the following topics:</span></span>

-   [<span data-ttu-id="13f57-112">Jerarquía del registro</span><span class="sxs-lookup"><span data-stu-id="13f57-112">Registry Hierarchy</span></span>](registry-hierarchy.md)
-   [<span data-ttu-id="13f57-113">Clases y servidores</span><span class="sxs-lookup"><span data-stu-id="13f57-113">Classes and Servers</span></span>](classes-and-servers.md)
-   [<span data-ttu-id="13f57-114">Clasificar componentes</span><span class="sxs-lookup"><span data-stu-id="13f57-114">Classifying Components</span></span>](classifying-components.md)
-   [<span data-ttu-id="13f57-115">Usar OleView</span><span class="sxs-lookup"><span data-stu-id="13f57-115">Using OleView</span></span>](using-oleview.md)
-   [<span data-ttu-id="13f57-116">Registrar componentes</span><span class="sxs-lookup"><span data-stu-id="13f57-116">Registering Components</span></span>](registering-components.md)
-   [<span data-ttu-id="13f57-117">Comprobando registro</span><span class="sxs-lookup"><span data-stu-id="13f57-117">Checking Registration</span></span>](checking-registration.md)
-   [<span data-ttu-id="13f57-118">Tipos de usuarios desconocidos</span><span class="sxs-lookup"><span data-stu-id="13f57-118">Unknown User Types</span></span>](unknown-user-types.md)
-   [<span data-ttu-id="13f57-119">Claves del registro COM</span><span class="sxs-lookup"><span data-stu-id="13f57-119">COM Registry Keys</span></span>](com-registry-keys.md)

 

 




